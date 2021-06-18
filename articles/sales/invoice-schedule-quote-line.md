---
title: Fakturaplaner for projektbaserede tilbudslinjer
description: Dette emne indeholder oplysninger om oprettelse af fakturaplaner og milepæle for tilbudslinjer.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0a8e94bf7ff807028cec05380ac8c9bc22094d82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010149"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Fakturaplaner for projektbaserede tilbudslinjer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

En projektbaseret tilbudslinje giver mulighed for at udtrykke en fakturaplan. Dette er valgfrit i forbindelse med tilbudsfasen, da programmet ikke understøtter fakturering af et projekt, når det er bundet til en tilbudslinje. Fakturering er kun tilladt, når tilbuddet er vundet. Den eneste downstream-virkning ved at oprette en fakturaplan i tilbudsfasen er, at denne fakturaplan kopieres over i den projektbaserede kontraktlinje. Hvis du ikke opretter en fakturaplan under tilbudsfasen, kan du gøre det på den projektbaserede kontraktlinje.

Overordnet set er formålet med fakturaplaner at give mulighed for automatisk oprettelse af fakturakladder for en projektbaseret kontraktlinje. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Opret en plan for fakturering af tid og materialer for en projektbaseret tilbudslinje

Når faktureringsmetoden for en projektbaseret tilbudslinje er tid og materialer, opretter systemet en datobaseret fakturaplan. Hvis du automatisk vil oprette en datobaseret fakturaplan, skal du udføre følgende trin.

1. Gå til **Indstillinger** > **fakturafrekvenser**, og konfigurer en fakturafrekvens.
2. På siden **Tilbud** skal du åbne projekttilbuddet og på fanen **Oversigt** angive en ønsket leveringsdato.
3. Åbn tids- og materialetilbudslinjen, som du vil bruge til at oprette en datobaseret fakturaplan for. 
4. På fanen **Fakturaplan** skal du vælge værdier i felterne **Faktureringsstart** og **Fakturafrekvens**. 
5. Vælg **Generér fakturaplan** i undergitteret.
6. Programmet genererer fakturaplanen med felterne **Kørselsdato for faktura**, **Skæringsdato for transaktion** og **Status for kørsel** angivet på følgende måde:

    - **Kørselsdato for faktura** angives til den dato, der er dikteret på baggrund af fakturafrekvensen.
    - **Skæringsdatoen for transaktionen** er angivet til dagen før **Kørselsdato for faktura**.
    - **Status for kørsel** angives automatisk til **Ikke kørt**. Når jobbet for automatisk oprettelse af en faktura køres for en bestemt kørselsdato for faktura, opdateres feltet til enten **Kørsel gennemført** eller **Kørsel mislykket**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Opret en plan for fakturering af fast pris for en projektbaseret tilbudslinje

Når den projektbaserede tilbudslinje har en **Fast** faktureringsmetode, opretter systemet en milepælsbaseret fakturaplan. Benyt følgende fremgangsmåde for automatisk at oprette denne plan for et fast sæt milepæle, der er fordelt ligeligt i kalenderperioden.

1. Gå til **Indstillinger** > **fakturafrekvenser**, og konfigurer en fakturafrekvens.
2. På siden **Tilbud** skal du åbne projekttilbuddet og på fanen **Oversigt** angive en ønsket leveringsdato.
3. Åbn tilbudslinjen med fast pris, som du vil bruge til at oprette en milepælsplan for. 
4. På fanen **Fakturaplan** skal du vælge værdier i felterne **Faktureringsstart** og **Fakturafrekvens**. 
5. Vælg **Generér periodiske milepæle** i undergitteret.
6. Programmet genererer fakturaplanen med et milepælsnavn, en dato og et beløb.

    - Milepælsnavnet angives til den dato, der er dikteret på baggrund af fakturafrekvensen.
    - Milepælsdatoen angives til den dato, der er dikteret på baggrund af fakturafrekvensen.
    - Milepælsbeløbet beregnes ved at dividere tilbuddets beløb på den projektbaserede tilbudslinje med antallet af milepæle, som det er dikteret af faktureringshyppigheden og startdatoen for fakturering samt de ønskede leveringsdatoer.
    - Hvis tilbudslinjen også har anslået momsbeløb, deles denne værdi mellem hver milepæl ligeligt, når der genereres periodiske milepæle.

### <a name="manually-create-milestones"></a>Opret milepæle manuelt

Der kan også oprettes milepæle for fast pris manuelt, når de ikke er periodisk opdelt. Sådan opretter du en milepæl manuelt:

Åbn tilbudslinjen med fast pris, hvor du vil oprette en milepæl. På fanen **Fakturaplan** skal du i undergitteret vælge **+ Opret ny milepæl for tilbudslinje** og angive de nødvendige oplysninger på baggrund af følgende tabel.

| **Felt** | **Placering** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Navn på milepæl | Hurtig oprettelse | Navnet på milepælen. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen |
| Projektopgave | Hurtig oprettelse | Hvis milepælen er knyttet til en projektopgave, kan du bruge denne reference til at tilføje en brugerdefineret logik ved at angive status for milepælen på baggrund af opgavestatus. | Programmet har ingen downstream-virkning for denne reference til en opgave. |
| Milepælsdato | Hurtig oprettelse | Angiv den dato, hvor processen til automatisk oprettelse af fakturaer skal holde øje med statussen for denne milepæl for at tage den i betragtning til fakturering. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |
| Fakturastatus | Hurtig oprettelse | Når der oprettes en milepæl, angives denne status altid til **Ikke klar til fakturering**. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |
| Linjebeløb | Hurtig oprettelse | Beløb eller værdi for den milepæl, der vil blive faktureret kunden. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |
| Moms | Hurtig oprettelse | Momsbeløb, der vil blive anvendt på milepælen. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]