---
title: Hvordan foretager jeg en "foreløbig reservation" af ressourcer i appversion 2.x?
description: I denne artikel beskrives, hvordan du midlertidigt kan reservere medlemmer af projektteamet med Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286016"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="55344-103">Hvordan foretager jeg en "foreløbig reservation" af ressourcer i webappen (Project Service-app v2.x)?</span><span class="sxs-lookup"><span data-stu-id="55344-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="55344-104">Du kan planlægge midlertidigt eller "foreløbigt reservere" en ressource til et projektteam for at vise, at du har planer om at tildele ressourcen til et projekt.</span><span class="sxs-lookup"><span data-stu-id="55344-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="55344-105">Foreløbige reservationer forbruger ikke en ressources ledig kapacitet.</span><span class="sxs-lookup"><span data-stu-id="55344-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="55344-106">Foreløbigt reserverede teammedlemmer kan ikke tildeles til projektopgaver.</span><span class="sxs-lookup"><span data-stu-id="55344-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="55344-107">Kun ressourcer med status Definitivt reserveret og bekræftelsestypen Bekræftet kan tildeles til opgaver (hvis de har tilstrækkelig mange definitivt reserverede timer at dække det tildelte arbejde).</span><span class="sxs-lookup"><span data-stu-id="55344-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="55344-108">Foreløbigt reserverede teammedlemmer vises i gitteret Teammedlem med deres foreløbige timer, der vises i kolonnen Reservér foreløbigt.</span><span class="sxs-lookup"><span data-stu-id="55344-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="55344-109">De vises også i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="55344-109">They also show up on the schedule board.</span></span> <span data-ttu-id="55344-110">Igen, de angiver ikke et forbrug af kapacitet, fordi foreløbige reservationer ikke forbruger en ressources kapacitet.</span><span class="sxs-lookup"><span data-stu-id="55344-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="55344-111">Der er tre måder at foretage en foreløbig reservation af et teammedlem på i et projekt med Project Service version 2.x.</span><span class="sxs-lookup"><span data-stu-id="55344-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="55344-112">Du kan reservere foreløbigt i planlægningsområdet ved at bruge funktionen Vedligehold reservationer eller ved at oprette en generisk ressource.</span><span class="sxs-lookup"><span data-stu-id="55344-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="55344-113">Disse metoder beskrives nedenfor.</span><span class="sxs-lookup"><span data-stu-id="55344-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="55344-114">Reserver foreløbigt med planlægningsområdet</span><span class="sxs-lookup"><span data-stu-id="55344-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="55344-115">Når du vil foretage en foreløbig reservation med planlægningsområdet, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="55344-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="55344-116">Åbn planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="55344-116">Open the schedule board.</span></span>
2. <span data-ttu-id="55344-117">Vælg fanen Projekt i panelet Krav til reservationer i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="55344-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="55344-118">Find det projekt, du vil foretage en foreløbige reservation af en ressource til.</span><span class="sxs-lookup"><span data-stu-id="55344-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="55344-119">Hvis du har mange projekter, skal du klikke på kolonneoverskriften Projekt og derefter bruge filteret til at finde dit projekt.</span><span class="sxs-lookup"><span data-stu-id="55344-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="55344-120">Klik på projektet, og træk det og slip det på ressourcens tidsgitter.</span><span class="sxs-lookup"><span data-stu-id="55344-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="55344-121">Derved åbnes panelet Opret ressourcereservation til højre.</span><span class="sxs-lookup"><span data-stu-id="55344-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="55344-122">Juster start-og slutdato, vælg reservationsstatus Foreløbig, og angiv timerne.</span><span class="sxs-lookup"><span data-stu-id="55344-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="55344-123">Klik på Reservér.</span><span class="sxs-lookup"><span data-stu-id="55344-123">Click Book.</span></span>
7. <span data-ttu-id="55344-124">Tilbage i projektet vises ressourcen nu som et teammedlem med de foreløbigt reserverede timer i kolonnen Reservér foreløbigt.</span><span class="sxs-lookup"><span data-stu-id="55344-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="55344-125">Bemærk, at du ikke kan tildele dem til opgaver i arbejdsopgavehierarki (WBS), fordi ressourcer skal komme reserveres definitivt i teamet for at blive tildelt.</span><span class="sxs-lookup"><span data-stu-id="55344-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="55344-126">Foretage en foreløbig reservation ved hjælp af funktionen Vedligeholde reservationer</span><span class="sxs-lookup"><span data-stu-id="55344-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="55344-127">Når du vil foretage en foreløbig reservation ved hjælp af Vedligehold reservationer, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="55344-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="55344-128">Klik på Ny fra teammedlemsgitteret.</span><span class="sxs-lookup"><span data-stu-id="55344-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="55344-129">Vælg den reserverbare ressource, rolle, fra/til.</span><span class="sxs-lookup"><span data-stu-id="55344-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="55344-130">Vælg en anden allokeringsmetode end Ingen:</span><span class="sxs-lookup"><span data-stu-id="55344-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="55344-131">Fuld kapacitet</span><span class="sxs-lookup"><span data-stu-id="55344-131">Full Capacity</span></span>
- <span data-ttu-id="55344-132">Kapacitet som procentdel</span><span class="sxs-lookup"><span data-stu-id="55344-132">Percentage Capacity</span></span>
- <span data-ttu-id="55344-133">Efter timer - jævn fordeling</span><span class="sxs-lookup"><span data-stu-id="55344-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="55344-134">Efter timer - flest timer først i perioden</span><span class="sxs-lookup"><span data-stu-id="55344-134">By Hours Front Load</span></span>
4. <span data-ttu-id="55344-135">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="55344-135">Click Save.</span></span> <span data-ttu-id="55344-136">Du kan se ressourcen i teamgitteret og vedkommendes timer, der er angivet som Definitiv.</span><span class="sxs-lookup"><span data-stu-id="55344-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="55344-137">Du kan vedligeholde ressourcens reservationer ved at klikke på Vedligehold reservationer.</span><span class="sxs-lookup"><span data-stu-id="55344-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="55344-138">Når planlægningsområdet åbnes, skal du udvide ressourcen for at få vist hans eller hendes reservationer.</span><span class="sxs-lookup"><span data-stu-id="55344-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="55344-139">Du kan se reservationen angivet som Definitiv.</span><span class="sxs-lookup"><span data-stu-id="55344-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="55344-140">Højreklik på reservationen, og vælg Reservér foreløbigt og derefter Foreløbigt under Skift status.</span><span class="sxs-lookup"><span data-stu-id="55344-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="55344-141">Status for reservation er nu Foreløbig.</span><span class="sxs-lookup"><span data-stu-id="55344-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="55344-142">Når du har lukket planlægningsområdet, kan du se, at timerne for ressourcen er ændret fra Definitiv til Foreløbig i teammedlemsgitteret.</span><span class="sxs-lookup"><span data-stu-id="55344-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="55344-143">Bemærk, at hvis du reserverer en ressource definitivt til teamet og derefter tildeler ressourcen opgaver i WBS, når du bruger Vedligehold reservationer til at ændre status fra Definitiv til Foreløbig, fjernes tildelingerne fra opgaver for den pågældende ressource, fordi kun definitivt reserverede ressourcer kan tildeles til opgaver.</span><span class="sxs-lookup"><span data-stu-id="55344-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="55344-144">Foretage en foreløbig reservation ved at oprette en generisk ressource</span><span class="sxs-lookup"><span data-stu-id="55344-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="55344-145">Du kan oprette en foreløbig reservation ved at oprette et generisk ressourceteammedlem, fuldføre via planlægningsområdet eller Anmodning om ressourcer og ændre typen under reservationen.</span><span class="sxs-lookup"><span data-stu-id="55344-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="55344-146">Det kan du gøre ved hjælp af følgende procedure:</span><span class="sxs-lookup"><span data-stu-id="55344-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="55344-147">Tildel roller i projektets WBS til de opgaver, du vil oprette generiske teammedlemmer for.</span><span class="sxs-lookup"><span data-stu-id="55344-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="55344-148">Klik på Opret projektteam.</span><span class="sxs-lookup"><span data-stu-id="55344-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="55344-149">Vælg den generiske ressource i projektteamets medlemsgitter, og klik på Reservér.</span><span class="sxs-lookup"><span data-stu-id="55344-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="55344-150">Vælg den ressource, som du vil reservere, i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="55344-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="55344-151">I panelet Opret ressourcereservation i planlægningsområdet skal du ændre reservationsstatus til Foreløbig.</span><span class="sxs-lookup"><span data-stu-id="55344-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="55344-152">Klik på Reservér eller Reservér og afslut.</span><span class="sxs-lookup"><span data-stu-id="55344-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="55344-153">Når du har lukket planlægningsområdet, kan du se den valgte ressource, der er føjet til teamet med Foreløbigt reserverede timer og tildelte timer.</span><span class="sxs-lookup"><span data-stu-id="55344-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="55344-154">Du kan også se, at den generiske ressource forbliver i teamet som et tegn på, at opgaverne er tilknyttet et foreløbigt reserveret teammedlem.</span><span class="sxs-lookup"><span data-stu-id="55344-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="55344-155">Når du er klar til at ændre en foreløbigt reserveret teammedlemsressource til et definitivt reserveret teammedlem, så du kan tildele ressourcen til opgaver, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="55344-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="55344-156">Vælg ressourcen, og klik på Vedligehold reservationer.</span><span class="sxs-lookup"><span data-stu-id="55344-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="55344-157">Når planlægningsområdet åbnes, skal du udvide ressourcen for at få vist hans eller hendes reservationer.</span><span class="sxs-lookup"><span data-stu-id="55344-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="55344-158">Du kan se reservationen markeret som Foreløbig.</span><span class="sxs-lookup"><span data-stu-id="55344-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="55344-159">Højreklik på reservationen, og vælg Reservér definitivt og derefter Definitivt under Skift status.</span><span class="sxs-lookup"><span data-stu-id="55344-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="55344-160">Status for reservation er nu Definitiv.</span><span class="sxs-lookup"><span data-stu-id="55344-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="55344-161">Når du har lukket planlægningsområdet, kan du se, at timerne for ressourcen er ændret fra Foreløbig til Definitiv i teammedlemsgitteret.</span><span class="sxs-lookup"><span data-stu-id="55344-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="55344-162">Du kan nu tildele ressourcen til opgaver (hvis der er overensstemmelse mellem de definitivt reserverede timer og indsatstimerne i opgaven, der skal tildeles).</span><span class="sxs-lookup"><span data-stu-id="55344-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="55344-163">Bemærk, at hvis du har fulgt trinnene for opfyldelse af generisk ressource i punkt #3 ovenfor, og du ændrer status for den foreløbige reserverbare ressource til definitiv, fjernes det generiske teammedlem fra teamet.</span><span class="sxs-lookup"><span data-stu-id="55344-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]