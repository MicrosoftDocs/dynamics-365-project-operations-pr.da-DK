---
title: Opret fakturaplaner på en projektbaseret kontraktlinje - lille
description: Dette emne indeholder oplysninger om oprettelse af fakturaplaner og milepæle.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4706a2a711efa7d176030deaa33b65bca28d8498
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273371"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Opret fakturaplaner på en projektbaseret kontraktlinje - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Du kan vedhæfte en fakturaplan på en projektbaseret kontraktlinje. Fakturering er kun tilladt, når kontrakten er blevet vundet for at oprette en projektkontrakt. Ved hjælp af fakturaplaner kan der automatisk oprettes kladdefakturaer for en projektbaseret kontraktlinje. Hvis du altid vil oprette fakturaer manuelt, kan du springe over oprettelse af fakturaplaner for en projektbaseret kontraktlinje eller en kontraktlinje.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Opret en fakturaplan for tid og materialer på en projektbaseret kontraktlinje

Når en projektbaseret kontraktlinje har faktureringsmetoden tid og materialer, kan du oprette en datobaseret fakturaplan. Hvis du automatisk vil oprette en datobaseret fakturaplan, skal du udføre følgende trin.

1. Gå til **Indstillinger** > **Faktureringshyppighed** for at konfigurere fakturahyppighed.
2. Åbn projektkontrakten og angiv på fanen **Oversigt** den ønskede leveringsdato.
3. Åbn den kontraktlinje for tid og materialer, som du vil oprette en datobaseret fakturaplan for. 
4. På fanen **Fakturaplan** skal du vælge en startdato for fakturering og faktureringshyppighed. 
5. Vælg **Generér fakturaplan** i undergitteret.

    Systemet genererer en fakturaplan med følgende feltoplysninger:

    - **Fakturaens kørselsdato** er angivet til en dato, som er baseret på fakturahyppighed.
    - **Skæringsdatoen for transaktionen** er angivet til dagen før **Kørselsdato for faktura**.
    - **Status for kørsel** angives automatisk til **Ikke kørt**. Når jobbet for automatisk oprettelse af en faktura køres for en bestemt **Kørselsdato for faktura**, opdateres feltet til **Kørsel gennemført** eller **Kørsel mislykket**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Opret en fakturaplan for en fast pris på en projektbaseret kontraktlinje

Når en projektbaseret kontraktlinje har en faktureringsmetode, der er angivet til fast pris, kan du oprette en fakturaplan, der er baseret på en milepæl. Fuldfør følgende trin for automatisk at oprette en milepælsbaseret fakturaplan for et fast sæt milepæle, der fordeles ligeligt for kalenderperioden.

1. Gå til **Indstillinger** > **Faktureringshyppighed** for at konfigurere fakturahyppighed.
2. Åbn projektkontrakten og angiv på fanen **Oversigt** den ønskede leveringsdato.
3. Åbn kontraktlinjen for den faste pris, som du vil oprette en milepælsplan for. 
4. På fanen **Fakturaplan (fakturering af milepæle)** skal du vælge startdatoen for fakturering og faktureringshyppighed. 
5. Vælg **Generér periodiske milepæle** i undergitteret.

    Systemet genererer fakturaplanen med følgende milepælsoplysninger.

    - **Milepælens navn** angives til den dato, der er dikteret på baggrund af fakturahyppigheden.
    - **Milepælens dato** angives til den dato, der er dikteret på baggrund af fakturahyppigheden.
    - **Milepælens beløb** beregnes ved at dividere kontraktbeløbet på den projektbaserede kontraktlinje med antallet af milepæle, som det er dikteret i hyppigheden, faktureringsstart og ønsket leveringsdato.
    - Hvis der er angivet en værdi i feltet **Estimeret momsbeløb** for kontraktlinjen, fordeles dette felt også til hver milepæl ligeligt, når der genereres periodiske milepæle.

Faktureringsmilepæle skal svare til den kontraktlige værdi for den projektbaserede kontraktlinje. Hvis de ikke er overensstemmende, opstår der en fejl. Du kan rette denne fejl ved at kontrollere, at faktureringsmilepælene samlede værdi udgør linjens kontraktværdi ved enten at oprette, redigere eller slette milepæle. Opdater siden, når du har foretaget ændringerne.

### <a name="manually-create-milestones"></a>Opret milepæle manuelt

Der kan oprettes milepæle med fast pris manuelt, når de ikke er periodisk opdelt. Hvis du vil oprette en milepæl manuelt, skal du benytte følgende fremgangsmåde.

1. Åbn kontraktlinjen for den faste pris, som du vil oprette en milepæl for. 
2. På fanen **Fakturaplan** skal du i undergitteret vælge **+ Opret en ny milepæl for kontraktlinje**.
3. I formularen **Oprettelse af milepæl** skal du angive de påkrævede oplysninger, der er baseret på følgende tabel. 

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| Navn på milepæl | Hurtig oprettelse | Tekstfelt for navnet på milepælen. | Dette felt indgår i projektkontraktlinjens milepæl og fakturaen. |
| Projektopgave | Hurtig oprettelse | Hvis milepælen er knyttet til en projektopgave, skal du bruge denne reference til at tilføje brugerdefineret logik og angive statussen for milepælen på baggrund af opgavens status. | Denne reference har ingen afledende virkning for en opgave. |
| Milepælsdato | Hurtig oprettelse | Den dato, hvor processen for automatisk oprettelse af fakturaer skal søge efter statussen for denne milepæl for at tage den i betragtning i forbindelse med fakturering. | Dette indgår i projektkontraktlinjens milepæl og fakturaen. |
| Fakturastatus | Hurtig oprettelse | Når milepælen er oprettet, angives denne status altid til **Ikke klar til fakturering** eller **Ikke påbegyndt**. | Dette indgår i projektkontraktlinjens milepæl og fakturaen. |
| Linjebeløb | Hurtig oprettelse | Beløbet eller værdien af den milepæl, der vil blive faktureret kunden. | Dette felt indgår i projektkontraktlinjens milepæl og fakturaen, |
| Moms | Hurtig oprettelse | Det momsbeløb, der anvendes på milepælen. | Dette indgår i projektkontraktlinjens milepæl og fakturaen. |

4. Vælg **Gem og luk**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]