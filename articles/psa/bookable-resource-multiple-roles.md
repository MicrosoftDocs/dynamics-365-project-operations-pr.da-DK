---
title: Anslå projektsalg og -omkostninger, når en reserverbar ressource udfylder flere roller på et projekt
description: Dette emne indeholder oplysninger om, hvordan du kan bruge prisfastsættelsesdimensioner til at understøtte prisfastsættelse og omkostningsberegning for en ressource, der udfylder flere roller på et projekt.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074224"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="55298-103">Anslå projektsalg og -omkostninger, når en reserverbar ressource udfylder flere roller på et projekt</span><span class="sxs-lookup"><span data-stu-id="55298-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="55298-104">Projektbaserede virksomheder har ofte brug for, at en ressource udfører flere roller på et projekt.</span><span class="sxs-lookup"><span data-stu-id="55298-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="55298-105">Hver af disse roller kan være have forskellige prisfastsættelser og omkostningsberegninger, hvilket betyder, at den samme ressources tid på projektet kan resultere i et andet økonomisk estimat, afhængigt af faktureringshyppighed og omkostningssatser for hver af rollerne.</span><span class="sxs-lookup"><span data-stu-id="55298-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="55298-106">Project Service Automation gør det muligt at konfigurere værdierne på gruppemedlemmets posten for den navngivne ressource og for forskellige tilsidesættelser på hver af de opgaver, som teammedlemmet er tildelt til.</span><span class="sxs-lookup"><span data-stu-id="55298-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="55298-107">I følgende eksempel forklares det, hvordan en simpel tilsidesættelse af denne værdi gør det muligt for en ressource at have flere roller på et projekt med forskellige omkostninger og faktureringshyppighed.</span><span class="sxs-lookup"><span data-stu-id="55298-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="55298-108">Opret opgaver</span><span class="sxs-lookup"><span data-stu-id="55298-108">Create tasks</span></span>
<span data-ttu-id="55298-109">Opret to projektopgaver på hver 40 timer, opgave A og opgave B. Vælg opgave A som forgænger for opgave B.</span><span class="sxs-lookup"><span data-stu-id="55298-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="55298-110">Konfigurer Rolle og Afdeling for et generisk projektgruppemedlem</span><span class="sxs-lookup"><span data-stu-id="55298-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="55298-111">På siden **Planlægning** skal du for opgave A vælge rækken **Opgave**.</span><span class="sxs-lookup"><span data-stu-id="55298-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="55298-112">Vælg feltet **Ressourcer** , og vælg **Opret** i rullelisten.</span><span class="sxs-lookup"><span data-stu-id="55298-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="55298-113">På siden **Hurtig oprettelse af teammedlem** skal du angive attributterne for det generiske teammedlem, der kan udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="55298-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="55298-114">Vælg den relevante rolle og afdeling, og vælg derefter **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="55298-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="55298-115">Der oprettes et generisk gruppemedlem, og medlemmet tildeles til denne opgave.</span><span class="sxs-lookup"><span data-stu-id="55298-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="55298-116">Gentag disse trin for opgave B, og kontrollér, at rollen og organisationsenheden for det generiske gruppemedlem, der er oprettet for opgave B, ikke er de samme som for opgave A.</span><span class="sxs-lookup"><span data-stu-id="55298-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="55298-117">Konfigurer rolle og afdeling for en projektopgave</span><span class="sxs-lookup"><span data-stu-id="55298-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="55298-118">Når du har oprettet opgave A, skal du markere opgaven og derefter vælge **Rediger opgave**.</span><span class="sxs-lookup"><span data-stu-id="55298-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="55298-119">På siden **Opgavedetaljer** skal du finde felterne **Rolle** og **Afdeling** og tilføje de værdier, der kræves af en ressource, som skal udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="55298-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="55298-120">Hvis du fuldfører disse scenarier ved hjælp af demonstrationsdata for Project Service Automation, skal du vælge **Konsulterende kundeemne** for rollen, og **Fabrikam US** som afdeling.</span><span class="sxs-lookup"><span data-stu-id="55298-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="55298-121">Vælg opgave B, og vælg derefter **Rediger opgave**.</span><span class="sxs-lookup"><span data-stu-id="55298-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="55298-122">På siden **Opgavedetaljer** skal du finde felterne **Rolle** og **Afdeling** og tilføje de værdier, der kræves af en ressource, som skal udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="55298-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="55298-123">Kontroller, at værdierne i felterne **Rolle** og **Afdeling** er forskellige for opgave B i forhold til opgave A.</span><span class="sxs-lookup"><span data-stu-id="55298-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="55298-124">Hvis du fuldfører disse scenarier ved hjælp af demonstrationsdata for Project Service Automation, skal du vælge **Netværksteknikker** for rollen, og **Fabrikam US** som afdeling.</span><span class="sxs-lookup"><span data-stu-id="55298-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="55298-125">Gem og luk, og vælg siden **Opgavedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="55298-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="55298-126">Teammedlem og skønsadfærd</span><span class="sxs-lookup"><span data-stu-id="55298-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="55298-127">På siden **Opgavedetaljer** skal du under **Teammedlem** vælge de to generiske teammedlemmer og derefter vælge **Generer krav**.</span><span class="sxs-lookup"><span data-stu-id="55298-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="55298-128">Dette vil generere ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="55298-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="55298-129">Vælg teammedlemmets række for **Konsulterende kundeemne** , og vælg derefter **Reserver**.</span><span class="sxs-lookup"><span data-stu-id="55298-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="55298-130">Planlægningsområdet åbnes og reserverer en ressource i henhold til det pågældende krav.</span><span class="sxs-lookup"><span data-stu-id="55298-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="55298-131">Vælg teammedlemmets række for **Netværksteknikker** , og vælg derefter **Reserver**.</span><span class="sxs-lookup"><span data-stu-id="55298-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="55298-132">Planlægningsområdet åbnes og reserverer den samme ressource i henhold til det pågældende krav.</span><span class="sxs-lookup"><span data-stu-id="55298-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="55298-133">Teammedlemsgitter</span><span class="sxs-lookup"><span data-stu-id="55298-133">Team Member grid</span></span> 
<span data-ttu-id="55298-134">I gitteret **Teammedlem** skal du lægge mærke til, at de to generiske poster for teammedlemmet er blevet slettet og erstattet med en ressource.</span><span class="sxs-lookup"><span data-stu-id="55298-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="55298-135">Der er ét sæt værdier for den ressource, som viser et standardsæt af værdier for **Rolle** og **Afdeling**.</span><span class="sxs-lookup"><span data-stu-id="55298-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="55298-136">Når du udvider rækken for det pågældende teammedlems post, kan du se de forskellige tildelinger i teammedlemmets post for begge disse opgaver.</span><span class="sxs-lookup"><span data-stu-id="55298-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="55298-137">Hver tildelingsrække har opgavespecifikke værdier for **Rolle** og **Afdeling**.</span><span class="sxs-lookup"><span data-stu-id="55298-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="55298-138">Gitter til estimater</span><span class="sxs-lookup"><span data-stu-id="55298-138">Estimates grid</span></span> 
<span data-ttu-id="55298-139">Når du navigerer til gitteret **Estimater** , vil du bemærke, at tildelingerne til den samme ressource er prisfastsat forskelligt.</span><span class="sxs-lookup"><span data-stu-id="55298-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="55298-140">Tildelingen for ressourcen på opgave A er prisfastsat ved hjælp af **Rolle** -attributværdien for **Konsulterende kundeemne**.</span><span class="sxs-lookup"><span data-stu-id="55298-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="55298-141">Tildelingen for den samme ressource på opgave B er prisfastsat ved hjælp af **Rolle** -attributværdien for **Netværkstekniker**.</span><span class="sxs-lookup"><span data-stu-id="55298-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





