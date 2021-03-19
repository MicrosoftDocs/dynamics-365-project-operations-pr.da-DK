---
title: Opret brugerdefinerede felter og objekter som dimensioner for prisfastsættelse
description: Dette emne indeholder oplysninger om, hvordan du kan oprette brugerdefinerede grupperede indstillinger eller objekter.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275621"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="1cfdc-103">Opret brugerdefinerede felter og objekter som dimensioner for prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="1cfdc-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="1cfdc-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="1cfdc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1cfdc-105">Benyt følgende fremgangsmåde, når du vil oprette en brugerdefineret grupperet indstilling eller et objekt som en prisfastsættelsesdimension.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="1cfdc-106">Se [Oversigt over prisfastsættelsesdimensioner](pricing-dimensions-overview.md) for at få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="1cfdc-107">Det anbefales, at du foretager alle ændringer af brugerdefinerede prisdimensioner i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="1cfdc-108">Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="1cfdc-109">Den vil også hjælpe til med at genbruge dit arbejde og gøre det nemmere at koble disse ændringer sammen med en anden forekomst. Når du har foretaget alle de nødvendige ændringer, skal du eksportere løsningen som **Administreret løsning** og importere den på andre forekomster for at genbruge din prisfastsættelsesopsætning.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="1cfdc-110">Oprette brugerdefinerede felter og grupperet indstilling i prisdimensionsløsningen</span><span class="sxs-lookup"><span data-stu-id="1cfdc-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="1cfdc-111">En prisdimension kan være en grupperet indstilling eller et objekt.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="1cfdc-112">Begge skal være oprettet i din prissætningsløsning.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="1cfdc-113">I fremgangsmåden i denne procedure forklares det, hvordan du kan oprette objektbaserede dimensioner og dimensioner baseret på en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="1cfdc-114">Objektbaserede dimensioner</span><span class="sxs-lookup"><span data-stu-id="1cfdc-114">Entity-based dimensions</span></span>
<span data-ttu-id="1cfdc-115">Benyt følgende fremgangsmåde for at oprette objektbaserede dimensioner:</span><span class="sxs-lookup"><span data-stu-id="1cfdc-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="1cfdc-116">Gå til **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="1cfdc-117">Vælg **Objekter** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="1cfdc-118">Vælg **Nyt** for at oprette et nyt objekt med navnet **Standardtitel**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="1cfdc-119">Angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definition af standardtitelobjekt](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="1cfdc-121">Dimensioner baseret på grupperet indstilling</span><span class="sxs-lookup"><span data-stu-id="1cfdc-121">Option set-based dimensions</span></span> 
<span data-ttu-id="1cfdc-122">Du kan oprette to dimensioner, der er baseret på grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="1cfdc-123">Brug **Ressourcens arbejdsplacering** til at følge prisen på arbejde på lokationen **Hjemme** og **På stedet**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="1cfdc-124">Brug **Ressourcens arbejdstimer** med værdierne **Almindelig** og **Overarbejde** for at foretage en markering, når arbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="1cfdc-125">Følgende grafik indeholder en oversigt over dimensionen **Ressourcens arbejdslokation**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdssted for ressource](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="1cfdc-127">Følgende grafik indeholder en oversigt over dimensionen **Ressourcens arbejdstid**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdstimer for ressource](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="1cfdc-129">Gå til **Indstillinger** > **Løsninger** og dobbeltklik på **\<your organization name> prisfastsættelsesdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="1cfdc-130">Vælg **Grupperede indstillinger** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="1cfdc-131">Vælg **Ny** for at oprette en ny grupperet indstilling, angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="1cfdc-132">Oprette data til objektbaserede dimensioner</span><span class="sxs-lookup"><span data-stu-id="1cfdc-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="1cfdc-133">Du kan oprette data til objektbaserede dimensioner manuelt eller ved hjælp af Microsoft Excel-import eller -serviceopkald.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="1cfdc-134">Følg trinnene i denne fremgangsmåde for at oprette to standard titler, **Systemtekniker** og **Seniorsystemtekniker** fra den objektbaserede dimension, **Standardtitel**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="1cfdc-135">Hvis de data, du vil oprette, er små, som i følgende eksempel, kan du bruge en standardformular.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="1cfdc-136">Vælg **Avanceret søgning**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="1cfdc-137">Vælg objektet **Standardtitel**, og vælg derefter **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="1cfdc-138">Alle rækkerne i objektet **Standardtitel** vises.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="1cfdc-139">Vælg **Ny**, angiv "Systemtekniker" i feltet **Navn**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="1cfdc-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-140">Close the page.</span></span> 
5. <span data-ttu-id="1cfdc-141">Gentag trin 1-3 for at oprette endnu en standardtitel til "Seniorsystemtekniker".</span><span class="sxs-lookup"><span data-stu-id="1cfdc-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Eksempeldata til objektet Standardtitel](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]