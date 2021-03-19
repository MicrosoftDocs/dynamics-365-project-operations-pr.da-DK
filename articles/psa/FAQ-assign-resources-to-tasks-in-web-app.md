---
title: Hvordan tildeler jeg en reserverbar ressource til en opgave i webappen?
description: En oversigt over, hvordan du kan tildele reserverbare ressourcer.
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
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286286"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="f93d6-103">Hvordan tildeler jeg en reserverbar ressource til en opgave i webappen (Project Service-app v2.x)?</span><span class="sxs-lookup"><span data-stu-id="f93d6-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f93d6-104">Der findes to metoder til at tildele en ressource til en opgave i Project Service.</span><span class="sxs-lookup"><span data-stu-id="f93d6-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="f93d6-105">Du kan reservere en ressource som et teammedlem og derefter tildele den til en opgave.</span><span class="sxs-lookup"><span data-stu-id="f93d6-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="f93d6-106">Eller du kan oprette et generisk teammedlem via rolletildeling på opgaver, oprette et team og derefter indfri kravene til sikkerhedskopiering med en navngivet ressource.</span><span class="sxs-lookup"><span data-stu-id="f93d6-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="f93d6-107">Bemærk, at hvis du vil tildele en reserverbar ressource til en opgave, skal det reserverbare ressourceteammedlem have nok tilgængelige reservationer.</span><span class="sxs-lookup"><span data-stu-id="f93d6-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="f93d6-108">Status for reservationen skal være Bekræftelsestype for Reservér definitivt og status Bekræftet.</span><span class="sxs-lookup"><span data-stu-id="f93d6-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="f93d6-109">Hvis der ikke er tilstrækkeligt mange reservationer for ressourcen, fjerner Project Service tildelingen og viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="f93d6-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="f93d6-110">*Det er ikke muligt at tildele ressourcen til opgaven – Følgende ressource(r) har ikke tilstrækkeligt mange timer reservereret til projekt*</span><span class="sxs-lookup"><span data-stu-id="f93d6-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="f93d6-111">Reservere en ressource som et teammedlem og derefter tildele ressourcen til en opgave</span><span class="sxs-lookup"><span data-stu-id="f93d6-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="f93d6-112">Med denne metode kan du føje en ressource til projektteamet og derefter tildele opgaver til ressourcen i projektplanen.</span><span class="sxs-lookup"><span data-stu-id="f93d6-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="f93d6-113">Her kan du se, hvordan du gør dette:</span><span class="sxs-lookup"><span data-stu-id="f93d6-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="f93d6-114">I teammedlemsgitteret kan du tilføje et nyt teammedlem ved at vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f93d6-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="f93d6-115">På skærmbilledet Hurtig oprettelse for teammedlemmer kan du vælge det reserverbare ressourcenavn og angive en rolle.</span><span class="sxs-lookup"><span data-stu-id="f93d6-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="f93d6-116">Vælg **Fra** og **Til** datoerne.</span><span class="sxs-lookup"><span data-stu-id="f93d6-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="f93d6-117">![Skærmbillede af tilføjelse af gruppemedlem](media/FAQ-Resources-to-Tasks2-1.png "Skærmbillede af tilføjelse af gruppemedlem")</span><span class="sxs-lookup"><span data-stu-id="f93d6-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="f93d6-118">Vælg en af følgende allokeringsmetoder til reservation af ressourcen:</span><span class="sxs-lookup"><span data-stu-id="f93d6-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="f93d6-119">**Fuld kapacitet** reserverer ressourcens fulde kapacitet for de angivne fra- og til-datoer.</span><span class="sxs-lookup"><span data-stu-id="f93d6-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="f93d6-120">**Kapacitet som procentdel** reserverer ressourcen med en procentdel af ressourcens kapacitet på de angivne fra- og til-datoer.</span><span class="sxs-lookup"><span data-stu-id="f93d6-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="f93d6-121">**Efter timer - jævn fordeling** reserverer ressourcen i et angivet antal timer og distribuerer dem jævnt pr. dag over de angivne fra- og til-datoer.</span><span class="sxs-lookup"><span data-stu-id="f93d6-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="f93d6-122">**Efter timer - flest timer først i perioden** reserverer ressourcen i et angivet antal timer og distribuerer timerne pr. dag med de største udgifter først i perioden hen over de angivne fra- og til-datoer.</span><span class="sxs-lookup"><span data-stu-id="f93d6-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="f93d6-123">Du skal ikke vælge **Ingen**, fordi det føjer ressourcen til teamet, men opretter ikke nogen reservationer, der forbruger ressourcens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="f93d6-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="f93d6-124">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f93d6-124">Select **Save**.</span></span>

    <span data-ttu-id="f93d6-125">Bemærk, at reservationstimerne skal kunne dække indsatstimer og datointervaller for de opgaver, som du tildeler denne ressource til.</span><span class="sxs-lookup"><span data-stu-id="f93d6-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="f93d6-126">Hvis de ikke er justerede, kan du ikke tildele ressourcen til opgaven.</span><span class="sxs-lookup"><span data-stu-id="f93d6-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="f93d6-127">Klik på ressourcecellens rulleliste i arbejdsopgavehierarkiet (WBS) for opgaven.</span><span class="sxs-lookup"><span data-stu-id="f93d6-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="f93d6-128">Derefter:</span><span class="sxs-lookup"><span data-stu-id="f93d6-128">Then:</span></span> 

    1. <span data-ttu-id="f93d6-129">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="f93d6-129">Select **Add**.</span></span>
    2. <span data-ttu-id="f93d6-130">Vælg rullelisten under **Ressourcer**, og vælg det teammedlem, du har tilføjet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="f93d6-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="f93d6-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f93d6-131">Select **OK**.</span></span> <span data-ttu-id="f93d6-132">Teammedlemmet tildeles nu til opgaven.</span><span class="sxs-lookup"><span data-stu-id="f93d6-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="f93d6-133">![Skærmbillede af tilføjelse af ressourcer med WBS](media/FAQ-Resources-to-Tasks2-2.png "Skærmbillede af tilføjelse af ressourcer med WBS")</span><span class="sxs-lookup"><span data-stu-id="f93d6-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="f93d6-134">Du kan se den samlede mængde af ressourcens tildelte timer under Tildelte timer i teammedlemsgitteret.</span><span class="sxs-lookup"><span data-stu-id="f93d6-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="f93d6-135">Den vil være mindre end eller lig med de reserverede timer for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="f93d6-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="f93d6-136">![Skærmbillede af tildelte timer for en ressource](media/FAQ-Resources-to-Tasks2-3.png "Skærmbillede af tildelte timer for en ressource")</span><span class="sxs-lookup"><span data-stu-id="f93d6-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="f93d6-137">Hvis den opgave, du forsøger at tildele til ressourcen, starter efter slutdatoen for ressourcereservationer, vises ressourcen ikke på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="f93d6-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="f93d6-138">Bemærk, at du kan tildele en ressource til flere timer end deres reserverede timer, hvis ressourcen har en vis mængde ikke-tildelt kapacitet.</span><span class="sxs-lookup"><span data-stu-id="f93d6-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="f93d6-139">I dette tilfælde tildeles ressourcen kun delvist op til deres reservationer.</span><span class="sxs-lookup"><span data-stu-id="f93d6-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="f93d6-140">Du kan se disse resterende ikke-tildelte opgavetimer ved at føje kolonnen Ubemandede timer til arbejdsopgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f93d6-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="f93d6-141">Hvis der er tildelt ressourcer til ressourcens reserverede timer (reserverede timer er lig med tildelte timer), vises følgende fejlmeddelelse, når du forsøger at tildele yderligere opgaver til ressourcen:</span><span class="sxs-lookup"><span data-stu-id="f93d6-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="f93d6-142">*Det er ikke muligt at tildele ressourcen til opgaven – Følgende ressource(r) har ikke tilstrækkeligt mange timer reservereret til projekt.*</span><span class="sxs-lookup"><span data-stu-id="f93d6-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="f93d6-143">Derudover tilføjes det teammedlem, der er standardprojektleder, og som føjes til teamet, når du opretter projektet, uden eventuelle reservationer og kan ikke tildeles til en opgave.</span><span class="sxs-lookup"><span data-stu-id="f93d6-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="f93d6-144">De vises ikke på rullelisten med ressourcer for opgaver.</span><span class="sxs-lookup"><span data-stu-id="f93d6-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="f93d6-145">Hvis du vil tildele denne ressource, skal du fjerne vedkommende fra teamet og derefter tilføje ham eller hende igen med en anden allokeringsmetode end Ingen.</span><span class="sxs-lookup"><span data-stu-id="f93d6-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="f93d6-146">Grunden til, at de føjes til teamet, når projektet oprettes, er, at et projekt har mindst én projektgodkender som standard.</span><span class="sxs-lookup"><span data-stu-id="f93d6-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="f93d6-147">Oprette et generisk teammedlem via rolletildeling på opgaver</span><span class="sxs-lookup"><span data-stu-id="f93d6-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="f93d6-148">Denne metode sikrer, at ressourcer har tilstrækkelige reservationer for opgaver.</span><span class="sxs-lookup"><span data-stu-id="f93d6-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="f93d6-149">Først skal du oprette en pladsholder eller en generisk ressource, der beskriver egenskaberne for den navngivne ressource, som du i sidste ende vil have til at arbejde med opgaverne, ved at oprette et team, når du har tildelt roller til opgaverne.</span><span class="sxs-lookup"><span data-stu-id="f93d6-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="f93d6-150">Her kan du se, hvordan du gør dette:</span><span class="sxs-lookup"><span data-stu-id="f93d6-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="f93d6-151">Vælg en opgave i arbejdsopgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f93d6-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="f93d6-152">Vælg ikonet **Tildelt rolle** på rullelisten i ressourcecellen.</span><span class="sxs-lookup"><span data-stu-id="f93d6-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="f93d6-153">Vælg rullelisten **Rolle**, og vælg rollen for den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="f93d6-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="f93d6-154">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f93d6-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="f93d6-155">![Skærmbillede af anvendelse af WBS til at tilføje ressourcer](media/FAQ-Resources-to-Tasks2-4.png "Skærmbillede af anvendelse af WBS til at tilføje ressourcer")</span><span class="sxs-lookup"><span data-stu-id="f93d6-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="f93d6-156">Når du har tildelt roller til opgaver i WBS, kan du vælge **Opret projektteam**.</span><span class="sxs-lookup"><span data-stu-id="f93d6-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="f93d6-157">Project Service opretter det mindste antal generiske teammedlemmer baseret på roller, ressourceorganisationsenheder og projektkalender ved at sammenlægge de tildelte opgaver.</span><span class="sxs-lookup"><span data-stu-id="f93d6-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="f93d6-158">![Skærmbillede af oprettelse af projektteam](media/FAQ-Resources-to-Tasks2-5.png "Skærmbillede af oprettelse af projektteam")</span><span class="sxs-lookup"><span data-stu-id="f93d6-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="f93d6-159">I gitteret Teammedlem kan se du ressourcer af typen Generisk ressource med navnet på rollen og stillingen.</span><span class="sxs-lookup"><span data-stu-id="f93d6-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="f93d6-160">Hvis der kræves to ressourcer til en rolle for at fuldføre arbejdet, opretter funktionen Opret team to teammedlemmer og bruger stillingsnavnet til at adskille dem.</span><span class="sxs-lookup"><span data-stu-id="f93d6-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="f93d6-161">![Skærmbillede af tilføjelse af to generiske ressourcer](media/FAQ-Resources-to-Tasks2-6.png "Skærmbillede af tilføjelse af to generiske ressourcer")</span><span class="sxs-lookup"><span data-stu-id="f93d6-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="f93d6-162">Du kan åbne sikkerhedskopiering af ressourcekrav for det generiske teammedlem ved at vælge linket under Ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="f93d6-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="f93d6-163">![Skærmbillede af åbning af det bagvedliggende ressourcekrav](media/FAQ-Resources-to-Tasks2-7.png "Skærmbillede af åbning af det bagvedliggende ressourcekrav")</span><span class="sxs-lookup"><span data-stu-id="f93d6-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="f93d6-164">Vælg **Reservér** for den generiske ressource, så du kan bruge planlægningsområdet til at finde og reservere en faktisk ressource.</span><span class="sxs-lookup"><span data-stu-id="f93d6-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="f93d6-165">Du kan også sende kravet til en ressourceansvarlig til indfrielse ved at vælge **Send anmodning**.</span><span class="sxs-lookup"><span data-stu-id="f93d6-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="f93d6-166">Når den generiske ressource er indfriet med en navngivet ressource, fjernes den generiske ressource fra teamet, og opgavetildelingerne for den generiske ressource tildeles til den navngivne ressource, der opfyldte ressourcekravet til den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="f93d6-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]