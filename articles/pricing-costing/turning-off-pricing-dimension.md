---
title: Deaktivering af en prisdimension
description: Dette emne indeholder oplysninger om, hvordan du deaktiverer prisfastsættelsesdimensioner.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650042"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="7d2f2-103">Deaktivering af en prisdimension</span><span class="sxs-lookup"><span data-stu-id="7d2f2-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="7d2f2-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="7d2f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d2f2-105">Det kan være nødvendigt at gennemgå og opdatere din prisstrategi hvert andet eller tredje år.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="7d2f2-106">Eventuelle opdateringer, du foretager, kræver måske, at du deaktiverer en eksisterende prisdimension og opretter en ny.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="7d2f2-107">Du kan f.eks. tidligere have prissat ud fra **Rolle**, men nu har du besluttet at prissætte ud fra **Arbejdserfaring**.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="7d2f2-108">Det kan kræve, at du deaktiverer **Rolle** som en prisfastsættelsesdimension og opretter **Arbejdserfaring** som en ny prisfastsættelsesdimension.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="7d2f2-109">Du deaktiverer en prisdimension, uanset om den er standard eller brugerdefineret, ved at indstille felterne **Gælder for Omkostning** og **Gælder for Salg** i prisdimensionen til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="7d2f2-110">Men når du gør det, kan du få vist fejlmeddelelsen **Prisfastsættelsesdimensionen kan ikke opdateres eller slettes, hvis der er tilknyttede prisposter.**</span><span class="sxs-lookup"><span data-stu-id="7d2f2-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Forretningsprocesfejl er sandsynlig, når du deaktiverer en prisdimension](media/Business-Process-Error.png)

<span data-ttu-id="7d2f2-112">Denne fejlmeddelelse angiver, at der findes prisposter, der tidligere var konfigureret for den dimension, som bliver deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="7d2f2-113">Alle poster for **Rollepris** og **Rolleprisavance**, der refererer til en dimension, skal slettes, før dimensionens anvendelighed kan indstilles til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="7d2f2-114">Denne regel gælder både for standardprisdimensioner og eventuelle brugerdefinerede prisdimensioner, som du kan have oprettet.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="7d2f2-115">Årsagen til denne validering er, at hver enkelt **Rollepris**-post skal have en entydig kombination af dimensioner.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="7d2f2-116">På en prisliste, der hedder **US Cost Rates 2018**, har du f.eks. følgende **Rollepris**-rækker.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="7d2f2-117">Standardtitel</span><span class="sxs-lookup"><span data-stu-id="7d2f2-117">Standard Title</span></span>         | <span data-ttu-id="7d2f2-118">Afdeling</span><span class="sxs-lookup"><span data-stu-id="7d2f2-118">Org Unit</span></span>    |<span data-ttu-id="7d2f2-119">Enhed</span><span class="sxs-lookup"><span data-stu-id="7d2f2-119">Unit</span></span>   |<span data-ttu-id="7d2f2-120">Pris</span><span class="sxs-lookup"><span data-stu-id="7d2f2-120">Price</span></span>  |<span data-ttu-id="7d2f2-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="7d2f2-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="7d2f2-122">Systemtekniker</span><span class="sxs-lookup"><span data-stu-id="7d2f2-122">Systems Engineer</span></span>|<span data-ttu-id="7d2f2-123">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="7d2f2-123">Contoso US</span></span>|<span data-ttu-id="7d2f2-124">Hour</span><span class="sxs-lookup"><span data-stu-id="7d2f2-124">Hour</span></span>| <span data-ttu-id="7d2f2-125">100</span><span class="sxs-lookup"><span data-stu-id="7d2f2-125">100</span></span>|<span data-ttu-id="7d2f2-126">USD</span><span class="sxs-lookup"><span data-stu-id="7d2f2-126">USD</span></span>|
| <span data-ttu-id="7d2f2-127">Seniorsystemtekniker</span><span class="sxs-lookup"><span data-stu-id="7d2f2-127">Senior Systems Engineer</span></span>|<span data-ttu-id="7d2f2-128">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="7d2f2-128">Contoso US</span></span>|<span data-ttu-id="7d2f2-129">Hour</span><span class="sxs-lookup"><span data-stu-id="7d2f2-129">Hour</span></span>| <span data-ttu-id="7d2f2-130">150</span><span class="sxs-lookup"><span data-stu-id="7d2f2-130">150</span></span>| <span data-ttu-id="7d2f2-131">USD</span><span class="sxs-lookup"><span data-stu-id="7d2f2-131">USD</span></span>|


<span data-ttu-id="7d2f2-132">Når du deaktiverer **Standardtitel** som prisfastsættelsesdimension, og prisfastsættelsesfunktionen søger efter en pris, bruger den kun værdien **Afdeling** fra inputkonteksten.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="7d2f2-133">Hvis **Afdeling** i inputkonteksten er "Contoso US", er resultatet ikke-deterministisk, da begge rækker stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="7d2f2-134">Hvis du vil undgå dette scenario, validerer systemet, at kombinationen af dimensioner er entydig, når du opretter **Rollepris**-poster.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="7d2f2-135">Hvis dimensionen er blevet deaktiveret, efter at **Rollepris**-posterne er oprettet, kan denne begrænsning blive overtrådt.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="7d2f2-136">Det er derfor nødvendigt, at du sletter alle rækker med **Rollepris** og **Rolleprisavance**, der har den pågældende dimensionsværdi udfyldt, før du deaktiverer en dimension.</span><span class="sxs-lookup"><span data-stu-id="7d2f2-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
