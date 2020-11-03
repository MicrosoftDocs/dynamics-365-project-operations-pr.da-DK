---
title: Nyheder eller ændringer i opdateringsudgivelse 19, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 19, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074125"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="fc6ec-103">Opdateringsudgivelse 19 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="fc6ec-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="fc6ec-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fc6ec-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fc6ec-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fc6ec-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fc6ec-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fc6ec-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fc6ec-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 19. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="fc6ec-110">Denne version har buildnummer V3.10.30.41 og er generelt tilgængelig via en opdatering, du selv har udført i maj 2020.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="fc6ec-111">19. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="fc6ec-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fc6ec-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="fc6ec-112">Bug fixes</span></span>

<span data-ttu-id="fc6ec-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="fc6ec-113">**Time and Expense**</span></span>

<span data-ttu-id="fc6ec-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="fc6ec-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="fc6ec-115">Fejl, der er afledt af import af tidsangivelser, er ikke bragt op til overfladen korrekt.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="fc6ec-116">Gitteret for tidsangivelse understøtter ikke adfærden for feltet **Kun dato**.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="fc6ec-117">Projektressourcer kan ikke oprette udgifter til et projekt.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="fc6ec-118">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="fc6ec-118">**Project Management**</span></span>

<span data-ttu-id="fc6ec-119">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="fc6ec-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="fc6ec-120">En underordnet opgave resulterer i et forkert indsatsestimat i forbindelse med beregningen af fuldførelse (EAC).</span><span class="sxs-lookup"><span data-stu-id="fc6ec-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="fc6ec-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="fc6ec-121">**Sales**</span></span>

<span data-ttu-id="fc6ec-122">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="fc6ec-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="fc6ec-123">Funktionen **Genberegning** fungerer ikke sammen med detaljer om kontraktlinjer for udgifter eller detaljer om tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="fc6ec-124">Der mangler **Opdater priser** for udgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="fc6ec-125">Kunderne kan ikke vælge brugerdefinerede kontraktstatusårsager på siden **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="fc6ec-126">Kunder oplever forringet ydeevne, når der oprettes en brugerdefineret prisliste ud fra et tilbud.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="fc6ec-127">Kunder oplever uoverensstemmelse med standarderne **enhed** på siderne **Detaljer om tilbudslinje** og **Detaljer om kontraktlinje**.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="fc6ec-128">Tilføjelse af elementer for ikke-fakturerbare transaktionskategorier til en debiterbar kontraktlinje respekterer ikke transaktionskategoriens faktureringstype **Ikke-fakturerbar**.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="fc6ec-129">Kunderne kan ikke bruge de netop tilføjede roller og kategorier i tidligere oprettede kontrakter.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="fc6ec-130">Kunder oplever forringet ydeevne ved unødvendig hentning i PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="fc6ec-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="fc6ec-131">Roller, der er konfigureret som ikke-fakturerbare på listen **Ressourcekategorier** , skal føjes til fanen **Fakturerbare roller** som **Ikke-fakturerbare** på kontraktlinjen for et projekt.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="fc6ec-132">Kunderne kan opleve forringet ydeevne, når de opretter et projekt, da **GetBookableResourceIdFromUser** henter alle kolonner med reserv rbare ressourcer i stedet for kun det primære id.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="fc6ec-133">Objektet **TransactionType** mangler plug-in'en til opdatering før validering for at forhindre brugere i at angive **Enheder** og **UnitGroups** , der ikke er gyldige for transaktionstyper.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="fc6ec-134">Trinnet **Fjern** virker ikke for import af tidsangivelse.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-134">The **Remove** step does not work for time entry import.</span></span>
