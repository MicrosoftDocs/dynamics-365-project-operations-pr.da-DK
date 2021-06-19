---
title: Omsætningsestimat for projekter med fast pris
description: Dette emne indeholder oplysninger om fastprisomsætning i projekter.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013794"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="6f01a-103">Omsætningsestimat for projekter med fast pris</span><span class="sxs-lookup"><span data-stu-id="6f01a-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="6f01a-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="6f01a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6f01a-105">Når du opretter en projektkontraktlinje med følgende attributter i Dynamics 365 Project Operations på Microsoft Dataverse, opretter systemet automatisk et projekt for estimering af fastprisomsætning.</span><span class="sxs-lookup"><span data-stu-id="6f01a-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="6f01a-106">Oplysningerne i dette projekt er baseret på følgende:</span><span class="sxs-lookup"><span data-stu-id="6f01a-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="6f01a-107">En faktureringsmetode med fast pris.</span><span class="sxs-lookup"><span data-stu-id="6f01a-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="6f01a-108">Et tilknyttet projekt.</span><span class="sxs-lookup"><span data-stu-id="6f01a-108">An associated project.</span></span>
  - <span data-ttu-id="6f01a-109">Mindst én milepæl, der er angivet under fanen **Fakturaplan** på siden **Projektkontraktlinje**.</span><span class="sxs-lookup"><span data-stu-id="6f01a-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="6f01a-110">Gennemse projekter med fastprisomsætningsestimater</span><span class="sxs-lookup"><span data-stu-id="6f01a-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="6f01a-111">Hvis du vil have vist estimater for omsætning i fastprisprojekter, skal du udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="6f01a-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="6f01a-112">I Dynamics 365 Finance-miljøet skal du gå til **Projektstyring og regnskab** > **Projekter** > **Estimater for omsætning i fastprisprojekter**.</span><span class="sxs-lookup"><span data-stu-id="6f01a-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="6f01a-113">Vælg det projekt, du vil have vist, og dobbeltklik på det **Estimerede projekt-id** for at åbne posten, og gennemse detaljerne for projektet.</span><span class="sxs-lookup"><span data-stu-id="6f01a-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="6f01a-114">Udvid fanen **Projekt**. Der vises ét projekt i gitteret for **Valgte projekter**.</span><span class="sxs-lookup"><span data-stu-id="6f01a-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="6f01a-115">Systemet bruger dette som standardprojekt, da det er det projekt, der er knyttet til projektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="6f01a-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="6f01a-116">Hvis du vil ændre tilknytningen, skal du vælge flere projekter og føje dem til gitteret **Valgte projekter**.</span><span class="sxs-lookup"><span data-stu-id="6f01a-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="6f01a-117">Hvis der er valgt flere projekter i dette gitter, beregnes de færdiggørelsesgraden og omsætningsestimater for projektet sammen for alle de valgte projekter.</span><span class="sxs-lookup"><span data-stu-id="6f01a-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="6f01a-118">Projektomkostninger, omsætningsprofil, omkostningsskabelon og periodekode kan angives manuelt.</span><span class="sxs-lookup"><span data-stu-id="6f01a-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="6f01a-119">Hvis de ikke angives manuelt, anvendes standardværdierne under beregning af første estimat for projektet ved hjælp af de regler, der er konfigureret for projektomkostnings- og omsætningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="6f01a-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]