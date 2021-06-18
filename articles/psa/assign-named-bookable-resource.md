---
title: Reservere navngivne reserverbare ressourcer til et projektteam og tildele opgaver
description: Dette emne indeholder oplysninger om, hvordan du reserverer navngivne ressourcer til projektteams og tildeler dem til opgaver.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009339"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="b1ead-103">Reservere navngivne reserverbare ressourcer til et projektteam og tildele opgaver</span><span class="sxs-lookup"><span data-stu-id="b1ead-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b1ead-104">Du kan føje en navngivet ressource til projektteamet ved at reservere den direkte for teamet.</span><span class="sxs-lookup"><span data-stu-id="b1ead-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="b1ead-105">Det kan du gøre ved at benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="b1ead-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="b1ead-106">Gå til **Projekter** i Project Service Automation, og vælg det åbne projekt, du skal reservere for.</span><span class="sxs-lookup"><span data-stu-id="b1ead-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="b1ead-107">Klik på **Ny** under fanen **Team** på siden **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b1ead-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Tilføjelse af et teammedlem fra fanen Team](media/RM-how-to-1.png)

3. <span data-ttu-id="b1ead-109">Vælg den reserverbare ressource i dialogboksen **Hurtig oprettelse af projektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="b1ead-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="b1ead-110">Feltet **Rolle** udfyldes med ressourcens standardrolle, hvis der er tildelt en sådan.</span><span class="sxs-lookup"><span data-stu-id="b1ead-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="b1ead-111">Du kan ændre rollen, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="b1ead-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="b1ead-112">Vælg den fra- og til-dato, som ressourcen skal bruge, og vælg derefter fordelingsmetoden for ressourcens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="b1ead-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="b1ead-113">Hvis teammedlemmet skal være projektgodkender, skal du vælge **Ja** i feltet **Projektgodkender**.</span><span class="sxs-lookup"><span data-stu-id="b1ead-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="b1ead-114">Det betyder, at teammedlemmet kan godkende indsendte tids- og udgiftsposter for dette projekt.</span><span class="sxs-lookup"><span data-stu-id="b1ead-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="b1ead-115">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b1ead-115">Click **Save**.</span></span>

![Tilføje et teammedlem i formularen Hurtig oprettelse](media/RM-how-to-2.png)


<span data-ttu-id="b1ead-117">Du kan nu tildele den reserverede ressource opgaver på projektet.</span><span class="sxs-lookup"><span data-stu-id="b1ead-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="b1ead-118">Klik på fanen **Planlæg** på siden **Projekt** for at tildele den nye ressource opgaver.</span><span class="sxs-lookup"><span data-stu-id="b1ead-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="b1ead-119">Den ressourcevælger, der åbnes i feltet **Ressourcer** i opgavegitteret, viser de teammedlemmer, du kan vælge.</span><span class="sxs-lookup"><span data-stu-id="b1ead-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Tildeling af en opgave for et teammedlem under fanen Planlæg](media/RM-how-to-3.png)

<span data-ttu-id="b1ead-121">I version 3 til Project Service Automation (PSA) er ressourcereservationer og opgavetildelinger ikke tæt sammenkoblet.</span><span class="sxs-lookup"><span data-stu-id="b1ead-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="b1ead-122">Det betyder, at når du bruger ressourcevælgeren i tidsplanen, kan du tildele teammedlemmer opgaver for flere timer, end deres reservationer dækker på projektet.</span><span class="sxs-lookup"><span data-stu-id="b1ead-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="b1ead-123">Du kan se forskellene mellem teammedlemmernes reservationer og tildelinger under fanen **Team** eller under fanen **Ressourceafstemning**. Du kan også afstemme forskellene mellem reservationer og tildelinger for ressourcer på et mere detaljeret niveau.</span><span class="sxs-lookup"><span data-stu-id="b1ead-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Fanen Ressourceafstemning](media/RM-how-to-4.png)

<span data-ttu-id="b1ead-125">Du kan også bruge ressource vælgeren under fanen **Planlæg** til at søge efter og vælge de reserverbare ressourcer, der ikke allerede er en del af projektteamet.</span><span class="sxs-lookup"><span data-stu-id="b1ead-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="b1ead-126">Disse vises i ressourcevælgeren som **Andre ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="b1ead-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Tildeling af en opgave for en ressource, der ikke er medlem af et team](media/RM-how-to-5.png)

<span data-ttu-id="b1ead-128">Når du gør dette, føjes ressourcen til projektteamet og tildeles opgaven, men der oprettes ikke nogen reservationer.</span><span class="sxs-lookup"><span data-stu-id="b1ead-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Teammedlemmer med tildelinger uden reservationer](media/RM-how-to-6.png)

<span data-ttu-id="b1ead-130">Du kan bruge fanen **Afstemning** til at udvide reservationsfunktionen eller **Planlægningsområde** til at reservere ressourcens kapacitet til projektet.</span><span class="sxs-lookup"><span data-stu-id="b1ead-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Udvide reservationer for et teammedlem under fanen Ressourceafstemning](media/RM-how-to-7.png)

<span data-ttu-id="b1ead-132">Når et teammedlem er reserveret på projektet, kan du bruge vedligeholdelse af reservationer eller planlægningsområdet til direkte at administrere deres reservationer.</span><span class="sxs-lookup"><span data-stu-id="b1ead-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]