---
title: Konfigurer de fakturerbare komponenter i en projektbaseret tilbudslinje
description: Dette emne indeholder oplysninger om inkluderede, fakturerbare og ikke-fakturerbare komponenter på projektbaserede tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642536"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfigurer de fakturerbare komponenter i en projektbaseret tilbudslinje

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

En projektbaseret tilbudslinje kan have inkluderede komponenter og fakturerbare komponenter.

Inkluderede komponenter er underlagt faktureringsmetoden, kundeopdelinger, grænser, der ikke må overskrides, og indstillinger for fakturahyppighed, som er defineret på den projektbaserede tilbudslinje.
En del af de inkluderede komponenter kan markeres som fakturerbare ved hjælp af **Faktureringstype**. Du kan vælge en af følgende indstillinger i feltet **Faktureringstype** i forbindelse med en tilbudslinje:

   - Fakturerbar
   - Ikke-fakturerbar

Der kan defineres fakturerbare komponenter for roller og transaktionskategorier.

Den omkostningssats, der er defineret for roller for en projekttilbudslinje, gælder kun for transaktionsklassen **Tid**. Hvis en projekttilbudslinje har angivet **Inkluder tid** = **Nej**, er fanen **Fakturerbare roller** ikke tilgængelig.

Den omkostningssats, der er defineret transaktionskategorier for en projekttilbudslinje, gælder kun for transaktionsklassen **Udgift**. Hvis en projekttilbudslinje har angivet **Inkluder udgifter** = **Nej**, er fanen **Fakturerbare kategorier** ikke tilgængelig.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Opdater en rolle til at være fakturerbar eller ikke-fakturerbar
En rolle kan være fakturerbar eller ikke-fakturerbar på en projektbaseret tilbudslinje. Faktureringstypen på en rolle kan konfigureres under fanen **Fakturerbare roller** for en projektbaseret tilbudslinje. Det kan du gøre ved at opdatere **Faktureringstype** i undergitteret **Fakturerbare roller**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Opdater en transaktionskategori til at være fakturerbar eller ikke-fakturerbar
En transaktionskategori kan være fakturerbar eller ikke-fakturerbar på en projektbaseret tilbudslinje. Faktureringstypen på en transaktion kan konfigureres under fanen **Fakturerbare kategorier** for en projektbaseret tilbudslinje. Det kan du gøre ved at opdatere feltet **Faktureringstype** i undergitteret **Fakturerbare kategorier**. 

## <a name="resolve-chargeability"></a>Løs fakturerbarhed

Et estimat eller faktisk værdi for tid anses kun for at være fakturerbar, hvis tiden inkluderes i tilbudslinjen, og hvis rollen er konfigureret som fakturerbar.
Et estimat eller faktisk værdi for en udgift anses kun for at være fakturerbar, hvis udgiften inkluderes i tilbudslinjen, og hvis transaktionskategorien er konfigureret som fakturerbar på tilbudslinjen. I følgende tabel vises, hvordan dine standardindstillinger for fakturerbarhed er angivet for hver faktiske værdi. Standardværdierne er baserede på de inkluderede komponenter og den faktureringstype, der er konfigureret på tilbudslinjen.

| Inkluderer tid | Inkluderer udgifter | Rolle | Kategori | Opgave |
| --- | --- | --- | --- | --- |
| Ja | Ja | Fakturerbar | Fakturerbar | Fakturering af en faktisk værdi for tid: Fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Ja | Ja | Ikke-fakturerbar | Fakturerbar | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Ja | Ja | Ikke-fakturerbar | Ikke-fakturerbar | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Ikke-fakturerbar |
| Nr. | Ja | Kan ikke angives | Fakturerbar | Fakturering af en faktisk værdi for tid: Ikke tilgængelig </br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Nr. | Ja | Kan ikke angives | Ikke-fakturerbar | Fakturering af en faktisk værdi for tid: Ikke tilgængelig </br>Faktureringstype på en faktisk værdi for en udgift: Ikke-fakturerbar |
| Ja | Nr. | Fakturerbar | Kan ikke angives | Fakturering af en faktisk værdi for tid: Fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Ikke tilgængelig |
| Ja | Nr. | Ikke-fakturerbar | Kan ikke angives | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar </br> Faktureringstype på en faktisk værdi for en udgift: Ikke tilgængelig |
