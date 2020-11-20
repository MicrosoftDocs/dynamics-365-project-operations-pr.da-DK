---
title: Nyheder eller ændringer i opdateringsudgivelse 25, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183536"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="8ad69-103">Nyheder eller ændringer i opdateringsudgivelse 25, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8ad69-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="8ad69-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8ad69-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8ad69-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="8ad69-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8ad69-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8ad69-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8ad69-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="8ad69-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8ad69-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8ad69-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8ad69-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede i forbindelse med Project Service Automation V3, opdateringsudgivelse 25. Denne version har build-nummer V 3.10.43.76 og er generelt tilgængelig via selvopdatering i oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="8ad69-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="8ad69-110">25. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="8ad69-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8ad69-111">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="8ad69-111">Bug fixes</span></span>

<span data-ttu-id="8ad69-112">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="8ad69-112">**Time and Expense**</span></span>

<span data-ttu-id="8ad69-113">Følgende fejl er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="8ad69-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="8ad69-114">Timeregistreringsdiagram viser yderligere data, som er baseret på et hentet for stort interval.</span><span class="sxs-lookup"><span data-stu-id="8ad69-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="8ad69-115">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="8ad69-115">**Resource Management**</span></span>

<span data-ttu-id="8ad69-116">Følgende fejl er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="8ad69-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="8ad69-117">Tilføjelse af kode itl Package Deployer for at springe over import af patch til Universal Resource Scheduling, hvis der allerede findes en nyere opdatering.</span><span class="sxs-lookup"><span data-stu-id="8ad69-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="8ad69-118">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="8ad69-118">**Project Management**</span></span>

<span data-ttu-id="8ad69-119">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="8ad69-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ad69-120">Rettelser af uoverensstemmelser i afrunding og valutakurs, der medfører ukorrekte planlagte omkostninger i gitteret til projektsporing.</span><span class="sxs-lookup"><span data-stu-id="8ad69-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="8ad69-121">Understøtter muligheden for at få vist to eller flere reaktionsgitre i formularen **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="8ad69-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="8ad69-122">Angivet validering for at imødegå muligheden for at tildele en opgave efter kalenderens slutdato, som resulterer i en mislykket ressourcetildeling.</span><span class="sxs-lookup"><span data-stu-id="8ad69-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="8ad69-123">Forbedret fejlhåndtering til imødegåelse af null-referenceundtagelsen, som blev genereret fra følgende:</span><span class="sxs-lookup"><span data-stu-id="8ad69-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="8ad69-124">**PreValidateProjectTeamMemberCreate**-plug-in</span><span class="sxs-lookup"><span data-stu-id="8ad69-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="8ad69-125">**PreValidateProjectTaskCreate**, når en projektopgave oprettes uden et tilknyttet projekt</span><span class="sxs-lookup"><span data-stu-id="8ad69-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="8ad69-126">**PreProjectTeamMemberCreate**-plug-in</span><span class="sxs-lookup"><span data-stu-id="8ad69-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="8ad69-127">**PostProjectTeamMemberDelete**-plug-in</span><span class="sxs-lookup"><span data-stu-id="8ad69-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="8ad69-128">**PreValidateProjectTaskDelete**-plug-in</span><span class="sxs-lookup"><span data-stu-id="8ad69-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="8ad69-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8ad69-129">**Sales**</span></span>

<span data-ttu-id="8ad69-130">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="8ad69-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ad69-131">Forbedret fejlhåndtering til imødegåelse af null-referenceundtagelser, der er genereret fra **Kopier projekt: estimering af administration af hjælperessourcer**.</span><span class="sxs-lookup"><span data-stu-id="8ad69-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="8ad69-132">**Ikke er klar til fakturering** på en **Faktureringsefterslæb for tid og materialer** rydder ikke faktureringsstatussen.</span><span class="sxs-lookup"><span data-stu-id="8ad69-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="8ad69-133">Rettede, fejlmærkede knapper for **Priser** på fanen **Rollepris** og **Katalogelementer**.</span><span class="sxs-lookup"><span data-stu-id="8ad69-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
