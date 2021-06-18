---
title: Tildele generiske, reserverbare ressourcer til en opgave og et projektteam
description: Denne emne indeholder oplysninger om reservation af generiske ressourcer til opgaver og projektteam.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: a1e22337d3fd3e7ff4147a9547fd3c272f4185d3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009384"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Tildele en opgave generiske reserverbare ressourcer og oprette ressourcekrav 

[!include [banner](../includes/psa-now-project-operations.md)]

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]