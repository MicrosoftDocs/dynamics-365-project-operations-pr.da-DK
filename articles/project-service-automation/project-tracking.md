---
title: Projektstatus og -omkostningsforbrug
description: Dette emne indeholder oplysninger om, hvordan du sporer projektstatus og omkostningsforbrug.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750603"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="b0498-103">Projektstatus og -omkostningsforbrug</span><span class="sxs-lookup"><span data-stu-id="b0498-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b0498-104">Behovet for at spore status i forhold til tidsplanen varierer fra branche til branche.</span><span class="sxs-lookup"><span data-stu-id="b0498-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="b0498-105">Nogle brancher sporer på et detaljeret niveau, mens andre brancher sporer på et højere niveau.</span><span class="sxs-lookup"><span data-stu-id="b0498-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="b0498-106">I dette emne vises, hvordan du planlægger for at opfylde din organisations behov.</span><span class="sxs-lookup"><span data-stu-id="b0498-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="b0498-107">Visning af indsatssporing</span><span class="sxs-lookup"><span data-stu-id="b0498-107">Effort tracking view</span></span>

<span data-ttu-id="b0498-108">Visningen af **Indsatssporing** sporer statussen for opgaver i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="b0498-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="b0498-109">Den sammenligner de faktiske indsatstimer, der er brugt på en opgave, med de planlagte indsatstimer for den pågældende opgave.</span><span class="sxs-lookup"><span data-stu-id="b0498-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="b0498-110">PSA bruger følgende formler til at beregne sporingsmålepunkter:</span><span class="sxs-lookup"><span data-stu-id="b0498-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="b0498-111">Status i procentsats = faktisk forbrug brugt indtil dato ÷ planlagt indsats for opgaven</span><span class="sxs-lookup"><span data-stu-id="b0498-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="b0498-112">Anslået tid inden fuldførelse (ETC) = planlagt indsats ÷ faktisk forbrug brugt indtil dato</span><span class="sxs-lookup"><span data-stu-id="b0498-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="b0498-113">Estimat ved fuldførelse (EAC) = resterende indsats + faktisk forbrug brugt indtil dato</span><span class="sxs-lookup"><span data-stu-id="b0498-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="b0498-114">Forventet afvigelse i tidsforbrug = planlagt indsats ÷ EAC</span><span class="sxs-lookup"><span data-stu-id="b0498-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="b0498-115">PSA viser en projektion af afvigelsen i tidsforbruget for opgaven.</span><span class="sxs-lookup"><span data-stu-id="b0498-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="b0498-116">Hvis EAC er højere end den planlagte indsats, projekteres opgaven til at tage længere tid, end det oprindeligt blev planlagt.</span><span class="sxs-lookup"><span data-stu-id="b0498-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="b0498-117">Projektet er derfor bagud i forhold til tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="b0498-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="b0498-118">Hvis EAC er lavere end den planlagte indsats, projekteres opgaven til at tage kortere tid, end det oprindeligt blev planlagt.</span><span class="sxs-lookup"><span data-stu-id="b0498-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="b0498-119">Projektet er derfor forud i forhold til tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="b0498-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="b0498-120">Ændre arbejdsindsats</span><span class="sxs-lookup"><span data-stu-id="b0498-120">Re-projecting effort</span></span>

<span data-ttu-id="b0498-121">Det er almindeligt, at en projektleder reviderer de oprindelige estimater for en opgave.</span><span class="sxs-lookup"><span data-stu-id="b0498-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="b0498-122">Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning.</span><span class="sxs-lookup"><span data-stu-id="b0498-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="b0498-123">Vi anbefaler dog ikke, at projektledere ændrer de oprindelige tal, fordi den oprindelige projektplan repræsenterer den etablerede sande kilde for projektets tidsplan og omkostningsestimat, og alle projektets interessenter er blevet enige herom.</span><span class="sxs-lookup"><span data-stu-id="b0498-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="b0498-124">En projektleder kan ændre arbejdsindsatsen på opgaver på to måder:</span><span class="sxs-lookup"><span data-stu-id="b0498-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="b0498-125">Tilsidesætte standard-ETC med et nyt estimat for den faktiske resterende indsats på opgaven.</span><span class="sxs-lookup"><span data-stu-id="b0498-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="b0498-126">Tilsidesætte standardstatussen i procent med et nyt estimat for den faktiske indsats på opgaven.</span><span class="sxs-lookup"><span data-stu-id="b0498-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="b0498-127">Hver af disse fremgangsmåder medfører en genberegning af ETC, EAC og statussen i procent samt den forventede afvigelse i tidsforbrug på en opgave.</span><span class="sxs-lookup"><span data-stu-id="b0498-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="b0498-128">EAC, ETC og status i procenten for hovedopgaver genberegnes også og giver en ny projektion af afvigelsen i tidsforbruget.</span><span class="sxs-lookup"><span data-stu-id="b0498-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="b0498-129">Ændring af arbejdsindsatsen på hovedopgaver</span><span class="sxs-lookup"><span data-stu-id="b0498-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="b0498-130">Arbejdsindsatsen for hovedopgaver og beholderopgaver kan ændres.</span><span class="sxs-lookup"><span data-stu-id="b0498-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="b0498-131">Uanset om brugeren ændrer arbejdsindsatsen ved hjælp af den resterende indsats eller statussen i procent på hovedopgaverne, tages følgende beregningssæt i anvendelse:</span><span class="sxs-lookup"><span data-stu-id="b0498-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="b0498-132">EAC, ETC og statussen i procent for opgaven beregnes.</span><span class="sxs-lookup"><span data-stu-id="b0498-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="b0498-133">Den nye EAC fordeles nedad til de underordnede opgaver i samme forhold, som den oprindelige EAC på opgaven blev fordelt.</span><span class="sxs-lookup"><span data-stu-id="b0498-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="b0498-134">Den nye EAC for hver af de enkeltstående opgaver nedad til bladnodeopgaver beregnes.</span><span class="sxs-lookup"><span data-stu-id="b0498-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="b0498-135">De påvirkede underordnede opgaver ned til bladnoderne får genberegnet deres ETC og status i procent på grundlag af EAC-værdien.</span><span class="sxs-lookup"><span data-stu-id="b0498-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="b0498-136">Dette medfører, at der laves en ny projektion for afvigelsen i tidsforbruget for opgaven.</span><span class="sxs-lookup"><span data-stu-id="b0498-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="b0498-137">EAC-værdierne for hovedopgaverne genberegnes helt ned til rodnoden.</span><span class="sxs-lookup"><span data-stu-id="b0498-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="b0498-138">Visning af omkostningssporing</span><span class="sxs-lookup"><span data-stu-id="b0498-138">Cost tracking view</span></span> 

<span data-ttu-id="b0498-139">Visningen **Omkostningssporing** sammenligner de faktiske omkostninger, der er brugt på en opgave, med de planlagte omkostninger for en opgave.</span><span class="sxs-lookup"><span data-stu-id="b0498-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="b0498-140">Denne visning viser kun omkostninger til arbejdsløn og inkluderer ikke omkostninger fra udgiftsestimaterne.</span><span class="sxs-lookup"><span data-stu-id="b0498-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="b0498-141">PSA bruger følgende formler til at beregne sporingsmålepunkter:</span><span class="sxs-lookup"><span data-stu-id="b0498-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="b0498-142">Procent af forbrug af omkostninger = faktiske omkostninger brugt indtil dato ÷ planlagte omkostninger for opgaven</span><span class="sxs-lookup"><span data-stu-id="b0498-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="b0498-143">Omkostninger indtil fuldførelse (CTC) = planlagte omkostninger ÷ faktiske omkostninger brugt indtil dato</span><span class="sxs-lookup"><span data-stu-id="b0498-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="b0498-144">EAC = CTC + faktiske omkostninger brugt indtil dato</span><span class="sxs-lookup"><span data-stu-id="b0498-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="b0498-145">Forventet omkostningsafvigelse = Planlagte omkostninger ÷ EAC</span><span class="sxs-lookup"><span data-stu-id="b0498-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="b0498-146">Der vises en projektion af afvigelsen i omkostningerne for opgaven.</span><span class="sxs-lookup"><span data-stu-id="b0498-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="b0498-147">Hvis EAC er højere end de planlagte omkostninger, projekteres opgaven til at have flere omkostninger, end det oprindeligt blev planlagt.</span><span class="sxs-lookup"><span data-stu-id="b0498-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="b0498-148">Der er derfor en tendens til at ligge over budgettet.</span><span class="sxs-lookup"><span data-stu-id="b0498-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="b0498-149">Hvis EAC er lavere end de planlagte omkostninger, projekteres opgaven til at have færre omkostninger, end det oprindeligt blev planlagt.</span><span class="sxs-lookup"><span data-stu-id="b0498-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="b0498-150">Der er derfor en tendens til at ligge under budgettet.</span><span class="sxs-lookup"><span data-stu-id="b0498-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="b0498-151">Projektlederens ændring af omkostningerne</span><span class="sxs-lookup"><span data-stu-id="b0498-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="b0498-152">Når indsatsen ændres, genberegnes CTC, EAC, det procentuelle omkostningsforbrug og den forventede omkostningsafvigelse alle sammen i visningen **Omkostningssporing**.</span><span class="sxs-lookup"><span data-stu-id="b0498-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="b0498-153">Projektstatusoversigt</span><span class="sxs-lookup"><span data-stu-id="b0498-153">Project status summary</span></span>

<span data-ttu-id="b0498-154">Når du sporer data i visningerne **Indsatssporing** og **Omkostningssporing** vises status og omkostningsforbrug på projektrodsnode-, hovedopgave- og bladnodeopgaveniveau.</span><span class="sxs-lookup"><span data-stu-id="b0498-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="b0498-155">Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over status på projektniveau.</span><span class="sxs-lookup"><span data-stu-id="b0498-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="b0498-156">Felter for statusoversigt</span><span class="sxs-lookup"><span data-stu-id="b0498-156">Status summary fields</span></span>

<span data-ttu-id="b0498-157">Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status.</span><span class="sxs-lookup"><span data-stu-id="b0498-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="b0498-158">Den bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko.</span><span class="sxs-lookup"><span data-stu-id="b0498-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="b0498-159">Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen.</span><span class="sxs-lookup"><span data-stu-id="b0498-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="b0498-160">Feltet **Status opdateret den** kan ikke redigeres, og værdien er et tidsstempel, der angiver, hvornår statussen senest blev opdateret.</span><span class="sxs-lookup"><span data-stu-id="b0498-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="b0498-161">Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b0498-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="b0498-162">Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, kan du angive disse felter til **Forud**</span><span class="sxs-lookup"><span data-stu-id="b0498-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="b0498-163">Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, kan du angive dem til **Bagud**.</span><span class="sxs-lookup"><span data-stu-id="b0498-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
