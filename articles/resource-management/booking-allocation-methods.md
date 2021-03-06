---
title: Reservationsallokeringsmetoder
description: Dette emne indeholder oplysninger om, hvordan metoder til reservationsfordeling fungerer i Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 74f8889022e42a7bbd37879df870401c0e103446
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897669"
---
# <a name="booking-allocation-methods"></a>Reservationsallokeringsmetoder

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Uanset om du tilføjer et teammedlem direkte i et projekt under fanen **Team** eller reserverer en ressource til et projekt eller krav i planlægningsområdet, er der forskellige reservationsallokeringsmetoder, som du kan bruge. I dette emne forklares, hvordan de enkelte metoder fungerer, og hvilke metoder som kan føre til overreservation af ressourcer.

## <a name="booking-allocation-methods"></a>Reservationsallokeringsmetoder

Du kan benytte seks metoder til reservationsfordeling:

- [Fuld kapacitet](#full)
- [Resterende kapacitet](#remaining)
- [Kapacitet som procentdel](#percentage)
- [Fordel timer jævnt](#evenly)
- [Flest timer først i perioden](#front)
- [Ingen](#none)

### <a name="full-capacity"></a><a name="full"></a>Fuld kapacitet 
Fuld kapacitet-metoden reserverer ressourcens fulde kapacitet for de angivne fra- og til-datoer. Hvis en ressource f.eks. har en kalender med angivelse af otte timers arbejde om dagen fem dage om ugen, reserveres ressourcen i 40 timer, hvis du angiver en start- og slutdato, der omfatter fem arbejdsdage. Reservationen foretages uden hensyn til ressourcens resterende kapacitet. Hvis en ressource allerede er reserveret i den pågældende periode, reserveres de 40 timer som yderligere timer, hvilket potentielt kan føre til overreservationer.

### <a name="remaining-capacity"></a><a name="remaining"></a>Resterende kapacitet
Resterende kapacitet-metoden er kun tilgængelig, når du reserverer direkte til et projekt ved hjælp af planlægningsområdet. Med denne metode reserveres ressourcens ledige kapacitet inden for det valgte datointerval. Hvis en ressource f.eks. har en kapacitet på 40 timer om ugen, og der allerede er reserveret 10 timer, resulterer reservation for den samme uge i reservation af de resterende 30 timers kapacitet for den pågældende uge.

### <a name="percentage-capacity"></a><a name="percentage"></a>Kapacitet som procentdel
Metoden kapacitet som procentdel reserverer ressourcen med en procentdel af kapaciteten på de angivne fra- og til-datoer. Hvis f.eks. en ressources kalender er angivet til otte timers arbejde om dagen fem dage om ugen, reserveres ressourcen i 20 timer, hvis du angiver en start- og slutdato, der omfatter fem arbejdsdage med 50 % kapacitet. De enkelte reservationer pr. dag fordeles ligeligt over perioden, fire timer om dagen i dette eksempel. Reservationen foretages uden hensyn til ressourcens resterende kapacitet. Hvis ressourcen allerede er reserveret i den pågældende periode til andre projekter, reserveres de 20 timer som yderligere timer, hvilket potentielt kan føre til overreservationer.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Fordel timer jævnt
Metoden timer med jævn fordeling reserverer ressourcen i et angivet antal timer og distribuerer tiden jævnt pr. dag over de angivne fra- og til-datoer. Hvis du f.eks. reserverer en ressource i 20 timer over en periode på fem dage, fordeler denne metode de 20 timer jævnt på fire timer om dagen. Reservationen foretages uden hensyn til ressourcens resterende kapacitet. Hvis ressourcen allerede er reserveret i den pågældende periode til andre projekter, reserveres de 20 timer som yderligere timer, hvilket potentielt kan føre til overreservationer.

### <a name="front-load-hours"></a><a name="front"></a>Flest timer først i perioden
Metoden flest timer først i perioden reserverer ressourcen i et angivet antal timer og distribuerer timerne pr. dag med de største udgifter først i perioden hen over de angivne fra- og til-datoer. Flest timer først i perioden forbruger ressourcens ledige kapacitet i rækkefølgen "først-ind-først-forbrugt". Hvis en ressources arbejdsplan f.eks. er otte timer om dagen fem dage om ugen, og ressourcen ikke har nogen aktuelle reservationer, giver reservation af ressourcen i 20 timer over en periode på fem arbejdsdage følgende daglige reservationsmønster: 

|                           |    Dag 1    |    Dag 2    |    Dag 3    |    Dag 4    |    Dag 5    |    I alt    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Eksisterende reservationer**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Ny reservation**          |    8        |    8        |    4        |    0        |    0        |    20       |

Flest timer først i perioden-metoden tager eksisterende reservationer og ledig kapacitet i betragtning. F.eks., hvis den samme ressource allerede har 20 timers reservationer i arbejdsugen, forbruger de nye reservationer den resterende kapacitet på følgende måde:

|                     | Dag 1 | Dag 2 | Dag 3 | Dag 4 | Dag 5 | I alt |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Eksisterende reservationer** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Ny reservation**       | 0     | 0     | 4     | 8     | 8     | 20    |

Da den ledige kapacitet tages i betragtning, kan du modtage en fejlmeddelelse, hvis ressourcen ikke har nogen resterende kapacitet, der kan bruges af reservationen. Du kan ikke overbooke med denne metode.

### <a name="none"></a><a name="none"></a>Ingen
Ingen-metoden er kun tilgængelig, når du reserverer fra fanen **Team** i et projekt. Denne metode tilføjer ressourcen som et teammedlem i projektet, men opretter ikke nogen reservationer, der forbruger ressourcens kapacitet. Denne metode bruges, når det teammedlem, der er standardprojektleder, tilføjes, når der oprettes et projekt. Den projektadministratorbruger, der oprettede projektet, tilføjes som standard i projektet, så projektobjektposten har en ejer, og der er én godkender af projektet. Denne bruger ikke har nogen reservationer, så hvis du vil reservere ressourcen, kan du enten slette og derefter tilføje vedkommende igen ved hjælp af en anden allokeringsmetode eller føje ressourcen til opgaver og derefter bruge **Udvid reservationer** under fanen **Afstemning** til at oprette reservationer til tildelingerne.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Allokeringsmetoder, der fører til overbookning
Følgende allokeringsmetoder kan altså føre til overbookning, hvis ressourcen allerede er allokeret til andre projekter (eller til andre arbejdsordrer eller objekter, der kan planlægges):

- Fuld kapacitet
- Kapacitet som procentdel
- Fordele timer jævnt

Når du bruger en af disse tre allokeringsmetoder, får du ikke besked om, at ressourcen er overbooket. Du kan kun løse overreservationsproblemet ved hjælp af planlægningsområdet.
