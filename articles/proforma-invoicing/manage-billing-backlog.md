---
title: Administrer faktureringsefterslæb
description: Dette emne indeholder oplysninger om, hvordan du kan få vist og arbejde med faktureringsefterslæbet i Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e428b551a755220cee67d54b2e63dd7a3c2ca393
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866770"
---
# <a name="manage-billing-backlog"></a>Administrer faktureringsefterslæb

**Finder anvendelse på:** Project Operations til ressource-/ikke-lagerbaserede scenarier

Dynamics 365 Project Operations har visninger dedikeret til at hjælpe med at administrere efterslæbet af fakturering. Hvis du vil administrere faktureringsefterslæbet, skal du vælge de tilsvarende links i området **Salg** under **Fakturering**. 

Følgende visninger er tilgængelige:

- Forskudshonorarer og Forskud
- Forskudshonorarer og Forskud til rådighed
- Milepæle for fast pris
- Ordrebeholdning for fakturering af tid og materiale

## <a name="retainers-and-advances"></a>Forskudshonorarer og Forskud

Visningslisterne for **Forskud og forskudshonorarer** angiver forskud og forskudshonorarer på tværs af alle projektkontrakter. Når et forskudshonorar eller et forskud faktureres, bliver forskudsbeløbet tilgængeligt for brug.

## <a name="available-retainers-and-advances"></a>Forskudshonorarer og Forskud til rådighed

Visningslisterne for **Tilgængelige forskud og forskudshonorarer** angiver alle forskud og forskudshonorarer på tværs af alle projektkontrakter. Når et forskudshonorar eller et forskud faktureres, bliver forskudsbeløbet tilgængeligt for brug og tilføjes til listen. Når beløbet for forskud eller forskudshonorar er brugt fuldstændigt, fjernes den fra listen.

## <a name="fixed-price-milestones"></a>Milepæle for fast pris

Visningslisterne **Fastprismilepæle** indeholder alle faste prismilepæle på tværs af alle projektkontraktlinjer. Fra denne visning kan en eller flere milepæle markeres som **Klar til fakturering** eller **Ikke klar til fakturering**. Hvis du markerer en milepæl som **Klar til fakturering**, bliver den tilgængelig for anvendelse i en kladdefaktura.

Når kontraktlinjer med flere kunder har en metode med fast pris, oprettes der en milepæl for hver kunde på kontraktlinjen. Du kan oprette en milepæl og derefter dele den op i individuelle kundespecifikke milepælsposter. Denne opdeling er intern og i overensstemmelse med procenten for opdeling af fakturaen, som er defineret for de enkelte kunder på kontraktlinjen. Visningen **Milepæle med fast pris** viser dig de enkelte kundespecifikke milepælsposter. Hver af disse milepælsposter kan særskilt markeres som **Klar til fakturering** fra denne visning. Når en eller flere af de relaterede milepælsopdelinger er markeret som **Klar til fakturering**, opdateres statussen for overskriften til **I gang** fra **Ikke påbegyndt**. Når alle milepælsopdelinger faktureres, opdateres statussen for overskriftsmilepælen til **Fuldført**.

En milepæl på en kladdefaktura vises i denne visning med en faktureringsstatus angivet til **Kundefaktura oprettet**. Når kladdefakturaen er blevet bekræftet, opdateres postens faktureringsstatus til **Kundefaktura er bogført**. 

> [!NOTE] 
> Opdater ikke denne statusværdi ved hjælp af brugerdefineret kode. Project Operations fungerer ikke korrekt, når disse statusværdier opdateres med brugerdefineret kode.

## <a name="time-and-material-billing-backlog"></a>Ordrebeholdning for fakturering af tid og materiale

Visningen **Faktureringsefterslæb for tid og materialer** viser alle de ikke-fakturerede faktiske salgstal på tværs af alle projektkontrakter i systemet, som ikke er faktureret. Enkelte eller flere ikke-fakturerede faktiske salgsværdier kan markeres som **Klar til fakturering** eller **Ikke-klar til fakturering** fra denne visning. Hvis du markerer en ikke-faktureret faktisk salgsværdi som **Klar til fakturering**, bliver den tilgængelig til brug i en kladdefaktura.

Ikke-fakturerede faktiske salgstal med en status angivet til **Må ikke overskrides**, som er **Mislykket**, kan ikke markeres som **Klar til fakturering**. Hvis de faktiske tal skal markeres som **Klar til fakturering**, skal du nulstille statussen på andre faktiske tal på den kontraktlinje, der er bindende, og derefter evaluere statussen **Må ikke overskrides** igen.

Hvis der er tale om en faktureringsmetode for tid og materialer i forbindelse med kontraktlinjer med flere kunder, oprettes der en ikke-faktureret faktisk salgsværdi for hver kunde på kontraktlinjen i henhold til den faktureringsprocentsats, der er defineret for hver enkelt kunde. Visningen **Faktureringsefterslæb for tid og materialer** kan du se de enkelte kundespecifikke ikke-fakturerede faktiske salgsværdier. Hver af disse ikke-fakturerede faktiske salgsposter kan særskilt markeres som **Klar til fakturering** fra denne visning.

En ikke-faktureret faktiske salgsværdi, som findes på en fakturakladde, fremgår i denne visning med faktureringsstatussen **Kundefaktura oprettet**. Når kladdefakturaen er bekræftet, opdateres faktureringsstatussen for denne post til **Kundefaktura er bogført**. 

> [!NOTE] 
> Opdater ikke denne statusværdi ved hjælp af brugerdefineret kode. Project Operations fungerer ikke korrekt, når disse statusværdier opdateres med brugerdefineret kode.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
