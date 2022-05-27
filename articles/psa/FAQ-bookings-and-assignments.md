---
title: Ressourcereservationer, og hvordan de er relateret til opgavetildelinger
description: Dette emne indeholder oplysninger om, hvordan du administrerer navngivne ressourcer, ressourcereservationer og opgavetildelinger, og hvordan de er relateret til hinanden.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 953d7ca1995eae823fd29d0a9e85ff6a2a2eb59b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575472"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Ressourcereservationer, og hvordan de er relateret til opgavetildelinger

[!include [banner](../includes/psa-now-project-operations.md)]

Der er to måder, hvorpå navngivne ressourcer kan reserveres til et projektteam og tildeles til projektopgaver:

- Ressourcen kan reserveres direkte til et projekt og efterfølgende tildeles til projektopgaver.
- Opgaverne kan tildeles til en generisk ressource, som derefter kan bruges til at finde og erstatte den generiske ressource med en navngivet ressource. 

I begge tilfælde reserveres ressourcens kapacitet ved reservationshandlingen.

Den projektleder, der planlægger projektet, ejer projektplanen og tidsplanen. Projektlederen kan reservere ressourcer til projektet med profiler, der er angivet i projektplanen, ved at bruge den generiske ressource til tildeling og derefter oprette en ressourceanmodning fra den. Projektlederen kan reservere ressourcer til et projekt og derefter tildele dem til opgaver, men det er ikke muligt at justere reservationsprofilerne med opgaveprofilerne. Reservationer påvirker ikke projektplanen.

Forestil dig et komplekst projekt med flere overlappende opgaver, hvor flere ressourcer af samme type skal arbejde samtidigt. Hvis en ressource får en profil, der adskiller sig fra den, der gælder for den samlede mængde tildelinger, er det vanskeligt at ændre opgaverne, så de svarer til profilen for reservationerne til deres separate opgaver og deres oprindelige profiler.

I eksemplet nedenfor er den samlede arbejdsmængde, der kræves af den samme ressource på et sæt bestående af fire opgaver, 62 timer over en periode på to uger, og der er en bestemt profil. Hvis ressourcen Bob er reserveret i 62 timer i de samme to uger, men med en anden profil, stemmer kravet og reservationerne overens.

| **Opgaveprofiler**    | **Timer i alt** | Ma 4-6 | Ti 5-6 | On 6-6 | To 7-6 | Fr 8-6 | Lø 9-6 | Sø 10-6 | Ma 11-6 | Ti 12-6 | On 13-6 | To 14-6 | Fr 15-6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Opgave 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Opgave 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Opgave 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Opgave 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totaler**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Bobs tilgængelighed
| **Ressourcereservation** | **Timer i alt** | Ma 4-6 | Ti 5-6 | On 6-6 | To 7-6 | Fr 8-6 | Lø 9-6 | Sø 10-6 | Ma 11-6 | Ti 12-6 | On 13-6 | To 14-6 | Fr 15-6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Der er dog ingen systematisk måde at tildele den reserverede timeprofil til opgaver på dagsbasis. Hvis projektlederen gerne vil ændre projektplanen for at imødekomme ressourcens tilgængelighed, skal han eller hun fjerne tildelingen og redigere alle opgaverne, så de svarer til reservationsprofilerne.

I det tilfælde at en organisation har givet både en projektleder og en ressourceansvarlig til opgave at udføre projektplanlægningen, opretter projektlederen tidsplanen, som omfatter at oprette en profil for det arbejde, der kræves. Den ressourceansvarlige må ikke kunne påvirke tidsplanen uden projektlederens vidende ved at ændre indsatsprofiler under reservationen af de faktiske ressourcer. Hvis den ressourceansvarlige indfrier noget andet end det, projektlederen anmodede om, skal de aftale indbyrdes, hvilke ændringer der er nødvendige i projektplanen.

Da reservationer og tildelinger ikke er tæt forbundne, er det muligt at reservere profiler, der adskiller sig fra opgaveprofilerne, eller at ændre tildelingerne, hvilket vil resultere i situationer, hvor reservationer og tildelinger ikke stemmer overens.

**Afstemningsvisning** gør det muligt for projektlederen at se reservationer og tildelinger for hvert enkelt medlem af projektteamet. Visningen bruger farver og skygge til at vise, hvor der er en uoverensstemmelse mellem et teammedlems reservationer og tildelinger. På grundlag af disse oplysninger kan projektlederen løse problemet ved enten at udvide ressourcereservationer for sager, hvor der er tildelinger og ingen reservationer, eller annullere reservationer, hvor ressourcer er reserveret, men ikke har tildelinger.

> [!NOTE]
> Hvis du flytter en opgave, som du selv har oprettet profiler for, gemmes disse profiler ikke. Profiler genoprettes ud fra projektkalenderen for at tage højde for ændringer i arbejdstimer og fridage. Dette er tilsigtet, eftersom systemet ikke kender formålet med den oprindelige profil og ikke kan finde ud af, om der er behov for at bevare denne profil i en ny tidsperiode. Da reservationer og tildelinger ikke er forbundne, bevarer reservationerne de oprindelige reservationsprofiler. I dette tilfælde skal du annullere og reservere igen til den nye tildelingsprofil.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
