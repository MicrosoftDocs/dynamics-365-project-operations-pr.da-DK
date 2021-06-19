---
title: Brug planlægnings-API'er til at udføre handlinger med planlægningsobjekter
description: Dette emne indeholder oplysninger om og eksempler på, hvordan du bruger planlægnings-API'er.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116790"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="5a9cd-103">Brug planlægnings-API'er til at udføre handlinger med planlægningsobjekter</span><span class="sxs-lookup"><span data-stu-id="5a9cd-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="5a9cd-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5a9cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="5a9cd-105">Visse eller alle de funktioner, der er omtalt i dette emne, er tilgængelige som en del af en forhåndsversion.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="5a9cd-106">Indholdet og funktionerne kan ændres.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="5a9cd-107">Planlægningsobjekter</span><span class="sxs-lookup"><span data-stu-id="5a9cd-107">Scheduling entities</span></span>

<span data-ttu-id="5a9cd-108">Med planlægnings-API'er kan du oprette, opdatere og slette handlinger med **Planlægningsobjekter**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="5a9cd-109">Disse objekter administreres via planlægningsprogrammet i Projekt til internettet.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="5a9cd-110">Handlinger til oprettelse, opdatering og sletning med **Planlægningsobjekter** var i tidligere udgivelser til Dynamics 365 Project Operations begrænset.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="5a9cd-111">I følgende tabel vises en fuldstændig liste over **Planlægningsobjekterne**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="5a9cd-112">Enhedsnavn</span><span class="sxs-lookup"><span data-stu-id="5a9cd-112">Entity name</span></span>  | <span data-ttu-id="5a9cd-113">Objektets logiske navn</span><span class="sxs-lookup"><span data-stu-id="5a9cd-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="5a9cd-114">Project</span><span class="sxs-lookup"><span data-stu-id="5a9cd-114">Project</span></span> | <span data-ttu-id="5a9cd-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="5a9cd-115">msdyn_project</span></span> |
| <span data-ttu-id="5a9cd-116">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="5a9cd-116">Project Task</span></span>  | <span data-ttu-id="5a9cd-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="5a9cd-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="5a9cd-118">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="5a9cd-118">Project Task Dependency</span></span>  | <span data-ttu-id="5a9cd-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="5a9cd-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="5a9cd-120">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="5a9cd-120">Resource Assignment</span></span> | <span data-ttu-id="5a9cd-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="5a9cd-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="5a9cd-122">Projektbucket</span><span class="sxs-lookup"><span data-stu-id="5a9cd-122">Project Bucket</span></span>  | <span data-ttu-id="5a9cd-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="5a9cd-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="5a9cd-124">Medlem af projektteam</span><span class="sxs-lookup"><span data-stu-id="5a9cd-124">Project Team Member</span></span> | <span data-ttu-id="5a9cd-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="5a9cd-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="5a9cd-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="5a9cd-126">OperationSet</span></span>

<span data-ttu-id="5a9cd-127">OperationSet er et arbejdsenhedsmønster, der kan bruges, når flere forespørgsler, der påvirker tidsplanen, skal behandles i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="5a9cd-128">Planlæg API'er</span><span class="sxs-lookup"><span data-stu-id="5a9cd-128">Schedule APIs</span></span>

<span data-ttu-id="5a9cd-129">Nedenfor vises en liste over aktuelle planlægnings-API'er.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="5a9cd-130">**msdyn_CreateProjectV1**: Denne API kan bruges til at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="5a9cd-131">Projekt- og standardprojektbucket oprettes med det samme.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="5a9cd-132">**msdyn_CreateTeamMemberV1**: Denne API kan bruges til at oprette et projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="5a9cd-133">Teammedlemsposten oprettes med det samme.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="5a9cd-134">**msdyn_CreateOperationSetV1**: Denne API kan bruges til at planlægge flere forespørgsler, der skal udføres i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="5a9cd-135">**msdyn_PSSCreateV1**: Denne API kan bruges til at oprette et objekt.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="5a9cd-136">Objektet kan være et af de planlægningsobjekter, der understøtter oprettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="5a9cd-137">**msdyn_PSSUpdateV1**: Denne API kan bruges til at opdatere et objekt.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="5a9cd-138">Objektet kan være et af de planlægningsobjekter, der understøtter opdateringshandlingen.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="5a9cd-139">**msdyn_PSSDeleteV1**: Denne API kan bruges til at slette et objekt.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="5a9cd-140">Objektet kan være et af de planlægningsobjekter, der understøtter slettehandlingen.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="5a9cd-141">**msdyn_ExecuteOperationSetV1**: Denne API bruges til at udføre alle handlinger i det givne operationssæt.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="5a9cd-142">Brug planlægnings-API'er med OperationSet</span><span class="sxs-lookup"><span data-stu-id="5a9cd-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="5a9cd-143">Da poster med både **CreateProjectV1** og **CreateTeamMemberV1** oprettes med det samme, kan disse API'er ikke bruges direkte i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="5a9cd-144">Du kan dog bruge API'en til at oprette de krævede poster, et **OperationSet** og derefter bruge disse forudoprettede poster i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="5a9cd-145">Understøttede handlinger</span><span class="sxs-lookup"><span data-stu-id="5a9cd-145">Supported operations</span></span>

| <span data-ttu-id="5a9cd-146">Planlægningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5a9cd-146">Scheduling entity</span></span> | <span data-ttu-id="5a9cd-147">Opret</span><span class="sxs-lookup"><span data-stu-id="5a9cd-147">Create</span></span> | <span data-ttu-id="5a9cd-148">Opdatering</span><span class="sxs-lookup"><span data-stu-id="5a9cd-148">Update</span></span> | <span data-ttu-id="5a9cd-149">Delete</span><span class="sxs-lookup"><span data-stu-id="5a9cd-149">Delete</span></span> | <span data-ttu-id="5a9cd-150">Vigtige overvejelser</span><span class="sxs-lookup"><span data-stu-id="5a9cd-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="5a9cd-151">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="5a9cd-151">Project task</span></span> | <span data-ttu-id="5a9cd-152">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-152">Yes</span></span> | <span data-ttu-id="5a9cd-153">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-153">Yes</span></span> | <span data-ttu-id="5a9cd-154">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-154">Yes</span></span> | <span data-ttu-id="5a9cd-155">Intet</span><span class="sxs-lookup"><span data-stu-id="5a9cd-155">None</span></span> |
| <span data-ttu-id="5a9cd-156">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="5a9cd-156">Project task dependency</span></span> | <span data-ttu-id="5a9cd-157">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-157">Yes</span></span> | <span data-ttu-id="5a9cd-158">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-158">Yes</span></span> | | <span data-ttu-id="5a9cd-159">Projektopgaveafhængighedsposter opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="5a9cd-160">I stedet kan en gammel post slettes, og der kan oprettes en ny post.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="5a9cd-161">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="5a9cd-161">Resource assignment</span></span> | <span data-ttu-id="5a9cd-162">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-162">Yes</span></span> | <span data-ttu-id="5a9cd-163">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-163">Yes</span></span> | | <span data-ttu-id="5a9cd-164">Handlinger med følgende felter understøttes ikke: **BookableResourceID**, **Indsats**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="5a9cd-165">Ressourcetildelingsposter opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="5a9cd-166">I stedet kan den gamle post slettes, og der kan oprettes en ny post.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="5a9cd-167">Projektbucket</span><span class="sxs-lookup"><span data-stu-id="5a9cd-167">Project bucket</span></span> | <span data-ttu-id="5a9cd-168">I/R</span><span class="sxs-lookup"><span data-stu-id="5a9cd-168">N/A</span></span> | <span data-ttu-id="5a9cd-169">I/R</span><span class="sxs-lookup"><span data-stu-id="5a9cd-169">N/A</span></span> | <span data-ttu-id="5a9cd-170">I/R</span><span class="sxs-lookup"><span data-stu-id="5a9cd-170">N/A</span></span> | <span data-ttu-id="5a9cd-171">Standardbucket oprettes ved hjælp af API'en **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="5a9cd-172">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="5a9cd-172">Project team member</span></span> | <span data-ttu-id="5a9cd-173">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-173">Yes</span></span> | <span data-ttu-id="5a9cd-174">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-174">Yes</span></span> | <span data-ttu-id="5a9cd-175">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-175">Yes</span></span> | <span data-ttu-id="5a9cd-176">Brug API'en **CreateTeamMemberV1** til oprettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="5a9cd-177">Project</span><span class="sxs-lookup"><span data-stu-id="5a9cd-177">Project</span></span> | <span data-ttu-id="5a9cd-178">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-178">Yes</span></span> | <span data-ttu-id="5a9cd-179">Ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-179">Yes</span></span> | <span data-ttu-id="5a9cd-180">I/R</span><span class="sxs-lookup"><span data-stu-id="5a9cd-180">N/A</span></span> | <span data-ttu-id="5a9cd-181">Handlinger med følgende felter understøttes ikke: **StateCode**, **BulkStatus**, **GlobalRevisionToken**, **CalendarID**, **Indsats**, **EffortCompleted**, **EffortRemaining**, **Status**, **Afsluttet**, **TaskEarliestStart** og **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="5a9cd-182">Disse API'er kan kaldes sammen med enhedsobjekter, der indeholder brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="5a9cd-183">Id-egenskaben er valgfri.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-183">The ID property is optional.</span></span> <span data-ttu-id="5a9cd-184">Hvis den oplyses, forsøger systemet at bruge den, og der udløses en undtagelse, hvis den ikke kan bruges.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="5a9cd-185">Hvis den ikke er angivet, oprettes den af systemet.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="5a9cd-186">Begrænsede felter</span><span class="sxs-lookup"><span data-stu-id="5a9cd-186">Restricted fields</span></span>

<span data-ttu-id="5a9cd-187">I følgende tabeller defineres de felter, der er begrænset fra **Opret** og **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="5a9cd-188">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="5a9cd-188">Project task</span></span>

| <span data-ttu-id="5a9cd-189">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-189">**Logical name**</span></span>                       | <span data-ttu-id="5a9cd-190">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-190">**Can create**</span></span> | <span data-ttu-id="5a9cd-191">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="5a9cd-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="5a9cd-193">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-193">no</span></span>             | <span data-ttu-id="5a9cd-194">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-194">no</span></span>               |
| <span data-ttu-id="5a9cd-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="5a9cd-196">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-196">no</span></span>             | <span data-ttu-id="5a9cd-197">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-197">no</span></span>               |
| <span data-ttu-id="5a9cd-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="5a9cd-198">msdyn_actualend</span></span>                        | <span data-ttu-id="5a9cd-199">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-199">no</span></span>             | <span data-ttu-id="5a9cd-200">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-200">no</span></span>               |
| <span data-ttu-id="5a9cd-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="5a9cd-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="5a9cd-202">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-202">no</span></span>             | <span data-ttu-id="5a9cd-203">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-203">no</span></span>               |
| <span data-ttu-id="5a9cd-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="5a9cd-205">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-205">no</span></span>             | <span data-ttu-id="5a9cd-206">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-206">no</span></span>               |
| <span data-ttu-id="5a9cd-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="5a9cd-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="5a9cd-208">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-208">no</span></span>             | <span data-ttu-id="5a9cd-209">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-209">no</span></span>               |
| <span data-ttu-id="5a9cd-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="5a9cd-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="5a9cd-211">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-211">no</span></span>             | <span data-ttu-id="5a9cd-212">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-212">no</span></span>               |
| <span data-ttu-id="5a9cd-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="5a9cd-214">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-214">no</span></span>             | <span data-ttu-id="5a9cd-215">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-215">no</span></span>               |
| <span data-ttu-id="5a9cd-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="5a9cd-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="5a9cd-217">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-217">no</span></span>             | <span data-ttu-id="5a9cd-218">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-218">no</span></span>               |
| <span data-ttu-id="5a9cd-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5a9cd-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="5a9cd-220">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-220">no</span></span>             | <span data-ttu-id="5a9cd-221">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-221">no</span></span>               |
| <span data-ttu-id="5a9cd-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5a9cd-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="5a9cd-223">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-223">no</span></span>             | <span data-ttu-id="5a9cd-224">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-224">no</span></span>               |
| <span data-ttu-id="5a9cd-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="5a9cd-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="5a9cd-226">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-226">no</span></span>             | <span data-ttu-id="5a9cd-227">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-227">no</span></span>               |
| <span data-ttu-id="5a9cd-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="5a9cd-229">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-229">no</span></span>             | <span data-ttu-id="5a9cd-230">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-230">no</span></span>               |
| <span data-ttu-id="5a9cd-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="5a9cd-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="5a9cd-232">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-232">no</span></span>             | <span data-ttu-id="5a9cd-233">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-233">no</span></span>               |
| <span data-ttu-id="5a9cd-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="5a9cd-235">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-235">no</span></span>             | <span data-ttu-id="5a9cd-236">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-236">no</span></span>               |
| <span data-ttu-id="5a9cd-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="5a9cd-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="5a9cd-238">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-238">no</span></span>             | <span data-ttu-id="5a9cd-239">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-239">no</span></span>               |
| <span data-ttu-id="5a9cd-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="5a9cd-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="5a9cd-241">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-241">no</span></span>             | <span data-ttu-id="5a9cd-242">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-242">no</span></span>               |
| <span data-ttu-id="5a9cd-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="5a9cd-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="5a9cd-244">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-244">no</span></span>             | <span data-ttu-id="5a9cd-245">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-245">no</span></span>               |
| <span data-ttu-id="5a9cd-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="5a9cd-247">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-247">no</span></span>             | <span data-ttu-id="5a9cd-248">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-248">no</span></span>               |
| <span data-ttu-id="5a9cd-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="5a9cd-250">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-250">no</span></span>             | <span data-ttu-id="5a9cd-251">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-251">no</span></span>               |
| <span data-ttu-id="5a9cd-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="5a9cd-253">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-253">no</span></span>             | <span data-ttu-id="5a9cd-254">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-254">no</span></span>               |
| <span data-ttu-id="5a9cd-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="5a9cd-256">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-256">no</span></span>             | <span data-ttu-id="5a9cd-257">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-257">no</span></span>               |
| <span data-ttu-id="5a9cd-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5a9cd-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="5a9cd-259">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-259">no</span></span>             | <span data-ttu-id="5a9cd-260">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-260">no</span></span>               |
| <span data-ttu-id="5a9cd-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="5a9cd-262">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-262">no</span></span>             | <span data-ttu-id="5a9cd-263">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-263">no</span></span>               |
| <span data-ttu-id="5a9cd-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="5a9cd-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="5a9cd-265">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-265">no</span></span>             | <span data-ttu-id="5a9cd-266">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-266">no</span></span>               |
| <span data-ttu-id="5a9cd-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="5a9cd-267">msdyn_progress</span></span>                         | <span data-ttu-id="5a9cd-268">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-268">no</span></span>             | <span data-ttu-id="5a9cd-269">nej (ja for P4W)</span><span class="sxs-lookup"><span data-stu-id="5a9cd-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="5a9cd-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="5a9cd-271">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-271">no</span></span>             | <span data-ttu-id="5a9cd-272">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-272">no</span></span>               |
| <span data-ttu-id="5a9cd-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="5a9cd-274">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-274">no</span></span>             | <span data-ttu-id="5a9cd-275">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-275">no</span></span>               |
| <span data-ttu-id="5a9cd-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5a9cd-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="5a9cd-277">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-277">no</span></span>             | <span data-ttu-id="5a9cd-278">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-278">no</span></span>               |
| <span data-ttu-id="5a9cd-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="5a9cd-280">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-280">no</span></span>             | <span data-ttu-id="5a9cd-281">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-281">no</span></span>               |
| <span data-ttu-id="5a9cd-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="5a9cd-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="5a9cd-283">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-283">no</span></span>             | <span data-ttu-id="5a9cd-284">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-284">no</span></span>               |
| <span data-ttu-id="5a9cd-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="5a9cd-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="5a9cd-286">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-286">no</span></span>             | <span data-ttu-id="5a9cd-287">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-287">no</span></span>               |
| <span data-ttu-id="5a9cd-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="5a9cd-289">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-289">no</span></span>             | <span data-ttu-id="5a9cd-290">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-290">no</span></span>               |
| <span data-ttu-id="5a9cd-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="5a9cd-292">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-292">no</span></span>             | <span data-ttu-id="5a9cd-293">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-293">no</span></span>               |
| <span data-ttu-id="5a9cd-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="5a9cd-295">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-295">no</span></span>             | <span data-ttu-id="5a9cd-296">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-296">no</span></span>               |
| <span data-ttu-id="5a9cd-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="5a9cd-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="5a9cd-298">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-298">no</span></span>             | <span data-ttu-id="5a9cd-299">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-299">no</span></span>               |
| <span data-ttu-id="5a9cd-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5a9cd-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="5a9cd-301">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-301">no</span></span>             | <span data-ttu-id="5a9cd-302">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-302">no</span></span>               |
| <span data-ttu-id="5a9cd-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="5a9cd-304">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-304">no</span></span>             | <span data-ttu-id="5a9cd-305">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-305">no</span></span>               |
| <span data-ttu-id="5a9cd-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="5a9cd-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="5a9cd-307">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-307">no</span></span>             | <span data-ttu-id="5a9cd-308">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-308">no</span></span>               |
| <span data-ttu-id="5a9cd-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="5a9cd-310">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-310">no</span></span>             | <span data-ttu-id="5a9cd-311">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-311">no</span></span>               |
| <span data-ttu-id="5a9cd-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="5a9cd-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="5a9cd-313">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-313">no</span></span>             | <span data-ttu-id="5a9cd-314">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-314">no</span></span>               |
| <span data-ttu-id="5a9cd-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="5a9cd-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="5a9cd-316">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-316">no</span></span>             | <span data-ttu-id="5a9cd-317">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-317">no</span></span>               |
| <span data-ttu-id="5a9cd-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="5a9cd-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="5a9cd-319">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-319">no</span></span>             | <span data-ttu-id="5a9cd-320">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-320">no</span></span>               |
| <span data-ttu-id="5a9cd-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="5a9cd-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="5a9cd-322">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-322">no</span></span>             | <span data-ttu-id="5a9cd-323">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-323">no</span></span>               |
| <span data-ttu-id="5a9cd-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="5a9cd-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="5a9cd-325">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-325">no</span></span>             | <span data-ttu-id="5a9cd-326">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-326">no</span></span>               |
| <span data-ttu-id="5a9cd-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="5a9cd-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="5a9cd-328">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-328">no</span></span>             | <span data-ttu-id="5a9cd-329">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-329">no</span></span>               |
| <span data-ttu-id="5a9cd-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="5a9cd-330">msdyn_summary</span></span>                          | <span data-ttu-id="5a9cd-331">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-331">no</span></span>             | <span data-ttu-id="5a9cd-332">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-332">no</span></span>               |
| <span data-ttu-id="5a9cd-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="5a9cd-334">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-334">no</span></span>             | <span data-ttu-id="5a9cd-335">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-335">no</span></span>               |
| <span data-ttu-id="5a9cd-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="5a9cd-337">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-337">no</span></span>             | <span data-ttu-id="5a9cd-338">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="5a9cd-339">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="5a9cd-339">Project task dependency</span></span>

| <span data-ttu-id="5a9cd-340">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-340">**Logical name**</span></span>              | <span data-ttu-id="5a9cd-341">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-341">**Can create**</span></span> | <span data-ttu-id="5a9cd-342">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="5a9cd-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="5a9cd-343">msdyn_linktype</span></span>                | <span data-ttu-id="5a9cd-344">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-344">no</span></span>             | <span data-ttu-id="5a9cd-345">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-345">no</span></span>           |
| <span data-ttu-id="5a9cd-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="5a9cd-346">msdyn_linktypename</span></span>            | <span data-ttu-id="5a9cd-347">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-347">no</span></span>             | <span data-ttu-id="5a9cd-348">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-348">no</span></span>           |
| <span data-ttu-id="5a9cd-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="5a9cd-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="5a9cd-350">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-350">yes</span></span>            | <span data-ttu-id="5a9cd-351">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-351">no</span></span>           |
| <span data-ttu-id="5a9cd-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="5a9cd-353">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-353">yes</span></span>            | <span data-ttu-id="5a9cd-354">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-354">no</span></span>           |
| <span data-ttu-id="5a9cd-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="5a9cd-355">msdyn_project</span></span>                 | <span data-ttu-id="5a9cd-356">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-356">yes</span></span>            | <span data-ttu-id="5a9cd-357">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-357">no</span></span>           |
| <span data-ttu-id="5a9cd-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-358">msdyn_projectname</span></span>             | <span data-ttu-id="5a9cd-359">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-359">yes</span></span>            | <span data-ttu-id="5a9cd-360">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-360">no</span></span>           |
| <span data-ttu-id="5a9cd-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="5a9cd-362">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-362">yes</span></span>            | <span data-ttu-id="5a9cd-363">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-363">no</span></span>           |
| <span data-ttu-id="5a9cd-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="5a9cd-364">msdyn_successortask</span></span>           | <span data-ttu-id="5a9cd-365">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-365">yes</span></span>            | <span data-ttu-id="5a9cd-366">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-366">no</span></span>           |
| <span data-ttu-id="5a9cd-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="5a9cd-368">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-368">yes</span></span>            | <span data-ttu-id="5a9cd-369">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="5a9cd-370">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="5a9cd-370">Resource assignment</span></span>

| <span data-ttu-id="5a9cd-371">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-371">**Logical name**</span></span>             | <span data-ttu-id="5a9cd-372">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-372">**Can create**</span></span> | <span data-ttu-id="5a9cd-373">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="5a9cd-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="5a9cd-375">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-375">yes</span></span>            | <span data-ttu-id="5a9cd-376">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-376">no</span></span>           |
| <span data-ttu-id="5a9cd-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="5a9cd-378">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-378">yes</span></span>            | <span data-ttu-id="5a9cd-379">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-379">no</span></span>           |
| <span data-ttu-id="5a9cd-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="5a9cd-381">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-381">no</span></span>             | <span data-ttu-id="5a9cd-382">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-382">no</span></span>           |
| <span data-ttu-id="5a9cd-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="5a9cd-384">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-384">no</span></span>             | <span data-ttu-id="5a9cd-385">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-385">no</span></span>           |
| <span data-ttu-id="5a9cd-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="5a9cd-386">msdyn_committype</span></span>             | <span data-ttu-id="5a9cd-387">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-387">no</span></span>             | <span data-ttu-id="5a9cd-388">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-388">no</span></span>           |
| <span data-ttu-id="5a9cd-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="5a9cd-389">msdyn_committypename</span></span>         | <span data-ttu-id="5a9cd-390">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-390">no</span></span>             | <span data-ttu-id="5a9cd-391">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-391">no</span></span>           |
| <span data-ttu-id="5a9cd-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5a9cd-392">msdyn_effort</span></span>                 | <span data-ttu-id="5a9cd-393">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-393">no</span></span>             | <span data-ttu-id="5a9cd-394">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-394">no</span></span>           |
| <span data-ttu-id="5a9cd-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5a9cd-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="5a9cd-396">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-396">no</span></span>             | <span data-ttu-id="5a9cd-397">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-397">no</span></span>           |
| <span data-ttu-id="5a9cd-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5a9cd-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="5a9cd-399">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-399">no</span></span>             | <span data-ttu-id="5a9cd-400">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-400">no</span></span>           |
| <span data-ttu-id="5a9cd-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5a9cd-401">msdyn_finish</span></span>                 | <span data-ttu-id="5a9cd-402">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-402">no</span></span>             | <span data-ttu-id="5a9cd-403">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-403">no</span></span>           |
| <span data-ttu-id="5a9cd-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="5a9cd-405">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-405">no</span></span>             | <span data-ttu-id="5a9cd-406">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-406">no</span></span>           |
| <span data-ttu-id="5a9cd-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="5a9cd-408">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-408">no</span></span>             | <span data-ttu-id="5a9cd-409">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-409">no</span></span>           |
| <span data-ttu-id="5a9cd-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="5a9cd-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="5a9cd-411">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-411">no</span></span>             | <span data-ttu-id="5a9cd-412">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-412">no</span></span>           |
| <span data-ttu-id="5a9cd-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5a9cd-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="5a9cd-414">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-414">no</span></span>             | <span data-ttu-id="5a9cd-415">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-415">no</span></span>           |
| <span data-ttu-id="5a9cd-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="5a9cd-417">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-417">no</span></span>             | <span data-ttu-id="5a9cd-418">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-418">no</span></span>           |
| <span data-ttu-id="5a9cd-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="5a9cd-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="5a9cd-420">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-420">no</span></span>             | <span data-ttu-id="5a9cd-421">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-421">no</span></span>           |
| <span data-ttu-id="5a9cd-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="5a9cd-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="5a9cd-423">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-423">no</span></span>             | <span data-ttu-id="5a9cd-424">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-424">no</span></span>           |
| <span data-ttu-id="5a9cd-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-425">msdyn_projectid</span></span>              | <span data-ttu-id="5a9cd-426">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-426">yes</span></span>            | <span data-ttu-id="5a9cd-427">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-427">no</span></span>           |
| <span data-ttu-id="5a9cd-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-428">msdyn_projectidname</span></span>          | <span data-ttu-id="5a9cd-429">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-429">no</span></span>             | <span data-ttu-id="5a9cd-430">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-430">no</span></span>           |
| <span data-ttu-id="5a9cd-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="5a9cd-432">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-432">no</span></span>             | <span data-ttu-id="5a9cd-433">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-433">no</span></span>           |
| <span data-ttu-id="5a9cd-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="5a9cd-435">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-435">no</span></span>             | <span data-ttu-id="5a9cd-436">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-436">no</span></span>           |
| <span data-ttu-id="5a9cd-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="5a9cd-437">msdyn_start</span></span>                  | <span data-ttu-id="5a9cd-438">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-438">no</span></span>             | <span data-ttu-id="5a9cd-439">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-439">no</span></span>           |
| <span data-ttu-id="5a9cd-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-440">msdyn_taskid</span></span>                 | <span data-ttu-id="5a9cd-441">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-441">no</span></span>             | <span data-ttu-id="5a9cd-442">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-442">no</span></span>           |
| <span data-ttu-id="5a9cd-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-443">msdyn_taskidname</span></span>             | <span data-ttu-id="5a9cd-444">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-444">no</span></span>             | <span data-ttu-id="5a9cd-445">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-445">no</span></span>           |
| <span data-ttu-id="5a9cd-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="5a9cd-447">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-447">no</span></span>             | <span data-ttu-id="5a9cd-448">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="5a9cd-449">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="5a9cd-449">Project team member</span></span>

| <span data-ttu-id="5a9cd-450">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-450">**Logical name**</span></span>                                 | <span data-ttu-id="5a9cd-451">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-451">**Can create**</span></span> | <span data-ttu-id="5a9cd-452">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="5a9cd-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="5a9cd-454">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-454">no</span></span>             | <span data-ttu-id="5a9cd-455">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-455">no</span></span>           |
| <span data-ttu-id="5a9cd-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="5a9cd-457">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-457">no</span></span>             | <span data-ttu-id="5a9cd-458">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-458">no</span></span>           |
| <span data-ttu-id="5a9cd-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="5a9cd-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="5a9cd-460">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-460">no</span></span>             | <span data-ttu-id="5a9cd-461">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-461">no</span></span>           |
| <span data-ttu-id="5a9cd-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="5a9cd-463">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-463">no</span></span>             | <span data-ttu-id="5a9cd-464">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-464">no</span></span>           |
| <span data-ttu-id="5a9cd-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5a9cd-465">msdyn_effort</span></span>                                     | <span data-ttu-id="5a9cd-466">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-466">no</span></span>             | <span data-ttu-id="5a9cd-467">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-467">no</span></span>           |
| <span data-ttu-id="5a9cd-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5a9cd-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="5a9cd-469">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-469">no</span></span>             | <span data-ttu-id="5a9cd-470">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-470">no</span></span>           |
| <span data-ttu-id="5a9cd-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5a9cd-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="5a9cd-472">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-472">no</span></span>             | <span data-ttu-id="5a9cd-473">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-473">no</span></span>           |
| <span data-ttu-id="5a9cd-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5a9cd-474">msdyn_finish</span></span>                                     | <span data-ttu-id="5a9cd-475">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-475">no</span></span>             | <span data-ttu-id="5a9cd-476">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-476">no</span></span>           |
| <span data-ttu-id="5a9cd-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="5a9cd-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="5a9cd-478">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-478">no</span></span>             | <span data-ttu-id="5a9cd-479">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-479">no</span></span>           |
| <span data-ttu-id="5a9cd-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="5a9cd-480">msdyn_hours</span></span>                                      | <span data-ttu-id="5a9cd-481">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-481">no</span></span>             | <span data-ttu-id="5a9cd-482">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-482">no</span></span>           |
| <span data-ttu-id="5a9cd-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="5a9cd-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="5a9cd-484">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-484">no</span></span>             | <span data-ttu-id="5a9cd-485">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-485">no</span></span>           |
| <span data-ttu-id="5a9cd-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="5a9cd-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="5a9cd-487">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-487">no</span></span>             | <span data-ttu-id="5a9cd-488">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-488">no</span></span>           |
| <span data-ttu-id="5a9cd-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="5a9cd-490">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-490">no</span></span>             | <span data-ttu-id="5a9cd-491">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-491">no</span></span>           |
| <span data-ttu-id="5a9cd-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="5a9cd-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="5a9cd-493">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-493">no</span></span>             | <span data-ttu-id="5a9cd-494">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-494">no</span></span>           |
| <span data-ttu-id="5a9cd-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="5a9cd-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="5a9cd-496">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-496">no</span></span>             | <span data-ttu-id="5a9cd-497">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-497">no</span></span>           |
| <span data-ttu-id="5a9cd-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="5a9cd-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="5a9cd-499">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-499">no</span></span>             | <span data-ttu-id="5a9cd-500">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-500">no</span></span>           |
| <span data-ttu-id="5a9cd-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="5a9cd-501">msdyn_start</span></span>                                      | <span data-ttu-id="5a9cd-502">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-502">no</span></span>             | <span data-ttu-id="5a9cd-503">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="5a9cd-504">Project</span><span class="sxs-lookup"><span data-stu-id="5a9cd-504">Project</span></span>

| <span data-ttu-id="5a9cd-505">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-505">**Logical name**</span></span>                       | <span data-ttu-id="5a9cd-506">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-506">**Can create**</span></span> | <span data-ttu-id="5a9cd-507">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="5a9cd-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="5a9cd-509">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-509">no</span></span>             | <span data-ttu-id="5a9cd-510">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-510">no</span></span>           |
| <span data-ttu-id="5a9cd-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="5a9cd-512">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-512">no</span></span>             | <span data-ttu-id="5a9cd-513">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-513">no</span></span>           |
| <span data-ttu-id="5a9cd-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="5a9cd-515">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-515">no</span></span>             | <span data-ttu-id="5a9cd-516">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-516">no</span></span>           |
| <span data-ttu-id="5a9cd-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="5a9cd-518">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-518">no</span></span>             | <span data-ttu-id="5a9cd-519">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-519">no</span></span>           |
| <span data-ttu-id="5a9cd-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="5a9cd-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="5a9cd-521">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-521">no</span></span>             | <span data-ttu-id="5a9cd-522">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-522">no</span></span>           |
| <span data-ttu-id="5a9cd-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="5a9cd-524">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-524">no</span></span>             | <span data-ttu-id="5a9cd-525">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-525">no</span></span>           |
| <span data-ttu-id="5a9cd-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="5a9cd-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="5a9cd-527">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-527">yes</span></span>            | <span data-ttu-id="5a9cd-528">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-528">no</span></span>           |
| <span data-ttu-id="5a9cd-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="5a9cd-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="5a9cd-530">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-530">yes</span></span>            | <span data-ttu-id="5a9cd-531">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-531">no</span></span>           |
| <span data-ttu-id="5a9cd-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="5a9cd-533">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-533">yes</span></span>            | <span data-ttu-id="5a9cd-534">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-534">no</span></span>           |
| <span data-ttu-id="5a9cd-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="5a9cd-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="5a9cd-536">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-536">no</span></span>             | <span data-ttu-id="5a9cd-537">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-537">no</span></span>           |
| <span data-ttu-id="5a9cd-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5a9cd-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="5a9cd-539">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-539">no</span></span>             | <span data-ttu-id="5a9cd-540">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-540">no</span></span>           |
| <span data-ttu-id="5a9cd-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="5a9cd-542">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-542">no</span></span>             | <span data-ttu-id="5a9cd-543">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-543">no</span></span>           |
| <span data-ttu-id="5a9cd-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="5a9cd-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="5a9cd-545">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-545">no</span></span>             | <span data-ttu-id="5a9cd-546">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-546">no</span></span>           |
| <span data-ttu-id="5a9cd-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="5a9cd-548">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-548">no</span></span>             | <span data-ttu-id="5a9cd-549">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-549">no</span></span>           |
| <span data-ttu-id="5a9cd-550">msdyn_varighed</span><span class="sxs-lookup"><span data-stu-id="5a9cd-550">msdyn_duration</span></span>                         | <span data-ttu-id="5a9cd-551">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-551">no</span></span>             | <span data-ttu-id="5a9cd-552">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-552">no</span></span>           |
| <span data-ttu-id="5a9cd-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5a9cd-553">msdyn_effort</span></span>                           | <span data-ttu-id="5a9cd-554">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-554">no</span></span>             | <span data-ttu-id="5a9cd-555">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-555">no</span></span>           |
| <span data-ttu-id="5a9cd-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5a9cd-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="5a9cd-557">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-557">no</span></span>             | <span data-ttu-id="5a9cd-558">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-558">no</span></span>           |
| <span data-ttu-id="5a9cd-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="5a9cd-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="5a9cd-560">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-560">no</span></span>             | <span data-ttu-id="5a9cd-561">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-561">no</span></span>           |
| <span data-ttu-id="5a9cd-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5a9cd-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="5a9cd-563">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-563">no</span></span>             | <span data-ttu-id="5a9cd-564">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-564">no</span></span>           |
| <span data-ttu-id="5a9cd-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5a9cd-565">msdyn_finish</span></span>                           | <span data-ttu-id="5a9cd-566">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-566">yes</span></span>            | <span data-ttu-id="5a9cd-567">ja</span><span class="sxs-lookup"><span data-stu-id="5a9cd-567">yes</span></span>          |
| <span data-ttu-id="5a9cd-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="5a9cd-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="5a9cd-569">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-569">no</span></span>             | <span data-ttu-id="5a9cd-570">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-570">no</span></span>           |
| <span data-ttu-id="5a9cd-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="5a9cd-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="5a9cd-572">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-572">no</span></span>             | <span data-ttu-id="5a9cd-573">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-573">no</span></span>           |
| <span data-ttu-id="5a9cd-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="5a9cd-575">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-575">no</span></span>             | <span data-ttu-id="5a9cd-576">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-576">no</span></span>           |
| <span data-ttu-id="5a9cd-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="5a9cd-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="5a9cd-578">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-578">no</span></span>             | <span data-ttu-id="5a9cd-579">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-579">no</span></span>           |
| <span data-ttu-id="5a9cd-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="5a9cd-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="5a9cd-581">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-581">no</span></span>             | <span data-ttu-id="5a9cd-582">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-582">no</span></span>           |
| <span data-ttu-id="5a9cd-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="5a9cd-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="5a9cd-584">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-584">no</span></span>             | <span data-ttu-id="5a9cd-585">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-585">no</span></span>           |
| <span data-ttu-id="5a9cd-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="5a9cd-587">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-587">no</span></span>             | <span data-ttu-id="5a9cd-588">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-588">no</span></span>           |
| <span data-ttu-id="5a9cd-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="5a9cd-590">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-590">no</span></span>             | <span data-ttu-id="5a9cd-591">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-591">no</span></span>           |
| <span data-ttu-id="5a9cd-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="5a9cd-593">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-593">no</span></span>             | <span data-ttu-id="5a9cd-594">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-594">no</span></span>           |
| <span data-ttu-id="5a9cd-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="5a9cd-596">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-596">no</span></span>             | <span data-ttu-id="5a9cd-597">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-597">no</span></span>           |
| <span data-ttu-id="5a9cd-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5a9cd-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="5a9cd-599">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-599">no</span></span>             | <span data-ttu-id="5a9cd-600">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-600">no</span></span>           |
| <span data-ttu-id="5a9cd-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="5a9cd-602">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-602">no</span></span>             | <span data-ttu-id="5a9cd-603">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-603">no</span></span>           |
| <span data-ttu-id="5a9cd-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="5a9cd-604">msdyn_progress</span></span>                         | <span data-ttu-id="5a9cd-605">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-605">no</span></span>             | <span data-ttu-id="5a9cd-606">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-606">no</span></span>           |
| <span data-ttu-id="5a9cd-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="5a9cd-608">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-608">no</span></span>             | <span data-ttu-id="5a9cd-609">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-609">no</span></span>           |
| <span data-ttu-id="5a9cd-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="5a9cd-611">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-611">no</span></span>             | <span data-ttu-id="5a9cd-612">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-612">no</span></span>           |
| <span data-ttu-id="5a9cd-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5a9cd-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="5a9cd-614">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-614">no</span></span>             | <span data-ttu-id="5a9cd-615">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-615">no</span></span>           |
| <span data-ttu-id="5a9cd-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="5a9cd-617">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-617">no</span></span>             | <span data-ttu-id="5a9cd-618">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-618">no</span></span>           |
| <span data-ttu-id="5a9cd-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="5a9cd-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="5a9cd-620">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-620">no</span></span>             | <span data-ttu-id="5a9cd-621">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-621">no</span></span>           |
| <span data-ttu-id="5a9cd-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="5a9cd-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="5a9cd-623">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-623">no</span></span>             | <span data-ttu-id="5a9cd-624">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-624">no</span></span>           |
| <span data-ttu-id="5a9cd-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="5a9cd-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="5a9cd-626">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-626">no</span></span>             | <span data-ttu-id="5a9cd-627">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-627">no</span></span>           |
| <span data-ttu-id="5a9cd-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="5a9cd-629">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-629">no</span></span>             | <span data-ttu-id="5a9cd-630">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-630">no</span></span>           |
| <span data-ttu-id="5a9cd-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="5a9cd-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="5a9cd-632">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-632">no</span></span>             | <span data-ttu-id="5a9cd-633">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-633">no</span></span>           |
| <span data-ttu-id="5a9cd-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="5a9cd-635">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-635">no</span></span>             | <span data-ttu-id="5a9cd-636">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-636">no</span></span>           |
| <span data-ttu-id="5a9cd-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="5a9cd-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="5a9cd-638">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-638">no</span></span>             | <span data-ttu-id="5a9cd-639">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-639">no</span></span>           |
| <span data-ttu-id="5a9cd-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="5a9cd-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="5a9cd-641">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-641">no</span></span>             | <span data-ttu-id="5a9cd-642">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-642">no</span></span>           |
| <span data-ttu-id="5a9cd-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="5a9cd-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="5a9cd-644">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-644">no</span></span>             | <span data-ttu-id="5a9cd-645">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-645">no</span></span>           |
| <span data-ttu-id="5a9cd-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="5a9cd-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="5a9cd-647">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-647">no</span></span>             | <span data-ttu-id="5a9cd-648">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-648">no</span></span>           |
| <span data-ttu-id="5a9cd-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="5a9cd-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="5a9cd-650">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-650">no</span></span>             | <span data-ttu-id="5a9cd-651">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-651">no</span></span>           |
| <span data-ttu-id="5a9cd-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="5a9cd-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="5a9cd-653">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-653">no</span></span>             | <span data-ttu-id="5a9cd-654">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-654">no</span></span>           |
| <span data-ttu-id="5a9cd-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="5a9cd-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="5a9cd-656">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-656">no</span></span>             | <span data-ttu-id="5a9cd-657">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-657">no</span></span>           |
| <span data-ttu-id="5a9cd-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="5a9cd-659">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-659">no</span></span>             | <span data-ttu-id="5a9cd-660">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-660">no</span></span>           |
| <span data-ttu-id="5a9cd-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="5a9cd-662">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-662">no</span></span>             | <span data-ttu-id="5a9cd-663">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-663">no</span></span>           |
| <span data-ttu-id="5a9cd-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="5a9cd-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="5a9cd-665">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-665">no</span></span>             | <span data-ttu-id="5a9cd-666">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-666">no</span></span>           |
| <span data-ttu-id="5a9cd-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5a9cd-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="5a9cd-668">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-668">no</span></span>             | <span data-ttu-id="5a9cd-669">nej</span><span class="sxs-lookup"><span data-stu-id="5a9cd-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="5a9cd-670">Begrænsninger og kendte problemer</span><span class="sxs-lookup"><span data-stu-id="5a9cd-670">Limitations and known issues</span></span>
<span data-ttu-id="5a9cd-671">Her følger en liste over begrænsninger og kendte problemer:</span><span class="sxs-lookup"><span data-stu-id="5a9cd-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="5a9cd-672">Planlægnings-API'er kan kun bruges af **Brugere med Microsoft Project-licens.**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="5a9cd-673">De kan ikke bruges af:</span><span class="sxs-lookup"><span data-stu-id="5a9cd-673">They can't be used by:</span></span>
    - <span data-ttu-id="5a9cd-674">Programbrugere</span><span class="sxs-lookup"><span data-stu-id="5a9cd-674">Application users</span></span>
    - <span data-ttu-id="5a9cd-675">Systembrugere</span><span class="sxs-lookup"><span data-stu-id="5a9cd-675">System users</span></span>
    - <span data-ttu-id="5a9cd-676">Integrationsbrugere</span><span class="sxs-lookup"><span data-stu-id="5a9cd-676">Integration users</span></span>
    - <span data-ttu-id="5a9cd-677">Andre brugere, der ikke har den påkrævede licens</span><span class="sxs-lookup"><span data-stu-id="5a9cd-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="5a9cd-678">Hvert **OperationSet** kan kun have op til 100 handlinger.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="5a9cd-679">Hver bruger kan kun have op til 10 åbne **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="5a9cd-680">Project Operations understøtter i øjeblikket maksimalt 500 opgaver i alt på et projekt.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="5a9cd-681">Status for fejl i **OperationSet** og fejllogfiler er ikke tilgængelige i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="5a9cd-682">Begrænsninger og grænser for projekter og opgaver</span><span class="sxs-lookup"><span data-stu-id="5a9cd-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="5a9cd-683">Fejlhåndtering</span><span class="sxs-lookup"><span data-stu-id="5a9cd-683">Error handling</span></span>

   - <span data-ttu-id="5a9cd-684">Hvis du vil gennemse de fejl, der er genereret i operationssæt, skal du gå til **Indstillinger** \> **Integration af planlægning** \> **Operationssæt**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="5a9cd-685">Hvis du vil gennemse de fejl, der er genereret fra tjenesten Project Service, skal du gå til **Indstillinger** \> **Integration af planlægning** \> **PSS-fejllogfiler**.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="5a9cd-686">Eksempelscenarie</span><span class="sxs-lookup"><span data-stu-id="5a9cd-686">Sample scenario</span></span>

<span data-ttu-id="5a9cd-687">I dette scenario skal du oprette et projekt, et teammedlem, fire opgaver og to ressourcetildelinger.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="5a9cd-688">Derefter skal du opdatere én opgave, opdatere projektet, slette én opgave, slette én ressourcetildeling og oprette en opgaveafhængighed.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="5a9cd-689">Yderligere eksempler</span><span class="sxs-lookup"><span data-stu-id="5a9cd-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
