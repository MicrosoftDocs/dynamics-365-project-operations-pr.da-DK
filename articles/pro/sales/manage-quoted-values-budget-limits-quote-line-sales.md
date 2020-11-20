---
title: Oversigt over projektbaserede tilbudslinjer - lille
description: Dette emne indeholder oplysninger om, hvordan du bruger projektbaserede tilbudslinjer til projektarbejde. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181085"
---
# <a name="project-based-quote-lines-overview---lite"></a>Oversigt over projektbaserede tilbudslinjer - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

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
| Navn | Navnet på tilbudslinjen, som kan hjælpe dig med at identificere den diskrete komponent i det tilbud, der estimeres. | Kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Faktureringsmetode | På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt på salgsmulighedslinjen. Dette felt indeholder de to primære kontraherende modeller, der understøttes af Dynamics 365 Project Operations:</br>- Fast pris</br>- Tid og materiale.| Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Project | Brug dette valgfrie felt til at identificere det projekt, der skal bruges til at levere arbejdet på denne aftale. Når et projekt knyttes til en tilbudslinje, kan det hjælpe med konfigurationen af fakturerbare opgaver og også til at udarbejde et projektbaseret estimat over tilbudslinjen som tilbudslinjedetaljer. Når et projekt ikke er knyttet til en projektbaseret tilbudslinje, skal estimatet oprettes manuelt ved at oprette hver enkelt tilbudslinjedetalje. | Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.|
| Inkluderede opgaver | Angiver, om denne tilbudslinje bruges til alle eller nogle af projektopgaverne for det valgte projekt. Dette felt har følgende mulige værdier:</br>- Alle projektopgaver</br>- Kun valgte projektopgaver</br>En tom værdi i dette felt svarer til indstillingen **Alle projektopgaver**. | Når du har valgt **Kun valgte projektopgaver** på projektsiden, kan du på fanen **Opsætning af opgavefakturering** vælge specifikke opgaver, der skal tilknyttes disse tilbudslinjer. Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Medtag tid | Et flag med **Ja**/**Nej** indikerer, om tidstransaktioner eller arbejdskraftomkostninger på de valgte projekter inkluderes i estimatet på tilbudslinjen. En værdi med **Nej** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne ikke inkluderes i estimatet på tilbudslinjen. En værdi med **Ja** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne inkluderes i estimatet på tilbudslinjen. | Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Medtag udgift | Et flag med **Ja**/**Nej** indikerer, om udgiftsomkostningerne på de valgte projekter inkluderes i estimatet på tilbudslinjen. En værdi med **Nej** indikerer, at udgiftsomkostningerne ikke inkluderes i estimatet på tilbudslinjen. En værdi med **Ja** indikerer, at udgiftsomkostningerne inkluderes i estimatet på tilbudslinjen. | Denne feltværdi kopieres over i den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Medtag gebyr | Et flag med **Ja**/**Nej** indikerer, om gebyrerne på de valgte projekter inkluderes i estimatet på tilbudslinjen. En værdi med **Nej** indikerer, at gebyrerne ikke inkluderes i estimatet på tilbudslinjen. En værdi med **Ja** indikerer, at gebyrerne inkluderes i estimatet på tilbudslinjen. | Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Tilbudsbeløb | Dette er det beløb, som vil blive tilbudt kunden for alt arbejde, der er anslået for denne projektbaserede tilbudslinje. På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt **Kundebudget** på salgsmulighedslinjen. Når den projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til beløbet i detaljerne i tilbudslinjen. | Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Anslået moms | Dette felt er et redigerbart felt, hvor brugeren kan tilføje det anslåede momsbeløb på tilbudslinjen. Når en projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til momsbeløbet i detaljerne i tilbudslinjen. | Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Tilbudsbeløb efter moms | Dette felt er tilbudslinjebeløbet efter moms og er skrivebeskyttet. Beløbet i dette felt beregnes som *Tilbudsbeløb + moms*. | Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Grænse, der ikke må overskrides | Dette felt kan redigeres og er kun tilgængeligt for projektbaserede tilbudslinjer med faktureringsmetoden **Tid og materiale**. | Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |
| Kundebudget | Dette felt kan redigeres og kopieres fra det tilsvarende felt på salgsmulighedslinjen, hvis tilbuddet blev oprettet ud fra en salgsmulighed. | Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Valideringsregler for felter under fanen Generelt på projektbaserede tilbudslinjer

**Regel 1**: Hvis feltet **Inkluderede opgaver** er tomt, eller hvis det er angivet til **Alle projektopgaver**, medtages der et projekt i tilbudslinjen.

**Regel 2**: Hvis feltet **Inkluderede opgaver** er tomt, eller hvis det er angivet til **Alle projektopgaver**, kan et projekt og en bestemt transaktionsklasse kun inkluderes på én projektbaseret tilbudslinje for et tilbud.

**Regel 3**: Hvis feltet **Inkluderede opgaver** er angivet til **Kun valgte projektopgaver**, kan et projekt og en bestemt transaktionsklasse inkluderes på flere projektbaseret tilbudslinjer for et tilbud.

**Regel 4**: Hvis en salgsmulighed har flere tilbud, kan der være tilbudslinjer fra forskellige tilbud, der alle refererer til det samme projekt, og som inkluderer samme transaktionsklasse.

**Regel 5**: Hvis de pågældende tilbud ikke hører til samme salgsmulighed, kan de ikke indeholde samme projekt- og transaktionsklasse.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Salgsmulighed</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Tilbud</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Tilbudslinje</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
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
                    <strong>Medtag</strong>
                </p>
                <p>
                    <strong>Gebyr</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Gyldig/ikke gyldig</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Årsag</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Overtrædelse af regel #2. Tid, udgifter og gebyrer på P1-projektet medtages på tilbudslinjerne QL1 og QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Overtrædelse af regel #2. Tid og gebyrer på P1-projektet medtages på tilbudslinjerne QL1 og QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
Tid og gebyrer på P1-projektet er medtaget i QL1.
Udgift til P1-projekt er inkluderet i QL2.
Der findes ingen overlapning i det, der medtages på hver tilbudslinje og er gyldig.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ikke gyldig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Overtrædelse af regel #2 ovenfor </p>
                <p>
Q1 inkluderer tid, udgifter og gebyrer i et undersæt af opgaver på projektet P1.
                </p>
                <p>
QL2 inkluderer tid, udgifter og gebyrer for hele P1-projektet P1 og overlapper med det, der er inkluderet i Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
I henhold til regel #3 ovenfor, </p>
                <p>
Q1 inkluderer tid, udgifter og gebyrer i et undersæt af opgaver på projektet P1.
                </p>
                <p>
QL2 inkluderer tid, udgifter og gebyrer for et undersæt af opgaver på projektet P1.
                </p>
                <p>
Den eneste yderligere validering sker ved hjælp af undersættet af opgaver i QL1, som er forskellige fra undersættet af opgaver i QL2. Dette sikrer, at der ikke er overlap. Dette gøres af systemet, når opgaverne er tilknyttet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Alle projektopgaver eller tomme </p>
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
            <td width="54" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Afhængigt af regel #5, Q1 og Q2 er der to tilbud på samme salgsmulighed, så de begge kan estimerer for de samme komponenter i et projekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Alle projektopgaver eller tomme </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Alle projektopgaver eller tomme </p>
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
            <td width="54" valign="top">
                <p>
Gyldig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Afhængigt af regel #4, Q1 og Q2 er der to tilbud på forskellige salgsmuligheder, så de kan ikke estimerer for de samme komponenter i det samme projekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Alle projektopgaver eller tomme </p>
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
            <td width="54" valign="top">
                <p>
Ikke gyldig </p>
            </td>
        </tr>
    </tbody>
</table>

