---
title: Konfigurer projektressourcer
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer eller anmoder om projektressourcer.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288732"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="c595d-103">Konfigurer projektressourcer</span><span class="sxs-lookup"><span data-stu-id="c595d-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c595d-104">Du skal konfigurere en kalender og knytte den til en medarbejder eller en arbejder.</span><span class="sxs-lookup"><span data-stu-id="c595d-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="c595d-105">Kalenderen bruges til at planlægge projektet og arbejdstiden for de ressourcer, der er reserveret til projektet.</span><span class="sxs-lookup"><span data-stu-id="c595d-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="c595d-106">I forbindelse med kalenderkonfigurationen kan projektledere udføre ressourceudjævning som led i ressourceoptimering.</span><span class="sxs-lookup"><span data-stu-id="c595d-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="c595d-107">Afhængigt af kalenderplanen kan der indføres begrænsninger for ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c595d-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="c595d-108">Du kan konfigurere en kalender på siden **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="c595d-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="c595d-109">Når du konfigurerer en arbejder som en projektressource, kan du vælge mellem arbejdere, der arbejder i den virksomhed, som du opretter ressourcer for.</span><span class="sxs-lookup"><span data-stu-id="c595d-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="c595d-110">Du kan også vælge arbejdere fra andre firmaer i organisationen.</span><span class="sxs-lookup"><span data-stu-id="c595d-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="c595d-111">Disse arbejdere kaldes interne ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c595d-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="c595d-112">I følgende procedurer får du beskrevet, hvordan du kan konfigurere en arbejder som en projektressource i virksomheden, og hvordan du kan konfigurere en intern projektressource.</span><span class="sxs-lookup"><span data-stu-id="c595d-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="c595d-113">Konfigurere en arbejder som en projektressource</span><span class="sxs-lookup"><span data-stu-id="c595d-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="c595d-114">På siden **Arbejdere** i listen **Arbejdere** skal du vælge den arbejder, som du tilføjer som en projektressource, og åbne arbejderposten.</span><span class="sxs-lookup"><span data-stu-id="c595d-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="c595d-115">Vælg **Projekt** &gt; **Opsætning** &gt; **Projektopsætning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c595d-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="c595d-116">Vælg en kalender, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="c595d-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="c595d-117">Du kan også angive standardprojekter for en ressource som en slags forhåndstildeling.</span><span class="sxs-lookup"><span data-stu-id="c595d-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="c595d-118">Forhåndstildelinger kan bruges, når ressourceledere eller projektleder på forhånd ved, hvilke projekter, som ressourcen skal arbejde på.</span><span class="sxs-lookup"><span data-stu-id="c595d-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="c595d-119">Forhåndstildelinger kan også være baseret på anmodningen fra en projektsponsor eller kunde.</span><span class="sxs-lookup"><span data-stu-id="c595d-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="c595d-120">Hvis du vil forhåndstildele et projekt, skal du på siden **Tildel projekter** under fanen **Projekter** i listen **Resterende projekter** vælge det relevante projekt.</span><span class="sxs-lookup"><span data-stu-id="c595d-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="c595d-121">Konfigurer en intern ressource</span><span class="sxs-lookup"><span data-stu-id="c595d-121">Set up an intercompany resource</span></span>

<span data-ttu-id="c595d-122">Når du konfigurerer en arbejder som en intern ressource, skal du fuldføre opsætningen i udlånsvirksomheden og den låntagende virksomhed.</span><span class="sxs-lookup"><span data-stu-id="c595d-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="c595d-123">I udlånsvirksomheden</span><span class="sxs-lookup"><span data-stu-id="c595d-123">In the lending company</span></span>

1. <span data-ttu-id="c595d-124">I Finance skal du kontrollere, at udlånsvirksomheden er valgt, og derefter fuldføre proceduren i forrige afsnit "Konfigurer en arbejder som en projektressource".</span><span class="sxs-lookup"><span data-stu-id="c595d-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="c595d-125">På siden **Internt regnskab** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c595d-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="c595d-126">I feltet **Juridisk enheds-id** skal du vælge udlånsvirksomheden.</span><span class="sxs-lookup"><span data-stu-id="c595d-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="c595d-127">Udfyld de resterende felter efter behov, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c595d-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="c595d-128">På siden **Overførelsespris** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c595d-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="c595d-129">I feltet **Juridisk låneenhed** skal du vælge den passende virksomhed.</span><span class="sxs-lookup"><span data-stu-id="c595d-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="c595d-130">Hvis du kun vil låne den låntagende virksomhed den ressource, som du oprettede i starten af denne sektion, skal du i feltet **Ressource** vælge navnet på den ressource, som du oprettede.</span><span class="sxs-lookup"><span data-stu-id="c595d-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="c595d-131">Lad feltet **Ressource** være tomt, hvis alle ressourcer i udlånsvirksomheden skal være tilgængelige for den låntagende virksomhed.</span><span class="sxs-lookup"><span data-stu-id="c595d-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="c595d-132">På siden **Projektstyring og regnskabsparametre** skal du under fanen **Internt** angive indstillingen **Aktiver planlægning af intern ressource og timesedler** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c595d-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="c595d-133">I den låntagende virksomhed</span><span class="sxs-lookup"><span data-stu-id="c595d-133">In the borrowing company</span></span>

- <span data-ttu-id="c595d-134">På siden **Ressourceliste** skal du i søgefiltret angive navnet på den ressource, som du oprettede til udlånsvirksomheden, for at verificere, at navnet er inkluderet i ressourcelisten for den låntagende virksomhed.</span><span class="sxs-lookup"><span data-stu-id="c595d-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="c595d-135">Anmod om projektressourcer</span><span class="sxs-lookup"><span data-stu-id="c595d-135">Request project resources</span></span>
<span data-ttu-id="c595d-136">Funktionaliteten i planlægningen af projektressourcer giver kun de ressourceansvarlige distribuere personaleressourcer til aftaler eller projekter.</span><span class="sxs-lookup"><span data-stu-id="c595d-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="c595d-137">Hvis du vil aktivere denne funktion, skal du udføre følgende opgaver eller kontrollere, at de er blevet fuldført:</span><span class="sxs-lookup"><span data-stu-id="c595d-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="c595d-138">Konfigurer nummerserier.</span><span class="sxs-lookup"><span data-stu-id="c595d-138">Set up number sequences.</span></span>
- <span data-ttu-id="c595d-139">Konfigurer arbejdsgange for projektstyring og regnskab.</span><span class="sxs-lookup"><span data-stu-id="c595d-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="c595d-140">Aktivér arbejdsprocesser for ressourceanmodninger.</span><span class="sxs-lookup"><span data-stu-id="c595d-140">Enable resource request workflows.</span></span>

<span data-ttu-id="c595d-141">Når de foregående opgaver er fuldført, kan du udføre følgende opgaver, som du har brug for:</span><span class="sxs-lookup"><span data-stu-id="c595d-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="c595d-142">Opret en ressourceanmodning på baggrund af en midlertidigt reserveret personaleressource.</span><span class="sxs-lookup"><span data-stu-id="c595d-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="c595d-143">Overvåg ressourceanmodninger.</span><span class="sxs-lookup"><span data-stu-id="c595d-143">Monitor resource requests.</span></span>
- <span data-ttu-id="c595d-144">Opfyld ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="c595d-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="c595d-145">Anmod om en personaleressource fra et WBS.</span><span class="sxs-lookup"><span data-stu-id="c595d-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="c595d-146">Reserver ressourcer til et projekt, uden at der skal anmodes om en personaleressource.</span><span class="sxs-lookup"><span data-stu-id="c595d-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]