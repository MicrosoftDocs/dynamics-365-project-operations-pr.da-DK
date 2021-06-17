---
title: Produktbaserede tilbudslinjer for omkostningsfastsættelse
description: Dette emne indeholder oplysninger om anvendelse af en kostpris på en produktbaseret tilbudslinje.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003444"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="7e4d7-103">Produktbaserede tilbudslinjer for omkostningsfastsættelse</span><span class="sxs-lookup"><span data-stu-id="7e4d7-103">Costing product-based quote lines</span></span>

<span data-ttu-id="7e4d7-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="7e4d7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7e4d7-105">Produktbaserede tilbudslinjer i Dynamics 365 Project Operations indeholder også feltet **Kostpris**.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="7e4d7-106">Dette felt bruges til at spore kostprisen for produktet på tilbudslinjen og til beregninger downstream-rentabilitet.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="7e4d7-107">Når der oprettes en produktbaseret tilbudslinje for et katalogprodukt, hentes omkostningen for den produktbaserede tilbudslinje fra feltet **Standardomkostning** i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="7e4d7-108">Feltet standardomkostning i produktkataloget konfigureres i organisationens grundvaluta.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="7e4d7-109">Standardomkostningen for en enhed på den produkt baserede tilbudslinje konverteres til salgsvalutaen i tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="7e4d7-110">Enhedsomkostning på en produktbaseret tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="7e4d7-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="7e4d7-111">Formålet med en enhedsomkostning på en produktbaseret tilbudslinje er at give mulighed for at have forskellige omkostninger for et produkt for hvert salg.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="7e4d7-112">Dette er ikke et typisk scenario, men nogle gange diskonteres omkostningen for produktet af leverandøren, afhængigt af den kunde i det endelige salg.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="7e4d7-113">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="7e4d7-113">For example:</span></span>

<span data-ttu-id="7e4d7-114">Fabrikam Robotics installerer robotarme i montagelinjer i A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="7e4d7-115">Fabrikam leverer Installationstjenester, men robotarme indkøbes fra Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="7e4d7-116">Hvis installationen af robotarme i A Datum Corporation åbner en ny vertikalbranche for arme fra Trey Robotics, kan Trey tilbyde en særlig rabat for denne aftale til Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="7e4d7-117">I dette tilfælde vil Fabrikam oprette produktbaseret tilbudslinje for robotarme og angive en særlig omkostning pr. enhed for dette tilbud.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="7e4d7-118">Denne omkostning adskiller sig fra standardomkostningen for arme fra Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="7e4d7-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]