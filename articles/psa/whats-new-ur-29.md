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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664636"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="148bc-103">Nyheder eller ændringer i opdateringsudgivelse 29, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="148bc-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="148bc-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="148bc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="148bc-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="148bc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="148bc-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="148bc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="148bc-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="148bc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="148bc-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="148bc-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="148bc-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 29. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="148bc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="148bc-110">Denne version har et build-nummer V3.10.47.7 og er generelt tilgængelig via egen opdatering i februar 2021.</span><span class="sxs-lookup"><span data-stu-id="148bc-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="148bc-111">29. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="148bc-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="148bc-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="148bc-112">Bug fixes</span></span>

<span data-ttu-id="148bc-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="148bc-113">**Time and Expense**</span></span>

<span data-ttu-id="148bc-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="148bc-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="148bc-115">Brugere kan ikke se, at arbejdstimer er logget på fridage i gitteret for tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="148bc-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="148bc-116">Godkendte udgiftsposter kan redigeres i gitteret.</span><span class="sxs-lookup"><span data-stu-id="148bc-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="148bc-117">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="148bc-117">**Project Management**</span></span>

<span data-ttu-id="148bc-118">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="148bc-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="148bc-119">Manglende valideringslogik, der sikrer, at ressourcetildelingens indsatstimer ikke kan være negative.</span><span class="sxs-lookup"><span data-stu-id="148bc-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="148bc-120">Ved hjælp af den brugerdefinerede handling **AssignResourcesForTask** opdateres alle felter i stedet for kun ændrede felter.</span><span class="sxs-lookup"><span data-stu-id="148bc-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="148bc-121">Når du kopierer et projekt i et miljø med tilføjelsesprogrammer eller arbejdsprocesser, der er registreret i hændelsen **Opretprojekt**, så opdateres attributten **msdyn_bulkgenerationstatus** ikke, hvis **CopyWBSToProject** mislykkes.</span><span class="sxs-lookup"><span data-stu-id="148bc-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="148bc-122">Når du udvider projektkalenderen, sorteres arbejdsdagene ikke i stigende rækkefølge, hvilket medfører, at visse opdateringer af projektopgaven ikke lykkes.</span><span class="sxs-lookup"><span data-stu-id="148bc-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="148bc-123">Hvis du ændrer projektlederen i et eksisterende projekt, udløses organisationsenhedens standardlogik.</span><span class="sxs-lookup"><span data-stu-id="148bc-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="148bc-124">**Salg**</span><span class="sxs-lookup"><span data-stu-id="148bc-124">**Sales**</span></span>

<span data-ttu-id="148bc-125">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="148bc-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="148bc-126">Fanen **Kontraktens ydeevne** på siden **Kontrakt** forbliver stille under initialisering, når der ikke findes nogen kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="148bc-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
