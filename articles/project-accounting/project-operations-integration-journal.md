---
title: Kladde til integration i Project Operations
description: Dette emne indeholder oplysninger om, hvordan du kan arbejde med kladden til integration i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a5f4d524530594bd3118f9b320acf4033c5d503
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948323"
---
# <a name="integration-journal-in-project-operations"></a>Kladde til integration i Project Operations

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Poster med tidsforbrug og udgifter opretter **Faktiske** transaktioner, som repræsenterer den operationelle visning af udfært arbejde i forhold til et projekt. Dynamics 365 Project Operations giver revisorer et værktøj til at revidere transaktioner og om nødvendigt justering af regnskabsattributter. Når gennemgangen og justeringerne er fuldført, bogføres transaktionerne i projektets underfinanskladde og finanskladde. En revisor kan udføre disse aktiviteter ved hjælp af kladden til **Integration af Project Operations** (**Dynamics 365 Finance** > **Projektstyring og regnskab** > **Kladder** > **Integration af Project Operations**).

![Flow for integration af kladde](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Opret poster i kladden til integration af Project Operations

Poster i kladden til integration af Project Operations oprettes ved hjælp af den periodiske proces **Importer fra den midlertidige tabel**. Du kan køre denne proces ved at gå til **Dynamics 365 Finance** > **Projektstyring og regnskab** > **Periodisk** > **Integration af Project Operations** > **Importer fra den midlertidige tabel**. Du kan køre processen interaktivt eller konfigurere processen til at køre i baggrunden efter behov.

Når den periodiske proces kører, findes der eventuelle faktiske værdier, der endnu ikke er føjet til kladden til integration af Project Operations. Der oprettes en kladdelinje for hver enkelt faktisk transaktion.
Systemet grupperer kladdelinjerne i separate kladder på basis af den valgte værdi i feltet **Periodeenhed i kladden for integration af Project Operations** (**Finance** > **Projektstyring og regnskab** > **Opsætning** > **Parametre for projektstyring og regnskab**, fanen **Project Operations på Dynamics 365 Customer Engagement**). De mulige værdier for dette felt omfatter:

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
    - Hvis **Transaktionskategorien** ikke er angivet i projektets faktiske værdi, bruger systemet værdien i feltet **Standardkategorier for projekt** på fanen **Project Operations på Dynamics 365 Customer Engagement** på siden **Parametre for projektstyring og regnskab**.
  - Feltet **Ressource** repræsenterer den projektressource, der er knyttet til denne transaktion. Ressourcen bruges som reference i projektfakturaforslag til kunder.
  - Feltet **Valutakurs** udfyldes som standard fra den **Valutakurser**, der er angivet i Dynamics 365 Finance. Hvis der mangler en valutakurskonfiguration, tilføjer den periodiske proces **Importer fra midlertidig** ikke posten til en kladde under importen, og der tilføjes en fejlmeddelelse til jobbets udførelseslog.
  - Feltet **Linjeegenskab** repræsenterer faktureringstypen i projektets faktiske værdier. Tilknytning af linjeegenskab og faktureringstype defineres på fanen **Project Operations på Dynamics 365 Customer Engagement** på siden **Parametre for projektstyring og regnskab**.

Det er kun følgende regnskabsattributter, der kan opdateres i integrationskladdelinjerne i Project Operations:

- **Faktureringsmomsgruppe** og **Faktureringsvaremomsgruppe**
- **Økonomiske dimensioner** (ved hjælp af handlingen **Fordel beløb**)

Integrationskladdelinjer kan slettes, men alle ikke-bogførte linjer indsættes igen i kladden, når du har kørt den periodiske proces **Importer fra midlertidig** på ny.

Når du bogfører integrationskladden, oprettes der en underfinanskonto for projektet og transaktioner på finanskontoen. Disse bruges til afledt kundefakturering, indtægtsføring og finansiel rapportering.


[!INCLUDE[footer-include](../includes/footer-banner.md)]