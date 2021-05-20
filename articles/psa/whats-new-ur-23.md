---
title: Nyheder eller ændringer i opdateringsudgivelse 23, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: f90c0d2168b261cf1b6ef10374f282274ea61af5
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948952"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="376f9-103">Opdateringsudgivelse 23 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="376f9-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="376f9-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="376f9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="376f9-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="376f9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="376f9-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="376f9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="376f9-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="376f9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="376f9-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="376f9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="376f9-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 23. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="376f9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="376f9-110">Denne version har build-nummer V 3.10.34.30 og er generelt tilgængelig via en opdatering, som du selv skal foretage, i august 2020.</span><span class="sxs-lookup"><span data-stu-id="376f9-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="376f9-111">23. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="376f9-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="376f9-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="376f9-112">Bug fixes</span></span>

<span data-ttu-id="376f9-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="376f9-113">**Time and Expense**</span></span>

<span data-ttu-id="376f9-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="376f9-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="376f9-115">Håndtering af en sag på kanten i **Slet projektteammedlem** for at angive en meningsfuld undtagelse.</span><span class="sxs-lookup"><span data-stu-id="376f9-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="376f9-116">Import af tildelinger medfører et tomt fjernelsesskærmbillede.</span><span class="sxs-lookup"><span data-stu-id="376f9-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="376f9-117">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="376f9-117">**Resource Management**</span></span>

<span data-ttu-id="376f9-118">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="376f9-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="376f9-119">**Ressourcekortet til ressourceudnyttelsesgitteret** viser forkerte data, når tidsskalaen er længere end fem dage.</span><span class="sxs-lookup"><span data-stu-id="376f9-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="376f9-120">Når kunderne opretter en reserverbar ressource, kan-plug-in'et til tider ikke automatisk tilføje ressourcen til en Microsoft Office 365-gruppe.</span><span class="sxs-lookup"><span data-stu-id="376f9-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="376f9-121">Visningen **Afstemning** viser manuelle konturer forkert i visningen **Uge** eller **Måned**.</span><span class="sxs-lookup"><span data-stu-id="376f9-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="376f9-122">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="376f9-122">**Project Management**</span></span>

<span data-ttu-id="376f9-123">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="376f9-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="376f9-124">Et stort antal objekter af typen **RetrieveMultiple for brugerindstillinger** medfører forringet ydeevne i forbindelse med projektgodkendelse og andre operationer.</span><span class="sxs-lookup"><span data-stu-id="376f9-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="376f9-125">Gitteret for opslag i ressourcers **Opgaveplanlægning** er begrænset, så der kun vises op til fem teammedlemmer fra projektteamet.</span><span class="sxs-lookup"><span data-stu-id="376f9-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="376f9-126">Gitteret for opslag i ressourcers **Opgaveplanlægning** filtrerer ikke inaktive ressourcer.</span><span class="sxs-lookup"><span data-stu-id="376f9-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="376f9-127">Den manuelle tilstand fungerer ikke som forventet i projektplanlægningens arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="376f9-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="376f9-128">Gitteret for **Opgaveplanlægning** viser **Inaktive transaktionskategorier**.</span><span class="sxs-lookup"><span data-stu-id="376f9-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="376f9-129">Gitteret for **Ressourcetildeling** afrunder forkert, når der er flere tildelinger i en opgave.</span><span class="sxs-lookup"><span data-stu-id="376f9-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="376f9-130">Der er afvigelser i afrundingsværdierne for det planlagte kostbeløb og de faktiske omkostninger for en enkelt opgave.</span><span class="sxs-lookup"><span data-stu-id="376f9-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="376f9-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="376f9-131">**Sales**</span></span>

<span data-ttu-id="376f9-132">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="376f9-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="376f9-133">Dobbeltklik på **Hent alle transaktionskategorier** opretter flere linjer.</span><span class="sxs-lookup"><span data-stu-id="376f9-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]