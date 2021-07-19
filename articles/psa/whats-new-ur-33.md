---
title: Nyheder eller ændringer i opdateringsudgivelse 33, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334521"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="9ac94-103">Nyheder eller ændringer i opdateringsudgivelse 33, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9ac94-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9ac94-104">Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen.</span><span class="sxs-lookup"><span data-stu-id="9ac94-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="9ac94-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="9ac94-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9ac94-106">Den er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9ac94-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9ac94-107">Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="9ac94-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="9ac94-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9ac94-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9ac94-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 33. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="9ac94-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="9ac94-110">Denne version har buildnummer V3.10.54.98 og er generelt tilgængelig via en egenopdatering i juli 2021.</span><span class="sxs-lookup"><span data-stu-id="9ac94-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="9ac94-111">33. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="9ac94-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9ac94-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="9ac94-112">Bug fixes</span></span>

<span data-ttu-id="9ac94-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="9ac94-113">**Time and Expense**</span></span>

<span data-ttu-id="9ac94-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="9ac94-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9ac94-115">To låste felter, **msdyn_description** og **msdyn_externaldescription** kan redigeres efter indsendelse.</span><span class="sxs-lookup"><span data-stu-id="9ac94-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="9ac94-116">Der vises en fejlmeddelelse, hvis der oprettes en udgiftspost, som ikke er relateret til et projekt.</span><span class="sxs-lookup"><span data-stu-id="9ac94-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="9ac94-117">Når der oprettes en tidsregistrering, angives ressourcerollen som standard til en inaktiv rolle.</span><span class="sxs-lookup"><span data-stu-id="9ac94-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="9ac94-118">Kladdelinjer, der er knyttet en tilbagekaldt eller slettet udgift, slettes ikke.</span><span class="sxs-lookup"><span data-stu-id="9ac94-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="9ac94-119">På **Formular til hurtig oprettelse af tidsregistrering** skal du opdatere visningen **Projektopgaveliste** for at ændre den som standard viste dato til opgavens startdato.</span><span class="sxs-lookup"><span data-stu-id="9ac94-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="9ac94-120">Når du opretter en tidsregistrering under fanen **Relateret** i den reserverbare ressource, oprettes tidsregistreringen forkert for den bruger, der er logget på, i stedet for den overordnede ressource, der kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="9ac94-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="9ac94-121">Nye felter tilføjes til dialogboksen **MDD-massegodkendelse**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="9ac94-122">**Projektplanlægning**</span><span class="sxs-lookup"><span data-stu-id="9ac94-122">**Project planning**</span></span>

<span data-ttu-id="9ac94-123">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="9ac94-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="9ac94-124">Dårlig ydeevne i forbindelse med oprettelse af projekter, når projektskabeloner med arbejdstid anvendes med komplekse kalendere.</span><span class="sxs-lookup"><span data-stu-id="9ac94-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="9ac94-125">Når startdatoen er større end slutdatoen, vises der en fejl i kopiprojektskabelonen på grund af forskelle i tidskomponenten i hvert felt.</span><span class="sxs-lookup"><span data-stu-id="9ac94-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="9ac94-126">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="9ac94-126">**Resource management**</span></span>

<span data-ttu-id="9ac94-127">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="9ac94-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="9ac94-128">Der bruges en forkert parameter i ressourceforbrugsforespørgslen, og XML fører til forkerte filterresultater i gitteret **Ressourceforbrug**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="9ac94-129">Bekræftelse af **Udvidelse af reservation** viser en forkert slutdato for reservationer.</span><span class="sxs-lookup"><span data-stu-id="9ac94-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="9ac94-130">**Salg**</span><span class="sxs-lookup"><span data-stu-id="9ac94-130">**Sales**</span></span>

<span data-ttu-id="9ac94-131">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="9ac94-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="9ac94-132">Der opstår en fejlmeddelelse, hvis der oprettes en kategoripris med manglende værdier.</span><span class="sxs-lookup"><span data-stu-id="9ac94-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="9ac94-133">Der opstår en fejlmeddelelse, hvis der oprettes en kontraktlinjemilepæl uden en ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="9ac94-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
