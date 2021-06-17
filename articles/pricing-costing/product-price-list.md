---
title: Produktprislister
description: Dette emne indeholder oplysninger om prislisterne i katalogprisfastsættelse, der bruges til projekttilbud og kontrakter.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004929"
---
# <a name="product-price-lists"></a><span data-ttu-id="b45e6-103">Produktprislister</span><span class="sxs-lookup"><span data-stu-id="b45e6-103">Product price lists</span></span>

<span data-ttu-id="b45e6-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b45e6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="b45e6-105">I Project Operations understøtter **Produktprislister** og relaterede prislisteelementobjekter funktionaliteten for prisfastsættelse af produkter i produktbaserede tilbuds- og kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="b45e6-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="b45e6-106">For produkter, der bruges på projekter, anvendes prislisteelementposterne for projektprislister.</span><span class="sxs-lookup"><span data-stu-id="b45e6-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="b45e6-107">Produkterne skal konfigureres, så de har standardomkostnings- og prislister i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="b45e6-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="b45e6-108">Anvend listeprisen, standardomkostningerne og de aktuelle omkostninger til at konfigurere standardomkostninger og listepriser.</span><span class="sxs-lookup"><span data-stu-id="b45e6-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="b45e6-109">Standardlistepriserne bruges kun i en tilbudslinje eller en projektkontraktlinje, hvis systemet ikke kan finde en prislistelinje for det pågældende produkt på produktprislisten for tilbuddet eller projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="b45e6-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="b45e6-110">Kostprisen for produktkataloglinjer kan ændres mellem tilbud.</span><span class="sxs-lookup"><span data-stu-id="b45e6-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="b45e6-111">Denne funktion er vigtig, for hvis du ikke præcist kan spore omkostninger, kan du ikke beregne driftsoverskuddet for projektaftaler.</span><span class="sxs-lookup"><span data-stu-id="b45e6-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="b45e6-112">Som standard bruges produktets standardomkostning som kostprisen.</span><span class="sxs-lookup"><span data-stu-id="b45e6-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="b45e6-113">Standardkostprisen kan dog opdateres i tilbudslinjen, hvis der findes en anden kostpris for det pågældende tilbud.</span><span class="sxs-lookup"><span data-stu-id="b45e6-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="b45e6-114">Prislisteelementer</span><span class="sxs-lookup"><span data-stu-id="b45e6-114">Price list items</span></span>

<span data-ttu-id="b45e6-115">Du kan føje produkter fra et produktkatalog til forskellige prislister.</span><span class="sxs-lookup"><span data-stu-id="b45e6-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="b45e6-116">Prislistelinjer for produkter refererer altid til en bestemt enhed.</span><span class="sxs-lookup"><span data-stu-id="b45e6-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="b45e6-117">Du kan konfigurere prislisteelementer for et produkt som et valutabeløb.</span><span class="sxs-lookup"><span data-stu-id="b45e6-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="b45e6-118">Alternativt kan den konfigureres som en funktion af listepris, aktuelle omkostninger eller standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="b45e6-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="b45e6-119">Funktionen prisfastsættelse understøtter forskellige afrundingsindstillinger, når produktpriser er konfigureret som en funktion af listeprisen, standardomkostninger eller aktuelle omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b45e6-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="b45e6-120">Ud over at udnytte flere prisfastsættelsesmetoder og afrundingsindstillinger kan du knytte rabatlister til prislisteelementer.</span><span class="sxs-lookup"><span data-stu-id="b45e6-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="b45e6-121">Standardproduktprisliste</span><span class="sxs-lookup"><span data-stu-id="b45e6-121">Default product price list</span></span>
<span data-ttu-id="b45e6-122">Hver kundepost indeholder feltet **Standardprisliste**, hvor du kan angive en prisliste, der stemmer overens med den valuta, der er angivet for kunden.</span><span class="sxs-lookup"><span data-stu-id="b45e6-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="b45e6-123">Der angives ikke automatisk en standardværdi i dette felt.</span><span class="sxs-lookup"><span data-stu-id="b45e6-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="b45e6-124">Når der findes en brugerdefineret prisaftale med en bestemt kunde, kan du bruge dette felt til at knytte en prisliste til den pågældende kunde.</span><span class="sxs-lookup"><span data-stu-id="b45e6-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="b45e6-125">For objekterne for salgsmulighed, tilbud og projektkontrakt bruges følgende rækkefølge til at angive standardproduktprislister.</span><span class="sxs-lookup"><span data-stu-id="b45e6-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="b45e6-126">Den samme rækkefølge bruges til projektprislister.</span><span class="sxs-lookup"><span data-stu-id="b45e6-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="b45e6-127">Tilbud</span><span class="sxs-lookup"><span data-stu-id="b45e6-127">Quote</span></span>
2.  <span data-ttu-id="b45e6-128">Salgsmulighed</span><span class="sxs-lookup"><span data-stu-id="b45e6-128">Opportunity</span></span>
3.  <span data-ttu-id="b45e6-129">Kunde</span><span class="sxs-lookup"><span data-stu-id="b45e6-129">Customer</span></span>
4.  <span data-ttu-id="b45e6-130">Globale indstillinger</span><span class="sxs-lookup"><span data-stu-id="b45e6-130">Global settings</span></span> 

<span data-ttu-id="b45e6-131">Som standard viser feltet **Produkt** på tilbudslinjen en liste over alle de aktive produkter i tilbuddets produktprisliste.</span><span class="sxs-lookup"><span data-stu-id="b45e6-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="b45e6-132">Hvis et produkt er blevet deaktiveret, eller hvis det er et kladdeprodukt, vises det ikke på listen, heller ikke selvom det er på prislisten.</span><span class="sxs-lookup"><span data-stu-id="b45e6-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="b45e6-133">Produktkataloglinjer tilføjes som fakturalinjer i den første faktura, der oprettes for en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="b45e6-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="b45e6-134">På en kladdefaktura kan de pågældende fakturalinjer slettes.</span><span class="sxs-lookup"><span data-stu-id="b45e6-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="b45e6-135">Hvis det er tilfældet, vil linjerne blive vist på en efterfølgende faktura, indtil de faktureres, eller indtil fakturaen er sendt til kunden.</span><span class="sxs-lookup"><span data-stu-id="b45e6-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="b45e6-136">Du kan ikke fakturere et delvist antal på en produktfakturalinje.</span><span class="sxs-lookup"><span data-stu-id="b45e6-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="b45e6-137">Når produktlinjerne fra projektkontrakten faktureres, oprettes der faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="b45e6-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="b45e6-138">Disse faktiske tal er dog ikke kædet sammen med det relaterede projektobjekt.</span><span class="sxs-lookup"><span data-stu-id="b45e6-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="b45e6-139">Det vil sige, at produktbaserede projektkontraktlinjer er uafhængige af projektbaseret brug.</span><span class="sxs-lookup"><span data-stu-id="b45e6-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
