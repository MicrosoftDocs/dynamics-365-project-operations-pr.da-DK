---
title: Oversigt over planlægningsassistent
description: Dette emne indeholder oplysninger om, hvordan du kan arbejde med planlægningsassistenten for at reservere ressourcer.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279221"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="99d2a-103">Oversigt over planlægningsassistent</span><span class="sxs-lookup"><span data-stu-id="99d2a-103">Schedule assistant overview</span></span>

<span data-ttu-id="99d2a-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="99d2a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="99d2a-105">Planlægningsassistent bruges til at reservere ressourcer på baggrund af de krav, der er defineret af projektlederen.</span><span class="sxs-lookup"><span data-stu-id="99d2a-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="99d2a-106">Planlægningsassistenten er afhængig af de parametre, der er angivet i ressourcekravet, for at finde ressourcen.</span><span class="sxs-lookup"><span data-stu-id="99d2a-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="99d2a-107">Planlægningsassistenten anbefaler ressourcer, der stemmer overens med de relevante krav, f.eks. tidsfrister eller færdigheder.</span><span class="sxs-lookup"><span data-stu-id="99d2a-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="99d2a-108">Når den identificerer passende ressourcer, kan Resource Manager eller projektlederen reservere ressourcen til arbejdet.</span><span class="sxs-lookup"><span data-stu-id="99d2a-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="99d2a-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="99d2a-109">Prerequisites</span></span>

<span data-ttu-id="99d2a-110">Planlægningsassistenten er en del af Universal Resource Scheduling-løsningen.</span><span class="sxs-lookup"><span data-stu-id="99d2a-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="99d2a-111">Denne løsning er inkluderet og installeres sammen med Dynamics 365 Project Operations, Dynamics 365 Field Service og Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="99d2a-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="99d2a-112">Matche krav og ressourcer</span><span class="sxs-lookup"><span data-stu-id="99d2a-112">Matching requirements and resources</span></span>

<span data-ttu-id="99d2a-113">Et genereret ressourcekrav er baseret på detaljer som f.eks.:</span><span class="sxs-lookup"><span data-stu-id="99d2a-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="99d2a-114">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="99d2a-114">Characteristics</span></span>
-   <span data-ttu-id="99d2a-115">Roller</span><span class="sxs-lookup"><span data-stu-id="99d2a-115">Roles</span></span>
-   <span data-ttu-id="99d2a-116">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="99d2a-116">Business units</span></span>
-   <span data-ttu-id="99d2a-117">Ressourcepræferencer</span><span class="sxs-lookup"><span data-stu-id="99d2a-117">Resource preferences</span></span>
-   <span data-ttu-id="99d2a-118">Indsatsprofiler</span><span class="sxs-lookup"><span data-stu-id="99d2a-118">Effort contours</span></span>
-   <span data-ttu-id="99d2a-119">Tidszone</span><span class="sxs-lookup"><span data-stu-id="99d2a-119">Time zone</span></span>

<span data-ttu-id="99d2a-120">I planlægningsassistenten bruges disse detaljer til at filtrere ressourcer.</span><span class="sxs-lookup"><span data-stu-id="99d2a-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="99d2a-121">Start planlægningsassistenten</span><span class="sxs-lookup"><span data-stu-id="99d2a-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="99d2a-122">Planlægningsassistent kan startes på to måder.</span><span class="sxs-lookup"><span data-stu-id="99d2a-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="99d2a-123">Hvis du bruger hybridtilstanden, kan du vælge et teammedlem med et ikke-opfyldt ressourcekrav i teammedlemsgitteret og derefter vælge **Reserver**.</span><span class="sxs-lookup"><span data-stu-id="99d2a-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="99d2a-124">Hvis du bruger den centrale tilstand, finder og vælger Resource Manageren ressourcen.</span><span class="sxs-lookup"><span data-stu-id="99d2a-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="99d2a-125">Planlægningsassistentfiltre</span><span class="sxs-lookup"><span data-stu-id="99d2a-125">Schedule assistant filters</span></span>

<span data-ttu-id="99d2a-126">Når planlægningsassistenten kører, vises detaljerne fra ressourcekravet som filtrerede værdier i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="99d2a-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="99d2a-127">Resource Manageren eller projektlederen kan finjustere resultaterne ved at justere filtrene, så de opfylder planlægningsbehovene.</span><span class="sxs-lookup"><span data-stu-id="99d2a-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="99d2a-128">I filtreringsruden vises de arbejdsrelaterede indstillinger, herunder:</span><span class="sxs-lookup"><span data-stu-id="99d2a-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="99d2a-129">Arbejdets start og afslutning</span><span class="sxs-lookup"><span data-stu-id="99d2a-129">Work start and end</span></span>
-   <span data-ttu-id="99d2a-130">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="99d2a-130">Characteristics</span></span>
-   <span data-ttu-id="99d2a-131">Roller</span><span class="sxs-lookup"><span data-stu-id="99d2a-131">Roles</span></span>
-   <span data-ttu-id="99d2a-132">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="99d2a-132">Organizational units</span></span>
-   <span data-ttu-id="99d2a-133">Ressourcevirksomhed</span><span class="sxs-lookup"><span data-stu-id="99d2a-133">Resourcing company</span></span>
-   <span data-ttu-id="99d2a-134">Ressourcetyper</span><span class="sxs-lookup"><span data-stu-id="99d2a-134">Resource types</span></span>
-   <span data-ttu-id="99d2a-135">Foretrukne ressourcer</span><span class="sxs-lookup"><span data-stu-id="99d2a-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]