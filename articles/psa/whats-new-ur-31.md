---
title: Nyheder eller ændringer i opdateringsudgivelse 31, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999124"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="33f09-103">Nyheder eller ændringer i opdateringsudgivelse 31, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="33f09-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="33f09-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="33f09-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="33f09-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="33f09-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="33f09-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="33f09-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="33f09-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="33f09-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="33f09-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="33f09-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="33f09-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 31. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="33f09-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="33f09-110">Denne version har buildnummer V3.10.52.77 og er generelt tilgængelig via en opdatering, du selv har udført i maj 2021.</span><span class="sxs-lookup"><span data-stu-id="33f09-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="33f09-111">31. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="33f09-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="33f09-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="33f09-112">Bug fixes</span></span>

<span data-ttu-id="33f09-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="33f09-113">**Time and Expense**</span></span>

<span data-ttu-id="33f09-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="33f09-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="33f09-115">Kommandoknapperne for tidsregistrering på siden **Reserverbar ressource** var forvirrende.</span><span class="sxs-lookup"><span data-stu-id="33f09-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="33f09-116">Der blev genereret en nulreferenceundtagelse **i Project.SetTrackingFields**, når en tidsregistrering godkendes.</span><span class="sxs-lookup"><span data-stu-id="33f09-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="33f09-117">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="33f09-117">**Resource Management**</span></span>

<span data-ttu-id="33f09-118">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="33f09-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="33f09-119">**Opret teammedlem** viser ikke korrekt indstillingen for metadata for reservationskonfiguration for **Standardstatus for bunden reservation**.</span><span class="sxs-lookup"><span data-stu-id="33f09-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="33f09-120">Når der opgraderes fra PSA 1.X til 3.X, mislykkes opgraderingsprocessen ved **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="33f09-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="33f09-121">**Salg**</span><span class="sxs-lookup"><span data-stu-id="33f09-121">**Sales**</span></span>

<span data-ttu-id="33f09-122">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="33f09-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="33f09-123">Faktisk omsætning konverterer beløbene til projektvalutaen i sporingsgitteret.</span><span class="sxs-lookup"><span data-stu-id="33f09-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="33f09-124">Valutastandarden er uklar, når der oprettes kladdelinjer, tilbudslinjer og kontraktlinjer i scenarier, hvor en organisations grundvaluta er forskellig fra projektvalutaen.</span><span class="sxs-lookup"><span data-stu-id="33f09-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="33f09-125">Forespørgslen **Afventende validering af rettelseskladde** filtrerer ikke efter projekt.</span><span class="sxs-lookup"><span data-stu-id="33f09-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="33f09-126">Resterende salg beregnes forkert i et projekt.</span><span class="sxs-lookup"><span data-stu-id="33f09-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="33f09-127">Tilbud, der er baseret på en kontakt, kan ikke oprettes, når de oprettes uden en prisliste.</span><span class="sxs-lookup"><span data-stu-id="33f09-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="33f09-128">Der vises ingen behandlingsspinner, når du vælger **Bekræft faktura**.</span><span class="sxs-lookup"><span data-stu-id="33f09-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="33f09-129">Der vises ingen behandlingsspinner, når du vælger **Opret faktura**.</span><span class="sxs-lookup"><span data-stu-id="33f09-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="33f09-130">Hvis du lukker et tilbud som tabt, annulleres reservationerne ikke.</span><span class="sxs-lookup"><span data-stu-id="33f09-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







