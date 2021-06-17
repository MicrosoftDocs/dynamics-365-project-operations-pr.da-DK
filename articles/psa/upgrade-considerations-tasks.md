---
title: Opgradere overvejelser i forbindelse med arbejdsopgavehierarkiet
description: Dette emne indeholder oplysninger om opgradering af arbejdsopgavehierarkiet fra Project Service Automation 2.x til 3.x.
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005604"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="29d6c-103">Opgradere overvejelser i forbindelse med arbejdsopgavehierarkiet</span><span class="sxs-lookup"><span data-stu-id="29d6c-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="29d6c-104">Dette emne indeholder oplysninger om opgradering af arbejdsopgavehierarkiet fra Project Service Automation 2.x til 3.x.</span><span class="sxs-lookup"><span data-stu-id="29d6c-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="29d6c-105">I dette emne defineres den korrekte tilstand for et projekt i PSA (Project Service Automation), der skal bruges for at opnå en vellykket opgradering.</span><span class="sxs-lookup"><span data-stu-id="29d6c-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="29d6c-106">Der findes også oplysninger om de almindelige blokeringsforhold, der medfører, at opgraderingen ikke lykkes.</span><span class="sxs-lookup"><span data-stu-id="29d6c-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="29d6c-107">Du kan finde flere oplysninger om definition af projektopgaver og deres funktioner i en projektplan i [Projektplaner](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="29d6c-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="29d6c-108">Nøgleobjekter</span><span class="sxs-lookup"><span data-stu-id="29d6c-108">Key entities</span></span>
<span data-ttu-id="29d6c-109">Hvis du vil have et nøjagtigt arbejdsopgavehierarki, der allerede er indlæst med ressourcer, skal følgende objekter bruges:</span><span class="sxs-lookup"><span data-stu-id="29d6c-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="29d6c-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="29d6c-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="29d6c-111">Projektteam</span><span class="sxs-lookup"><span data-stu-id="29d6c-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="29d6c-112">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="29d6c-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="29d6c-113">Ressourcetildelinger</span><span class="sxs-lookup"><span data-stu-id="29d6c-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="29d6c-114">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="29d6c-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="29d6c-115">Reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="29d6c-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="29d6c-116">Hvis du vil definere en ressources indlæste arbejdsopgavehierarki, skal du udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="29d6c-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="29d6c-117">Oprette et nyt projekt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-117">Create a new project.</span></span> <span data-ttu-id="29d6c-118">Du finder flere oplysninger om, hvordan du opretter et nyt projekt i [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="29d6c-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="29d6c-119">Oprette en eller flere opgaver.</span><span class="sxs-lookup"><span data-stu-id="29d6c-119">Create one or more tasks.</span></span> <span data-ttu-id="29d6c-120">Du finder flere oplysninger om, hvordan du opretter en opgave i [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="29d6c-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="29d6c-121">Definere opgaveafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="29d6c-121">Define the task dependencies.</span></span> <span data-ttu-id="29d6c-122">Du kan finde flere oplysninger i [Projektopgaveafhængighed](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="29d6c-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="29d6c-123">Tildele projektteammedlemmer til projektet.</span><span class="sxs-lookup"><span data-stu-id="29d6c-123">Assign project team members to the project.</span></span> <span data-ttu-id="29d6c-124">Du kan finde flere oplysninger i [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="29d6c-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="29d6c-125">Tildele projektteammedlemmer til opgaverne.</span><span class="sxs-lookup"><span data-stu-id="29d6c-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="29d6c-126">Du kan finde flere oplysninger i [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="29d6c-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="29d6c-127">Projektteamrelationer</span><span class="sxs-lookup"><span data-stu-id="29d6c-127">Project team relationships</span></span>

<span data-ttu-id="29d6c-128">Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:</span><span class="sxs-lookup"><span data-stu-id="29d6c-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="29d6c-129">Alle projektteammedlemmer skal være tilknyttet en reserverbar ressource.</span><span class="sxs-lookup"><span data-stu-id="29d6c-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="29d6c-130">Alle projektteammedlemmer skal være tilknyttet det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="29d6c-131">Projektopgaverelationer</span><span class="sxs-lookup"><span data-stu-id="29d6c-131">Project task relationships</span></span>
<span data-ttu-id="29d6c-132">Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:</span><span class="sxs-lookup"><span data-stu-id="29d6c-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="29d6c-133">Eventuelle relaterede opgaver skal være knyttet til det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="29d6c-134">Alle linjeopgaver skal have en overordnet opgave.</span><span class="sxs-lookup"><span data-stu-id="29d6c-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="29d6c-135">Alle opgaver skal have et overordnet projekt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="29d6c-136">Gældende betingelser.</span><span class="sxs-lookup"><span data-stu-id="29d6c-136">Valid conditions</span></span>

- <span data-ttu-id="29d6c-137">Alle opgavevarigheder skal være længere end eller lig med (> =) en time og mindre end 1.800.000 minutter (1.250 dage).\*</span><span class="sxs-lookup"><span data-stu-id="29d6c-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="29d6c-138">Alle opgaver skal have en startdato, der ikke ligger før 1.1.2000.\*</span><span class="sxs-lookup"><span data-stu-id="29d6c-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="29d6c-139">Alle opgaver skal have en startdato senest 17 år fra i dag.\*</span><span class="sxs-lookup"><span data-stu-id="29d6c-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="29d6c-140">Alle opgaver skal have en startdato, der ligger før eller er lig med deres slutdato.</span><span class="sxs-lookup"><span data-stu-id="29d6c-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="29d6c-141">Alle transaktionstyper for klassificeringer (udgift, materiale, moms og tid) skal indeholde værdier for **Standardenhed** og **Enhedsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="29d6c-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="29d6c-142">Datoformater med bogstaver skal undgås.</span><span class="sxs-lookup"><span data-stu-id="29d6c-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="29d6c-143">Potentielle afhjælpningstrin</span><span class="sxs-lookup"><span data-stu-id="29d6c-143">Potential mitigation steps</span></span>
- <span data-ttu-id="29d6c-144">Brug avanceret søgning til at identificere projektopgaver, der ikke indeholder et projekt-ID.</span><span class="sxs-lookup"><span data-stu-id="29d6c-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="29d6c-145">Brug avanceret søgning til at identificere projektopgaver, hvor den planlagte varighed er større end > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="29d6c-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="29d6c-146">Før du foretager ændringer i data, skal du undersøge eventuelle tilpasninger, der er knyttet til det objekt, der kan have ført til dataenes dårlige tilstand.</span><span class="sxs-lookup"><span data-stu-id="29d6c-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="29d6c-147">Disse tilpasninger skal rettes, før du kan fortsætte med datarelaterede opdateringer.</span><span class="sxs-lookup"><span data-stu-id="29d6c-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="29d6c-148">I forbindelse med de identificerede opgaver, der er gået tabt, kan du overveje at slette disse opgaver, hvis de ikke er nødvendige, eller hvis de skal knyttes til det korrekte overordnede projekt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="29d6c-149">I forbindelse med opgaver, hvor varigheden er større end 1.250 dage, skal du overveje at tilføje flere opgaver, som tilsammen kan udgøre den samlede varighed, hvis det er muligt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="29d6c-150">Elementer, der er angivet med en stjerne (\*), har grænser, der skyldes, at styring af kunderelationer (CRM) kun understøtter 7.320 gentagelsesudvidelser.</span><span class="sxs-lookup"><span data-stu-id="29d6c-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="29d6c-151">Du skal være under denne grænse.</span><span class="sxs-lookup"><span data-stu-id="29d6c-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="29d6c-152">Ressourcetildelingsrelationer</span><span class="sxs-lookup"><span data-stu-id="29d6c-152">Resource Assignment relationships</span></span>
<span data-ttu-id="29d6c-153">Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:</span><span class="sxs-lookup"><span data-stu-id="29d6c-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="29d6c-154">Alle ressourcetildelinger i et arbejdsopgavehierarki skal være relateret til det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="29d6c-155">Alle ressourcetildelinger i et arbejdsopgavehierarki skal være knyttet til projektteammedlemmer i det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="29d6c-156">Potentielle afhjælpningstrin</span><span class="sxs-lookup"><span data-stu-id="29d6c-156">Potential mitigation steps</span></span>
- <span data-ttu-id="29d6c-157">Identificer alle de opgaver, der falder uden for de betingelser, der er beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="29d6c-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="29d6c-158">Eventuelle ressourcetildelinger, der ikke længere er gyldige, skal slettes.</span><span class="sxs-lookup"><span data-stu-id="29d6c-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="29d6c-159">Afhængighedsrelationer for projektopgave</span><span class="sxs-lookup"><span data-stu-id="29d6c-159">Project task dependency relationships</span></span>
<span data-ttu-id="29d6c-160">Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:</span><span class="sxs-lookup"><span data-stu-id="29d6c-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="29d6c-161">Alle projektopgaveafhængigheder skal være relateret til det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="29d6c-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="29d6c-162">En opgave kan ikke have samme afhængighed refereret mere end én gang.</span><span class="sxs-lookup"><span data-stu-id="29d6c-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]