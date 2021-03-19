---
title: Produktbaserede tilbudslinjer.
description: Dette emne indeholder oplysninger om produktbaserede tilbudslinjer.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284081"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="f3128-103">Produktbaserede tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="f3128-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="f3128-104">Du kan oprette produktbaserede tilbudslinjer i Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f3128-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="f3128-105">Produktbaserede tilbudslinjer kan være "linjer, der skal rekvireres", eller de kan være elementer fra produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="f3128-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="f3128-106">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="f3128-106">Product catalog</span></span>

<span data-ttu-id="f3128-107">Produkterne i et Dynamics 365-produktkatalog har en standardenhed og enhedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3128-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="f3128-108">Hvis flere produkter deler det samme sæt attributter, kan du oprette en produktfamilie, der også har de pågældende attributter.</span><span class="sxs-lookup"><span data-stu-id="f3128-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="f3128-109">Alle produkter i én produktfamilie arver det samme sæt attributter.</span><span class="sxs-lookup"><span data-stu-id="f3128-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="f3128-110">Et firma sælger f.eks. abonnementslicenser til forskellige typer programmer.</span><span class="sxs-lookup"><span data-stu-id="f3128-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="f3128-111">Alle abonnementsprogrammer har følgende to attributter:</span><span class="sxs-lookup"><span data-stu-id="f3128-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="f3128-112">Antal brugere</span><span class="sxs-lookup"><span data-stu-id="f3128-112">Number of users</span></span> 
- <span data-ttu-id="f3128-113">Abonnements varighed (i måneder)</span><span class="sxs-lookup"><span data-stu-id="f3128-113">Subscription duration (in months)</span></span>

<span data-ttu-id="f3128-114">En god måde at vedligeholde denne type katalog på er at oprette en produktserie med navnet **Abonnementsprogrammer**, og som har **Antal brugere** og **Abonnements varighed** som attributter.</span><span class="sxs-lookup"><span data-stu-id="f3128-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="f3128-115">Du kan derefter føje individuelle produkter, f.eks. **Dynamics 365 Sales** eller **Dynamics 365 Field Service**, til produktserien **Abonnementsprogrammer**.</span><span class="sxs-lookup"><span data-stu-id="f3128-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="f3128-116">Tilføjelse af produktkatalogelementer til et projekttilbud</span><span class="sxs-lookup"><span data-stu-id="f3128-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="f3128-117">Siderne for projekttilbud og projektkontrakter indeholder afsnit til to typer linjer: projektbaserede linjer og produktbaserede linjer.</span><span class="sxs-lookup"><span data-stu-id="f3128-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="f3128-118">I forbindelse med produktbaserede linjer bruges Dynamics 365 til at føje elementer fra et produktkatalog til et tilbud.</span><span class="sxs-lookup"><span data-stu-id="f3128-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="f3128-119">Rullelisten på tilbudslinjen eller på projektkontraktlinjen indeholder alle de produkter og enheder i produktprislisten, der er knyttet til tilbuddet eller projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="f3128-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="f3128-120">Du kan også tilføje produkter, der ikke er en del af et tilbuds produktprisliste.</span><span class="sxs-lookup"><span data-stu-id="f3128-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="f3128-121">Derudover kan du vælge produkter fra andre prislister, eller du kan vælge produkter direkte fra produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="f3128-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="f3128-122">Når du vælger produkter direkte fra et produktkatalog, bruges standardprislisten for produktet til at beregne produktets salgspris.</span><span class="sxs-lookup"><span data-stu-id="f3128-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="f3128-123">Hvis der ikke er angivet en standardprisliste, angives prisen til 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="f3128-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="f3128-124">Hvis en tilbudslinje er baseret på et produktkatalog, kan du tilsidesætte salgsprisen direkte på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="f3128-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="f3128-125">Bemærk, at en tilbudslinje i Dynamics 365 har feltet **Prisfastsættelse**.</span><span class="sxs-lookup"><span data-stu-id="f3128-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="f3128-126">Der findes følgende to værdier:</span><span class="sxs-lookup"><span data-stu-id="f3128-126">Two values are available:</span></span>

- <span data-ttu-id="f3128-127">Tilsidesæt prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="f3128-127">Override pricing</span></span>  
- <span data-ttu-id="f3128-128">Benyt som standard</span><span class="sxs-lookup"><span data-stu-id="f3128-128">Use default</span></span>

<span data-ttu-id="f3128-129">Hvis du angiver dette felt til **Tilsidesæt prisfastsættelse**, angives der ikke en standardpris i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f3128-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="f3128-130">Du skal angive en pris for produktet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="f3128-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="f3128-131">Hvis du angiver dette felt til **Benyt som standard**, bruger Dynamics 365 standardsalgsprisen og låser feltet for at forhindre, at der redigeres.</span><span class="sxs-lookup"><span data-stu-id="f3128-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="f3128-132">Når du har installeret PSA, angives standardsalgspriserne på de produktbaserede linjer i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="f3128-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="f3128-133">Feltet **Prisfastsættelse** indstilles derefter til **Tilsidesæt prisfastsættelse**, så du kan redigere standardprisen i tilbudslinjerne.</span><span class="sxs-lookup"><span data-stu-id="f3128-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Indstilling af tilsidesæt prisfastsættelse](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="f3128-135">Mængdefaktorer for produkter</span><span class="sxs-lookup"><span data-stu-id="f3128-135">Quantity factors for products</span></span>

<span data-ttu-id="f3128-136">I PSA bruges mængdefaktorer til at understøtte salget af abonnementsbaserede produkter.</span><span class="sxs-lookup"><span data-stu-id="f3128-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="f3128-137">I forbindelse med abonnementsbaserede produkter udtrykkes antallet i tilbuds- eller projektkontraktlinjen som antallet af brugermåneder.</span><span class="sxs-lookup"><span data-stu-id="f3128-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="f3128-138">Prisen for abonnementsprogrammer gemmes som regel i kataloget som pris pr. bruger pr. måned.</span><span class="sxs-lookup"><span data-stu-id="f3128-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="f3128-139">Men du kan også bruge andre tidsbeskrivelser i stedet.</span><span class="sxs-lookup"><span data-stu-id="f3128-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="f3128-140">Under salgsprocessen er prisen i tilbudslinjen som regel den pris pr. bruger, pris pr. måned, som blev forhandlet og fratrukket af IT-salgsagenten.</span><span class="sxs-lookup"><span data-stu-id="f3128-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="f3128-141">Hver handel har et forskelligt antal brugere og et forskelligt antal abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="f3128-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="f3128-142">Det antal, der bruges til at beregne beløbet i tilbudslinjen, er et produkt af antallet af brugere og antallet af abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="f3128-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="f3128-143">For at understøtte denne type salg introduceres konceptet med mængdefaktorer i PSA.</span><span class="sxs-lookup"><span data-stu-id="f3128-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="f3128-144">Mængdefaktorer er baseret på produktattributterne i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f3128-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="f3128-145">Når du konfigurerer bestemte egenskaber for et produkt, giver PSA dig mulighed for at markere et undersæt af disse egenskaber eller alle egenskaberne som mængdefaktorer.</span><span class="sxs-lookup"><span data-stu-id="f3128-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="f3128-146">PSA validerer, at kun numeriske egenskaber eller produktegenskaber med numerisk datatype markeres som mængdefaktorer.</span><span class="sxs-lookup"><span data-stu-id="f3128-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="f3128-147">Når et produkt, som der konfigureres mængdefaktorer for, føjes til en tilbudslinje, bliver feltet **Antal** i tilbudslinjen et skrivebeskyttet felt.</span><span class="sxs-lookup"><span data-stu-id="f3128-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="f3128-148">Når du har angivet værdier for produktegenskaber, der er mængdefaktorer, beregner PSA antallet i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="f3128-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="f3128-149">Dynamics 365 kan f.eks. have følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="f3128-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="f3128-150">**Antal brugere** – Antallet af brugere</span><span class="sxs-lookup"><span data-stu-id="f3128-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="f3128-151">**Antal måneder** – Antallet af abonnementsmåneder</span><span class="sxs-lookup"><span data-stu-id="f3128-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="f3128-152">**Produkt-SKU**</span><span class="sxs-lookup"><span data-stu-id="f3128-152">**Product SKU**</span></span> 

<span data-ttu-id="f3128-153">Egenskaberne **Antal brugere** og **Antal måneder** kan mærkes som mængdefaktorer ved at redigere egenskaberne for produktlinjen.</span><span class="sxs-lookup"><span data-stu-id="f3128-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Mærkning af Antal brugere og Antal måneder som kvalitetsfaktorer](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]