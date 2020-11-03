---
title: Produktbaserede kontraktlinjer for omkostningsfastsættelse
description: Dette emne indeholder oplysninger om oprettelse
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074403"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="3287e-103">Produktbaserede kontraktlinjer for omkostningsfastsættelse</span><span class="sxs-lookup"><span data-stu-id="3287e-103">Costing product-based contract lines</span></span>

<span data-ttu-id="3287e-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3287e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3287e-105">Produktbaserede kontraktlinjer i Dynamics 365 Project Operations omfatter feltet **Kostpris** , som indeholder kostprisen på produktet i relation til beregning af den afledte rentabilitet.</span><span class="sxs-lookup"><span data-stu-id="3287e-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="3287e-106">Når der oprettes en produktbaseret kontaktlinje for et katalogprodukt, hentes omkostningen for den produktbaserede kontraktlinje som standard fra feltet **Standardomkostning** i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="3287e-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3287e-107">Feltet **Standardomkostning** i produktkataloget konfigureres i organisationens grundvaluta.</span><span class="sxs-lookup"><span data-stu-id="3287e-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3287e-108">Når enhedsomkostningen konverteres til standarden på kontraktlinjen, konverteres den til salgsvalutaen i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="3287e-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="3287e-109">Enhedsomkostning på en produktbaseret kontraktlinje</span><span class="sxs-lookup"><span data-stu-id="3287e-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="3287e-110">Med en enhedsomkostning på en produktbaseret kontraktlinje kan du have forskellige produktomkostninger ved hvert salg af en enhed.</span><span class="sxs-lookup"><span data-stu-id="3287e-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="3287e-111">Selvom det ikke altid er nødvendigt, er der visse scenarier, hvor produktets omkostninger kan diskonteres for kunden af leverandøren.</span><span class="sxs-lookup"><span data-stu-id="3287e-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="3287e-112">Overvej følgende scenarie:</span><span class="sxs-lookup"><span data-stu-id="3287e-112">Consider the following scenario:</span></span>

<span data-ttu-id="3287e-113">Fabrikam Robotics installerer robotarme i montagelinjerne hos Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="3287e-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="3287e-114">Fabrikam leverer Installationstjenester, men robotarme indkøbes fra Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3287e-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="3287e-115">Hvis installationen af robotarme i Adatum Corporation åbner en ny vertikalbranche for Trey Reserarch, kan de tilbyde Fabrikam en særlig rabat i denne aftale.</span><span class="sxs-lookup"><span data-stu-id="3287e-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="3287e-116">I dette tilfælde opretter Fabrikam en produktbaseret kontraktlinje for Robotic Arms og angiver en omkostning pr. enhed for denne kontrakt, som adskiller sig fra standardomkostningerne ved robotarme fra Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3287e-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
