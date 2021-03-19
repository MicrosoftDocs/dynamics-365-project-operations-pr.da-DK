---
title: Kopiér et projekt
description: Dette emne indeholder oplysninger om kopiering af projekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479512"
---
# <a name="copy-a-project"></a><span data-ttu-id="c90c2-103">Kopiér et projekt</span><span class="sxs-lookup"><span data-stu-id="c90c2-103">Copy a project</span></span>

<span data-ttu-id="c90c2-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c90c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c90c2-105">Ved hjælp af Dynamics 365 Project Operations kan du hurtigt oprette nye projekter ved at vælge **Kopiér projekt** i formularen **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="c90c2-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="c90c2-106">Hvis du vil kopiere et projekt, skal du åbne det projekt, du vil kopiere, og derefter vælge **Kopiér projekt**.</span><span class="sxs-lookup"><span data-stu-id="c90c2-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="c90c2-107">Handlingen kopierer:</span><span class="sxs-lookup"><span data-stu-id="c90c2-107">The action will copy:</span></span>

- <span data-ttu-id="c90c2-108">Projektegenskaber (den anslåede startdato kopieres fra kildeprojektet)</span><span class="sxs-lookup"><span data-stu-id="c90c2-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="c90c2-109">Arbejdsopgavehierarkiet</span><span class="sxs-lookup"><span data-stu-id="c90c2-109">The Work breakdown structure</span></span>
- <span data-ttu-id="c90c2-110">Projektteamets medlemmer</span><span class="sxs-lookup"><span data-stu-id="c90c2-110">Project team members</span></span>
- <span data-ttu-id="c90c2-111">Projektestimater</span><span class="sxs-lookup"><span data-stu-id="c90c2-111">Project estimates</span></span>
- <span data-ttu-id="c90c2-112">Projektets udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="c90c2-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="c90c2-113">Projektegenskaber</span><span class="sxs-lookup"><span data-stu-id="c90c2-113">Project properties</span></span>

<span data-ttu-id="c90c2-114">Når projektet kopieres, kopieres værdierne i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="c90c2-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="c90c2-115">Navn</span><span class="sxs-lookup"><span data-stu-id="c90c2-115">Name</span></span>
- <span data-ttu-id="c90c2-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c90c2-116">Description</span></span>
- <span data-ttu-id="c90c2-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="c90c2-117">Customer</span></span>
- <span data-ttu-id="c90c2-118">Kalenderskabelon</span><span class="sxs-lookup"><span data-stu-id="c90c2-118">Calendar Template</span></span>
- <span data-ttu-id="c90c2-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="c90c2-119">Currency</span></span>
- <span data-ttu-id="c90c2-120">Kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="c90c2-120">Contracting Unit</span></span>
- <span data-ttu-id="c90c2-121">Projektleder</span><span class="sxs-lookup"><span data-stu-id="c90c2-121">Project Manager</span></span>
- <span data-ttu-id="c90c2-122">Status</span><span class="sxs-lookup"><span data-stu-id="c90c2-122">Status</span></span>
- <span data-ttu-id="c90c2-123">Overordnet projektstatus</span><span class="sxs-lookup"><span data-stu-id="c90c2-123">Overall Project Status</span></span>
- <span data-ttu-id="c90c2-124">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="c90c2-124">Comments</span></span>
- <span data-ttu-id="c90c2-125">Estimater</span><span class="sxs-lookup"><span data-stu-id="c90c2-125">Estimates</span></span>
- <span data-ttu-id="c90c2-126">Anslået startdato</span><span class="sxs-lookup"><span data-stu-id="c90c2-126">Estimated Start Date</span></span>
- <span data-ttu-id="c90c2-127">Slutdato</span><span class="sxs-lookup"><span data-stu-id="c90c2-127">Finish Date</span></span>
- <span data-ttu-id="c90c2-128">Indsats (timer)</span><span class="sxs-lookup"><span data-stu-id="c90c2-128">Effort (Hours)</span></span>
- <span data-ttu-id="c90c2-129">Anslåede arbejdsomkostninger</span><span class="sxs-lookup"><span data-stu-id="c90c2-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="c90c2-130">Anslåede udgiftsomkostninger</span><span class="sxs-lookup"><span data-stu-id="c90c2-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="c90c2-131">Arbejdsopgavehierarki</span><span class="sxs-lookup"><span data-stu-id="c90c2-131">Work breakdown structure</span></span>

<span data-ttu-id="c90c2-132">Når projektet kopieres, kopieres hele det ressourceindlæste arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="c90c2-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="c90c2-133">Navngivne ressourcer erstattes med generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c90c2-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="c90c2-134">Hvis de navngivne ressourcer ikke har samme arbejdstid som den generiske ressource, vil tidsplanen blive genberegnet, og opgavevarighederne kan blive ændret.</span><span class="sxs-lookup"><span data-stu-id="c90c2-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="c90c2-135">Projektteamets medlemmer</span><span class="sxs-lookup"><span data-stu-id="c90c2-135">Project team members</span></span>

<span data-ttu-id="c90c2-136">Når et projektteam kopieres fra kildeprojektet, kopieres de generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c90c2-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="c90c2-137">Standardressourcetildelinger bevares også, som de var, i kildeprojektet.</span><span class="sxs-lookup"><span data-stu-id="c90c2-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="c90c2-138">Navngivne ressourcer konverteres til generiske teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="c90c2-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="c90c2-139">Estimater</span><span class="sxs-lookup"><span data-stu-id="c90c2-139">Estimates</span></span>

<span data-ttu-id="c90c2-140">Når projektet kopieres, kopieres både ressource- og udgiftsestimatlinjer fra kildeprojektet.</span><span class="sxs-lookup"><span data-stu-id="c90c2-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="c90c2-141">Oplysninger om, hvordan du får adgang til Kopier projekt via programmering, finder du under [Udvikling af projektskabeloner med Kopier projekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="c90c2-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
