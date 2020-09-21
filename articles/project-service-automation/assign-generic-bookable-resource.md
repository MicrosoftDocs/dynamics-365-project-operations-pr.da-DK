---
title: Tildele generiske, reserverbare ressourcer til en opgave og et projektteam
description: Denne emne indeholder oplysninger om reservation af generiske ressourcer til opgaver og projektteam.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750640"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Tildele en opgave generiske reserverbare ressourcer og oprette ressourcekrav 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Udover at reservere og tildele navngivne eller faktiske ressourcer for projektet, kan du tildele projektopgaver generiske ressourcer. Disse ressourcer kan fungere som pladsholdere for navngivne ressourcer, indtil du er klar til at bemande dit projekt med navngivne ressourcer. 

1. I Project Service Automation (PSA) skal du åbne **Projekt**-siden og bruge fanen **Tidsplan** til at angive navnet på den generiske ressource i cellen **Ressource** i tidsplanen. Du kan også klikke på ikonet **Ressource** i cellen for at åbne ressourcevælgeren og derefter angive navnet på den generiske ressource, du vil oprette.

![Oprette og tildele et generisk teammedlem](media/RM-how-to-9.png)

Derved åbnes panelet **Hurtig oprettelse: Medlem af projektteam**. 

2. Angiv rollen og organisationsenheden for det generiske ressourceteammedlem, og klik derefter på **Gem**.

![Hurtig oprettelse af generisk teammedlem](media/RM-how-to-10.png)

3. Når du har oprettet det nye generiske ressourceteammedlem, tildeles det opgaven. Du kan fortsætte med at tildele den pågældende generiske ressource til andre opgaver i opgaveplanlægningen.

![Tildeling af eksisterende generisk teammedlem til opgaver](media/RM-how-to-11.png)

4. Når du har tildelt den generiske ressource, kan du oprette et ressourcekrav og opfylde det ved at reservere eller sende en ressourceanmodning direkte til en ressourceansvarlig.

![Generering af et krav til et generisk teammedlem](media/RM-how-to-12.png)

Udover at kunne bruge ressourcevælgeren som nævnt ovenfor i teammedlemsgitteret kan du tilføje generiske ressourcer direkte. Ressourcerne tilføjes med et ressourcekrav, der er baseret på de start- og slutdatoer og den fordelingsmetode, der er angivet i panelet **Hurtig oprettelse: Medlem af projektteam**.

Du kan se en forskel, hvis du tilføjer det generiske teammedlem direkte og derefter tildeler flere opgaver til den generiske ressource end de har de påkrævede timer til at dække. Klik på **Generér krav** for at gendanne kravet for at afstemme de påkrævede timer med tildelinger.

Du kan også klikke på linket **Ressourcekrav** i teamgitteret for at åbne kravet og tilføje færdigheder, foretrukne ressourcer osv.

![Ressourcekrav](media/RM-how-to-13.png)

