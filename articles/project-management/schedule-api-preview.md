---
title: Brug planlægnings-API'er til at udføre handlinger med planlægningsobjekter
description: Dette emne indeholder oplysninger om og eksempler på, hvordan du bruger planlægnings-API'er.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950797"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="6b4a4-103">Brug planlægnings-API'er til at udføre handlinger med planlægningsobjekter</span><span class="sxs-lookup"><span data-stu-id="6b4a4-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="6b4a4-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6b4a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="6b4a4-105">Visse eller alle de funktioner, der er omtalt i dette emne, er tilgængelige som en del af en forhåndsversion.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="6b4a4-106">Indholdet og funktionerne kan ændres.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="6b4a4-107">Planlægningsobjekter</span><span class="sxs-lookup"><span data-stu-id="6b4a4-107">Scheduling entities</span></span>

<span data-ttu-id="6b4a4-108">Med planlægnings-API'er kan du oprette, opdatere og slette handlinger med **Planlægningsobjekter**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="6b4a4-109">Disse objekter administreres via planlægningsprogrammet i Projekt til internettet.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="6b4a4-110">Handlinger til oprettelse, opdatering og sletning med **Planlægningsobjekter** var i tidligere udgivelser til Dynamics 365 Project Operations begrænset.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="6b4a4-111">I følgende tabel vises en fuldstændig liste over **Planlægningsobjekterne**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="6b4a4-112">Enhedsnavn</span><span class="sxs-lookup"><span data-stu-id="6b4a4-112">Entity name</span></span>  | <span data-ttu-id="6b4a4-113">Objektets logiske navn</span><span class="sxs-lookup"><span data-stu-id="6b4a4-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="6b4a4-114">Project</span><span class="sxs-lookup"><span data-stu-id="6b4a4-114">Project</span></span> | <span data-ttu-id="6b4a4-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="6b4a4-115">msdyn_project</span></span> |
| <span data-ttu-id="6b4a4-116">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="6b4a4-116">Project Task</span></span>  | <span data-ttu-id="6b4a4-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="6b4a4-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="6b4a4-118">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="6b4a4-118">Project Task Dependency</span></span>  | <span data-ttu-id="6b4a4-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="6b4a4-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="6b4a4-120">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="6b4a4-120">Resource Assignment</span></span> | <span data-ttu-id="6b4a4-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="6b4a4-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="6b4a4-122">Projektbucket</span><span class="sxs-lookup"><span data-stu-id="6b4a4-122">Project Bucket</span></span>  | <span data-ttu-id="6b4a4-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="6b4a4-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="6b4a4-124">Medlem af projektteam</span><span class="sxs-lookup"><span data-stu-id="6b4a4-124">Project Team Member</span></span> | <span data-ttu-id="6b4a4-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="6b4a4-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="6b4a4-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="6b4a4-126">OperationSet</span></span>

<span data-ttu-id="6b4a4-127">OperationSet er et arbejdsenhedsmønster, der kan bruges, når flere forespørgsler, der påvirker tidsplanen, skal behandles i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="6b4a4-128">Planlæg API'er</span><span class="sxs-lookup"><span data-stu-id="6b4a4-128">Schedule APIs</span></span>

<span data-ttu-id="6b4a4-129">Nedenfor vises en liste over aktuelle planlægnings-API'er.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="6b4a4-130">**msdyn_CreateProjectV1**: Denne API kan bruges til at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="6b4a4-131">Projekt- og standardprojektbucket oprettes med det samme.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="6b4a4-132">**msdyn_CreateTeamMemberV1**: Denne API kan bruges til at oprette et projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="6b4a4-133">Teammedlemsposten oprettes med det samme.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="6b4a4-134">**msdyn_CreateOperationSetV1**: Denne API kan bruges til at planlægge flere forespørgsler, der skal udføres i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="6b4a4-135">**msdyn_PSSCreateV1**: Denne API kan bruges til at oprette et objekt.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="6b4a4-136">Objektet kan være et af de planlægningsobjekter, der understøtter oprettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="6b4a4-137">**msdyn_PSSUpdateV1**: Denne API kan bruges til at opdatere et objekt.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="6b4a4-138">Objektet kan være et af de planlægningsobjekter, der understøtter opdateringshandlingen.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="6b4a4-139">**msdyn_PSSDeleteV1**: Denne API kan bruges til at slette et objekt.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="6b4a4-140">Objektet kan være et af de planlægningsobjekter, der understøtter slettehandlingen.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="6b4a4-141">**msdyn_ExecuteOperationSetV1**: Denne API bruges til at udføre alle handlinger i det givne operationssæt.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="6b4a4-142">Brug planlægnings-API'er med OperationSet</span><span class="sxs-lookup"><span data-stu-id="6b4a4-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="6b4a4-143">Da poster med både **CreateProjectV1** og **CreateTeamMemberV1** oprettes med det samme, kan disse API'er ikke bruges direkte i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="6b4a4-144">Du kan dog bruge API'en til at oprette de krævede poster, et **OperationSet** og derefter bruge disse forudoprettede poster i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="6b4a4-145">Understøttede handlinger</span><span class="sxs-lookup"><span data-stu-id="6b4a4-145">Supported operations</span></span>

| <span data-ttu-id="6b4a4-146">Planlægningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6b4a4-146">Scheduling entity</span></span> | <span data-ttu-id="6b4a4-147">Opret</span><span class="sxs-lookup"><span data-stu-id="6b4a4-147">Create</span></span> | <span data-ttu-id="6b4a4-148">Opdatering</span><span class="sxs-lookup"><span data-stu-id="6b4a4-148">Update</span></span> | <span data-ttu-id="6b4a4-149">Delete</span><span class="sxs-lookup"><span data-stu-id="6b4a4-149">Delete</span></span> | <span data-ttu-id="6b4a4-150">Vigtige overvejelser</span><span class="sxs-lookup"><span data-stu-id="6b4a4-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="6b4a4-151">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="6b4a4-151">Project task</span></span> | <span data-ttu-id="6b4a4-152">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-152">Yes</span></span> | <span data-ttu-id="6b4a4-153">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-153">Yes</span></span> | <span data-ttu-id="6b4a4-154">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-154">Yes</span></span> | <span data-ttu-id="6b4a4-155">Intet</span><span class="sxs-lookup"><span data-stu-id="6b4a4-155">None</span></span> |
| <span data-ttu-id="6b4a4-156">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="6b4a4-156">Project task dependency</span></span> | <span data-ttu-id="6b4a4-157">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-157">Yes</span></span> | <span data-ttu-id="6b4a4-158">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-158">Yes</span></span> | | <span data-ttu-id="6b4a4-159">Projektopgaveafhængighedsposter opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="6b4a4-160">I stedet kan en gammel post slettes, og der kan oprettes en ny post.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="6b4a4-161">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="6b4a4-161">Resource assignment</span></span> | <span data-ttu-id="6b4a4-162">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-162">Yes</span></span> | <span data-ttu-id="6b4a4-163">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-163">Yes</span></span> | | <span data-ttu-id="6b4a4-164">Handlinger med følgende felter understøttes ikke: **BookableResourceID**, **Indsats**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="6b4a4-165">Ressourcetildelingsposter opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="6b4a4-166">I stedet kan den gamle post slettes, og der kan oprettes en ny post.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="6b4a4-167">Projektbucket</span><span class="sxs-lookup"><span data-stu-id="6b4a4-167">Project bucket</span></span> | <span data-ttu-id="6b4a4-168">I/R</span><span class="sxs-lookup"><span data-stu-id="6b4a4-168">N/A</span></span> | <span data-ttu-id="6b4a4-169">I/R</span><span class="sxs-lookup"><span data-stu-id="6b4a4-169">N/A</span></span> | <span data-ttu-id="6b4a4-170">I/R</span><span class="sxs-lookup"><span data-stu-id="6b4a4-170">N/A</span></span> | <span data-ttu-id="6b4a4-171">Standardbucket oprettes ved hjælp af API'en **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="6b4a4-172">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="6b4a4-172">Project team member</span></span> | <span data-ttu-id="6b4a4-173">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-173">Yes</span></span> | <span data-ttu-id="6b4a4-174">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-174">Yes</span></span> | <span data-ttu-id="6b4a4-175">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-175">Yes</span></span> | <span data-ttu-id="6b4a4-176">Brug API'en **CreateTeamMemberV1** til oprettelseshandlingen.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="6b4a4-177">Project</span><span class="sxs-lookup"><span data-stu-id="6b4a4-177">Project</span></span> | <span data-ttu-id="6b4a4-178">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-178">Yes</span></span> | <span data-ttu-id="6b4a4-179">Ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-179">Yes</span></span> | <span data-ttu-id="6b4a4-180">I/R</span><span class="sxs-lookup"><span data-stu-id="6b4a4-180">N/A</span></span> | <span data-ttu-id="6b4a4-181">Handlinger med følgende felter understøttes ikke: **StateCode**, **BulkStatus**, **GlobalRevisionToken**, **CalendarID**, **Indsats**, **EffortCompleted**, **EffortRemaining**, **Status**, **Afsluttet**, **TaskEarliestStart** og **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="6b4a4-182">Disse API'er kan kaldes sammen med enhedsobjekter, der indeholder brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="6b4a4-183">Id-egenskaben er valgfri.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-183">The ID property is optional.</span></span> <span data-ttu-id="6b4a4-184">Hvis den oplyses, forsøger systemet at bruge den, og der udløses en undtagelse, hvis den ikke kan bruges.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="6b4a4-185">Hvis den ikke er angivet, oprettes den af systemet.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="6b4a4-186">Begrænsede felter</span><span class="sxs-lookup"><span data-stu-id="6b4a4-186">Restricted fields</span></span>

<span data-ttu-id="6b4a4-187">I følgende tabeller defineres de felter, der er begrænset fra **Opret** og **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="6b4a4-188">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="6b4a4-188">Project task</span></span>

| <span data-ttu-id="6b4a4-189">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-189">**Logical name**</span></span>                       | <span data-ttu-id="6b4a4-190">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-190">**Can create**</span></span> | <span data-ttu-id="6b4a4-191">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="6b4a4-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="6b4a4-193">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-193">no</span></span>             | <span data-ttu-id="6b4a4-194">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-194">no</span></span>               |
| <span data-ttu-id="6b4a4-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="6b4a4-196">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-196">no</span></span>             | <span data-ttu-id="6b4a4-197">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-197">no</span></span>               |
| <span data-ttu-id="6b4a4-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="6b4a4-198">msdyn_actualend</span></span>                        | <span data-ttu-id="6b4a4-199">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-199">no</span></span>             | <span data-ttu-id="6b4a4-200">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-200">no</span></span>               |
| <span data-ttu-id="6b4a4-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="6b4a4-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="6b4a4-202">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-202">no</span></span>             | <span data-ttu-id="6b4a4-203">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-203">no</span></span>               |
| <span data-ttu-id="6b4a4-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="6b4a4-205">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-205">no</span></span>             | <span data-ttu-id="6b4a4-206">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-206">no</span></span>               |
| <span data-ttu-id="6b4a4-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="6b4a4-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="6b4a4-208">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-208">no</span></span>             | <span data-ttu-id="6b4a4-209">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-209">no</span></span>               |
| <span data-ttu-id="6b4a4-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="6b4a4-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="6b4a4-211">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-211">no</span></span>             | <span data-ttu-id="6b4a4-212">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-212">no</span></span>               |
| <span data-ttu-id="6b4a4-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="6b4a4-214">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-214">no</span></span>             | <span data-ttu-id="6b4a4-215">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-215">no</span></span>               |
| <span data-ttu-id="6b4a4-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="6b4a4-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="6b4a4-217">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-217">no</span></span>             | <span data-ttu-id="6b4a4-218">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-218">no</span></span>               |
| <span data-ttu-id="6b4a4-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6b4a4-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="6b4a4-220">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-220">no</span></span>             | <span data-ttu-id="6b4a4-221">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-221">no</span></span>               |
| <span data-ttu-id="6b4a4-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="6b4a4-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="6b4a4-223">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-223">no</span></span>             | <span data-ttu-id="6b4a4-224">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-224">no</span></span>               |
| <span data-ttu-id="6b4a4-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="6b4a4-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="6b4a4-226">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-226">no</span></span>             | <span data-ttu-id="6b4a4-227">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-227">no</span></span>               |
| <span data-ttu-id="6b4a4-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="6b4a4-229">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-229">no</span></span>             | <span data-ttu-id="6b4a4-230">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-230">no</span></span>               |
| <span data-ttu-id="6b4a4-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="6b4a4-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="6b4a4-232">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-232">no</span></span>             | <span data-ttu-id="6b4a4-233">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-233">no</span></span>               |
| <span data-ttu-id="6b4a4-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="6b4a4-235">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-235">no</span></span>             | <span data-ttu-id="6b4a4-236">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-236">no</span></span>               |
| <span data-ttu-id="6b4a4-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="6b4a4-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="6b4a4-238">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-238">no</span></span>             | <span data-ttu-id="6b4a4-239">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-239">no</span></span>               |
| <span data-ttu-id="6b4a4-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="6b4a4-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="6b4a4-241">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-241">no</span></span>             | <span data-ttu-id="6b4a4-242">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-242">no</span></span>               |
| <span data-ttu-id="6b4a4-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="6b4a4-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="6b4a4-244">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-244">no</span></span>             | <span data-ttu-id="6b4a4-245">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-245">no</span></span>               |
| <span data-ttu-id="6b4a4-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="6b4a4-247">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-247">no</span></span>             | <span data-ttu-id="6b4a4-248">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-248">no</span></span>               |
| <span data-ttu-id="6b4a4-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="6b4a4-250">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-250">no</span></span>             | <span data-ttu-id="6b4a4-251">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-251">no</span></span>               |
| <span data-ttu-id="6b4a4-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="6b4a4-253">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-253">no</span></span>             | <span data-ttu-id="6b4a4-254">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-254">no</span></span>               |
| <span data-ttu-id="6b4a4-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="6b4a4-256">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-256">no</span></span>             | <span data-ttu-id="6b4a4-257">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-257">no</span></span>               |
| <span data-ttu-id="6b4a4-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6b4a4-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="6b4a4-259">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-259">no</span></span>             | <span data-ttu-id="6b4a4-260">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-260">no</span></span>               |
| <span data-ttu-id="6b4a4-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="6b4a4-262">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-262">no</span></span>             | <span data-ttu-id="6b4a4-263">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-263">no</span></span>               |
| <span data-ttu-id="6b4a4-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="6b4a4-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="6b4a4-265">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-265">no</span></span>             | <span data-ttu-id="6b4a4-266">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-266">no</span></span>               |
| <span data-ttu-id="6b4a4-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="6b4a4-267">msdyn_progress</span></span>                         | <span data-ttu-id="6b4a4-268">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-268">no</span></span>             | <span data-ttu-id="6b4a4-269">nej (ja for P4W)</span><span class="sxs-lookup"><span data-stu-id="6b4a4-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="6b4a4-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="6b4a4-271">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-271">no</span></span>             | <span data-ttu-id="6b4a4-272">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-272">no</span></span>               |
| <span data-ttu-id="6b4a4-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="6b4a4-274">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-274">no</span></span>             | <span data-ttu-id="6b4a4-275">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-275">no</span></span>               |
| <span data-ttu-id="6b4a4-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="6b4a4-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="6b4a4-277">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-277">no</span></span>             | <span data-ttu-id="6b4a4-278">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-278">no</span></span>               |
| <span data-ttu-id="6b4a4-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="6b4a4-280">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-280">no</span></span>             | <span data-ttu-id="6b4a4-281">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-281">no</span></span>               |
| <span data-ttu-id="6b4a4-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="6b4a4-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="6b4a4-283">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-283">no</span></span>             | <span data-ttu-id="6b4a4-284">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-284">no</span></span>               |
| <span data-ttu-id="6b4a4-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="6b4a4-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="6b4a4-286">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-286">no</span></span>             | <span data-ttu-id="6b4a4-287">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-287">no</span></span>               |
| <span data-ttu-id="6b4a4-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="6b4a4-289">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-289">no</span></span>             | <span data-ttu-id="6b4a4-290">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-290">no</span></span>               |
| <span data-ttu-id="6b4a4-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="6b4a4-292">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-292">no</span></span>             | <span data-ttu-id="6b4a4-293">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-293">no</span></span>               |
| <span data-ttu-id="6b4a4-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="6b4a4-295">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-295">no</span></span>             | <span data-ttu-id="6b4a4-296">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-296">no</span></span>               |
| <span data-ttu-id="6b4a4-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="6b4a4-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="6b4a4-298">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-298">no</span></span>             | <span data-ttu-id="6b4a4-299">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-299">no</span></span>               |
| <span data-ttu-id="6b4a4-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="6b4a4-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="6b4a4-301">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-301">no</span></span>             | <span data-ttu-id="6b4a4-302">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-302">no</span></span>               |
| <span data-ttu-id="6b4a4-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="6b4a4-304">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-304">no</span></span>             | <span data-ttu-id="6b4a4-305">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-305">no</span></span>               |
| <span data-ttu-id="6b4a4-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="6b4a4-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="6b4a4-307">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-307">no</span></span>             | <span data-ttu-id="6b4a4-308">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-308">no</span></span>               |
| <span data-ttu-id="6b4a4-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="6b4a4-310">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-310">no</span></span>             | <span data-ttu-id="6b4a4-311">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-311">no</span></span>               |
| <span data-ttu-id="6b4a4-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="6b4a4-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="6b4a4-313">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-313">no</span></span>             | <span data-ttu-id="6b4a4-314">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-314">no</span></span>               |
| <span data-ttu-id="6b4a4-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="6b4a4-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="6b4a4-316">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-316">no</span></span>             | <span data-ttu-id="6b4a4-317">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-317">no</span></span>               |
| <span data-ttu-id="6b4a4-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="6b4a4-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="6b4a4-319">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-319">no</span></span>             | <span data-ttu-id="6b4a4-320">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-320">no</span></span>               |
| <span data-ttu-id="6b4a4-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="6b4a4-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="6b4a4-322">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-322">no</span></span>             | <span data-ttu-id="6b4a4-323">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-323">no</span></span>               |
| <span data-ttu-id="6b4a4-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="6b4a4-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="6b4a4-325">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-325">no</span></span>             | <span data-ttu-id="6b4a4-326">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-326">no</span></span>               |
| <span data-ttu-id="6b4a4-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="6b4a4-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="6b4a4-328">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-328">no</span></span>             | <span data-ttu-id="6b4a4-329">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-329">no</span></span>               |
| <span data-ttu-id="6b4a4-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="6b4a4-330">msdyn_summary</span></span>                          | <span data-ttu-id="6b4a4-331">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-331">no</span></span>             | <span data-ttu-id="6b4a4-332">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-332">no</span></span>               |
| <span data-ttu-id="6b4a4-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="6b4a4-334">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-334">no</span></span>             | <span data-ttu-id="6b4a4-335">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-335">no</span></span>               |
| <span data-ttu-id="6b4a4-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="6b4a4-337">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-337">no</span></span>             | <span data-ttu-id="6b4a4-338">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="6b4a4-339">Projektopgaveafhængighed</span><span class="sxs-lookup"><span data-stu-id="6b4a4-339">Project task dependency</span></span>

| <span data-ttu-id="6b4a4-340">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-340">**Logical name**</span></span>              | <span data-ttu-id="6b4a4-341">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-341">**Can create**</span></span> | <span data-ttu-id="6b4a4-342">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="6b4a4-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="6b4a4-343">msdyn_linktype</span></span>                | <span data-ttu-id="6b4a4-344">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-344">no</span></span>             | <span data-ttu-id="6b4a4-345">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-345">no</span></span>           |
| <span data-ttu-id="6b4a4-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="6b4a4-346">msdyn_linktypename</span></span>            | <span data-ttu-id="6b4a4-347">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-347">no</span></span>             | <span data-ttu-id="6b4a4-348">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-348">no</span></span>           |
| <span data-ttu-id="6b4a4-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="6b4a4-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="6b4a4-350">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-350">yes</span></span>            | <span data-ttu-id="6b4a4-351">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-351">no</span></span>           |
| <span data-ttu-id="6b4a4-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="6b4a4-353">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-353">yes</span></span>            | <span data-ttu-id="6b4a4-354">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-354">no</span></span>           |
| <span data-ttu-id="6b4a4-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="6b4a4-355">msdyn_project</span></span>                 | <span data-ttu-id="6b4a4-356">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-356">yes</span></span>            | <span data-ttu-id="6b4a4-357">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-357">no</span></span>           |
| <span data-ttu-id="6b4a4-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-358">msdyn_projectname</span></span>             | <span data-ttu-id="6b4a4-359">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-359">yes</span></span>            | <span data-ttu-id="6b4a4-360">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-360">no</span></span>           |
| <span data-ttu-id="6b4a4-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="6b4a4-362">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-362">yes</span></span>            | <span data-ttu-id="6b4a4-363">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-363">no</span></span>           |
| <span data-ttu-id="6b4a4-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="6b4a4-364">msdyn_successortask</span></span>           | <span data-ttu-id="6b4a4-365">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-365">yes</span></span>            | <span data-ttu-id="6b4a4-366">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-366">no</span></span>           |
| <span data-ttu-id="6b4a4-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="6b4a4-368">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-368">yes</span></span>            | <span data-ttu-id="6b4a4-369">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="6b4a4-370">Ressourcetildeling</span><span class="sxs-lookup"><span data-stu-id="6b4a4-370">Resource assignment</span></span>

| <span data-ttu-id="6b4a4-371">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-371">**Logical name**</span></span>             | <span data-ttu-id="6b4a4-372">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-372">**Can create**</span></span> | <span data-ttu-id="6b4a4-373">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="6b4a4-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="6b4a4-375">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-375">yes</span></span>            | <span data-ttu-id="6b4a4-376">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-376">no</span></span>           |
| <span data-ttu-id="6b4a4-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="6b4a4-378">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-378">yes</span></span>            | <span data-ttu-id="6b4a4-379">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-379">no</span></span>           |
| <span data-ttu-id="6b4a4-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="6b4a4-381">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-381">no</span></span>             | <span data-ttu-id="6b4a4-382">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-382">no</span></span>           |
| <span data-ttu-id="6b4a4-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="6b4a4-384">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-384">no</span></span>             | <span data-ttu-id="6b4a4-385">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-385">no</span></span>           |
| <span data-ttu-id="6b4a4-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="6b4a4-386">msdyn_committype</span></span>             | <span data-ttu-id="6b4a4-387">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-387">no</span></span>             | <span data-ttu-id="6b4a4-388">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-388">no</span></span>           |
| <span data-ttu-id="6b4a4-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="6b4a4-389">msdyn_committypename</span></span>         | <span data-ttu-id="6b4a4-390">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-390">no</span></span>             | <span data-ttu-id="6b4a4-391">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-391">no</span></span>           |
| <span data-ttu-id="6b4a4-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6b4a4-392">msdyn_effort</span></span>                 | <span data-ttu-id="6b4a4-393">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-393">no</span></span>             | <span data-ttu-id="6b4a4-394">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-394">no</span></span>           |
| <span data-ttu-id="6b4a4-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6b4a4-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="6b4a4-396">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-396">no</span></span>             | <span data-ttu-id="6b4a4-397">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-397">no</span></span>           |
| <span data-ttu-id="6b4a4-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6b4a4-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="6b4a4-399">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-399">no</span></span>             | <span data-ttu-id="6b4a4-400">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-400">no</span></span>           |
| <span data-ttu-id="6b4a4-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6b4a4-401">msdyn_finish</span></span>                 | <span data-ttu-id="6b4a4-402">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-402">no</span></span>             | <span data-ttu-id="6b4a4-403">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-403">no</span></span>           |
| <span data-ttu-id="6b4a4-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="6b4a4-405">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-405">no</span></span>             | <span data-ttu-id="6b4a4-406">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-406">no</span></span>           |
| <span data-ttu-id="6b4a4-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="6b4a4-408">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-408">no</span></span>             | <span data-ttu-id="6b4a4-409">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-409">no</span></span>           |
| <span data-ttu-id="6b4a4-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="6b4a4-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="6b4a4-411">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-411">no</span></span>             | <span data-ttu-id="6b4a4-412">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-412">no</span></span>           |
| <span data-ttu-id="6b4a4-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6b4a4-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="6b4a4-414">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-414">no</span></span>             | <span data-ttu-id="6b4a4-415">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-415">no</span></span>           |
| <span data-ttu-id="6b4a4-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="6b4a4-417">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-417">no</span></span>             | <span data-ttu-id="6b4a4-418">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-418">no</span></span>           |
| <span data-ttu-id="6b4a4-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="6b4a4-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="6b4a4-420">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-420">no</span></span>             | <span data-ttu-id="6b4a4-421">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-421">no</span></span>           |
| <span data-ttu-id="6b4a4-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="6b4a4-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="6b4a4-423">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-423">no</span></span>             | <span data-ttu-id="6b4a4-424">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-424">no</span></span>           |
| <span data-ttu-id="6b4a4-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-425">msdyn_projectid</span></span>              | <span data-ttu-id="6b4a4-426">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-426">yes</span></span>            | <span data-ttu-id="6b4a4-427">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-427">no</span></span>           |
| <span data-ttu-id="6b4a4-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-428">msdyn_projectidname</span></span>          | <span data-ttu-id="6b4a4-429">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-429">no</span></span>             | <span data-ttu-id="6b4a4-430">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-430">no</span></span>           |
| <span data-ttu-id="6b4a4-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="6b4a4-432">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-432">no</span></span>             | <span data-ttu-id="6b4a4-433">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-433">no</span></span>           |
| <span data-ttu-id="6b4a4-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="6b4a4-435">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-435">no</span></span>             | <span data-ttu-id="6b4a4-436">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-436">no</span></span>           |
| <span data-ttu-id="6b4a4-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="6b4a4-437">msdyn_start</span></span>                  | <span data-ttu-id="6b4a4-438">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-438">no</span></span>             | <span data-ttu-id="6b4a4-439">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-439">no</span></span>           |
| <span data-ttu-id="6b4a4-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-440">msdyn_taskid</span></span>                 | <span data-ttu-id="6b4a4-441">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-441">no</span></span>             | <span data-ttu-id="6b4a4-442">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-442">no</span></span>           |
| <span data-ttu-id="6b4a4-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-443">msdyn_taskidname</span></span>             | <span data-ttu-id="6b4a4-444">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-444">no</span></span>             | <span data-ttu-id="6b4a4-445">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-445">no</span></span>           |
| <span data-ttu-id="6b4a4-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="6b4a4-447">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-447">no</span></span>             | <span data-ttu-id="6b4a4-448">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="6b4a4-449">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="6b4a4-449">Project team member</span></span>

| <span data-ttu-id="6b4a4-450">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-450">**Logical name**</span></span>                                 | <span data-ttu-id="6b4a4-451">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-451">**Can create**</span></span> | <span data-ttu-id="6b4a4-452">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="6b4a4-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="6b4a4-454">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-454">no</span></span>             | <span data-ttu-id="6b4a4-455">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-455">no</span></span>           |
| <span data-ttu-id="6b4a4-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="6b4a4-457">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-457">no</span></span>             | <span data-ttu-id="6b4a4-458">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-458">no</span></span>           |
| <span data-ttu-id="6b4a4-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="6b4a4-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="6b4a4-460">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-460">no</span></span>             | <span data-ttu-id="6b4a4-461">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-461">no</span></span>           |
| <span data-ttu-id="6b4a4-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="6b4a4-463">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-463">no</span></span>             | <span data-ttu-id="6b4a4-464">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-464">no</span></span>           |
| <span data-ttu-id="6b4a4-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6b4a4-465">msdyn_effort</span></span>                                     | <span data-ttu-id="6b4a4-466">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-466">no</span></span>             | <span data-ttu-id="6b4a4-467">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-467">no</span></span>           |
| <span data-ttu-id="6b4a4-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6b4a4-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="6b4a4-469">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-469">no</span></span>             | <span data-ttu-id="6b4a4-470">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-470">no</span></span>           |
| <span data-ttu-id="6b4a4-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6b4a4-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="6b4a4-472">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-472">no</span></span>             | <span data-ttu-id="6b4a4-473">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-473">no</span></span>           |
| <span data-ttu-id="6b4a4-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6b4a4-474">msdyn_finish</span></span>                                     | <span data-ttu-id="6b4a4-475">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-475">no</span></span>             | <span data-ttu-id="6b4a4-476">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-476">no</span></span>           |
| <span data-ttu-id="6b4a4-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="6b4a4-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="6b4a4-478">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-478">no</span></span>             | <span data-ttu-id="6b4a4-479">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-479">no</span></span>           |
| <span data-ttu-id="6b4a4-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="6b4a4-480">msdyn_hours</span></span>                                      | <span data-ttu-id="6b4a4-481">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-481">no</span></span>             | <span data-ttu-id="6b4a4-482">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-482">no</span></span>           |
| <span data-ttu-id="6b4a4-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="6b4a4-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="6b4a4-484">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-484">no</span></span>             | <span data-ttu-id="6b4a4-485">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-485">no</span></span>           |
| <span data-ttu-id="6b4a4-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="6b4a4-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="6b4a4-487">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-487">no</span></span>             | <span data-ttu-id="6b4a4-488">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-488">no</span></span>           |
| <span data-ttu-id="6b4a4-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="6b4a4-490">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-490">no</span></span>             | <span data-ttu-id="6b4a4-491">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-491">no</span></span>           |
| <span data-ttu-id="6b4a4-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="6b4a4-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="6b4a4-493">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-493">no</span></span>             | <span data-ttu-id="6b4a4-494">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-494">no</span></span>           |
| <span data-ttu-id="6b4a4-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="6b4a4-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="6b4a4-496">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-496">no</span></span>             | <span data-ttu-id="6b4a4-497">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-497">no</span></span>           |
| <span data-ttu-id="6b4a4-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="6b4a4-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="6b4a4-499">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-499">no</span></span>             | <span data-ttu-id="6b4a4-500">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-500">no</span></span>           |
| <span data-ttu-id="6b4a4-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="6b4a4-501">msdyn_start</span></span>                                      | <span data-ttu-id="6b4a4-502">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-502">no</span></span>             | <span data-ttu-id="6b4a4-503">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="6b4a4-504">Project</span><span class="sxs-lookup"><span data-stu-id="6b4a4-504">Project</span></span>

| <span data-ttu-id="6b4a4-505">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-505">**Logical name**</span></span>                       | <span data-ttu-id="6b4a4-506">**Kan oprette**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-506">**Can create**</span></span> | <span data-ttu-id="6b4a4-507">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="6b4a4-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="6b4a4-509">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-509">no</span></span>             | <span data-ttu-id="6b4a4-510">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-510">no</span></span>           |
| <span data-ttu-id="6b4a4-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="6b4a4-512">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-512">no</span></span>             | <span data-ttu-id="6b4a4-513">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-513">no</span></span>           |
| <span data-ttu-id="6b4a4-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="6b4a4-515">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-515">no</span></span>             | <span data-ttu-id="6b4a4-516">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-516">no</span></span>           |
| <span data-ttu-id="6b4a4-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="6b4a4-518">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-518">no</span></span>             | <span data-ttu-id="6b4a4-519">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-519">no</span></span>           |
| <span data-ttu-id="6b4a4-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="6b4a4-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="6b4a4-521">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-521">no</span></span>             | <span data-ttu-id="6b4a4-522">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-522">no</span></span>           |
| <span data-ttu-id="6b4a4-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="6b4a4-524">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-524">no</span></span>             | <span data-ttu-id="6b4a4-525">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-525">no</span></span>           |
| <span data-ttu-id="6b4a4-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="6b4a4-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="6b4a4-527">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-527">yes</span></span>            | <span data-ttu-id="6b4a4-528">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-528">no</span></span>           |
| <span data-ttu-id="6b4a4-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="6b4a4-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="6b4a4-530">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-530">yes</span></span>            | <span data-ttu-id="6b4a4-531">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-531">no</span></span>           |
| <span data-ttu-id="6b4a4-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="6b4a4-533">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-533">yes</span></span>            | <span data-ttu-id="6b4a4-534">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-534">no</span></span>           |
| <span data-ttu-id="6b4a4-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="6b4a4-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="6b4a4-536">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-536">no</span></span>             | <span data-ttu-id="6b4a4-537">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-537">no</span></span>           |
| <span data-ttu-id="6b4a4-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="6b4a4-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="6b4a4-539">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-539">no</span></span>             | <span data-ttu-id="6b4a4-540">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-540">no</span></span>           |
| <span data-ttu-id="6b4a4-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="6b4a4-542">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-542">no</span></span>             | <span data-ttu-id="6b4a4-543">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-543">no</span></span>           |
| <span data-ttu-id="6b4a4-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="6b4a4-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="6b4a4-545">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-545">no</span></span>             | <span data-ttu-id="6b4a4-546">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-546">no</span></span>           |
| <span data-ttu-id="6b4a4-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="6b4a4-548">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-548">no</span></span>             | <span data-ttu-id="6b4a4-549">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-549">no</span></span>           |
| <span data-ttu-id="6b4a4-550">msdyn_varighed</span><span class="sxs-lookup"><span data-stu-id="6b4a4-550">msdyn_duration</span></span>                         | <span data-ttu-id="6b4a4-551">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-551">no</span></span>             | <span data-ttu-id="6b4a4-552">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-552">no</span></span>           |
| <span data-ttu-id="6b4a4-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6b4a4-553">msdyn_effort</span></span>                           | <span data-ttu-id="6b4a4-554">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-554">no</span></span>             | <span data-ttu-id="6b4a4-555">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-555">no</span></span>           |
| <span data-ttu-id="6b4a4-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6b4a4-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="6b4a4-557">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-557">no</span></span>             | <span data-ttu-id="6b4a4-558">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-558">no</span></span>           |
| <span data-ttu-id="6b4a4-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="6b4a4-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="6b4a4-560">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-560">no</span></span>             | <span data-ttu-id="6b4a4-561">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-561">no</span></span>           |
| <span data-ttu-id="6b4a4-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6b4a4-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="6b4a4-563">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-563">no</span></span>             | <span data-ttu-id="6b4a4-564">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-564">no</span></span>           |
| <span data-ttu-id="6b4a4-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6b4a4-565">msdyn_finish</span></span>                           | <span data-ttu-id="6b4a4-566">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-566">yes</span></span>            | <span data-ttu-id="6b4a4-567">ja</span><span class="sxs-lookup"><span data-stu-id="6b4a4-567">yes</span></span>          |
| <span data-ttu-id="6b4a4-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="6b4a4-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="6b4a4-569">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-569">no</span></span>             | <span data-ttu-id="6b4a4-570">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-570">no</span></span>           |
| <span data-ttu-id="6b4a4-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="6b4a4-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="6b4a4-572">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-572">no</span></span>             | <span data-ttu-id="6b4a4-573">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-573">no</span></span>           |
| <span data-ttu-id="6b4a4-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="6b4a4-575">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-575">no</span></span>             | <span data-ttu-id="6b4a4-576">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-576">no</span></span>           |
| <span data-ttu-id="6b4a4-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="6b4a4-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="6b4a4-578">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-578">no</span></span>             | <span data-ttu-id="6b4a4-579">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-579">no</span></span>           |
| <span data-ttu-id="6b4a4-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="6b4a4-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="6b4a4-581">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-581">no</span></span>             | <span data-ttu-id="6b4a4-582">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-582">no</span></span>           |
| <span data-ttu-id="6b4a4-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="6b4a4-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="6b4a4-584">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-584">no</span></span>             | <span data-ttu-id="6b4a4-585">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-585">no</span></span>           |
| <span data-ttu-id="6b4a4-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="6b4a4-587">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-587">no</span></span>             | <span data-ttu-id="6b4a4-588">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-588">no</span></span>           |
| <span data-ttu-id="6b4a4-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="6b4a4-590">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-590">no</span></span>             | <span data-ttu-id="6b4a4-591">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-591">no</span></span>           |
| <span data-ttu-id="6b4a4-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="6b4a4-593">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-593">no</span></span>             | <span data-ttu-id="6b4a4-594">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-594">no</span></span>           |
| <span data-ttu-id="6b4a4-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="6b4a4-596">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-596">no</span></span>             | <span data-ttu-id="6b4a4-597">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-597">no</span></span>           |
| <span data-ttu-id="6b4a4-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6b4a4-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="6b4a4-599">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-599">no</span></span>             | <span data-ttu-id="6b4a4-600">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-600">no</span></span>           |
| <span data-ttu-id="6b4a4-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="6b4a4-602">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-602">no</span></span>             | <span data-ttu-id="6b4a4-603">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-603">no</span></span>           |
| <span data-ttu-id="6b4a4-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="6b4a4-604">msdyn_progress</span></span>                         | <span data-ttu-id="6b4a4-605">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-605">no</span></span>             | <span data-ttu-id="6b4a4-606">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-606">no</span></span>           |
| <span data-ttu-id="6b4a4-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="6b4a4-608">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-608">no</span></span>             | <span data-ttu-id="6b4a4-609">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-609">no</span></span>           |
| <span data-ttu-id="6b4a4-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="6b4a4-611">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-611">no</span></span>             | <span data-ttu-id="6b4a4-612">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-612">no</span></span>           |
| <span data-ttu-id="6b4a4-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="6b4a4-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="6b4a4-614">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-614">no</span></span>             | <span data-ttu-id="6b4a4-615">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-615">no</span></span>           |
| <span data-ttu-id="6b4a4-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="6b4a4-617">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-617">no</span></span>             | <span data-ttu-id="6b4a4-618">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-618">no</span></span>           |
| <span data-ttu-id="6b4a4-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="6b4a4-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="6b4a4-620">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-620">no</span></span>             | <span data-ttu-id="6b4a4-621">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-621">no</span></span>           |
| <span data-ttu-id="6b4a4-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="6b4a4-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="6b4a4-623">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-623">no</span></span>             | <span data-ttu-id="6b4a4-624">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-624">no</span></span>           |
| <span data-ttu-id="6b4a4-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="6b4a4-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="6b4a4-626">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-626">no</span></span>             | <span data-ttu-id="6b4a4-627">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-627">no</span></span>           |
| <span data-ttu-id="6b4a4-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="6b4a4-629">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-629">no</span></span>             | <span data-ttu-id="6b4a4-630">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-630">no</span></span>           |
| <span data-ttu-id="6b4a4-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="6b4a4-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="6b4a4-632">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-632">no</span></span>             | <span data-ttu-id="6b4a4-633">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-633">no</span></span>           |
| <span data-ttu-id="6b4a4-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="6b4a4-635">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-635">no</span></span>             | <span data-ttu-id="6b4a4-636">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-636">no</span></span>           |
| <span data-ttu-id="6b4a4-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="6b4a4-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="6b4a4-638">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-638">no</span></span>             | <span data-ttu-id="6b4a4-639">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-639">no</span></span>           |
| <span data-ttu-id="6b4a4-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="6b4a4-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="6b4a4-641">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-641">no</span></span>             | <span data-ttu-id="6b4a4-642">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-642">no</span></span>           |
| <span data-ttu-id="6b4a4-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="6b4a4-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="6b4a4-644">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-644">no</span></span>             | <span data-ttu-id="6b4a4-645">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-645">no</span></span>           |
| <span data-ttu-id="6b4a4-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="6b4a4-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="6b4a4-647">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-647">no</span></span>             | <span data-ttu-id="6b4a4-648">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-648">no</span></span>           |
| <span data-ttu-id="6b4a4-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="6b4a4-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="6b4a4-650">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-650">no</span></span>             | <span data-ttu-id="6b4a4-651">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-651">no</span></span>           |
| <span data-ttu-id="6b4a4-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="6b4a4-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="6b4a4-653">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-653">no</span></span>             | <span data-ttu-id="6b4a4-654">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-654">no</span></span>           |
| <span data-ttu-id="6b4a4-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="6b4a4-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="6b4a4-656">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-656">no</span></span>             | <span data-ttu-id="6b4a4-657">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-657">no</span></span>           |
| <span data-ttu-id="6b4a4-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="6b4a4-659">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-659">no</span></span>             | <span data-ttu-id="6b4a4-660">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-660">no</span></span>           |
| <span data-ttu-id="6b4a4-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="6b4a4-662">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-662">no</span></span>             | <span data-ttu-id="6b4a4-663">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-663">no</span></span>           |
| <span data-ttu-id="6b4a4-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="6b4a4-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="6b4a4-665">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-665">no</span></span>             | <span data-ttu-id="6b4a4-666">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-666">no</span></span>           |
| <span data-ttu-id="6b4a4-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6b4a4-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="6b4a4-668">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-668">no</span></span>             | <span data-ttu-id="6b4a4-669">nej</span><span class="sxs-lookup"><span data-stu-id="6b4a4-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="6b4a4-670">Begrænsninger og kendte problemer</span><span class="sxs-lookup"><span data-stu-id="6b4a4-670">Limitations and known issues</span></span>
<span data-ttu-id="6b4a4-671">Her følger en liste over begrænsninger og kendte problemer:</span><span class="sxs-lookup"><span data-stu-id="6b4a4-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="6b4a4-672">Planlægnings-API'er kan kun bruges af **Brugere med Microsoft Project-licens.**</span><span class="sxs-lookup"><span data-stu-id="6b4a4-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="6b4a4-673">De kan ikke bruges af:</span><span class="sxs-lookup"><span data-stu-id="6b4a4-673">They can't be used by:</span></span>
    - <span data-ttu-id="6b4a4-674">Programbrugere</span><span class="sxs-lookup"><span data-stu-id="6b4a4-674">Application users</span></span>
    - <span data-ttu-id="6b4a4-675">Systembrugere</span><span class="sxs-lookup"><span data-stu-id="6b4a4-675">System users</span></span>
    - <span data-ttu-id="6b4a4-676">Integrationsbrugere</span><span class="sxs-lookup"><span data-stu-id="6b4a4-676">Integration users</span></span>
    - <span data-ttu-id="6b4a4-677">Andre brugere, der ikke har den påkrævede licens</span><span class="sxs-lookup"><span data-stu-id="6b4a4-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="6b4a4-678">Hvert **OperationSet** kan kun have op til 100 handlinger.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="6b4a4-679">Hver bruger kan kun have op til 10 åbne **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="6b4a4-680">Project Operations understøtter i øjeblikket maksimalt 500 opgaver i alt på et projekt.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="6b4a4-681">Status for fejl i **OperationSet** og fejllogfiler er ikke tilgængelige i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="6b4a4-682">Planlægnings-API'er findes i offentlige forhåndsversioner.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="6b4a4-683">Brugen af disse API'er i et produktionsmiljø understøttes ikke af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="6b4a4-684">Begrænsninger og grænser for projekter og opgaver</span><span class="sxs-lookup"><span data-stu-id="6b4a4-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="6b4a4-685">Fejlhåndtering</span><span class="sxs-lookup"><span data-stu-id="6b4a4-685">Error handling</span></span>

   - <span data-ttu-id="6b4a4-686">Hvis du vil gennemse de fejl, der er genereret i operationssæt, skal du gå til **Indstillinger** \> **Integration af planlægning** \> **Operationssæt**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="6b4a4-687">Hvis du vil gennemse de fejl, der er genereret fra tjenesten Project Service, skal du gå til **Indstillinger** \> **Integration af planlægning** \> **PSS-fejllogfiler**.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="6b4a4-688">Eksempelscenarie</span><span class="sxs-lookup"><span data-stu-id="6b4a4-688">Sample scenario</span></span>

<span data-ttu-id="6b4a4-689">I dette scenario skal du oprette et projekt, et teammedlem, fire opgaver og to ressourcetildelinger.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="6b4a4-690">Derefter skal du opdatere én opgave, opdatere projektet, slette én opgave, slette én ressourcetildeling og oprette en opgaveafhængighed.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="6b4a4-691">Yderligere eksempler</span><span class="sxs-lookup"><span data-stu-id="6b4a4-691">Additional samples</span></span>

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
