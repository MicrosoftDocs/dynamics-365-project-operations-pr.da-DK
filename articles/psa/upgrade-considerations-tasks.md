---
title: Opgradere overvejelser i forbindelse med arbejdsopgavehierarkiet
description: Dette emne indeholder oplysninger om opgradering af arbejdsopgavehierarkiet fra Project Service Automation 2.x til 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 0b75fd372732f42a3557aaa5eccec1f24a644941
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121796"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="c8ed1-103">Opgradere overvejelser i forbindelse med arbejdsopgavehierarkiet</span><span class="sxs-lookup"><span data-stu-id="c8ed1-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="c8ed1-104">Dette emne indeholder oplysninger om opgradering af arbejdsopgavehierarkiet fra Project Service Automation 2.x til 3.x.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="c8ed1-105">I dette emne defineres den korrekte tilstand for et projekt i PSA (Project Service Automation), der skal bruges for at opnå en vellykket opgradering.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="c8ed1-106">Der findes også oplysninger om de almindelige blokeringsforhold, der medfører, at opgraderingen ikke lykkes.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="c8ed1-107">Du kan finde flere oplysninger om definition af projektopgaver og deres funktioner i en projektplan i [Projektplaner](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="c8ed1-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="c8ed1-108">Nøgleobjekter</span><span class="sxs-lookup"><span data-stu-id="c8ed1-108">Key entities</span></span>
<span data-ttu-id="c8ed1-109">Hvis du vil have et nøjagtigt arbejdsopgavehierarki, der allerede er indlæst med ressourcer, skal følgende objekter bruges:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="c8ed1-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="c8ed1-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="c8ed1-111">Projektteam</span><span class="sxs-lookup"><span data-stu-id="c8ed1-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="c8ed1-112">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="c8ed1-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="c8ed1-113">Ressourcetildelinger</span><span class="sxs-lookup"><span data-stu-id="c8ed1-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="c8ed1-114">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="c8ed1-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="c8ed1-115">Reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="c8ed1-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="c8ed1-116">Hvis du vil definere en ressources indlæste arbejdsopgavehierarki, skal du udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="c8ed1-117">Oprette et nyt projekt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-117">Create a new project.</span></span> <span data-ttu-id="c8ed1-118">Du finder flere oplysninger om, hvordan du opretter et nyt projekt i [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="c8ed1-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="c8ed1-119">Oprette en eller flere opgaver.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-119">Create one or more tasks.</span></span> <span data-ttu-id="c8ed1-120">Du finder flere oplysninger om, hvordan du opretter en opgave i [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="c8ed1-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="c8ed1-121">Definere opgaveafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-121">Define the task dependencies.</span></span> <span data-ttu-id="c8ed1-122">Du kan finde flere oplysninger i [Projektopgaveafhængighed](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="c8ed1-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="c8ed1-123">Tildele projektteammedlemmer til projektet.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-123">Assign project team members to the project.</span></span> <span data-ttu-id="c8ed1-124">Du kan finde flere oplysninger i [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="c8ed1-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="c8ed1-125">Tildele projektteammedlemmer til opgaverne.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="c8ed1-126">Du kan finde flere oplysninger i [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="c8ed1-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="c8ed1-127">Projektteamrelationer</span><span class="sxs-lookup"><span data-stu-id="c8ed1-127">Project team relationships</span></span>

<span data-ttu-id="c8ed1-128">Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="c8ed1-129">Alle projektteammedlemmer skal være tilknyttet en reserverbar ressource.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="c8ed1-130">Alle projektteammedlemmer skal være tilknyttet det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="c8ed1-131">Projektopgaverelationer</span><span class="sxs-lookup"><span data-stu-id="c8ed1-131">Project task relationships</span></span>
<span data-ttu-id="c8ed1-132">Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="c8ed1-133">Eventuelle relaterede opgaver skal være knyttet til det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="c8ed1-134">Alle linjeopgaver skal have en overordnet opgave.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="c8ed1-135">Alle opgaver skal have et overordnet projekt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="c8ed1-136">Gældende betingelser.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-136">Valid conditions</span></span>

- <span data-ttu-id="c8ed1-137">Alle opgavevarigheder skal være længere end eller lig med (> =) en time og mindre end 1.800.000 minutter (1.250 dage).\*</span><span class="sxs-lookup"><span data-stu-id="c8ed1-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="c8ed1-138">Alle opgaver skal have en startdato, der ikke ligger før 1.1.2000.\*</span><span class="sxs-lookup"><span data-stu-id="c8ed1-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="c8ed1-139">Alle opgaver skal have en startdato senest 17 år fra i dag.\*</span><span class="sxs-lookup"><span data-stu-id="c8ed1-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="c8ed1-140">Alle opgaver skal have en startdato, der ligger før eller er lig med deres slutdato.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="c8ed1-141">Alle transaktionstyper for klassificeringer (udgift, materiale, moms og tid) skal indeholde værdier for **Standardenhed** og **Enhedsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="c8ed1-142">Datoformater med bogstaver skal undgås.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="c8ed1-143">Potentielle afhjælpningstrin</span><span class="sxs-lookup"><span data-stu-id="c8ed1-143">Potential mitigation steps</span></span>
- <span data-ttu-id="c8ed1-144">Brug avanceret søgning til at identificere projektopgaver, der ikke indeholder et projekt-ID.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="c8ed1-145">Brug avanceret søgning til at identificere projektopgaver, hvor den planlagte varighed er større end > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="c8ed1-146">Før du foretager ændringer i data, skal du undersøge eventuelle tilpasninger, der er knyttet til det objekt, der kan have ført til dataenes dårlige tilstand.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="c8ed1-147">Disse tilpasninger skal rettes, før du kan fortsætte med datarelaterede opdateringer.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="c8ed1-148">I forbindelse med de identificerede opgaver, der er gået tabt, kan du overveje at slette disse opgaver, hvis de ikke er nødvendige, eller hvis de skal knyttes til det korrekte overordnede projekt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="c8ed1-149">I forbindelse med opgaver, hvor varigheden er større end 1.250 dage, skal du overveje at tilføje flere opgaver, som tilsammen kan udgøre den samlede varighed, hvis det er muligt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="c8ed1-150">Elementer, der er angivet med en stjerne (\*), har grænser, der skyldes, at styring af kunderelationer (CRM) kun understøtter 7.320 gentagelsesudvidelser.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="c8ed1-151">Du skal være under denne grænse.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="c8ed1-152">Ressourcetildelingsrelationer</span><span class="sxs-lookup"><span data-stu-id="c8ed1-152">Resource Assignment relationships</span></span>
<span data-ttu-id="c8ed1-153">Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="c8ed1-154">Alle ressourcetildelinger i et arbejdsopgavehierarki skal være relateret til det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="c8ed1-155">Alle ressourcetildelinger i et arbejdsopgavehierarki skal være knyttet til projektteammedlemmer i det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="c8ed1-156">Potentielle afhjælpningstrin</span><span class="sxs-lookup"><span data-stu-id="c8ed1-156">Potential mitigation steps</span></span>
- <span data-ttu-id="c8ed1-157">Identificer alle de opgaver, der falder uden for de betingelser, der er beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="c8ed1-158">Eventuelle ressourcetildelinger, der ikke længere er gyldige, skal slettes.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="c8ed1-159">Afhængighedsrelationer for projektopgave</span><span class="sxs-lookup"><span data-stu-id="c8ed1-159">Project task dependency relationships</span></span>
<span data-ttu-id="c8ed1-160">Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="c8ed1-161">Alle projektopgaveafhængigheder skal være relateret til det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="c8ed1-162">En opgave kan ikke have samme afhængighed refereret mere end én gang.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-162">A task can't have the same dependency referenced more than once.</span></span>
