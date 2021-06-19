---
title: Nyheder eller ændringer i opdateringsudgivelse 32, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129659"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="c3c97-103">Nyheder eller ændringer i opdateringsudgivelse 32, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c3c97-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c3c97-104">Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen.</span><span class="sxs-lookup"><span data-stu-id="c3c97-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="c3c97-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="c3c97-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c3c97-106">Den er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c3c97-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c3c97-107">Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="c3c97-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="c3c97-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c3c97-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c3c97-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 32. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="c3c97-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="c3c97-110">Denne version har buildnummer V3.10.53.108 og er generelt tilgængelig via en selvopdatering i juni 2021.</span><span class="sxs-lookup"><span data-stu-id="c3c97-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="c3c97-111">32. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="c3c97-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c3c97-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="c3c97-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="c3c97-113">Generelt</span><span class="sxs-lookup"><span data-stu-id="c3c97-113">General</span></span>

- <span data-ttu-id="c3c97-114">Når en større opgradering mislykkes, bør kun indgangspunkterne i hovedprogrammet blive blokeret for at sikre, at delte objekter stadig er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="c3c97-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="c3c97-115">Tid og udgift</span><span class="sxs-lookup"><span data-stu-id="c3c97-115">Time and Expense</span></span>

<span data-ttu-id="c3c97-116">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="c3c97-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="c3c97-117">**TimeEntriesImportFromResourceAssignment** vedligeholder ikke start- og sluttiderne for ressourcetildelingsudsnit.</span><span class="sxs-lookup"><span data-stu-id="c3c97-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="c3c97-118">Når du vælger **Åben post** i gitteret **Tidsregistrering**, kan du muligvis ikke vælge andre formularer.</span><span class="sxs-lookup"><span data-stu-id="c3c97-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="c3c97-119">Mens du importerer tildelinger til tidsregistreringen, kan klientkodeforespørgslen oprette en lang URL-adresse, som ikke lykkes med at udføre forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="c3c97-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="c3c97-120">Når en værdi er slettet fra en celle i gitteret **Tidsregistrering**, forbliver fokus ikke på gitteret.</span><span class="sxs-lookup"><span data-stu-id="c3c97-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="c3c97-121">Knappen **Afvis** er blevet fjernet fra visningen **Behandling af godkendelser** for moderne godkendelser.</span><span class="sxs-lookup"><span data-stu-id="c3c97-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="c3c97-122">Stabiliteten og ydeevnen af massegodkendelse af tidsregistreringer påvirkes af fastlåsninger og en fejl i den passende håndtering af tilpasninger, der er relateret til objektet **Tidsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="c3c97-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="c3c97-123">Projektplanlægning</span><span class="sxs-lookup"><span data-stu-id="c3c97-123">Project Planning</span></span>

- <span data-ttu-id="c3c97-124">Der oprettes en nulreferenceundtagelse, når du opdaterer et projekt, der har en null-værdi i feltet **Kontraktenhed**.</span><span class="sxs-lookup"><span data-stu-id="c3c97-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="c3c97-125">**Opdater projekttotaler** beregner de resterende omkostninger og salg i et projekt forkert.</span><span class="sxs-lookup"><span data-stu-id="c3c97-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="c3c97-126">Overflødige prisfastsættelsesberegninger påvirker den ydeevne, der er relateret til opdateringer af ressourcetildelinger.</span><span class="sxs-lookup"><span data-stu-id="c3c97-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="c3c97-127">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="c3c97-127">Resource Management</span></span>

<span data-ttu-id="c3c97-128">Følgende fejl er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="c3c97-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="c3c97-129">Når en reserverbar ressources kalenderkapacitet er større end 1, genkender Project Service Automation ikke kapaciteten korrekt som 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="c3c97-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="c3c97-130">Der indtræffer derfor en uendelig løkke i planlægningsvisningen.</span><span class="sxs-lookup"><span data-stu-id="c3c97-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="c3c97-131">Salg</span><span class="sxs-lookup"><span data-stu-id="c3c97-131">Sales</span></span>

<span data-ttu-id="c3c97-132">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="c3c97-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="c3c97-133">Når der oprettes en gitterlinje, som har en brugerdefineret transaktionstype, indtræffer følgende null-referenceundtagelse: *Microsoft.Dynamics.ProjectService.Plugins.StilstandLinePlugins.ValidateUnitScheduleAndUnitActionTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodePlaugin)*.</span><span class="sxs-lookup"><span data-stu-id="c3c97-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="c3c97-134">Der bør ikke tilføjes roller og kategorier, der er deaktiveret, før et tilbud kopieres til fakturerbare roller og kategorier i det nyligt kopierede tilbud.</span><span class="sxs-lookup"><span data-stu-id="c3c97-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="c3c97-135">Dokumentdatoen og regnskabsdatoen stemmer ikke overens med den startdato, der findes på en fakturalinjedetalje, som oprettes direkte på en kladdefaktura.</span><span class="sxs-lookup"><span data-stu-id="c3c97-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="c3c97-136">Der oprettes null-referenceundtagelser i scenarier, der er relateret til deaktiveringen af roller og kategorier, før et tilbud kopieres.</span><span class="sxs-lookup"><span data-stu-id="c3c97-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="c3c97-137">Handlingen **Opdater priser** på siden **Projekter** opdaterer ikke udgiftsestimater og materialeestimater.</span><span class="sxs-lookup"><span data-stu-id="c3c97-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
