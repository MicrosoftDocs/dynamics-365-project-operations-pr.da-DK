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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074187"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="8ff7b-103">Tildele en opgave generiske reserverbare ressourcer og oprette ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="8ff7b-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8ff7b-104">Udover at reservere og tildele navngivne eller faktiske ressourcer for projektet, kan du tildele projektopgaver generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="8ff7b-105">Disse ressourcer kan fungere som pladsholdere for navngivne ressourcer, indtil du er klar til at bemande dit projekt med navngivne ressourcer.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="8ff7b-106">I Project Service Automation (PSA) skal du åbne **Projekt** -siden og bruge fanen **Tidsplan** til at angive navnet på den generiske ressource i cellen **Ressource** i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="8ff7b-107">Du kan også klikke på ikonet **Ressource** i cellen for at åbne ressourcevælgeren og derefter angive navnet på den generiske ressource, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Oprette og tildele et generisk teammedlem](media/RM-how-to-9.png)

<span data-ttu-id="8ff7b-109">Derved åbnes panelet **Hurtig oprettelse: Medlem af projektteam**.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="8ff7b-110">Angiv rollen og organisationsenheden for det generiske ressourceteammedlem, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Hurtig oprettelse af generisk teammedlem](media/RM-how-to-10.png)

3. <span data-ttu-id="8ff7b-112">Når du har oprettet det nye generiske ressourceteammedlem, tildeles det opgaven.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="8ff7b-113">Du kan fortsætte med at tildele den pågældende generiske ressource til andre opgaver i opgaveplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Tildeling af eksisterende generisk teammedlem til opgaver](media/RM-how-to-11.png)

4. <span data-ttu-id="8ff7b-115">Når du har tildelt den generiske ressource, kan du oprette et ressourcekrav og opfylde det ved at reservere eller sende en ressourceanmodning direkte til en ressourceansvarlig.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generering af et krav til et generisk teammedlem](media/RM-how-to-12.png)

<span data-ttu-id="8ff7b-117">Udover at kunne bruge ressourcevælgeren som nævnt ovenfor i teammedlemsgitteret kan du tilføje generiske ressourcer direkte.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="8ff7b-118">Ressourcerne tilføjes med et ressourcekrav, der er baseret på de start- og slutdatoer og den fordelingsmetode, der er angivet i panelet **Hurtig oprettelse: Medlem af projektteam**.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="8ff7b-119">Du kan se en forskel, hvis du tilføjer det generiske teammedlem direkte og derefter tildeler flere opgaver til den generiske ressource end de har de påkrævede timer til at dække.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="8ff7b-120">Klik på **Generér krav** for at gendanne kravet for at afstemme de påkrævede timer med tildelinger.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="8ff7b-121">Du kan også klikke på linket **Ressourcekrav** i teamgitteret for at åbne kravet og tilføje færdigheder, foretrukne ressourcer osv.</span><span class="sxs-lookup"><span data-stu-id="8ff7b-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Ressourcekrav](media/RM-how-to-13.png)

