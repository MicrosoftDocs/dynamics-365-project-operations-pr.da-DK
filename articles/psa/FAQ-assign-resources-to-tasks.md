---
title: Tildele en ressource til en opgave
description: Dette emne indeholder oplysninger om, hvordan du tildeler ressourcer til opgaver.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074361"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="b684f-103">Tildele en ressource til en opgave</span><span class="sxs-lookup"><span data-stu-id="b684f-103">Assign a resource to a task</span></span>

<span data-ttu-id="b684f-104">Der findes tre metoder til at tildele en ressource til en opgave i Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b684f-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="b684f-105">Reservere en ressource som et teammedlem og derefter tildele ressourcen til en opgave</span><span class="sxs-lookup"><span data-stu-id="b684f-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="b684f-106">Du kan føje en ressource til projektteamet og derefter tildele ressourcen til opgaver i projektplanen.</span><span class="sxs-lookup"><span data-stu-id="b684f-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="b684f-107">I fanen **Teammedlem** kan du tilføje et nyt teammedlem ved at vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b684f-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="b684f-108">Panelet **Hurtig oprettelse af teammedlem** åbnes, hvor du kan vælge det reserverbare ressourcenavn og angive en rolle.</span><span class="sxs-lookup"><span data-stu-id="b684f-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="b684f-109">Vælg en af følgende allokeringsmetoder til reservation af ressourcen:</span><span class="sxs-lookup"><span data-stu-id="b684f-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="b684f-110">**Fuld kapacitet** reserverer ressourcens fulde kapacitet for de angivne fra- og til-datoer.</span><span class="sxs-lookup"><span data-stu-id="b684f-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="b684f-111">**Kapacitet som procentdel** reserverer ressourcen med en procentdel af ressourcens kapacitet på de angivne fra- og til-datoer.</span><span class="sxs-lookup"><span data-stu-id="b684f-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="b684f-112">**Efter timer - jævn fordeling** reserverer ressourcen i et angivet antal timer og distribuerer dem jævnt pr. dag over de angivne fra- og til-datoer.</span><span class="sxs-lookup"><span data-stu-id="b684f-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="b684f-113">**Efter timer - flest timer først i perioden** reserverer ressourcen i et angivet antal timer og distribuerer timerne pr. dag med de største udgifter først i perioden hen over de angivne fra- og til-datoer.</span><span class="sxs-lookup"><span data-stu-id="b684f-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="b684f-114">**Ingen** tilføjer ressourcen til teamet, men opretter ikke eventuelle reservationer, der kan absorbere deres kapacitet.</span><span class="sxs-lookup"><span data-stu-id="b684f-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="b684f-115">I gitteret **Tidsplan** for en opgave skal du vælge ikonet **Resource** i ressourcecellen og derefter vælge det teammedlem, du lige har tilføjet, under **Teammedlemmer** .</span><span class="sxs-lookup"><span data-stu-id="b684f-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="b684f-116">I fanerne **Teammedlem** og **Afstemning** viser ressourcen reserverede timer og tildelte timer.</span><span class="sxs-lookup"><span data-stu-id="b684f-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="b684f-117">Timerne bør være ens, men det er ikke noget krav, fordi reservationer og tildelinger ikke er tæt sammenknyttede.</span><span class="sxs-lookup"><span data-stu-id="b684f-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="b684f-118">Fanen **Afstemning** giver dig oplysninger om, hvornår de er forskellige, f.eks. når du tildeler en ressource flere timer, end du har reserveret.</span><span class="sxs-lookup"><span data-stu-id="b684f-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="b684f-119">Hvis du har brug for det, kan du korrigere oplysningerne ved at udvide ressourcens reservationer eller ændre tildelingen.</span><span class="sxs-lookup"><span data-stu-id="b684f-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="b684f-120">Oprette et generisk teammedlem via opgavetildeling</span><span class="sxs-lookup"><span data-stu-id="b684f-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="b684f-121">Når du opretter et generisk teammedlem via opgavetildeling, opretter du en pladsholder eller en generisk ressource, der beskriver egenskaberne for den navngivne ressource, som du i sidste ende vil have til at arbejde med opgaverne.</span><span class="sxs-lookup"><span data-stu-id="b684f-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="b684f-122">Du kan derefter oprette et krav (eller sende en anmodning ved hjælp af kravet), der bruges til at søge efter, og reservere den navngivne ressource.</span><span class="sxs-lookup"><span data-stu-id="b684f-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="b684f-123">Vælg **Resource** -ikonet i ressourcecellen i gitteret **Planlægning** for en opgave.</span><span class="sxs-lookup"><span data-stu-id="b684f-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="b684f-124">Skriv et navn, der skal fungere som pladsholderressourcens navn.</span><span class="sxs-lookup"><span data-stu-id="b684f-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="b684f-125">F.eks. programadministrator.</span><span class="sxs-lookup"><span data-stu-id="b684f-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="b684f-126">Vælg **Opret** , og angiv rollen for den generiske ressource i feltet **Hurtig oprettelse af projektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="b684f-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="b684f-127">Du kan fortsætte med at tildele opgaver til denne pladsholderressource ved at vælge ressourcen i **Resourcevælgeren** for opgaven.</span><span class="sxs-lookup"><span data-stu-id="b684f-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="b684f-128">De er angivet under **Teammedlemmer**.</span><span class="sxs-lookup"><span data-stu-id="b684f-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="b684f-129">Når du har tildelt den generiske ressource, skal du vælge den generiske ressource under fanen **Team** og derefter vælge **Generer krav** for at oprette et ressourcekrav for den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="b684f-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="b684f-130">Vælg **Reservér** for den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="b684f-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="b684f-131">Du kan derefter bruge planlægningsområdet til at finde og reservere en faktisk ressource.</span><span class="sxs-lookup"><span data-stu-id="b684f-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="b684f-132">Du kan også sende kravet til en ressourceansvarlig til indfrielse.</span><span class="sxs-lookup"><span data-stu-id="b684f-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="b684f-133">Når den generiske ressource er indfriet med en navngivet ressource, fjernes den generiske ressource fra teamet, og opgavetildelingerne for den generiske ressource tildeles til den navngivne ressource, der opfyldte ressourcekravet til den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="b684f-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="b684f-134">Tildele en navngivet ressource fra listen over alle reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="b684f-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="b684f-135">Du kan bruge søgefeltet i **Resourcevælgeren** til at søge i alle de reserverbare ressourcer i Project Service og tildele dem til en opgave.</span><span class="sxs-lookup"><span data-stu-id="b684f-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="b684f-136">Ressourcer, der er tildelt på denne måde, føjes til teamet uden reservationer.</span><span class="sxs-lookup"><span data-stu-id="b684f-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="b684f-137">Dette svarer til at tilføje et gruppemedlem og vælge Ingen som fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="b684f-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="b684f-138">Ressourcen vises under fanen **Team** og fanen **Afstemning** som ressourcer med tildelinger og et reservationsunderskud.</span><span class="sxs-lookup"><span data-stu-id="b684f-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="b684f-139">Reservér dem, hvis du vil bruge deres tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="b684f-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="b684f-140">Vælg **Resource** -ikonet i ressourcecellen i gitteret **Planlægning** for en opgave.</span><span class="sxs-lookup"><span data-stu-id="b684f-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="b684f-141">Begynd at skrive et navn.</span><span class="sxs-lookup"><span data-stu-id="b684f-141">Start typing a name.</span></span> <span data-ttu-id="b684f-142">Søgeresultaterne for navnet vises i **Resourcevælgeren** under **Andre ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="b684f-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="b684f-143">Vælg den ressource, som du vil tildele til opgaven.</span><span class="sxs-lookup"><span data-stu-id="b684f-143">Select the resource that you want to assign to the task.</span></span>

