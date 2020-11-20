---
title: Opret brugerdefinerede felter og objekter som dimensioner for prisfastsættelse
description: Dette emne indeholder oplysninger om, hvordan du kan oprette brugerdefinerede grupperede indstillinger eller objekter.
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130886"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="d0e81-103">Opret brugerdefinerede felter og objekter som dimensioner for prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="d0e81-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="d0e81-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="d0e81-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0e81-105">Benyt følgende fremgangsmåde, når du vil oprette en brugerdefineret grupperet indstilling eller et objekt.</span><span class="sxs-lookup"><span data-stu-id="d0e81-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0e81-106">Det anbefales, at du foretager alle ændringer af brugerdefinerede prisdimensioner i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="d0e81-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="d0e81-107">Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til en anden forekomst.</span><span class="sxs-lookup"><span data-stu-id="d0e81-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d0e81-108">Når du har foretaget alle de nødvendige ændringer, skal du eksportere løsningen som en **Administreret løsning** og importere den i andre forekomster for at genbruge din prissætning.</span><span class="sxs-lookup"><span data-stu-id="d0e81-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="d0e81-109">Oprette en brugerdefineret løsning til prisdimensioner</span><span class="sxs-lookup"><span data-stu-id="d0e81-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="d0e81-110">Gå til **Indstillinger** > **Løsninger**, og vælg derefter **Ny** for at oprette en ny løsning.</span><span class="sxs-lookup"><span data-stu-id="d0e81-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="d0e81-111">Navngiv løsningen **\<your organization name> prisfastsættelsesdimensioner**, angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="d0e81-112">Oprette brugerdefinerede felter og grupperet indstilling i prisdimensionsløsningen</span><span class="sxs-lookup"><span data-stu-id="d0e81-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="d0e81-113">En prisdimension kan være en grupperet indstilling eller et objekt.</span><span class="sxs-lookup"><span data-stu-id="d0e81-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="d0e81-114">Begge skal være oprettet i din prissætningsløsning.</span><span class="sxs-lookup"><span data-stu-id="d0e81-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="d0e81-115">I fremgangsmåden i denne procedure forklares det, hvordan du kan oprette objektbaserede dimensioner og dimensioner baseret på en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="d0e81-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="d0e81-116">Objektbaserede dimensioner</span><span class="sxs-lookup"><span data-stu-id="d0e81-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="d0e81-117">Gå til **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="d0e81-118">Vælg **Objekter** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="d0e81-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="d0e81-119">Vælg **Nyt** for at oprette et nyt objekt med navnet **Standardtitel**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="d0e81-120">Angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="d0e81-121">Dimensioner baseret på grupperet indstilling</span><span class="sxs-lookup"><span data-stu-id="d0e81-121">Option set-based dimensions</span></span> 
<span data-ttu-id="d0e81-122">Du kan oprette to dimensioner, der er baseret på grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="d0e81-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="d0e81-123">Brug **Arbejdssted for ressource** til at spore prisen på arbejdet på arbejdsstedet **Privat** og **Privat** og brug **Arbejdstimer for ressource** med værdierne **Almindelig** og **Overtid** for at anvende en markering, når arbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="d0e81-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="d0e81-124">Gå til **Indstillinger** > **Løsninger** og dobbeltklik på **\<your organization name> prisfastsættelsesdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d0e81-125">Vælg **Grupperede indstillinger** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="d0e81-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="d0e81-126">Vælg **Ny** for at oprette en ny grupperet indstilling, angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="d0e81-127">Oprette data til objektbaserede dimensioner</span><span class="sxs-lookup"><span data-stu-id="d0e81-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="d0e81-128">Du kan oprette data til objektbaserede dimensioner manuelt eller ved hjælp af Microsoft Excel-import eller -serviceopkald.</span><span class="sxs-lookup"><span data-stu-id="d0e81-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="d0e81-129">Følg trinnene i denne fremgangsmåde for at oprette to standard titler, **Systemtekniker** og **Seniorsystemtekniker** fra den objektbaserede dimension, **Standardtitel**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="d0e81-130">Hvis de data, du vil oprette, er små, som i følgende eksempel, kan du bruge en standardformular.</span><span class="sxs-lookup"><span data-stu-id="d0e81-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="d0e81-131">Vælg **Avanceret søgning**, Vælg objektets **Standardtitel**, og vælg derefter **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="d0e81-132">Alle rækkerne i objektet **Standardtitel** vises.</span><span class="sxs-lookup"><span data-stu-id="d0e81-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="d0e81-133">Vælg **Ny**, angiv "Systemtekniker" i feltet **Navn**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="d0e81-134">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="d0e81-134">Close the form.</span></span> 
4. <span data-ttu-id="d0e81-135">Gentag trin 1-3 for at oprette endnu en standardtitel til "Seniorsystemtekniker".</span><span class="sxs-lookup"><span data-stu-id="d0e81-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d0e81-136">Tilføje alle nødvendige objekter og relaterede komponenter i løsningen til prisfastsættelsesdimensionen</span><span class="sxs-lookup"><span data-stu-id="d0e81-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="d0e81-137">Du skal føje følgende objekter til din prisfastsættelsesløsning.</span><span class="sxs-lookup"><span data-stu-id="d0e81-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="d0e81-138">Følg trinnene i denne fremgangsmåde for at foretage nogle vigtige skemaændringer i prissætningsløsningen, så objekterne bliver opmærksomme på de nye prisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="d0e81-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="d0e81-139">Vælg **Indstillinger** > **Løsninger** og dobbeltklik på **\<your organization name> prisfastsættelsesdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d0e81-140">Vælg **Tilføj eksisterende** > **Objekter** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="d0e81-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="d0e81-141">Vælg følgende objekter i dialogboksen **Løsningskomponenter**:</span><span class="sxs-lookup"><span data-stu-id="d0e81-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="d0e81-142">Faktisk</span><span class="sxs-lookup"><span data-stu-id="d0e81-142">Actual</span></span>
  - <span data-ttu-id="d0e81-143">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="d0e81-143">Bookable Resource</span></span>
  - <span data-ttu-id="d0e81-144">Estimatlinje</span><span class="sxs-lookup"><span data-stu-id="d0e81-144">Estimate Line</span></span>
  - <span data-ttu-id="d0e81-145">Fakturalinjedetalje</span><span class="sxs-lookup"><span data-stu-id="d0e81-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="d0e81-146">Kladdelinje</span><span class="sxs-lookup"><span data-stu-id="d0e81-146">Journal Line</span></span>
  - <span data-ttu-id="d0e81-147">Projektkontraktlinjedetalje</span><span class="sxs-lookup"><span data-stu-id="d0e81-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="d0e81-148">Medlem af projektteam</span><span class="sxs-lookup"><span data-stu-id="d0e81-148">Project Team Member</span></span>
  - <span data-ttu-id="d0e81-149">Tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="d0e81-149">Quote Line Detail</span></span>
  - <span data-ttu-id="d0e81-150">Rolleprisavance</span><span class="sxs-lookup"><span data-stu-id="d0e81-150">Role Price Markup</span></span>
  - <span data-ttu-id="d0e81-151">Rollepris</span><span class="sxs-lookup"><span data-stu-id="d0e81-151">Role Price</span></span> 
  - <span data-ttu-id="d0e81-152">Tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="d0e81-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="d0e81-153">Sørg for at inkludere alle formularer og visninger for hvert af de valgte objekter.</span><span class="sxs-lookup"><span data-stu-id="d0e81-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="d0e81-154">Vælg **Nej**, når du bliver bedt om at inkludere afhængige objekter for de objekter, der er valgt ovenfor.</span><span class="sxs-lookup"><span data-stu-id="d0e81-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

