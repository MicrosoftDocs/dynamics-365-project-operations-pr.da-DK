---
title: Planlægningstilstande
description: Dette emne indeholder oplysninger om planlægningstilstande.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116700"
---
# <a name="scheduling-modes"></a><span data-ttu-id="b36a2-103">Planlægningstilstande</span><span class="sxs-lookup"><span data-stu-id="b36a2-103">Scheduling modes</span></span>

<span data-ttu-id="b36a2-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b36a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b36a2-105">Dynamics 365 Project Operations giver organisationer muligheden for at definere, hvordan de administrerer ændringer af nøglevariabler i arbejdsopgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="b36a2-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="b36a2-106">Projektledere kan på baggrund af organisationens specifikke behov foretage ændringer af planlægningstilstanden, når der oprettes et projekt.</span><span class="sxs-lookup"><span data-stu-id="b36a2-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="b36a2-107">Der findes tre planlægningstilstande i Project Operations:</span><span class="sxs-lookup"><span data-stu-id="b36a2-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="b36a2-108">Fast varighed (dette er standardtilstanden)</span><span class="sxs-lookup"><span data-stu-id="b36a2-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="b36a2-109">Fast indsats (*Arbejde*)</span><span class="sxs-lookup"><span data-stu-id="b36a2-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="b36a2-110">Faste enheder</span><span class="sxs-lookup"><span data-stu-id="b36a2-110">Fixed units</span></span>

<span data-ttu-id="b36a2-111">De værdier, der påvirkes af definitionen af en bestemt planlægningstilstand, bestemmes af følgende formel:</span><span class="sxs-lookup"><span data-stu-id="b36a2-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="b36a2-112">Indsats = Varighed x Enheder</span><span class="sxs-lookup"><span data-stu-id="b36a2-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="b36a2-113">Når du definerer et projekts planlægningstilstand, angiver du en af disse værdier, som derefter ikke kan ændres.</span><span class="sxs-lookup"><span data-stu-id="b36a2-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="b36a2-114">Fastholdelse af værdi som en konstant medfører, at den værdi skal prioriteres, hvilket giver systemet besked om, at den ikke skal ændres, når de to andre værdier ændres.</span><span class="sxs-lookup"><span data-stu-id="b36a2-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="b36a2-115">Følgende tabel indeholder oplysninger om, hvordan det påvirker valget af en bestemt tilstand.</span><span class="sxs-lookup"><span data-stu-id="b36a2-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="b36a2-116">**I denne opgave**</span><span class="sxs-lookup"><span data-stu-id="b36a2-116">**In this task**</span></span>             | <span data-ttu-id="b36a2-117">**Hvis du reviderer enheder**</span><span class="sxs-lookup"><span data-stu-id="b36a2-117">**If you revise units**</span></span>   | <span data-ttu-id="b36a2-118">**Hvis du reviderer varigheden**</span><span class="sxs-lookup"><span data-stu-id="b36a2-118">**If you revise duration**</span></span> | <span data-ttu-id="b36a2-119">**Hvis du reviderer indsatsen**</span><span class="sxs-lookup"><span data-stu-id="b36a2-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="b36a2-120">Fast enhedsopgave</span><span class="sxs-lookup"><span data-stu-id="b36a2-120">Fixed units task</span></span>     | <span data-ttu-id="b36a2-121">Varigheden genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-121">Duration is recalculated.</span></span> | <span data-ttu-id="b36a2-122">Indsatsen genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-122">Effort is recalculated.</span></span>    | <span data-ttu-id="b36a2-123">Varigheden genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="b36a2-124">Fast indsatsopgave</span><span class="sxs-lookup"><span data-stu-id="b36a2-124">Fixed effort task</span></span>    | <span data-ttu-id="b36a2-125">Varigheden genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-125">Duration is recalculated.</span></span> | <span data-ttu-id="b36a2-126">Enheder genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-126">Units are recalculated.</span></span>    | <span data-ttu-id="b36a2-127">Varigheden genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="b36a2-128">Fast varighedsopgave</span><span class="sxs-lookup"><span data-stu-id="b36a2-128">Fixed duration task</span></span>  | <span data-ttu-id="b36a2-129">Indsatsen genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-129">Effort is recalculated.</span></span>   | <span data-ttu-id="b36a2-130">Indsatsen genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-130">Effort is recalculated.</span></span>    | <span data-ttu-id="b36a2-131">Enheder genberegnes.</span><span class="sxs-lookup"><span data-stu-id="b36a2-131">Units are recalculated.</span></span>   |

<span data-ttu-id="b36a2-132">Du kan finde flere oplysninger om konsekvenserne af en bestemt tilstand under [Ændring af opgavetypen for at opnå en mere nøjagtig planlægning](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="b36a2-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="b36a2-133">I emnet bruges udtrykket **Arbejde** i stedet for **Indsats**.</span><span class="sxs-lookup"><span data-stu-id="b36a2-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="b36a2-134">Ændre organisationens planlægningstilstand</span><span class="sxs-lookup"><span data-stu-id="b36a2-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="b36a2-135">Udfør følgende trin for at definere planlægningstilstanden for en organisation.</span><span class="sxs-lookup"><span data-stu-id="b36a2-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="b36a2-136">Gå til **Indstillinger** \> **Generelt** \> **Parametre**, og vælg derefter projektparameteren.</span><span class="sxs-lookup"><span data-stu-id="b36a2-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="b36a2-137">På siden **Projektparametre** skal du vælge standardplanlægningstilstanden for organisationen og derefter definere projektlederens mulighed for at tilsidesætte indstillingen under oprettelsen af et nyt projekt.</span><span class="sxs-lookup"><span data-stu-id="b36a2-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="b36a2-138">Ændr planlægningstilstandsindstillingen for et projekt</span><span class="sxs-lookup"><span data-stu-id="b36a2-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="b36a2-139">Hvis en organisation tillader projektlederen at tilsidesætte standardplanlægningstilstanden, kan projektlederen foretage denne ændring, når vedkommende opretter et nyt projekt.</span><span class="sxs-lookup"><span data-stu-id="b36a2-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="b36a2-140">Men når projektet er gemt, kan planlægningstilstanden ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="b36a2-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="b36a2-141">Kopierede projekter</span><span class="sxs-lookup"><span data-stu-id="b36a2-141">Copied projects</span></span>

<span data-ttu-id="b36a2-142">Da der oprettes et projekt, når kopien af projekthandlingen foretages, kan projektlederen ikke angive planlægningstilstanden.</span><span class="sxs-lookup"><span data-stu-id="b36a2-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="b36a2-143">Destinationsprojektet vil altid være standard for den tilstand, der er defineret på organisationsniveau.</span><span class="sxs-lookup"><span data-stu-id="b36a2-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="b36a2-144">Kopierede opgaver</span><span class="sxs-lookup"><span data-stu-id="b36a2-144">Copied tasks</span></span>

<span data-ttu-id="b36a2-145">Når en opgave kopieres fra et projekt til et andet, arver opgaven planlægningstilstanden for destinationsprojektet.</span><span class="sxs-lookup"><span data-stu-id="b36a2-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
