---
title: Opret projekttilbud ud fra salgsmuligheder
description: Dette emne indeholder oplysninger om oprettelse af et projekttilbud fra en salgsmulighed.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074084"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="c7fcd-103">Opret projekttilbud ud fra salgsmuligheder</span><span class="sxs-lookup"><span data-stu-id="c7fcd-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="c7fcd-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c7fcd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7fcd-105">Der kan oprettes tilbud fra projektsalgsmuligheder på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="c7fcd-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="c7fcd-106">Fra fanen **Tilbud** på siden **Projektsalgsmulighed**</span><span class="sxs-lookup"><span data-stu-id="c7fcd-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="c7fcd-107">Fra flowet for salgsprocessen for salgsmulighed</span><span class="sxs-lookup"><span data-stu-id="c7fcd-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="c7fcd-108">Ved at opdatere salgsmulighedsreferencen i et eksisterende tilbud</span><span class="sxs-lookup"><span data-stu-id="c7fcd-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="c7fcd-109">Fra fanen Tilbud på siden Projektsalgsmulighed</span><span class="sxs-lookup"><span data-stu-id="c7fcd-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="c7fcd-110">Hvis du vil oprette et projekttilbud ud fra en salgsmulighed, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="c7fcd-111">Åbn siden **Projektsalgsmulighed** , og vælg derefter fanen **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="c7fcd-112">I undergitteret **Tilbud** skal du vælge **+** for at oprette et nyt projekttilbud, der er baseret på salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="c7fcd-113">Alle salgsmulighedslinjer og relaterede projektprislister kopieres til det nye tilbud fra salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="c7fcd-114">Fra flowet for salgsprocessen for salgsmulighed</span><span class="sxs-lookup"><span data-stu-id="c7fcd-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="c7fcd-115">Hvis du vil oprette et tilbud ud fra salgsprocesflowet for salgsmuligheden, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="c7fcd-116">Åbn salgsmuligheden fra salgsprocesflowet for salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="c7fcd-117">Vælg fasen **Kvalificer**.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="c7fcd-118">Vælg **Næste** , og vælg derefter **+ Opret** for at oprette et nyt tilbud.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="c7fcd-119">De fleste oplysninger under fanen **Oversigt** for dette nye tilbud vil være angivet som standard fra salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="c7fcd-120">Angiv de påkrævede oplysninger, der mangler, eller opdater standardværdier efter behov under fanen **Oversigt** ,</span><span class="sxs-lookup"><span data-stu-id="c7fcd-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="c7fcd-121">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-121">Select **Save**.</span></span> <span data-ttu-id="c7fcd-122">Det nye tilbud oprettes og knyttes til salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="c7fcd-123">Du kan nu få vist tilbudsoplysningerne under fanen **Tilbud** på siden **Salgsmulighed**.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="c7fcd-124">Salgsprocessen for salgsmuligheden flyttes til næste fase, **Foreslå**.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="c7fcd-125">Ved at opdatere salgsmulighedsreferencen i et eksisterende tilbud</span><span class="sxs-lookup"><span data-stu-id="c7fcd-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="c7fcd-126">Et eksisterende tilbud kan knyttes til en salgsmulighed.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="c7fcd-127">Benyt følgende fremgangsmåde for at opdatere oplysningerne om salgsmuligheder i et eksisterende tilbud.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="c7fcd-128">Åbn siden **Tilbud** , og vælg derefter fanen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="c7fcd-129">I feltet **Salgsmulighed** skal du vælge den salgsmulighed, som du vil knytte til tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="c7fcd-130">Du kan se tilbuddet i gitteret **Tilbud** for salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="c7fcd-131">Ved hjælp af salgsprocessen for salgsmuligheden kan salgsmuligheden flyttes til næste fase, **Foreslå**.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="c7fcd-132">Når du flytter en salgsmulighed til denne fase, kan du vælge dette tilbud på en liste over tilbud, der er knyttet til salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="c7fcd-133">Hvis du vælger dette tilbud, betyder det, at du fortsætter med det.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="c7fcd-134">Alle de andre tilbud, der er knyttet til salgsmuligheden, er stadig tilgængelige og aktive, indtil et af dem er vundet.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="c7fcd-135">Du kan flytte salgsprocessen tilbage til forrige fase **Kvalificer** og vælge et andet tilbud, som du ønsker at fortsætte med.</span><span class="sxs-lookup"><span data-stu-id="c7fcd-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
