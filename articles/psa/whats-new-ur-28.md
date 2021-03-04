---
title: Nyheder eller ændringer i opdateringsudgivelse 28, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150616"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="07e94-103">Nyheder eller ændringer i opdateringsudgivelse 28, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="07e94-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="07e94-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="07e94-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="07e94-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="07e94-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="07e94-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="07e94-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="07e94-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="07e94-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="07e94-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="07e94-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="07e94-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede i forbindelse med Project Service Automation V3, opdateringsudgivelse 28. Denne version har build-nummer V3.10.46.32 og er generelt tilgængelig via selvopdatering i januar 2021.</span><span class="sxs-lookup"><span data-stu-id="07e94-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="07e94-110">28. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="07e94-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="07e94-111">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="07e94-111">Bug fixes</span></span>

<span data-ttu-id="07e94-112">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="07e94-112">**Time and Expense**</span></span>

<span data-ttu-id="07e94-113">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="07e94-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="07e94-114">Brugerne kan bruge **Masseredigering** til at opdatere tidsregistreringer, der er godkendt og indsendt.</span><span class="sxs-lookup"><span data-stu-id="07e94-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="07e94-115">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="07e94-115">**Project Management**</span></span>

<span data-ttu-id="07e94-116">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="07e94-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="07e94-117">I de tilfælde, hvor opgave-GUID'et fortolkes som et tal, kan opgaver ikke åbnes til redigering ved hjælp af **Rediger opgave** på båndet på siden **Arbejdsopgavehierarki**.</span><span class="sxs-lookup"><span data-stu-id="07e94-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="07e94-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="07e94-118">**Sales**</span></span>

<span data-ttu-id="07e94-119">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="07e94-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="07e94-120">Der genereres en null-referenceundtagelse, når tilføjelsesprogrammet **GetEstimatesForProject** aktiveres.</span><span class="sxs-lookup"><span data-stu-id="07e94-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="07e94-121">**Markering af klar til at blive faktureret** i milepælsgitteret, opdaterer kun attributter delvist, bortset fra attributten **Fakturastatus**, som opdateres.</span><span class="sxs-lookup"><span data-stu-id="07e94-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

