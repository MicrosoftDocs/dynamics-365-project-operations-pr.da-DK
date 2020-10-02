---
title: Opsætning af salgsprisliste
description: Dette emne indeholder oplysninger om salgsprislister til prisfastsættelse af projekter.
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896454"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="fec00-103">Opsætning af salgsprisliste</span><span class="sxs-lookup"><span data-stu-id="fec00-103">Sales price list setup</span></span>

<span data-ttu-id="fec00-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="fec00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fec00-105">I forbindelse med projekttilbud og kontrakter har en projektprisliste et andet mønster for pristilsidesættelse end en produktprisliste.</span><span class="sxs-lookup"><span data-stu-id="fec00-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="fec00-106">På en produktkatalogbaseret tilbudslinje kan du tilsidesætte prisen på roller og kategorier direkte på tilbudslinjen, da alle tilbudslinjer peger på præcist ét katalogelement.</span><span class="sxs-lookup"><span data-stu-id="fec00-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="fec00-107">Men på en projektbaseret tilbudslinje kan du dog ikke tilsidesætte prisen for roller og kategorier direkte på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="fec00-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="fec00-108">Du kan bruge projektprislisten til at arbejde med de to forskellige tilsidesættelses mønstre.</span><span class="sxs-lookup"><span data-stu-id="fec00-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="fec00-109">Det anbefales, at du har en separat prisliste for projektressourcerne og dine katalogelementer på grund af de funktionsmæssige forskelle mellem de to, når du tilsidesætter prissætningen.</span><span class="sxs-lookup"><span data-stu-id="fec00-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="fec00-110">Hvert af følgende objekter kan have en eller flere tilknyttede salgsprislister for projektprissætning:</span><span class="sxs-lookup"><span data-stu-id="fec00-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="fec00-111">Kunde (konto)</span><span class="sxs-lookup"><span data-stu-id="fec00-111">Customer (account)</span></span> 
- <span data-ttu-id="fec00-112">Salgsmulighed</span><span class="sxs-lookup"><span data-stu-id="fec00-112">Opportunity</span></span> 
- <span data-ttu-id="fec00-113">Tilbud</span><span class="sxs-lookup"><span data-stu-id="fec00-113">Quote</span></span> 
- <span data-ttu-id="fec00-114">Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="fec00-114">Project Contract</span></span>

<span data-ttu-id="fec00-115">Tilknytningen af disse objekter til en prisliste angives af listerne over projektpriser.</span><span class="sxs-lookup"><span data-stu-id="fec00-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="fec00-116">Du kan knytte en eller flere prislister til salgsobjekterne Kunde, Salgsmulighed, Tilbud og Projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="fec00-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="fec00-117">Der angives ikke automatisk en standardprisliste for projekter på en kundepost.</span><span class="sxs-lookup"><span data-stu-id="fec00-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="fec00-118">Du kan dog manuelt knytte en liste over projektpriser til kundeposten.</span><span class="sxs-lookup"><span data-stu-id="fec00-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="fec00-119">Du bør dog kun tilknytte en liste med projektpriser manuelt, hvis du har en bestemt prisaftale med kunden.</span><span class="sxs-lookup"><span data-stu-id="fec00-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="fec00-120">Når en projektprisliste er knyttet til et salgsobjekt, valideres følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="fec00-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="fec00-121">Prislisten har konteksten **Salg**.</span><span class="sxs-lookup"><span data-stu-id="fec00-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="fec00-122">Valutaen for prislisten svarer til kundevalutaen.</span><span class="sxs-lookup"><span data-stu-id="fec00-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="fec00-123">I en projektkontrakt bruges følgende prioriteret rækkefølge til automatisk at angive tilknyttede projektprislister:</span><span class="sxs-lookup"><span data-stu-id="fec00-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="fec00-124">Tilbud</span><span class="sxs-lookup"><span data-stu-id="fec00-124">Quote</span></span>
2. <span data-ttu-id="fec00-125">Salgsmulighed</span><span class="sxs-lookup"><span data-stu-id="fec00-125">Opportunity</span></span>
3. <span data-ttu-id="fec00-126">Kunde</span><span class="sxs-lookup"><span data-stu-id="fec00-126">Customer</span></span> 
4. <span data-ttu-id="fec00-127">Globale indstillinger</span><span class="sxs-lookup"><span data-stu-id="fec00-127">Global settings</span></span> 

<span data-ttu-id="fec00-128">Når en projektprisliste angives som standard, validerer systemet, om valutaen stemmer overens med kundens valuta, og at de standardprislister, der er angivet, har en kontekst af **Salg**.</span><span class="sxs-lookup"><span data-stu-id="fec00-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="fec00-129">Du kan knytte flere projektprislister til objekterne Kunde, Salgsmulighed, Tilbud og Projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="fec00-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="fec00-130">Denne funktion understøtter datospecifikke standardpriser for en længerevarende projektkontrakt, hvor der kan kræves mere end én prisliste for at tage højde for prisopdateringer, der opstår på grund af inflation.</span><span class="sxs-lookup"><span data-stu-id="fec00-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="fec00-131">Men hvis de prislister, du knytter til kunde-, salgsmuligheds-, tilbuds- eller projektkontraktobjektet, har et overlappende datointerval, kan standardpriserne være forkerte.</span><span class="sxs-lookup"><span data-stu-id="fec00-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="fec00-132">Du skal derfor sikre dig, at de projektprislister, der har overlappende datointerval, ikke er knyttet til disse objekter.</span><span class="sxs-lookup"><span data-stu-id="fec00-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
