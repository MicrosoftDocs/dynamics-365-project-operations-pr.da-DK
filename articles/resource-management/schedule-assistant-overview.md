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
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125621"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="14cf6-103">Oversigt over planlægningsassistent</span><span class="sxs-lookup"><span data-stu-id="14cf6-103">Schedule assistant overview</span></span>

<span data-ttu-id="14cf6-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="14cf6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="14cf6-105">Planlægningsassistent bruges til at reservere ressourcer på baggrund af de krav, der er defineret af projektlederen.</span><span class="sxs-lookup"><span data-stu-id="14cf6-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="14cf6-106">Planlægningsassistenten er afhængig af de parametre, der er angivet i ressourcekravet, for at finde ressourcen.</span><span class="sxs-lookup"><span data-stu-id="14cf6-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="14cf6-107">Planlægningsassistenten anbefaler ressourcer, der stemmer overens med de relevante krav, f.eks. tidsfrister eller færdigheder.</span><span class="sxs-lookup"><span data-stu-id="14cf6-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="14cf6-108">Når den identificerer passende ressourcer, kan Resource Manager eller projektlederen reservere ressourcen til arbejdet.</span><span class="sxs-lookup"><span data-stu-id="14cf6-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="14cf6-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="14cf6-109">Prerequisites</span></span>

<span data-ttu-id="14cf6-110">Planlægningsassistenten er en del af Universal Resource Scheduling-løsningen.</span><span class="sxs-lookup"><span data-stu-id="14cf6-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="14cf6-111">Denne løsning er inkluderet og installeret sammen med Dynamics 365 Project Operations, Dynamics 365 Field Service og Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="14cf6-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="14cf6-112">Matche krav og ressourcer</span><span class="sxs-lookup"><span data-stu-id="14cf6-112">Matching requirements and resources</span></span>

<span data-ttu-id="14cf6-113">Et genereret ressourcekrav er baseret på detaljer som f.eks.:</span><span class="sxs-lookup"><span data-stu-id="14cf6-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="14cf6-114">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="14cf6-114">Characteristics</span></span>
-   <span data-ttu-id="14cf6-115">Roller</span><span class="sxs-lookup"><span data-stu-id="14cf6-115">Roles</span></span>
-   <span data-ttu-id="14cf6-116">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="14cf6-116">Business units</span></span>
-   <span data-ttu-id="14cf6-117">Ressourcepræferencer</span><span class="sxs-lookup"><span data-stu-id="14cf6-117">Resource preferences</span></span>
-   <span data-ttu-id="14cf6-118">Indsatsprofiler</span><span class="sxs-lookup"><span data-stu-id="14cf6-118">Effort contours</span></span>
-   <span data-ttu-id="14cf6-119">Tidszone</span><span class="sxs-lookup"><span data-stu-id="14cf6-119">Time zone</span></span>

<span data-ttu-id="14cf6-120">I planlægningsassistenten bruges disse detaljer til at filtrere ressourcer.</span><span class="sxs-lookup"><span data-stu-id="14cf6-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="14cf6-121">Start planlægningsassistenten</span><span class="sxs-lookup"><span data-stu-id="14cf6-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="14cf6-122">Planlægningsassistent kan startes på to måder.</span><span class="sxs-lookup"><span data-stu-id="14cf6-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="14cf6-123">Hvis du bruger hybridtilstanden, kan du vælge et teammedlem med et ikke-opfyldt ressourcekrav i teammedlemsgitteret og derefter vælge **Reserver**.</span><span class="sxs-lookup"><span data-stu-id="14cf6-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="14cf6-124">Hvis du bruger den centrale tilstand, finder og vælger Resource Manageren ressourcen.</span><span class="sxs-lookup"><span data-stu-id="14cf6-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="14cf6-125">Planlægningsassistentfiltre</span><span class="sxs-lookup"><span data-stu-id="14cf6-125">Schedule assistant filters</span></span>

<span data-ttu-id="14cf6-126">Når planlægningsassistenten kører, vises detaljerne fra ressourcekravet som filtrerede værdier i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="14cf6-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="14cf6-127">Resource Manageren eller projektlederen kan finjustere resultaterne ved at justere filtrene, så de opfylder planlægningsbehovene.</span><span class="sxs-lookup"><span data-stu-id="14cf6-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="14cf6-128">I filtreringsruden vises de arbejdsrelaterede indstillinger, herunder:</span><span class="sxs-lookup"><span data-stu-id="14cf6-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="14cf6-129">Arbejdets start og afslutning</span><span class="sxs-lookup"><span data-stu-id="14cf6-129">Work start and end</span></span>
-   <span data-ttu-id="14cf6-130">Egenskaber</span><span class="sxs-lookup"><span data-stu-id="14cf6-130">Characteristics</span></span>
-   <span data-ttu-id="14cf6-131">Roller</span><span class="sxs-lookup"><span data-stu-id="14cf6-131">Roles</span></span>
-   <span data-ttu-id="14cf6-132">Afdelinger</span><span class="sxs-lookup"><span data-stu-id="14cf6-132">Organizational units</span></span>
-   <span data-ttu-id="14cf6-133">Ressourcevirksomhed</span><span class="sxs-lookup"><span data-stu-id="14cf6-133">Resourcing company</span></span>
-   <span data-ttu-id="14cf6-134">Ressourcetyper</span><span class="sxs-lookup"><span data-stu-id="14cf6-134">Resource types</span></span>
-   <span data-ttu-id="14cf6-135">Foretrukne ressourcer</span><span class="sxs-lookup"><span data-stu-id="14cf6-135">Preferred resources</span></span>
