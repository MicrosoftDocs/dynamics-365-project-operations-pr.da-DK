---
title: Projektplaner
description: Dette emne indeholder oplysninger om, hvordan du opretter en tidsplan.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074207"
---
# <a name="project-schedules"></a><span data-ttu-id="43db7-103">Projektplaner</span><span class="sxs-lookup"><span data-stu-id="43db7-103">Project schedules</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="43db7-104">En projektplan kommunikerer, hvad der skal udføres, hvilke ressourcer der skal udføre arbejdet, og tidsrammen, som arbejdet skal udføres i.</span><span class="sxs-lookup"><span data-stu-id="43db7-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="43db7-105">Projektplanen afspejler det arbejde, der er knyttet til levering af projektet til tiden.</span><span class="sxs-lookup"><span data-stu-id="43db7-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="43db7-106">I Dynamics 365 Project Service Automation kan du oprette en projektplan ved at opdele arbejdet i opgaver, der kan administreres, vurdere den tid, det tager at udføre de enkelte opgaver, og angive opgaveafhængigheder og opgavevarigheder samt vurdere de standardressourcer, der skal udføre opgaverne.</span><span class="sxs-lookup"><span data-stu-id="43db7-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="43db7-107">Projektplanen oprettes under fanen **Tidsplan** på projektsiden.</span><span class="sxs-lookup"><span data-stu-id="43db7-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="43db7-108">Opgaver</span><span class="sxs-lookup"><span data-stu-id="43db7-108">Tasks</span></span>

<span data-ttu-id="43db7-109">Det første trin i oprettelsen af en projektplan er at bryde arbejdet op i dele, der kan administreres.</span><span class="sxs-lookup"><span data-stu-id="43db7-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="43db7-110">Planen i PSA understøtter følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="43db7-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="43db7-111">Rodnoden til projekt</span><span class="sxs-lookup"><span data-stu-id="43db7-111">Project root node</span></span>
- <span data-ttu-id="43db7-112">Oversigts- eller beholderopgaver</span><span class="sxs-lookup"><span data-stu-id="43db7-112">Summary or container tasks</span></span>
- <span data-ttu-id="43db7-113">Bladnodeopgaver</span><span class="sxs-lookup"><span data-stu-id="43db7-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="43db7-114">Rodnoden til projekt</span><span class="sxs-lookup"><span data-stu-id="43db7-114">Project root node</span></span>

<span data-ttu-id="43db7-115">Projektets rodnode er hovedopgaven på øverste niveau for projektet.</span><span class="sxs-lookup"><span data-stu-id="43db7-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="43db7-116">Alle andre projektopgaver oprettes under den.</span><span class="sxs-lookup"><span data-stu-id="43db7-116">All other project tasks are created under it.</span></span> <span data-ttu-id="43db7-117">Navnet på rodnoden angives altid til navnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="43db7-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="43db7-118">Indsats, datoer og varighed af rodnoden opsummeres på grundlag af værdierne i hierarkiet under den.</span><span class="sxs-lookup"><span data-stu-id="43db7-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="43db7-119">Du kan ikke redigere egenskaberne for rodnoden.</span><span class="sxs-lookup"><span data-stu-id="43db7-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="43db7-120">Du kan heller ikke slette rodnoden.</span><span class="sxs-lookup"><span data-stu-id="43db7-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="43db7-121">Oversigts- eller beholderopgaver</span><span class="sxs-lookup"><span data-stu-id="43db7-121">Summary or container tasks</span></span> 

<span data-ttu-id="43db7-122">Hovedopgaver har underopgaver eller beholderopgaver under sig.</span><span class="sxs-lookup"><span data-stu-id="43db7-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="43db7-123">De har ikke deres egen arbejdsindsats eller egne omkostninger.</span><span class="sxs-lookup"><span data-stu-id="43db7-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="43db7-124">Deres arbejdsindsats og omkostninger er i stedet en akkumulering af arbejdsindsats og omkostninger i forbindelse med deres beholderopgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="43db7-125">Hovedopgavens startdato er startdatoen for beholderopgaver, og slutdatoen er slutdatoen for beholderopgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="43db7-126">Navnet på en hovedopgave kan redigeres, men planlægningens egenskaber (tidsforbrug, datoer og varighed) kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="43db7-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="43db7-127">Hvis du sletter en hovedopgave, sletter du også alle dens beholderopgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="43db7-128">Bladnodeopgaver</span><span class="sxs-lookup"><span data-stu-id="43db7-128">Leaf node tasks</span></span>

<span data-ttu-id="43db7-129">Bladnodeopgaver repræsenterer det mest detaljerede arbejde på projektet.</span><span class="sxs-lookup"><span data-stu-id="43db7-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="43db7-130">De har en anslået indsats, anslåede ressourcer, planlagt start- og slutdato samt en varighed.</span><span class="sxs-lookup"><span data-stu-id="43db7-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="43db7-131">Oprettelse af et opgavehierarki</span><span class="sxs-lookup"><span data-stu-id="43db7-131">Creating a task hierarchy</span></span>

<span data-ttu-id="43db7-132">Du kan oprette et arbejdshierarki ved brug af følgende valgmuligheder:</span><span class="sxs-lookup"><span data-stu-id="43db7-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="43db7-133">Knappen **Tilføj opgave**</span><span class="sxs-lookup"><span data-stu-id="43db7-133">**Add task** button</span></span>
- <span data-ttu-id="43db7-134">Knappen **Ryk opgave ind**</span><span class="sxs-lookup"><span data-stu-id="43db7-134">**Indent task** button</span></span>
- <span data-ttu-id="43db7-135">Knappen **Ryk opgave ud**</span><span class="sxs-lookup"><span data-stu-id="43db7-135">**Outdent task** button</span></span>
- <span data-ttu-id="43db7-136">Knapperne **Flyt op** og **Flyt ned**</span><span class="sxs-lookup"><span data-stu-id="43db7-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="43db7-137">Hjælp til handicappede og tastaturgenveje</span><span class="sxs-lookup"><span data-stu-id="43db7-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="43db7-138">Tilføj opgave</span><span class="sxs-lookup"><span data-stu-id="43db7-138">Add task</span></span>

<span data-ttu-id="43db7-139">Knappen **Tilføj opgave** giver dig mulighed for at oprette en ny opgave i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="43db7-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="43db7-140">Hvis du ikke vælger en placering, indsættes opgave til sidst.</span><span class="sxs-lookup"><span data-stu-id="43db7-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="43db7-141">Der tildeles et tidsplans-id til alle opgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="43db7-142">Tidsplans-id'et repræsenterer opgavens dybde og placering i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="43db7-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="43db7-143">Det bruger dispositionsnummerering.</span><span class="sxs-lookup"><span data-stu-id="43db7-143">It uses outline numbering.</span></span> <span data-ttu-id="43db7-144">I forbindelse med opgaver på det første niveau under projektets rodnode bruges et nummereringsskema med 1, 2, 3 osv.</span><span class="sxs-lookup"><span data-stu-id="43db7-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="43db7-145">I forbindelse med opgaver under det første niveau bruges et nummereringsskema med 1.1, 1.2, 1.3 osv.</span><span class="sxs-lookup"><span data-stu-id="43db7-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="43db7-146">Ryk opgave ind.</span><span class="sxs-lookup"><span data-stu-id="43db7-146">Indent task</span></span>

<span data-ttu-id="43db7-147">Når en opgave rykkes ind, bliver den et underordnet element i den opgave, der er direkte over den.</span><span class="sxs-lookup"><span data-stu-id="43db7-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="43db7-148">Opgavens tidsplans-id genberegnes derefter, så det er baseret på tidsplans-id'et for den nye overordnede opgave og følger skemaet til dispositionsnummerering.</span><span class="sxs-lookup"><span data-stu-id="43db7-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="43db7-149">Den overordnede opgave er nu en hovedopgave eller en beholderopgave.</span><span class="sxs-lookup"><span data-stu-id="43db7-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="43db7-150">Den er derfor en akkumulering af dens underopgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="43db7-151">Ryk opgave ud.</span><span class="sxs-lookup"><span data-stu-id="43db7-151">Outdent task</span></span> 

<span data-ttu-id="43db7-152">Når en opgave rykkes ud, er den ikke længere underordnet i forbindelse med den opgave, der var dens overordnede opgave.</span><span class="sxs-lookup"><span data-stu-id="43db7-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="43db7-153">Tidsplans-id'et genberegnes derefter, så det afspejler opgavens opdaterede dybde og placering i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="43db7-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="43db7-154">Indsatsen, omkostningerne og datoerne for den forrige overordnede opgave genberegnes, så de ikke inkluderer denne opgave.</span><span class="sxs-lookup"><span data-stu-id="43db7-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="43db7-155">Flyt op og Flyt ned.</span><span class="sxs-lookup"><span data-stu-id="43db7-155">Move up and Move down</span></span> 

<span data-ttu-id="43db7-156">Knapperne **Flyt op** og **Flyt ned** ændrer placeringen af en opgave i dens overordnede hierarki.</span><span class="sxs-lookup"><span data-stu-id="43db7-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="43db7-157">Ændringer af denne type påvirker ikke opgavens indsats, omkostninger, datoer eller varighed.</span><span class="sxs-lookup"><span data-stu-id="43db7-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="43db7-158">Det er kun opgavens tidsplans-id, der påvirkes.</span><span class="sxs-lookup"><span data-stu-id="43db7-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="43db7-159">Tidsplans-id'et genberegnes, så det afspejler opgavens nye placering i den overordnede opgaves liste over underordnede opgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="43db7-160">Hjælp til handicappede og tastaturgenveje</span><span class="sxs-lookup"><span data-stu-id="43db7-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="43db7-161">Gitteret **Planlægning** er fuldt tilgængeligt og kan bruges sammen med skærmlæsere, f.eks. Oplæser, JAWS eller NVDA.</span><span class="sxs-lookup"><span data-stu-id="43db7-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="43db7-162">Du kan flytte gennem gitterområdet ved hjælp af piletasterne (som i Microsoft Excel), du kan bruge tabulatortasten til at gennemblade de interaktive brugergrænsefladeelementer, og du kan bruge pil ned-tasten, tasten ENTER eller mellemrumstasten til at vælge og aktivere rullemenuerne.</span><span class="sxs-lookup"><span data-stu-id="43db7-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="43db7-163">Kolonneoverskrifterne er også interaktive.</span><span class="sxs-lookup"><span data-stu-id="43db7-163">The column headers are also interactive.</span></span> <span data-ttu-id="43db7-164">Du kan skjule og få vist kolonner, bruge tabulatortasten og piletasterne til at bevæge dig gennem kolonneoverskrifterne og bruge handlingsknapperne på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="43db7-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="43db7-165">Du kan desuden bruge følgende tastaturgenveje:</span><span class="sxs-lookup"><span data-stu-id="43db7-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="43db7-166">**Opdater** : ALT + SKIFT + F5</span><span class="sxs-lookup"><span data-stu-id="43db7-166">**Refresh** : ALT+SHIFT+F5</span></span>
- <span data-ttu-id="43db7-167">**Tilføj** : Alt + SHIFT + Insert</span><span class="sxs-lookup"><span data-stu-id="43db7-167">**Add** : ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="43db7-168">**Slet** : ALT + SHIFT + Delete</span><span class="sxs-lookup"><span data-stu-id="43db7-168">**Delete** : ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="43db7-169">**Flyt op/ned** : ALT + SHIFT + pil op/ned</span><span class="sxs-lookup"><span data-stu-id="43db7-169">**Move up/down** : ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="43db7-170">**Indrykning/udrykning** : ALT_SHIFT + venstre/højre pil</span><span class="sxs-lookup"><span data-stu-id="43db7-170">**Indent/Outdent** : ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="43db7-171">**Udvid/skjul hierarkier** : ALT + SHIFT + plus/minus-taster</span><span class="sxs-lookup"><span data-stu-id="43db7-171">**Expand/Collapse Hierarchies** : ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="43db7-172">Opgaveattributter</span><span class="sxs-lookup"><span data-stu-id="43db7-172">Task attributes</span></span>

<span data-ttu-id="43db7-173">En opgaves navn beskriver det arbejde, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="43db7-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="43db7-174">I PSA er de attributter, der er knyttet til en opgave, en beskrivelse af opgaveplanen og kravene til personaleansættelse.</span><span class="sxs-lookup"><span data-stu-id="43db7-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![Opgaveattributter](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="43db7-176">Planlæg attributter</span><span class="sxs-lookup"><span data-stu-id="43db7-176">Schedule attributes</span></span>

<span data-ttu-id="43db7-177">Attributterne **Indsats** , **Startdato** , **Slutdato** og **Varighed** definerer opgavens tidsplan.</span><span class="sxs-lookup"><span data-stu-id="43db7-177">The **Effort** , **Start date** , **End date** , and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="43db7-178">Yderligere planlægningsattributter omfatter:</span><span class="sxs-lookup"><span data-stu-id="43db7-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="43db7-179">**Tidsforbrug** : Angiv et estimat for de timer, der kræves for at fuldføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="43db7-179">**Effort hours** : Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="43db7-180">**Varighed** : Angiv det antal arbejdsdage, der skal bruges for at fuldføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="43db7-180">**Duration** : Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="43db7-181">**Tidsplans-id** : Dette automatisk genererede id bruges til at sortere opgaver i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="43db7-181">**Schedule ID** : This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="43db7-182">Afhængigheder mellem opgaverne styrer den faktiske rækkefølge, hvori opgaverne udføres.</span><span class="sxs-lookup"><span data-stu-id="43db7-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="43db7-183">Bemandingsattributter</span><span class="sxs-lookup"><span data-stu-id="43db7-183">Staffing attributes</span></span>

<span data-ttu-id="43db7-184">Der kan opnås adgang til medarbejderattributter via feltet **Ressourcer** i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="43db7-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="43db7-185">Du kan enten søge efter en eksisterende ressource eller klikke på **Opret** og i ruden **Hurtig oprettelse** tilføje et medlem af projektteamet som en ny ressource.</span><span class="sxs-lookup"><span data-stu-id="43db7-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="43db7-186">Felterne **Rolle** , **Ressourceenhed** og **Navn på stilling** bruges til at beskrive personalekravene for opgaven.</span><span class="sxs-lookup"><span data-stu-id="43db7-186">The **Role** , **Resourcing Unit** , and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="43db7-187">Disse medarbejderattributter sammen med opgaveplanlægning bruges til at finde tilgængelige ressourcer til udførelse af denne opgave.</span><span class="sxs-lookup"><span data-stu-id="43db7-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="43db7-188">**Rolle** – Angiv den type ressource, der kræves til udførelse af opgaven.</span><span class="sxs-lookup"><span data-stu-id="43db7-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="43db7-189">**Ressourceenhed** – Angiv den enhed, som ressourcer til opgaven skal tildeles fra.</span><span class="sxs-lookup"><span data-stu-id="43db7-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="43db7-190">Denne attribut påvirker omkostnings- og salgsestimatet for opgaven, hvis kostprisen og fakturasatsen for ressourcen er angivet på baggrund af reressourceenhederne.</span><span class="sxs-lookup"><span data-stu-id="43db7-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="43db7-191">**Stillingsnavn** – Angiv et fuldt navn til den generiske ressource, der fungerer som pladsholder for den ressource, der til sidst udfører arbejdet.</span><span class="sxs-lookup"><span data-stu-id="43db7-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="43db7-192">Feltet **Ressourcer** indeholder stillingsnavnet på den generiske ressource eller den navngivne ressource, når der findes en ressource.</span><span class="sxs-lookup"><span data-stu-id="43db7-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="43db7-193">Feltet **Kategori** indeholder de værdier, der angiver en bredere arbejdstype, som opgaven kan grupperes i.</span><span class="sxs-lookup"><span data-stu-id="43db7-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="43db7-194">Dette felt påvirker ikke planlægning eller bemanding.</span><span class="sxs-lookup"><span data-stu-id="43db7-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="43db7-195">Det bruges kun til rapportering.</span><span class="sxs-lookup"><span data-stu-id="43db7-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="43db7-196">Opgaveafhængigheder</span><span class="sxs-lookup"><span data-stu-id="43db7-196">Task dependencies</span></span> 

<span data-ttu-id="43db7-197">Du kan bruge planlægningen i PSA til at oprette foregående relationer mellem opgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="43db7-198">Feltet **Foregående aktivitet** under **Opgaver** bruger en eller flere værdier til at angive, hvilke opgaver en opgave afhænger af.</span><span class="sxs-lookup"><span data-stu-id="43db7-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="43db7-199">Når du tildeler en foregående værdi til en opgave, kan opgaven kun starte, når du har fuldført de foregående opgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="43db7-200">På grund af afhængigheden nulstilles opgavens planlagte startdato til den dato, hvor de foregående opgaver fuldføres.</span><span class="sxs-lookup"><span data-stu-id="43db7-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="43db7-201">Opgavetilstanden påvirker ikke de opdateringer, der er foretaget af start- og slutdatoerne for foregående/afhængige opgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="43db7-202">Opgavetilstand</span><span class="sxs-lookup"><span data-stu-id="43db7-202">Task mode</span></span> 

<span data-ttu-id="43db7-203">Opgavetilstanden bestemmer planlægningen af bladnodeopgaver.</span><span class="sxs-lookup"><span data-stu-id="43db7-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="43db7-204">PSA understøtter to tilstande for opgaver for hver opgave: automatisk planlægning og manuel planlægning.</span><span class="sxs-lookup"><span data-stu-id="43db7-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="43db7-205">Automatisk planlægning</span><span class="sxs-lookup"><span data-stu-id="43db7-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="43db7-206">Når du vælger opgavetilstanden **Planlagt automatisk** for en opgave, bruger planlægningsprogrammet planlægningsreglerne på opgaveattributterne for at bestemme planlægningen for opgaven:</span><span class="sxs-lookup"><span data-stu-id="43db7-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="43db7-207">Planlægningsregler</span><span class="sxs-lookup"><span data-stu-id="43db7-207">Scheduling rules</span></span>

<span data-ttu-id="43db7-208">Der gælder som standard, at hvis en bladnodeopgave ikke har foregående opgaver, er dens startdato angivet til projektets planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="43db7-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="43db7-209">Varigheden af en bladnodeopgave beregnes altid som antallet af arbejdsdage mellem dets start- og slutdatoer.</span><span class="sxs-lookup"><span data-stu-id="43db7-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="43db7-210">Når en opgave er planlagt automatisk, vil planlægningsprogrammet følge disse regler:</span><span class="sxs-lookup"><span data-stu-id="43db7-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="43db7-211">Start- og slutdatoen for opgaven skal være arbejdsdage i henhold til projektets planlægningskalender.</span><span class="sxs-lookup"><span data-stu-id="43db7-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="43db7-212">Startdatoen for en opgave, der har foregående opgaver, er automatisk angivet til den seneste slutdato for sine forgængere.</span><span class="sxs-lookup"><span data-stu-id="43db7-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="43db7-213">Indsatsen beregnes ved hjælp af denne formel: antal personer × varighed × timer på en normal arbejdsdag i projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="43db7-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="43db7-214">Manuel planlægning</span><span class="sxs-lookup"><span data-stu-id="43db7-214">Manual scheduling</span></span>

<span data-ttu-id="43db7-215">Hvis reglerne for automatisk planlægning ikke opfylder dine krav, kan du indstille opgavetilstanden for opgaven til **Manuelt planlagt**.</span><span class="sxs-lookup"><span data-stu-id="43db7-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="43db7-216">Denne indstilling stopper planlægningsprogrammet i at beregne værdierne for andre planlægningsattributter.</span><span class="sxs-lookup"><span data-stu-id="43db7-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="43db7-217">Uanset opgavetilstand kan du altid påvirke den afhængige opgaves startdato, hvis du angiver de foregående opgaver for opgaverne.</span><span class="sxs-lookup"><span data-stu-id="43db7-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>