---
title: Konfigurer standardomkostninger for arbejde og udgifter
description: I dette emne beskrives det, hvordan du kan konfigurere standardomkostninger for arbejdskraft og udgifter i et projekt.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 517e5ae776cff18aec81e5446a7aaedfba61ac0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011004"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="92329-103">Konfigurer standardomkostninger for arbejde og udgifter</span><span class="sxs-lookup"><span data-stu-id="92329-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92329-104">I dette emne beskrives det, hvordan du kan konfigurere standardomkostninger for arbejdskraft og udgifter i et projekt.</span><span class="sxs-lookup"><span data-stu-id="92329-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="92329-105">Denne opgave anvender datasættet USSI.</span><span class="sxs-lookup"><span data-stu-id="92329-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="92329-106">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (time)** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="92329-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="92329-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="92329-107">Select **New**.</span></span>
3. <span data-ttu-id="92329-108">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="92329-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="92329-109">Angiv et nummer i feltet **Kostpris**.</span><span class="sxs-lookup"><span data-stu-id="92329-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="92329-110">Du kan oprette en standardkostpris for projektkategorien, eller du kan konfigurere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en hvilken som helst kombination af disse.</span><span class="sxs-lookup"><span data-stu-id="92329-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="92329-111">Den anvendte kostpris er kostprisen med det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="92329-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="92329-112">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="92329-112">Select **Save**.</span></span>
6. <span data-ttu-id="92329-113">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (time)** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="92329-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="92329-114">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="92329-114">Select **New**.</span></span>
8. <span data-ttu-id="92329-115">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="92329-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="92329-116">Vælg en indstilling i feltet **Gyldig til**.</span><span class="sxs-lookup"><span data-stu-id="92329-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="92329-117">Angiv et nummer i feltet **Prisfastsættelse**.</span><span class="sxs-lookup"><span data-stu-id="92329-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="92329-118">Du kan oprette en standardsalgspris for timetransaktioner eller for en projektkategori.</span><span class="sxs-lookup"><span data-stu-id="92329-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="92329-119">Du kan også konfigurere salgspriser pr. arbejdernummer, projektnummer, kategori, transaktionsdato eller en hvilken som helst kombination heraf.</span><span class="sxs-lookup"><span data-stu-id="92329-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="92329-120">Den faktiske salgspris, som anvendes, når en arbejder angiver en transaktion i timekladden, er den salgspris, der har det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="92329-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="92329-121">Hvis du f.eks. både konfigurerer en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="92329-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="92329-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="92329-122">Select **Save**.</span></span>
12. <span data-ttu-id="92329-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="92329-123">Close the page.</span></span>
13. <span data-ttu-id="92329-124">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgifter)** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="92329-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="92329-125">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="92329-125">Select **New**.</span></span>
15. <span data-ttu-id="92329-126">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="92329-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="92329-127">Angiv et nummer i feltet **Kostpris**.</span><span class="sxs-lookup"><span data-stu-id="92329-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="92329-128">Det er muligt at udfylde flere felter, men dette er minimumskravet for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="92329-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="92329-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="92329-129">Select **Save**.</span></span>
18. <span data-ttu-id="92329-130">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgifter)** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="92329-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="92329-131">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="92329-131">Select **New**.</span></span>
20. <span data-ttu-id="92329-132">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="92329-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="92329-133">Vælg en indstilling i feltet **Gyldig til**.</span><span class="sxs-lookup"><span data-stu-id="92329-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="92329-134">Angiv et nummer i feltet **Prisfastsættelse**.</span><span class="sxs-lookup"><span data-stu-id="92329-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="92329-135">Den faktiske salgspris, som anvendes, når en arbejder angiver transaktioner i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="92329-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="92329-136">Hvis du f.eks. både konfigurerer en generel og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.</span><span class="sxs-lookup"><span data-stu-id="92329-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="92329-137">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="92329-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]