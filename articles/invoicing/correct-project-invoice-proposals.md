---
title: Ret regnskabet på forslag til projektfakturakladder
description: I dette emne forklares det, hvordan du kan justere regnskabsrelaterede oplysninger i en fakturaforslagskladde.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251195"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Ret regnskabet på forslag til projektfakturakladder

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

*Driftsmæssige detaljer* for projektfakturaer vedligeholdes af projektlederen på en pro forma-faktura. Disse oplysninger omfatter beslutningen om de timer, udgifter, materiale eller milepæle, der skal faktureres, satserne og anvendelsen af forfalds- og tilbageholdelsesbeløb. Når du har bekræftet den oprindelige pro-forma-faktura, kan du justere de driftsmæssige detaljer ved at oprette og bekræfte en [korrigerende pro forma-faktura](../proforma-invoicing/corrective-invoices.md).

*Regnskabsdetaljer* for projektfakturaer vedligeholdes i et fakturadokument, der er rettet mod kunden. Disse oplysninger omfatter beregningen af moms og de økonomiske dimensioner, der anvendes på fakturaen. Dette emne tilvejebringer detaljer om, hvordan disse regnskabsdetaljer kan justeres i en projektfakturaforslagskladde.

## <a name="adjust-sales-tax"></a>Juster moms

Standardfaktureringsmomsgrupper og varesalgsmomsgrupper kan justeres direkte i fakturaforslagsdokumentet. Hvis du vil justere disse grupper, skal du vælge **Rediger** og derefter angive en ny værdi i feltet **Momsgruppe** eller **Varesalgsmomsgruppe** på alle projektfakturalinjer. 

## <a name="adjust-financial-dimensions"></a>Tilpas økonomiske dimensioner

Økonomiske dimensioner kan ikke redigeres direkte på en projektfakturaforslagslinje. Følg i stedet disse trin for at justere økonomiske dimensioner i et forslag til en projektfaktura.

1. Vælg **Slet alle** i projektfakturaforslaget for at fjerne projektfakturaforslagslinjerne.

    > [!NOTE]
    > Knappen **Slet alle** er først tilgængelig, når systemadministrator aktiverer funktionen **Slet fakturaforslagslinjer ved brug af Project Operations til ressourcebaserede/ikke-lagerbaserede scenarier** i arbejdsområdet **Funktionsadministration**.

2. Tilpas de økonomiske dimensioner:

    - **Acontotransaktioner (faktureringsmilepæle):** Gå til **Alle projekter** \> **Administrer** \> **Acontotransaktioner**, og vælg den milepæl, der kræver tilpasning. Opdater derefter værdierne efter behov under fanen **Økonomiske dimensioner**.
    - **Tids-, udgifts- og materialetransaktioner:** På siden **Bogførte projekttransaktioner** skal du vælge **Tilpas regnskab** for at opdatere de økonomiske dimensioner.

3. Når du er færdig med at justere værdierne for den økonomiske dimension, skal du gå til **Projektstyring og regnskab** \> **Periodisk** \> **Integration af Project Operations** og vælge **Importér fra midlertidig tabel** for at køre den periodiske proces. I denne proces bruges de opdaterede værdier for den økonomiske dimension til at oprette projektfakturaforslagslinjerne igen. De opdaterede værdier bruges derefter i underkontiene og hovedbog for projektet, når projektfakturaen bogføres.
