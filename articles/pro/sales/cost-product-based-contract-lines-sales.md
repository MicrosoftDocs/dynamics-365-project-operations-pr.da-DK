---
title: Produktbaserede kontraktlinjer for omkostninger - lille
description: Dette emne indeholder oplysninger om oprettelse
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764452"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="ffa47-103">Produktbaserede kontraktlinjer for omkostninger - lille</span><span class="sxs-lookup"><span data-stu-id="ffa47-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="ffa47-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="ffa47-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ffa47-105">Produktbaserede kontraktlinjer i Dynamics 365 Project Operations omfatter feltet **Kostpris**, som gemmer kostprisen for produktet til beregninger af downstream-rentabilitet.</span><span class="sxs-lookup"><span data-stu-id="ffa47-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="ffa47-106">Når der oprettes en produktbaseret kontraktlinje for et katalogprodukt, hentes omkostningen for linjen som standard fra feltet **Standardomkostning** i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="ffa47-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="ffa47-107">Feltet **Standardomkostning** i produktkataloget konfigureres i organisationens grundvaluta.</span><span class="sxs-lookup"><span data-stu-id="ffa47-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="ffa47-108">Når enhedsomkostningen konverteres til standarden på kontraktlinjen, konverteres den til salgsvalutaen i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="ffa47-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="ffa47-109">Enhedsomkostning på en produktbaseret kontraktlinje</span><span class="sxs-lookup"><span data-stu-id="ffa47-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="ffa47-110">Med en enhedsomkostning på en produktbaseret kontraktlinje kan du have forskellige produktomkostninger ved hvert salg af en enhed.</span><span class="sxs-lookup"><span data-stu-id="ffa47-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="ffa47-111">Selvom det ikke altid er nødvendigt, er der visse scenarier, hvor produktets omkostninger kan diskonteres for kunden af leverandøren.</span><span class="sxs-lookup"><span data-stu-id="ffa47-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="ffa47-112">Overvej følgende scenarie:</span><span class="sxs-lookup"><span data-stu-id="ffa47-112">Consider the following scenario:</span></span>

<span data-ttu-id="ffa47-113">Fabrikam Robotics installerer robotarme i montagelinjerne hos Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="ffa47-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="ffa47-114">Fabrikam leverer installationstjenester, men robotarmene er fra Trey Research.</span><span class="sxs-lookup"><span data-stu-id="ffa47-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="ffa47-115">Hvis installationen af robotarme i Adatum Corporation åbner en ny vertikalbranche for Trey Reserarch, kan de tilbyde Fabrikam en særlig rabat i denne aftale.</span><span class="sxs-lookup"><span data-stu-id="ffa47-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="ffa47-116">I dette tilfælde opretter Fabrikam en produktbaseret kontraktlinje for Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="ffa47-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="ffa47-117">Der angives en omkostning pr. enhed for denne kontrakt.</span><span class="sxs-lookup"><span data-stu-id="ffa47-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="ffa47-118">Omkostningen er forskellig fra omkostningen ved robotarme fra Trey Research.</span><span class="sxs-lookup"><span data-stu-id="ffa47-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
