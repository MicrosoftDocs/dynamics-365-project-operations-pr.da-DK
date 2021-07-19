---
title: Oversigt over projektbaserede kontraktlinjer
description: Dette emne indeholder oplysninger om at arbejde med projektbaserede kontraktlinjer.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369909"
---
# <a name="project-based-contract-lines-overview"></a>Oversigt over projektbaserede kontraktlinjer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Projektbaserede kontraktlinjer i Dynamics 365 Project Operations er designet til at rumme estimat- og faktureringsaftaler for specifikke komponenter i projektarbejde på en aftale. Strukturen i en projektbaseret kontraktlinje udvides for projektestimater og faktureringsscenarier med følgende koncepter:

- Faktureringsmetode
- Projekt- og opgavetilknytning
- Inkluderede transaktionsklasser
- Grænse, der ikke må overskrides
- Opsætning af fakturerbarhed
- Estimater ved hjælp af kontraktlinjedetaljer
- Kontraktlinjekunder

I følgende tabel medtages felterne under fanen **Generelt** for projektbaserede kontraktlinjer, som hjælper med at konfigurere grundlaget for et detaljeret, grundlæggende estimat og faktureringsaftaler for projektbaseret arbejde.

| Felt | Beskrivelse | Downstream-virkning |
| --- | --- | --- |
| **Navn** | Navn på kontraktlinjen. Dette identificerer den diskrete komponent i kontrakten, der skal estimeres. I en projektkontrakt, der er oprettet ud fra et tilbud, kopieres denne værdi fra en tilsvarende værdi for den projektbaserede tilbudslinje. | Navnet kopieres til den projektfakturalinje, der oprettes fra denne kontraktlinje, når fakturaen oprettes. |
| **Faktureringsmetode** | På en projektkontrakt, der er oprettet ud fra et tilbud, kopieres denne værdi fra det tilsvarende felt på tilbudslinjen. Dette er en grupperet indstilling, der repræsenterer de to primære kontraktmodeller, som understøttes af Project Operations:</br>- **Fast pris**</br>- **Tid og materiale** | Den faktiske transaktion behandles på grundlag af faktureringsmetoden for den kontrakt, der henvises til. Hvis den kontraktlinje, der henvises til af den faktiske værdi, har en faktureringsmetode for tid og materialer, oprettes der poster for omkostninger og ikke-faktureret faktisk salgsværdier. Hvis den kontraktlinje, der henvises til af den faktiske værdi, har en faktureringsmetode for fast pris, oprettes der kun en faktisk omkostningsværdi. |
| **Project** | Brug dette felt til at identificere det projekt, der skal bruges til at levere arbejdet på denne aftale. | Denne værdi bruges sammen med **Inkluderede opgaver** og **Inkluderede transaktionsklasser** til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost. |
| **Inkluderede opgaver** | Angiver, om denne kontraktlinje inkluderer alle projektopgaver for det valgte projekt eller kun et undersæt af opgaverne. Dette er en grupperet indstilling, der har følgende mulige værdier:</br>- **Alle projektopgaver**</br>- **Kun markerede projektopgaver**. En tom værdi i dette felt svarer til at vælge **Alle projektopgaver**. | Hvis du har valgt **Kun markerede opgaver**, kan du vælge bestemte opgaver og knytte dem til denne kontraktlinje under fanen **Opsætning af opgavefakturering** på siden **Projekt**. Værdien anvendes sammen med klasserne **Projekt** og **Inkluderet transaktion** til at fortolke kontraktlinjereferencen på en post for en faktisk værdi eller en estimatlinje. |
| **Medtag tid** | Værdien **Ja**/**Nej** angiver, om tidstransaktioner eller arbejdsomkostninger for det valgte projekt skal medtages på denne kontraktlinje. En værdi angivet til **Nej** medfører, at tidstransaktionerne eller arbejdsomkostninger ikke medtages på denne kontraktlinje. Hvis værdien **Ja** er angivet, betyder det, at de bliver medtaget. | Denne værdi bruges sammen med projektet til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost. |
| **Medtag udgift** | Værdien **Ja**/**Nej** angiver, om udgiftsomkostninger for det valgte projekt skal medtages på denne kontraktlinje. En værdi angivet til **Nej** medfører, at udgiftsomkostningen ikke medtages på denne kontraktlinje. Hvis værdien **Ja** er angivet, betyder det, at den bliver medtaget. | Denne værdi bruges sammen med projektet til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost. |
| **Medtag materialer** | Værdien **Ja**/**Nej** angiver, om materialeomkostninger for det valgte projekt skal medtages på denne kontraktlinje. En værdi angivet som **Nej** indikerer, at materialeomkostningerne ikke bliver medtaget på denne kontraktlinje. Hvis værdien **Ja** er angivet, betyder det, at den bliver medtaget. | Denne værdi bruges sammen med projektet til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost. |
| **Medtag gebyr** | Værdien **Ja**/**Nej** angiver, om gebyrer for det valgte projekt skal medtages på denne kontraktlinje. En værdi angivet til **Nej** medfører, at gebyrerne ikke medtages på denne kontraktlinje. Hvis værdien **Ja** er angivet, betyder det, at de bliver medtaget. | Denne værdi bruges sammen med projektet til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost. |
| **Kontraktbeløb** | På en kontraktlinje med fast pris er dette beløb den aftalte værdi, der skal faktureres kunden for alle de arbejdskomponenter, der er knyttet til kontraktlinjen. På en kontraktlinje med tid og materialer er dette beløb en estimeret værdi for det, der skal faktureres kunden for alle de arbejdskomponenter, der er knyttet til kontraktlinjen. På en projektkontrakt, som er oprettet ud fra et tilbud, kopieres denne værdi fra det tilsvarende felt på tilbudslinjen. Når en projektbaseret kontraktlinje indeholder linjeoplysninger, er dette felt låst mod redigering og opsummeres i på grundlag af beløbet i kontraktlinjeoplysningerne. | Når kontraktlinjen indeholder linjeoplysninger, kan denne værdi ændres ved at ændre beløbene på linjedetaljerne. På en kontraktlinje med fast pris bruges denne værdi til at oprette beløbet før moms på periodiske faktureringsmilepæle. |
| **Anslået moms** | Brugeren kan redigere dette felt for at angive det estimerede momsbeløb på kontraktlinjen. Når en projektbaseret kontraktlinje indeholder linjeoplysninger, er dette felt låst mod redigering og opsummeres i på grundlag af momsbeløbet i kontraktlinjeoplysningerne. | Når kontraktlinjen indeholder linjeoplysninger, kan denne værdi ændres ved at ændre momsbeløbene på linjedetaljerne. På en kontraktlinje med fast pris bruges denne værdi til at oprette momsen på periodiske faktureringsmilepæle. |
| **Kontraktbeløb efter moms** | Beløbet på kontraktlinjen efter moms. Dette felt er skrivebeskyttet og beregnes som **Kontraktbeløb + moms**. | På en kontraktlinje med fast pris bruges denne værdi til at oprette periodiske faktureringsmilepæle. |
| **Grænse, der ikke må overskrides** | Brugeren kan redigere dette felt, og det er kun tilgængeligt for projektbaserede kontraktlinjer, der har faktureringsmetoden angivet som tid og materialer. | Brugeren kan redigere dette felt. Når en faktisk værdi for tid og materialer refererer til denne kontraktlinje for tid og materiale, evalueres beløbet på den faktiske værdi i forhold til grænsen, der ikke må overskrides, på kontraktlinjen. Denne evaluering fuldføres, når der redegøres for de allerede brugte og forpligtede beløb. |
| **Kundebudget** | Dette felt kan redigeres og kopieres fra det tilsvarende felt på tilbudslinjen, hvis kontrakten er blevet oprettet på grundlag af et tilbud. | Dette felt bruges kun til orientering, og det har ingen afledede virkninger. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Valideringsregler for indstillingerne under fanen Generelt på projektbaserede kontraktlinjer

Regel 1: Hvis feltet **Inkluderede opgaver** er tomt eller angivet til **Alle projektopgaver**, medtages alle opgaver i projektet på kontraktlinjen.

Regel 2: Når feltet **Inkluderede opgaver** er tomt eller eksplicit angivet til **Alle projektopgaver**, kan et projekt og en bestemt transaktionsklasse kun inkluderes på én projektbaseret kontraktlinje i en kontrakt.

Regel 3: Når feltet **Inkluderede opgaver** er angivet til **Kun markerede projektopgaver**, kan et projekt og en bestemt transaktionsklasse inkluderes på flere projektbaserede kontraktlinjer i en kontrakt.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Kontrakt</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Kontraktlinje</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Inkluderede opgaver</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Medtag tid</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Medtag udgift</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Medtag materialer</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Inkluder</strong>
                </p>
                <p>
                    <strong>Gebyr</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Gyldig/ikke gyldig</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Årsag</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Overtrædelse af regel #2. Tid, udgifter, materialer og gebyrer på P1-projektet medtages på både tilbudslinjerne CL1 og CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Overtrædelse af regel #2. Tid, materialer og gebyrer på P1-projektet medtages på både tilbudslinjerne CL1 og CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Tid, materialer og gebyrer på P1-projektet medtages på CL1.
                </p>
                <ul>
                    <li>
Udgift til P1-projekt er inkluderet i CL2.
                    </li>
                </ul>
                <p>
Der er ingen overlapningen i det, der inkluderes på de enkelte kontraktlinjer, og derfor er det gyldigt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="42" valign="top">
                <p>
Nr. </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Overtrædelse af regel nr. 2 </p>
                <p>
C1 omfatter tid, materialer, udgifter og gebyrer på et undersæt af opgaver på projekt P1.
                </p>
                <p>
CL2 inkluderer tid, materialer, udgifter og gebyrer for hele projekt P1 og overlapper derfor med det, der er medtaget i C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
I henhold til regel nr. 3 </p>
                <p>
C1 omfatter tid, udgifter, materialer og gebyrer på et undersæt af opgaver på projekt P1.
                </p>
                <p>
CL2 omfatter tid, udgifter, materialer og gebyrer for et undersæt af opgaver på projekt P1.
                </p>
                <p>
Den eneste yderligere validering er omkring det undersæt af opgaver på CL1, som er forskellig fra undersættet af opgaver i CL2 for at sikre, at der ikke er nogen overlapning. Dette gøres af systemet, når opgaverne er tilknyttet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
