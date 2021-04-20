---
title: Konfigurer fakturerbare komponenter i en projektbaseret kontraktlinje
description: Dette emne indeholder oplysninger om, hvordan du tilføjer fakturerbare komponenter til kontraktlinjer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858466"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurer fakturerbare komponenter i en projektbaseret kontraktlinje

_**Gælder for:** Lille udrulning - aftale om proformafakturering, Project Operations for ressource/ikke-lagerbaserede scenarier_

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

Et estimat eller en faktisk værdi, der oprettes for tid, kan kun faktureres, hvis:

   - **Tid** er inkluderet på kontraktlinjen.
   - **Rolle** er konfigureret som fakturerbar på kontraktlinjen.
   - **Inkluderede opgaver** er angivet til **Valgte opgaver** på kontraktlinjen.
 
 Hvis disse tre ting er sande, konfigureres opgaven også som fakturerbar. 

Et estimat eller en faktisk værdi, der oprettes for udgift, kan kun faktureres, hvis:

   - **Udgift** er inkluderet på kontraktlinjen
   - **Transaktionskategori** er konfigureret som fakturerbar på kontraktlinjen
   - **Inkluderede opgaver** er angivet til **Valgte opgaver** på kontraktlinjen
  
 Hvis disse tre ting er sande, konfigureres **Opgaven** også som fakturerbar. 

Et estimat eller en faktisk værdi, der oprettes for materialer, kan kun faktureres, hvis:

   - **Materialer** er inkluderet på kontraktlinjen
   - **Inkluderede opgaver** er angivet til **Valgte opgaver** på kontraktlinjen

Hvis disse to ting er sande, konfigureres **Opgaven** også som fakturerbar. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inkluderer tid</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inkluderer udgifter</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Materialer er inkluderet</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Inkluderede opgaver</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rolle</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategori</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Opgave</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Indvirkning af fakturerbarhed</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: <strong>Fakturerbar</strong>
                </p>
                <p>
Faktureringstype på faktiske materialer: <strong>Fakturerbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: <strong>Fakturerbar</strong>
                </p>
                <p>
Faktureringstype på faktiske materialer: <strong>Fakturerbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: Fakturerbar </p>
                <p>
Faktureringstype på faktiske materialer: Kan faktureres </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for materialer: <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for materialer: <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på faktiske materialer: Kan faktureres </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Fakturerbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Ikke tilgængelig</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: Fakturerbar </p>
                <p>
Faktureringstype på faktiske materialer: Kan faktureres </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Ikke tilgængelig</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på faktiske materialer: Kan faktureres </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: Fakturerbar </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke tilgængelig</strong>
                </p>
                <p>
Faktureringstype på faktiske materialer: Kan faktureres </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke tilgængelig</strong>
                </p>
                <p>
Faktureringstype på faktiske materialer: Kan faktureres </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturerbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: Fakturerbar </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift: Fakturerbar </p>
                <p>
Faktureringstype på en faktisk værdi for materialer: <strong>Ikke tilgængelig</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Hele projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke angives </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for en udgift:<strong> Ikke-fakturerbar </strong>
                </p>
                <p>
Faktureringstype på en faktisk værdi for materialer:<strong> Ikke tilgængelig</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
