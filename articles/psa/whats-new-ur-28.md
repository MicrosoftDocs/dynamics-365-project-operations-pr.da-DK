---
title: Nyheder eller ændringer i opdateringsudgivelse 28, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 28, V3.
author: ruhercul
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010509"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="b617c-103">Nyheder eller ændringer i opdateringsudgivelse 28, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b617c-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b617c-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b617c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b617c-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="b617c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b617c-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b617c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b617c-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="b617c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b617c-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b617c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b617c-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede i forbindelse med Project Service Automation V3, opdateringsudgivelse 28. Denne version har build-nummer V3.10.46.32 og er generelt tilgængelig via selvopdatering i januar 2021.</span><span class="sxs-lookup"><span data-stu-id="b617c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="b617c-110">28. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="b617c-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b617c-111">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="b617c-111">Bug fixes</span></span>

<span data-ttu-id="b617c-112">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="b617c-112">**Time and Expense**</span></span>

<span data-ttu-id="b617c-113">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="b617c-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="b617c-114">Brugerne kan bruge **Masseredigering** til at opdatere tidsregistreringer, der er godkendt og indsendt.</span><span class="sxs-lookup"><span data-stu-id="b617c-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="b617c-115">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="b617c-115">**Project Management**</span></span>

<span data-ttu-id="b617c-116">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="b617c-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="b617c-117">I de tilfælde, hvor opgave-GUID'et fortolkes som et tal, kan opgaver ikke åbnes til redigering ved hjælp af **Rediger opgave** på båndet på siden **Arbejdsopgavehierarki**.</span><span class="sxs-lookup"><span data-stu-id="b617c-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="b617c-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b617c-118">**Sales**</span></span>

<span data-ttu-id="b617c-119">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="b617c-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="b617c-120">Der genereres en null-referenceundtagelse, når tilføjelsesprogrammet **GetEstimatesForProject** aktiveres.</span><span class="sxs-lookup"><span data-stu-id="b617c-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="b617c-121">**Markering af klar til at blive faktureret** i milepælsgitteret, opdaterer kun attributter delvist, bortset fra attributten **Fakturastatus**, som opdateres.</span><span class="sxs-lookup"><span data-stu-id="b617c-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]