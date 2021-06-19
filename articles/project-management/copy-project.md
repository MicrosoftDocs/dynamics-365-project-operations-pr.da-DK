---
title: Kopiér et projekt
description: Dette emne indeholder oplysninger om kopiering af projekter i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091247"
---
# <a name="copy-a-project"></a><span data-ttu-id="9e27a-103">Kopiér et projekt</span><span class="sxs-lookup"><span data-stu-id="9e27a-103">Copy a project</span></span>

<span data-ttu-id="9e27a-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="9e27a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e27a-105">Ved hjælp af Dynamics 365 Project Operations kan du hurtigt oprette nye projekter ved at vælge **Kopiér projekt** i formularen **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="9e27a-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="9e27a-106">Hvis du vil kopiere et projekt, skal du åbne det projekt, du vil kopiere, og derefter vælge **Kopiér projekt**.</span><span class="sxs-lookup"><span data-stu-id="9e27a-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="9e27a-107">Handlingen kopierer følgende:</span><span class="sxs-lookup"><span data-stu-id="9e27a-107">The action will copy the following:</span></span>

- <span data-ttu-id="9e27a-108">Projektegenskaber</span><span class="sxs-lookup"><span data-stu-id="9e27a-108">Project properties</span></span> 
- <span data-ttu-id="9e27a-109">Arbejdsopgavehierarki</span><span class="sxs-lookup"><span data-stu-id="9e27a-109">Work breakdown structure</span></span>
- <span data-ttu-id="9e27a-110">Projektteamets medlemmer</span><span class="sxs-lookup"><span data-stu-id="9e27a-110">Project team members</span></span>
- <span data-ttu-id="9e27a-111">Projektestimater</span><span class="sxs-lookup"><span data-stu-id="9e27a-111">Project estimates</span></span>
- <span data-ttu-id="9e27a-112">Projektets udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="9e27a-112">Project expense estimates</span></span>
- <span data-ttu-id="9e27a-113">Projektmaterialeestimater</span><span class="sxs-lookup"><span data-stu-id="9e27a-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="9e27a-114">Projektegenskaber</span><span class="sxs-lookup"><span data-stu-id="9e27a-114">Project properties</span></span>

<span data-ttu-id="9e27a-115">Når projektet kopieres, kopieres værdierne i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="9e27a-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="9e27a-116">Navn</span><span class="sxs-lookup"><span data-stu-id="9e27a-116">Name</span></span>
- <span data-ttu-id="9e27a-117">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9e27a-117">Description</span></span>
- <span data-ttu-id="9e27a-118">Kunde</span><span class="sxs-lookup"><span data-stu-id="9e27a-118">Customer</span></span>
- <span data-ttu-id="9e27a-119">Kalenderskabelon</span><span class="sxs-lookup"><span data-stu-id="9e27a-119">Calendar Template</span></span>
- <span data-ttu-id="9e27a-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="9e27a-120">Currency</span></span>
- <span data-ttu-id="9e27a-121">Kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="9e27a-121">Contracting Unit</span></span>
- <span data-ttu-id="9e27a-122">Projektleder</span><span class="sxs-lookup"><span data-stu-id="9e27a-122">Project Manager</span></span>
- <span data-ttu-id="9e27a-123">Status</span><span class="sxs-lookup"><span data-stu-id="9e27a-123">Status</span></span>
- <span data-ttu-id="9e27a-124">Overordnet projektstatus</span><span class="sxs-lookup"><span data-stu-id="9e27a-124">Overall Project Status</span></span>
- <span data-ttu-id="9e27a-125">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="9e27a-125">Comments</span></span>
- <span data-ttu-id="9e27a-126">Estimater</span><span class="sxs-lookup"><span data-stu-id="9e27a-126">Estimates</span></span>
- <span data-ttu-id="9e27a-127">Anslået startdato: Datoen, hvor projektet oprettes ud fra kopien.</span><span class="sxs-lookup"><span data-stu-id="9e27a-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="9e27a-128">Anslået slutdato: Denne dato justeres på baggrund af startdatoen for det nye projekt, der blev oprettet på baggrund af kopien.</span><span class="sxs-lookup"><span data-stu-id="9e27a-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="9e27a-129">Indsats (timer)</span><span class="sxs-lookup"><span data-stu-id="9e27a-129">Effort (Hours)</span></span>
- <span data-ttu-id="9e27a-130">Anslåede arbejdsomkostninger</span><span class="sxs-lookup"><span data-stu-id="9e27a-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="9e27a-131">Anslåede udgiftsomkostninger</span><span class="sxs-lookup"><span data-stu-id="9e27a-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="9e27a-132">Anslåede materialeomkostninger</span><span class="sxs-lookup"><span data-stu-id="9e27a-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="9e27a-133">Kopiér projekt er en langvarig handling.</span><span class="sxs-lookup"><span data-stu-id="9e27a-133">Copy project is a long running operation.</span></span> <span data-ttu-id="9e27a-134">Projektposter, deres relevante attributter og mange relaterede objekter kopieres også.</span><span class="sxs-lookup"><span data-stu-id="9e27a-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="9e27a-135">På grund af handlingens langvarige karakteristika er destinationsprojektsiden låst til redigering, når kopien er startet, og indtil kopieringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="9e27a-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="9e27a-136">Arbejdsopgavehierarki</span><span class="sxs-lookup"><span data-stu-id="9e27a-136">Work breakdown structure</span></span>

<span data-ttu-id="9e27a-137">Når projektet kopieres, kopieres hele det ressourceindlæste arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="9e27a-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="9e27a-138">Navngivne ressourcer erstattes med generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="9e27a-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="9e27a-139">Hvis de navngivne ressourcer ikke har samme arbejdstid som den generiske ressource, vil tidsplanen blive genberegnet, og opgavevarighederne kan blive ændret.</span><span class="sxs-lookup"><span data-stu-id="9e27a-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="9e27a-140">Projektteamets medlemmer</span><span class="sxs-lookup"><span data-stu-id="9e27a-140">Project team members</span></span>

<span data-ttu-id="9e27a-141">Når et projektteam kopieres fra kildeprojektet, kopieres de generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="9e27a-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="9e27a-142">Standardressourcetildelinger bevares også, som de var, i kildeprojektet.</span><span class="sxs-lookup"><span data-stu-id="9e27a-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="9e27a-143">Navngivne ressourcer konverteres til generiske teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="9e27a-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="9e27a-144">Estimater</span><span class="sxs-lookup"><span data-stu-id="9e27a-144">Estimates</span></span>

<span data-ttu-id="9e27a-145">Når projektet kopieres, kopieres ressource-, udgifts- og materialeestimatlinjer fra kildeprojektet.</span><span class="sxs-lookup"><span data-stu-id="9e27a-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="9e27a-146">Oplysninger om, hvordan du får adgang til Kopier projekt via programmering, finder du under [Udvikling af projektskabeloner med Kopier projekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="9e27a-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
