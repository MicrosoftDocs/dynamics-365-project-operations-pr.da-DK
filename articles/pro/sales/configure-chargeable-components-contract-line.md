---
title: Konfigurer fakturerbare komponenter i en projektbaseret kontraktlinje - lille
description: Dette emne indeholder oplysninger om, hvordan du tilføjer fakturerbare komponenter til kontraktlinjer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 46429c94ca9aa1ebbbe9fc689a9a5bd6c52dc59e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177144"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfigurer fakturerbare komponenter i en projektbaseret kontraktlinje - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En projektbaseret kontraktlinje har *inkluderede* komponenter og *fakturerbare* komponenter.

Inkluderede komponenter er komponenter, der er underlagt:

  - Faktureringsmetode og kundeopdelinger
  - Grænser, der ikke må overskrides 
  - Indstillinger for fakturahyppighed, der er defineret på den projektbaserede kontraktlinje

Et undersæt af de inkluderede komponenter kan markeres som fakturerbart ved hjælp af feltet **Faktureringstype**. Feltet **Faktureringstype** er en grupperet indstilling, der gør det muligt at benytte følgende værdier i sammenhæng med en kontraktlinje:

  - Fakturerbar
  - Ikke-fakturerbar

Der kan defineres fakturerbare komponenter for opgaver, roller og transaktionskategorier.

Fakturerbarheden defineres på opgaver i en projektkontraktlinje og gælder for alle de transaktionsklasser, der er medtaget på linjen. Hvis feltet **Inkluder opgaver** i en kontraktlinje er tomt eller indstillet til **Hele projektet**, er fanen **Fakturerbare opgaver** ikke tilgængelig.

Den fakturerbarhed, der er defineret på roller i en projektkontraktlinje, gælder kun for transaktionsklassen **Tid**. Hvis feltet **Inkluder tid** i en kontraktlinje er indstillet til **Nej**, er fanen **Fakturerbare roller** ikke tilgængelig.

Den fakturerbarhed, der er defineret på transaktionskategorier i en projektkontraktlinje, gælder kun for transaktionsklassen **Udgifter**. Hvis feltet **Inkluder udgifter** er indstillet til **Nej**, er fanen **Fakturerbare kategorier** ikke tilgængelig.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Opdater en projektopgave som fakturerbar eller ikke-fakturerbar

En projektopgave kan være fakturerbar eller ikke-fakturerbar på en bestemt kontraktlinje, hvilket gør følgende opsætning mulig:

Hvis en projektbaseret kontraktlinje indeholder **Tid** og en bestemt opgave, er **T1** tilknyttet hertil som fakturerbar. Hvis der findes en anden kontraktlinje, som indeholder **Udgifter**, kan du tilknytte T1-opgaven på kontraktlinjen som ikke-fakturerbar. Resultatet er, at al den tid, der er registreret på opgaven, er fakturerbar, og alle udgifter er ikke-fakturerbare.

En opgaves faktureringstype kan konfigureres under fanen **Fakturerbare opgaver** på kontraktlinjen ved at opdatere feltet **Faktureringstype** i undergitteret for kontraktlinjeopgaver. Du kan også opdatere feltet **Faktureringstype** i undergitteret i opsætningen af opgavefakturering for et projekt, som viser de kontraktlinjer, der er knyttede til en opgave.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Opdater en rolle som fakturerbar eller ikke-fakturerbar

En rolle kan være fakturerbar eller ikke-fakturerbar på en bestemt kontraktlinje.

En rolles faktureringstype kan konfigureres under fanen **Fakturerbare roller** på en kontraktlinje. Det kan du gøre ved at opdatere feltet **Faktureringstype** i undergitteret **Fakturerbare roller**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Opdater en transaktionskategori som fakturerbar eller ikke-fakturerbar

En transaktionskategori kan være fakturerbar eller ikke-fakturerbar på en bestemt kontraktlinje.

En transaktions faktureringstype kan konfigureres under fanen **Fakturerbare kategorier** på en projektbaseret kontraktlinje. Det kan du gøre ved at opdatere feltet **Faktureringstype** i undergitteret **Fakturerbare kategorier**.

### <a name="resolve-chargeability"></a>Løs fakturerbarhed

Et estimat eller en faktisk værdi, der er oprettet for tid, anses kun for at være fakturerbar, hvis **Tid** medtages på kontraktlinjen, og hvis **Opgave** og **Rolle** er konfigureret som fakturerbar på kontraktlinjen.

Et estimat eller en faktisk værdi, der er oprettet for udgifter, anses kun for at være fakturerbar, hvis **Udgifter** medtages på kontraktlinjen, og hvis kategorierne **Opgave** og **Transaktion** er konfigureret som fakturerbare på kontraktlinjen.


| Inkluderer tid | Inkluderer udgifter | Inkluderer opgaver | Rolle           | Kategori       | Opgave                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ja           | Ja              | Hele projektet | Fakturerbar     | Fakturerbar     | Fakturering af en faktisk værdi for tid: **Fakturerbar** </br> Faktureringstype på en faktisk værdi for en udgift: **Fakturerbar**           |
| Ja           | Ja              | Valgte opgaver | Fakturerbar     | Fakturerbar     | Fakturering af en faktisk værdi for tid: **Fakturerbar** </br> Faktureringstype på en faktisk værdi for en udgift: **Fakturerbar**           |
| Ja           | Ja              | Valgte opgaver | Ikke-fakturerbar | Fakturerbar     | Fakturering af en faktisk værdi for tid: **Ikke-fakturerbar** </br> Faktureringstype på en faktisk værdi for en udgift: **Fakturerbar**       |
| Ja           | Ja              | Valgte opgaver | Fakturerbar     | Fakturerbar     | Fakturering af en faktisk værdi for tid: **Ikke-fakturerbar** </br> Faktureringstype på en faktisk værdi for en udgift: **Ikke-fakturerbar** |
| Ja           | Ja              | Valgte opgaver | Ikke-fakturerbar | Fakturerbar     | Fakturering af en faktisk værdi for tid: **Ikke-fakturerbar** </br> Faktureringstype på en faktisk værdi for en udgift: **Ikke-fakturerbar** |
| Ja           | Ja              | Valgte opgaver | Ikke-fakturerbar | Ikke-fakturerbar | Fakturering af en faktisk værdi for tid: **Ikke-fakturerbar** </br> Faktureringstype på en faktisk værdi for en udgift: **Ikke-fakturerbar** |
| Nr.            | Ja              | Hele projektet | Kan ikke angives   | Fakturerbar     | Fakturering af en faktisk værdi for tid: **Ikke tilgængelig**</br>Faktureringstype på en faktisk værdi for en udgift: **Fakturerbar**          |
| Nr.            | Ja              | Hele projektet | Kan ikke angives   | Ikke-fakturerbar | Fakturering af en faktisk værdi for tid: **Ikke tilgængelig**</br> Faktureringstype på en faktisk værdi for en udgift: **Ikke-fakturerbar**     |
| Ja           | Nr.               | Hele projektet | Fakturerbar     | Kan ikke angives   | Fakturering af en faktisk værdi for tid: **Fakturerbar** </br> Faktureringstype på en faktisk værdi for en udgift: **Ikke tilgængelig**        |
| Ja           | Nr.               | Hele projektet | Ikke-fakturerbar | Kan ikke angives   | Fakturering af en faktisk værdi for tid: **Ikke-fakturerbar** </br>Faktureringstype på en faktisk værdi for en udgift: **Ikke tilgængelig**   |
