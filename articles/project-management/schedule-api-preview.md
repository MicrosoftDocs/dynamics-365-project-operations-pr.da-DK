---
title: Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter
description: Dette emne indeholder oplysninger og eksempler på brug af projektplanlægnings-API'er.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293220"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="7cadc-103">Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter</span><span class="sxs-lookup"><span data-stu-id="7cadc-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="7cadc-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="7cadc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="7cadc-105">Visse eller alle de funktioner, der er omtalt i dette emne, er tilgængelige som en del af en forhåndsversion.</span><span class="sxs-lookup"><span data-stu-id="7cadc-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="7cadc-106">Indholdet og funktionerne kan ændres.</span><span class="sxs-lookup"><span data-stu-id="7cadc-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="7cadc-107">Planlægningsobjekter</span><span class="sxs-lookup"><span data-stu-id="7cadc-107">Scheduling entities</span></span>

<span data-ttu-id="7cadc-108">Projektplanlægnings-API'er gør det muligt at oprette, opdatere og slette handlinger med **Planlægningsobjekter**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="7cadc-109">Disse objekter administreres via planlægningsprogrammet i Projekt til internettet.</span><span class="sxs-lookup"><span data-stu-id="7cadc-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="7cadc-110">Handlinger til oprettelse, opdatering og sletning med **Planlægningsobjekter** var i tidligere udgivelser til Dynamics 365 Project Operations begrænset.</span><span class="sxs-lookup"><span data-stu-id="7cadc-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="7cadc-111">Følgende tabel indeholder en fuldstændig liste over projektplanlægningsobjekterne.</span><span class="sxs-lookup"><span data-stu-id="7cadc-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="7cadc-112">Enhedsnavn</span><span class="sxs-lookup"><span data-stu-id="7cadc-112">Entity name</span></span>  | <span data-ttu-id="7cadc-113">Objektets logiske navn</span><span class="sxs-lookup"><span data-stu-id="7cadc-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="7cadc-114">Project</span><span class="sxs-lookup"><span data-stu-id="7cadc-114">Project</span></span> | <span data-ttu-id="7cadc-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="7cadc-115">msdyn_project</span></span> |
| <span data-ttu-id="7cadc-116">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="7cadc-116">Project Task</span></span>  | <span data-ttu-id="7cadc-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="7cadc-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="7cadc-118">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="7cadc-118">Project Task Dependency</span></span>  | <span data-ttu-id="7cadc-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="7cadc-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="7cadc-120">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="7cadc-120">Resource Assignment</span></span> | <span data-ttu-id="7cadc-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="7cadc-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="7cadc-122">Projektbucket</span><span class="sxs-lookup"><span data-stu-id="7cadc-122">Project Bucket</span></span>  | <span data-ttu-id="7cadc-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="7cadc-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="7cadc-124">Medlem af projektteam</span><span class="sxs-lookup"><span data-stu-id="7cadc-124">Project Team Member</span></span> | <span data-ttu-id="7cadc-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="7cadc-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="7cadc-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="7cadc-126">OperationSet</span></span>

<span data-ttu-id="7cadc-127">OperationSet er et arbejdsenhedsmønster, der kan bruges, når flere forespørgsler, der påvirker tidsplanen, skal behandles i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="7cadc-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="7cadc-128">Projektplanlægnings-API'er</span><span class="sxs-lookup"><span data-stu-id="7cadc-128">Project schedule APIs</span></span>

<span data-ttu-id="7cadc-129">Følgende er en liste over aktuelle projektplanlægnings-API'er.</span><span class="sxs-lookup"><span data-stu-id="7cadc-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="7cadc-130">**msdyn_CreateProjectV1**: Denne API kan bruges til at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="7cadc-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="7cadc-131">Projekt- og standardprojektbucket oprettes med det samme.</span><span class="sxs-lookup"><span data-stu-id="7cadc-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="7cadc-132">**msdyn_CreateTeamMemberV1**: Denne API kan bruges til at oprette et projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="7cadc-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="7cadc-133">Teammedlemsposten oprettes med det samme.</span><span class="sxs-lookup"><span data-stu-id="7cadc-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="7cadc-134">**msdyn_CreateOperationSetV1**: Denne API kan bruges til at planlægge flere forespørgsler, der skal udføres i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="7cadc-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="7cadc-135">**msdyn_PSSCreateV1**: Denne API kan bruges til at oprette et objekt.</span><span class="sxs-lookup"><span data-stu-id="7cadc-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="7cadc-136">Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter oprettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="7cadc-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="7cadc-137">**msdyn_PSSUpdateV1**: Denne API kan bruges til at opdatere et objekt.</span><span class="sxs-lookup"><span data-stu-id="7cadc-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="7cadc-138">Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter opdateringshandlingen.</span><span class="sxs-lookup"><span data-stu-id="7cadc-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="7cadc-139">**msdyn_PSSDeleteV1**: Denne API kan bruges til at slette et objekt.</span><span class="sxs-lookup"><span data-stu-id="7cadc-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="7cadc-140">Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter slettehandlingen.</span><span class="sxs-lookup"><span data-stu-id="7cadc-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="7cadc-141">**msdyn_ExecuteOperationSetV1**: Denne API bruges til at udføre alle handlinger i det givne operationssæt.</span><span class="sxs-lookup"><span data-stu-id="7cadc-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="7cadc-142">Brug af projektplanlægnings-API'er med handlingssæt</span><span class="sxs-lookup"><span data-stu-id="7cadc-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="7cadc-143">Da poster med både **CreateProjectV1** og **CreateTeamMemberV1** oprettes med det samme, kan disse API'er ikke bruges direkte i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="7cadc-144">Du kan dog bruge API'en til at oprette de krævede poster, et **OperationSet** og derefter bruge disse forudoprettede poster i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="7cadc-145">Understøttede handlinger</span><span class="sxs-lookup"><span data-stu-id="7cadc-145">Supported operations</span></span>

| <span data-ttu-id="7cadc-146">Planlægningsobjekt</span><span class="sxs-lookup"><span data-stu-id="7cadc-146">Scheduling entity</span></span> | <span data-ttu-id="7cadc-147">Opret</span><span class="sxs-lookup"><span data-stu-id="7cadc-147">Create</span></span> | <span data-ttu-id="7cadc-148">Opdatering</span><span class="sxs-lookup"><span data-stu-id="7cadc-148">Update</span></span> | <span data-ttu-id="7cadc-149">Delete</span><span class="sxs-lookup"><span data-stu-id="7cadc-149">Delete</span></span> | <span data-ttu-id="7cadc-150">Vigtige overvejelser</span><span class="sxs-lookup"><span data-stu-id="7cadc-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="7cadc-151">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="7cadc-151">Project task</span></span> | <span data-ttu-id="7cadc-152">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-152">Yes</span></span> | <span data-ttu-id="7cadc-153">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-153">Yes</span></span> | <span data-ttu-id="7cadc-154">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-154">Yes</span></span> | <span data-ttu-id="7cadc-155">Intet</span><span class="sxs-lookup"><span data-stu-id="7cadc-155">None</span></span> |
| <span data-ttu-id="7cadc-156">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="7cadc-156">Project task dependency</span></span> | <span data-ttu-id="7cadc-157">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-157">Yes</span></span> | <span data-ttu-id="7cadc-158">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-158">Yes</span></span> | | <span data-ttu-id="7cadc-159">Projektopgaveafhængighedsposter opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="7cadc-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="7cadc-160">I stedet kan en gammel post slettes, og der kan oprettes en ny post.</span><span class="sxs-lookup"><span data-stu-id="7cadc-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="7cadc-161">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="7cadc-161">Resource assignment</span></span> | <span data-ttu-id="7cadc-162">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-162">Yes</span></span> | <span data-ttu-id="7cadc-163">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-163">Yes</span></span> | | <span data-ttu-id="7cadc-164">Handlinger med følgende felter understøttes ikke: **BookableResourceID**, **Indsats**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="7cadc-165">Ressourcetildelingsposter opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="7cadc-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="7cadc-166">I stedet kan den gamle post slettes, og der kan oprettes en ny post.</span><span class="sxs-lookup"><span data-stu-id="7cadc-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="7cadc-167">Projektbucket</span><span class="sxs-lookup"><span data-stu-id="7cadc-167">Project bucket</span></span> | <span data-ttu-id="7cadc-168">I/R</span><span class="sxs-lookup"><span data-stu-id="7cadc-168">N/A</span></span> | <span data-ttu-id="7cadc-169">I/R</span><span class="sxs-lookup"><span data-stu-id="7cadc-169">N/A</span></span> | <span data-ttu-id="7cadc-170">I/R</span><span class="sxs-lookup"><span data-stu-id="7cadc-170">N/A</span></span> | <span data-ttu-id="7cadc-171">Standardbucket oprettes ved hjælp af API'en **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="7cadc-172">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="7cadc-172">Project team member</span></span> | <span data-ttu-id="7cadc-173">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-173">Yes</span></span> | <span data-ttu-id="7cadc-174">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-174">Yes</span></span> | <span data-ttu-id="7cadc-175">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-175">Yes</span></span> | <span data-ttu-id="7cadc-176">Brug API'en **CreateTeamMemberV1** til oprettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="7cadc-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="7cadc-177">Project</span><span class="sxs-lookup"><span data-stu-id="7cadc-177">Project</span></span> | <span data-ttu-id="7cadc-178">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-178">Yes</span></span> | <span data-ttu-id="7cadc-179">Ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-179">Yes</span></span> | <span data-ttu-id="7cadc-180">I/R</span><span class="sxs-lookup"><span data-stu-id="7cadc-180">N/A</span></span> | <span data-ttu-id="7cadc-181">Handlinger med følgende felter understøttes ikke: **StateCode**, **BulkStatus**, **GlobalRevisionToken**, **CalendarID**, **Indsats**, **EffortCompleted**, **EffortRemaining**, **Status**, **Afsluttet**, **TaskEarliestStart** og **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="7cadc-182">Disse API'er kan kaldes sammen med enhedsobjekter, der indeholder brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="7cadc-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="7cadc-183">Id-egenskaben er valgfri.</span><span class="sxs-lookup"><span data-stu-id="7cadc-183">The ID property is optional.</span></span> <span data-ttu-id="7cadc-184">Hvis den oplyses, forsøger systemet at bruge den, og der udløses en undtagelse, hvis den ikke kan bruges.</span><span class="sxs-lookup"><span data-stu-id="7cadc-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="7cadc-185">Hvis den ikke er angivet, oprettes den af systemet.</span><span class="sxs-lookup"><span data-stu-id="7cadc-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="7cadc-186">Begrænsede felter</span><span class="sxs-lookup"><span data-stu-id="7cadc-186">Restricted fields</span></span>

<span data-ttu-id="7cadc-187">I følgende tabeller defineres de felter, der er begrænset fra **Opret** og **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="7cadc-188">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="7cadc-188">Project task</span></span>

| <span data-ttu-id="7cadc-189">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="7cadc-189">**Logical name**</span></span>                       | <span data-ttu-id="7cadc-190">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="7cadc-190">**Can create**</span></span> | <span data-ttu-id="7cadc-191">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="7cadc-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="7cadc-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="7cadc-193">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-193">no</span></span>             | <span data-ttu-id="7cadc-194">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-194">no</span></span>               |
| <span data-ttu-id="7cadc-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="7cadc-196">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-196">no</span></span>             | <span data-ttu-id="7cadc-197">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-197">no</span></span>               |
| <span data-ttu-id="7cadc-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="7cadc-198">msdyn_actualend</span></span>                        | <span data-ttu-id="7cadc-199">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-199">no</span></span>             | <span data-ttu-id="7cadc-200">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-200">no</span></span>               |
| <span data-ttu-id="7cadc-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="7cadc-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="7cadc-202">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-202">no</span></span>             | <span data-ttu-id="7cadc-203">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-203">no</span></span>               |
| <span data-ttu-id="7cadc-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="7cadc-205">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-205">no</span></span>             | <span data-ttu-id="7cadc-206">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-206">no</span></span>               |
| <span data-ttu-id="7cadc-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="7cadc-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="7cadc-208">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-208">no</span></span>             | <span data-ttu-id="7cadc-209">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-209">no</span></span>               |
| <span data-ttu-id="7cadc-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="7cadc-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="7cadc-211">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-211">no</span></span>             | <span data-ttu-id="7cadc-212">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-212">no</span></span>               |
| <span data-ttu-id="7cadc-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="7cadc-214">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-214">no</span></span>             | <span data-ttu-id="7cadc-215">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-215">no</span></span>               |
| <span data-ttu-id="7cadc-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="7cadc-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="7cadc-217">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-217">no</span></span>             | <span data-ttu-id="7cadc-218">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-218">no</span></span>               |
| <span data-ttu-id="7cadc-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7cadc-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="7cadc-220">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-220">no</span></span>             | <span data-ttu-id="7cadc-221">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-221">no</span></span>               |
| <span data-ttu-id="7cadc-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7cadc-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="7cadc-223">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-223">no</span></span>             | <span data-ttu-id="7cadc-224">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-224">no</span></span>               |
| <span data-ttu-id="7cadc-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="7cadc-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="7cadc-226">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-226">no</span></span>             | <span data-ttu-id="7cadc-227">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-227">no</span></span>               |
| <span data-ttu-id="7cadc-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="7cadc-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="7cadc-229">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-229">no</span></span>             | <span data-ttu-id="7cadc-230">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-230">no</span></span>               |
| <span data-ttu-id="7cadc-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="7cadc-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="7cadc-232">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-232">no</span></span>             | <span data-ttu-id="7cadc-233">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-233">no</span></span>               |
| <span data-ttu-id="7cadc-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="7cadc-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="7cadc-235">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-235">no</span></span>             | <span data-ttu-id="7cadc-236">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-236">no</span></span>               |
| <span data-ttu-id="7cadc-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="7cadc-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="7cadc-238">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-238">no</span></span>             | <span data-ttu-id="7cadc-239">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-239">no</span></span>               |
| <span data-ttu-id="7cadc-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="7cadc-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="7cadc-241">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-241">no</span></span>             | <span data-ttu-id="7cadc-242">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-242">no</span></span>               |
| <span data-ttu-id="7cadc-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="7cadc-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="7cadc-244">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-244">no</span></span>             | <span data-ttu-id="7cadc-245">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-245">no</span></span>               |
| <span data-ttu-id="7cadc-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="7cadc-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="7cadc-247">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-247">no</span></span>             | <span data-ttu-id="7cadc-248">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-248">no</span></span>               |
| <span data-ttu-id="7cadc-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="7cadc-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="7cadc-250">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-250">no</span></span>             | <span data-ttu-id="7cadc-251">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-251">no</span></span>               |
| <span data-ttu-id="7cadc-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="7cadc-253">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-253">no</span></span>             | <span data-ttu-id="7cadc-254">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-254">no</span></span>               |
| <span data-ttu-id="7cadc-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="7cadc-256">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-256">no</span></span>             | <span data-ttu-id="7cadc-257">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-257">no</span></span>               |
| <span data-ttu-id="7cadc-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7cadc-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="7cadc-259">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-259">no</span></span>             | <span data-ttu-id="7cadc-260">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-260">no</span></span>               |
| <span data-ttu-id="7cadc-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="7cadc-262">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-262">no</span></span>             | <span data-ttu-id="7cadc-263">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-263">no</span></span>               |
| <span data-ttu-id="7cadc-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="7cadc-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="7cadc-265">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-265">no</span></span>             | <span data-ttu-id="7cadc-266">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-266">no</span></span>               |
| <span data-ttu-id="7cadc-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="7cadc-267">msdyn_progress</span></span>                         | <span data-ttu-id="7cadc-268">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-268">no</span></span>             | <span data-ttu-id="7cadc-269">nej (ja for P4W)</span><span class="sxs-lookup"><span data-stu-id="7cadc-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="7cadc-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="7cadc-271">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-271">no</span></span>             | <span data-ttu-id="7cadc-272">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-272">no</span></span>               |
| <span data-ttu-id="7cadc-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="7cadc-274">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-274">no</span></span>             | <span data-ttu-id="7cadc-275">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-275">no</span></span>               |
| <span data-ttu-id="7cadc-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7cadc-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="7cadc-277">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-277">no</span></span>             | <span data-ttu-id="7cadc-278">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-278">no</span></span>               |
| <span data-ttu-id="7cadc-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="7cadc-280">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-280">no</span></span>             | <span data-ttu-id="7cadc-281">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-281">no</span></span>               |
| <span data-ttu-id="7cadc-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="7cadc-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="7cadc-283">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-283">no</span></span>             | <span data-ttu-id="7cadc-284">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-284">no</span></span>               |
| <span data-ttu-id="7cadc-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="7cadc-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="7cadc-286">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-286">no</span></span>             | <span data-ttu-id="7cadc-287">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-287">no</span></span>               |
| <span data-ttu-id="7cadc-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="7cadc-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="7cadc-289">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-289">no</span></span>             | <span data-ttu-id="7cadc-290">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-290">no</span></span>               |
| <span data-ttu-id="7cadc-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="7cadc-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="7cadc-292">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-292">no</span></span>             | <span data-ttu-id="7cadc-293">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-293">no</span></span>               |
| <span data-ttu-id="7cadc-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="7cadc-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="7cadc-295">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-295">no</span></span>             | <span data-ttu-id="7cadc-296">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-296">no</span></span>               |
| <span data-ttu-id="7cadc-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="7cadc-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="7cadc-298">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-298">no</span></span>             | <span data-ttu-id="7cadc-299">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-299">no</span></span>               |
| <span data-ttu-id="7cadc-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7cadc-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="7cadc-301">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-301">no</span></span>             | <span data-ttu-id="7cadc-302">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-302">no</span></span>               |
| <span data-ttu-id="7cadc-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="7cadc-304">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-304">no</span></span>             | <span data-ttu-id="7cadc-305">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-305">no</span></span>               |
| <span data-ttu-id="7cadc-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="7cadc-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="7cadc-307">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-307">no</span></span>             | <span data-ttu-id="7cadc-308">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-308">no</span></span>               |
| <span data-ttu-id="7cadc-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="7cadc-310">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-310">no</span></span>             | <span data-ttu-id="7cadc-311">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-311">no</span></span>               |
| <span data-ttu-id="7cadc-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="7cadc-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="7cadc-313">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-313">no</span></span>             | <span data-ttu-id="7cadc-314">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-314">no</span></span>               |
| <span data-ttu-id="7cadc-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="7cadc-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="7cadc-316">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-316">no</span></span>             | <span data-ttu-id="7cadc-317">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-317">no</span></span>               |
| <span data-ttu-id="7cadc-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="7cadc-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="7cadc-319">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-319">no</span></span>             | <span data-ttu-id="7cadc-320">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-320">no</span></span>               |
| <span data-ttu-id="7cadc-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="7cadc-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="7cadc-322">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-322">no</span></span>             | <span data-ttu-id="7cadc-323">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-323">no</span></span>               |
| <span data-ttu-id="7cadc-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="7cadc-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="7cadc-325">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-325">no</span></span>             | <span data-ttu-id="7cadc-326">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-326">no</span></span>               |
| <span data-ttu-id="7cadc-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="7cadc-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="7cadc-328">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-328">no</span></span>             | <span data-ttu-id="7cadc-329">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-329">no</span></span>               |
| <span data-ttu-id="7cadc-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="7cadc-330">msdyn_summary</span></span>                          | <span data-ttu-id="7cadc-331">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-331">no</span></span>             | <span data-ttu-id="7cadc-332">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-332">no</span></span>               |
| <span data-ttu-id="7cadc-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="7cadc-334">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-334">no</span></span>             | <span data-ttu-id="7cadc-335">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-335">no</span></span>               |
| <span data-ttu-id="7cadc-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="7cadc-337">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-337">no</span></span>             | <span data-ttu-id="7cadc-338">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="7cadc-339">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="7cadc-339">Project task dependency</span></span>

| <span data-ttu-id="7cadc-340">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="7cadc-340">**Logical name**</span></span>              | <span data-ttu-id="7cadc-341">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="7cadc-341">**Can create**</span></span> | <span data-ttu-id="7cadc-342">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="7cadc-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="7cadc-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="7cadc-343">msdyn_linktype</span></span>                | <span data-ttu-id="7cadc-344">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-344">no</span></span>             | <span data-ttu-id="7cadc-345">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-345">no</span></span>           |
| <span data-ttu-id="7cadc-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="7cadc-346">msdyn_linktypename</span></span>            | <span data-ttu-id="7cadc-347">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-347">no</span></span>             | <span data-ttu-id="7cadc-348">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-348">no</span></span>           |
| <span data-ttu-id="7cadc-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="7cadc-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="7cadc-350">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-350">yes</span></span>            | <span data-ttu-id="7cadc-351">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-351">no</span></span>           |
| <span data-ttu-id="7cadc-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="7cadc-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="7cadc-353">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-353">yes</span></span>            | <span data-ttu-id="7cadc-354">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-354">no</span></span>           |
| <span data-ttu-id="7cadc-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="7cadc-355">msdyn_project</span></span>                 | <span data-ttu-id="7cadc-356">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-356">yes</span></span>            | <span data-ttu-id="7cadc-357">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-357">no</span></span>           |
| <span data-ttu-id="7cadc-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="7cadc-358">msdyn_projectname</span></span>             | <span data-ttu-id="7cadc-359">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-359">yes</span></span>            | <span data-ttu-id="7cadc-360">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-360">no</span></span>           |
| <span data-ttu-id="7cadc-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="7cadc-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="7cadc-362">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-362">yes</span></span>            | <span data-ttu-id="7cadc-363">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-363">no</span></span>           |
| <span data-ttu-id="7cadc-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="7cadc-364">msdyn_successortask</span></span>           | <span data-ttu-id="7cadc-365">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-365">yes</span></span>            | <span data-ttu-id="7cadc-366">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-366">no</span></span>           |
| <span data-ttu-id="7cadc-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="7cadc-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="7cadc-368">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-368">yes</span></span>            | <span data-ttu-id="7cadc-369">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="7cadc-370">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="7cadc-370">Resource assignment</span></span>

| <span data-ttu-id="7cadc-371">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="7cadc-371">**Logical name**</span></span>             | <span data-ttu-id="7cadc-372">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="7cadc-372">**Can create**</span></span> | <span data-ttu-id="7cadc-373">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="7cadc-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="7cadc-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="7cadc-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="7cadc-375">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-375">yes</span></span>            | <span data-ttu-id="7cadc-376">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-376">no</span></span>           |
| <span data-ttu-id="7cadc-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="7cadc-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="7cadc-378">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-378">yes</span></span>            | <span data-ttu-id="7cadc-379">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-379">no</span></span>           |
| <span data-ttu-id="7cadc-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="7cadc-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="7cadc-381">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-381">no</span></span>             | <span data-ttu-id="7cadc-382">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-382">no</span></span>           |
| <span data-ttu-id="7cadc-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="7cadc-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="7cadc-384">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-384">no</span></span>             | <span data-ttu-id="7cadc-385">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-385">no</span></span>           |
| <span data-ttu-id="7cadc-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="7cadc-386">msdyn_committype</span></span>             | <span data-ttu-id="7cadc-387">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-387">no</span></span>             | <span data-ttu-id="7cadc-388">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-388">no</span></span>           |
| <span data-ttu-id="7cadc-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="7cadc-389">msdyn_committypename</span></span>         | <span data-ttu-id="7cadc-390">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-390">no</span></span>             | <span data-ttu-id="7cadc-391">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-391">no</span></span>           |
| <span data-ttu-id="7cadc-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7cadc-392">msdyn_effort</span></span>                 | <span data-ttu-id="7cadc-393">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-393">no</span></span>             | <span data-ttu-id="7cadc-394">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-394">no</span></span>           |
| <span data-ttu-id="7cadc-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7cadc-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="7cadc-396">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-396">no</span></span>             | <span data-ttu-id="7cadc-397">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-397">no</span></span>           |
| <span data-ttu-id="7cadc-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7cadc-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="7cadc-399">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-399">no</span></span>             | <span data-ttu-id="7cadc-400">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-400">no</span></span>           |
| <span data-ttu-id="7cadc-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7cadc-401">msdyn_finish</span></span>                 | <span data-ttu-id="7cadc-402">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-402">no</span></span>             | <span data-ttu-id="7cadc-403">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-403">no</span></span>           |
| <span data-ttu-id="7cadc-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="7cadc-405">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-405">no</span></span>             | <span data-ttu-id="7cadc-406">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-406">no</span></span>           |
| <span data-ttu-id="7cadc-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="7cadc-408">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-408">no</span></span>             | <span data-ttu-id="7cadc-409">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-409">no</span></span>           |
| <span data-ttu-id="7cadc-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="7cadc-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="7cadc-411">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-411">no</span></span>             | <span data-ttu-id="7cadc-412">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-412">no</span></span>           |
| <span data-ttu-id="7cadc-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7cadc-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="7cadc-414">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-414">no</span></span>             | <span data-ttu-id="7cadc-415">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-415">no</span></span>           |
| <span data-ttu-id="7cadc-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="7cadc-417">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-417">no</span></span>             | <span data-ttu-id="7cadc-418">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-418">no</span></span>           |
| <span data-ttu-id="7cadc-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="7cadc-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="7cadc-420">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-420">no</span></span>             | <span data-ttu-id="7cadc-421">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-421">no</span></span>           |
| <span data-ttu-id="7cadc-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="7cadc-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="7cadc-423">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-423">no</span></span>             | <span data-ttu-id="7cadc-424">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-424">no</span></span>           |
| <span data-ttu-id="7cadc-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="7cadc-425">msdyn_projectid</span></span>              | <span data-ttu-id="7cadc-426">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-426">yes</span></span>            | <span data-ttu-id="7cadc-427">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-427">no</span></span>           |
| <span data-ttu-id="7cadc-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="7cadc-428">msdyn_projectidname</span></span>          | <span data-ttu-id="7cadc-429">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-429">no</span></span>             | <span data-ttu-id="7cadc-430">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-430">no</span></span>           |
| <span data-ttu-id="7cadc-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="7cadc-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="7cadc-432">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-432">no</span></span>             | <span data-ttu-id="7cadc-433">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-433">no</span></span>           |
| <span data-ttu-id="7cadc-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="7cadc-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="7cadc-435">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-435">no</span></span>             | <span data-ttu-id="7cadc-436">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-436">no</span></span>           |
| <span data-ttu-id="7cadc-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="7cadc-437">msdyn_start</span></span>                  | <span data-ttu-id="7cadc-438">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-438">no</span></span>             | <span data-ttu-id="7cadc-439">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-439">no</span></span>           |
| <span data-ttu-id="7cadc-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="7cadc-440">msdyn_taskid</span></span>                 | <span data-ttu-id="7cadc-441">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-441">no</span></span>             | <span data-ttu-id="7cadc-442">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-442">no</span></span>           |
| <span data-ttu-id="7cadc-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="7cadc-443">msdyn_taskidname</span></span>             | <span data-ttu-id="7cadc-444">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-444">no</span></span>             | <span data-ttu-id="7cadc-445">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-445">no</span></span>           |
| <span data-ttu-id="7cadc-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="7cadc-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="7cadc-447">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-447">no</span></span>             | <span data-ttu-id="7cadc-448">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="7cadc-449">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="7cadc-449">Project team member</span></span>

| <span data-ttu-id="7cadc-450">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="7cadc-450">**Logical name**</span></span>                                 | <span data-ttu-id="7cadc-451">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="7cadc-451">**Can create**</span></span> | <span data-ttu-id="7cadc-452">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="7cadc-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="7cadc-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="7cadc-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="7cadc-454">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-454">no</span></span>             | <span data-ttu-id="7cadc-455">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-455">no</span></span>           |
| <span data-ttu-id="7cadc-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="7cadc-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="7cadc-457">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-457">no</span></span>             | <span data-ttu-id="7cadc-458">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-458">no</span></span>           |
| <span data-ttu-id="7cadc-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="7cadc-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="7cadc-460">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-460">no</span></span>             | <span data-ttu-id="7cadc-461">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-461">no</span></span>           |
| <span data-ttu-id="7cadc-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="7cadc-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="7cadc-463">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-463">no</span></span>             | <span data-ttu-id="7cadc-464">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-464">no</span></span>           |
| <span data-ttu-id="7cadc-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7cadc-465">msdyn_effort</span></span>                                     | <span data-ttu-id="7cadc-466">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-466">no</span></span>             | <span data-ttu-id="7cadc-467">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-467">no</span></span>           |
| <span data-ttu-id="7cadc-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7cadc-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="7cadc-469">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-469">no</span></span>             | <span data-ttu-id="7cadc-470">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-470">no</span></span>           |
| <span data-ttu-id="7cadc-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7cadc-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="7cadc-472">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-472">no</span></span>             | <span data-ttu-id="7cadc-473">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-473">no</span></span>           |
| <span data-ttu-id="7cadc-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7cadc-474">msdyn_finish</span></span>                                     | <span data-ttu-id="7cadc-475">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-475">no</span></span>             | <span data-ttu-id="7cadc-476">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-476">no</span></span>           |
| <span data-ttu-id="7cadc-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="7cadc-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="7cadc-478">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-478">no</span></span>             | <span data-ttu-id="7cadc-479">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-479">no</span></span>           |
| <span data-ttu-id="7cadc-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="7cadc-480">msdyn_hours</span></span>                                      | <span data-ttu-id="7cadc-481">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-481">no</span></span>             | <span data-ttu-id="7cadc-482">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-482">no</span></span>           |
| <span data-ttu-id="7cadc-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="7cadc-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="7cadc-484">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-484">no</span></span>             | <span data-ttu-id="7cadc-485">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-485">no</span></span>           |
| <span data-ttu-id="7cadc-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="7cadc-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="7cadc-487">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-487">no</span></span>             | <span data-ttu-id="7cadc-488">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-488">no</span></span>           |
| <span data-ttu-id="7cadc-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="7cadc-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="7cadc-490">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-490">no</span></span>             | <span data-ttu-id="7cadc-491">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-491">no</span></span>           |
| <span data-ttu-id="7cadc-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="7cadc-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="7cadc-493">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-493">no</span></span>             | <span data-ttu-id="7cadc-494">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-494">no</span></span>           |
| <span data-ttu-id="7cadc-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="7cadc-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="7cadc-496">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-496">no</span></span>             | <span data-ttu-id="7cadc-497">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-497">no</span></span>           |
| <span data-ttu-id="7cadc-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="7cadc-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="7cadc-499">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-499">no</span></span>             | <span data-ttu-id="7cadc-500">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-500">no</span></span>           |
| <span data-ttu-id="7cadc-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="7cadc-501">msdyn_start</span></span>                                      | <span data-ttu-id="7cadc-502">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-502">no</span></span>             | <span data-ttu-id="7cadc-503">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="7cadc-504">Project</span><span class="sxs-lookup"><span data-stu-id="7cadc-504">Project</span></span>

| <span data-ttu-id="7cadc-505">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="7cadc-505">**Logical name**</span></span>                       | <span data-ttu-id="7cadc-506">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="7cadc-506">**Can create**</span></span> | <span data-ttu-id="7cadc-507">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="7cadc-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="7cadc-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="7cadc-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="7cadc-509">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-509">no</span></span>             | <span data-ttu-id="7cadc-510">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-510">no</span></span>           |
| <span data-ttu-id="7cadc-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="7cadc-512">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-512">no</span></span>             | <span data-ttu-id="7cadc-513">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-513">no</span></span>           |
| <span data-ttu-id="7cadc-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="7cadc-515">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-515">no</span></span>             | <span data-ttu-id="7cadc-516">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-516">no</span></span>           |
| <span data-ttu-id="7cadc-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="7cadc-518">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-518">no</span></span>             | <span data-ttu-id="7cadc-519">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-519">no</span></span>           |
| <span data-ttu-id="7cadc-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="7cadc-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="7cadc-521">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-521">no</span></span>             | <span data-ttu-id="7cadc-522">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-522">no</span></span>           |
| <span data-ttu-id="7cadc-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="7cadc-524">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-524">no</span></span>             | <span data-ttu-id="7cadc-525">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-525">no</span></span>           |
| <span data-ttu-id="7cadc-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="7cadc-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="7cadc-527">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-527">yes</span></span>            | <span data-ttu-id="7cadc-528">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-528">no</span></span>           |
| <span data-ttu-id="7cadc-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="7cadc-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="7cadc-530">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-530">yes</span></span>            | <span data-ttu-id="7cadc-531">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-531">no</span></span>           |
| <span data-ttu-id="7cadc-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="7cadc-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="7cadc-533">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-533">yes</span></span>            | <span data-ttu-id="7cadc-534">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-534">no</span></span>           |
| <span data-ttu-id="7cadc-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="7cadc-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="7cadc-536">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-536">no</span></span>             | <span data-ttu-id="7cadc-537">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-537">no</span></span>           |
| <span data-ttu-id="7cadc-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7cadc-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="7cadc-539">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-539">no</span></span>             | <span data-ttu-id="7cadc-540">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-540">no</span></span>           |
| <span data-ttu-id="7cadc-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="7cadc-542">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-542">no</span></span>             | <span data-ttu-id="7cadc-543">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-543">no</span></span>           |
| <span data-ttu-id="7cadc-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="7cadc-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="7cadc-545">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-545">no</span></span>             | <span data-ttu-id="7cadc-546">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-546">no</span></span>           |
| <span data-ttu-id="7cadc-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="7cadc-548">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-548">no</span></span>             | <span data-ttu-id="7cadc-549">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-549">no</span></span>           |
| <span data-ttu-id="7cadc-550">msdyn_varighed</span><span class="sxs-lookup"><span data-stu-id="7cadc-550">msdyn_duration</span></span>                         | <span data-ttu-id="7cadc-551">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-551">no</span></span>             | <span data-ttu-id="7cadc-552">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-552">no</span></span>           |
| <span data-ttu-id="7cadc-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7cadc-553">msdyn_effort</span></span>                           | <span data-ttu-id="7cadc-554">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-554">no</span></span>             | <span data-ttu-id="7cadc-555">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-555">no</span></span>           |
| <span data-ttu-id="7cadc-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7cadc-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="7cadc-557">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-557">no</span></span>             | <span data-ttu-id="7cadc-558">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-558">no</span></span>           |
| <span data-ttu-id="7cadc-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="7cadc-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="7cadc-560">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-560">no</span></span>             | <span data-ttu-id="7cadc-561">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-561">no</span></span>           |
| <span data-ttu-id="7cadc-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7cadc-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="7cadc-563">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-563">no</span></span>             | <span data-ttu-id="7cadc-564">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-564">no</span></span>           |
| <span data-ttu-id="7cadc-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7cadc-565">msdyn_finish</span></span>                           | <span data-ttu-id="7cadc-566">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-566">yes</span></span>            | <span data-ttu-id="7cadc-567">ja</span><span class="sxs-lookup"><span data-stu-id="7cadc-567">yes</span></span>          |
| <span data-ttu-id="7cadc-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="7cadc-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="7cadc-569">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-569">no</span></span>             | <span data-ttu-id="7cadc-570">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-570">no</span></span>           |
| <span data-ttu-id="7cadc-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="7cadc-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="7cadc-572">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-572">no</span></span>             | <span data-ttu-id="7cadc-573">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-573">no</span></span>           |
| <span data-ttu-id="7cadc-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="7cadc-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="7cadc-575">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-575">no</span></span>             | <span data-ttu-id="7cadc-576">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-576">no</span></span>           |
| <span data-ttu-id="7cadc-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="7cadc-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="7cadc-578">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-578">no</span></span>             | <span data-ttu-id="7cadc-579">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-579">no</span></span>           |
| <span data-ttu-id="7cadc-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="7cadc-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="7cadc-581">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-581">no</span></span>             | <span data-ttu-id="7cadc-582">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-582">no</span></span>           |
| <span data-ttu-id="7cadc-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="7cadc-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="7cadc-584">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-584">no</span></span>             | <span data-ttu-id="7cadc-585">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-585">no</span></span>           |
| <span data-ttu-id="7cadc-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="7cadc-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="7cadc-587">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-587">no</span></span>             | <span data-ttu-id="7cadc-588">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-588">no</span></span>           |
| <span data-ttu-id="7cadc-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="7cadc-590">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-590">no</span></span>             | <span data-ttu-id="7cadc-591">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-591">no</span></span>           |
| <span data-ttu-id="7cadc-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="7cadc-593">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-593">no</span></span>             | <span data-ttu-id="7cadc-594">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-594">no</span></span>           |
| <span data-ttu-id="7cadc-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="7cadc-596">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-596">no</span></span>             | <span data-ttu-id="7cadc-597">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-597">no</span></span>           |
| <span data-ttu-id="7cadc-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7cadc-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="7cadc-599">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-599">no</span></span>             | <span data-ttu-id="7cadc-600">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-600">no</span></span>           |
| <span data-ttu-id="7cadc-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="7cadc-602">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-602">no</span></span>             | <span data-ttu-id="7cadc-603">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-603">no</span></span>           |
| <span data-ttu-id="7cadc-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="7cadc-604">msdyn_progress</span></span>                         | <span data-ttu-id="7cadc-605">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-605">no</span></span>             | <span data-ttu-id="7cadc-606">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-606">no</span></span>           |
| <span data-ttu-id="7cadc-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="7cadc-608">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-608">no</span></span>             | <span data-ttu-id="7cadc-609">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-609">no</span></span>           |
| <span data-ttu-id="7cadc-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="7cadc-611">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-611">no</span></span>             | <span data-ttu-id="7cadc-612">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-612">no</span></span>           |
| <span data-ttu-id="7cadc-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7cadc-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="7cadc-614">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-614">no</span></span>             | <span data-ttu-id="7cadc-615">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-615">no</span></span>           |
| <span data-ttu-id="7cadc-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="7cadc-617">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-617">no</span></span>             | <span data-ttu-id="7cadc-618">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-618">no</span></span>           |
| <span data-ttu-id="7cadc-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="7cadc-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="7cadc-620">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-620">no</span></span>             | <span data-ttu-id="7cadc-621">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-621">no</span></span>           |
| <span data-ttu-id="7cadc-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="7cadc-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="7cadc-623">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-623">no</span></span>             | <span data-ttu-id="7cadc-624">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-624">no</span></span>           |
| <span data-ttu-id="7cadc-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="7cadc-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="7cadc-626">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-626">no</span></span>             | <span data-ttu-id="7cadc-627">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-627">no</span></span>           |
| <span data-ttu-id="7cadc-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="7cadc-629">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-629">no</span></span>             | <span data-ttu-id="7cadc-630">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-630">no</span></span>           |
| <span data-ttu-id="7cadc-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="7cadc-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="7cadc-632">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-632">no</span></span>             | <span data-ttu-id="7cadc-633">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-633">no</span></span>           |
| <span data-ttu-id="7cadc-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="7cadc-635">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-635">no</span></span>             | <span data-ttu-id="7cadc-636">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-636">no</span></span>           |
| <span data-ttu-id="7cadc-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="7cadc-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="7cadc-638">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-638">no</span></span>             | <span data-ttu-id="7cadc-639">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-639">no</span></span>           |
| <span data-ttu-id="7cadc-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="7cadc-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="7cadc-641">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-641">no</span></span>             | <span data-ttu-id="7cadc-642">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-642">no</span></span>           |
| <span data-ttu-id="7cadc-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="7cadc-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="7cadc-644">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-644">no</span></span>             | <span data-ttu-id="7cadc-645">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-645">no</span></span>           |
| <span data-ttu-id="7cadc-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="7cadc-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="7cadc-647">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-647">no</span></span>             | <span data-ttu-id="7cadc-648">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-648">no</span></span>           |
| <span data-ttu-id="7cadc-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="7cadc-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="7cadc-650">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-650">no</span></span>             | <span data-ttu-id="7cadc-651">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-651">no</span></span>           |
| <span data-ttu-id="7cadc-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="7cadc-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="7cadc-653">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-653">no</span></span>             | <span data-ttu-id="7cadc-654">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-654">no</span></span>           |
| <span data-ttu-id="7cadc-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="7cadc-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="7cadc-656">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-656">no</span></span>             | <span data-ttu-id="7cadc-657">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-657">no</span></span>           |
| <span data-ttu-id="7cadc-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="7cadc-659">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-659">no</span></span>             | <span data-ttu-id="7cadc-660">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-660">no</span></span>           |
| <span data-ttu-id="7cadc-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="7cadc-662">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-662">no</span></span>             | <span data-ttu-id="7cadc-663">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-663">no</span></span>           |
| <span data-ttu-id="7cadc-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="7cadc-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="7cadc-665">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-665">no</span></span>             | <span data-ttu-id="7cadc-666">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-666">no</span></span>           |
| <span data-ttu-id="7cadc-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7cadc-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="7cadc-668">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-668">no</span></span>             | <span data-ttu-id="7cadc-669">nej</span><span class="sxs-lookup"><span data-stu-id="7cadc-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="7cadc-670">Begrænsninger og kendte problemer</span><span class="sxs-lookup"><span data-stu-id="7cadc-670">Limitations and known issues</span></span>
<span data-ttu-id="7cadc-671">Her følger en liste over begrænsninger og kendte problemer:</span><span class="sxs-lookup"><span data-stu-id="7cadc-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="7cadc-672">Projektplanlægnings-Api'er kan kun bruges af **Brugere med Microsoft Project-licens**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="7cadc-673">De kan ikke bruges af:</span><span class="sxs-lookup"><span data-stu-id="7cadc-673">They can't be used by:</span></span>
    - <span data-ttu-id="7cadc-674">Programbrugere</span><span class="sxs-lookup"><span data-stu-id="7cadc-674">Application users</span></span>
    - <span data-ttu-id="7cadc-675">Systembrugere</span><span class="sxs-lookup"><span data-stu-id="7cadc-675">System users</span></span>
    - <span data-ttu-id="7cadc-676">Integrationsbrugere</span><span class="sxs-lookup"><span data-stu-id="7cadc-676">Integration users</span></span>
    - <span data-ttu-id="7cadc-677">Andre brugere, der ikke har den påkrævede licens</span><span class="sxs-lookup"><span data-stu-id="7cadc-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="7cadc-678">Hvert **OperationSet** kan kun have op til 100 handlinger.</span><span class="sxs-lookup"><span data-stu-id="7cadc-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="7cadc-679">Hver bruger kan kun have op til 10 åbne **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="7cadc-680">Project Operations understøtter i øjeblikket maksimalt 500 opgaver i alt på et projekt.</span><span class="sxs-lookup"><span data-stu-id="7cadc-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="7cadc-681">Status for fejl i **OperationSet** og fejllogfiler er ikke tilgængelige i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="7cadc-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="7cadc-682">Begrænsninger og grænser for projekter og opgaver</span><span class="sxs-lookup"><span data-stu-id="7cadc-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="7cadc-683">Fejlhåndtering</span><span class="sxs-lookup"><span data-stu-id="7cadc-683">Error handling</span></span>

   - <span data-ttu-id="7cadc-684">Hvis du vil gennemse de fejl, der er genereret i operationssæt, skal du gå til **Indstillinger** \> **Integration af planlægning** \> **Operationssæt**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="7cadc-685">Hvis du vil gennemse de fejl, der er genereret fra projektplanlægningstjenesten, skal du gå til **Indstillinger** \> **Planlægning af integration** \> **PSS-fejllogfiler**.</span><span class="sxs-lookup"><span data-stu-id="7cadc-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="7cadc-686">Eksempelscenarie</span><span class="sxs-lookup"><span data-stu-id="7cadc-686">Sample scenario</span></span>

<span data-ttu-id="7cadc-687">I dette scenario skal du oprette et projekt, et teammedlem, fire opgaver og to ressourcetildelinger.</span><span class="sxs-lookup"><span data-stu-id="7cadc-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="7cadc-688">Derefter skal du opdatere én opgave, opdatere projektet, slette én opgave, slette én ressourcetildeling og oprette en opgaveafhængighed.</span><span class="sxs-lookup"><span data-stu-id="7cadc-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="7cadc-689">Yderligere eksempler</span><span class="sxs-lookup"><span data-stu-id="7cadc-689">Additional samples</span></span>

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
