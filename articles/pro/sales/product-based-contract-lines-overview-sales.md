---
title: Oversigt over produktbaserede kontraktlinjer
description: Dette emne indeholder oplysninger om produktbaserede kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074099"
---
# <a name="product-based-contract-lines-overview"></a><span data-ttu-id="b8486-103">Oversigt over produktbaserede kontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="b8486-103">Product-based contract lines overview</span></span>

<span data-ttu-id="b8486-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b8486-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b8486-105">Du kan oprette produktbaserede kontraktlinjer i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b8486-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="b8486-106">Produktbaserede kontraktlinjer kan være manuelt oprettede linjer, eller de kan være elementer fra produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="b8486-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="b8486-107">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="b8486-107">Product catalog</span></span>

<span data-ttu-id="b8486-108">Produkterne i produktkataloget har en standardenhed og enhedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b8486-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="b8486-109">Hvis flere produkter deler det samme sæt attributter, kan du oprette en produktfamilie, der også har de pågældende attributter.</span><span class="sxs-lookup"><span data-stu-id="b8486-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="b8486-110">Alle produkter i én produktfamilie arver det samme sæt attributter.</span><span class="sxs-lookup"><span data-stu-id="b8486-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="b8486-111">Et firma sælger f.eks. abonnementslicenser til forskellige typer af software.</span><span class="sxs-lookup"><span data-stu-id="b8486-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="b8486-112">Alle abonnementsprogrammer har følgende to attributter:</span><span class="sxs-lookup"><span data-stu-id="b8486-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="b8486-113">Antal brugere</span><span class="sxs-lookup"><span data-stu-id="b8486-113">Number of users</span></span>
- <span data-ttu-id="b8486-114">Abonnements varighed (i måneder)</span><span class="sxs-lookup"><span data-stu-id="b8486-114">Subscription duration (in months)</span></span>

<span data-ttu-id="b8486-115">Hvis du vil bibeholde denne type katalog, skal du oprette en produktfamilie kaldet **Abonnementssoftware**.</span><span class="sxs-lookup"><span data-stu-id="b8486-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="b8486-116">Tilføj attributterne **Antal brugere** og **Abonnementsvarighed** til produktfamilien.</span><span class="sxs-lookup"><span data-stu-id="b8486-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="b8486-117">Tilføj derefter de enkelte produkter til produktfamilien **Abonnementssoftware**.</span><span class="sxs-lookup"><span data-stu-id="b8486-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="b8486-118">Tilføj produktkatalogelementer til en projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="b8486-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="b8486-119">Projektkontrakter indeholder afsnit til to typer linjer, nemlig projektbaserede linjer og produktbaserede linjer.</span><span class="sxs-lookup"><span data-stu-id="b8486-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="b8486-120">Produktbaserede linjer omfatter alle produkter og enheder i produktprislisten på kontrakten.</span><span class="sxs-lookup"><span data-stu-id="b8486-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="b8486-121">Produkter, der ikke er en del af en kontrakts produktprisliste, kan tilføjes.</span><span class="sxs-lookup"><span data-stu-id="b8486-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="b8486-122">Du kan vælge produkter fra andre prislister eller direkte fra produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="b8486-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="b8486-123">Når du vælger produkter direkte fra et produktkatalog, bruges standardprislisten for produktet som produktets salgspris.</span><span class="sxs-lookup"><span data-stu-id="b8486-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="b8486-124">Hvis der ikke er angivet en standardprisliste, angives prisen til 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="b8486-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="b8486-125">Hvis en kontraktlinje er baseret på et produktkatalog, kan du tilsidesætte salgsprisen direkte på linjen.</span><span class="sxs-lookup"><span data-stu-id="b8486-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="b8486-126">En kontraktlinje indeholder feltet **Prisfastsættelse** med de to værdier:</span><span class="sxs-lookup"><span data-stu-id="b8486-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="b8486-127">**Tilsidesæt prisfastsættelse**</span><span class="sxs-lookup"><span data-stu-id="b8486-127">**Override pricing**</span></span>
- <span data-ttu-id="b8486-128">**Benyt standard**</span><span class="sxs-lookup"><span data-stu-id="b8486-128">**Use default**</span></span>

<span data-ttu-id="b8486-129">Hvis du angiver feltet **Prisfastsættelse** til **Tilsidesæt prisfastsættelse** , angives standardprisen ikke.</span><span class="sxs-lookup"><span data-stu-id="b8486-129">If you set the **Pricing** field to **Override pricing** , the default price isn't set.</span></span> <span data-ttu-id="b8486-130">Angiv en pris for produktet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="b8486-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="b8486-131">Hvis du angiver feltet som **Brug standard** , bruges standardsalgsprisen, og feltet kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="b8486-131">If you set the field to **Use default** , the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="b8486-132">Når du har installeret Project Operations, angives standardsalgspriserne på de produktbaserede linjer i en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="b8486-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="b8486-133">Feltet **Prisfastsættelse** indstilles til **Tilsidesæt prisfastsættelse** , så du kan redigere standardprisen i kontraktlinjerne.</span><span class="sxs-lookup"><span data-stu-id="b8486-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="b8486-134">Dette er en tilsidesættelse specifik for Project Operations for produktbaserede linjers funktion i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b8486-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
