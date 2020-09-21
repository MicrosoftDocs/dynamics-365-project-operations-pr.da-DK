---
title: Nyheder i 15. opdateringsudgivelse til Project Service Automation, V3
description: Dette emne indeholder oplysninger om nyhederne i 15. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750542"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="4db89-103">15. opdateringsudgivelse til Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="4db89-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="4db89-104">Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="4db89-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="4db89-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="4db89-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4db89-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4db89-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4db89-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="4db89-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="4db89-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4db89-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4db89-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 15. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="4db89-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="4db89-110">Denne version har build-nummer V3.10.5.28 og er generelt tilgængelig via en opdatering, du selv skal foretage, i januar 2020.</span><span class="sxs-lookup"><span data-stu-id="4db89-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="4db89-111">15. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="4db89-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="4db89-112">Forbedringer</span><span class="sxs-lookup"><span data-stu-id="4db89-112">Enhancements</span></span>

- <span data-ttu-id="4db89-113">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="4db89-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4db89-114">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="4db89-114">Bug fixes</span></span>

- <span data-ttu-id="4db89-115">Tid og udgift</span><span class="sxs-lookup"><span data-stu-id="4db89-115">Time and Expense</span></span>

  - <span data-ttu-id="4db89-116">Løst: Du kan tilføje fejlbehandling ved indlæsning i afstemningsvisningen.</span><span class="sxs-lookup"><span data-stu-id="4db89-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="4db89-117">Løst: Projektressourcehub: Omdøb **Beløb** for mindre flertydighed.</span><span class="sxs-lookup"><span data-stu-id="4db89-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="4db89-118">Løst: Juster visningen af **Kopier kolonnerne for tidsregistrering** for at medtage typen.</span><span class="sxs-lookup"><span data-stu-id="4db89-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="4db89-119">Løst: Redigering af varighed af tidsregistrering i gittervisning ved hjælp af decimaltal resulterer i en ukendt fejl for visse tal.</span><span class="sxs-lookup"><span data-stu-id="4db89-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="4db89-120">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="4db89-120">Project Management</span></span>

  - <span data-ttu-id="4db89-121">Løst: Rullemenuen til **Brug i sporingsvisning** udvides nu på baggrund af bredden af indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="4db89-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="4db89-122">Løst: I forbindelse med styringen af projekter i tidszonen +13, kan der blive vist unøjagtige resultater i opgaveberegninger.</span><span class="sxs-lookup"><span data-stu-id="4db89-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="4db89-123">Løst: **Sluttidspunktet for teammedlem** er blevet rettet, når der bruges en 24-timerskalender.</span><span class="sxs-lookup"><span data-stu-id="4db89-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="4db89-124">Løst: **BPF** i hovedformularen **msdyn_project** er atter aktiveret.</span><span class="sxs-lookup"><span data-stu-id="4db89-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="4db89-125">Løst: Beregning af tildelinger ignorerer ikke længere en dag.</span><span class="sxs-lookup"><span data-stu-id="4db89-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="4db89-126">Løst: Der er føjet et nyt meddelelsesbanner til projektformularen, når der er afvigelser mellem tidszonen for bruger og projekt.</span><span class="sxs-lookup"><span data-stu-id="4db89-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="4db89-127">Sales</span><span class="sxs-lookup"><span data-stu-id="4db89-127">Sales</span></span>

  - <span data-ttu-id="4db89-128">Løst: Opslag i kategorien for estimerede udgifter kan anvendes til at filtrere dubletter.</span><span class="sxs-lookup"><span data-stu-id="4db89-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="4db89-129">Løst: Koden i **PluginDomain.ExecuteInTryCatchBlock(..)** skjuler ikke længere undtagelsens oprindelse.</span><span class="sxs-lookup"><span data-stu-id="4db89-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="4db89-130">Løst: Du får ikke længere en fejlmeddelelse i **Projektopslag** i formularen **Tilbudslinje**, når der er mere end 1.000 projekter.</span><span class="sxs-lookup"><span data-stu-id="4db89-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="4db89-131">Løst: Gitteret **Anslået** for arbejdsestimater og udgiftsestimater viser nu det korrekte valutasymbol.</span><span class="sxs-lookup"><span data-stu-id="4db89-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="4db89-132">Løst: Når en organisation opdaterer PSA fra 14. opdateringsudgivelse til 15. opdateringsudgivelse, vises fanen **Planlægning** ikke længere som tom i formularen **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="4db89-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
