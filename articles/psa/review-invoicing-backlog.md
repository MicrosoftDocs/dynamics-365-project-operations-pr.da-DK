---
title: Gennemse ordrebeholdning for fakturering vedrørende projekter og projektkontrakter
description: Dette emne indeholder oplysninger om, hvordan du gennemgår tid, udgifter og produktbeholdninger, og hvordan du markerer dem som klar til fakturering.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074381"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Gennemse ordrebeholdning for fakturering vedrørende projekter og projektkontrakter

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Når en transaktion er klar til at få oprettet og behandlet en faktura, skal transaktionen markeres som **Klar til fakturering**. I dette emne beskrives de transaktionstyper, der kan oprettes.

## <a name="review-the-time-and-material-billing-backlog"></a>Gennemse ordrebeholdning for fakturering af tid og materiale

Når en tidsregistrering eller en udgiftspost sendes og godkendes til et projekt, opretter PSA en faktisk projektkomponent. Hvis kombinationen af projektet og transaktionsklassen er knyttet til en kontraktlinje for et tids- og materialeprojekt, oprettes der to faktiske oplysninger, når posten godkendes:

- Faktisk omkostning 
- Ikke-faktureret faktisk salg

Ikke-fakturerede faktiske salgsværdier repræsenterer ordrer til fakturering, og deres faktureringsstatus skal angives til **Klar til fakturering**. Når der oprettes en projektfaktura, kopieres ikke-fakturerede faktiske salgsværdier, der er markeret som **Klar til fakturering,** over som fakturalinjedetaljer.

Hvis du vil gennemgå ordrebeholdning for fakturering af tid og materiale, skal du gå til **Salg** \> **Fakturering** \> **Ordrebeholdning for fakturering af tid og materiale**. Markér alle de ikke-fakturerede faktiske salgstal, der er klar til at blive faktureret, og vælg derefter **Klar til fakturering**. Faktureringsstatussen for disse faktiske tal ændres til **Klar til fakturering**.

![Ordrebeholdning for fakturering af tid og materiale](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Gennemgå ordrebeholdning for produktfakturering

Når en projektkontrakt har produktbaserede kontraktlinjer i PSA, betragtes disse linjer som klar til fakturering, hver gang der oprettes en faktura for projektkontrakten. Alle produkter, som har kontraktlinjer, der er markeret som **Klar til fakturering,** kopieres til projektfakturaen som projektfakturalinjer.

Hvis du vil gennemse ordrebeholdningen for produktfakturering, skal du gå til **Salg** \> **Fakturering** \> **Ordrebeholdning for produktfakturering**. Markér alle produktbaserede kontraktlinjer, der er klar til at blive faktureret, og vælg derefter **Klar til fakturering**. Faktureringsstatussen for disse linjer ændres til **Klar til fakturering**.

![Ordrebeholdning for produktfakturering](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Gennemse faktureringsmilepæle for fastpriskontrakter

Hver projektkontraktlinje, der har en fastpris-faktureringsmetode, skal definere kontraktmilepæle. Disse kontraktmilepæle kan kun faktureres, hvis de er markeret som **Klar til fakturering**. 

Hvis du vil gennemse faktureringsmilepæle, skal du gå til **Salg** \> **Fakturering** \> **Milepæle for fast pris**. Markér de milepæle, der er klar til at blive faktureret, og vælg derefter **Klar til fakturering**. Faktureringsstatussen for disse milepæle ændres til **Klar til fakturering**.

![Milepæle for fast pris](media/FPBacklog.png)
