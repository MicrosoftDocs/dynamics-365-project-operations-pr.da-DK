---
title: Projektstatus og -omkostningsforbrug
description: Dette emne indeholder oplysninger om sporing af projektstatus og omkostningsforbrug.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148006"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="78de9-103">Projektstatus og -omkostningsforbrug</span><span class="sxs-lookup"><span data-stu-id="78de9-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="78de9-104">Behovet for at spore status i forhold til tidsplanen varierer fra branche til branche.</span><span class="sxs-lookup"><span data-stu-id="78de9-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="78de9-105">Nogle brancher sporer på et detaljeret niveau, mens andre brancher sporer på et højere niveau.</span><span class="sxs-lookup"><span data-stu-id="78de9-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="78de9-106">I dette emne vises, hvordan du planlægger for at opfylde din organisations behov.</span><span class="sxs-lookup"><span data-stu-id="78de9-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="78de9-107">Visning af indsatssporing</span><span class="sxs-lookup"><span data-stu-id="78de9-107">Effort tracking view</span></span>

<span data-ttu-id="78de9-108">Visningen af **Indsatssporing** sporer statussen for opgaver i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="78de9-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="78de9-109">Den sammenligner de faktiske timer, der er brugt på en opgave, med opgavens planlagte forbrug af timer.</span><span class="sxs-lookup"><span data-stu-id="78de9-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="78de9-110">Project Service Automation bruger følgende formler til at beregne sporingsmålepunkter:</span><span class="sxs-lookup"><span data-stu-id="78de9-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="78de9-111">Til at begynde med i opgaveoprettelsen: planlagte omkostninger angives til den estimerede omkostning ved fuldførelse.</span><span class="sxs-lookup"><span data-stu-id="78de9-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="78de9-112">Når der registreres faktiske oplysninger på opgaven, foretages der en beregning af følgende i Visningen af tidsforbrugssporing</span><span class="sxs-lookup"><span data-stu-id="78de9-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="78de9-113">Procentvis fremgang = faktisk tidsforbrug til dato - estimeret ved fuldførelse (EAC)</span><span class="sxs-lookup"><span data-stu-id="78de9-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="78de9-114">Estimeret tid til fuldførelse (ETC) = estimeret ved fuldfuldførelse (EAC) – faktisk tidsforbrug til dato</span><span class="sxs-lookup"><span data-stu-id="78de9-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="78de9-115">EAC = resterende tidsforbrug + faktisk tidsforbrug til dato</span><span class="sxs-lookup"><span data-stu-id="78de9-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="78de9-116">Forventet afvigelse i tidsforbrug = planlagt indsats ÷ EAC</span><span class="sxs-lookup"><span data-stu-id="78de9-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="78de9-117">Project Service Automation viser en projektion af afvigelsen i tidsforbruget for opgaven.</span><span class="sxs-lookup"><span data-stu-id="78de9-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="78de9-118">Hvis EAC er højere end den planlagte indsats, projekteres opgaven til at tage længere tid, end det oprindeligt blev planlagt.</span><span class="sxs-lookup"><span data-stu-id="78de9-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="78de9-119">Projektet er derfor bagud i forhold til tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="78de9-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="78de9-120">Hvis EAC er lavere end den planlagte indsats, projekteres opgaven til at tage kortere tid, end det oprindeligt blev planlagt.</span><span class="sxs-lookup"><span data-stu-id="78de9-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="78de9-121">Projektet er derfor forud i forhold til tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="78de9-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="78de9-122">Ændre arbejdsindsats</span><span class="sxs-lookup"><span data-stu-id="78de9-122">Reprojecting effort</span></span>

<span data-ttu-id="78de9-123">Det er almindeligt, at en projektleder reviderer de oprindelige estimater for en opgave.</span><span class="sxs-lookup"><span data-stu-id="78de9-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="78de9-124">Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning.</span><span class="sxs-lookup"><span data-stu-id="78de9-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="78de9-125">Vi anbefaler dog ikke, at projektledere ændrer de oprindelige tal, fordi den oprindelige projektplan repræsenterer den etablerede sande kilde for projektets tidsplan og omkostningsestimat, og alle projektets interessenter er blevet enige herom.</span><span class="sxs-lookup"><span data-stu-id="78de9-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="78de9-126">En projektleder kan ændre arbejdsindsatsen på opgaver på to måder:</span><span class="sxs-lookup"><span data-stu-id="78de9-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="78de9-127">Tilsidesætte standard-ETC med et nyt estimat for den faktiske resterende indsats på opgaven.</span><span class="sxs-lookup"><span data-stu-id="78de9-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="78de9-128">Tilsidesætte standardstatussen i procent med et nyt estimat for den faktiske indsats på opgaven.</span><span class="sxs-lookup"><span data-stu-id="78de9-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="78de9-129">Hver af disse fremgangsmåder medfører en genberegning af ETC, EAC og statussen i procent samt den forventede afvigelse i tidsforbrug på en opgave.</span><span class="sxs-lookup"><span data-stu-id="78de9-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="78de9-130">EAC, ETC og status i procenten for hovedopgaver genberegnes også og giver en ny projektion af afvigelsen i tidsforbruget.</span><span class="sxs-lookup"><span data-stu-id="78de9-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="78de9-131">Ændring af arbejdsindsatsen på hovedopgaver</span><span class="sxs-lookup"><span data-stu-id="78de9-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="78de9-132">Arbejdsindsatsen for hovedopgaver og beholderopgaver kan ændres.</span><span class="sxs-lookup"><span data-stu-id="78de9-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="78de9-133">Uanset om brugeren ændrer arbejdsindsatsen ved hjælp af den resterende indsats eller statussen i procent på hovedopgaverne, tages følgende beregningssæt i anvendelse:</span><span class="sxs-lookup"><span data-stu-id="78de9-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="78de9-134">EAC, ETC og statussen i procent for opgaven beregnes.</span><span class="sxs-lookup"><span data-stu-id="78de9-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="78de9-135">Den nye EAC fordeles nedad til de underordnede opgaver i samme forhold, som den oprindelige EAC på opgaven blev fordelt.</span><span class="sxs-lookup"><span data-stu-id="78de9-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="78de9-136">Den nye EAC for hver af de enkelte opgaver nedad til bladnodeopgaver beregnes.</span><span class="sxs-lookup"><span data-stu-id="78de9-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="78de9-137">De påvirkede underordnede opgaver ned til bladnoderne får genberegnet deres ETC og status i procent på grundlag af EAC-værdien.</span><span class="sxs-lookup"><span data-stu-id="78de9-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="78de9-138">Dette medfører, at der laves en ny projektion for afvigelsen i tidsforbruget for opgaven.</span><span class="sxs-lookup"><span data-stu-id="78de9-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="78de9-139">EAC-værdierne for hovedopgaverne genberegnes helt ned til rodnoden.</span><span class="sxs-lookup"><span data-stu-id="78de9-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="78de9-140">Visning af omkostningssporing</span><span class="sxs-lookup"><span data-stu-id="78de9-140">Cost tracking view</span></span> 

<span data-ttu-id="78de9-141">Visningen **Omkostningssporing** sammenligner de faktiske omkostninger, der er brugt på en opgave, med de planlagte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="78de9-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="78de9-142">Denne visning viser kun omkostninger til arbejdsløn og inkluderer ikke omkostninger fra udgiftsestimaterne.</span><span class="sxs-lookup"><span data-stu-id="78de9-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="78de9-143">Project Service Automation bruger følgende formler til at beregne sporingsmålepunkter:</span><span class="sxs-lookup"><span data-stu-id="78de9-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="78de9-144">Når en opgave oprettes, er de planlagte omkostninger lig med de anslåede omkostninger ved fuldførelse.</span><span class="sxs-lookup"><span data-stu-id="78de9-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="78de9-145">Når faktiske oplysninger registreres på opgaven, beregnes følgende i visningen af **Sporing** af omkostninger:</span><span class="sxs-lookup"><span data-stu-id="78de9-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="78de9-146">Procent af forbrugte omkostninger = faktiske omkostninger brugt til dato ÷ estimerede omkostninger ved fuldførelse af opgaven</span><span class="sxs-lookup"><span data-stu-id="78de9-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="78de9-147">Omkostninger for at fuldføre (CTC) = estimerede omkostninger ved fuldførelse - faktiske omkostninger brugt til dato</span><span class="sxs-lookup"><span data-stu-id="78de9-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="78de9-148">Estimerede omkostninger ved fuldførelse = CTC + faktiske omkostninger brugt til dato</span><span class="sxs-lookup"><span data-stu-id="78de9-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="78de9-149">Anslået omkostningsafvigelse = planlagte omkostninger – estimerede omkostninger ved fuldførelse</span><span class="sxs-lookup"><span data-stu-id="78de9-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="78de9-150">Der vises en projektion af afvigelsen i omkostningerne for opgaven.</span><span class="sxs-lookup"><span data-stu-id="78de9-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="78de9-151">Hvis de estimerede omkostninger ved fuldførelse er højere end de planlagte omkostninger, projekteres opgaven til at blive dyrere, end det oprindeligt var planlagt.</span><span class="sxs-lookup"><span data-stu-id="78de9-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="78de9-152">Der er derfor en tendens til at ligge over budgettet.</span><span class="sxs-lookup"><span data-stu-id="78de9-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="78de9-153">Hvis de estimerede omkostninger ved fuldførelse er lavere end de planlagte omkostninger, projekteres opgaven til at blive billigere, end det oprindeligt var planlagt, og har derfor en tendens til at ligge under budgettet.</span><span class="sxs-lookup"><span data-stu-id="78de9-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="78de9-154">Projektlederens ændring af omkostningerne</span><span class="sxs-lookup"><span data-stu-id="78de9-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="78de9-155">Når tidsforbruget ændres, genberegnes CTC, de estimerede omkostninger ved fuldførelse, det procentuelle omkostningsforbrug og den forventede omkostningsafvigelse alle sammen i visningen **Omkostningssporing**.</span><span class="sxs-lookup"><span data-stu-id="78de9-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="78de9-156">Projektstatusoversigt</span><span class="sxs-lookup"><span data-stu-id="78de9-156">Project status summary</span></span>

<span data-ttu-id="78de9-157">Når du sporer data i visningerne **Indsatssporing** og **Omkostningssporing** vises status og omkostningsforbrug på projektrodsnode-, hovedopgave- og bladnodeopgaveniveau.</span><span class="sxs-lookup"><span data-stu-id="78de9-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="78de9-158">Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over status på projektniveau.</span><span class="sxs-lookup"><span data-stu-id="78de9-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="78de9-159">Felter for statusoversigt</span><span class="sxs-lookup"><span data-stu-id="78de9-159">Status summary fields</span></span>

<span data-ttu-id="78de9-160">Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status.</span><span class="sxs-lookup"><span data-stu-id="78de9-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="78de9-161">Den bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko.</span><span class="sxs-lookup"><span data-stu-id="78de9-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="78de9-162">Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen.</span><span class="sxs-lookup"><span data-stu-id="78de9-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="78de9-163">Feltet **Status opdateret den** kan ikke redigeres, og værdien er et tidsstempel, der angiver, hvornår statussen senest blev opdateret.</span><span class="sxs-lookup"><span data-stu-id="78de9-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="78de9-164">Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="78de9-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="78de9-165">Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, kan du angive disse felter til **Forud**</span><span class="sxs-lookup"><span data-stu-id="78de9-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="78de9-166">Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, kan du angive dem til **Bagud**.</span><span class="sxs-lookup"><span data-stu-id="78de9-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
