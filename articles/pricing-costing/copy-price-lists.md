---
title: Kopier prislister
description: Dette emne indeholder oplysninger om, hvordan du kopierer prislister i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074211"
---
# <a name="copy-price-lists"></a><span data-ttu-id="e78ab-103">Kopier prislister</span><span class="sxs-lookup"><span data-stu-id="e78ab-103">Copy price lists</span></span>

<span data-ttu-id="e78ab-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="e78ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e78ab-105">Du kan oprette kopier af prislister i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e78ab-105">You can create copies of price lists in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="e78ab-106">Du kan f.eks. oprette prislister for det kommende år ved hjælp af en prisliste fra det aktuelle år.</span><span class="sxs-lookup"><span data-stu-id="e78ab-106">For example, you can create price lists for the upcoming year using a price list from the current year.</span></span>  <span data-ttu-id="e78ab-107">Du kan også kopiere en prisliste for faktureringssatser og salgspriser fra prislisterne for omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e78ab-107">Or, you might copy a price list for bill rates and sales prices from the price lists for cost.</span></span> 

<span data-ttu-id="e78ab-108">Hvis du vil oprette en kopi af prislisten, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="e78ab-108">To make a copy of price list, complete the following steps.</span></span>

1. <span data-ttu-id="e78ab-109">Åbn den prisliste, som du vil oprette en kopi af, og vælg **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="e78ab-109">Open the price list that you want to make a copy of and select **Copy**.</span></span>
2. <span data-ttu-id="e78ab-110">Angiv de nødvendige oplysninger for at kopiere prislisten.</span><span class="sxs-lookup"><span data-stu-id="e78ab-110">Enter any necessary information to copy the price list.</span></span> <span data-ttu-id="e78ab-111">I følgende tabel vises overvejelser, du skal huske, når du angiver oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e78ab-111">The following table shows considerations to keep in mind when entering information.</span></span>

| <span data-ttu-id="e78ab-112">Felt</span><span class="sxs-lookup"><span data-stu-id="e78ab-112">Field</span></span> | <span data-ttu-id="e78ab-113">Relevans, formål og vejledning</span><span class="sxs-lookup"><span data-stu-id="e78ab-113">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="e78ab-114">Downstream-virkning</span><span class="sxs-lookup"><span data-stu-id="e78ab-114">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e78ab-115">Navn</span><span class="sxs-lookup"><span data-stu-id="e78ab-115">Name</span></span> | <span data-ttu-id="e78ab-116">Navnet på kildeprislisten, hvor der er tilføjet **-kopien**.</span><span class="sxs-lookup"><span data-stu-id="e78ab-116">The name of the source price list with the **-copy** appended.</span></span> | <span data-ttu-id="e78ab-117">Prislisten inkluderer denne værdi på alle listesider og indstillinger for rullelister.</span><span class="sxs-lookup"><span data-stu-id="e78ab-117">The price list includes this value on all list pages and drop-down options.</span></span> |
| <span data-ttu-id="e78ab-118">Sammenhæng</span><span class="sxs-lookup"><span data-stu-id="e78ab-118">Context</span></span> | <span data-ttu-id="e78ab-119">Angiv den kontekst, der skal vises for destinationsprislisten.</span><span class="sxs-lookup"><span data-stu-id="e78ab-119">Enter the context that you want for the target price list.</span></span> | <span data-ttu-id="e78ab-120">En prisliste med konteksten **Omkostninger** bruges til at slå prisen for omkostningsestimater og faktiske omkostningsværdier op.</span><span class="sxs-lookup"><span data-stu-id="e78ab-120">A price list that has the context set to **Cost** is used to look up the price for cost estimates and cost actuals.</span></span> <span data-ttu-id="e78ab-121">En prisliste med konteksten **Salg** bruges til at slå prisen for salgsestimater og faktiske salgsværdier op.</span><span class="sxs-lookup"><span data-stu-id="e78ab-121">A price list that has the context set to **Sales** is used to look up price for sales estimates and sales actuals.</span></span> <span data-ttu-id="e78ab-122">Kun prislister med konteksten **Salg** kan tilknyttes en projektprisliste for en kunde, tilbud eller kontrakt.</span><span class="sxs-lookup"><span data-stu-id="e78ab-122">Only price lists that have the context set to **Sales** can be attached to a project price list for a customer, quotes, or contract.</span></span> |
| <span data-ttu-id="e78ab-123">Startdato</span><span class="sxs-lookup"><span data-stu-id="e78ab-123">Start Date</span></span> | <span data-ttu-id="e78ab-124">Startdatoen for den periode, hvor prislisten er gældende.</span><span class="sxs-lookup"><span data-stu-id="e78ab-124">The start date of the period in which is price list is effective.</span></span> | <span data-ttu-id="e78ab-125">Sammen med **Slutdato** bruges dette felt til at afgøre, hvilken prisliste der gælder for en bestemt estimatlinje eller faktisk linje.</span><span class="sxs-lookup"><span data-stu-id="e78ab-125">Together with **End Date** , this field is used to determine which price list is applicable for a certain estimate or actual line.</span></span> |
| <span data-ttu-id="e78ab-126">Slutdato</span><span class="sxs-lookup"><span data-stu-id="e78ab-126">End Date</span></span> | <span data-ttu-id="e78ab-127">Slutdatoen for den periode, hvor prislisten er gældende.</span><span class="sxs-lookup"><span data-stu-id="e78ab-127">The end date of the period in which is price list is effective.</span></span> | <span data-ttu-id="e78ab-128">Sammen med **Startdato** bruges dette felt til at afgøre, hvilken prisliste der gælder for en bestemt estimatlinje eller en faktisk linje.</span><span class="sxs-lookup"><span data-stu-id="e78ab-128">Together with **Start Date** , this field is used to determine which price list is applicable for a certain estimate or actual line.</span></span> |
| <span data-ttu-id="e78ab-129">Valuta</span><span class="sxs-lookup"><span data-stu-id="e78ab-129">Currency</span></span> | <span data-ttu-id="e78ab-130">Destinationsprislistens valuta.</span><span class="sxs-lookup"><span data-stu-id="e78ab-130">The currency of the source price list.</span></span> <span data-ttu-id="e78ab-131">Denne kan ændres.</span><span class="sxs-lookup"><span data-stu-id="e78ab-131">This can be changed.</span></span> | <span data-ttu-id="e78ab-132">Når denne ændring er foretaget, konverteres alle elementer i de nye prislinjer for arbejdskraft, udgifter og produktkatalog til destinationsprislistens valuta i forbindelse med kopieringen.</span><span class="sxs-lookup"><span data-stu-id="e78ab-132">When this is changed, all resulting price lines for labor, expense, and product catalog items are converted to the target price list currency during the copy.</span></span> |
| <span data-ttu-id="e78ab-133">Tidsenhed</span><span class="sxs-lookup"><span data-stu-id="e78ab-133">Time Unit</span></span> | <span data-ttu-id="e78ab-134">Destinationsprislistens valuta.</span><span class="sxs-lookup"><span data-stu-id="e78ab-134">The currency of the source price list.</span></span> <span data-ttu-id="e78ab-135">Denne kan ændres.</span><span class="sxs-lookup"><span data-stu-id="e78ab-135">This can be changed.</span></span> | <span data-ttu-id="e78ab-136">Når denne ændring er foretaget, konverteres alle de nye prislinjer for arbejdskraftselementer til destinationsprislistens undermodul i forbindelse med kopieringen.</span><span class="sxs-lookup"><span data-stu-id="e78ab-136">When this is changed, all the resulting price lines for labor items are converted to the target price list unit during the copy.</span></span> <span data-ttu-id="e78ab-137">Konverteringen fra opsætningen af undermodulet for tid i kildeprislisten og destinationsprislistens undermodul for tid bruges.</span><span class="sxs-lookup"><span data-stu-id="e78ab-137">The conversion from the unit setup for the source price list time unit and target price list time unit is used.</span></span> |
| <span data-ttu-id="e78ab-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e78ab-138">Description</span></span> | <span data-ttu-id="e78ab-139">En beskrivelse af kildeprislisten med tilføjelsen **-kopien**.</span><span class="sxs-lookup"><span data-stu-id="e78ab-139">A description of the source price list with the **-copy** appended.</span></span> <span data-ttu-id="e78ab-140">Dette er et tekstfelt, som giver dig mulighed for at få en beskrivelse af prislisten på flere linjer.</span><span class="sxs-lookup"><span data-stu-id="e78ab-140">This is a text field and allows you to have multi-line description of the price list.</span></span> | <span data-ttu-id="e78ab-141">Dette felt vises i de **Tilknyttede** visninger på prislisten i forskellige objekter, der har relaterede prislister.</span><span class="sxs-lookup"><span data-stu-id="e78ab-141">This field is shown in the **Associated** views on the price list in various entities that have related price lists.</span></span> |

3. <span data-ttu-id="e78ab-142">Gem prislisten.</span><span class="sxs-lookup"><span data-stu-id="e78ab-142">Save the price list.</span></span> 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a><span data-ttu-id="e78ab-143">Opdater en prisliste ved at anvende en avance for alle priser</span><span class="sxs-lookup"><span data-stu-id="e78ab-143">Update a price list by applying a mark-up to all the prices</span></span>

1. <span data-ttu-id="e78ab-144">På fanerne **Rolle** , **Kategori** og **Prislisteelement** i en prisliste kan du vælge **Opdater priser** for at anvende en avance for alle priser i undergitteret.</span><span class="sxs-lookup"><span data-stu-id="e78ab-144">On the **Role** , **Category** , and **Price List Item** tabs of a price list, you can select **Update Prices** to apply a markup for all prices in the sub-grid.</span></span> 
2. <span data-ttu-id="e78ab-145">Angiv en avance på den dialogside, der vises.</span><span class="sxs-lookup"><span data-stu-id="e78ab-145">On the dialog page that opens, enter a mark-up.</span></span> <span data-ttu-id="e78ab-146">Du kan også angive en negativ avanceprocent for at reducere priserne med en bestemt procentdel.</span><span class="sxs-lookup"><span data-stu-id="e78ab-146">You can also enter a negative mark-up percent to decrease prices by a certain percentage.</span></span> 
3. <span data-ttu-id="e78ab-147">Vælg **OK** på dialogsiden, og kontrollér derefter, at priserne i undergitteret afspejler de ændringer, du har foretaget.</span><span class="sxs-lookup"><span data-stu-id="e78ab-147">Select **OK** on the dialog page and then verify that the prices in the sub-grid reflect the changes you made.</span></span>