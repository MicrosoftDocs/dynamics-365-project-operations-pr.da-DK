---
title: Planlægge et projekt med et arbejdsopgavehierarki
description: Sådan planlægger du et projekt med et arbejdsopgavehierarki i Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127871"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="03439-103">Planlægge et projekt med et arbejdsopgavehierarki (Project Service)</span><span class="sxs-lookup"><span data-stu-id="03439-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="03439-104">En projektplan kommunikerer, hvad der skal udføres, hvilke ressourcer der skal udføre arbejdet og tidsrammen, som arbejdet skal udføres i.</span><span class="sxs-lookup"><span data-stu-id="03439-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="03439-105">Projektplanen afspejler det arbejde, der er knyttet til levering af projektet til tiden.</span><span class="sxs-lookup"><span data-stu-id="03439-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="03439-106">En af de første trin i den indledende fase af projektet er at komme med en projektplan.</span><span class="sxs-lookup"><span data-stu-id="03439-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="03439-107">Hvis du vil oprette en projektplan, skal du oprette et arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="03439-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="03439-108">Opret en projektstruktur med et arbejdsopgavehierarki, som hjælper dig med at:</span><span class="sxs-lookup"><span data-stu-id="03439-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="03439-109">Opdele arbejdet i overskuelige opgaver</span><span class="sxs-lookup"><span data-stu-id="03439-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="03439-110">Anslå den tid, det tager at fuldføre en opgave</span><span class="sxs-lookup"><span data-stu-id="03439-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="03439-111">Oprette opgaveafhængigheder og opgavevarighed</span><span class="sxs-lookup"><span data-stu-id="03439-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="03439-112">Bestemme de roller, der er nødvendige for at udføre hver opgave</span><span class="sxs-lookup"><span data-stu-id="03439-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="03439-113">Projektplanen i arbejdsopgavehierarkiet har et velkendt udseende, komplet med et interaktivt Gantt-diagram.</span><span class="sxs-lookup"><span data-stu-id="03439-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="03439-114">Oprette et arbejdsopgavehierarki til et projekt</span><span class="sxs-lookup"><span data-stu-id="03439-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="03439-115">Opret et arbejdsopgavehierarki for at repræsentere sekvensen af opgaver i et projekt.</span><span class="sxs-lookup"><span data-stu-id="03439-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="03439-116">Arbejdsopgavehierarkiet indeholder opgaver, krav til hver enkelt opgave og oplysninger om indtægter og omkostninger.</span><span class="sxs-lookup"><span data-stu-id="03439-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="03439-117">I din arbejdsopgavehierarki kan du tilføje::</span><span class="sxs-lookup"><span data-stu-id="03439-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="03439-118">Rækkefølgen af opgaverne i et hierarki</span><span class="sxs-lookup"><span data-stu-id="03439-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="03439-119">Andre opgaver, som eventuelt skal udføres, før en opgave kan startes.</span><span class="sxs-lookup"><span data-stu-id="03439-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="03439-120">Startdato, sidste dato og varighed for en opgave</span><span class="sxs-lookup"><span data-stu-id="03439-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="03439-121">Antallet timer, der kræves for en opgave</span><span class="sxs-lookup"><span data-stu-id="03439-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="03439-122">Eventuelle påkrævede færdigheder og uddannelse hos arbejderne</span><span class="sxs-lookup"><span data-stu-id="03439-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="03439-123">De arbejdere, der er tildelt til en opgave</span><span class="sxs-lookup"><span data-stu-id="03439-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="03439-124">Anslået omsætning og omkostninger</span><span class="sxs-lookup"><span data-stu-id="03439-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="03439-125">Opgavetyper</span><span class="sxs-lookup"><span data-stu-id="03439-125">Task types</span></span>  
<span data-ttu-id="03439-126">Du skal bruge følgende typer opgaver, når du opretter dit arbejdsopgavehierarki:</span><span class="sxs-lookup"><span data-stu-id="03439-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="03439-127">**Rodnoden til projekt**</span><span class="sxs-lookup"><span data-stu-id="03439-127">**Project root node**</span></span> | <span data-ttu-id="03439-128">Den øverste oversigtsopgave for projektet.</span><span class="sxs-lookup"><span data-stu-id="03439-128">The top-level summary task for the project.</span></span> <span data-ttu-id="03439-129">Alle andre projektopgaver oprettes under den.</span><span class="sxs-lookup"><span data-stu-id="03439-129">All other project tasks are created under it.</span></span> <span data-ttu-id="03439-130">Navnet på rodopgaven er navnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="03439-130">The name of the root task is the project name.</span></span> <span data-ttu-id="03439-131">Indsats, datoer og varighed af rodnoden er baseret på værdierne i hierarkiet under den.</span><span class="sxs-lookup"><span data-stu-id="03439-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="03439-132">Du kan ikke redigere egenskaber for rodnode eller slette rodnoden.</span><span class="sxs-lookup"><span data-stu-id="03439-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="03439-133">**Oversigts- eller beholderopgaver**</span><span class="sxs-lookup"><span data-stu-id="03439-133">**Summary or container tasks**</span></span> | <span data-ttu-id="03439-134">En oversigtsopgave er en opgave, som har underordnede opgaver.</span><span class="sxs-lookup"><span data-stu-id="03439-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="03439-135">En hovedopgave indeholder ingen arbejdsindsats eller egne omkostninger.</span><span class="sxs-lookup"><span data-stu-id="03439-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="03439-136">Dens arbejdsindsats og omkostninger er en pakke bestående af dens underopgaver.</span><span class="sxs-lookup"><span data-stu-id="03439-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="03439-137">Du kan ændre navnet på en oversigtsopgave, men du kan ikke ændre indsats, datoer eller varighed, fordi de beregnes automatisk.</span><span class="sxs-lookup"><span data-stu-id="03439-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="03439-138">Hvis du sletter en oversigtsopgave, slettes opgaven og alle dens underopgaver.</span><span class="sxs-lookup"><span data-stu-id="03439-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="03439-139">**Bladnodeopgaver**</span><span class="sxs-lookup"><span data-stu-id="03439-139">**Leaf node tasks**</span></span> | <span data-ttu-id="03439-140">En bladnodeopgave repræsenterer det mest detaljerede arbejde på projektet.</span><span class="sxs-lookup"><span data-stu-id="03439-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="03439-141">Den har en anslået indsats, en planlagt antal ressourcer, planlagte start- og slutdatoer og en varighed.</span><span class="sxs-lookup"><span data-stu-id="03439-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="03439-142">Opgavehierarki</span><span class="sxs-lookup"><span data-stu-id="03439-142">Task hierarchy</span></span>  
 <span data-ttu-id="03439-143">Du har følgende valgmuligheder, når du opretter et opgavehierarki:</span><span class="sxs-lookup"><span data-stu-id="03439-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="03439-144">**Tilføj opgave**.</span><span class="sxs-lookup"><span data-stu-id="03439-144">**Add task**.</span></span>   <span data-ttu-id="03439-145">Du kan tilføje en opgave på en placering, du vælger i opgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="03439-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="03439-146">Hvis du ikke vælger en placering, vises den nye opgave i slutningen.</span><span class="sxs-lookup"><span data-stu-id="03439-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="03439-147">**Indryk opgave**.</span><span class="sxs-lookup"><span data-stu-id="03439-147">**Indent task**.</span></span>   <span data-ttu-id="03439-148">Indryk en opgave for at gøre den til en underordnet til opgaven direkte over den.</span><span class="sxs-lookup"><span data-stu-id="03439-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="03439-149">**Ryk opgave ud**.</span><span class="sxs-lookup"><span data-stu-id="03439-149">**Outdent task**.</span></span>   <span data-ttu-id="03439-150">Ryk en opgave ud, så den ikke længere er en underopgave til dens oprindelige overordnede opgave.</span><span class="sxs-lookup"><span data-stu-id="03439-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="03439-151">**Flyt op og Flyt**.</span><span class="sxs-lookup"><span data-stu-id="03439-151">**Move up and Move down**.</span></span>   <span data-ttu-id="03439-152">Flyt opgaver op eller ned i hierarkiet med dens overordnede opgave.</span><span class="sxs-lookup"><span data-stu-id="03439-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="03439-153">Hvis du flytter en opgave op eller ned, har det ingen indflydelse på indsats, omkostninger, datoer eller varighed.</span><span class="sxs-lookup"><span data-stu-id="03439-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="03439-154">Opgaveattributter</span><span class="sxs-lookup"><span data-stu-id="03439-154">Task attributes</span></span>  
 <span data-ttu-id="03439-155">En opgaves navn beskriver det arbejde, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="03439-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="03439-156">Du kan bruge forskellige opgaveattributter til at beskrive tidsplan og krav til arbejdskraft til opgaven.</span><span class="sxs-lookup"><span data-stu-id="03439-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="03439-157">Planlæg attributter</span><span class="sxs-lookup"><span data-stu-id="03439-157">Schedule attributes</span></span>

 - <span data-ttu-id="03439-158">Tildel værdier til **Indsatstimer**, **Antal ressourcer**, **Startdato**, **Slutdato** og **Varighed** til at bestemme tidspunktet for opgaven.</span><span class="sxs-lookup"><span data-stu-id="03439-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="03439-159">**Indsats** er et skøn over de timer, det tager at udføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="03439-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="03439-160">**Antal ressourcer** er et skøn, der giver projektlederen til opgave til at komme med den bedste mulige tidsplan.</span><span class="sxs-lookup"><span data-stu-id="03439-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="03439-161">**Varighed** (i dage) angiver antallet af arbejdsdage, det tager at fuldføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="03439-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="03439-162">Bemandingsattributter</span><span class="sxs-lookup"><span data-stu-id="03439-162">Staffing attributes</span></span>

 - <span data-ttu-id="03439-163">**Rolle**, **ressourceafdeling**, **antal ressourcer,** og **ressourcer** beskriver behov for personale til opgaven.</span><span class="sxs-lookup"><span data-stu-id="03439-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="03439-164">**Rolle** beskriver den type ressource, der er nødvendige for at udføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="03439-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="03439-165">**Ressourceafdeling** angiver den afdeling, der skal bemandes ressourcer til denne opgave. Dette påvirker også omkostninger og salgsvurdering af opgaven, da dette er taget i betragtning ved fastsættelsen af enhedssalgsprisen for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="03439-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="03439-166">**Ressourcer** indeholder en generisk ressource eller en navngivet ressource, når der findes en.</span><span class="sxs-lookup"><span data-stu-id="03439-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="03439-167">Opgaveafhængigheder</span><span class="sxs-lookup"><span data-stu-id="03439-167">Task dependencies</span></span>  
 <span data-ttu-id="03439-168">Du kan oprette relationer mellem foregående opgaver mellem en eller flere opgaver i arbejdsopgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="03439-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="03439-169">Du kan angive en eller flere værdier for feltet foregående opgaver for at angive de opgaver, som det vil være afhængige af.</span><span class="sxs-lookup"><span data-stu-id="03439-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="03439-170">Når du tildeler en foregående værdi til en opgave, kan opgaven kun starte, når du har fuldført de foregående opgaver.</span><span class="sxs-lookup"><span data-stu-id="03439-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="03439-171">Angivelse af denne afhængighed på en opgave medfører genberegning af den planlagte startdato for opgaven som seneste slutningen af alle de foregående opgaver.</span><span class="sxs-lookup"><span data-stu-id="03439-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="03439-172">Indvirkningen af relateret til foregående på en tidsplan er ikke begrænset af opgavetilstanden, der er defineret på opgaven.</span><span class="sxs-lookup"><span data-stu-id="03439-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="03439-173">Opgavetilstand</span><span class="sxs-lookup"><span data-stu-id="03439-173">Task mode</span></span>  
 <span data-ttu-id="03439-174">Opgavetilstand er en af de vigtige faktorer, der bestemmerplanlægning af bladnodeopgaver.</span><span class="sxs-lookup"><span data-stu-id="03439-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="03439-175">Der er to tilstande for opgave for hver opgave: automatisk planlægning og manuel planlægning.</span><span class="sxs-lookup"><span data-stu-id="03439-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="03439-176">**Automatisk planlægning**.</span><span class="sxs-lookup"><span data-stu-id="03439-176">**Auto scheduling**.</span></span>   <span data-ttu-id="03439-177">Når du vælger opgavetilstanden Planlagt automatisk, bruger planlægningsprogrammet planlægningsreglerne på følgende opgaveattributter til at bestemme planlægningen for opgaven:</span><span class="sxs-lookup"><span data-stu-id="03439-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="03439-178">Foregående</span><span class="sxs-lookup"><span data-stu-id="03439-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="03439-179">Indsats</span><span class="sxs-lookup"><span data-stu-id="03439-179">Effort</span></span>  
  
    -   <span data-ttu-id="03439-180">Antal ressourcer</span><span class="sxs-lookup"><span data-stu-id="03439-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="03439-181">Start- og slutdatoer</span><span class="sxs-lookup"><span data-stu-id="03439-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="03439-182">**Planlægningsregler**.</span><span class="sxs-lookup"><span data-stu-id="03439-182">**Scheduling rules**.</span></span>   <span data-ttu-id="03439-183">Startdatoen for en bladnodeopgave, der ikke har foregående er som standard projektets planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="03439-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="03439-184">Varigheden af en bladnodeopgave beregnes altid som antallet af arbejdsdage mellem dets start- og slutdatoer.</span><span class="sxs-lookup"><span data-stu-id="03439-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="03439-185">Når en opgave er planlagt automatisk, vil planlægningsprogrammet følge nedenstående regler:</span><span class="sxs-lookup"><span data-stu-id="03439-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="03439-186">Start- og slutdatoer for en opgave skal altid være arbejdsdage i projektets planlægningskalender</span><span class="sxs-lookup"><span data-stu-id="03439-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="03439-187">Startdatoen for en opgave, der har foregående opgaver, er som standard den seneste slutdato af sine forgængere</span><span class="sxs-lookup"><span data-stu-id="03439-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="03439-188">Indsats = antal personer \* varighed \* timer i en standardarbejdsdag i projektkalenderen</span><span class="sxs-lookup"><span data-stu-id="03439-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="03439-189">**Manuel planlægning**.</span><span class="sxs-lookup"><span data-stu-id="03439-189">**Manual scheduling**.</span></span>   <span data-ttu-id="03439-190">I nogle tilfælde kan du afvige fra disse regler.</span><span class="sxs-lookup"><span data-stu-id="03439-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="03439-191">I disse tilfælde kan du angive, at tilstanden for opgaven skal være manuelt planlagt.</span><span class="sxs-lookup"><span data-stu-id="03439-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="03439-192">Dette stopper planlægningsprogrammet fra at beregne værdier for andre planlægningsattributter.</span><span class="sxs-lookup"><span data-stu-id="03439-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="03439-193">Angivelse af foregående opgaver har altid indflydelse på startdatoen for den afhængige opgave.</span><span class="sxs-lookup"><span data-stu-id="03439-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="03439-194">Oprette et arbejdsopgavehierarki</span><span class="sxs-lookup"><span data-stu-id="03439-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="03439-195">Gå til **Project Service > Projekter**.</span><span class="sxs-lookup"><span data-stu-id="03439-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="03439-196">Klik på det projekt, som du vil arbejde på.</span><span class="sxs-lookup"><span data-stu-id="03439-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="03439-197">Vælg pil ned ud for projektnavnet på linjen øverst på skærmen, og klik derefter på Arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="03439-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="03439-198">Hvis du vil tilføje en opgave, skal du klikke på **Tilføj opgave**.</span><span class="sxs-lookup"><span data-stu-id="03439-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="03439-199">Udfyld felterne for opgaven, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="03439-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="03439-200">Fortsæt med at tilføje opgaver, indtil arbejdsopgavehierarkiet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="03439-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="03439-201">Når du opretter dit arbejdsopgavehierarki, kan du gøre følgende for at organisere dine opgaver:</span><span class="sxs-lookup"><span data-stu-id="03439-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="03439-202">Marker en opgave, og klik på **Indryk** for at flytte den under en anden opgave, eller klik på Ryk ud for at flytte den ud af et niveau.</span><span class="sxs-lookup"><span data-stu-id="03439-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="03439-203">Marker en opgave, og klik på **Flyt op** eller **Flyt ned** for at flytte den op eller ned på listen.</span><span class="sxs-lookup"><span data-stu-id="03439-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="03439-204">Klik på **Skjul Gantt** for at skjule Gantt-diagrammet, og klik på **Vis Gantt** for at vise det igen.</span><span class="sxs-lookup"><span data-stu-id="03439-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="03439-205">Vælg en anden tidsperiode for Gantt-diagrammet i **Tidsskala**.</span><span class="sxs-lookup"><span data-stu-id="03439-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="03439-206">Klik for at tilføje de roller, du har angivet i dit arbejdsopgavehierarki til projektets teammedlemmer, klik på **Opret projektteam**.</span><span class="sxs-lookup"><span data-stu-id="03439-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="03439-207">Klik på **Gem** i nederste højre hjørne af skærmen, når du er færdig med at foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="03439-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="03439-208">Se også</span><span class="sxs-lookup"><span data-stu-id="03439-208">See Also</span></span>  
 [<span data-ttu-id="03439-209">Vejledning til projektledere</span><span class="sxs-lookup"><span data-stu-id="03439-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
