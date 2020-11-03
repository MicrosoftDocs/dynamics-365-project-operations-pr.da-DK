---
title: Forskudskontrakter og kontrakter baseret på forskudshonorar
description: Dette emne indeholder oplysninger om kontraktmodeller, der er baseret på forskudshonorarer eller forskud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ccf8ff4fa52fa6ff9fe534dfbe6736afc24ffba
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087862"
---
# <a name="advances-and-retainer-based-contracts"></a>Forskudskontrakter og kontrakter baseret på forskudshonorar 


_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dynamics 365 Project Operations understøtter kontrakter baseret på forskudshonorarer. En kontrakt, der er baseret på forskudshonorarer, er et forhandlet sæt ligeligt fordelte betalinger, som kunden faktureres for i hele projektets varighed. Denne kontrakttype bruges typisk til faktureringsmodeller, der er baseret på tid og materiale eller forbrug, hvor der er behov for at give kunden en forudsigelig plan for fakturering og betaling. Faktiske omsætningsoplysninger periodiseret i hver periode afstemmes mod den betaling, der modtages fra kunden i begyndelsen af perioden. I overensstemmelse med konceptet med faktureringsmodellen for tid og materiale kan omsætningsværdierne periodiseret i de enkelte perioder variere med de påløbne omkostninger. Hvis den periodiserede omsætning er større end det beløb, der modtages i begyndelsen af perioden, kan det pågældende projekts leveringsvirksomhed gøre følgende:

- Kun fakturer kunden for den overskydende del 
- Udskyde afstemningen af omsætningen til næste faktureringsperiode og udarbejde en endelig faktura ved projektets afslutning for eventuelle resterende ikke-afstemt omsætning

Den væsentligste forskel i Project Operations mellem en kontraktmodel, der er baseret på forskudshonorarer, og en kontraktmodel, der er baseret på fast pris, er, at fakturabeløbet ikke er knyttet til eller bundet af de påløbne omkostninger i kontraktmodellen, der er baseret på fast pris. Fakturering følger en milepælsbaseret fremgangsmåde, der er tilpasset de omkostninger, som er påløbet i den pågældende periode. I en kontrakt, der er baseret på forskudshonorarer, registreres den omsætning, der kan faktureres, baseret på faktureringsmetoden på kontraktlinjen. Når faktureringsmetoden er tid og materiale, er den fakturerbare omsætning bundet til de omkostninger, der er påløbet i en given periode, og kan variere fra periode til periode. Kunden faktureres dog kun det beløb, der er angivet i det periodiske forskudshonorar. Systemet bruger en anden faktura i slutningen af perioden til at afstemme den fakturerbare omsætning, der er registreret i perioden i forhold til det beløb, kunden blev faktureret for i starten af perioden.

Fordelen ved denne metode er, at kundens omkostninger bliver forudsigelige i planlægning af forskudshonoraret i modsætning til en typisk tids- og materialemodel. Den organisation, der leverer projektet, kan også få dækket risikoen i relation til at opkræve de omkostninger, der er påløbet som følge af stigninger i omfang, hvilket ikke ville have været muligt i en fast pris-model.

Ud over en periodisk plan, der er baseret på forskudshonorar, kan Project Operations registrere et engangsforskud fra en kunde og afstemme det i forhold til de forskellige projektomkostningskomponenter.

Forskudshonoraret i Project Operations er ikke tilgængelig til brug, før det er faktureret til kunden. Dette angives ved følgende felter på undergitteret for forskud og forskudshonorarer.

| Felt | Relevans, formål og vejledning | Downstream-virkning |
| --- | --- | --- |
| Beløb til rådighed | Det beløb, der kan bruges på posten med forskudshonorar eller forskud. | Indtil forskuddet eller forskudshonoraret er blevet faktureret, er det ikke muligt at anvende beløbet, hvilket betyder, at det disponible beløb er nul. |
| Anvendt beløb | Det beløb, der allerede er brugt på forskudshonorar eller forskud. | Et forskud eller forskudshonorar kan være delvist afstemt på en faktura med faktiske omkostninger, hvor en del vil være markeret som allerede anvendt eller forbrugt. Resten af forskuddet eller forskudshonoraret er tilgængeligt til afstemning på fremtidige fakturaer med faktiske omkostninger. |
