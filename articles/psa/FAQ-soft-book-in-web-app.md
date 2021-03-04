---
title: Hvordan foretager jeg en "foreløbig reservation" af ressourcer i appversion 2.x?
description: I denne artikel beskrives, hvordan du midlertidigt kan reservere medlemmer af projektteamet med Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6bd13c448f4ce16fb93843df54f26cdd9bb884f4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146476"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Hvordan foretager jeg en "foreløbig reservation" af ressourcer i webappen (Project Service-app v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Du kan planlægge midlertidigt eller "foreløbigt reservere" en ressource til et projektteam for at vise, at du har planer om at tildele ressourcen til et projekt. Foreløbige reservationer forbruger ikke en ressources ledig kapacitet. Foreløbigt reserverede teammedlemmer kan ikke tildeles til projektopgaver. Kun ressourcer med status Definitivt reserveret og bekræftelsestypen Bekræftet kan tildeles til opgaver (hvis de har tilstrækkelig mange definitivt reserverede timer at dække det tildelte arbejde).

Foreløbigt reserverede teammedlemmer vises i gitteret Teammedlem med deres foreløbige timer, der vises i kolonnen Reservér foreløbigt. De vises også i planlægningsområdet. Igen, de angiver ikke et forbrug af kapacitet, fordi foreløbige reservationer ikke forbruger en ressources kapacitet.

Der er tre måder at foretage en foreløbig reservation af et teammedlem på i et projekt med Project Service version 2.x. Du kan reservere foreløbigt i planlægningsområdet ved at bruge funktionen Vedligehold reservationer eller ved at oprette en generisk ressource. Disse metoder beskrives nedenfor.

## <a name="soft-book-with-the-schedule-board"></a>Reserver foreløbigt med planlægningsområdet

Når du vil foretage en foreløbig reservation med planlægningsområdet, skal du gøre følgende: 
1. Åbn planlægningsområdet.
2. Vælg fanen Projekt i panelet Krav til reservationer i planlægningsområdet.
3. Find det projekt, du vil foretage en foreløbige reservation af en ressource til. Hvis du har mange projekter, skal du klikke på kolonneoverskriften Projekt og derefter bruge filteret til at finde dit projekt.
4. Klik på projektet, og træk det og slip det på ressourcens tidsgitter.
5. Derved åbnes panelet Opret ressourcereservation til højre. Juster start-og slutdato, vælg reservationsstatus Foreløbig, og angiv timerne. 
6. Klik på Reservér.
7. Tilbage i projektet vises ressourcen nu som et teammedlem med de foreløbigt reserverede timer i kolonnen Reservér foreløbigt.

Bemærk, at du ikke kan tildele dem til opgaver i arbejdsopgavehierarki (WBS), fordi ressourcer skal komme reserveres definitivt i teamet for at blive tildelt.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Foretage en foreløbig reservation ved hjælp af funktionen Vedligeholde reservationer

Når du vil foretage en foreløbig reservation ved hjælp af Vedligehold reservationer, skal du gøre følgende:
1. Klik på Ny fra teammedlemsgitteret.
2. Vælg den reserverbare ressource, rolle, fra/til.
3. Vælg en anden allokeringsmetode end Ingen:
- Fuld kapacitet
- Kapacitet som procentdel
- Efter timer - jævn fordeling
- Efter timer - flest timer først i perioden
4. Klik på Gem. Du kan se ressourcen i teamgitteret og vedkommendes timer, der er angivet som Definitiv.
5. Du kan vedligeholde ressourcens reservationer ved at klikke på Vedligehold reservationer.
6. Når planlægningsområdet åbnes, skal du udvide ressourcen for at få vist hans eller hendes reservationer. Du kan se reservationen angivet som Definitiv.
7. Højreklik på reservationen, og vælg Reservér foreløbigt og derefter Foreløbigt under Skift status. Status for reservation er nu Foreløbig.
8. Når du har lukket planlægningsområdet, kan du se, at timerne for ressourcen er ændret fra Definitiv til Foreløbig i teammedlemsgitteret.
Bemærk, at hvis du reserverer en ressource definitivt til teamet og derefter tildeler ressourcen opgaver i WBS, når du bruger Vedligehold reservationer til at ændre status fra Definitiv til Foreløbig, fjernes tildelingerne fra opgaver for den pågældende ressource, fordi kun definitivt reserverede ressourcer kan tildeles til opgaver.

## <a name="soft-book-by-creating-a-generic-resource"></a>Foretage en foreløbig reservation ved at oprette en generisk ressource

Du kan oprette en foreløbig reservation ved at oprette et generisk ressourceteammedlem, fuldføre via planlægningsområdet eller Anmodning om ressourcer og ændre typen under reservationen.
Det kan du gøre ved hjælp af følgende procedure:

1. Tildel roller i projektets WBS til de opgaver, du vil oprette generiske teammedlemmer for.
2. Klik på Opret projektteam.
3. Vælg den generiske ressource i projektteamets medlemsgitter, og klik på Reservér.
4. Vælg den ressource, som du vil reservere, i planlægningsområdet.
5. I panelet Opret ressourcereservation i planlægningsområdet skal du ændre reservationsstatus til Foreløbig.
6. Klik på Reservér eller Reservér og afslut.

Når du har lukket planlægningsområdet, kan du se den valgte ressource, der er føjet til teamet med Foreløbigt reserverede timer og tildelte timer. Du kan også se, at den generiske ressource forbliver i teamet som et tegn på, at opgaverne er tilknyttet et foreløbigt reserveret teammedlem.

Når du er klar til at ændre en foreløbigt reserveret teammedlemsressource til et definitivt reserveret teammedlem, så du kan tildele ressourcen til opgaver, skal du gøre følgende:

1. Vælg ressourcen, og klik på Vedligehold reservationer.
2. Når planlægningsområdet åbnes, skal du udvide ressourcen for at få vist hans eller hendes reservationer. Du kan se reservationen markeret som Foreløbig.
3. Højreklik på reservationen, og vælg Reservér definitivt og derefter Definitivt under Skift status. Status for reservation er nu Definitiv.
4. Når du har lukket planlægningsområdet, kan du se, at timerne for ressourcen er ændret fra Foreløbig til Definitiv i teammedlemsgitteret. Du kan nu tildele ressourcen til opgaver (hvis der er overensstemmelse mellem de definitivt reserverede timer og indsatstimerne i opgaven, der skal tildeles). Bemærk, at hvis du har fulgt trinnene for opfyldelse af generisk ressource i punkt #3 ovenfor, og du ændrer status for den foreløbige reserverbare ressource til definitiv, fjernes det generiske teammedlem fra teamet.
