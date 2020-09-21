---
title: Spore et projekts status
description: Sådan sporer du et projekts status i Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750616"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="b3d8f-103">Spore et projekts status (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b3d8f-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b3d8f-104">Brug [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] til at spore status for en klients projekt.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="b3d8f-105">Som engagementet skrider frem, opdateres projektets faser, så de afspejler fasen i engagementet:</span><span class="sxs-lookup"><span data-stu-id="b3d8f-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="b3d8f-106">**Ny**</span><span class="sxs-lookup"><span data-stu-id="b3d8f-106">**New**</span></span>    | <span data-ttu-id="b3d8f-107">Når du opretter et projekt, indstilles fasen til **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="b3d8f-108">Hvis du har oprettet projektet fra en skabelon, kan projektet i denne fase have en tidsplan, estimater og teamdata.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="b3d8f-109">Ellers vil det være projektets disposition, og du skal manuelt angive resten af projektkomponenterne.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="b3d8f-110">**Tilbud**</span><span class="sxs-lookup"><span data-stu-id="b3d8f-110">**Quote**</span></span>   |      <span data-ttu-id="b3d8f-111">Når du knytter et projekt til et tilbud eller opretter det fra et tilbud, angives projektfasen til **Tilbud**, og de forventede start- og slutdatoer opdateres også.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="b3d8f-112">Når projektet er i fasen tilbud, vises oplysninger om tilbuddet under fanen **Salg** på siden **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="b3d8f-113">**Planlæg**</span><span class="sxs-lookup"><span data-stu-id="b3d8f-113">**Plan**</span></span>   |                                     <span data-ttu-id="b3d8f-114">Når du vinder et tilbud, der er knyttet til et projekt, og når engagementet går videre til kontraktfasen, opdateres projektfasen til **Plan**.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="b3d8f-115">Kontraktoplysninger vises under fanen **Salg** på siden **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="b3d8f-116">**Fuldført**</span><span class="sxs-lookup"><span data-stu-id="b3d8f-116">**Complete**</span></span> |                    <span data-ttu-id="b3d8f-117">Når projektarbejdet er fuldført, kan du vende fasen til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="b3d8f-118">Når projektfasen er angivet til Fuldført, er det underforstået, at arbejdet er 100 % færdigt, men at projektet holdes åbent for alle ventende tids- eller udgiftsposteringer, der skal registreres.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="b3d8f-119">**Luk**</span><span class="sxs-lookup"><span data-stu-id="b3d8f-119">**Close**</span></span>   |           <span data-ttu-id="b3d8f-120">Når alle transaktioner er blevet registreret på projektet, og du ikke forventer at logge mere, kan du manuelt indstille fasen til **Luk**.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="b3d8f-121">Når projektet er indstillet til **Luk**, kan du ikke logge flere posteringer på projektet, og projektet vil være skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="b3d8f-122">Sådan spores et projekts status</span><span class="sxs-lookup"><span data-stu-id="b3d8f-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="b3d8f-123">Gå til **Project Service > Projekter**.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="b3d8f-124">Klik på det projekt, som du vil arbejde på.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="b3d8f-125">Vælg pil ned ud for projektnavnet på linjen øverst på skærmen, og klik derefter på **Projektsporing**.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="b3d8f-126">Vælg **Indsatssporing** eller **Omkostningssporing** på rullelisten over opgavelisten.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="b3d8f-127">Dobbeltklik på en opgave for at redigere den.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-127">Double-click any task to edit it.</span></span> <span data-ttu-id="b3d8f-128">Du kan også flytte eller tilpasse størrelsen på søjlerne i Gantt-diagrammet for at ændre klokkeslæt og status for en opgave.</span><span class="sxs-lookup"><span data-stu-id="b3d8f-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="b3d8f-129">Se også</span><span class="sxs-lookup"><span data-stu-id="b3d8f-129">See Also</span></span>  
 [<span data-ttu-id="b3d8f-130">Vejledning til projektledere</span><span class="sxs-lookup"><span data-stu-id="b3d8f-130">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
