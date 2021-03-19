---
title: Tilsidesæt projektsalgsprislister
description: Dette emne indeholder oplysninger om oprettelse af brugerdefinerede salgsprislister.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275531"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="9fa29-103">Tilsidesæt projektsalgsprislister</span><span class="sxs-lookup"><span data-stu-id="9fa29-103">Override project sales price lists</span></span>

<span data-ttu-id="9fa29-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="9fa29-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="9fa29-105">Kundespecifikke projektprislister</span><span class="sxs-lookup"><span data-stu-id="9fa29-105">Customer-specific project price lists</span></span>

<span data-ttu-id="9fa29-106">Kundespecifikke prisaftaler kan konfigureres som projektprislister på en kontopost i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9fa29-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="9fa29-107">Hvis du vil oprette en kundespecifik projektprisliste, skal du i området **Salg** går til kontoposten.</span><span class="sxs-lookup"><span data-stu-id="9fa29-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="9fa29-108">Åbn listesiden med **Konti**.</span><span class="sxs-lookup"><span data-stu-id="9fa29-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="9fa29-109">Find og dobbeltklik på en kundepost for at åbne detaljesiden for **Konto**.</span><span class="sxs-lookup"><span data-stu-id="9fa29-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="9fa29-110">På fanen **Projektprislister** skal du vælge **+ Ny projektprisliste**.</span><span class="sxs-lookup"><span data-stu-id="9fa29-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="9fa29-111">På siden **Ny projektprisliste** skal du vælge en prisliste i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="9fa29-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="9fa29-112">Kun prislister, hvor konteksten er angivet til **Salg**, og hvis valuta matcher kontovalutaen, medtages.</span><span class="sxs-lookup"><span data-stu-id="9fa29-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="9fa29-113">Navngiv tilknytningen og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9fa29-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="9fa29-114">Der oprettes en kundespecifik projektprisliste.</span><span class="sxs-lookup"><span data-stu-id="9fa29-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="9fa29-115">Denne prisliste bruges som standard for projektpriser på projekttilbud eller kontrakter, der er oprettet for denne kunde, når den oprettede dato for tilbuddet eller projektkontrakten falder inden for prislistens ikraftrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="9fa29-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="9fa29-116">Brugerdefineret prisfastsættelse på projekttilbud</span><span class="sxs-lookup"><span data-stu-id="9fa29-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="9fa29-117">På projekttilbud kan du have projektprisfastsættelser, som starter med en standardprisliste, der som standard hentes fra kunden eller fra projektparametrene.</span><span class="sxs-lookup"><span data-stu-id="9fa29-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="9fa29-118">Når du har brug for brugerdefinere prisfastsættelse for projektrelateret arbejde på et bestemt tilbud, kan du opnå dette ved hjælp af den tilknyttede enhed med projektprislister.</span><span class="sxs-lookup"><span data-stu-id="9fa29-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="9fa29-119">Udfør følgende trin for at konfigurere tilbudsspecifik projektprisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="9fa29-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="9fa29-120">Åbn projekttilbud, og vælg fanen **Projektprislister**.</span><span class="sxs-lookup"><span data-stu-id="9fa29-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="9fa29-121">I undergitteret skal du vælge **Opret brugerdefineret prisfastsættelse**.</span><span class="sxs-lookup"><span data-stu-id="9fa29-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="9fa29-122">Alle de projektprislister, der er knyttet til tilbuddet, kopieres til nye prislister.</span><span class="sxs-lookup"><span data-stu-id="9fa29-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="9fa29-123">Navnene på de nye prislister afspejler navnet på tilbuddet med et datotidsstempel for det tidspunkt, hvor disse prislister blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="9fa29-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="9fa29-124">Du kan bruge hver af disse prislister og foretage opdateringer til arbejdskraftpriser (rollepris) og udgiftspriser (kategoripris).</span><span class="sxs-lookup"><span data-stu-id="9fa29-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="9fa29-125">Disse priser gælder kun for dette projekttilbud.</span><span class="sxs-lookup"><span data-stu-id="9fa29-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="9fa29-126">Prislister på en projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="9fa29-126">Price lists on a project contract</span></span>

<span data-ttu-id="9fa29-127">På en projektkontrakt er projektprisfastsættelse som standard altid en brugerdefineret prisliste med navnet på kontrakten og tidspunkt for oprettelse, der er føjet til navnet.</span><span class="sxs-lookup"><span data-stu-id="9fa29-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="9fa29-128">Dette gælder, uanset om kontrakten blev oprettet, da tilbuddet blev vundet, eller om kontrakten blev oprettet fra bunden.</span><span class="sxs-lookup"><span data-stu-id="9fa29-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="9fa29-129">Hvis det er nødvendigt, kan du fjerne denne tilknytning til den brugerdefinerede prisliste og knytte en standardprisliste til projektkontrakten i stedet.</span><span class="sxs-lookup"><span data-stu-id="9fa29-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="9fa29-130">Når du knytter en standardprisliste til projektprislisterne på et tilbud eller en kontrakt, vil eventuelle ændringer af priserne i prislisten påvirke alle tilbud og kontrakter, der bruger prislisten.</span><span class="sxs-lookup"><span data-stu-id="9fa29-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]