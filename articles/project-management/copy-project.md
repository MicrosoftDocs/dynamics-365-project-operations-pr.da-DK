---
title: Kopiér et projekt
description: Dette emne indeholder oplysninger om kopiering af projekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908011"
---
# <a name="copy-a-project"></a><span data-ttu-id="69924-103">Kopiér et projekt</span><span class="sxs-lookup"><span data-stu-id="69924-103">Copy a project</span></span>

<span data-ttu-id="69924-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="69924-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="69924-105">Med Dynamics 365 Project Operations kan du hurtigt bygge nye projekter ved at bruge handlingen **Kopiér projekt** på formularen **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="69924-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="69924-106">Hvis du vil kopiere et projekt, skal du vælge et projekt og derefter vælge **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="69924-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="69924-107">Handlingen kopierer:</span><span class="sxs-lookup"><span data-stu-id="69924-107">The action will copy:</span></span>

- <span data-ttu-id="69924-108">Projektegenskaber</span><span class="sxs-lookup"><span data-stu-id="69924-108">Project properties</span></span>
- <span data-ttu-id="69924-109">Arbejdsopgavehierarkiet</span><span class="sxs-lookup"><span data-stu-id="69924-109">The Work breakdown structure</span></span>
- <span data-ttu-id="69924-110">Projektteamets medlemmer</span><span class="sxs-lookup"><span data-stu-id="69924-110">Project team members</span></span>
- <span data-ttu-id="69924-111">Projektestimater</span><span class="sxs-lookup"><span data-stu-id="69924-111">Project estimates</span></span>
- <span data-ttu-id="69924-112">Projektets udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="69924-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="69924-113">Projektegenskaber</span><span class="sxs-lookup"><span data-stu-id="69924-113">Project properties</span></span>

<span data-ttu-id="69924-114">Når projektet kopieres, kopieres værdierne i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="69924-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="69924-115">Navn</span><span class="sxs-lookup"><span data-stu-id="69924-115">Name</span></span>
- <span data-ttu-id="69924-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="69924-116">Description</span></span>
- <span data-ttu-id="69924-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="69924-117">Customer</span></span>
- <span data-ttu-id="69924-118">Kalenderskabelon</span><span class="sxs-lookup"><span data-stu-id="69924-118">Calendar Template</span></span>
- <span data-ttu-id="69924-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="69924-119">Currency</span></span>
- <span data-ttu-id="69924-120">Kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="69924-120">Contracting Unit</span></span>
- <span data-ttu-id="69924-121">Projektleder</span><span class="sxs-lookup"><span data-stu-id="69924-121">Project Manager</span></span>
- <span data-ttu-id="69924-122">Status</span><span class="sxs-lookup"><span data-stu-id="69924-122">Status</span></span>
- <span data-ttu-id="69924-123">Overordnet projektstatus</span><span class="sxs-lookup"><span data-stu-id="69924-123">Overall Project Status</span></span>
- <span data-ttu-id="69924-124">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="69924-124">Comments</span></span>
- <span data-ttu-id="69924-125">Estimater</span><span class="sxs-lookup"><span data-stu-id="69924-125">Estimates</span></span>
- <span data-ttu-id="69924-126">Anslået startdato</span><span class="sxs-lookup"><span data-stu-id="69924-126">Estimated Start Date</span></span>
- <span data-ttu-id="69924-127">Slutdato</span><span class="sxs-lookup"><span data-stu-id="69924-127">Finish Date</span></span>
- <span data-ttu-id="69924-128">Indsats (timer)</span><span class="sxs-lookup"><span data-stu-id="69924-128">Effort (Hours)</span></span>
- <span data-ttu-id="69924-129">Anslåede arbejdsomkostninger</span><span class="sxs-lookup"><span data-stu-id="69924-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="69924-130">Anslåede udgiftsomkostninger</span><span class="sxs-lookup"><span data-stu-id="69924-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="69924-131">Arbejdsopgavehierarki</span><span class="sxs-lookup"><span data-stu-id="69924-131">Work breakdown structure</span></span>

<span data-ttu-id="69924-132">Når projektet kopieres, kopieres hele det ressourceindlæste arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="69924-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="69924-133">Navngivne ressourcer erstattes med generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="69924-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="69924-134">Hvis de navngivne ressourcer ikke har samme arbejdstid som den generiske ressource, vil tidsplanen blive genberegnet, og opgavevarighederne kan blive ændret.</span><span class="sxs-lookup"><span data-stu-id="69924-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="69924-135">Projektteamets medlemmer</span><span class="sxs-lookup"><span data-stu-id="69924-135">Project team members</span></span>

<span data-ttu-id="69924-136">Når et projektteam kopieres fra kildeprojektet, kopieres de generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="69924-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="69924-137">Standardressourcetildelinger bevares også, som de var, i kildeprojektet.</span><span class="sxs-lookup"><span data-stu-id="69924-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="69924-138">Navngivne ressourcer konverteres til generiske teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="69924-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="69924-139">Estimater</span><span class="sxs-lookup"><span data-stu-id="69924-139">Estimates</span></span>

<span data-ttu-id="69924-140">Når projektet kopieres, kopieres både ressource- og udgiftsestimatlinjer fra kildeprojektet.</span><span class="sxs-lookup"><span data-stu-id="69924-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>