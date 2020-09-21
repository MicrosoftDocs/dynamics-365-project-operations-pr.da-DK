---
title: Konfigurer standardomkostninger for arbejde og udgifter
description: I dette emne beskrives det, hvordan du kan konfigurere standardomkostninger for arbejdskraft og udgifter i et projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750636"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="6c43d-103">Konfigurer standardomkostninger for arbejde og udgifter</span><span class="sxs-lookup"><span data-stu-id="6c43d-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c43d-104">I dette emne beskrives det, hvordan du kan konfigurere standardomkostninger for arbejdskraft og udgifter i et projekt.</span><span class="sxs-lookup"><span data-stu-id="6c43d-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="6c43d-105">Denne opgave anvender datasættet USSI.</span><span class="sxs-lookup"><span data-stu-id="6c43d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6c43d-106">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (time)** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6c43d-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="6c43d-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-107">Select **New**.</span></span>
3. <span data-ttu-id="6c43d-108">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="6c43d-109">Angiv et nummer i feltet **Kostpris**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="6c43d-110">Du kan oprette en standardkostpris for projektkategorien, eller du kan konfigurere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en hvilken som helst kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="6c43d-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="6c43d-111">Den anvendte kostpris er kostprisen med det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="6c43d-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="6c43d-112">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-112">Select **Save**.</span></span>
6. <span data-ttu-id="6c43d-113">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (time)** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6c43d-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="6c43d-114">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-114">Select **New**.</span></span>
8. <span data-ttu-id="6c43d-115">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="6c43d-116">Vælg en indstilling i feltet **Gyldig til**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="6c43d-117">Angiv et nummer i feltet **Prisfastsættelse**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="6c43d-118">Du kan oprette en standardsalgspris for timetransaktioner eller for en projektkategori.</span><span class="sxs-lookup"><span data-stu-id="6c43d-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="6c43d-119">Du kan også konfigurere salgspriser pr. arbejdernummer, projektnummer, kategori, transaktionsdato eller en hvilken som helst kombination heraf.</span><span class="sxs-lookup"><span data-stu-id="6c43d-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="6c43d-120">Den faktiske salgspris, som anvendes, når en arbejder angiver en transaktion i timekladden, er den salgspris, der har det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="6c43d-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6c43d-121">Hvis du f.eks. både konfigurerer en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="6c43d-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="6c43d-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-122">Select **Save**.</span></span>
12. <span data-ttu-id="6c43d-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6c43d-123">Close the page.</span></span>
13. <span data-ttu-id="6c43d-124">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgifter)** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6c43d-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="6c43d-125">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-125">Select **New**.</span></span>
15. <span data-ttu-id="6c43d-126">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="6c43d-127">Angiv et nummer i feltet **Kostpris**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="6c43d-128">Det er muligt at udfylde flere felter, men dette er minimumskravet for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="6c43d-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="6c43d-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-129">Select **Save**.</span></span>
18. <span data-ttu-id="6c43d-130">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgifter)** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6c43d-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="6c43d-131">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-131">Select **New**.</span></span>
20. <span data-ttu-id="6c43d-132">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="6c43d-133">Vælg en indstilling i feltet **Gyldig til**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="6c43d-134">Angiv et nummer i feltet **Prisfastsættelse**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="6c43d-135">Den faktiske salgspris, som anvendes, når en arbejder angiver transaktioner i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="6c43d-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6c43d-136">Hvis du f.eks. både konfigurerer en generel og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="6c43d-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="6c43d-137">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c43d-137">Select **Save**.</span></span>

