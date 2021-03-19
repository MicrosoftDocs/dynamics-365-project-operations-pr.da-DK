---
title: Opret et projektteam
description: Dette emne indeholder oplysninger om, hvordan du opretter og administrerer projektteams.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270851"
---
# <a name="create-a-project-team"></a><span data-ttu-id="32126-103">Opret et projektteam</span><span class="sxs-lookup"><span data-stu-id="32126-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32126-104">Hvis du vil bruge de roller, der tidligere blev konfigureret i et projekt, skal en projektleder knytte rollerne sammen med projektet.</span><span class="sxs-lookup"><span data-stu-id="32126-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="32126-105">Der kan tildeles flere roller til et projekt.</span><span class="sxs-lookup"><span data-stu-id="32126-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="32126-106">For at forhindre forvirring navngives disse roller automatisk i forbindelse med reservationen.</span><span class="sxs-lookup"><span data-stu-id="32126-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="32126-107">Hvis projektlederen f.eks. har behov for tre softwareteknikere, oprettes der automatisk tre roller for softwareteknikere, der automatisk navngives **softwareingeniør1**, **softwareingeniør 2** og **softwareingeniør 3**.</span><span class="sxs-lookup"><span data-stu-id="32126-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="32126-108">Hvis der tidligere er konfigureret rolleegenskaber for rollen, anvendes de som et filter under søgninger efter en ressource.</span><span class="sxs-lookup"><span data-stu-id="32126-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="32126-109">Du kan tilføje yderligere egenskaber, hvis du vil begrænse søgningen yderligere.</span><span class="sxs-lookup"><span data-stu-id="32126-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="32126-110">Visningsindstillinger kan også tilpasses for at give en bedre visning af ressourcetilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="32126-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="32126-111">Der er mulighed for at få vist tilgængelighed baseret på tid, dag, uge, måned, kvartal og år.</span><span class="sxs-lookup"><span data-stu-id="32126-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="32126-112">Der findes også en indstilling, der viser tilgængelighed og resterende kapacitet for ressourcer.</span><span class="sxs-lookup"><span data-stu-id="32126-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="32126-113">Denne indstilling er nyttig i forbindelse med tidsstyring, når du beregner ledig tid for aktiviteter eller tilgængelighed af ressourcer.</span><span class="sxs-lookup"><span data-stu-id="32126-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="32126-114">Projektlederen kan vælge en rolle på siden og derefter vælge at reservere en ressource til at udfylde rollen, hvis der findes en tilgængelig ressource, der opfylder behovet.</span><span class="sxs-lookup"><span data-stu-id="32126-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="32126-115">Bemærk, at der ikke skal reserveres ressourcer på dette tidspunkt i planlægningsstadiet.</span><span class="sxs-lookup"><span data-stu-id="32126-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="32126-116">Når du opretter en WBS, kan du erstatte roller med personaleressourcer i projektet.</span><span class="sxs-lookup"><span data-stu-id="32126-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="32126-117">Hvis roller erstattes med personaleressourcer i WBS, opdaterer ressourceopsætningen automatisk projektteamets liste og planlægning.</span><span class="sxs-lookup"><span data-stu-id="32126-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="32126-118">[![Projektteamets liste, som indeholder både roller og faktiske ressourcer](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="32126-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="32126-119">Projektlederen har forskellige muligheder for at reservere en ressource til et bestemt projekt, f.eks. **Resterende kapacitet**, **Fuld kapacitet**, **Kapacitetsprocent** og **Angiv timer**.</span><span class="sxs-lookup"><span data-stu-id="32126-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="32126-120">Disse indstillinger for reservation kan når som helst annulleres, hvis ressourcetildelingerne ændres.</span><span class="sxs-lookup"><span data-stu-id="32126-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="32126-121">Der understøttes to typer af reservation:</span><span class="sxs-lookup"><span data-stu-id="32126-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="32126-122">**Reserver definitivt** – Ressourcereservationen blev godkendt og bekræftet til at arbejde på aftalen i den angivne periode.</span><span class="sxs-lookup"><span data-stu-id="32126-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="32126-123">**Reserver foreløbig** – Ressourcereservationer blev midlertidigt angivet til at arbejde på aftalen i den angivne periode.</span><span class="sxs-lookup"><span data-stu-id="32126-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="32126-124">Følgende procedure forklarer, hvordan du opretter et projektteam.</span><span class="sxs-lookup"><span data-stu-id="32126-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="32126-125">Opret et projektteam</span><span class="sxs-lookup"><span data-stu-id="32126-125">Create a project team</span></span>

1. <span data-ttu-id="32126-126">På listesiden **Alle projekter** skal du vælge et projekt og derefter vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="32126-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="32126-127">På fanen **Projektteam og planlægning** skal du i feltet **Planlæg slutdato** angive den planlagte startdato plus en måned.</span><span class="sxs-lookup"><span data-stu-id="32126-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="32126-128">Hvis planens startdato f.eks. er den 24. juni 2017 (24/06/2017), skal du angive **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="32126-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="32126-129">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="32126-129">Select **Add**.</span></span>
4. <span data-ttu-id="32126-130">I ruden **Tilføj roller til projektet** skal du i feltet **Rolle** vælge **Overordnet projektleder**.</span><span class="sxs-lookup"><span data-stu-id="32126-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="32126-131">Vælg **Krævede kompetencer**.</span><span class="sxs-lookup"><span data-stu-id="32126-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="32126-132">På siden **Vælg egenskaber** vælges de egenskaber, som du tidligere har angivet for rollen overordnet projektleder, som standard.</span><span class="sxs-lookup"><span data-stu-id="32126-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="32126-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="32126-133">Select **OK**.</span></span>
7. <span data-ttu-id="32126-134">På siden **Tilføj roller til projekt** skal du i feltet **Antal ressourcer** angive **1**.</span><span class="sxs-lookup"><span data-stu-id="32126-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="32126-135">I feltet **Ressource** vises opslaget for alle de ressourcer, der har de krævede kompetencer.</span><span class="sxs-lookup"><span data-stu-id="32126-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="32126-136">Vælg **Daniel Goldschmidt**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="32126-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="32126-137">På siden **Projekt** skal du vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="32126-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="32126-138">I ruden **Tilføj roller til projektet** skal du i feltet **Rolle** vælge **Teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="32126-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="32126-139">Angiv **5** i feltet **Antal ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="32126-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="32126-140">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="32126-140">Select **Create**.</span></span>
12. <span data-ttu-id="32126-141">På siden **Projekter** skal du vælge **Opfyld ressource**.</span><span class="sxs-lookup"><span data-stu-id="32126-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="32126-142">Overvåg projektteams</span><span class="sxs-lookup"><span data-stu-id="32126-142">Monitor project teams</span></span>
1. <span data-ttu-id="32126-143">På siden **Alle projekter** skal du vælge linket **Projekt-id** for projektet **XYZ-opgraderingsfase 2**.</span><span class="sxs-lookup"><span data-stu-id="32126-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="32126-144">På hurtigfanen **Projektteam og planlægning** skal du kontrollere, at de viste projektressourcer er korrekt angivet.</span><span class="sxs-lookup"><span data-stu-id="32126-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]