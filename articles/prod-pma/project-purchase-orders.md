---
title: Indkøbsordrer for et projekt
description: I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer til et projekt. Den anvendte metode afhænger af formålet med indkøbsordren, og hvornår de indkøbte varerne forbruges samt tilskrives et projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074160"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="349cb-104">Indkøbsordrer for et projekt</span><span class="sxs-lookup"><span data-stu-id="349cb-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="349cb-105">I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer til et projekt.</span><span class="sxs-lookup"><span data-stu-id="349cb-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="349cb-106">Den anvendte metode afhænger af formålet med indkøbsordren, og hvornår de indkøbte varerne forbruges samt tilskrives et projekt.</span><span class="sxs-lookup"><span data-stu-id="349cb-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="349cb-107">Metoder til oprettelse af en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="349cb-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="349cb-108">Du kan benytte en af følgende fremgangsmåder for at oprette en købsordre i projektstyring og regnskab.</span><span class="sxs-lookup"><span data-stu-id="349cb-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="349cb-109">Formålet med indkøbsordren afgør, hvornår indkøbsordren forbruges, og derfor hvornår varerne kan tilskrives et projekt.</span><span class="sxs-lookup"><span data-stu-id="349cb-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="349cb-110">Metode</span><span class="sxs-lookup"><span data-stu-id="349cb-110">Method</span></span></th>
<th><span data-ttu-id="349cb-111">Formål</span><span class="sxs-lookup"><span data-stu-id="349cb-111">Purpose</span></span></th>
<th><span data-ttu-id="349cb-112">Forbrug af varer</span><span class="sxs-lookup"><span data-stu-id="349cb-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="349cb-113">Opret en indkøbsordre direkte fra et projekt.</span><span class="sxs-lookup"><span data-stu-id="349cb-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="349cb-114">Brug denne metode til at købe varer fra en ekstern leverandør, som skal forbruges i et projekt.</span><span class="sxs-lookup"><span data-stu-id="349cb-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="349cb-115">Du kan oprette indkøbsordren på to måder:</span><span class="sxs-lookup"><span data-stu-id="349cb-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="349cb-116">Fra selve projektet.</span><span class="sxs-lookup"><span data-stu-id="349cb-116">From the project itself.</span></span> <span data-ttu-id="349cb-117">I dette tilfælde er projektet allerede defineret for indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="349cb-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="349cb-118">Ved at gå til projektets indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="349cb-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="349cb-119">Du skal både vælge den leverandør og det projekt, som du vil oprette indkøbsordren for.</span><span class="sxs-lookup"><span data-stu-id="349cb-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="349cb-120">Varer forbruges, når leverandørfakturaen opdateres.</span><span class="sxs-lookup"><span data-stu-id="349cb-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="349cb-121">Opret en indkøbsordre fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="349cb-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="349cb-122">Brug denne metode til at købe varer, når du opretter en salgsordre fra et projekt.</span><span class="sxs-lookup"><span data-stu-id="349cb-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="349cb-123">Varerne forbruges, når salgsordren faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="349cb-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="349cb-124">Opret en indkøbsordre ud fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="349cb-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="349cb-125">Brug denne metode til at købe varer, når du opretter et varebehov fra et projekt.</span><span class="sxs-lookup"><span data-stu-id="349cb-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="349cb-126">Varer forbruges, når følgesedlen til varebehovet opdateres.</span><span class="sxs-lookup"><span data-stu-id="349cb-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="349cb-127">Når du opdaterer leverandørfakturaen eller følgesedlen, bliver du bedt om at opdatere følgesedlen for varebehovet.</span><span class="sxs-lookup"><span data-stu-id="349cb-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="349cb-128">Du kan finde flere oplysninger i [Modtag varer på købsordre fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="349cb-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

