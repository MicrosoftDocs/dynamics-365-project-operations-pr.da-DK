---
title: Konfigurer projektkategorier
description: Dette emne indeholder oplysninger om opsætning af projektkategorier.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895959"
---
# <a name="configure-project-categories"></a><span data-ttu-id="da5b8-103">Konfigurer projektkategorier</span><span class="sxs-lookup"><span data-stu-id="da5b8-103">Configure project categories</span></span>

<span data-ttu-id="da5b8-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="da5b8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="da5b8-105">Project Operations tilbyder effektive funktioner til kategorisering af indtægter og udgifter på projekter.</span><span class="sxs-lookup"><span data-stu-id="da5b8-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="da5b8-106">Kategorier giver mulighed for at rapportere og analysere projekttransaktioner og oprette en rapport, der skal bogføres i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="da5b8-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="da5b8-107">I følgende diagram illustreres korrelationen mellem transaktionskategorier, delte kategorier og projektkategorier.</span><span class="sxs-lookup"><span data-stu-id="da5b8-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="da5b8-108">Transaktionskategorier er den grundlæggende gruppering for projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="da5b8-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="da5b8-109">I denne gruppering findes der et sæt delte kategorier, som kan deles på tværs af programmer og moduler.</span><span class="sxs-lookup"><span data-stu-id="da5b8-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="da5b8-110">Mere dybdegående er projektkategorier det mest detaljerede niveau for kategorier.</span><span class="sxs-lookup"><span data-stu-id="da5b8-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="da5b8-111">Projektkategorier er specifikke for en juridisk enhed, et modul og program.</span><span class="sxs-lookup"><span data-stu-id="da5b8-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korrelationen mellem transaktionskategorier, delte kategorier og projektkategorier](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="da5b8-113">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="da5b8-113">Transaction categories</span></span>

<span data-ttu-id="da5b8-114">Transaktionskategorier repræsenterer den grundlæggende gruppering for projekttransaktioner og er ikke virksomheds- eller transaktionstypespecifikke.</span><span class="sxs-lookup"><span data-stu-id="da5b8-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="da5b8-115">Contoso Robotics bruger f.eks. design-, rejse-, installations- og servicetransaktionskategorier til at gruppere projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="da5b8-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="da5b8-116">Transaktionskategorier defineres i Project Operations-modulet.</span><span class="sxs-lookup"><span data-stu-id="da5b8-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="da5b8-117">Gå til **Indstillinger** \> **Transaktionskategorier** for at åbne formularen.</span><span class="sxs-lookup"><span data-stu-id="da5b8-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="da5b8-118">Opret en ny transaktionskategori ved enten at vælge **Ny** eller ved at vælge **Importér fra Excel**.</span><span class="sxs-lookup"><span data-stu-id="da5b8-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="da5b8-119">Delte kategorier</span><span class="sxs-lookup"><span data-stu-id="da5b8-119">Shared categories</span></span>

<span data-ttu-id="da5b8-120">I Dynamics 365 bruges begrebet Delte kategorier til at kategorisere udgifter i forskellige programmer, f.eks Dynamics 365 Finance, Dynamics 365 Supply Chain og Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="da5b8-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="da5b8-121">For hver oprettet transaktionskategori opretter Project Operations automatisk fire relaterede delte kategorier: timer, udgifter, gebyrer og varer.</span><span class="sxs-lookup"><span data-stu-id="da5b8-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="da5b8-122">Du kan gennemse og justere de delte kategorier ved at gå til **Projektstyring og regnskab** \> **Opsætning** \> **Kategorier** \> **Delte kategorier**.</span><span class="sxs-lookup"><span data-stu-id="da5b8-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="da5b8-123">Projektkategorier</span><span class="sxs-lookup"><span data-stu-id="da5b8-123">Project categories</span></span>

<span data-ttu-id="da5b8-124">Projektkategorier repræsenterer det mest detaljerede niveau for kategorikonfiguration og skal konfigureres separat og for hvert enkelt firma af en projektbogholder.</span><span class="sxs-lookup"><span data-stu-id="da5b8-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="da5b8-125">Gå til **Projektstyring og regnskab** \> **Opsætning** \> **Kategorier** \> **Projektkategorier**.</span><span class="sxs-lookup"><span data-stu-id="da5b8-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="da5b8-126">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="da5b8-126">Select **New**.</span></span>
3. <span data-ttu-id="da5b8-127">Vælg **Kategori-id** for den delte kategori, du har oprettet i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="da5b8-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="da5b8-128">Project Operations gør det kun muligt at bruge de delte kategorier, der er knyttet til transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="da5b8-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="da5b8-129">Vælg en kategorigruppe.</span><span class="sxs-lookup"><span data-stu-id="da5b8-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="da5b8-130">Kategorigrupper</span><span class="sxs-lookup"><span data-stu-id="da5b8-130">Category groups</span></span>

<span data-ttu-id="da5b8-131">Kategorigrupper bruges til at dele egenskaber, primært posteringsprofiler, mellem relaterede projektkategorier.</span><span class="sxs-lookup"><span data-stu-id="da5b8-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="da5b8-132">Der skal være mindst én kategorigruppe for hver enkelt transaktionstype, og hver enkelt projektkategori tildeles en gruppe.</span><span class="sxs-lookup"><span data-stu-id="da5b8-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="da5b8-133">Bogføringsspecifikationerne i Project Operations er defineret i reglerne for projektomkostnings- og indtægtsprofil, projektkategorier og kategorigrupper.</span><span class="sxs-lookup"><span data-stu-id="da5b8-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="da5b8-134">Du kan oprette kategorigrupper ved at gå til **Projektstyring og regnskab** \> **Opsætning** \> **Kategorier** \> **Kategorigrupper**.</span><span class="sxs-lookup"><span data-stu-id="da5b8-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
