---
title: Nyheder eller ændringer i opdateringsudgivelse 29, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948615"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="6e4e3-103">Nyheder eller ændringer i opdateringsudgivelse 29, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6e4e3-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6e4e3-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6e4e3-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6e4e3-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6e4e3-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6e4e3-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6e4e3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6e4e3-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 29. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="6e4e3-110">Denne version har et build-nummer V3.10.47.7 og er generelt tilgængelig via egen opdatering i februar 2021.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="6e4e3-111">29. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="6e4e3-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6e4e3-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="6e4e3-112">Bug fixes</span></span>

<span data-ttu-id="6e4e3-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="6e4e3-113">**Time and Expense**</span></span>

<span data-ttu-id="6e4e3-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="6e4e3-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6e4e3-115">Brugere kan ikke se, at arbejdstimer er logget på fridage i gitteret for tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="6e4e3-116">Godkendte udgiftsposter kan redigeres i gitteret.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="6e4e3-117">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="6e4e3-117">**Project Management**</span></span>

<span data-ttu-id="6e4e3-118">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="6e4e3-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="6e4e3-119">Manglende valideringslogik, der sikrer, at ressourcetildelingens indsatstimer ikke kan være negative.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="6e4e3-120">Ved hjælp af den brugerdefinerede handling **AssignResourcesForTask** opdateres alle felter i stedet for kun ændrede felter.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="6e4e3-121">Når du kopierer et projekt i et miljø med tilføjelsesprogrammer eller arbejdsprocesser, der er registreret i hændelsen **Opretprojekt**, så opdateres attributten **msdyn_bulkgenerationstatus** ikke, hvis **CopyWBSToProject** mislykkes.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="6e4e3-122">Når du udvider projektkalenderen, sorteres arbejdsdagene ikke i stigende rækkefølge, hvilket medfører, at visse opdateringer af projektopgaven ikke lykkes.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="6e4e3-123">Hvis du ændrer projektlederen i et eksisterende projekt, udløses organisationsenhedens standardlogik.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="6e4e3-124">**Salg**</span><span class="sxs-lookup"><span data-stu-id="6e4e3-124">**Sales**</span></span>

<span data-ttu-id="6e4e3-125">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="6e4e3-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="6e4e3-126">Fanen **Kontraktens ydeevne** på siden **Kontrakt** forbliver stille under initialisering, når der ikke findes nogen kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="6e4e3-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>