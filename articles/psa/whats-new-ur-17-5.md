---
title: Nyheder eller ændringer i opdateringsudgivelse 17.5 til Project Service Automation, hotfix V3
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 17.5, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 235a27d45b3c82303d4ef5434c779b3c11421586
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118781"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="d836d-103">Opdateringsudgivelse 17.5 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="d836d-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="d836d-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d836d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d836d-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="d836d-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="d836d-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d836d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d836d-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="d836d-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="d836d-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d836d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d836d-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for V3, 17.5. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="d836d-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="d836d-110">Denne version har build-nummer V3.10.7.32 og er generelt tilgængelig via en opdatering, du selv skal foretage, i marts 2020.</span><span class="sxs-lookup"><span data-stu-id="d836d-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="d836d-111">17.5. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="d836d-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d836d-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="d836d-112">Bug fixes</span></span>


<span data-ttu-id="d836d-113">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="d836d-113">**Project Management**</span></span>

- <span data-ttu-id="d836d-114">Løst: Problemer med synkronisering på serversiden, som opstår i forbindelse med opgaver med lang varighed, er blevet håndteret.</span><span class="sxs-lookup"><span data-stu-id="d836d-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="d836d-115">Løst: 24-timers arbejdstimeskabeloner tilføjer ved en fejl en ekstra dag til opgaver.</span><span class="sxs-lookup"><span data-stu-id="d836d-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="d836d-116">Løst: Håndtering af +13 GMT-arbejdstimeskabeloner, hvor der ved en fejl skiftes opgaver én dag for tidligt.</span><span class="sxs-lookup"><span data-stu-id="d836d-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

