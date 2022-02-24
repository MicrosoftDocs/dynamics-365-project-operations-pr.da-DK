---
title: Oversigt over projektbaserede tilbudslinjer
description: Dette emne indeholder oplysninger om, hvordan du bruger projektbaserede tilbudslinjer til projektarbejde.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858691"
---
# <a name="project-based-quote-lines-overview"></a>Oversigt over projektbaserede tilbudslinjer 

_**Gælder for:** Lille udrulning - aftale om proformafakturering, Project Operations for ressource/ikke-lagerbaserede scenarier_

Projektbaserede tilbudslinjer er udviklet til at hjælpe med at vurdere projektarbejdet på en aftale. Strukturen for en projektbaseret tilbudslinje forlænges for projektestimater med følgende koncepter:

- Faktureringsmetode
- Projekt- og opgavetilknytning
- Inkluderede transaktionsklasser
- Grænse, der ikke må overskrides
- Opsætning af fakturerbarhed
- Estimering ved hjælp af tilbudslinjedetaljer
- Tilbudslinjekunder

Følgende tabel indeholder oplysninger om felterne under fanen **Generelt** på den projektbaserede tilbudslinje. Disse felter bruges til at konfigurere grundlaget for en detaljeret estimering overslag af projektarbejdet fra start til slut.

| **Felt** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- |
| Navn | Navnet på tilbudslinjen, der hjælper dig med at identificere det diskrete komponent i det tilbud, der estimeres. | Kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Faktureringsmetode | På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt på salgsmulighedslinjen. Feltet omfatter de to primære kontraktmodeller, der understøttes af Dynamics 365 Project Operations:</br>- Fast pris</br>- Tid og materiale.| Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Project | Brug dette valgfrie felt til at identificere det projekt, der skal bruges til at levere arbejdet på denne aftale. Når et projekt knyttes til en tilbudslinje, kan det hjælpe med konfigurationen af fakturerbare opgaver og også til at udarbejde et projektbaseret estimat over tilbudslinjen som tilbudslinjedetaljer. Når et projekt ikke er knyttet til en projektbaseret tilbudslinje, skal estimatet oprettes manuelt ved at oprette hver enkelt tilbudslinjedetalje. | Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.|
| Inkluderede opgaver | Angiver, om denne tilbudslinje bruges til alle eller nogle af projektopgaverne for det valgte projekt. Dette felt har følgende mulige værdier:</br>- Alle projektopgaver</br>- Kun valgte projektopgaver</br>En tom værdi i dette felt svarer til indstillingen **Alle projektopgaver**. | Når **Kun valgte projektopgaver** vælges på projektsiden, kan du under fanen **Konfiguration af opgavefakturering** vælge bestemte opgaver, som du vil knytte sammen med tilbudslinjen. Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Medtag tid | Værdien **Ja**/**Nej** angiver, om tidstransaktioner eller arbejdsomkostninger for det valgte projekt skal medtages i estimatet på denne tilbudslinje. En værdi med **Nej** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne ikke inkluderes i estimatet på tilbudslinjen. En værdi med **Ja** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne inkluderes i estimatet på tilbudslinjen. | Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Medtag udgift | Værdien **Ja**/**Nej** angiver, om udgiftsomkostninger for det valgte projekt skal medtages i estimatet på denne tilbudslinje. En værdi med **Nej** indikerer, at udgiftsomkostningerne ikke inkluderes i estimatet på tilbudslinjen. En værdi med **Ja** indikerer, at udgiftsomkostningerne inkluderes i estimatet på tilbudslinjen. | Værdien kopieres over til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Medtag materiale | Værdien **Ja**/**Nej** angiver, om materialeomkostninger for det valgte projekt skal medtages i estimatet på denne tilbudslinje. En værdi angivet som **Nej** indikerer, at materialeomkostningerne ikke bliver medtaget i estimatet på denne tilbudslinje. En værdi angivet som **Ja** indikerer, at materialeomkostningerne bliver medtaget i estimatet på denne tilbudslinje. | Værdien kopieres over til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Medtag gebyr | Værdien **Ja**/**Nej** angiver, om gebyrer for det valgte projekt skal medtages i estimatet på denne tilbudslinje. En værdi med **Nej** indikerer, at gebyrerne ikke inkluderes i estimatet på tilbudslinjen. En værdi med **Ja** indikerer, at gebyrerne inkluderes i estimatet på tilbudslinjen. | Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Tilbudsbeløb | Dette er det beløb, der oplyses kunden for alt det budgetterede arbejde med denne projektbaserede tilbudslinje. På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt **Kundebudget** på salgsmulighedslinjen. Når den projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til beløbet i detaljerne i tilbudslinjen. | Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Anslået moms | Dette felt er et redigerbart felt, hvor brugeren kan tilføje det anslåede momsbeløb på tilbudslinjen. Når en projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til momsbeløbet i detaljerne i tilbudslinjen. | Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Tilbudsbeløb efter moms | Dette felt er tilbudslinjebeløbet efter moms og er skrivebeskyttet. Beløbet i dette felt beregnes som *Tilbudsbeløb + moms*. | Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Grænse, der ikke må overskrides | Dette felt kan redigeres og er kun tilgængeligt for projektbaserede tilbudslinjer med faktureringsmetoden **Tid og materiale**. | Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |
| Kundebudget | Dette felt kan redigeres og kopieres fra det tilsvarende felt på salgsmulighedslinjen, hvis tilbuddet blev oprettet ud fra en salgsmulighed. | Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Valideringsregler for felter under fanen Generelt på projektbaserede tilbudslinjer

**Regel 1**: Hvis feltet **Inkluderede opgaver** er tomt, eller hvis det er angivet til **Alle projektopgaver**, medtages der et projekt i tilbudslinjen.

**Regel 2**: Hvis feltet **Inkluderede opgaver** er tomt, eller hvis det er angivet til **Alle projektopgaver**, kan et projekt og en bestemt transaktionsklasse kun inkluderes på én projektbaseret tilbudslinje for et tilbud.

**Regel 3**: Hvis feltet **Inkluderede opgaver** er angivet til **Kun valgte projektopgaver**, kan et projekt og en bestemt transaktionsklasse inkluderes på flere projektbaseret tilbudslinjer for et tilbud.

**Regel 4**: Hvis en salgsmulighed har flere tilbud, kan der være tilbudslinjer fra forskellige tilbud, der alle refererer til det samme projekt, og som inkluderer samme transaktionsklasse.

**Regel 5**: Hvis de pågældende tilbud ikke hører til samme salgsmulighed, kan de ikke indeholde samme projekt- og transaktionsklasse.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Salgsmulighed</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Tilbud</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Tilbudslinje</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Inkluderede opgaver</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Medtag tid</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Medtag udgift</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Medtag materiale</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Inkluder</strong>
                </p>
                <p>
                    <strong>Gebyr</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Gyldig/ikke gyldig</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Årsag</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Overtrædelse af regel #2. Tid, udgifter og gebyrer på P1-projektet medtages på tilbudslinjerne QL1 og QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Overtrædelse af regel #2. Tid, materialer og gebyrer på P1-projektet medtages på tilbudslinjerne QL1 og QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Tid, materialer og gebyrer på P1-projektet medtages på QL1 <br>
Udgift til P1-projekt er inkluderet i QL2 <br>
Der er ingen overlapningen i det, der inkluderes på de enkelte tilbudslinjer, og derfor er det gyldigt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="41" valign="top">
                <p>
Nr. </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Overtrædelse af regel nr. 2 </p>
                <p>
Q1 omfatter Tid, Materialer, Udgifter og Gebyrer på et undersæt af opgaver på projekt P1 </p>
                <p>
QL2 inkluderer Tid, Udgifter og Gebyrer for hele projekt P1 og overlapper derfor med det, der er medtaget i Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
I henhold til regel nr. 3, </p>
                <p>
Q1 omfatter Tid, Materialer, Udgifter og Gebyrer på et undersæt af opgaver på projekt P1.
                </p>
                <p>
QL2 omfatter Tid, Materialer, Udgifter og Gebyrer for et undersæt af opgaver på projekt P1.
                </p>
                <p>
Den eneste yderligere validering er omkring det undersæt af opgaver på QL1, som er forskellig fra undersættet af opgaver i QL2 for at sikre, at der ikke sker overlapning. Dette gøres af systemet, når opgaverne er tilknyttet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kun valgte opgaver </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle projektopgaver eller tomme </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
I henhold til regel nr. 5 er Q1 og Q2 to tilbud på samme salgsmulighed, så de kan begge estimere for de samme komponenter i et projekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle projektopgaver eller tomme </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle projektopgaver eller tomme </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
I henhold til regel nr. 4 er Q1 og Q2 to tilbud på forskellige salgsmuligheder, så de kan ikke estimere for de samme komponenter i samme projekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle projektopgaver eller tomme </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
