---
title: Administrer faktureringsefterslæbet - lille
description: Dette emne indeholder oplysninger om de forskellige visninger, der er tilgængelige til brug i forbindelse med administration af faktureringsefterslæbet.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e3ca167fa53a6923727eff3e7c34c8706dc7455
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176964"
---
# <a name="manage-the-billing-backlog---lite"></a>Administrer faktureringsefterslæbet - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dynamics 365 Project Operations har dedikerede visninger, der kan hjælpe dig med at administrere faktureringsefterslæbet. Hvis du vil administrere faktureringsefterslæbet, skal du vælge de tilsvarende links i området **Salg** under **Fakturering**. 

Følgende visninger er tilgængelige:

- Forskudshonorarer og Forskud
- Forskudshonorarer og Forskud til rådighed
- Milepæle for fast pris
- Ordrebeholdning for produktfakturering
- Ordrebeholdning for fakturering af tid og materiale

## <a name="retainers-and-advances"></a>Forskudshonorarer og Forskud

Visningen **Forskudshonorarer og forskud** viser alle forskudshonorarer og forskud på tværs af alle projektkontrakter i systemet. Når et forskudshonorar eller et forskud faktureres, bliver forskudsbeløbet tilgængeligt for brug.

## <a name="available-retainers-and-advances"></a>Forskudshonorarer og Forskud til rådighed

Visningen **Tilgængelige forskudshonorarer og forskud** viser alle tilgængelige forskudshonorarer og forskud på tværs af alle projektkontrakter i systemet. Når et forskudshonorar eller et forskud faktureres, bliver forskudsbeløbet tilgængeligt for brug og tilføjes til listen. Når hele beløbet for forskudshonoraret eller forskuddet er blevet brugt, fjernes det fra listen.

## <a name="fixed-price-milestones"></a>Milepæle for fast pris

Visningen **Milepæle med faste priser** viser en liste over alle milepæle med fast pris på tværs af alle projektkontraktlinjer i systemet. Enkelte eller flere milepæle kan markeres som **Klar til fakturering** eller **Ikke klar til fakturering** fra denne visning. Hvis du markerer en milepæl som **Klar til fakturering**, bliver den tilgængelig for anvendelse i en kladdefaktura.

Når kontraktlinjer med flere kunder har en metode med fast pris, oprettes der en milepæl for hver kunde på kontraktlinjen. Du kan oprette en milepæl og derefter dele den op i individuelle kundespecifikke milepælsposter. Denne opdeling er intern og i overensstemmelse med procenten for opdeling af fakturaen, som er defineret for de enkelte kunder på kontraktlinjen. Visningen **Milepæle med fast pris** viser dig de enkelte kundespecifikke milepælsposter. Hver af disse milepælsposter kan særskilt markeres som **Klar til fakturering** fra denne visning. Når en eller flere af de relaterede milepælsopdelinger er markeret som **Klar til fakturering**, opdateres overskriftens status til **I gang** fra **Ikke påbegyndt**. Når alle milepælsopdelingerne er blev faktureret, opdateres statussen for milepælens overskrift til **Fuldført**.

En milepæl på en kladdefaktura vises i denne visning med en faktureringsstatus angivet til **Kundefaktura oprettet**. Når kladdefakturaen er blevet bekræftet, opdateres postens faktureringsstatus til **Kundefaktura er bogført**. Opdater ikke denne statusværdi ved hjælp af brugerdefineret kode. Project Operations fungerer ikke korrekt, når disse statusværdier opdateres med brugerdefineret kode.

## <a name="product-billing-backlog"></a>Ordrebeholdning for produktfakturering

Visningen **Faktureringsefterslæb for produkt** viser alle produktbaserede kontraktlinjer på tværs af alle projektkontrakter i systemet. Enkelte eller flere produktbaserede kontraktlinjer kan markeres som **Klar til fakturering** eller **Ikke klar til fakturering** fra denne visning. Hvis du markerer en produktbaseret kontraktlinje som **Klar til fakturering**, bliver den tilgængelig for anvendelse i en kladdefaktura.

Der vises i denne visning en produktbaseret kontraktlinje, der er på en kladdefaktura, med en faktureringsstatus **Kundefaktura oprettet**. Når kladdefakturaen er bekræftet, opdateres faktureringsstatussen for denne post til **Kundefaktura er bogført**. Opdater ikke denne statusværdi ved hjælp af brugerdefineret kode. Project Operations fungerer ikke korrekt, når disse statusværdier opdateres med brugerdefineret kode.

## <a name="time-and-material-billing-backlog"></a>Ordrebeholdning for fakturering af tid og materiale

Visningen **Faktureringsefterslæb for tid og materialer** viser alle de ikke-fakturerede faktiske salgstal på tværs af alle projektkontrakter i systemet, som ikke er faktureret. Enkelte eller flere ikke-fakturerede faktiske salgsværdier kan markeres som **Klar til fakturering** eller **Ikke-klar til fakturering** fra denne visning. Hvis du markerer en ikke-faktureret faktisk salgsværdi som **Klar til fakturering**, bliver den tilgængelig til brug i en kladdefaktura.

Ikke-fakturerede faktiske salgstal med en status angivet til **Må ikke overskrides**, som er **Mislykket**, kan ikke markeres som **Klar til fakturering**. Hvis de faktiske værdier skal markeres som **Klar til fakturering**, skal du nulstille statussen for andre faktiske værdier på den kontraktlinje, der er bekræftet. og derefter revurdere statussen **Må ikke overskrides**.

Hvis der er tale om en faktureringsmetode for tid og materialer i forbindelse med kontraktlinjer med flere kunder, oprettes der en ikke-faktureret faktisk salgsværdi for hver kunde på kontraktlinjen i henhold til den faktureringsprocentsats, der er defineret for hver enkelt kunde. Visningen **Faktureringsefterslæb for tid og materialer** kan du se de enkelte kundespecifikke ikke-fakturerede faktiske salgsværdier. Hver af disse ikke-fakturerede faktiske salgsposter kan særskilt markeres som **Klar til fakturering** fra denne visning.

En ikke-faktureret faktisk salgsværdi i en kladdefaktura vises i denne visning med en faktureringsstatus **Kundefaktura oprettet**. Når kladdefakturaen er bekræftet, opdateres faktureringsstatussen for denne post til **Kundefaktura er bogført**. Opdater ikke denne statusværdi ved hjælp af brugerdefineret kode. Project Operations fungerer ikke korrekt, når disse statusværdier opdateres med brugerdefineret kode.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]