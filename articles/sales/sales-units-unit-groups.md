---
title: Undermoduler og enhedsgrupper
description: Dette emne indeholder oplysninger om, hvordan du opretter enheder og enhedsgrupper i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898749"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="f7a5d-103">Undermoduler og enhedsgrupper</span><span class="sxs-lookup"><span data-stu-id="f7a5d-103">Units and unit groups</span></span>

<span data-ttu-id="f7a5d-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="f7a5d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7a5d-105">Enheder er det antal eller målinger, som du kan sælge dine produkter eller tjenester i.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="f7a5d-106">Hvis du for eksempel sælger haveartikler, kan du sælge frø i enheder af pakker, kasser og paller.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="f7a5d-107">En enhedsgruppe er en samling af disse forskellige enheder.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="f7a5d-108">Hvis du vil udføre trinnene i dette emne, skal du sørge for, at du er tildelt rollen som systemadministrator eller rollen som Sales Professional Manager eller har tilsvarende tilladelser.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="f7a5d-109">Oprette en enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="f7a5d-109">Create a unit group</span></span>

1. <span data-ttu-id="f7a5d-110">Vælg **Enheder** i oversigten over webstedet.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="f7a5d-111">Vælg **Ny** og i dialogboksen **Opret enhedsgruppe** skal du angive enhedens navn.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="f7a5d-112">Angiv den laveste almindelige måleenhed, som produktet sælges i, i feltet **Primær enhed**.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="f7a5d-113">Du kan f.eks. angive "stk." eller "kg.".</span><span class="sxs-lookup"><span data-stu-id="f7a5d-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="f7a5d-114">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="f7a5d-115">Tilføj enheder til en enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="f7a5d-115">Add units to a unit group</span></span>

1. <span data-ttu-id="f7a5d-116">Åbn en enhedsgruppe, og på fanen **Relateret** skal du vælge **Enheder**.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="f7a5d-117">Du vil se, at den primære enhed allerede er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="f7a5d-118">Vælg **Tilføj ny enhed**, og på siden **Opret hurtig: enhed** skal du i feltet **Navn** angive navnet på enheden.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="f7a5d-119">I feltet **Antal** skal du angive det antal, som enheden skal indeholde.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="f7a5d-120">Hvis f.eks. en boks indeholder to styk, skal du angive "2".</span><span class="sxs-lookup"><span data-stu-id="f7a5d-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="f7a5d-121">I feltet **Basisenhed** skal du vælge en basisenhed for at oprette den mindste måleenhed for enheden.</span><span class="sxs-lookup"><span data-stu-id="f7a5d-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="f7a5d-122">Du kan f. eks. vælge "stk.".</span><span class="sxs-lookup"><span data-stu-id="f7a5d-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="f7a5d-123">Vælg **Gem**:</span><span class="sxs-lookup"><span data-stu-id="f7a5d-123">Select **Save**:</span></span>
