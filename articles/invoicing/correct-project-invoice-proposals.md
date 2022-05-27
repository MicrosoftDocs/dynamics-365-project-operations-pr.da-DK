---
title: Ret regnskabet på forslag til projektfakturakladder
description: I dette emne forklares det, hvordan du kan justere regnskabsrelaterede oplysninger i en fakturaforslagskladde.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575067"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Ret regnskabet på forslag til projektfakturakladder

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

*Driftsmæssige detaljer* for projektfakturaer vedligeholdes af projektlederen på en pro forma-faktura. Disse oplysninger omfatter beslutningen om de timer, udgifter, materiale eller milepæle, der skal faktureres, satserne og anvendelsen af forfalds- og tilbageholdelsesbeløb. Når du har bekræftet den oprindelige pro-forma-faktura, kan du justere de driftsmæssige detaljer ved at oprette og bekræfte en [korrigerende pro forma-faktura](../proforma-invoicing/corrective-invoices.md).

*Regnskabsdetaljer* for projektfakturaer vedligeholdes i et fakturadokument, der er rettet mod kunden. Disse oplysninger omfatter beregningen af moms og de økonomiske dimensioner, der anvendes på fakturaen. Dette emne tilvejebringer detaljer om, hvordan disse regnskabsdetaljer kan justeres i en projektfakturaforslagskladde.

## <a name="adjust-sales-tax"></a>Juster moms

Standardfaktureringsmomsgrupper og varesalgsmomsgrupper kan justeres direkte i fakturaforslagsdokumentet. Hvis du vil justere disse grupper, skal du vælge **Rediger** og derefter angive en ny værdi i feltet **Momsgruppe** eller **Varesalgsmomsgruppe** på alle projektfakturalinjer. 

## <a name="adjust-financial-dimensions"></a>Tilpas økonomiske dimensioner

### <a name="header-dimensions"></a>Overskriftsdimensioner

De økonomiske dimensioner i fakturaen er som standard afledt af de ikke-fakturerede projekttransaktionsposter, der faktureres. Med systemindstillingerne kan du dog bruge økonomiske dimensioner i overskriften på projektfakturaforslag til at bogføre kundesaldi. Hvis du vil aktivere denne funktion, skal du vælge **Tillad opdateringer af projektdimension for debitorer** på fanen **Finanser** på siden **Projektstyring og regnskabsparametre**.

Økonomiske dimensioner i fakturaoverskrifter kan redigeres, før en faktura sendes. På siden **Projektfakturaforslag** skal du gå til visningen **Overskrift** og derefter redigere værdier under fanen **Økonomiske dimensioner**.

Visningen **Overskrift** er først tilgængelig, når systemadministratoren aktiverer funktionen **Brug projektfakturaforslag og fakturakladdeformularer sammen med visning af overskrift og linjer** i arbejdsområder **Funktionsstyring**. Denne funktion kræver opdatering af Finance til 10.0.25 eller nyere.

### <a name="line-dimensions"></a>Linjedimensioner

Økonomiske dimensioner kan ikke redigeres direkte på en projektfakturaforslagslinje. Følg i stedet disse trin for at justere økonomiske dimensioner i et forslag til en projektfaktura.

1. Vælg **Slet alle** i projektfakturaforslaget for at fjerne projektfakturaforslagslinjerne.

    Knappen **Slet alle** er først tilgængelig, når systemadministrator aktiverer funktionen **Slet fakturaforslagslinjer ved brug af Project Operations til ressourcebaserede/ikke-lagerbaserede scenarier** i arbejdsområdet **Funktionsadministration**.

2. Tilpas de økonomiske dimensioner:

    - **Acontotransaktioner (faktureringsmilepæle):** Gå til **Alle projekter** \> **Administrer** \> **Acontotransaktioner**, og vælg den milepæl, der kræver tilpasning. Opdater derefter værdierne efter behov under fanen **Økonomiske dimensioner**.
    - **Tids-, udgifts- og materialetransaktioner:** På siden **Bogførte projekttransaktioner** skal du vælge **Tilpas regnskab** for at opdatere de økonomiske dimensioner.

3. Når du er færdig med at justere værdierne for den økonomiske dimension, skal du gå til **Projektstyring og regnskab** \> **Periodisk** \> **Integration af Project Operations** og vælge **Importér fra midlertidig tabel** for at køre den periodiske proces. I denne proces bruges de opdaterede værdier for den økonomiske dimension til at oprette projektfakturaforslagslinjerne igen. De opdaterede værdier bruges derefter i underkontiene og hovedbog for projektet, når projektfakturaen bogføres.
