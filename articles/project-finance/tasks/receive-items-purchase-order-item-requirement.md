---
title: Modtag varer på indkøbsordre fra varebehov
description: I dette emne forklares, hvordan du modtager varer på en indkøbsordre fra et varebehov.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750480"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="0eb95-103">Modtag varer på indkøbsordre fra varebehov</span><span class="sxs-lookup"><span data-stu-id="0eb95-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0eb95-104">I dette emne forklares, hvordan du modtager varer på en indkøbsordre fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="0eb95-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="0eb95-105">Hvis du bruger et varebehov i stedet for en varetransaktion, kan du planlægge leveringen lige før varen faktisk anvendes, oprette en indkøbsordre, inkludere varen i handelsaftalestrukturen og inkludere varebehovet i produktionsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="0eb95-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="0eb95-106">Denne opgave anvender datasættet USSI.</span><span class="sxs-lookup"><span data-stu-id="0eb95-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="0eb95-107">Gå til **Moduler > Projektstyring og regnskab > Projekter > Alle projekter** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="0eb95-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="0eb95-108">Vælg linket i den ønskede række på listen.</span><span class="sxs-lookup"><span data-stu-id="0eb95-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="0eb95-109">Vælg **Plan** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0eb95-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="0eb95-110">Vælg **varebehov**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="0eb95-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-111">Select **New**.</span></span>
6. <span data-ttu-id="0eb95-112">Angiv eller vælg en værdi i feltet **Varenummer** i den nye række.</span><span class="sxs-lookup"><span data-stu-id="0eb95-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="0eb95-113">Angiv et nummer i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="0eb95-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-114">Select **Save**.</span></span>
9. <span data-ttu-id="0eb95-115">Vælg **Administrer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0eb95-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="0eb95-116">Vælg **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-116">Select **Functions**.</span></span>
11. <span data-ttu-id="0eb95-117">Vælg **Opret en indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="0eb95-118">Markér afkrydsningsfeltet **Inkluder alle**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="0eb95-119">I feltet **Leverandørkonto** skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="0eb95-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="0eb95-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-120">Select **OK**.</span></span>
15. <span data-ttu-id="0eb95-121">Gå til **Moduler > Kreditor > Indkøbsordrer > Alle indkøbsordrer** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="0eb95-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="0eb95-122">Vælg linket i den ønskede række på listen.</span><span class="sxs-lookup"><span data-stu-id="0eb95-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="0eb95-123">Vælg **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0eb95-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="0eb95-124">Vælg **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="0eb95-125">Vælg **Modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0eb95-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="0eb95-126">Vælg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="0eb95-127">Skriv en værdi i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="0eb95-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0eb95-128">Select **OK**.</span></span>

