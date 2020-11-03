---
title: Ressourceestimater
description: Dette emne indeholder oplysninger om, hvordan ressourceestimater beregnes i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074092"
---
# <a name="resource-estimates"></a><span data-ttu-id="7780b-103">Ressourceestimater</span><span class="sxs-lookup"><span data-stu-id="7780b-103">Resource estimates</span></span>

<span data-ttu-id="7780b-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="7780b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7780b-105">Ressourceestimater hentes fra faseinddelt tidsforbrug, der er defineret i arbejdsopgavehierarkiet sammen med de gældende dimensioner for prisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="7780b-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="7780b-106">Beregningen er som regel **pris/time for hver rolle x timer.**</span><span class="sxs-lookup"><span data-stu-id="7780b-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="7780b-107">Tidsfaseinddelt arbejdsindsats for de enkelte ressourcer gemmes i posten for ressourcetildelingen.</span><span class="sxs-lookup"><span data-stu-id="7780b-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="7780b-108">Prisfastsættelsen gemmes i en foruddefineret prisliste.</span><span class="sxs-lookup"><span data-stu-id="7780b-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="7780b-109">Enhedsomregning anvendes på baggrund af den gældende prisliste.</span><span class="sxs-lookup"><span data-stu-id="7780b-109">Unit conversion is applied based on the applicable price list.</span></span>

![Ressourceestimater](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="7780b-111">Standarder for kostpris og omkostningsvaluta</span><span class="sxs-lookup"><span data-stu-id="7780b-111">Default cost price and cost currency</span></span>

<span data-ttu-id="7780b-112">Kostpriser hentes som standard fra afdelingen.</span><span class="sxs-lookup"><span data-stu-id="7780b-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="7780b-113">Standarder for faktureringshyppighed og salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="7780b-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="7780b-114">Salgspriser anvendes én gang pr. handel.</span><span class="sxs-lookup"><span data-stu-id="7780b-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="7780b-115">Hierarkiet for standardprislisten er som følger:</span><span class="sxs-lookup"><span data-stu-id="7780b-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="7780b-116">Organisation</span><span class="sxs-lookup"><span data-stu-id="7780b-116">Organization</span></span>
2. <span data-ttu-id="7780b-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="7780b-117">Customer</span></span>
3. <span data-ttu-id="7780b-118">Tilbud/kontrakt</span><span class="sxs-lookup"><span data-stu-id="7780b-118">Quote/contract</span></span>
