---
title: Se det fakturerbare tidsforbrug for ressourcer
description: Dette emne indeholder oplysninger om visningen ressourceforbrug.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750493"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="c05c3-103">Se det fakturerbare tidsforbrug for ressourcer</span><span class="sxs-lookup"><span data-stu-id="c05c3-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="c05c3-104">Visningen **Tidsforbrug** på siden **Tidsforbrug for ressource i Project Service** viser fakturerbart tidsforbrug for hver reserverbar ressource.</span><span class="sxs-lookup"><span data-stu-id="c05c3-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="c05c3-105">Da visningen er baseret på planlægningsområdet, finder du mange af de samme funktioner.</span><span class="sxs-lookup"><span data-stu-id="c05c3-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Skærmbillede af visningen Tidsforbrug](media/FAQ-utilization-1.png)
 

<span data-ttu-id="c05c3-107">Beregningen af fakturerbart tidsforbrug fungerer på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="c05c3-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="c05c3-108">Fakturerbart tidsforbrug = (fakturerbare faktiske timer)/(ressourcens kapacitet)</span><span class="sxs-lookup"><span data-stu-id="c05c3-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="c05c3-109">Cellerne repræsenterer det beregnede fakturerbare tidsforbrug for den periode, der er valgt (dage, uger eller måneder).</span><span class="sxs-lookup"><span data-stu-id="c05c3-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="c05c3-110">Farverne i hver celle viser det fakturerbare tidsforbrug for en ressource i forhold til ressourcens fakturerbare tidsforbrug, der er målet.</span><span class="sxs-lookup"><span data-stu-id="c05c3-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="c05c3-111">Det tidsforbrug, der er målet, kan indstilles i enten ressourcens standardrolle eller i den enkelte ressource.</span><span class="sxs-lookup"><span data-stu-id="c05c3-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="c05c3-112">Beregningen ser først på personen for målet og derefter på ressourcens standardrolle.</span><span class="sxs-lookup"><span data-stu-id="c05c3-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="c05c3-113">Angive målet for en ressource</span><span class="sxs-lookup"><span data-stu-id="c05c3-113">Set target on a resource</span></span>

1. <span data-ttu-id="c05c3-114">Gå til **Ressourcer** \> **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c05c3-115">Vælg en ressource for at åbne posten.</span><span class="sxs-lookup"><span data-stu-id="c05c3-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="c05c3-116">Under fanen **Project Service** kan du angive ressourcens mål-tidsforbrug.</span><span class="sxs-lookup"><span data-stu-id="c05c3-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Skærmbillede, hvor fanen Projektstyring bruges til at angive det tidsforbrug, der er målet](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="c05c3-118">Angive mål-tidsforbrug for en rolle</span><span class="sxs-lookup"><span data-stu-id="c05c3-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="c05c3-119">Gå til **Ressourcer** \> **Ressourceroller**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="c05c3-120">Vælg en rolle og åbn posten.</span><span class="sxs-lookup"><span data-stu-id="c05c3-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="c05c3-121">Indstil måltidsforbruget for rollen.</span><span class="sxs-lookup"><span data-stu-id="c05c3-121">Set the target utilization for the role.</span></span>

> ![Skærmbillede, hvor Ressourceroller indstilles til det tidsforbrug, der er målet](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="c05c3-123">Beregne det fakturerbare tidsforbrug for en ressource?</span><span class="sxs-lookup"><span data-stu-id="c05c3-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="c05c3-124">For at beregne det fakturerbare tidsforbrug for en ressource skal du opfylde nogle forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="c05c3-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="c05c3-125">Angive standardrolle for individuel ressource</span><span class="sxs-lookup"><span data-stu-id="c05c3-125">Set default role for individual resource</span></span>

<span data-ttu-id="c05c3-126">For det første skal mål-tidsforbruget angives i enten den enkelte ressource eller i ressourceroller.</span><span class="sxs-lookup"><span data-stu-id="c05c3-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="c05c3-127">Hvis du bruger ressourceroller til mål, skal hver enkelt ressource have en standardrolle.</span><span class="sxs-lookup"><span data-stu-id="c05c3-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="c05c3-128">Du kan angive rollen ved at gå til **Ressourcer** \> **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c05c3-129">Vælg en ressource, åbn posten, og vælg derefter fanen **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="c05c3-130">I gitteret **Resourcerolle** skal du sørge for, at der er en rolle til ressourcen, og at **Er standard** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="c05c3-131">Skift faktureringstype for ressourcerolle</span><span class="sxs-lookup"><span data-stu-id="c05c3-131">Change billing type for resource role</span></span>

<span data-ttu-id="c05c3-132">Ressourcerollerne skal indstilles til faktureringstypen **fakturerbar**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="c05c3-133">Gå til **Ressourcer** \> **Ressourceroller**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="c05c3-134">Åbn den post, du ønsker at opdatere, og indstil derefter faktureringstypens standard til **Fakturerbar**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="c05c3-135">Angive arbejdstimer for ressourcerolle</span><span class="sxs-lookup"><span data-stu-id="c05c3-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="c05c3-136">Ressourcen skal have arbejdstimer til kapacitetsberegningen.</span><span class="sxs-lookup"><span data-stu-id="c05c3-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="c05c3-137">Gå til **Ressourcer** \> **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c05c3-138">Vælg en ressource for at åbne posten, og vælg derefter **Vis arbejdstimer**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="c05c3-139">Du kan masseopdatere listen over ressourcer ved at anvende en **arbejdstimeskabelon** fra visningen **Ressourceliste**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="c05c3-140">Fejlfinding af fakturerbare faktiske timer</span><span class="sxs-lookup"><span data-stu-id="c05c3-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="c05c3-141">De faktiske fakturerbare timer er hentet fra objektet **Faktiske**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="c05c3-142">Faktiske med faktureringstypen **fakturerbar** medtages i beregningen, og derfor skal du have projekter, hvor de faktiske værdier er fakturerbare.</span><span class="sxs-lookup"><span data-stu-id="c05c3-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="c05c3-143">Hvis du ikke kan se fakturerbart tidsforbrug, er her nogle ting, du kan kontrollere:</span><span class="sxs-lookup"><span data-stu-id="c05c3-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="c05c3-144">Ressourcen har definerede arbejdstimer for kapacitet.</span><span class="sxs-lookup"><span data-stu-id="c05c3-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="c05c3-145">Ressourcen er enten et individuelt definerede tidsforbrugmål eller har en standardrolle tildelt til den.</span><span class="sxs-lookup"><span data-stu-id="c05c3-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="c05c3-146">Rollen med et defineret tidsforbrugmål.</span><span class="sxs-lookup"><span data-stu-id="c05c3-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="c05c3-147">Faktiske har faktureringstypen **fakturerbar** for den periode, du forventer en beregning af tidsforbrug for.</span><span class="sxs-lookup"><span data-stu-id="c05c3-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="c05c3-148">Kontrollér følgende, hvis du får vist faktiske med andre faktureringstyper end fakturerbar:</span><span class="sxs-lookup"><span data-stu-id="c05c3-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="c05c3-149">Den rolle, der er brugt på den faktiske indeholder en anden standardfaktureringstype end fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="c05c3-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="c05c3-150">Rollen i den projektkontraktlinje, der sikkerhedskopierer projektet, er indstillet til ikke-fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="c05c3-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="c05c3-151">Projektet har ikke en tilknyttet kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="c05c3-151">The project does not have an associated contract line.</span></span>

