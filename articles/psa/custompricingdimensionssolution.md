---
title: Opret brugerdefinerede løsninger til prisfastsættelsesdimensioner
description: I dette emne beskrives det, hvordan du kan oprette en brugerdefineret løsning, når du opretter brugerdefinerede prisfastsættelsesdimensioner.
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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144632"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="3cf71-103">Opret brugerdefinerede løsninger til prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="3cf71-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="3cf71-104">Alle ændringer af brugerdefineret prisfastsættelsesdimensioner bør være i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="3cf71-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="3cf71-105">Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til en anden forekomst.</span><span class="sxs-lookup"><span data-stu-id="3cf71-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="3cf71-106">Når du har foretaget de nødvendige ændringer, skal du eksportere løsningen som en **Administreret løsning** og importere den i andre forekomster for at genbruge din prisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="3cf71-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="3cf71-107">Vælg **Indstillinger** > **Løsninger**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3cf71-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="3cf71-108">Navngiv løsningen **\<your organization name> prisfastsættelsesdimensioner**, angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3cf71-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Oprettelse af en brugerdefineret løsning til prisdimensioner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="3cf71-110">Tilføj alle nødvendige objekter og relaterede komponenter i løsningen til prisfastsættelsesdimensionen</span><span class="sxs-lookup"><span data-stu-id="3cf71-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="3cf71-111">Du skal føje følgende Project Service-objekter til din prissætningsløsning.</span><span class="sxs-lookup"><span data-stu-id="3cf71-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="3cf71-112">Fuldfør trinnene i denne fremgangsmåde for at foretage nogle vigtige skemaændringer i prisfastsættelsesløsningen, så enhederne bliver opmærksomme på de nye prisfastsættelsesdimensioner.</span><span class="sxs-lookup"><span data-stu-id="3cf71-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="3cf71-113">Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="3cf71-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3cf71-114">Vælg **Tilføj eksisterende** > **Objekter** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="3cf71-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="3cf71-115">Vælg følgende objekter i dialogboksen **Løsningskomponenter**:</span><span class="sxs-lookup"><span data-stu-id="3cf71-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="3cf71-116">Faktisk</span><span class="sxs-lookup"><span data-stu-id="3cf71-116">Actual</span></span>
- <span data-ttu-id="3cf71-117">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="3cf71-117">Bookable Resource</span></span>
- <span data-ttu-id="3cf71-118">Estimatlinje</span><span class="sxs-lookup"><span data-stu-id="3cf71-118">Estimate Line</span></span>
- <span data-ttu-id="3cf71-119">Projektopgave</span><span class="sxs-lookup"><span data-stu-id="3cf71-119">Project Task</span></span>
- <span data-ttu-id="3cf71-120">Fakturalinjedetalje</span><span class="sxs-lookup"><span data-stu-id="3cf71-120">Invoice Line Detail</span></span>
- <span data-ttu-id="3cf71-121">Kladdelinje</span><span class="sxs-lookup"><span data-stu-id="3cf71-121">Journal Line</span></span>
- <span data-ttu-id="3cf71-122">Projektkontraktlinjedetalje</span><span class="sxs-lookup"><span data-stu-id="3cf71-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="3cf71-123">Medlem af projektteam</span><span class="sxs-lookup"><span data-stu-id="3cf71-123">Project Team Member</span></span>
- <span data-ttu-id="3cf71-124">Tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="3cf71-124">Quote Line Detail</span></span>
- <span data-ttu-id="3cf71-125">Rolleprisavance</span><span class="sxs-lookup"><span data-stu-id="3cf71-125">Role Price Markup</span></span>
- <span data-ttu-id="3cf71-126">Rollepris</span><span class="sxs-lookup"><span data-stu-id="3cf71-126">Role Price</span></span> 
- <span data-ttu-id="3cf71-127">Tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="3cf71-127">Time Entry</span></span> 

> ![Tilføje eksisterende objekter i prisdimensionsløsningen](media/Existing-entities-to-PD-solution.png)

> ![Vælge løsningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="3cf71-130">Sørg for at inkludere alle formularer og visninger for hvert af de valgte objekter.</span><span class="sxs-lookup"><span data-stu-id="3cf71-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="3cf71-131">Vælg **Nej**, når du bliver bedt om at inkludere afhængige objekter for de valgte objekter.</span><span class="sxs-lookup"><span data-stu-id="3cf71-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Inkluder ikke alle relaterede komponenter](media/Do-not-include-required.png)


