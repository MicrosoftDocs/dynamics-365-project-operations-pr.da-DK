---
title: Hvorfor anvendes en standardpris på nul for faktiske tidsrelaterede omkostninger?
description: Fejlfinding af, hvorfor en pris får standardværdien 0 for faktiske tidsrelaterede omkostninger.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 65f2bc773a376800928cc3746691061d8e290f74
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285791"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="67702-103">Hvorfor anvendes en standardpris på nul for faktiske tidsrelaterede omkostninger?</span><span class="sxs-lookup"><span data-stu-id="67702-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="67702-104">Disse ofte stillede spørgsmål gælder for faktiske værdier, hvor transaktionsklassen er indstillet til Tid, og transaktionstypen er Omkostning.</span><span class="sxs-lookup"><span data-stu-id="67702-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="67702-105">Følgende tre kontroller hjælper dig med at foretage fejlfinding af grunden til, at standardprisen på 0 anvendes til faktiske tidsrelaterede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="67702-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="67702-106">Kontrol 1: Find kostprislisten for projektet</span><span class="sxs-lookup"><span data-stu-id="67702-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="67702-107">Find projektet fra projektfeltet for den faktiske værdi, og gå derefter til projektsiden.</span><span class="sxs-lookup"><span data-stu-id="67702-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="67702-108">Klik på linket til kontraktenheden i feltet.</span><span class="sxs-lookup"><span data-stu-id="67702-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="67702-109">Kontroller, om kontraktenheden har en prisliste i gitteret Kostprislister, på siden Kontraktenhed.</span><span class="sxs-lookup"><span data-stu-id="67702-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="67702-110">Hvis der er mere end én prisliste, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="67702-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="67702-111">Project Service understøtter kun én prisliste pr. afdeling.</span><span class="sxs-lookup"><span data-stu-id="67702-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="67702-112">Fjern alle prislister fra dette objekt, indtil der kun én prisliste tilknyttet i gitteret Kostprislister for afdelingen.</span><span class="sxs-lookup"><span data-stu-id="67702-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="67702-113">Hvis der ikke er en prisliste knyttet til afdelingen, skal du notere valutaen i afdelingen.</span><span class="sxs-lookup"><span data-stu-id="67702-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="67702-114">Gå til Project Service og til Parametre, og åbn fanen Prislister. Kontroller, om der er nogen prislister, hvor konteksten er indstillet til Omkostninger og valuta, og som stemmer overens med valutaen i afdelingen.</span><span class="sxs-lookup"><span data-stu-id="67702-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="67702-115">Hvis der ikke er nogen prislister, der svarer til de pågældende kriterier, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="67702-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="67702-116">Sørg for, at du har mindst én prisliste, hvis kontekst er indstillet til Omkostninger, og hvis valuta svarer til valutaen i afdelingen.</span><span class="sxs-lookup"><span data-stu-id="67702-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="67702-117">Hvis der findes mere end én prisliste, der svarer til de pågældende kriterier, skal du fortsætte med at læse dette dokument for at foretage yderligere kontrol.</span><span class="sxs-lookup"><span data-stu-id="67702-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="67702-118">Kontrol 2: Er der nogen af de prislister, der er angivet ovenfor, gyldige for den specifikke dato for den faktiske tidsrelaterede omkostning?</span><span class="sxs-lookup"><span data-stu-id="67702-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="67702-119">Hvis Project Service skal tage en prisliste for standardprisen i betragtning, skal denne prisliste gælde for datoen i den faktiske tidsrelaterede omkostning.</span><span class="sxs-lookup"><span data-stu-id="67702-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="67702-120">Kontroller følgende for at se, om de prislister, der er identificeret overfor, gælder:</span><span class="sxs-lookup"><span data-stu-id="67702-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="67702-121">Kontroller, at start- og slutdatoer under fanen Generelt for de prislister, der er tilknyttet, ikke er tomme.</span><span class="sxs-lookup"><span data-stu-id="67702-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="67702-122">Hvis start- og slutdatoerne til i prislisterne ovenfor, er tomme, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="67702-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="67702-123">Noter startdatofeltet i den faktiske tidsrelaterede omkostning, og kontroller, om en eller flere af de prislister, der er identificeret, er relevant for denne dato.</span><span class="sxs-lookup"><span data-stu-id="67702-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="67702-124">Eksempelvis skal datoen for den faktiske tidsrelaterede omkostning ligge inden for start- og slutdatoen på prislisten.</span><span class="sxs-lookup"><span data-stu-id="67702-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="67702-125">Hvis der ikke er en prisliste, der dækker denne dato på den faktiske tidsrelaterede omkostning, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="67702-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="67702-126">Du skal ændre start- og slutdatoer på prislisten for at sikre, at prislisten omfatter datoen for den faktiske tidsrelaterede omkostning.</span><span class="sxs-lookup"><span data-stu-id="67702-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="67702-127">Hvis der er mere end én prisliste, der dækker datoen for den faktiske tidsrelaterede omkostning, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="67702-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="67702-128">Du kan løse dette problem ved at redigere start- og slutdatoerne på prislisterne, så der er kun én prisliste, der dækker datoen for den faktiske tidsrelaterede omkostning.</span><span class="sxs-lookup"><span data-stu-id="67702-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="67702-129">Hvis der kun er én prisliste, der dækker denne dato for den faktiske tidsrelaterede omkostning, skal du gå til den næste kontrol i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="67702-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="67702-130">Når du har foretaget de nødvendige rettelser, skal du genoprette en tidsrelateret post, godkende den og kontrollere, at den faktiske tidsrelaterede omkostning viser en gyldig pris.</span><span class="sxs-lookup"><span data-stu-id="67702-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="67702-131">Kontrol 3: Findes der en pris på prislisten for prissætningsdimensionerne i den faktiske tidsrelaterede omkostning?</span><span class="sxs-lookup"><span data-stu-id="67702-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="67702-132">Hvis du har fuldført kontrol 1 og kontrol 2, bør du kun have én prisliste, der gælder for datoen for den faktiske tidsrelaterede omkostning, nu.</span><span class="sxs-lookup"><span data-stu-id="67702-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="67702-133">Åbn denne projektprisliste, og gå til fanen Rollepriser. Kontroller, at der er en række i gitteret til prissætningsdimensionerne i den faktiske tidsrelaterede omkostning.</span><span class="sxs-lookup"><span data-stu-id="67702-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="67702-134">Hvis der ikke er en række i rolleprisgitteret for prissætningsdimensionerne i den faktiske tidsrelaterede omkostning, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="67702-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="67702-135">Opret en række i gitteret Rollepriser til prissætningsdimensionerne i din faktiske tidsrelaterede omkostning.</span><span class="sxs-lookup"><span data-stu-id="67702-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="67702-136">Når du har gjort det, skal du genoprette en tidsrelateret post, godkende den og kontrollere, at den faktiske tidsrelaterede omkostning viser en gyldig pris.</span><span class="sxs-lookup"><span data-stu-id="67702-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="67702-137">Hvis du stadig ikke kan se en gyldig pris i din faktiske tidsrelaterede omkostning, skal du anmode om support.</span><span class="sxs-lookup"><span data-stu-id="67702-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]