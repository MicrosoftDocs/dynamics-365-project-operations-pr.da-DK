---
title: Konfigurer intern projektfakturering
description: I dette emne beskrives det, hvordan du kan konfigurere projektfakturering mellem to firmaer i din organisation.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750503"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="48e0d-103">Konfigurer intern projektfakturering</span><span class="sxs-lookup"><span data-stu-id="48e0d-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48e0d-104">I dette emne beskrives det, hvordan du kan konfigurere projektfakturering mellem to firmaer i din organisation.</span><span class="sxs-lookup"><span data-stu-id="48e0d-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="48e0d-105">Denne opgave anvender datasættet USSI.</span><span class="sxs-lookup"><span data-stu-id="48e0d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="48e0d-106">Gå til **Moduler > Kreditor > Leverandører > Alle leverandører** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="48e0d-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="48e0d-107">På listen **Alle leverandører** skal du finde og vælge den ønskede post.</span><span class="sxs-lookup"><span data-stu-id="48e0d-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="48e0d-108">Vælg **Generelt** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="48e0d-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="48e0d-109">Vælg **Intern**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="48e0d-110">Angiv **Aktiv** til **Ja** for at aktivere intern handel.</span><span class="sxs-lookup"><span data-stu-id="48e0d-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="48e0d-111">I feltet **Kundevirksomhed** skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="48e0d-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="48e0d-112">I feltet **Min konto** skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="48e0d-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="48e0d-113">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-113">Select **Save**.</span></span>
9. <span data-ttu-id="48e0d-114">Luk siderne for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="48e0d-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="48e0d-115">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Projektstyring og regnskabsparametre** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="48e0d-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="48e0d-116">Vælg fanen **Intern**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="48e0d-117">Flyt skyderen til **Ja** for at aktivere intern ressourceplanlægning og timesedler.</span><span class="sxs-lookup"><span data-stu-id="48e0d-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="48e0d-118">Marker den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="48e0d-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="48e0d-119">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-119">Select **New**.</span></span>
15. <span data-ttu-id="48e0d-120">I feltet **Låntagende juridisk enhed** skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="48e0d-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="48e0d-121">Marker afkrydsningsfeltet **Akkumuler omsætning**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="48e0d-122">I feltet **Standardkategori for timesedler** skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="48e0d-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="48e0d-123">I feltet **Standardkategori for udgifter** skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="48e0d-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="48e0d-124">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-124">Select **Save**.</span></span>
20. <span data-ttu-id="48e0d-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="48e0d-125">Close the page.</span></span>
21. <span data-ttu-id="48e0d-126">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Bogføring > Konfiguration af bogføring i hovedbogen** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="48e0d-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="48e0d-127">I feltet **Kontotyper i hovedbogen** skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="48e0d-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="48e0d-128">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-128">Select **New**.</span></span>
24. <span data-ttu-id="48e0d-129">I feltet **Hovedkonto** i den nye række skal du angive de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="48e0d-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="48e0d-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-130">Select **Save**.</span></span>
26. <span data-ttu-id="48e0d-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="48e0d-131">Close the page.</span></span>
27. <span data-ttu-id="48e0d-132">Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Overfør pris** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="48e0d-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="48e0d-133">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-133">Select **New**.</span></span>
29. <span data-ttu-id="48e0d-134">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="48e0d-135">I feltet **Låntagende juridisk enhed** skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="48e0d-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="48e0d-136">I feltet **Model for overførsel af pris** skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="48e0d-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="48e0d-137">Angiv et nummer i feltet **Prisfastsættelse**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="48e0d-138">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="48e0d-138">Select **Save**.</span></span>

