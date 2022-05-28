---
title: Konfigurer de fakturerbare komponenter i en tilbudslinje
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere fakturerbare og ikke-fakturerbare komponenter på en projektbaseret tilbudslinje.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3c9bd23f4e78e3ea5ae8f74ff1a4829a11f91929
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598389"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurer de fakturerbare komponenter i en tilbudslinje 

_**Gælder for:** Lille udrulning - aftale om proformafakturering, Project Operations for ressource/ikke-lagerbaserede scenarier_

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

En projektopgave kan være fakturerbar eller ikke-fakturerbar i sammenhæng med en bestemt projektbaseret tilbudslinje, hvilket gør følgende opsætning mulig.

Hvis en projektbaseret tilbudslinje indeholder **Tid** og opgaven **T1**, knyttes opgaven til tilbudslinjen som fakturerbar. Hvis der findes en anden tilbudslinje, som indeholder **Udgifter**, kan du tilknytte opgaven **T1** på tilbudslinjen som ikke-fakturerbar. Resultatet er, at al den tid, der registreres på opgaven, er fakturerbar, og alle udgifter der registreres på opgaven er ikke-fakturerbare.

En opgaves faktureringstype kan konfigureres på fanen **Fakturerbare opgaver** for en projektbaseret tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Tilbudslinjeopgaver**. Du kan også opdatere faktureringstypen for en projektopgave i feltet **Faktureringstype** i undergitteret for opsætningen af opgavefakturering for et projekt, som viser de tilbudslinjer, der er knyttede til en opgave.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Opdater en rolle til at være fakturerbar eller ikke-fakturerbar

En rolle kan være fakturerbar eller ikke-fakturerbar i relation til en bestemt projektbaseret tilbudslinje.

En rolles faktureringstype kan konfigureres på fanen **Fakturerbare roller** for en tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Fakturerbare roller**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Opdater en transaktionskategori til at være fakturerbar eller ikke-fakturerbar

En transaktionskategori kan være fakturerbar eller ikke-fakturerbar på en bestemt tilbudslinje.

En transaktions faktureringstype kan konfigureres på fanen **Fakturerbare kategorier** for en tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Fakturerbare kategorier**.

### <a name="resolve-chargeability"></a>Løs fakturerbarhed
En anslået eller faktisk oprettet tid kan kun opkræves, hvis:

   - **Tid** er inkluderet på tilbudslinjen.
   - **Rolle** konfigureres som fakturerbar på tilbudslinjen.
   - **Inkluderede opgaver** angives til **Valgte opgaver** på tilbudslinjen. 

Hvis disse tre ting er sande, konfigureres **Opgaven** også som fakturerbar. 

Et estimat eller en faktisk værdi, der oprettes for udgift, kan kun faktureres, hvis: 

   - **Udgift** er inkluderet på tilbudslinjen.
   - **Transaktionskategori** konfigureres som fakturerbar på tilbudslinjen.
   - **Inkluderede opgaver** angives til **Valgte opgaver** på tilbudslinjen.

Hvis disse tre ting er sande, konfigureres **Opgaven** også som fakturerbar. 

En anslået eller faktisk værdi, der er oprettet for materialer, kan kun faktureres, hvis:

   - **Materialer** er inkluderet på tilbudslinjen.
   - **Inkluderede opgaver** angives til **Valgte opgaver** på tilbudslinjen.

Hvis disse to ting er sande, bør **Opgaven** også være konfigureret som fakturerbar. 


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
Kan ikke konfigureres </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: Fakturerbar </p>
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
Fakturerbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering af en faktisk værdi for tid: Fakturerbar </p>
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
Kan ikke konfigureres </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Fakturerbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke konfigureres </p>
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
Kan ikke konfigureres </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ikke-fakturerbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke konfigureres </p>
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
Kan ikke konfigureres </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke konfigureres </p>
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
Kan ikke konfigureres </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan ikke konfigureres </p>
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
Kan ikke konfigureres </p>
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
Kan ikke konfigureres </p>
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
