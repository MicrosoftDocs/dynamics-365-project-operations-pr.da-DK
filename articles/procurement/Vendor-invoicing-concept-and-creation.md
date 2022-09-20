---
title: Oprette leverandørfakturaer
description: I denne artikel beskrives begrebet leverandørfakturaer, og hvordan du kan oprette dem i Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475410"
---
# <a name="create-vendor-invoices"></a>Oprette leverandørfakturaer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Hvis du vil bruge den funktion, der er beskrevet i denne artikel, skal du aktivere funktionen **Aktivér faktiske underleverandører for Project Operations for ressourcebaserede scenarier** i arbejdsområdet **Funktionsadministration**.

Fakturering af leverandører i Microsoft Dynamics 365 Project Operations kan bruges til at registrere omkostninger fra leveringer af tjenester og/eller materialer på et projekt, der er fuldført efter leverandører.

Når tjenester og/eller materialer udbydes til en underleverandør, repræsenterer en underentreprise den kontraktmæssige aftale med den pågældende leverandør. Når leverandøren leverer tjenesten, eller materialerne modtages og bruges på projektopgaver, registreres omkostningerne for projektet. Leverandøren sender derefter jævnligt fakturaer. Disse fakturaer er kontrolleret og sammenholdt med de omkostninger, der er registreret for projektet. Når bekræftelsesprocessen er fuldført, bekræftes og frigives leverandørfakturaen til betaling.

## <a name="scenarios-for-use"></a>Scenarier for brug

Leverandørfakturaer i Project Operations kan bruges til at understøtte to separate scenarier:

- Kunder bruger alle erfaringer med underleverandører.
- Kunder bruger ikke alle erfaringer fra underleverandører, men vil have et ensartet billede af omkostningerne til projekter i Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kunder bruger alle erfaringer med underleverandører

Erfaringer med leverandørfakturaer gør det muligt at kontrollere og tilpasse tidsposter, materialeforbrug og udgifter, som refererer til komponenter fra underleverandører og matcher dem med leverandørfakturalinjer. Denne proces kan bruges til at kontrollere, om leverandørfakturalinjerne er korrekte. Når verifikationsprocessen er fuldført, og leverandørfakturaen er bekræftet, modposteres de faktiske værdier, der blev registreret ved hjælp af godkendte tids-, udgifts- og materialeforbrugslogfiler, og der oprettes nye faktiske omkostninger ved hjælp af leverandørfakturalinjer.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kunder bruger ikke alle erfaringer fra underleverandører, men vil have et ensartet billede af omkostningerne til projekter i Project Operations

Hvis du sporer underentrepriseprocessen i et tredjepartssystem, kan du registrere omkostninger fra det pågældende tredjepartssystem i Project Operations ved at oprette leverandørfakturaer, der ikke refererer til underentrepriser. På denne måde kan dine projektledere få én samlet visning af alle omkostninger for et bestemt projekt.

## <a name="create-vendor-invoices-in-project-operations"></a>Oprette leverandørfakturaer i Project Operations

Leverandørfakturaer oprettes i Dynamics 365 Finance ved hjælp af modulet **Kreditor**. Du kan ikke oprette leverandørfakturaer direkte i Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Konfigurere bekræftelse af leverandørfakturaer

Hvis leverandørens faktura er beregnet til en underleverandør i Dataverse, skal du aktivere parameteren **Manuel bekræftelse fra PM er påkrævet**. Indstillingen bestemmer, om leverandørfakturaen automatisk skal bekræftes i Dataverse, eller om den skal bekræftes manuelt. Overskriften på alle projektleverandørfakturaer indeholder en indstilling med samme navn. Indstillingen i overskriften på alle projektleverandørfakturaer er som standard angivet til den værdi, du angiver her. Du kan dog opdatere værdien efter behov i overskriften på de enkelte leverandørfakturaer.

Hvis indstillingen er angivet til **Ja**, har den leverandørfaktura, der er oprettet i Finance og synkroniseret til Dataverse, statussen **Kladde**. Fakturaen skal derefter valideres og godkendes af projektlederen og bekræftes, inden den behandles og sendes til de specifikke projekt- og finanskonti i Finance.

Hvis indstillingen er angivet til **Nej**, bekræftes leverandørfakturaen automatisk. Ingen yderligere handling er nødvendig.

Benyt følgende fremgangsmåde for at konfigurere bekræftelse af leverandørfakturaer.

1. Gå i Finance til **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.
1. Angiv indstillingen **Manuel bekræftelse fra PM er påkrævet** til **Ja** under fanen **Finansiel**, hvis firmapolitikken kræver bekræftelse af underleverandørs leverandørfakturaer. Hvis bekræftelse fra projektlederen ikke er påkrævet i Dataverse, skal du lade den grupperede indstilling være **Nej**. Indstillingen bruges som standard på siden **Afventende leverandørfaktura**.

> [!NOTE]
> Leverandørfakturaer, der er oprettet til underleverandører i Dataverse, kan kun behandles korrekt, hvis indstillingen **Manuel bekræftelse fra PM er påkrævet** er angivet til **Ja**. Faktiske omkostninger for tid, materiale og udgifter, som underleverandører opretter, kan kun sammenholdes manuelt med fakturalinjer for leverandører af projektlederen, hvis indstillingen er angivet til **Ja**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Konfigurere en integrationskonto til indkøb for leverandørfakturaer

Når en leverandørfaktura bogføres i Finance til Project Operations – Integreret miljø (ikke-lager), bogføres økonomi i indkøbsintegrationskontoen. De faktiske værdier genereres af systemet o Dataverse for den bogførte faktura. Disse faktiske tal bogføres i Finance ved hjælp af projektintegrationskladden. Når du bogfører projektintegrationskladden, bogføres den faktiske omkostning, og indkøbsintegrationskontoen tilbageføres.

Konfigurer en integrationskonto til indkøb for leverandørfakturaer ved at følge disse trin.

1. Gå i Finance til **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.
1. Under fanen **Project Operations på Dynamics 365 Customer Engagement** skal du vælge **Materialer** \> **Indkøbsintegrationskonto**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Oprette og bogføre leverandørfakturaer for underentreprise

Når en kreditorbogholder modtager en faktura fra underleverandøren, oprettes der en ny faktura i Finance.

1. Gå i Finance til **Kreditor** \> **Fakturaer** \> **Ventende kreditorfakturaer**.
1. Vælg **Ny** i **handlingsruden** for at oprette en leverandørfaktura.
1. Vælg **Underleverandør** i feltet **Fakturakonto** i fakturaoverskriften.
1. Vælg fakturadatoen.
1. Angiv indstillingen **Manuel bekræftelse fra PM er påkrævet** til **Ja** under fanen **Overskrift**. Standardindstillingen kommer fra siden **Parametre for projektstyring og regnskab**. Den kan dog ændres på leverandørfakturaniveau.
1. Vælg **Tilføj linje** i oversigtspanelet **Fakturalinje** for at oprette en leverandørfakturalinje.
1. Vælg den indkøbskategori, der blev oprettet for underleverandørlinjer, og angiv enhedspris, måleenhed og antal.
1. Vælg det projekt, som underleverandøren deler underleverandørfakturaen med, under fanen **Projekt** i sektionen med leverandørfakturalinjer.
1. Vælg projektkategorien. Det kan være af typen **Vare**, **Udgift**, **Materiale** eller **Timer**.
1. Vælg kun rollen, hvis den valgte projektkategori er af typen **Time**.
1. Vælg **Bogfør** for at bogføre leverandørfakturaen.

Du kan også oprette en leverandørfaktura ved at gå til **Kreditor** \> **Fakturaer** \> **Åbne leverandørfakturaer** og vælge **Ny**.

Når leverandørens faktura bogføres, bliver den tilgængelig i Dataverse til bekræftelse og behandling af projektlederen.

## <a name="vendor-invoice-processing-in-dataverse"></a>Leverandørfakturabehandling i Dataverse

På den leverandørfaktura, der oprettes i Dataverse, kommer nogle feltværdier fra den leverandørfaktura, der er registreret i Finance. Andre værdier er standardværdier, der kommer fra underleverandøren.

Følgende felter og relaterede poster kopieres fra underentreprisen til overskriften på leverandørfakturaen:

- Valuta
- Kontraktenhed
- Betalingsbetingelser

I Project Operations bruges følgende feltværdier på fakturalinjerne for leverandøren til at angive standardlinjen i underentrepriseaftalen:

- Transaktionsklasse
- Rolle
- Transaktionskategori
- Produktfelter
- Project
- Opgave

> [!NOTE]
> Fastprislinjer i underentrepriseaftaler understøttes ikke i Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
