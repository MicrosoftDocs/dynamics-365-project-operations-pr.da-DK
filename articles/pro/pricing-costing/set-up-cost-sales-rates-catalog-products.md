---
title: Konfigurer satser for omkostninger og salg af katalogprodukter - lille
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere satser for omkostninger og salg for varer i et produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004309"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="69152-103">Konfigurer satser for omkostninger og salg af katalogprodukter - lille</span><span class="sxs-lookup"><span data-stu-id="69152-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="69152-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="69152-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="69152-105">Opsætningen af priser for produktkatalogvarer i Dynamics 365 Project Operations er den samme som i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="69152-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="69152-106">I Project Operations kan produkter ikke estimeres eller bruges på projekter, så produktkatalogpriser behøver ikke at blive angivet på projektprislister for tilbud og kontrakter.</span><span class="sxs-lookup"><span data-stu-id="69152-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="69152-107">Brug feltet **Produktpris** i et tilbud, en kontrakt eller på en konto til at konfigurere produktkatalogpriser.</span><span class="sxs-lookup"><span data-stu-id="69152-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="69152-108">Konfigurer ikke produktkatalogpriser på projektprislisterne.</span><span class="sxs-lookup"><span data-stu-id="69152-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="69152-109">Projektprislister er eksklusive for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="69152-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="69152-110">Den applikationsspecifikke forretningslogik kopierer prislisterne fra et tilbud til en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="69152-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="69152-111">Resultatet er en kontraktspecifik projektprisliste.</span><span class="sxs-lookup"><span data-stu-id="69152-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="69152-112">Kopieringshandlingen kan forsinke processen for vundne tilbud, hvis projektets prisliste i tilbuddet bliver for stor.</span><span class="sxs-lookup"><span data-stu-id="69152-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="69152-113">Produktprislisterne kopieres ikke for at oprette brugerdefinerede prislister på kontrakter.</span><span class="sxs-lookup"><span data-stu-id="69152-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="69152-114">Da der ikke er nogen kopiering involveret, påvirkes tilbudsprocessens ydeevne ikke.</span><span class="sxs-lookup"><span data-stu-id="69152-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]