---
title: Oprette brugerdefinerede felter og objekter
description: I dette emne beskrives det, hvordan du kan oprette grupperede indstillinger og objekter i din egen løsning i Power Apps-platformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074241"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="dbb70-103">Oprette brugerdefinerede felter og objekter</span><span class="sxs-lookup"><span data-stu-id="dbb70-103">Create custom fields and entities</span></span> 

<span data-ttu-id="dbb70-104">Benyt følgende fremgangsmåde, når du vil oprette en brugerdefineret grupperet indstilling eller et objekt på Power Apps-platformen.</span><span class="sxs-lookup"><span data-stu-id="dbb70-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="dbb70-105">Fremgangsmåderne i dette emne skal udføres ved hjælp af webgrænsefladen i Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="dbb70-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbb70-106">Det anbefales, at du foretager alle ændringer af brugerdefinerede prisdimensioner i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="dbb70-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="dbb70-107">Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til en anden forekomst.</span><span class="sxs-lookup"><span data-stu-id="dbb70-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="dbb70-108">Når du har foretaget alle de nødvendige ændringer, skal du eksportere løsningen som en **Administreret løsning** og importere den i andre forekomster for at genbruge din prissætning.</span><span class="sxs-lookup"><span data-stu-id="dbb70-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="dbb70-109">Oprette brugerdefinerede felter og grupperet indstilling i prisdimensionsløsningen</span><span class="sxs-lookup"><span data-stu-id="dbb70-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="dbb70-110">En prisdimension kan være en grupperet indstilling eller et objekt.</span><span class="sxs-lookup"><span data-stu-id="dbb70-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="dbb70-111">Begge skal være oprettet i din prissætningsløsning.</span><span class="sxs-lookup"><span data-stu-id="dbb70-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="dbb70-112">I fremgangsmåden i denne procedure forklares det, hvordan du kan oprette objektbaserede dimensioner og dimensioner baseret på en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="dbb70-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="dbb70-113">Objektbaserede dimensioner</span><span class="sxs-lookup"><span data-stu-id="dbb70-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="dbb70-114">Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner** i PSA.</span><span class="sxs-lookup"><span data-stu-id="dbb70-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="dbb70-115">Vælg **Objekter** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="dbb70-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="dbb70-116">Klik på **Nyt** for at oprette et nyt objekt med navnet **Standardtitel**.</span><span class="sxs-lookup"><span data-stu-id="dbb70-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="dbb70-117">Angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dbb70-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definition af standardtitelobjekt](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="dbb70-119">Dimensioner baseret på grupperet indstilling</span><span class="sxs-lookup"><span data-stu-id="dbb70-119">Option set-based dimensions</span></span> 
<span data-ttu-id="dbb70-120">Du kan oprette to dimensioner, der er baseret på grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="dbb70-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="dbb70-121">Brug **Arbejdssted for ressource** til at spore prisen på arbejdet på arbejdsstedet **Privat** og **Privat** og brug **Arbejdstimer for ressource** med værdierne **Almindelig** og **Overtid** for at anvende en markering, når arbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="dbb70-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="dbb70-122">Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner** i PSA.</span><span class="sxs-lookup"><span data-stu-id="dbb70-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="dbb70-123">Vælg **Grupperede indstillinger** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="dbb70-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="dbb70-124">Klik på **Ny** for at oprette en ny grupperet indstilling, angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dbb70-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="dbb70-125">Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdssted for ressource</span><span class="sxs-lookup"><span data-stu-id="dbb70-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="dbb70-126">Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdstimer for ressource</span><span class="sxs-lookup"><span data-stu-id="dbb70-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="dbb70-127">Oprette data til objektbaserede dimensioner</span><span class="sxs-lookup"><span data-stu-id="dbb70-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="dbb70-128">Du kan oprette data til objektbaserede dimensioner manuelt eller ved hjælp af Microsoft Excel-import eller -serviceopkald.</span><span class="sxs-lookup"><span data-stu-id="dbb70-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="dbb70-129">Følg trinnene i denne fremgangsmåde for at oprette to standard titler, **Systemtekniker** og **Seniorsystemtekniker** fra den objektbaserede dimension, **Standardtitel**.</span><span class="sxs-lookup"><span data-stu-id="dbb70-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="dbb70-130">Hvis de data, du vil oprette, er små, som i følgende eksempel, kan du bruge en standardformular.</span><span class="sxs-lookup"><span data-stu-id="dbb70-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="dbb70-131">Klik på **Avanceret søgning** i PSA.</span><span class="sxs-lookup"><span data-stu-id="dbb70-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="dbb70-132">Vælg objektet **Standardtitel** , og klik derefter på **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="dbb70-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="dbb70-133">Alle rækkerne i objektet **Standardtitel** vises.</span><span class="sxs-lookup"><span data-stu-id="dbb70-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="dbb70-134">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dbb70-134">Click **New**.</span></span> <span data-ttu-id="dbb70-135">Angiv "Systemtekniker" i feltet **Navn** , og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dbb70-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="dbb70-136">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="dbb70-136">Close the form.</span></span> 
4. <span data-ttu-id="dbb70-137">Gentag trin 1-3 for at oprette endnu en standardtitel til "Seniorsystemtekniker".</span><span class="sxs-lookup"><span data-stu-id="dbb70-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="dbb70-138">Eksempeldata til objektet Standardtitel</span><span class="sxs-lookup"><span data-stu-id="dbb70-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

