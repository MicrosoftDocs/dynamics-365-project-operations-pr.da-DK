---
title: Oversigt over produktbaserede tilbudslinjer - lille
description: Dette emne indeholder oplysninger om at arbejde med produktbaserede tilbudslinjer.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369819"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="80128-103">Oversigt over produktbaserede tilbudslinjer - lille</span><span class="sxs-lookup"><span data-stu-id="80128-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="80128-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="80128-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="80128-105">Du kan oprette produktbaserede tilbudslinjer i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="80128-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="80128-106">Produktbaserede tilbudslinjer kan tilføjes manuelt, eller de kan være elementer fra produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="80128-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="80128-107">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="80128-107">Product catalog</span></span>

<span data-ttu-id="80128-108">Hvert produkt i produktkataloget har en standardenhed og enhedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="80128-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="80128-109">Hvis flere produkter deler det samme sæt attributter, kan du oprette en produktfamilie, der deler de pågældende attributter.</span><span class="sxs-lookup"><span data-stu-id="80128-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="80128-110">Et firma sælger f.eks. abonnementslicenser til forskellige typer af software.</span><span class="sxs-lookup"><span data-stu-id="80128-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="80128-111">Alle abonnementsprogrammer har følgende to attributter:</span><span class="sxs-lookup"><span data-stu-id="80128-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="80128-112">Antal brugere</span><span class="sxs-lookup"><span data-stu-id="80128-112">Number of users</span></span>
- <span data-ttu-id="80128-113">Et abonnements varighed målt i måneder</span><span class="sxs-lookup"><span data-stu-id="80128-113">A subscription duration measured in months</span></span>

<span data-ttu-id="80128-114">For at vedligeholde denne type katalog skal du oprette en produktserie med navnet **Abonnementsprogram** og tilføje antallet af brugere og abonnementets varighed som attributter.</span><span class="sxs-lookup"><span data-stu-id="80128-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="80128-115">Derefter kan du tilføje de enkelte produkter til produktfamilien **Abonnementsprogram**.</span><span class="sxs-lookup"><span data-stu-id="80128-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="80128-116">Tilføj produktkatalogelementer til et projekttilbud</span><span class="sxs-lookup"><span data-stu-id="80128-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="80128-117">Siderne **Projekttilbud** og **Projektkontrakt** indeholder sektioner for projektbaserede linjer og produktbaserede linjer.</span><span class="sxs-lookup"><span data-stu-id="80128-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="80128-118">For produktbaserede linjer indeholder rullelisten på tilbudslinjen eller på projektkontraktlinjen alle produkter og enheder i produktprislisten.</span><span class="sxs-lookup"><span data-stu-id="80128-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="80128-119">Du kan også tilføje produkter, der ikke er en del af produktprislisten.</span><span class="sxs-lookup"><span data-stu-id="80128-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="80128-120">Derudover kan du vælge produkter fra andre prislister eller direkte fra produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="80128-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="80128-121">Når du vælger produkter direkte fra et produktkatalog, bruges standardprislisten for produktet til at beregne produktets salgspris.</span><span class="sxs-lookup"><span data-stu-id="80128-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="80128-122">Hvis der ikke er angivet en standardprisliste, angives prisen til nul (0).</span><span class="sxs-lookup"><span data-stu-id="80128-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="80128-123">Når en tilbudslinje er baseret på et produktkatalog, kan du tilsidesætte salgsprisen direkte på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="80128-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="80128-124">En tilbudslinje i feltet **Prisfastsættelse** med to tilgængelige værdier:</span><span class="sxs-lookup"><span data-stu-id="80128-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="80128-125">**Tilsidesæt prisfastsættelse**</span><span class="sxs-lookup"><span data-stu-id="80128-125">**Override Pricing**</span></span>
- <span data-ttu-id="80128-126">**Benyt standard**</span><span class="sxs-lookup"><span data-stu-id="80128-126">**Use Default**</span></span>

<span data-ttu-id="80128-127">Hvis du vælger **Tilsidesæt prisfastsættelse**, er standardprisen ikke angivet.</span><span class="sxs-lookup"><span data-stu-id="80128-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="80128-128">Du skal i stedet angive en pris for produktet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="80128-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="80128-129">Hvis du vælger **Brug standard**, bruges standardsalgsprisen, og feltet er låst mod redigering.</span><span class="sxs-lookup"><span data-stu-id="80128-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="80128-130">Standardsalgspriserne angives på de produktbaserede linjer i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="80128-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="80128-131">Feltet **Prisfastsættelse** angives derefter til **Tilsidesæt prisfastsættelse**, så du kan redigere standardprisen i tilbudslinjerne.</span><span class="sxs-lookup"><span data-stu-id="80128-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="80128-132">Dette er en tilsidesættelse af projektbaserede linjers funktion i Dynamics 365 Sales, som er specifik for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="80128-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]