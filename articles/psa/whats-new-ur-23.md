---
title: Nyheder eller ændringer i opdateringsudgivelse 23, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 23, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074119"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="2bca6-103">Opdateringsudgivelse 23 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="2bca6-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="2bca6-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2bca6-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2bca6-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="2bca6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2bca6-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2bca6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2bca6-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="2bca6-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2bca6-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2bca6-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2bca6-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 23. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="2bca6-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="2bca6-110">Denne version har build-nummer V 3.10.34.30 og er generelt tilgængelig via en opdatering, som du selv skal foretage, i august 2020.</span><span class="sxs-lookup"><span data-stu-id="2bca6-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="2bca6-111">23. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="2bca6-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2bca6-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="2bca6-112">Bug fixes</span></span>

<span data-ttu-id="2bca6-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="2bca6-113">**Time and Expense**</span></span>

<span data-ttu-id="2bca6-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="2bca6-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="2bca6-115">Håndtering af en sag på kanten i **Slet projektteammedlem** for at angive en meningsfuld undtagelse.</span><span class="sxs-lookup"><span data-stu-id="2bca6-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="2bca6-116">Import af tildelinger medfører et tomt fjernelsesskærmbillede.</span><span class="sxs-lookup"><span data-stu-id="2bca6-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="2bca6-117">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="2bca6-117">**Resource Management**</span></span>

<span data-ttu-id="2bca6-118">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="2bca6-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="2bca6-119">**Ressourcekortet til ressourceudnyttelsesgitteret** viser forkerte data, når tidsskalaen er længere end fem dage.</span><span class="sxs-lookup"><span data-stu-id="2bca6-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="2bca6-120">Når kunderne opretter en reserverbar ressource, kan-plug-in'et til tider ikke automatisk tilføje ressourcen til en Microsoft Office 365-gruppe.</span><span class="sxs-lookup"><span data-stu-id="2bca6-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="2bca6-121">Visningen **Afstemning** viser manuelle konturer forkert i visningen **Uge** eller **Måned**.</span><span class="sxs-lookup"><span data-stu-id="2bca6-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="2bca6-122">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="2bca6-122">**Project Management**</span></span>

<span data-ttu-id="2bca6-123">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="2bca6-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="2bca6-124">Et stort antal objekter af typen **RetrieveMultiple for brugerindstillinger** medfører forringet ydeevne i forbindelse med projektgodkendelse og andre operationer.</span><span class="sxs-lookup"><span data-stu-id="2bca6-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="2bca6-125">Gitteret for opslag i ressourcers **Opgaveplanlægning** er begrænset, så der kun vises op til fem teammedlemmer fra projektteamet.</span><span class="sxs-lookup"><span data-stu-id="2bca6-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="2bca6-126">Gitteret for opslag i ressourcers **Opgaveplanlægning** filtrerer ikke inaktive ressourcer.</span><span class="sxs-lookup"><span data-stu-id="2bca6-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="2bca6-127">Den manuelle tilstand fungerer ikke som forventet i projektplanlægningens arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="2bca6-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="2bca6-128">Gitteret for **Opgaveplanlægning** viser **Inaktive transaktionskategorier**.</span><span class="sxs-lookup"><span data-stu-id="2bca6-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="2bca6-129">Gitteret for **Ressourcetildeling** afrunder forkert, når der er flere tildelinger i en opgave.</span><span class="sxs-lookup"><span data-stu-id="2bca6-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="2bca6-130">Der er afvigelser i afrundingsværdierne for det planlagte kostbeløb og de faktiske omkostninger for en enkelt opgave.</span><span class="sxs-lookup"><span data-stu-id="2bca6-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="2bca6-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2bca6-131">**Sales**</span></span>

<span data-ttu-id="2bca6-132">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="2bca6-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="2bca6-133">Dobbeltklik på **Hent alle transaktionskategorier** opretter flere linjer.</span><span class="sxs-lookup"><span data-stu-id="2bca6-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
