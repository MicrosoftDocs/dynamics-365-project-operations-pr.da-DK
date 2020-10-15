---
title: Bevar projektteamets medlemmer
description: Denne emne indeholder oplysninger om reservation af navngivne ressourcer til projektteam og deres tildeling af opgaver.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961841"
---
# <a name="maintain-team-members"></a><span data-ttu-id="0bf23-103">Bevar projektteamets medlemmer</span><span class="sxs-lookup"><span data-stu-id="0bf23-103">Maintain team members</span></span>

<span data-ttu-id="0bf23-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0bf23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0bf23-105">Du kan tilføje en navngivet ressource til projektteamet ved at reservere den direkte til teamet.</span><span class="sxs-lookup"><span data-stu-id="0bf23-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="0bf23-106">Gå til **Projekter** i Dynamics 365 Project Operations, og vælg det åbne projekt, du skal reservere for.</span><span class="sxs-lookup"><span data-stu-id="0bf23-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="0bf23-107">På siden **Projekt** skal du på fanen **Team** vælge **Nyt**.</span><span class="sxs-lookup"><span data-stu-id="0bf23-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="0bf23-108">Vælg den reserverbare ressource i dialogboksen **Hurtig oprettelse af projektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="0bf23-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="0bf23-109">Feltet **Rolle** udfyldes med ressourcens standardrolle, hvis der er tildelt en sådan.</span><span class="sxs-lookup"><span data-stu-id="0bf23-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="0bf23-110">Du kan ændre rollen.</span><span class="sxs-lookup"><span data-stu-id="0bf23-110">You can change the role.</span></span> 
4. <span data-ttu-id="0bf23-111">Vælg den fra- og til-dato, som ressourcen skal bruge, og vælg derefter fordelingsmetoden for ressourcens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="0bf23-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="0bf23-112">I feltet **Projektgodkender** skal du vælge **Ja**, hvis teammedlemmet skal være projektgodkender.</span><span class="sxs-lookup"><span data-stu-id="0bf23-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="0bf23-113">Teammedlemmet kan godkende indsendte tids- og udgiftsregistreringer for dette projekt.</span><span class="sxs-lookup"><span data-stu-id="0bf23-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="0bf23-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0bf23-114">Select **Save**.</span></span>

<span data-ttu-id="0bf23-115">Du kan nu tildele den reserverede ressource opgaver på projektet.</span><span class="sxs-lookup"><span data-stu-id="0bf23-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="0bf23-116">På siden **Projekt** skal du på fanen **Planlæg** tildele opgaver til den nye ressource.</span><span class="sxs-lookup"><span data-stu-id="0bf23-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="0bf23-117">Den ressourcevælger, der åbnes i feltet **Ressourcer** i opgavegitteret, viser de teammedlemmer, du kan vælge.</span><span class="sxs-lookup"><span data-stu-id="0bf23-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="0bf23-118">I Project Operations er ressourcereservationer og opgavetildelinger ikke tæt sammenkoblet.</span><span class="sxs-lookup"><span data-stu-id="0bf23-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="0bf23-119">Når du bruger ressourcevælgeren i tidsplanen, kan du tildele teammedlemmer opgaver for flere timer, end deres reservationer dækker på projektet.</span><span class="sxs-lookup"><span data-stu-id="0bf23-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="0bf23-120">Forskellene mellem teammedlemmers reservationer og tildelinger vises under fanerne **Team** og **Ressourceafstemning**.</span><span class="sxs-lookup"><span data-stu-id="0bf23-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="0bf23-121">Du kan også afstemme forskellene mellem reservationer og tildelinger for ressourcer på et mere detaljeret niveau.</span><span class="sxs-lookup"><span data-stu-id="0bf23-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="0bf23-122">Anvend ressourcevælgeren under fanen **Planlæg** til at søge efter og vælge de reserverbare ressourcer, der ikke allerede er en del af projektteamet.</span><span class="sxs-lookup"><span data-stu-id="0bf23-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="0bf23-123">Disse ressourcer vises i ressourcevælgeren som **Andre ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="0bf23-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="0bf23-124">Når du foretager et valg, tilføjes ressourcen til projektteamet og tildeles opgaven, men der oprettes ikke nogen reservationer.</span><span class="sxs-lookup"><span data-stu-id="0bf23-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="0bf23-125">Du kan bruge fanen **Afstemning** til at udvide reservationsfunktionen eller **Planlægningsområde** til at reservere ressourcens kapacitet til projektet.</span><span class="sxs-lookup"><span data-stu-id="0bf23-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="0bf23-126">Når et teammedlem er reserveret på projektet, kan du bruge **Bevar reservationer** eller **Planlægningsområdet** til direkte at administrere deres reservationer.</span><span class="sxs-lookup"><span data-stu-id="0bf23-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
