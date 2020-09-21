---
title: Ændringer i ressourcestyringen (Project Service Automation 3.x)
description: Dette emne indeholder oplysninger om ændringerne i ressourcestyringsområdet.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750562"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="dc59b-103">Ændringer i ressourcestyringen (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="dc59b-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="dc59b-104">Sektionerne i dette emne indeholder oplysninger om de ændringer, der er foretaget i ressourcestyringsområdet i Dynamics 365 Project Service Automation version 3.x.</span><span class="sxs-lookup"><span data-stu-id="dc59b-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="dc59b-105">Projektestimater</span><span class="sxs-lookup"><span data-stu-id="dc59b-105">Project estimates</span></span>

<span data-ttu-id="dc59b-106">I stedet for at være baseret på **msdyn\_projecttask**-objektet (**Projektopgave**) baseres projektestimater på objektet **msdyn\_ressourceassignment** (**Ressourcetildeling**).</span><span class="sxs-lookup"><span data-stu-id="dc59b-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="dc59b-107">Ressourcetildelinger er blevet "kilden til sandhed" for opgaveplanlægning og prisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="dc59b-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="dc59b-108">Linjeopgaver</span><span class="sxs-lookup"><span data-stu-id="dc59b-108">Line tasks</span></span>

<span data-ttu-id="dc59b-109">I PSA 3.x er linjeopgaver forældede (frarådes).</span><span class="sxs-lookup"><span data-stu-id="dc59b-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="dc59b-110">Tildelinger peger nu på hele opgaven i stedet for linjeopgaver.</span><span class="sxs-lookup"><span data-stu-id="dc59b-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="dc59b-111">I det følgende eksempel kan du se, hvordan en opgave med navnet "Testopgave" tildeles til teammedlemmer A og B i tidligere versioner af PSA og i PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="dc59b-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="dc59b-112">**Før PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="dc59b-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="dc59b-113">Testopgave</span><span class="sxs-lookup"><span data-stu-id="dc59b-113">Test task</span></span>

        - <span data-ttu-id="dc59b-114">Testopgave – Linjeopgave 1</span><span class="sxs-lookup"><span data-stu-id="dc59b-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="dc59b-115">Tildeling til A</span><span class="sxs-lookup"><span data-stu-id="dc59b-115">Assignment to A</span></span>

        - <span data-ttu-id="dc59b-116">Testopgave – Linjeopgave 2</span><span class="sxs-lookup"><span data-stu-id="dc59b-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="dc59b-117">Tildeling til B</span><span class="sxs-lookup"><span data-stu-id="dc59b-117">Assignment to B</span></span>

- <span data-ttu-id="dc59b-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="dc59b-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="dc59b-119">Testopgave</span><span class="sxs-lookup"><span data-stu-id="dc59b-119">Test task</span></span>

        - <span data-ttu-id="dc59b-120">Tildeling til A</span><span class="sxs-lookup"><span data-stu-id="dc59b-120">Assignment to A</span></span>
        - <span data-ttu-id="dc59b-121">Tildeling til B</span><span class="sxs-lookup"><span data-stu-id="dc59b-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="dc59b-122">Ikke-tildelt tildeling</span><span class="sxs-lookup"><span data-stu-id="dc59b-122">Unassigned assignment</span></span>

<span data-ttu-id="dc59b-123">I PSA 3.x er en ikke-tildelt tildeling en tildeling, der er tildelt til et **NULL**-teammedlem og **NULL**-ressource.</span><span class="sxs-lookup"><span data-stu-id="dc59b-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="dc59b-124">Ikke-tildelte tildelinger kan forekomme i et par scenarier:</span><span class="sxs-lookup"><span data-stu-id="dc59b-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="dc59b-125">Hvis en opgave er blevet oprettet, men endnu ikke er tildelt til et teammedlem, oprettes der altid en ikke-tildelt tildeling.</span><span class="sxs-lookup"><span data-stu-id="dc59b-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="dc59b-126">Hvis alle modtagere af en opgave fjernes, oprettes der en ikke-tildelt tildeling igen for den pågældende opgave.</span><span class="sxs-lookup"><span data-stu-id="dc59b-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="dc59b-127">Planlægningsfelter på objektet Projektopgave</span><span class="sxs-lookup"><span data-stu-id="dc59b-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="dc59b-128">Felterne på **msdyn\_projecttask**-objektet er forældede eller flyttet til objektet **msdyn\_resourceassignment**, eller der henvises nu til dem fra objektet **msdyn\_projectteam** (**Projektteammedlem**).</span><span class="sxs-lookup"><span data-stu-id="dc59b-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="dc59b-129">Feltet frarådes i msdyn\_projecttask (projektopgave)</span><span class="sxs-lookup"><span data-stu-id="dc59b-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="dc59b-130">Nyt felt i msdyn\_resourceassignment (ressourcetildeling)</span><span class="sxs-lookup"><span data-stu-id="dc59b-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="dc59b-131">Kommentar</span><span class="sxs-lookup"><span data-stu-id="dc59b-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="dc59b-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="dc59b-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="dc59b-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc59b-133">None</span></span> | |
| <span data-ttu-id="dc59b-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="dc59b-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="dc59b-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc59b-135">None</span></span> | |
| <span data-ttu-id="dc59b-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="dc59b-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="dc59b-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc59b-137">None</span></span> | |
| <span data-ttu-id="dc59b-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="dc59b-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="dc59b-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc59b-139">None</span></span> | |
| <span data-ttu-id="dc59b-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="dc59b-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="dc59b-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="dc59b-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="dc59b-142">Formatet for JavaScript Object Notation-datastrukturen (JSON), der er gemt i feltet, er blevet ændret.</span><span class="sxs-lookup"><span data-stu-id="dc59b-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="dc59b-143">Planlægge en profil</span><span class="sxs-lookup"><span data-stu-id="dc59b-143">Schedule contour</span></span>

<span data-ttu-id="dc59b-144">Planlægningsprofilen gemmes i feltet **Planlagt arbejde** (**msdyn\_plannedwork**) for hvert enkelt **ressourcetildelings**-objekt (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="dc59b-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="dc59b-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="dc59b-145">Structure</span></span>

<span data-ttu-id="dc59b-146">Den nye struktur i planlægningsprofilen består af fleksible tidsrum, der defineres for hver dag i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="dc59b-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="dc59b-147">Hvert tidsrum har følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="dc59b-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="dc59b-148">**Start** – Start på arbejdstimerne for dagen ifølge projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="dc59b-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="dc59b-149">**Slut** – Slut på arbejdstimerne for dagen ifølge projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="dc59b-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="dc59b-150">**Timer** – Det antal timer, der er tildelt på dagen.</span><span class="sxs-lookup"><span data-stu-id="dc59b-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="dc59b-151">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="dc59b-151">**Example**</span></span>

<span data-ttu-id="dc59b-152">I dette eksempel bruges der en projektkalender, hvor arbejdsdagen er kl. 9-17 i tidszonen UTC-8.</span><span class="sxs-lookup"><span data-stu-id="dc59b-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="dc59b-153">Automatisk planlægning og manuel planlægning</span><span class="sxs-lookup"><span data-stu-id="dc59b-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="dc59b-154">Hvis en opgave planlægges automatisk, indlæses timerne i forvejen, og opgavevarigheden reduceres måske.</span><span class="sxs-lookup"><span data-stu-id="dc59b-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="dc59b-155">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="dc59b-155">**Example**</span></span>

<span data-ttu-id="dc59b-156">Den følgende opgave planlægges automatisk i 18 timer over tre dage (3. december 2018 til 5. december 2018).</span><span class="sxs-lookup"><span data-stu-id="dc59b-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="dc59b-157">Hvis en opgave planlægges manuelt, fordeles timerne jævnt over alle datoer.</span><span class="sxs-lookup"><span data-stu-id="dc59b-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="dc59b-158">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="dc59b-158">**Example**</span></span>

<span data-ttu-id="dc59b-159">Den følgende opgave er planlagt automatisk til 18 timer over tre dage (3. december 2018 til 5. december 2018).</span><span class="sxs-lookup"><span data-stu-id="dc59b-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="dc59b-160">Tildelingsenhed</span><span class="sxs-lookup"><span data-stu-id="dc59b-160">Assignment unit</span></span>

<span data-ttu-id="dc59b-161">Tildelingsenheden er udeladt i PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="dc59b-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="dc59b-162">Tiden for opgaven fordeles nu ligeligt pr. dag mellem alle de tildelte ressourcer.</span><span class="sxs-lookup"><span data-stu-id="dc59b-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="dc59b-163">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="dc59b-163">**Example**</span></span>

<span data-ttu-id="dc59b-164">I dette eksempel tildeles opgaven til to ressourcer, og den planlægges automatisk til 36 timer over tre dage (3. december 2018 til 5. december 2018).</span><span class="sxs-lookup"><span data-stu-id="dc59b-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="dc59b-165">Tildeling 1:</span><span class="sxs-lookup"><span data-stu-id="dc59b-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="dc59b-166">Tildeling 2:</span><span class="sxs-lookup"><span data-stu-id="dc59b-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="dc59b-167">Prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="dc59b-167">Pricing dimensions</span></span>

<span data-ttu-id="dc59b-168">I PSA 3.x er felterne for ressourcespecifikke prisfastsættelsesdimensioner (f.eks. **Rolle** og **Afdeling**) blevet fjernet fra objektet **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="dc59b-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="dc59b-169">Disse felter kan nu hentes fra det aktuelle projektteammedlem (**msdyn\_projectteam**) i ressourcetildelingen (**msdyn\_resourceassignment**), når der genereres projektestimater.</span><span class="sxs-lookup"><span data-stu-id="dc59b-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="dc59b-170">Der er føjet et nyt felt, **msdyn\_organizationalunit**, til objektet **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="dc59b-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="dc59b-171">Feltet frarådes i msdyn\_projecttask (projektopgave)</span><span class="sxs-lookup"><span data-stu-id="dc59b-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="dc59b-172">Felt fra msdyn\_projectteam (projektteammedlem), der bruges i stedet</span><span class="sxs-lookup"><span data-stu-id="dc59b-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="dc59b-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="dc59b-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="dc59b-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="dc59b-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="dc59b-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="dc59b-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="dc59b-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="dc59b-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="dc59b-177">Profiler</span><span class="sxs-lookup"><span data-stu-id="dc59b-177">Contours</span></span>

<span data-ttu-id="dc59b-178">Profilfelterne for prisfastsættelse og estimerng er udeladt i objektet **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="dc59b-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="dc59b-179">De er blevet flyttet til objektet **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="dc59b-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="dc59b-180">Feltet frarådes i msdyn\_projecttask (projektopgave)</span><span class="sxs-lookup"><span data-stu-id="dc59b-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="dc59b-181">Nyt felt i msdyn\_resourceassignment (ressourcetildeling)</span><span class="sxs-lookup"><span data-stu-id="dc59b-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="dc59b-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="dc59b-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="dc59b-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="dc59b-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="dc59b-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="dc59b-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="dc59b-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="dc59b-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="dc59b-186">De følgende felter er blevet føjet til objektet **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="dc59b-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="dc59b-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="dc59b-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="dc59b-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="dc59b-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="dc59b-189">De følgende felter for planlagte, faktiske og resterende omkostninger og salg er uændrede i objektet **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="dc59b-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="dc59b-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="dc59b-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="dc59b-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="dc59b-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="dc59b-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="dc59b-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="dc59b-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="dc59b-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="dc59b-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="dc59b-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="dc59b-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="dc59b-195">msdyn\_remainingsales</span></span>
