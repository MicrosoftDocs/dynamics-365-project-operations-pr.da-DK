---
title: Konfigurer fakturerbare komponenter i en projektkontraktlinje
description: Dette emne indeholder oplysninger om inkluderede, fakturerbare og ikke-fakturerbare komponenter på kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 60a2792f7783053a288303e1dcc01a986e948300
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858331"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Konfigurer fakturerbare komponenter i en projektkontraktlinje

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

En projektbaseret kontraktlinje indeholder konceptet for inkluderede, fakturerbare og ikke-fakturerbare komponenter.

Inkluderede komponenter er underlagt den faktureringsmetode og de kundeopdelinger, maksimumgrænser, der ikke må overskrides, samt de indstillinger for fakturahyppighed, der er defineret på den projektbaserede kontraktlinje.

Et undersæt af de inkluderede komponenter kan markeres som fakturerbart ved at opdatere feltet **Faktureringstype**.

Der kan defineres fakturerbare komponenter for roller og transaktionskategorier.

I relation til en projektkontraktlinje gælder den fakturerbarhed, der er defineret på en rolle, kun for transaktionsklassen **Tid**. Hvis **Inkluder tid** er indstillet til **Nej** på en projektkontraktlinje, er fanen **Fakturerbare roller** ikke tilgængelig.

Den fakturerbarhed, der er defineret på transaktionskategorier i en projektkontraktlinje, gælder kun for transaktionsklassen **Udgifter**. Hvis **Inkluder udgifter** er indstillet til **Nej** på en projektkontraktlinje, er fanen **Fakturerbare kategorier** ikke tilgængelig.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Opdater en rolle til at være fakturerbar eller ikke-fakturerbar

En rolle kan være fakturerbar eller ikke-fakturerbar på en bestemt projektbaseret kontraktlinje.

På fanen **Fakturerbare roller** for en projektbaseret kontraktlinje kan du i undergitteret **Fakturerbare kategorier** i feltet **Faktureringstype** opdatere en rolles faktureringstype.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Opdater en transaktionskategori til at være fakturerbar eller ikke-fakturerbar

En transaktionskategori kan være fakturerbar eller ikke-fakturerbar på en bestemt projektbaseret kontraktlinje.

På fanen **Fakturerbare kategorier** for en projektbaseret kontraktlinje kan du i undergitteret **Fakturerbare kategorier** i feltet **Faktureringstype** opdatere en transaktions faktureringstype.

### <a name="resolve-chargeability"></a>Løs fakturerbarhed

Et estimat eller en faktisk værdi, der er oprettet for tid, anses kun for at være fakturerbar, hvis tid inkluderes på kontraktlinjen, og hvis rollen er konfigureret som fakturerbar på kontraktlinjen.

Et estimat eller en faktisk værdi, der er oprettet for udgifter, anses kun for at være fakturerbar, hvis udgifter medtages på kontraktlinjen, og hvis transaktionskategorien er konfigureret som fakturerbare på kontraktlinjen.

| Inkluderer tid | Inkluderer udgifter | Rolle | Kategori | Opgave |
| --- | --- | --- | --- | --- |
| Ja | Ja | Fakturerbar | Fakturerbar | Fakturering af en faktisk værdi for tid: Fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Ja | Ja | Ikke-fakturerbar | Fakturerbar | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Ja | Ja | Ikke-fakturerbar | Ikke-fakturerbar | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Ikke-fakturerbar |
| Nr. | Ja | Kan ikke angives | Fakturerbar | Fakturering af en faktisk værdi for tid: Ikke tilgængelig </br>Faktureringstype på en faktisk værdi for en udgift: Fakturerbar |
| Nr. | Ja | Kan ikke angives | Ikke-fakturerbar | Fakturering af en faktisk værdi for tid: Ikke tilgængelig </br>Faktureringstype på en faktisk værdi for en udgift: Ikke-fakturerbar |
| Ja | Nr. | Fakturerbar | Kan ikke angives | Fakturering af en faktisk værdi for tid: Fakturerbar </br>Faktureringstype på en faktisk værdi for en udgift: Ikke tilgængelig |
| Ja | Nr. | Ikke-fakturerbar | Kan ikke angives | Fakturering af en faktisk værdi for tid: Ikke-fakturerbar </br> Faktureringstype på en faktisk værdi for en udgift: Ikke tilgængelig |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
