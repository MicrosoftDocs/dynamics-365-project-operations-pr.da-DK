---
title: Ressourceestimater
description: Dette emne indeholder oplysninger om, hvordan ressourceestimater beregnes i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286511"
---
# <a name="resource-estimates"></a><span data-ttu-id="190b5-103">Ressourceestimater</span><span class="sxs-lookup"><span data-stu-id="190b5-103">Resource estimates</span></span>

<span data-ttu-id="190b5-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="190b5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="190b5-105">Ressourceestimater hentes fra faseinddelt tidsforbrug, der er defineret i arbejdsopgavehierarkiet sammen med de gældende dimensioner for prisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="190b5-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="190b5-106">Beregningen er som regel **pris/time for hver rolle x timer.**</span><span class="sxs-lookup"><span data-stu-id="190b5-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="190b5-107">Tidsfaseinddelt arbejdsindsats for de enkelte ressourcer gemmes i posten for ressourcetildelingen.</span><span class="sxs-lookup"><span data-stu-id="190b5-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="190b5-108">Prisfastsættelsen gemmes i en foruddefineret prisliste.</span><span class="sxs-lookup"><span data-stu-id="190b5-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="190b5-109">Enhedsomregning anvendes på baggrund af den gældende prisliste.</span><span class="sxs-lookup"><span data-stu-id="190b5-109">Unit conversion is applied based on the applicable price list.</span></span>

![Ressourceestimater](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="190b5-111">Standarder for kostpris og omkostningsvaluta</span><span class="sxs-lookup"><span data-stu-id="190b5-111">Default cost price and cost currency</span></span>

<span data-ttu-id="190b5-112">Kostpriser hentes som standard fra afdelingen.</span><span class="sxs-lookup"><span data-stu-id="190b5-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="190b5-113">Standarder for faktureringshyppighed og salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="190b5-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="190b5-114">Salgspriser anvendes én gang pr. handel.</span><span class="sxs-lookup"><span data-stu-id="190b5-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="190b5-115">Hierarkiet for standardprislisten er som følger:</span><span class="sxs-lookup"><span data-stu-id="190b5-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="190b5-116">Organisation</span><span class="sxs-lookup"><span data-stu-id="190b5-116">Organization</span></span>
2. <span data-ttu-id="190b5-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="190b5-117">Customer</span></span>
3. <span data-ttu-id="190b5-118">Tilbud/kontrakt</span><span class="sxs-lookup"><span data-stu-id="190b5-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]