---
title: Nyheder eller ændringer i opdateringsudgivelse 29.5 til Project Service Automation hotfix V3
description: I dette emne vises de funktioner og rettelser, der er tilgængelige i Project Service Automation, opdateringsudgivelse 29.5 hotfix, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715655"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="fdf69-103">Nyheder eller ændringer i opdateringsudgivelse 29.5, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fdf69-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="fdf69-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fdf69-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fdf69-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="fdf69-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fdf69-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fdf69-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fdf69-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="fdf69-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fdf69-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fdf69-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fdf69-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 29.5. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="fdf69-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="fdf69-110">Denne version har build-nummer V3.10.47.150 og er generelt tilgængelig via en opdatering, du selv skal foretage, i januar 2021.</span><span class="sxs-lookup"><span data-stu-id="fdf69-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="fdf69-111">29.5. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="fdf69-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fdf69-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="fdf69-112">Bug fixes</span></span>


<span data-ttu-id="fdf69-113">**Salg**</span><span class="sxs-lookup"><span data-stu-id="fdf69-113">**Sales**</span></span>

<span data-ttu-id="fdf69-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="fdf69-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="fdf69-115">Der kan opstå en nulreferenceundtagelse i **ContractLineMapHelper.UpdateContractLineDetailPriceListReference**, når du lukker et tilbud som vundet, og tilbuddet ikke indeholder en prisliste.</span><span class="sxs-lookup"><span data-stu-id="fdf69-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
