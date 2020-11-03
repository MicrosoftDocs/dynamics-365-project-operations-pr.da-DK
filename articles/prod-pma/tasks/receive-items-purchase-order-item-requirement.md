---
title: Modtag varer på indkøbsordre fra varebehov
description: I dette emne forklares, hvordan du modtager varer på en indkøbsordre fra et varebehov.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074339"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="5ee1d-103">Modtag varer på indkøbsordre fra varebehov</span><span class="sxs-lookup"><span data-stu-id="5ee1d-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ee1d-104">I dette emne forklares, hvordan du modtager varer på en indkøbsordre fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="5ee1d-105">Hvis du bruger et varebehov i stedet for en varetransaktion, kan du planlægge leveringen lige før varen faktisk anvendes, oprette en indkøbsordre, inkludere varen i handelsaftalestrukturen og inkludere varebehovet i produktionsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="5ee1d-106">Denne opgave anvender datasættet USSI.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="5ee1d-107">Gå til **Moduler > Projektstyring og regnskab > Projekter > Alle projekter** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="5ee1d-108">Vælg linket i den ønskede række på listen.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="5ee1d-109">Vælg **Plan** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="5ee1d-110">Vælg **varebehov**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="5ee1d-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-111">Select **New**.</span></span>
6. <span data-ttu-id="5ee1d-112">Angiv eller vælg en værdi i feltet **Varenummer** i den nye række.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="5ee1d-113">Angiv et nummer i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="5ee1d-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-114">Select **Save**.</span></span>
9. <span data-ttu-id="5ee1d-115">Vælg **Administrer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="5ee1d-116">Vælg **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-116">Select **Functions**.</span></span>
11. <span data-ttu-id="5ee1d-117">Vælg **Opret en indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="5ee1d-118">Markér afkrydsningsfeltet **Inkluder alle**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="5ee1d-119">I feltet **Leverandørkonto** skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="5ee1d-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-120">Select **OK**.</span></span>
15. <span data-ttu-id="5ee1d-121">Gå til **Moduler > Kreditor > Indkøbsordrer > Alle indkøbsordrer** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="5ee1d-122">Vælg linket i den ønskede række på listen.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="5ee1d-123">Vælg **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="5ee1d-124">Vælg **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="5ee1d-125">Vælg **Modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="5ee1d-126">Vælg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="5ee1d-127">Skriv en værdi i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="5ee1d-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ee1d-128">Select **OK**.</span></span>

