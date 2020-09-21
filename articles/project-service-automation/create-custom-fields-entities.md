---
title: Oprette brugerdefinerede felter og objekter
description: I dette emne beskrives det, hvordan du kan oprette grupperede indstillinger og objekter i din egen løsning i Power Apps-platformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750610"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="a5201-103">Oprette brugerdefinerede felter og objekter</span><span class="sxs-lookup"><span data-stu-id="a5201-103">Create custom fields and entities</span></span> 

<span data-ttu-id="a5201-104">Benyt følgende fremgangsmåde, når du vil oprette en brugerdefineret grupperet indstilling eller et objekt på Power Apps-platformen.</span><span class="sxs-lookup"><span data-stu-id="a5201-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="a5201-105">Fremgangsmåderne i dette emne skal udføres ved hjælp af webgrænsefladen i Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a5201-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5201-106">Det anbefales, at du foretager alle ændringer af brugerdefinerede prisdimensioner i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="a5201-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="a5201-107">Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til en anden forekomst.</span><span class="sxs-lookup"><span data-stu-id="a5201-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="a5201-108">Når du har foretaget alle de nødvendige ændringer, skal du eksportere løsningen som en **Administreret løsning** og importere den i andre forekomster for at genbruge din prissætning.</span><span class="sxs-lookup"><span data-stu-id="a5201-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="a5201-109">Oprette en brugerdefineret løsning til prisdimensioner</span><span class="sxs-lookup"><span data-stu-id="a5201-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="a5201-110">Klik i PSA på **Indstillinger** > **Løsninger**, og klik derefter på **Ny** for at oprette en ny løsning.</span><span class="sxs-lookup"><span data-stu-id="a5201-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="a5201-111">Navngiv løsningen **\<navnet på din organisation > prisdimensioner**, angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a5201-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Oprettelse af en brugerdefineret løsning til prisdimensioner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="a5201-113">Oprette brugerdefinerede felter og grupperet indstilling i prisdimensionsløsningen</span><span class="sxs-lookup"><span data-stu-id="a5201-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="a5201-114">En prisdimension kan være en grupperet indstilling eller et objekt.</span><span class="sxs-lookup"><span data-stu-id="a5201-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="a5201-115">Begge skal være oprettet i din prissætningsløsning.</span><span class="sxs-lookup"><span data-stu-id="a5201-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="a5201-116">I fremgangsmåden i denne procedure forklares det, hvordan du kan oprette objektbaserede dimensioner og dimensioner baseret på en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="a5201-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="a5201-117">Objektbaserede dimensioner</span><span class="sxs-lookup"><span data-stu-id="a5201-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="a5201-118">I PSA skal du klikke på **Indstillinger** > **Løsninger** og derefter dobbeltklikke på **\<organisationens navn> prisdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="a5201-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="a5201-119">Vælg **Objekter** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="a5201-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="a5201-120">Klik på **Nyt** for at oprette et nyt objekt med navnet **Standardtitel**.</span><span class="sxs-lookup"><span data-stu-id="a5201-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="a5201-121">Angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a5201-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definition af standardtitelobjekt](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="a5201-123">Dimensioner baseret på grupperet indstilling</span><span class="sxs-lookup"><span data-stu-id="a5201-123">Option set-based dimensions</span></span> 
<span data-ttu-id="a5201-124">Du kan oprette to dimensioner, der er baseret på grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="a5201-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="a5201-125">Brug **Arbejdssted for ressource** til at spore prisen på arbejdet på arbejdsstedet **Privat** og **Privat** og brug **Arbejdstimer for ressource** med værdierne **Almindelig** og **Overtid** for at anvende en markering, når arbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="a5201-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="a5201-126">I PSA skal du klikke på **Indstillinger** > **Løsninger** og derefter dobbeltklikke på **\<din organisations navn> prisdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="a5201-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="a5201-127">Vælg **Grupperede indstillinger** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="a5201-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="a5201-128">Klik på **Ny** for at oprette en ny grupperet indstilling, angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a5201-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="a5201-129">Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdssted for ressource</span><span class="sxs-lookup"><span data-stu-id="a5201-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="a5201-130">Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdstimer for ressource</span><span class="sxs-lookup"><span data-stu-id="a5201-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="a5201-131">Oprette data til objektbaserede dimensioner</span><span class="sxs-lookup"><span data-stu-id="a5201-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="a5201-132">Du kan oprette data til objektbaserede dimensioner manuelt eller ved hjælp af Microsoft Excel-import eller -serviceopkald.</span><span class="sxs-lookup"><span data-stu-id="a5201-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="a5201-133">Følg trinnene i denne fremgangsmåde for at oprette to standard titler, **Systemtekniker** og **Seniorsystemtekniker** fra den objektbaserede dimension, **Standardtitel**.</span><span class="sxs-lookup"><span data-stu-id="a5201-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="a5201-134">Hvis de data, du vil oprette, er små, som i følgende eksempel, kan du bruge en standardformular.</span><span class="sxs-lookup"><span data-stu-id="a5201-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="a5201-135">Klik på **Avanceret søgning** i PSA.</span><span class="sxs-lookup"><span data-stu-id="a5201-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="a5201-136">Vælg objektet **Standardtitel**, og klik derefter på **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="a5201-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="a5201-137">Alle rækkerne i objektet **Standardtitel** vises.</span><span class="sxs-lookup"><span data-stu-id="a5201-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="a5201-138">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a5201-138">Click **New**.</span></span> <span data-ttu-id="a5201-139">Angiv "Systemtekniker" i feltet **Navn**, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a5201-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="a5201-140">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="a5201-140">Close the form.</span></span> 
4. <span data-ttu-id="a5201-141">Gentag trin 1-3 for at oprette endnu en standardtitel til "Seniorsystemtekniker".</span><span class="sxs-lookup"><span data-stu-id="a5201-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="a5201-142">Eksempeldata til objektet Standardtitel</span><span class="sxs-lookup"><span data-stu-id="a5201-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="a5201-143">Tilføje alle nødvendige PSA-objekter og relaterede komponenter i en prisdimensionsløsning</span><span class="sxs-lookup"><span data-stu-id="a5201-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="a5201-144">Du skal føje følgende Project Service-objekter til din prissætningsløsning.</span><span class="sxs-lookup"><span data-stu-id="a5201-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="a5201-145">Følg trinnene i denne fremgangsmåde for at foretage nogle vigtige skemaændringer i prissætningsløsningen, så objekterne bliver opmærksomme på de nye prisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="a5201-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="a5201-146">I PSA skal du klikke på **Indstillinger** > **Løsninger** og derefter dobbeltklikke på **\<organisationens navn> prisdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="a5201-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="a5201-147">Vælg **Tilføj eksisterende** > **Objekter** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="a5201-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="a5201-148">Vælg følgende objekter i dialogboksen **Løsningskomponenter**:</span><span class="sxs-lookup"><span data-stu-id="a5201-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="a5201-149">Faktisk</span><span class="sxs-lookup"><span data-stu-id="a5201-149">Actual</span></span>
- <span data-ttu-id="a5201-150">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="a5201-150">Bookable Resource</span></span>
- <span data-ttu-id="a5201-151">Estimatlinje</span><span class="sxs-lookup"><span data-stu-id="a5201-151">Estimate Line</span></span>
- <span data-ttu-id="a5201-152">Fakturalinjedetalje</span><span class="sxs-lookup"><span data-stu-id="a5201-152">Invoice Line Detail</span></span>
- <span data-ttu-id="a5201-153">Kladdelinje</span><span class="sxs-lookup"><span data-stu-id="a5201-153">Journal Line</span></span>
- <span data-ttu-id="a5201-154">Projektkontraktlinjedetalje</span><span class="sxs-lookup"><span data-stu-id="a5201-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="a5201-155">Medlem af projektteam</span><span class="sxs-lookup"><span data-stu-id="a5201-155">Project Team Member</span></span>
- <span data-ttu-id="a5201-156">Tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="a5201-156">Quote Line Detail</span></span>
- <span data-ttu-id="a5201-157">Rolleprisavance</span><span class="sxs-lookup"><span data-stu-id="a5201-157">Role Price Markup</span></span>
- <span data-ttu-id="a5201-158">Rollepris</span><span class="sxs-lookup"><span data-stu-id="a5201-158">Role Price</span></span> 
- <span data-ttu-id="a5201-159">Tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="a5201-159">Time Entry</span></span> 

> ![Tilføje eksisterende objekter i prisdimensionsløsningen](media/Existing-entities-to-PD-solution.png)

> ![Vælge løsningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="a5201-162">Sørg for at inkludere alle formularer og visninger for hvert af de valgte objekter.</span><span class="sxs-lookup"><span data-stu-id="a5201-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="a5201-163">Klik på **Nej**, når du bliver bedt om at inkludere afhængige objekter for de objekter, der er valgt ovenfor.</span><span class="sxs-lookup"><span data-stu-id="a5201-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Inkluder ikke alle relaterede komponenter](media/Do-not-include-required.png)


