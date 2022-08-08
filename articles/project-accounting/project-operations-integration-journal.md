---
title: Kladde til integration i Project Operations
description: Denne artikel indeholder oplysninger om, hvordan du arbejder med integrationskladden i Project Operations.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106268"
---
# <a name="integration-journal-in-project-operations"></a>Kladde til integration i Project Operations

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Poster med tidsforbrug, udgifter, gebyrer og materialer opretter **Faktiske** transaktioner, som repræsenterer den operationelle visning af færdiggjort arbejde i forhold til et projekt. Dynamics 365 Project Operations giver revisorer et værktøj til at revidere transaktioner og om nødvendigt justering af regnskabsattributter. Når gennemgangen og justeringerne er fuldført, bogføres transaktionerne i projektets underfinanskladde og finanskladde. En revisor kan udføre disse aktiviteter ved hjælp af kladden **Project Operations-integration** (**Dynamics 365 Finance** > **Projektstyring og regnskab** > **Kladder** > **Project Operations-integration**.

![Flow for integration af kladde.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Opret poster i kladden til integration af Project Operations

Poster i kladden til integration af Project Operations oprettes ved hjælp af den periodiske proces **Importer fra den midlertidige tabel**. Du kan køre denne proces ved at gå til **Dynamics 365 Finance** > **Projektstyring og regnskab** > **Periodisk** > **Project Operations-integration** > **Import fra den midlertidige tabel**. Du kan køre processen interaktivt eller konfigurere processen til at køre i baggrunden efter behov.

Når den periodiske proces kører, findes der eventuelle faktiske værdier, der endnu ikke er føjet til kladden til integration af Project Operations. Der oprettes en kladdelinje for hver enkelt faktisk transaktion.
Systemet grupperer kladdelinjer i separate kladder baseret på den værdi, der er valgt i feltet **Periodeenhed i Project Operations-integrationskladde** (**Finance** > **Projektstyring og regnskab** > **Konfiguration** > **Projektstyrings- og regnskabsparametre**, **Project Operations på fanen Dynamics 365 Customer Engagement**). De mulige værdier for dette felt omfatter:

  - **Dage**: De faktiske værdier er grupperet efter transaktionsdato. Der oprettes en separat kladde for hver dag.
  - **Måneder**: De faktiske værdier er grupperet efter kalendermåned. Der oprettes en separat kladde for hver måned.
  - **År**: De faktiske værdier er grupperet efter kalenderår. Der oprettes en separat kladde for hvert år.
  - **Alle**: Alle de faktiske transaktioner inkluderes i den samme integrationskladde. Hvis kladden ikke er tilgængelig, når den periodiske proces kører, f.eks. hvis kladden er i gang med at bogføre transaktioner, oprettes der en ny kladde.

Kladdelinjer oprettes på baggrund af de faktiske projektoplysninger. Følgende liste indeholder nogle af de mere bemærkelsesværdige regler for standarder og transformation:

  - Hver enkelt faktisk projekttransaktion indeholder en linje i integrationskladden til Project Operations. Omkostnings- og ikke-fakturerede salgstransaktioner for faktureringstypen tid og materialer vises på separate linjer.
  - Feltet **Dato** repræsenterer datoen for transaktionen. Feltet **Regnskabsdato** repræsenterer den dato, hvor transaktionen registreres i hovedbogen. Hvis regnskabsdatoen er i en [afsluttet regnskabsperiode](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), og den pågældende parameter **Automatisk indstiller regnskabsdato til den åbne hovedbogsperiode** angives under fanen **Finans** på siden med **Parametrene for projektstyring og regnskab**, vil systemet tilpasse regnskabsdatoen for transaktionen til den første dato i den næste åbne hovedbogsperiode.
  - Feltet **Bilag** viser bilagsnummeret for alle faktiske transaktioner. Bilagsnummerserien defineres under fanen **Nummerserier** på siden **Parametre for projektstyring og regnskab**. Hver linje tildeles et nyt nummer. Når bilaget er bogført, kan du se, hvordan omkostninger og ikke-faktureret salgstransaktion relateres, ved at vælge **Relaterede bilag** på siden **Bilagstransaktion**.
  - Feltet **Kategori** repræsenterer en projekttransaktioner og standarder, der er baseret på transaktionskategorien for den relaterede faktiske projektværdi.
    - Hvis **Transaktionskategorien** er angivet i projektets faktiske værdi, og der findes en relateret **Projektkategori** i en bestemt juridisk enhed, bruges denne projektkategori som standard.
    - Hvis **Transaktionskategorien** ikke er angivet i de faktiske projektværdier, bruger systemet værdien i feltet **Projektkategoristandarder** under fanen **Project Operations på Dynamics 365 Customer Engagement** på siden **Projektstyrings- og regnskabsparametre**.
  - Feltet **Ressource** repræsenterer den projektressource, der er knyttet til denne transaktion. Ressourcen bruges som reference i projektfakturaforslag til kunder.
  - Feltet **Valutakurser** bruges som standard ud fra den **Valutakurs**, der er angivet i Dynamics 365 Finance. Hvis der mangler en valutakurskonfiguration, tilføjer den periodiske proces **Importer fra midlertidig** ikke posten til en kladde under importen, og der tilføjes en fejlmeddelelse til jobbets udførelseslog.
  - Feltet **Linjeegenskab** repræsenterer faktureringstypen i projektets faktiske værdier. Tilknytning af linjeegenskab og faktureringstype defineres under fanen **Project Operations på fanen Dynamics 365 Customer Engagement** på siden **Projektstyrings- og regnskabsparametre**.

Det er kun følgende regnskabsattributter, der kan opdateres i integrationskladdelinjerne i Project Operations:

- **Faktureringsmomsgruppe** og **Faktureringsvaremomsgruppe**
- **Økonomiske dimensioner** (ved hjælp af handlingen **Fordel beløb**)

Integrationskladdelinjer kan slettes. Alle ikke-bogførte linjer indsættes dog i kladden igen, når du har kørt den periodiske proces **Importér fra midlertidig** på ny.

### <a name="post-the-project-operations-integration-journal"></a>Bogfør integrationskladden til Project Operations

Når du bogfører integrationskladden, oprettes der en underfinanskonto for projektet og transaktioner på finanskontoen. Disse bruges til afledt kundefakturering, indtægtsføring og finansiel rapportering.

Den valgte integrationskladde til Project Operations kan udgives ved hjælp af **Bogfør** på siden for integrationskladden for Project Operations. Alle kladder kan automatisk bogføres ved at køre en proces på **Periodiske** > **Project Operations-integration** > **Bogfør integrationskladden til Project Operations**.

Bogføring kan udføres interaktivt eller i en batch. Bemærk, at alle kladder, der har mere end 100 linjer, automatisk bliver bogført i en batch. Hvis du vil opnå en bedre ydeevne, når du bogfører kladder med mange linjer i en batch, skal du aktivere funktionen **integrationskladden til Project Operations ved hjælp af flere batchopgaver** i arbejdsområdet **Funktionsstyring**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Overfør alle linjer, der indeholder bogføringsfejl til en ny kladde

> [!NOTE]
> Hvis du vil bruge denne funktion, skal du aktivere funktionen **Overførelse af alle linjer med bogføringsføringsfejl til en ny integrationskladde i Project Operations** i arbejdsområdet **Funktionsstyring**.

Under bogføring til integrationskladden til Project Operations validerer systemet alle linjer i kladden. Systemet bogfører alle linjer, der ikke indeholder fejl, og opretter en ny kladde for alle linjer med bogføringsfejl. Hvis du vil gennemgå kladderne med bogføringsfejl, skal du gå til **Projektstyring og regnskab** > **Kladder** > **Integrationskladde til Project Operations** og filtrere kladderne ved hjælp af feltet **Oprindelig kladde**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
