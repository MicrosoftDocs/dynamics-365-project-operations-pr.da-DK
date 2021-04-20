---
title: Brug planlægnings-API'er til at udføre handlinger med planlægningsobjekter
description: Dette emne indeholder oplysninger om og eksempler på, hvordan du bruger planlægnings-API'er.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868122"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="f2cec-103">Brug planlægnings-API'er til at udføre handlinger med planlægningsobjekter</span><span class="sxs-lookup"><span data-stu-id="f2cec-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="f2cec-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="f2cec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="f2cec-105">Visse eller alle de funktioner, der er omtalt i dette emne, er tilgængelige som en del af en forhåndsversion.</span><span class="sxs-lookup"><span data-stu-id="f2cec-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="f2cec-106">Indholdet og funktionerne kan ændres.</span><span class="sxs-lookup"><span data-stu-id="f2cec-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="f2cec-107">Planlægningsobjekter</span><span class="sxs-lookup"><span data-stu-id="f2cec-107">Scheduling entities</span></span>

<span data-ttu-id="f2cec-108">Med planlægnings-API'er kan du oprette, opdatere og slette handlinger med **Planlægningsobjekter**.</span><span class="sxs-lookup"><span data-stu-id="f2cec-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="f2cec-109">Disse objekter administreres via planlægningsprogrammet i Projekt til internettet.</span><span class="sxs-lookup"><span data-stu-id="f2cec-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="f2cec-110">Handlinger til oprettelse, opdatering og sletning med **Planlægningsobjekter** var i tidligere udgivelser til Dynamics 365 Project Operations begrænset.</span><span class="sxs-lookup"><span data-stu-id="f2cec-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="f2cec-111">I følgende tabel vises en fuldstændig liste over **Planlægningsobjekterne**.</span><span class="sxs-lookup"><span data-stu-id="f2cec-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="f2cec-112">Enhedsnavn</span><span class="sxs-lookup"><span data-stu-id="f2cec-112">Entity name</span></span>  | <span data-ttu-id="f2cec-113">Objektets logiske navn</span><span class="sxs-lookup"><span data-stu-id="f2cec-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="f2cec-114">Project</span><span class="sxs-lookup"><span data-stu-id="f2cec-114">Project</span></span> | <span data-ttu-id="f2cec-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f2cec-115">msdyn_project</span></span> |
| <span data-ttu-id="f2cec-116">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="f2cec-116">Project Task</span></span>  | <span data-ttu-id="f2cec-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="f2cec-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="f2cec-118">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="f2cec-118">Project Task Dependency</span></span>  | <span data-ttu-id="f2cec-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="f2cec-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="f2cec-120">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="f2cec-120">Resource Assignment</span></span> | <span data-ttu-id="f2cec-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="f2cec-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="f2cec-122">Projektbucket</span><span class="sxs-lookup"><span data-stu-id="f2cec-122">Project Bucket</span></span>  | <span data-ttu-id="f2cec-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="f2cec-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="f2cec-124">Medlem af projektteam</span><span class="sxs-lookup"><span data-stu-id="f2cec-124">Project Team Member</span></span> | <span data-ttu-id="f2cec-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="f2cec-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="f2cec-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="f2cec-126">OperationSet</span></span>

<span data-ttu-id="f2cec-127">OperationSet er et arbejdsenhedsmønster, der kan bruges, når flere forespørgsler, der påvirker tidsplanen, skal behandles i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="f2cec-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="f2cec-128">Planlæg API'er</span><span class="sxs-lookup"><span data-stu-id="f2cec-128">Schedule APIs</span></span>

<span data-ttu-id="f2cec-129">Nedenfor vises en liste over aktuelle planlægnings-API'er.</span><span class="sxs-lookup"><span data-stu-id="f2cec-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="f2cec-130">**msdyn_CreateProjectV1**: Denne API kan bruges til at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="f2cec-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="f2cec-131">Projekt- og standardprojektbucket oprettes med det samme.</span><span class="sxs-lookup"><span data-stu-id="f2cec-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="f2cec-132">**msdyn_CreateTeamMemberV1**: Denne API kan bruges til at oprette et projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="f2cec-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="f2cec-133">Teammedlemsposten oprettes med det samme.</span><span class="sxs-lookup"><span data-stu-id="f2cec-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="f2cec-134">**msdyn_CreateOperationSetV1**: Denne API kan bruges til at planlægge flere forespørgsler, der skal udføres i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="f2cec-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="f2cec-135">**msdyn_PSSCreateV1**: Denne API kan bruges til at oprette et objekt.</span><span class="sxs-lookup"><span data-stu-id="f2cec-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="f2cec-136">Objektet kan være et af de planlægningsobjekter, der understøtter oprettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="f2cec-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="f2cec-137">**msdyn_PSSUpdateV1**: Denne API kan bruges til at opdatere et objekt.</span><span class="sxs-lookup"><span data-stu-id="f2cec-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="f2cec-138">Objektet kan være et af de planlægningsobjekter, der understøtter opdateringshandlingen.</span><span class="sxs-lookup"><span data-stu-id="f2cec-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="f2cec-139">**msdyn_PSSDeleteV1**: Denne API kan bruges til at slette et objekt.</span><span class="sxs-lookup"><span data-stu-id="f2cec-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="f2cec-140">Objektet kan være et af de planlægningsobjekter, der understøtter slettehandlingen.</span><span class="sxs-lookup"><span data-stu-id="f2cec-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="f2cec-141">**msdyn_ExecuteOperationSetV1**: Denne API bruges til at udføre alle handlinger i det givne operationssæt.</span><span class="sxs-lookup"><span data-stu-id="f2cec-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="f2cec-142">Brug planlægnings-API'er med OperationSet</span><span class="sxs-lookup"><span data-stu-id="f2cec-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="f2cec-143">Da poster med både **CreateProjectV1** og **CreateTeamMemberV1** oprettes med det samme, kan disse API'er ikke bruges direkte i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f2cec-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="f2cec-144">Du kan dog bruge API'en til at oprette de krævede poster, et **OperationSet** og derefter bruge disse forudoprettede poster i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f2cec-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="f2cec-145">Understøttede handlinger</span><span class="sxs-lookup"><span data-stu-id="f2cec-145">Supported operations</span></span>

| <span data-ttu-id="f2cec-146">Planlægningsobjekt</span><span class="sxs-lookup"><span data-stu-id="f2cec-146">Scheduling entity</span></span> | <span data-ttu-id="f2cec-147">Opret</span><span class="sxs-lookup"><span data-stu-id="f2cec-147">Create</span></span> | <span data-ttu-id="f2cec-148">Opdatering</span><span class="sxs-lookup"><span data-stu-id="f2cec-148">Update</span></span> | <span data-ttu-id="f2cec-149">Delete</span><span class="sxs-lookup"><span data-stu-id="f2cec-149">Delete</span></span> | <span data-ttu-id="f2cec-150">Vigtige overvejelser</span><span class="sxs-lookup"><span data-stu-id="f2cec-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="f2cec-151">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="f2cec-151">Project task</span></span> | <span data-ttu-id="f2cec-152">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-152">Yes</span></span> | <span data-ttu-id="f2cec-153">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-153">Yes</span></span> | <span data-ttu-id="f2cec-154">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-154">Yes</span></span> | <span data-ttu-id="f2cec-155">Intet</span><span class="sxs-lookup"><span data-stu-id="f2cec-155">None</span></span> |
| <span data-ttu-id="f2cec-156">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="f2cec-156">Project task dependency</span></span> | <span data-ttu-id="f2cec-157">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-157">Yes</span></span> | <span data-ttu-id="f2cec-158">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-158">Yes</span></span> | | <span data-ttu-id="f2cec-159">Projektopgaveafhængighedsposter opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="f2cec-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="f2cec-160">I stedet kan en gammel post slettes, og der kan oprettes en ny post.</span><span class="sxs-lookup"><span data-stu-id="f2cec-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f2cec-161">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="f2cec-161">Resource assignment</span></span> | <span data-ttu-id="f2cec-162">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-162">Yes</span></span> | <span data-ttu-id="f2cec-163">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-163">Yes</span></span> | | <span data-ttu-id="f2cec-164">Handlinger med følgende felter understøttes ikke: **BookableResourceID**, **Indsats**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="f2cec-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="f2cec-165">Ressourcetildelingsposter opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="f2cec-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="f2cec-166">I stedet kan den gamle post slettes, og der kan oprettes en ny post.</span><span class="sxs-lookup"><span data-stu-id="f2cec-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f2cec-167">Projektbucket</span><span class="sxs-lookup"><span data-stu-id="f2cec-167">Project bucket</span></span> | <span data-ttu-id="f2cec-168">I/R</span><span class="sxs-lookup"><span data-stu-id="f2cec-168">N/A</span></span> | <span data-ttu-id="f2cec-169">I/R</span><span class="sxs-lookup"><span data-stu-id="f2cec-169">N/A</span></span> | <span data-ttu-id="f2cec-170">I/R</span><span class="sxs-lookup"><span data-stu-id="f2cec-170">N/A</span></span> | <span data-ttu-id="f2cec-171">Standardbucket oprettes ved hjælp af API'en **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="f2cec-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="f2cec-172">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="f2cec-172">Project team member</span></span> | <span data-ttu-id="f2cec-173">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-173">Yes</span></span> | <span data-ttu-id="f2cec-174">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-174">Yes</span></span> | <span data-ttu-id="f2cec-175">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-175">Yes</span></span> | <span data-ttu-id="f2cec-176">Brug API'en **CreateTeamMemberV1** til oprettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="f2cec-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="f2cec-177">Project</span><span class="sxs-lookup"><span data-stu-id="f2cec-177">Project</span></span> | <span data-ttu-id="f2cec-178">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-178">Yes</span></span> | <span data-ttu-id="f2cec-179">Ja</span><span class="sxs-lookup"><span data-stu-id="f2cec-179">Yes</span></span> | <span data-ttu-id="f2cec-180">I/R</span><span class="sxs-lookup"><span data-stu-id="f2cec-180">N/A</span></span> | <span data-ttu-id="f2cec-181">Handlinger med følgende felter understøttes ikke: **StateCode**, **BulkStatus**, **GlobalRevisionToken**, **CalendarID**, **Indsats**, **EffortCompleted**, **EffortRemaining**, **Status**, **Afsluttet**, **TaskEarliestStart** og **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="f2cec-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="f2cec-182">Disse API'er kan kaldes sammen med enhedsobjekter, der indeholder brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="f2cec-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="f2cec-183">Id-egenskaben er valgfri.</span><span class="sxs-lookup"><span data-stu-id="f2cec-183">The ID property is optional.</span></span> <span data-ttu-id="f2cec-184">Hvis den oplyses, forsøger systemet at bruge den, og der udløses en undtagelse, hvis den ikke kan bruges.</span><span class="sxs-lookup"><span data-stu-id="f2cec-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="f2cec-185">Hvis den ikke er angivet, oprettes den af systemet.</span><span class="sxs-lookup"><span data-stu-id="f2cec-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="f2cec-186">Begrænsninger og kendte problemer</span><span class="sxs-lookup"><span data-stu-id="f2cec-186">Limitations and known issues</span></span>
<span data-ttu-id="f2cec-187">Her følger en liste over begrænsninger og kendte problemer:</span><span class="sxs-lookup"><span data-stu-id="f2cec-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="f2cec-188">Planlægnings-API'er kan kun bruges af **Brugere med Microsoft Project-licens.**</span><span class="sxs-lookup"><span data-stu-id="f2cec-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="f2cec-189">De kan ikke bruges af:</span><span class="sxs-lookup"><span data-stu-id="f2cec-189">They can't be used by:</span></span>
    - <span data-ttu-id="f2cec-190">Programbrugere</span><span class="sxs-lookup"><span data-stu-id="f2cec-190">Application users</span></span>
    - <span data-ttu-id="f2cec-191">Systembrugere</span><span class="sxs-lookup"><span data-stu-id="f2cec-191">System users</span></span>
    - <span data-ttu-id="f2cec-192">Integrationsbrugere</span><span class="sxs-lookup"><span data-stu-id="f2cec-192">Integration users</span></span>
    - <span data-ttu-id="f2cec-193">Andre brugere, der ikke har den påkrævede licens</span><span class="sxs-lookup"><span data-stu-id="f2cec-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="f2cec-194">Hvert **OperationSet** kan kun have op til 100 handlinger.</span><span class="sxs-lookup"><span data-stu-id="f2cec-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="f2cec-195">Hver bruger kan kun have op til 10 åbne **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f2cec-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="f2cec-196">Project Operations understøtter i øjeblikket maksimalt 500 opgaver i alt på et projekt.</span><span class="sxs-lookup"><span data-stu-id="f2cec-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="f2cec-197">Status for fejl i **OperationSet** og fejllogfiler er ikke tilgængelige i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="f2cec-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="f2cec-198">Planlægnings-API'er findes i offentlige forhåndsversioner.</span><span class="sxs-lookup"><span data-stu-id="f2cec-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="f2cec-199">Brugen af disse API'er i et produktionsmiljø understøttes ikke af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2cec-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="f2cec-200">Eksempelscenarie</span><span class="sxs-lookup"><span data-stu-id="f2cec-200">Sample scenario</span></span>

<span data-ttu-id="f2cec-201">I dette scenario skal du oprette et projekt, et teammedlem, fire opgaver og to ressourcetildelinger.</span><span class="sxs-lookup"><span data-stu-id="f2cec-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="f2cec-202">Derefter skal du opdatere én opgave, opdatere projektet, slette én opgave, slette én ressourcetildeling og oprette en opgaveafhængighed.</span><span class="sxs-lookup"><span data-stu-id="f2cec-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="f2cec-203">Yderligere eksempler</span><span class="sxs-lookup"><span data-stu-id="f2cec-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
