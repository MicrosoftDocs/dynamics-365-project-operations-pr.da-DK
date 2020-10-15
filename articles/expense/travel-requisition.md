---
title: Rejserekvisitioner
description: Dette emne indeholder oplysninger om rejserekvisitioner.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906120"
---
# <a name="travel-requisitions"></a><span data-ttu-id="cc1db-103">Rejserekvisitioner</span><span class="sxs-lookup"><span data-stu-id="cc1db-103">Travel requisitions</span></span>

<span data-ttu-id="cc1db-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="cc1db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cc1db-105">En rejserekvisition viser de udgifter, der vil blive afholdt i forbindelse med rejsen.</span><span class="sxs-lookup"><span data-stu-id="cc1db-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="cc1db-106">En rejserekvisition er indsendt til gennemsyn og kan bruges til at autorisere udgifter.</span><span class="sxs-lookup"><span data-stu-id="cc1db-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="cc1db-107">Du skal muligvis indsende en rejserekvisition, før du afholder en eventuel udgift, der skal betales af organisationen.</span><span class="sxs-lookup"><span data-stu-id="cc1db-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="cc1db-108">Dette krav gælder, uanset om du opkræves udgifterne på et af firmaets kreditkort, betaler med kontanter, som du har modtaget fra et kontantforskud, eller afholder udgifter af egen lomme, som refunderes af organisationen.</span><span class="sxs-lookup"><span data-stu-id="cc1db-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="cc1db-109">Rejserekvisitioner og -politikker kan bruges til at administrere organisationens udgifter.</span><span class="sxs-lookup"><span data-stu-id="cc1db-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="cc1db-110">Hvis din organisation f.eks. arbejder på et fastprisprojekt, der kræver rejse, skal rejseudgifterne for projektets teammedlemmer være inden for projektbudgettet.</span><span class="sxs-lookup"><span data-stu-id="cc1db-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="cc1db-111">Ved at kræve, at rejseudgifter godkendes, før de afholdes, kan organisationen være med til at sikre, at projektet forbliver inden for budgettet.</span><span class="sxs-lookup"><span data-stu-id="cc1db-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="cc1db-112">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="cc1db-112">Configuration</span></span> 

<span data-ttu-id="cc1db-113">Rejserekvisitioner kan konfigureres som "obligatoriske" ved at aktivere parameteren "Forhåndsgodkendelse af rejser er obligatorisk" i parametrene for udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="cc1db-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="cc1db-114">Opret og indsend en rejserekvisition</span><span class="sxs-lookup"><span data-stu-id="cc1db-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="cc1db-115">Gå til **Mine udgifter: rejserekvisition**, og vælg **Ny rejserekvisition**.</span><span class="sxs-lookup"><span data-stu-id="cc1db-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="cc1db-116">Angiv et formål og en destination for rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="cc1db-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="cc1db-117">I feltet **Rejsebeskrivelse** skal du angive eventuelle yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="cc1db-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="cc1db-118">Opret et udgiftslinjeelement for hver af de forventede udgifter, f.eks. fly, måltider eller billeje.</span><span class="sxs-lookup"><span data-stu-id="cc1db-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="cc1db-119">Medtag den skønnede dato, beløb og valutaen for de enkelte udgifter.</span><span class="sxs-lookup"><span data-stu-id="cc1db-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="cc1db-120">Vælg **Gem**, når du er færdig med at tilføje de forventede udgifter.</span><span class="sxs-lookup"><span data-stu-id="cc1db-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="cc1db-121">Når du er klar til at indsende rejserekvisitionen, skal du vælge **Arbejdsproces** > **Indsend**.</span><span class="sxs-lookup"><span data-stu-id="cc1db-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="cc1db-122">Du kan få vist dine godkendte rejserekvisitioner under **Mine udgifter: rejserekvisition**.</span><span class="sxs-lookup"><span data-stu-id="cc1db-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="cc1db-123">Få vist tilgængelige rejserekvisitioner</span><span class="sxs-lookup"><span data-stu-id="cc1db-123">View available travel requisitions</span></span>

<span data-ttu-id="cc1db-124">Du kan få vist alle dine godkendte rejserekvisitioner under **Mine udgifter: rejserekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="cc1db-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="cc1db-125">Godkend rejserekvisitioner</span><span class="sxs-lookup"><span data-stu-id="cc1db-125">Approve travel requisitions</span></span>

<span data-ttu-id="cc1db-126">Vælg den rejserekvisition, du vil godkende, og vælg derefter **Arbejdsproces** > **Godkend**.</span><span class="sxs-lookup"><span data-stu-id="cc1db-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="cc1db-127">Indsend en udgiftsrapport ved hjælp af den godkendte rejserekvisition</span><span class="sxs-lookup"><span data-stu-id="cc1db-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="cc1db-128">Opret en ny udgiftsrapport og vælg i udgiftsrapportens overskrift, og fra listen over godkendte rejserekvisitioner **Tilknyt til rejserekvisition**.</span><span class="sxs-lookup"><span data-stu-id="cc1db-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="cc1db-129">Feltet **Rejserekvisitionsbeløb** opdateres automatisk i udgiftsrapportens overskrift.</span><span class="sxs-lookup"><span data-stu-id="cc1db-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="cc1db-130">Tilføj de omkostninger, der er påløbet under rejsen.</span><span class="sxs-lookup"><span data-stu-id="cc1db-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="cc1db-131">Hvis feltet **Forhåndsgodkendt** er aktiveret, opdateres det afstemte beløb og det godkendte beløb for den specifikke udgiftsart.</span><span class="sxs-lookup"><span data-stu-id="cc1db-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="cc1db-132">Når du tilknytter en udgiftsrapport til en godkendt rejserekvisition, kan transaktionsbeløbet ikke være større end det godkendte beløb.</span><span class="sxs-lookup"><span data-stu-id="cc1db-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
