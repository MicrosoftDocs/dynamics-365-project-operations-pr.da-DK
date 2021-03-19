---
title: Levere arbejdsestimater for et projekt under salgsprocessen
description: Sådan leverer du arbejdsestimater for et projekt under salgsprocessen i Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283541"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="3780e-103">Levere arbejdsestimater for et projekt under salgsprocessen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3780e-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3780e-104">Under salgsprocessen kan du udarbejde salgsestimater fra bunden med tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="3780e-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="3780e-105">-funktioner i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] giver en mere videnskabelig og fremsynet måde at fremsætte salgsestimater på ved at opdele arbejdselementer og knytte de relevante attributter, der bidrager til estimater for projektet, til arbejdsopgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="3780e-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="3780e-106">Når du har vundet salget, kan du bruge det tilknyttede arbejdsopgavehierarki i projektplanen og raffinere det efter dine behov til gennemførelse af projektet.</span><span class="sxs-lookup"><span data-stu-id="3780e-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="3780e-107">Sammenkæde et projekt med en tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="3780e-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="3780e-108">Når du opretter en projektbaseret tilbudslinje, kan du oprette et nyt projekt fra tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="3780e-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="3780e-109">Du kan derefter bruge projektskabeloner, der enten er forudkonfigurerede standardprojektplaner og økonomiske estimater, der er fælles for din organisation, eller en kopi af en projektplan og estimater fra et tidligere projekt.</span><span class="sxs-lookup"><span data-stu-id="3780e-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="3780e-110">Når du opretter et projekt, kan du vælge en projektskabelon for at få et grundlag for at tilpasse projektplanen, estimater og rollekrav.</span><span class="sxs-lookup"><span data-stu-id="3780e-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="3780e-111">Når projektet oprettes fra tilbuddet, knyttes det automatisk til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="3780e-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="3780e-112">Projektestimatkomponenter</span><span class="sxs-lookup"><span data-stu-id="3780e-112">Project estimate components</span></span>  
 <span data-ttu-id="3780e-113">Arbejdsopgavehierarkiet i et projekt er en måde at opdele arbejdet i opgaver, vedligeholde et hierarki af opgaver og tildele et estimat over den indsats, der kræves for at fuldføre hver opgave.</span><span class="sxs-lookup"><span data-stu-id="3780e-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="3780e-114">Du kan også knytte roller til en opgave for at angive en vurdering af den ressourcetype, der kræves for at fuldføre en opgave og en tidsplan.</span><span class="sxs-lookup"><span data-stu-id="3780e-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="3780e-115">Med arbejdsopgavehierarkiet kan du bestemme arbejdsindsats og planlægge estimater.</span><span class="sxs-lookup"><span data-stu-id="3780e-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="3780e-116">Som standard bruger projektet standardprislister, som du definerede tidligere.</span><span class="sxs-lookup"><span data-stu-id="3780e-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="3780e-117">De kost- og salgspriser, der er defineret i prislisterne, hjælper med at bestemme økonomiske estimater for projektets arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="3780e-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="3780e-118">Hvis dit projekt er knyttet til et tilbud, og tilbuddet har en anden prisliste end standardprislisten, bruges tilbuddets prisliste til økonomiske estimater.</span><span class="sxs-lookup"><span data-stu-id="3780e-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="3780e-119">Importere estimater fra et projekt til et tilbud</span><span class="sxs-lookup"><span data-stu-id="3780e-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="3780e-120">Når du har projektestimater i projektet, kan du importere disse estimater til tilbudslinjen:</span><span class="sxs-lookup"><span data-stu-id="3780e-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="3780e-121">I **Tilbudslinjedetaljer** skal du klikke på **Importér fra estimat**.</span><span class="sxs-lookup"><span data-stu-id="3780e-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="3780e-122">Vælg, om projektestimater, der er opsummeret efter transaktionstype, rolle eller nodeniveau for arbejdsopgavehierarki, skal importeres.</span><span class="sxs-lookup"><span data-stu-id="3780e-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3780e-123">Se også</span><span class="sxs-lookup"><span data-stu-id="3780e-123">See Also</span></span>  
 [<span data-ttu-id="3780e-124">Vejledning til projektledere</span><span class="sxs-lookup"><span data-stu-id="3780e-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]