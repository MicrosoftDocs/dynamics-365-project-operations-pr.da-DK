---
title: Konfigurer udgiftskategorier
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere udgiftskategorier og delte kategorier for udgiftsrapporter.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074062"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="14ed2-103">Konfigurer udgiftskategorier</span><span class="sxs-lookup"><span data-stu-id="14ed2-103">Set up expense categories</span></span>

<span data-ttu-id="14ed2-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="14ed2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="14ed2-105">Når medarbejdere opretter udgiftsrapporter, skal hver enkelt udgift, de registrerer, være knyttet til en udgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="14ed2-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="14ed2-106">Udgiftskategorier afledes af delte kategorier, der kan deles på tværs af de juridiske enheder i organisationen.</span><span class="sxs-lookup"><span data-stu-id="14ed2-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="14ed2-107">Afhængigt af, hvordan organisationen er defineret, kan disse udgiftskategorier også deles i andre områder.</span><span class="sxs-lookup"><span data-stu-id="14ed2-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="14ed2-108">Afhængigt af definitionen af din organisation og vejledning fra implementeringsteamet skal du afgøre, om de kategorier, der bruges i udgiftsstyring, kun skal bruges i udgiftsstyring eller skal deles i andre områder.</span><span class="sxs-lookup"><span data-stu-id="14ed2-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="14ed2-109">Disse kategorier kan deles mellem projektstyring og regnskab samt udgiftsstyring eller mellem projektstyring og regnskab og produktion.</span><span class="sxs-lookup"><span data-stu-id="14ed2-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="14ed2-110">De kan dog ikke deles mellem udgiftsstyring og produktion.</span><span class="sxs-lookup"><span data-stu-id="14ed2-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="14ed2-111">Før du kan gå i gang med konfigurationsprocessen, skal der træffes følgende beslutninger for de enkelte udgiftskategorier:</span><span class="sxs-lookup"><span data-stu-id="14ed2-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="14ed2-112">Hvad er udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="14ed2-112">What is the expense category?</span></span> <span data-ttu-id="14ed2-113">Som eksempel kan nævnes kategorier for fly, hotel eller kørsel.</span><span class="sxs-lookup"><span data-stu-id="14ed2-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="14ed2-114">Kan udgiftskategorien også bruges i projektstyring og regnskab?</span><span class="sxs-lookup"><span data-stu-id="14ed2-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="14ed2-115">Det kan den, hvis du også træffer følgende beslutninger:</span><span class="sxs-lookup"><span data-stu-id="14ed2-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="14ed2-116">Hvilke omkostningskonti skal bruges til følgende udgifter?</span><span class="sxs-lookup"><span data-stu-id="14ed2-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="14ed2-117">Omkostning</span><span class="sxs-lookup"><span data-stu-id="14ed2-117">Cost</span></span>
        - <span data-ttu-id="14ed2-118">Lønfordeling</span><span class="sxs-lookup"><span data-stu-id="14ed2-118">Payroll allocation</span></span>
        - <span data-ttu-id="14ed2-119">Værdi af omkostningerne ved IGVA</span><span class="sxs-lookup"><span data-stu-id="14ed2-119">WIP-cost value</span></span>
        - <span data-ttu-id="14ed2-120">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="14ed2-120">Cost-item</span></span>
        - <span data-ttu-id="14ed2-121">Værdielement for omkostning ved IGVA</span><span class="sxs-lookup"><span data-stu-id="14ed2-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="14ed2-122">Periodiseret tab</span><span class="sxs-lookup"><span data-stu-id="14ed2-122">Accrued loss</span></span>
        - <span data-ttu-id="14ed2-123">Periodiseret tab for IGVA</span><span class="sxs-lookup"><span data-stu-id="14ed2-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="14ed2-124">Hvilke omsætningskonti skal der bruges til følgende omsætningskilder?</span><span class="sxs-lookup"><span data-stu-id="14ed2-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="14ed2-125">Faktureret omsætning</span><span class="sxs-lookup"><span data-stu-id="14ed2-125">Invoiced revenue</span></span>
        - <span data-ttu-id="14ed2-126">Periodiseret omsætning - salgsværdi</span><span class="sxs-lookup"><span data-stu-id="14ed2-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="14ed2-127">IGVA - salgsværdi</span><span class="sxs-lookup"><span data-stu-id="14ed2-127">WIP-sales value</span></span>
        - <span data-ttu-id="14ed2-128">Periodiseret omsætning - produktion</span><span class="sxs-lookup"><span data-stu-id="14ed2-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="14ed2-129">IGVA - produktion</span><span class="sxs-lookup"><span data-stu-id="14ed2-129">WIP-production</span></span>
        - <span data-ttu-id="14ed2-130">Periodiseret omsætning - overskud</span><span class="sxs-lookup"><span data-stu-id="14ed2-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="14ed2-131">IGVA - overskud</span><span class="sxs-lookup"><span data-stu-id="14ed2-131">WIP-profit</span></span>
        - <span data-ttu-id="14ed2-132">Periodiseret omsætning - abonnement</span><span class="sxs-lookup"><span data-stu-id="14ed2-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="14ed2-133">IGVA - abonnement</span><span class="sxs-lookup"><span data-stu-id="14ed2-133">WIP-subscription</span></span>

- <span data-ttu-id="14ed2-134">Hvad er udgiftstypen?</span><span class="sxs-lookup"><span data-stu-id="14ed2-134">What is the expense type?</span></span>
- <span data-ttu-id="14ed2-135">Hvad er standardbetalingsmetoden for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="14ed2-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="14ed2-136">Skal udgifter i udgiftskategorien specificeres?</span><span class="sxs-lookup"><span data-stu-id="14ed2-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="14ed2-137">Hvad er den primære standardkonto for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="14ed2-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="14ed2-138">Hvad er standardvaremomsgruppen for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="14ed2-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="14ed2-139">Er yderligere betalingsmetoder for udgiftskategorien tilladt?</span><span class="sxs-lookup"><span data-stu-id="14ed2-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="14ed2-140">Hvis det er tilfældet, hvilke?</span><span class="sxs-lookup"><span data-stu-id="14ed2-140">If so, what are they?</span></span>
- <span data-ttu-id="14ed2-141">Er der underkategorier i denne udgiftskategori?</span><span class="sxs-lookup"><span data-stu-id="14ed2-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="14ed2-142">I så fald skal du også træffer følgende beslutninger:</span><span class="sxs-lookup"><span data-stu-id="14ed2-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="14ed2-143">Er nogen af underkategorierne undtaget fra momsopkrævning?</span><span class="sxs-lookup"><span data-stu-id="14ed2-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="14ed2-144">Hvad er varemomsgruppen for underkategorierne?</span><span class="sxs-lookup"><span data-stu-id="14ed2-144">What is the item sales tax group of the subcategories?</span></span>
