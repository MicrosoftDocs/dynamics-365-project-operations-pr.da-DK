---
title: Opret en løsning til brugerdefinerede prisfastsættelsesdimensioner
description: Dette emne indeholder oplysninger om, hvordan du opretter løsninger for brugertilpassede prisfastsættelsesdimensioner.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278411"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="0ce21-103">Opret en løsning til brugerdefinerede prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="0ce21-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="0ce21-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0ce21-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="0ce21-105">Alle ændringer af brugerdefineret prisfastsættelsesdimensioner bør være i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="0ce21-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="0ce21-106">Denne vigtige bedste praksis tillader større fleksibilitet til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til andre forekomster.</span><span class="sxs-lookup"><span data-stu-id="0ce21-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="0ce21-107">Når du foretager de nødvendige ændringer, skal du eksportere løsningen som en **Administreret** løsning og derefter importere den i andre forekomster for at genbruge den.</span><span class="sxs-lookup"><span data-stu-id="0ce21-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="0ce21-108">Opret en løsning til brugerdefinerede prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="0ce21-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="0ce21-109">Vælg **Indstillinger** > **Løsninger**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0ce21-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="0ce21-110">Navngiv løsningen *<your organization name> prisfastsættelsesdimensioner*.</span><span class="sxs-lookup"><span data-stu-id="0ce21-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="0ce21-111">Angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0ce21-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Oprettelse af en løsning til brugerdefinerede prisfastsættelsesdimensioner](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="0ce21-113">Tilføj alle nødvendige objekter og relaterede komponenter i løsningen til prisfastsættelsesdimensionen</span><span class="sxs-lookup"><span data-stu-id="0ce21-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="0ce21-114">Tilføj følgende Project Service-objekter til din prisfastsættelsesløsning for at foretage vigtige skemaændringer i prisfastsættelsesløsningen.</span><span class="sxs-lookup"><span data-stu-id="0ce21-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="0ce21-115">Når du har fuldført denne procedure, genkender objekterne de nye prisfastsættelsesdimensioner.</span><span class="sxs-lookup"><span data-stu-id="0ce21-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="0ce21-116">Vælg **Indstillinger** > **Løsninger**, og dobbeltklik derefter på **<*dit organisationsnavn*> prisfastsættelsesdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="0ce21-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="0ce21-117">Vælg **Tilføj eksisterende** > **Objekter** i venstre navigationsrude i løsningsoversigten.</span><span class="sxs-lookup"><span data-stu-id="0ce21-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="0ce21-118">Vælg følgende objekter i dialogboksen **Løsningskomponenter**:</span><span class="sxs-lookup"><span data-stu-id="0ce21-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="0ce21-119">**Faktisk**</span><span class="sxs-lookup"><span data-stu-id="0ce21-119">**Actual**</span></span>
   - <span data-ttu-id="0ce21-120">**Reserverbar ressource**</span><span class="sxs-lookup"><span data-stu-id="0ce21-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="0ce21-121">**Estimatlinje**</span><span class="sxs-lookup"><span data-stu-id="0ce21-121">**Estimate Line**</span></span>
   - <span data-ttu-id="0ce21-122">**Projektopgave**</span><span class="sxs-lookup"><span data-stu-id="0ce21-122">**Project Task**</span></span>
   - <span data-ttu-id="0ce21-123">**Fakturalinjedetalje**</span><span class="sxs-lookup"><span data-stu-id="0ce21-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="0ce21-124">**Kladdelinje**</span><span class="sxs-lookup"><span data-stu-id="0ce21-124">**Journal Line**</span></span>
   - <span data-ttu-id="0ce21-125">**Projektkontraktlinjedetalje**</span><span class="sxs-lookup"><span data-stu-id="0ce21-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="0ce21-126">**Medlem af projektteam**</span><span class="sxs-lookup"><span data-stu-id="0ce21-126">**Project Team Member**</span></span>
   - <span data-ttu-id="0ce21-127">**Tilbudslinjedetaljer**</span><span class="sxs-lookup"><span data-stu-id="0ce21-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="0ce21-128">**Rolleprisavance**</span><span class="sxs-lookup"><span data-stu-id="0ce21-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="0ce21-129">**Rollepris**</span><span class="sxs-lookup"><span data-stu-id="0ce21-129">**Role Price**</span></span>
   - <span data-ttu-id="0ce21-130">**Tidsregistrering**</span><span class="sxs-lookup"><span data-stu-id="0ce21-130">**Time Entry**</span></span>
 
   ![Tilføj eksisterende løsning for brugertilpasset prisfastsættelsesdimension](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="0ce21-132">Gennemgå for hvert objekt de komponenter, der tilføjes, og den endelige liste over enhedsaktiver for hver enhed.</span><span class="sxs-lookup"><span data-stu-id="0ce21-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="0ce21-133">Inkluder alle formularer og visninger for hvert af de valgte objekter.</span><span class="sxs-lookup"><span data-stu-id="0ce21-133">Include all forms and views for each of the selected entities.</span></span>

  ![Objekter tilføjet](./media/solution-component-selection.png)


5.  <span data-ttu-id="0ce21-135">Når du bliver bedt om at medtage eventuelle afhængige objekter for de valgte objekter, skal du vælge **Nej, medtag ikke de påkrævede komponenter.**</span><span class="sxs-lookup"><span data-stu-id="0ce21-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Herunder afhængige enheder](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]