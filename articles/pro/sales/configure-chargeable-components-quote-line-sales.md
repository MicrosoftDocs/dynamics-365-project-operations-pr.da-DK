---
title: Konfigurer de fakturerbare komponenter i en tilbudslinje - lille
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere fakturerbare og ikke-fakturerbare komponenter på en projektbaseret tilbudslinje.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177099"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Konfigurer de fakturerbare komponenter i en tilbudslinje - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En projektbaseret tilbudslinje indeholder konceptet for *inkluderede* komponenter og *fakturerbare* komponenter.

Inkluderede komponenter er underlagt:

  - Faktureringsmetode og kundeopdelinger
  - Grænser, der ikke må overskrides 
  - Indstillinger for fakturahyppighed, der er defineret på den projektbaserede tilbudslinje

Et undersæt af de inkluderede komponenter kan markeres som fakturerbart ved hjælp af feltet **Faktureringstype**. Feltet **Faktureringstype** er en grupperet indstilling, der gør det muligt at benytte følgende værdier i sammenhæng med en tilbudslinje:

  - Fakturerbar
  - Ikke-fakturerbar

Der kan defineres fakturerbare komponenter for opgaver, roller og transaktionskategorier.

Fakturerbarheden defineres på opgaverne i en tilbudslinje og gælder for alle de transaktionsklasser, der er medtaget på den pågældende linje. Hvis feltet **Medtag opgaver** er indstillet til **Hele projektet** eller er tomt, er fanen **Fakturerbare opgaver** ikke tilgængelig.

Fakturerbarhed defineres på roller i en tilbudslinje og gælder kun for transaktionsklassen **Tid**. Hvis feltet **Inkluder tid** er indstillet til **Nej** på en projekttilbudslinje, er fanen **Fakturerbare roller** ikke tilgængelig.

Fakturerbarhed defineres på transaktionskategorier i en tilbudslinje og gælder kun for transaktionsklassen **Udgifter**. Hvis feltet **Inkluder udgifter** er indstillet til **Nej** på en projekttilbudslinje, er fanen **Fakturerbare kategorier** ikke tilgængelig.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Opdater en projektopgave for at gøre den fakturerbar eller ikke-fakturerbar

En projektopgave kan være fakturerbar eller ikke-fakturerbar i sammenhæng med en bestemt projektbaseret tilbudslinje, hvilket gør følgende opsætning mulig:

Hvis en projektbaseret tilbudslinje indeholder **Tid** og opgaven **T1**, knyttes opgaven til tilbudslinjen som fakturerbar. Hvis der findes en anden tilbudslinje, som indeholder **Udgifter**, kan du tilknytte opgaven **T1** på tilbudslinjen som ikke-fakturerbar. Resultatet er, at al den tid, der registreres på opgaven, er fakturerbar, og alle udgifter der registreres på opgaven er ikke-fakturerbare.

En opgaves faktureringstype kan konfigureres på fanen **Fakturerbare opgaver** for en projektbaseret tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Tilbudslinjeopgaver**. Du kan også opdatere faktureringstypen for en projektopgave i feltet **Faktureringstype** i undergitteret for opsætningen af opgavefakturering for et projekt, som viser de tilbudslinjer, der er knyttede til en opgave.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Opdater en rolle til at være fakturerbar eller ikke-fakturerbar

En rolle kan være fakturerbar eller ikke-fakturerbar i relation til en bestemt projektbaseret tilbudslinje.

En rolles faktureringstype kan konfigureres på fanen **Fakturerbare roller** for en tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Fakturerbare roller**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Opdater en transaktionskategori til at være fakturerbar eller ikke-fakturerbar

En transaktionskategori kan være fakturerbar eller ikke-fakturerbar på en bestemt tilbudslinje.

En transaktions faktureringstype kan konfigureres på fanen **Fakturerbare kategorier** for en tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Fakturerbare kategorier**.

### <a name="resolve-chargeability"></a>Løs fakturerbarhed
Et estimat eller en faktisk værdi, der er oprettet for tid, anses kun for at være fakturerbar, hvis **Tid** medtages på tilbudslinjen, og hvis **Opgave** og **Rolle** er konfigureret som fakturerbar på tilbudslinjen.

Et estimat eller en faktisk værdi, der er oprettet for udgifter, anses kun for at være fakturerbar, hvis **Udgifter** medtages på tilbudslinjen, og hvis **Opgave** og **Transaktionskategori** er konfigureret som fakturerbare på tilbudslinjen.

| Inkluderer tid | Inkluderer udgifter | Inkluderede opgaver | Rolle | Kategori | Opgave | Fakturering |
| --- | --- | --- | --- | --- | --- | --- |
| Ja | Ja | Hele projektet | Fakturerbar | Fakturerbar | Kan ikke angives | Fakturering af en faktisk værdi for tid: Fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Ja | Ja | Kun valgte opgaver | Fakturerbar | Fakturerbar | Fakturerbar | Fakturering af en faktisk værdi for tid: Fakturerbar</br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Ja | Ja | Kun valgte opgaver | Ikke-fakturerbar | Fakturerbar | Fakturerbar | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar</br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Ja | Ja | Kun valgte opgaver | Fakturerbar | Fakturerbar | Ikke-fakturerbar | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar</br> Faktureringstype på en faktisk værdi for en udgift: Ikke-fakturerbar |
| Ja | Ja | Kun valgte opgaver | Ikke-fakturerbar | Fakturerbar | Ikke-fakturerbar | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar</br> Faktureringstype på en faktisk værdi for en udgift: Ikke-fakturerbar |
| Ja | Ja | Kun valgte opgaver | Ikke-fakturerbar | Ikke-fakturerbar | Fakturerbar | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar</br> Faktureringstype på en faktisk værdi for en udgift: Ikke-fakturerbar |
| Nr. | Ja | Hele projektet | Kan ikke angives | Fakturerbar | Kan ikke angives | Fakturering af en faktisk værdi for tid: Ikke tilgængelig </br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Nr. | Ja | Hele projektet | Kan ikke angives | Ikke-fakturerbar | Kan ikke angives | Fakturering af en faktisk værdi for tid: Ikke tilgængelig </br>Faktureringstype på en faktisk værdi for en udgift: Ikke-fakturerbar |
| Ja | Nr. | Hele projektet | Fakturerbar | Kan ikke angives | Kan ikke angives | Fakturering af en faktisk værdi for tid: Fakturerbar</br>Faktureringstype på en faktisk værdi for en udgift: Ikke tilgængelig |
| Ja | Nr. | Hele projektet | Ikke-fakturerbar | Kan ikke angives | Kan ikke angives | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Ikke tilgængelig |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]