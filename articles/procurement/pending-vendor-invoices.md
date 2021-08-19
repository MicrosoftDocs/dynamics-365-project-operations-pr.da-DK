---
title: Køb ikke-lagerførte materialer ved hjælp af en afventende leverandørfaktura
description: I dette emne forklares det, hvordan afventende leverandørfakturaer registreres.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009029"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Køb ikke-lagerførte materialer ved hjælp af en afventende leverandørfaktura

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når en virksomhed anskaffer ikke-lagerførte materialer til et projekt, kan omkostningerne straks registreres i forhold til projektet. 

Som eksempel kan nævnes Contoso Robotics US, der udfører et udstyrsfornyelsesprojekt og har brug for softwarelicenser. Disse licenser indkøbes fra en tredjepartsleverandør.  Ved hjælp af Dynamics 365 Finance kan kreditormedarbejderen registrere et afventende fakturadokument for leverandøren, og tildele licensomkostningerne direkte på udstyrsfornyelsesprojektet. 

> [!IMPORTANT]
> Før du bruger den funktion, der er beskrevet i dette emne, skal du gennemse og anvende de påkrævede konfigurationer. Du kan finde flere oplysninger i [Aktiver ikke-lagerførte materialer og afventende leverandørfakturaer](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Bogfør en projektrelateret afventende leverandørfaktura 

Afventende leverandørfakturaer kan registreres på siden **Afventende leverandørfakturaer** (**Kreditor** > **Fakturaer** > **Afventende leverandørfakturaer**). Udfør følgende trin for at bogføre en projektrelateret afventende leverandørfaktura:

1. Gå til **Kreditor** > **Fakturaer**, og vælg **Ny**. 
2. I feltet **Fakturakonto** skal du vælge en leverandør, og i feltet **Nummer** skal du angive leverandørens fakturaidentifikation.
3. Tilføj en linje til leverandørens faktura, og vælg i feltet **Varenummer** den ikke-lagerførte vare, der er købt hos leverandøren. 

    > [!NOTE]
    > Leverandørfakturalinjer, der er baseret på en indkøbskategori, kan ikke registreres i forhold til projektet. 
    
5. Tilføj det købte antal. Enhedsprisen udfyldes automatisk af systemet på basis af den ikke-lagerførte varepriskonfiguration. 
6. Kontrollér det samlede beløb og andre påkrævede oplysninger på linjen.
7. På linjedetaljerne skal du på fanen **Projekt** vælge det projekt-id, som denne vare vil blive registreret på.
8. Du kan også vælge aktivitetsnummeret og opdatere projektkategorien og linjeegenskaben.
9. Bogfør afventende leverandørfakturaer. Når fakturaen er bogført, registrerer systemet følgende:
    
    - Leverandørens saldobeløb.
    - Momsbeløbet.
    - Omkostningen i forhold til projektet registreres for indkøbsintegrationskontoen.
    - Den faktiske projekttransaktion i Dataverse. Transaktionen behandles yderligere ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md). Når du bogfører denne kladde, flyttes beløbet fra indkøbsintegrationskontoen til projektomkostningskontoen.
