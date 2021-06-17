---
title: Deaktivering af en prisdimension
description: Dette emne indeholder oplysninger om, hvordan du deaktiverer prisfastsættelsesdimensioner.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004524"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="25a63-103">Deaktivering af en prisdimension</span><span class="sxs-lookup"><span data-stu-id="25a63-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="25a63-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="25a63-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25a63-105">Det kan være nødvendigt at gennemgå og opdatere din prisstrategi hvert andet eller tredje år.</span><span class="sxs-lookup"><span data-stu-id="25a63-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="25a63-106">Eventuelle opdateringer, du foretager, kræver måske, at du deaktiverer en eksisterende prisdimension og opretter en ny.</span><span class="sxs-lookup"><span data-stu-id="25a63-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="25a63-107">Du kan f.eks. tidligere have prissat ud fra **Rolle**, men nu har du besluttet at prissætte ud fra **Arbejdserfaring**.</span><span class="sxs-lookup"><span data-stu-id="25a63-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="25a63-108">Det kan kræve, at du deaktiverer **Rolle** som en prisfastsættelsesdimension og opretter **Arbejdserfaring** som en ny prisfastsættelsesdimension.</span><span class="sxs-lookup"><span data-stu-id="25a63-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="25a63-109">Du deaktiverer en prisdimension, uanset om den er standard eller brugerdefineret, ved at indstille felterne **Gælder for Omkostning** og **Gælder for Salg** i prisdimensionen til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="25a63-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="25a63-110">Men når du gør det, kan du få vist fejlmeddelelsen **Prisfastsættelsesdimensionen kan ikke opdateres eller slettes, hvis der er tilknyttede prisposter.**</span><span class="sxs-lookup"><span data-stu-id="25a63-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Forretningsprocesfejl er sandsynlig, når du deaktiverer en prisdimension](media/Business-Process-Error.png)

<span data-ttu-id="25a63-112">Denne fejlmeddelelse angiver, at der findes prisposter, der tidligere var konfigureret for den dimension, som bliver deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="25a63-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="25a63-113">Alle poster for **Rollepris** og **Rolleprisavance**, der refererer til en dimension, skal slettes, før dimensionens anvendelighed kan indstilles til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="25a63-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="25a63-114">Denne regel gælder både for standardprisdimensioner og eventuelle brugerdefinerede prisdimensioner, som du kan have oprettet.</span><span class="sxs-lookup"><span data-stu-id="25a63-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="25a63-115">Årsagen til denne validering er, at hver enkelt **Rollepris**-post skal have en entydig kombination af dimensioner.</span><span class="sxs-lookup"><span data-stu-id="25a63-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="25a63-116">På en prisliste, der hedder **US Cost Rates 2018**, har du f.eks. følgende **Rollepris**-rækker.</span><span class="sxs-lookup"><span data-stu-id="25a63-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="25a63-117">Standardtitel</span><span class="sxs-lookup"><span data-stu-id="25a63-117">Standard Title</span></span>         | <span data-ttu-id="25a63-118">Afdeling</span><span class="sxs-lookup"><span data-stu-id="25a63-118">Org Unit</span></span>    |<span data-ttu-id="25a63-119">Enhed</span><span class="sxs-lookup"><span data-stu-id="25a63-119">Unit</span></span>   |<span data-ttu-id="25a63-120">Pris</span><span class="sxs-lookup"><span data-stu-id="25a63-120">Price</span></span>  |<span data-ttu-id="25a63-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="25a63-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="25a63-122">Systemtekniker</span><span class="sxs-lookup"><span data-stu-id="25a63-122">Systems Engineer</span></span>|<span data-ttu-id="25a63-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="25a63-123">Contoso US</span></span>|<span data-ttu-id="25a63-124">Time</span><span class="sxs-lookup"><span data-stu-id="25a63-124">Hour</span></span>| <span data-ttu-id="25a63-125">100</span><span class="sxs-lookup"><span data-stu-id="25a63-125">100</span></span>|<span data-ttu-id="25a63-126">USD</span><span class="sxs-lookup"><span data-stu-id="25a63-126">USD</span></span>|
| <span data-ttu-id="25a63-127">Seniorsystemtekniker</span><span class="sxs-lookup"><span data-stu-id="25a63-127">Senior Systems Engineer</span></span>|<span data-ttu-id="25a63-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="25a63-128">Contoso US</span></span>|<span data-ttu-id="25a63-129">Time</span><span class="sxs-lookup"><span data-stu-id="25a63-129">Hour</span></span>| <span data-ttu-id="25a63-130">150</span><span class="sxs-lookup"><span data-stu-id="25a63-130">150</span></span>| <span data-ttu-id="25a63-131">USD</span><span class="sxs-lookup"><span data-stu-id="25a63-131">USD</span></span>|


<span data-ttu-id="25a63-132">Når du deaktiverer **Standardtitel** som prisfastsættelsesdimension, og prisfastsættelsesfunktionen søger efter en pris, bruger den kun værdien **Afdeling** fra inputkonteksten.</span><span class="sxs-lookup"><span data-stu-id="25a63-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="25a63-133">Hvis **Afdeling** i inputkonteksten er "Contoso USA", er resultatet ikke-deterministisk, da begge rækker stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="25a63-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="25a63-134">Hvis du vil undgå dette scenario, validerer systemet, at kombinationen af dimensioner er entydig, når du opretter **Rollepris**-poster.</span><span class="sxs-lookup"><span data-stu-id="25a63-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="25a63-135">Hvis dimensionen er blevet deaktiveret, efter at **Rollepris**-posterne er oprettet, kan denne begrænsning blive overtrådt.</span><span class="sxs-lookup"><span data-stu-id="25a63-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="25a63-136">Det er derfor nødvendigt, at du sletter alle rækker med **Rollepris** og **Rolleprisavance**, der har den pågældende dimensionsværdi udfyldt, før du deaktiverer en dimension.</span><span class="sxs-lookup"><span data-stu-id="25a63-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]