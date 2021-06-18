---
title: Nyheder eller ændringer i opdateringsudgivelse 15, V3, til Project Service Automation
description: Dette emne indeholder oplysninger om nyhederne i 15. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 86aadca637939120d0ccd839e7c425e9e8d38aec
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006819"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="16097-103">Opdateringsudgivelse 15 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="16097-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="16097-104">Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="16097-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="16097-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="16097-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="16097-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="16097-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="16097-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="16097-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="16097-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="16097-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="16097-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 15. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="16097-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="16097-110">Denne version har build-nummer V3.10.5.28 og er generelt tilgængelig via en opdatering, du selv skal foretage, i januar 2020.</span><span class="sxs-lookup"><span data-stu-id="16097-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="16097-111">15. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="16097-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="16097-112">Forbedringer</span><span class="sxs-lookup"><span data-stu-id="16097-112">Enhancements</span></span>

- <span data-ttu-id="16097-113">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="16097-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="16097-114">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="16097-114">Bug fixes</span></span>

- <span data-ttu-id="16097-115">Tid og udgift</span><span class="sxs-lookup"><span data-stu-id="16097-115">Time and Expense</span></span>

  - <span data-ttu-id="16097-116">Løst: Du kan tilføje fejlbehandling ved indlæsning i afstemningsvisningen.</span><span class="sxs-lookup"><span data-stu-id="16097-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="16097-117">Løst: Projektressourcehub: Omdøb **Beløb** for mindre flertydighed.</span><span class="sxs-lookup"><span data-stu-id="16097-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="16097-118">Løst: Juster visningen af **Kopier kolonnerne for tidsregistrering** for at medtage typen.</span><span class="sxs-lookup"><span data-stu-id="16097-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="16097-119">Løst: Redigering af varighed af tidsregistrering i gittervisning ved hjælp af decimaltal resulterer i en ukendt fejl for visse tal.</span><span class="sxs-lookup"><span data-stu-id="16097-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="16097-120">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="16097-120">Project Management</span></span>

  - <span data-ttu-id="16097-121">Løst: Rullemenuen til **Brug i sporingsvisning** udvides nu på baggrund af bredden af indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="16097-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="16097-122">Løst: I forbindelse med styringen af projekter i tidszonen +13, kan der blive vist unøjagtige resultater i opgaveberegninger.</span><span class="sxs-lookup"><span data-stu-id="16097-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="16097-123">Løst: **Sluttidspunktet for teammedlem** er blevet rettet, når der bruges en 24-timerskalender.</span><span class="sxs-lookup"><span data-stu-id="16097-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="16097-124">Løst: **BPF** i hovedformularen **msdyn_project** er atter aktiveret.</span><span class="sxs-lookup"><span data-stu-id="16097-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="16097-125">Løst: Beregning af tildelinger ignorerer ikke længere en dag.</span><span class="sxs-lookup"><span data-stu-id="16097-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="16097-126">Løst: Der er føjet et nyt meddelelsesbanner til projektformularen, når der er afvigelser mellem tidszonen for bruger og projekt.</span><span class="sxs-lookup"><span data-stu-id="16097-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="16097-127">Sales</span><span class="sxs-lookup"><span data-stu-id="16097-127">Sales</span></span>

  - <span data-ttu-id="16097-128">Løst: Opslag i kategorien for estimerede udgifter kan anvendes til at filtrere dubletter.</span><span class="sxs-lookup"><span data-stu-id="16097-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="16097-129">Løst: Koden i **PluginDomain.ExecuteInTryCatchBlock(..)** skjuler ikke længere undtagelsens oprindelse.</span><span class="sxs-lookup"><span data-stu-id="16097-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="16097-130">Løst: Du får ikke længere en fejlmeddelelse i **Projektopslag** i formularen **Tilbudslinje**, når der er mere end 1.000 projekter.</span><span class="sxs-lookup"><span data-stu-id="16097-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="16097-131">Løst: Gitteret **Anslået** for arbejdsestimater og udgiftsestimater viser nu det korrekte valutasymbol.</span><span class="sxs-lookup"><span data-stu-id="16097-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="16097-132">Løst: Når en organisation opdaterer PSA fra 14. opdateringsudgivelse til 15. opdateringsudgivelse, vises fanen **Planlægning** ikke længere som tom i formularen **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="16097-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]