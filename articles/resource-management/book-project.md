---
title: Reserver til et projekt
description: Dette emne indeholder oplysninger om, hvordan du reserverer en ressource til et projekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908019"
---
# <a name="book-to-a-project"></a><span data-ttu-id="e6586-103">Reserver til et projekt</span><span class="sxs-lookup"><span data-stu-id="e6586-103">Book to a project</span></span>

<span data-ttu-id="e6586-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="e6586-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e6586-105">Der er tidspunkter, hvor en projektleder eller Ressource Manager skal allokere en ressource til et projekt, uden at et bestemt krav er defineret af et generelt teammedlem.</span><span class="sxs-lookup"><span data-stu-id="e6586-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="e6586-106">Dette kan opnås på en af tre forskellige måder.</span><span class="sxs-lookup"><span data-stu-id="e6586-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="e6586-107">Reserver fra teammedlemsgitteret</span><span class="sxs-lookup"><span data-stu-id="e6586-107">Book from the team member grid</span></span>
- <span data-ttu-id="e6586-108">Reserver fra planlægningsområdet</span><span class="sxs-lookup"><span data-stu-id="e6586-108">Book from the schedule board</span></span>
- <span data-ttu-id="e6586-109">Reserver fra formularen **Projekt**</span><span class="sxs-lookup"><span data-stu-id="e6586-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="e6586-110">Reserver fra teammedlemsgitteret</span><span class="sxs-lookup"><span data-stu-id="e6586-110">Book from the team member grid</span></span>

<span data-ttu-id="e6586-111">Hvis din organisation arbejder i tilstanden hybrid ressourceallokering, kan den pågældende projektleder reservere en ressource direkte til projektet ved at benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="e6586-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="e6586-112">Gå til projektteammedlemsgitteret, og vælg **Ny** fra projektet.</span><span class="sxs-lookup"><span data-stu-id="e6586-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="e6586-113">Definer ressourcens stillingsnavn og rolle.</span><span class="sxs-lookup"><span data-stu-id="e6586-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="e6586-114">Vælg den reserverbare ressource i det tilgængelige opslag.</span><span class="sxs-lookup"><span data-stu-id="e6586-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="e6586-115">Når du har valgt ressourcen, skal du definere følgende feltoplysninger for at reservere ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e6586-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="e6586-116">Startdato</span><span class="sxs-lookup"><span data-stu-id="e6586-116">Start date</span></span>
    - <span data-ttu-id="e6586-117">Slutdato</span><span class="sxs-lookup"><span data-stu-id="e6586-117">Finish date</span></span>
    - <span data-ttu-id="e6586-118">Allokeringsmetode</span><span class="sxs-lookup"><span data-stu-id="e6586-118">Allocation method</span></span>
    - <span data-ttu-id="e6586-119">Timer, hvis det er relevant</span><span class="sxs-lookup"><span data-stu-id="e6586-119">Hours, if applicable</span></span>
    - <span data-ttu-id="e6586-120">Projektgodkender</span><span class="sxs-lookup"><span data-stu-id="e6586-120">Project approver</span></span>

6. <span data-ttu-id="e6586-121">Vælg **Gem og luk**</span><span class="sxs-lookup"><span data-stu-id="e6586-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="e6586-122">Reserver fra planlægningsområdet</span><span class="sxs-lookup"><span data-stu-id="e6586-122">Book from the schedule board</span></span>

<span data-ttu-id="e6586-123">Når en Resource manager skal reservere en ressource direkte til et projekt, kan vedkommende bruge planlægningsområdet og projektkravet.</span><span class="sxs-lookup"><span data-stu-id="e6586-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="e6586-124">Projektkravet er et ressourcekrav, der altid kan konteres imod.</span><span class="sxs-lookup"><span data-stu-id="e6586-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="e6586-125">For at reservere direkte i en projektformular fra planlægningsområdet skal du fuldføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="e6586-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="e6586-126">Naviger til planlægningsområdet, og filtrer på den venstre side de ressourcer, som du overvejer til kravet.</span><span class="sxs-lookup"><span data-stu-id="e6586-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="e6586-127">I nederste rude skal du vælge fanen **Projekt** for at få vist en liste over projektkrav.</span><span class="sxs-lookup"><span data-stu-id="e6586-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="e6586-128">Træk kravet til en ressource, og angiv følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="e6586-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="e6586-129">Startdato</span><span class="sxs-lookup"><span data-stu-id="e6586-129">Start date</span></span>
    - <span data-ttu-id="e6586-130">Slutdato</span><span class="sxs-lookup"><span data-stu-id="e6586-130">Finish date</span></span>
    - <span data-ttu-id="e6586-131">Reservationsstatus</span><span class="sxs-lookup"><span data-stu-id="e6586-131">Booking status</span></span>
    - <span data-ttu-id="e6586-132">Reservationsmetode</span><span class="sxs-lookup"><span data-stu-id="e6586-132">Booking method</span></span>
    - <span data-ttu-id="e6586-133">Varighed</span><span class="sxs-lookup"><span data-stu-id="e6586-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="e6586-134">Reserver fra projektformularen</span><span class="sxs-lookup"><span data-stu-id="e6586-134">Book from the Project form</span></span>

<span data-ttu-id="e6586-135">Som projektleder kan du få brug for at reservere en ressource til et projekt, men kender kun kriterierne i stedet for navnet på ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e6586-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="e6586-136">Benyt følgende fremgangsmåde for at bruge planlægningsassistenten til at finde en ressource, der er baseret på alle tilgængelige attributter for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e6586-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="e6586-137">Naviger til projektet, og vælg **Reserver** for at åbne planlægningsassistenten.</span><span class="sxs-lookup"><span data-stu-id="e6586-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="e6586-138">Ved hjælp af filtrene i venstre side af planlægningsassistenten skal du indskrænke kriterierne og vælge **Søg**.</span><span class="sxs-lookup"><span data-stu-id="e6586-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="e6586-139">Du kan reservere en ressource på baggrund af de ressourcer, der returneres i resultaterne.</span><span class="sxs-lookup"><span data-stu-id="e6586-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="e6586-140">Denne metode opretter ikke reservationer for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e6586-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="e6586-141">Den tilføjer i stedet ressourcen til teamet.</span><span class="sxs-lookup"><span data-stu-id="e6586-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="e6586-142">Når teammedlemmet er blevet tilføjet til projektet, kan projektlederen bruge det til at fastholde reservationer eller forlænge reservationer for at tilføje de nødvendige reservationer til ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e6586-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
