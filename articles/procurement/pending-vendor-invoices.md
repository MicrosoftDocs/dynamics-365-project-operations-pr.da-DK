---
title: Indkøb af ikke-lagerførte materialer eller indkøbskategorier ved hjælp af en afventende leverandørfaktura
description: I dette emne forklares det, hvordan afventende leverandørfakturaer registreres.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612650"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Indkøb af ikke-lagerførte materialer eller indkøbskategorier ved hjælp af en afventende leverandørfaktura

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når en virksomhed indkøber ikke-lagerførte materialer eller indkøbskategorier til et projekt, kan omkostningerne registreres direkte på projektet. 

Contoso Robotics USA er f.eks. i gang med at udføre et projekt til fornyelse af udstyr, og der skal bruges softwarelicenser. Disse licenser indkøbes fra en tredjepartsleverandør.  Ved hjælp af Dynamics 365 Finance registrerer debitormedarbejderen et afventende leverandørfakturadokument og tilskriver licensomkostningerne direkte på projektet til fornyelse af udstyr. 

> [!IMPORTANT]
> Før du bruger den funktion, der er beskrevet i dette emne, skal du gennemse og anvende de påkrævede konfigurationer. Du kan finde flere oplysninger i [Aktiver ikke-lagerbaserede materialer og afventende leverandørfakturaer](configure-materials-nonstocked.md) og [Brug indkøbskategorier sammen med projektkøbsordre og afventende leverandørfakturaer](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Bogfør en projektrelateret afventende leverandørfaktura 

Afventende leverandørfakturaer kan registreres på siden **Afventende leverandørfakturaer** (**Kreditor** > **Fakturaer** > **Afventende leverandørfakturaer**). Udfør følgende trin for at bogføre en projektrelateret afventende leverandørfaktura:

1. Gå til **Kreditor** > **Fakturaer**, og vælg **Ny**. 
1. I feltet **Leverandørkonto** skal du vælge en leverandør og derefter angive leverandørfakturaens identifikation i feltet **Nummer**.
1. Tilføj en linje til leverandørfakturaen, og vælg derefter i feltet **Varenummer** den ikke-lagerførte vare, der er indkøbt hos leverandøren. Du kan også i feltet **Indkøbskategori** vælge den kategori, der blev købt fra leverandøren.   
1. Tilføj den købte mængde. Enhedsprisen udfyldes automatisk af systemet på grundlag af den ikke-lagerbaserede varepriskonfiguration. 
1. Kontrollér det samlede beløb og andre påkrævede oplysninger på linjen.
1. Vælg id'et for det projekt, som dette element skal registreres i, under fanen **Projekt** i linjedetaljerne.
1. Valgfrit: Vælg aktivitetsnummeret, og opdater projektkategorien og linjeegenskaben.
1. Bogfør den afvendte leverandørfaktura. Når fakturaen er bogført, registrerer systemet følgende oplysninger:
    
    - Leverandørens saldobeløb.
    - Momsbeløbet.
    - Omkostningen i forhold til projektet registreres for indkøbsintegrationskontoen.
    - Projekttransaktionen med faktiske omkostninger i Dataverse.  Transaktionen behandles yderligere ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md). Når du bogfører denne kladde, flyttes beløbet fra indkøbsintegrationskontoen til projektomkostningskontoen. 
    - Køb, der faktureres til projektkunden ved hjælp af tids- og materialefaktureringsmetoden. Derudover oprettes der ikke-fakturerede salgstransaktioner for indkøbene i Dataverse. Produktprislisten i Dataverse bruges til salgspriser og beløb for ikke-faktureret salgstransaktion.
