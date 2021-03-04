---
title: Spore et projekts status
description: Sådan sporer du et projekts status i Project Service
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
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149581"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="321c3-103">Spore et projekts status (Project Service)</span><span class="sxs-lookup"><span data-stu-id="321c3-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="321c3-104">Brug [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] til at spore status for en klients projekt.</span><span class="sxs-lookup"><span data-stu-id="321c3-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="321c3-105">Som engagementet skrider frem, opdateres projektets faser, så de afspejler fasen i engagementet:</span><span class="sxs-lookup"><span data-stu-id="321c3-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="321c3-106">**Ny**</span><span class="sxs-lookup"><span data-stu-id="321c3-106">**New**</span></span>    | <span data-ttu-id="321c3-107">Når du opretter et projekt, indstilles fasen til **Ny**.</span><span class="sxs-lookup"><span data-stu-id="321c3-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="321c3-108">Hvis du har oprettet projektet fra en skabelon, kan projektet i denne fase have en tidsplan, estimater og teamdata.</span><span class="sxs-lookup"><span data-stu-id="321c3-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="321c3-109">Ellers vil det være projektets disposition, og du skal manuelt angive resten af projektkomponenterne.</span><span class="sxs-lookup"><span data-stu-id="321c3-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="321c3-110">**Tilbud**</span><span class="sxs-lookup"><span data-stu-id="321c3-110">**Quote**</span></span>   |      <span data-ttu-id="321c3-111">Når du knytter et projekt til et tilbud eller opretter det fra et tilbud, angives projektfasen til **Tilbud**, og de forventede start- og slutdatoer opdateres også.</span><span class="sxs-lookup"><span data-stu-id="321c3-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="321c3-112">Når projektet er i fasen tilbud, vises oplysninger om tilbuddet under fanen **Salg** på siden **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="321c3-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="321c3-113">**Planlæg**</span><span class="sxs-lookup"><span data-stu-id="321c3-113">**Plan**</span></span>   |                                     <span data-ttu-id="321c3-114">Når du vinder et tilbud, der er knyttet til et projekt, og når engagementet går videre til kontraktfasen, opdateres projektfasen til **Plan**.</span><span class="sxs-lookup"><span data-stu-id="321c3-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="321c3-115">Kontraktoplysninger vises under fanen **Salg** på siden **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="321c3-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="321c3-116">**Fuldført**</span><span class="sxs-lookup"><span data-stu-id="321c3-116">**Complete**</span></span> |                    <span data-ttu-id="321c3-117">Når projektarbejdet er fuldført, kan du vende fasen til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="321c3-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="321c3-118">Når projektfasen er angivet til Fuldført, er det underforstået, at arbejdet er 100 % færdigt, men at projektet holdes åbent for alle ventende tids- eller udgiftsposteringer, der skal registreres.</span><span class="sxs-lookup"><span data-stu-id="321c3-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="321c3-119">**Luk**</span><span class="sxs-lookup"><span data-stu-id="321c3-119">**Close**</span></span>   |           <span data-ttu-id="321c3-120">Når alle transaktioner er blevet registreret på projektet, og du ikke forventer at logge mere, kan du manuelt indstille fasen til **Luk**.</span><span class="sxs-lookup"><span data-stu-id="321c3-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="321c3-121">Når projektet er indstillet til **Luk**, kan du ikke logge flere posteringer på projektet, og projektet vil være skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="321c3-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="321c3-122">Sådan spores et projekts status</span><span class="sxs-lookup"><span data-stu-id="321c3-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="321c3-123">Gå til **Project Service > Projekter**.</span><span class="sxs-lookup"><span data-stu-id="321c3-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="321c3-124">Klik på det projekt, som du vil arbejde på.</span><span class="sxs-lookup"><span data-stu-id="321c3-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="321c3-125">Vælg pil ned ud for projektnavnet på linjen øverst på skærmen, og klik derefter på **Projektsporing**.</span><span class="sxs-lookup"><span data-stu-id="321c3-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="321c3-126">Vælg **Indsatssporing** eller **Omkostningssporing** på rullelisten over opgavelisten.</span><span class="sxs-lookup"><span data-stu-id="321c3-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="321c3-127">Dobbeltklik på en opgave for at redigere den.</span><span class="sxs-lookup"><span data-stu-id="321c3-127">Double-click any task to edit it.</span></span> <span data-ttu-id="321c3-128">Du kan også flytte eller tilpasse størrelsen på søjlerne i Gantt-diagrammet for at ændre klokkeslæt og status for en opgave.</span><span class="sxs-lookup"><span data-stu-id="321c3-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="321c3-129">Se også</span><span class="sxs-lookup"><span data-stu-id="321c3-129">See Also</span></span>  
 [<span data-ttu-id="321c3-130">Vejledning til projektledere</span><span class="sxs-lookup"><span data-stu-id="321c3-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
