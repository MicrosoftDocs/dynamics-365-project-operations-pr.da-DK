---
title: Slå en prisdimension fra
description: I dette emne vises, hvordan du kan konfigurere prisdimensioner i Project Service-løsningen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281831"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="19717-103">Slå en prisdimension fra</span><span class="sxs-lookup"><span data-stu-id="19717-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="19717-104">Det kan være nødvendigt at gennemgå og opdatere din prisstrategi hvert andet eller tredje år.</span><span class="sxs-lookup"><span data-stu-id="19717-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="19717-105">Eventuelle opdateringer, du foretager, kræver måske, at du deaktiverer en eksisterende prisdimension og opretter en ny.</span><span class="sxs-lookup"><span data-stu-id="19717-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="19717-106">Du kan f.eks. tidligere have prissat ud fra **Rolle**, men nu har du besluttet at prissætte ud fra **Arbejdserfaring**.</span><span class="sxs-lookup"><span data-stu-id="19717-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="19717-107">Det kan kræve, at du deaktiverer **Rolle** som en prisdimension og opretter **Arbejdserfaring** som en ny prisdimension.</span><span class="sxs-lookup"><span data-stu-id="19717-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="19717-108">Du deaktiverer en prisdimension, uanset om den er standard eller brugerdefineret, ved at indstille felterne **Gælder for Omkostning** og **Gælder for Salg** i prisdimensionen til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="19717-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="19717-109">Men når du gør dette, modtager du måske følgende fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="19717-109">However, when you do this, you might receive the following error message.</span></span>

![Forretningsprocesfejl er sandsynlig, når du deaktiverer en prisdimension](media/Business-Process-Error.png)


<span data-ttu-id="19717-111">Denne fejlmeddelelse angiver, at der findes prisposter, der tidligere var konfigureret for den dimension, som bliver deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="19717-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="19717-112">Alle poster for **Rollepris** og **Rolleprisavance**, der refererer til en dimension, skal slettes, før dimensionens anvendelighed kan indstilles til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="19717-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="19717-113">Denne regel gælder både for standardprisdimensioner og eventuelle brugerdefinerede prisdimensioner, som du kan have oprettet.</span><span class="sxs-lookup"><span data-stu-id="19717-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="19717-114">Årsagen til denne validering er, at Project Service har den begrænsning, at hver enkelt **Rollepris**-post skal have en entydig kombination af dimensioner.</span><span class="sxs-lookup"><span data-stu-id="19717-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="19717-115">På en prisliste, der hedder **US Cost Rates 2018**, har du f.eks. følgende **Rollepris**-rækker.</span><span class="sxs-lookup"><span data-stu-id="19717-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="19717-116">Standardtitel</span><span class="sxs-lookup"><span data-stu-id="19717-116">Standard Title</span></span>         | <span data-ttu-id="19717-117">Afdeling</span><span class="sxs-lookup"><span data-stu-id="19717-117">Org Unit</span></span>    |<span data-ttu-id="19717-118">Enhed</span><span class="sxs-lookup"><span data-stu-id="19717-118">Unit</span></span>   |<span data-ttu-id="19717-119">Pris</span><span class="sxs-lookup"><span data-stu-id="19717-119">Price</span></span>  |<span data-ttu-id="19717-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="19717-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="19717-121">Systemtekniker</span><span class="sxs-lookup"><span data-stu-id="19717-121">Systems Engineer</span></span>|<span data-ttu-id="19717-122">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="19717-122">Contoso US</span></span>|<span data-ttu-id="19717-123">Hour</span><span class="sxs-lookup"><span data-stu-id="19717-123">Hour</span></span>| <span data-ttu-id="19717-124">100</span><span class="sxs-lookup"><span data-stu-id="19717-124">100</span></span>|<span data-ttu-id="19717-125">USD</span><span class="sxs-lookup"><span data-stu-id="19717-125">USD</span></span>|
| <span data-ttu-id="19717-126">Seniorsystemtekniker</span><span class="sxs-lookup"><span data-stu-id="19717-126">Senior Systems Engineer</span></span>|<span data-ttu-id="19717-127">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="19717-127">Contoso US</span></span>|<span data-ttu-id="19717-128">Hour</span><span class="sxs-lookup"><span data-stu-id="19717-128">Hour</span></span>| <span data-ttu-id="19717-129">150</span><span class="sxs-lookup"><span data-stu-id="19717-129">150</span></span>| <span data-ttu-id="19717-130">USD</span><span class="sxs-lookup"><span data-stu-id="19717-130">USD</span></span>|


<span data-ttu-id="19717-131">Når du slår **Standardtitel** fra som prisdimension, og prissætningsfunktionen i Project Service søger efter en pris, bruger den kun værdien **Afdeling** fra inputkonteksten.</span><span class="sxs-lookup"><span data-stu-id="19717-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="19717-132">Hvis **Afdeling** i inputkonteksten er "Contoso US", er resultatet ikke-deterministisk, da begge rækker stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="19717-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="19717-133">Hvis du vil undgå dette scenario, validerer Project Service, at kombinationen af dimensioner er entydig, når du opretter **Rollepris**-poster.</span><span class="sxs-lookup"><span data-stu-id="19717-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="19717-134">Hvis dimensionen er blevet deaktiveret, efter at **Rollepris**-posterne er oprettet, kan denne begrænsning blive overtrådt.</span><span class="sxs-lookup"><span data-stu-id="19717-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="19717-135">Det er derfor nødvendigt, at du sletter alle rækker med **Rollepris** og **Rolleprisavance**, der har den pågældende dimensionsværdi udfyldt, før du deaktiverer en dimension.</span><span class="sxs-lookup"><span data-stu-id="19717-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]