---
title: Produktprislister
description: Dette emne indeholder oplysninger om prislisterne i katalogprisfastsættelse, der bruges til projekttilbud og kontrakter.
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
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898164"
---
# <a name="product-price-lists"></a><span data-ttu-id="4057a-103">Produktprislister</span><span class="sxs-lookup"><span data-stu-id="4057a-103">Product price lists</span></span>

<span data-ttu-id="4057a-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="4057a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4057a-105">Prislister og objekter for prislisteelementer understøtter prisfastsættelse i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="4057a-105">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="4057a-106">I de fleste tilfælde bruges denne funktion i forbindelse med katalogbaserede linjer i projekttilbud og projektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="4057a-106">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="4057a-107">I forbindelse med projektbaserede linjer repræsenterer en kontrakt handlen, efter at den blev vundet.</span><span class="sxs-lookup"><span data-stu-id="4057a-107">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="4057a-108">Da forhandlingsprocessen sædvanligvis ligger før den vundne handel, kopieres den prisfastsættelse, der er knyttet til tilbuddet, altid som den er til en ny prisliste og knyttes til kontrakten.</span><span class="sxs-lookup"><span data-stu-id="4057a-108">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="4057a-109">Denne nye prisliste kan ikke ændres uden for kontraktens omfang.</span><span class="sxs-lookup"><span data-stu-id="4057a-109">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="4057a-110">Denne begrænsning er med til at beskytte den satstabel, der er blevet forhandlet om, mod eventuelle prisændringer, der opstår på den overordnede prisliste.</span><span class="sxs-lookup"><span data-stu-id="4057a-110">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="4057a-111">Produkterne skal konfigureres, så de har standardomkostnings- og prislister i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="4057a-111">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="4057a-112">Anvend listeprisen, standardomkostningerne og de aktuelle omkostninger til at konfigurere standardomkostninger og listepriser.</span><span class="sxs-lookup"><span data-stu-id="4057a-112">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="4057a-113">Standardlistepriserne bruges kun i en tilbudslinje eller en projektkontraktlinje, hvis systemet ikke kan finde en prislistelinje for det pågældende produkt på produktprislisten for tilbuddet eller projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="4057a-113">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="4057a-114">Kostprisen for produktkataloglinjer kan ændres mellem tilbud.</span><span class="sxs-lookup"><span data-stu-id="4057a-114">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="4057a-115">Denne funktion er vigtig, for hvis du ikke præcist kan spore omkostninger, kan du ikke beregne driftsoverskuddet for projektaftaler.</span><span class="sxs-lookup"><span data-stu-id="4057a-115">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="4057a-116">Som standard bruges produktets standardomkostning som kostprisen.</span><span class="sxs-lookup"><span data-stu-id="4057a-116">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="4057a-117">Standardkostprisen kan dog opdateres i tilbudslinjen, hvis der findes en anden kostpris for det pågældende tilbud.</span><span class="sxs-lookup"><span data-stu-id="4057a-117">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="4057a-118">Prislisteelementer</span><span class="sxs-lookup"><span data-stu-id="4057a-118">Price list items</span></span>

<span data-ttu-id="4057a-119">Du kan føje produkter fra et produktkatalog til forskellige prislister.</span><span class="sxs-lookup"><span data-stu-id="4057a-119">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="4057a-120">Prislistelinjer for produkter refererer altid til en bestemt enhed.</span><span class="sxs-lookup"><span data-stu-id="4057a-120">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="4057a-121">Du kan konfigurere prislisteelementer for et produkt som et valutabeløb.</span><span class="sxs-lookup"><span data-stu-id="4057a-121">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="4057a-122">Alternativt kan den konfigureres som en funktion af listepris, aktuelle omkostninger eller standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="4057a-122">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="4057a-123">PSA understøtter forskellige afrundingsindstillinger, når priser er konfigureret som en funktion af listeprisen, standardomkostninger eller aktuelle omkostninger.</span><span class="sxs-lookup"><span data-stu-id="4057a-123">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="4057a-124">Ud over at udnytte flere prisfastsættelsesmetoder og afrundingsindstillinger kan du knytte rabatlister til prislisteelementer.</span><span class="sxs-lookup"><span data-stu-id="4057a-124">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

<span data-ttu-id="4057a-125">Når du opretter en ny brugerdefineret prisliste for et tilbud ved at vælge **Opret brugerdefineret prisfastsættelse** på siden **Projekttilbud**, oprettes en kopi af prislisten, og feltet **Objekt** i overskriften for den nye prisliste angives til **Salgsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="4057a-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, a copy of the price list is made, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="4057a-126">Navnet på den nye prisliste tilføjes sammen med navnet på tilbuddet og et tidsstempel.</span><span class="sxs-lookup"><span data-stu-id="4057a-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="4057a-127">Du kan også bruge navnet på den nye prisliste og navnet på tilbuddet i brugerdefinerede arbejdsprocesser til at udløse yderligere gennemgang og godkendelse for tilbud, der bruger brugerdefineret prissætning.</span><span class="sxs-lookup"><span data-stu-id="4057a-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="4057a-128">Standardproduktprisliste</span><span class="sxs-lookup"><span data-stu-id="4057a-128">Default product price list</span></span>
<span data-ttu-id="4057a-129">Hver kundepost indeholder feltet **Standardprisliste**, hvor du kan angive en prisliste, der stemmer overens med den valuta, der er angivet for kunden.</span><span class="sxs-lookup"><span data-stu-id="4057a-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="4057a-130">Der angives ikke automatisk en standardværdi i dette felt.</span><span class="sxs-lookup"><span data-stu-id="4057a-130">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="4057a-131">Når der findes en brugerdefineret prisaftale med en bestemt kunde, kan du bruge dette felt til at knytte en prisliste til den pågældende kunde.</span><span class="sxs-lookup"><span data-stu-id="4057a-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="4057a-132">For objekterne for salgsmulighed, tilbud og projektkontrakt bruges følgende rækkefølge til at angive standardproduktprislister.</span><span class="sxs-lookup"><span data-stu-id="4057a-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="4057a-133">Den samme rækkefølge bruges til projektprislister.</span><span class="sxs-lookup"><span data-stu-id="4057a-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="4057a-134">Tilbud</span><span class="sxs-lookup"><span data-stu-id="4057a-134">Quote</span></span>
2.  <span data-ttu-id="4057a-135">Salgsmulighed</span><span class="sxs-lookup"><span data-stu-id="4057a-135">Opportunity</span></span>
3.  <span data-ttu-id="4057a-136">Kunde</span><span class="sxs-lookup"><span data-stu-id="4057a-136">Customer</span></span>
4.  <span data-ttu-id="4057a-137">Globale indstillinger</span><span class="sxs-lookup"><span data-stu-id="4057a-137">Global settings</span></span> 

<span data-ttu-id="4057a-138">Som standard viser feltet **Produkt** på tilbudslinjen en liste over alle de aktive produkter i tilbuddets produktprisliste.</span><span class="sxs-lookup"><span data-stu-id="4057a-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="4057a-139">Hvis et produkt er blevet deaktiveret, eller hvis det er et kladdeprodukt, vises det ikke på listen, heller ikke selvom det er på prislisten.</span><span class="sxs-lookup"><span data-stu-id="4057a-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="4057a-140">Produktkataloglinjer tilføjes som fakturalinjer i den første faktura, der oprettes for en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="4057a-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="4057a-141">På en kladdefaktura kan de pågældende fakturalinjer slettes.</span><span class="sxs-lookup"><span data-stu-id="4057a-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="4057a-142">Hvis det er tilfældet, vil linjerne blive vist på en efterfølgende faktura, indtil de faktureres, eller indtil fakturaen er sendt til kunden.</span><span class="sxs-lookup"><span data-stu-id="4057a-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="4057a-143">Du kan ikke fakturere et delvist antal på en produktfakturalinje.</span><span class="sxs-lookup"><span data-stu-id="4057a-143">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="4057a-144">Når produktlinjerne fra projektkontrakten faktureres, oprettes der faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="4057a-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="4057a-145">Disse faktiske tal er dog ikke kædet sammen med det relaterede projektobjekt.</span><span class="sxs-lookup"><span data-stu-id="4057a-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="4057a-146">Det vil sige, at produktbaserede projektkontraktlinjer er uafhængige af projektbaseret brug.</span><span class="sxs-lookup"><span data-stu-id="4057a-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="4057a-147">Materialeforbrug på projekter spores ikke.</span><span class="sxs-lookup"><span data-stu-id="4057a-147">Material consumption on projects isn't tracked.</span></span>