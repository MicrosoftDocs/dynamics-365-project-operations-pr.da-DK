---
title: Opret et projekt
description: Sådan opretter du et projekt i Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074184"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="f0e5f-103">Oprette et projekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f0e5f-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f0e5f-104">Opret et projekt med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funktioner i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], når du vil oprette en salgsmulighed, et tilbud eller en kontrakt for projektbaserede servicer.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="f0e5f-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funktionerne hjælper dig med at administrere dit projekt fra salgsmulighed til færdiggørelse.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="f0e5f-106">Når du opretter et projekt, skal du også oprette et arbejdsopgavehierarki, som påvirker dine tilbud, omkostningsestimater og ressourcestyring.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="f0e5f-107">Gå til **Project Service > Projekter**.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="f0e5f-108">Klik på **Nyt projekt**.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="f0e5f-109">I området **Oversigt** skal du angive et navn til projektet og derefter udfylde så mange detaljer som muligt.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="f0e5f-110">Elementer, der skal udfyldes, er markeret med en rød stjerne (\*).</span><span class="sxs-lookup"><span data-stu-id="f0e5f-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="f0e5f-111">Klik på **Gem** for at oprette projektet, så du kan fortsætte med at redigere det.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="f0e5f-112">Derefter skal du oprette et arbejdsopgavehierarki for projektet for at definere de opgaver, timing og ressourceroller, der er nødvendige for projektet.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="f0e5f-113">Project Service Automation respekterer tidszonen for den anvendte skabelon for **Arbejdstid** i forbindelse med planlægningen.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="f0e5f-114">Når du får vist planlagte opgaver, vises start- og slutdatoerne for en opgave dog i brugerens tidszone.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="f0e5f-115">Dette gælder for andre tidsfaseinddelte visninger i formularen **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="f0e5f-116">Hvis brugerens tidszone ikke stemmer overens med tidszonen i den arbejdstidsskabelon, der er anvendt på projektet, vises der en advarsel, som forklarer forskellen.</span><span class="sxs-lookup"><span data-stu-id="f0e5f-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="f0e5f-117">Se også</span><span class="sxs-lookup"><span data-stu-id="f0e5f-117">See Also</span></span>  
 [<span data-ttu-id="f0e5f-118">Vejledning til projektledere</span><span class="sxs-lookup"><span data-stu-id="f0e5f-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)