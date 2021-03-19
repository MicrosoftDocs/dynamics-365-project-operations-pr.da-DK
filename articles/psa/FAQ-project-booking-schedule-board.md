---
title: Oprette en projektreservation fra planlægningsområdet
description: Denne emne indeholder oplysninger om, hvordan du kan oprette en projektreservation fra planlægningsområdet.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286106"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="e9bbd-103">Oprette en projektreservation fra planlægningsområdet</span><span class="sxs-lookup"><span data-stu-id="e9bbd-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e9bbd-104">Du kan reservere en ressource til et projekt direkte fra fanen **Team** i projektet eller ved at generere et ressourcekrav fra en tildeling af et generisk teammedlem og derefter indfri genererede krav med et projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="e9bbd-105">Du kan også reservere en ressource til et projekt direkte fra planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="e9bbd-106">Der er tre måder, du kan gøre det på:</span><span class="sxs-lookup"><span data-stu-id="e9bbd-106">There are three ways to do this:</span></span>

- <span data-ttu-id="e9bbd-107">**Reservere fra et genereret ressourcekrav:** Du kan oprette et ressourcekrav, når du har oprettet en generisk ressource og tildelt opgaver i et projekt.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="e9bbd-108">**Reservere fra det primære krav:** De primære krav vises i planlægningsområdet under fanen **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="e9bbd-109">**Reservere fra et nyt ressourcekrav:** Du kan oprette et ressourcekrav fra bunden og knytte det til et projekt.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="e9bbd-110">I planlægningsområdet vises ressourcekravet under fanen **Åbn Krav**.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="e9bbd-111">Reservere fra et genereret ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="e9bbd-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="e9bbd-112">Du kan oprette en generisk ressource og tildele den en eller flere opgaver i et projekt.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="e9bbd-113">Derefter kan du oprette et ressourcekrav ud fra det generiske teammedlem.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="e9bbd-114">I planlægningsområdet vises denne ressource under fanen **Åbn Krav**. Det kan være nødvendigt at bruge kolonnefiltre på gitteret, hvis du har mange åbne krav.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="e9bbd-115">![Åbn fanen Krav i planlægningsområdet](media/FAQ-Project-Booking-Schedule-Board-1.png "Skærmbillede af reservations- og tildelingstabel")</span><span class="sxs-lookup"><span data-stu-id="e9bbd-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e9bbd-116">Vælg kravet.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-116">Select the requirement.</span></span> <span data-ttu-id="e9bbd-117">Fanen **Find tilgængelighed** vises over den valgte række.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="e9bbd-118">Når du vælger fanen, åbnes tilstanden Planlægningsassistent i planlægningsområdet, og derefter filtreres de tilgængelige ressourcer, der opfylder ressourcekravet.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="e9bbd-119">Derefter kan du reservere en ressource.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="e9bbd-120">Du kan også trække og slippe den markerede række fra bunden af planlægningsområdet til en ressourcecelle i gitteret ovenfor.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="e9bbd-121">Når du slipper kravet, åbnes panelet **Opret ressourcereservation** til højre.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="e9bbd-122">Hvis du vælger **Reservér**, reserveres ressourcen til projektteamet.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-122">Selecting **Book** books the resource onto the project team.</span></span>

![Panelet Opret ressourcereservation](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="e9bbd-124">Reservere fra det primære krav</span><span class="sxs-lookup"><span data-stu-id="e9bbd-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="e9bbd-125">Når du opretter et projekt i Project Service, oprettes der automatisk et ressourcekrav, der kaldes det primære krav.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="e9bbd-126">Det er et tomt krav, der bruges til hurtigt at reservere en ressource i planlægningsområdet uden at generere et krav eller oprette et fra bunden.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="e9bbd-127">Da kravet er tomt, skal du angive datoer samt fordelingsmetoden og timer, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="e9bbd-128">Du kan reservere en ressource med det primære krav ved i planlægningsområdet at vælge fanen **Projekt**. Hvis du har mange projekter, skal du muligvis bruge kolonnefilteret i kolonnen **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="e9bbd-129">![Kolonnefiltre i planlægningsområdet](media/FAQ-Project-Booking-Schedule-Board-2.png "Skærmbillede af reservations- og tildelingstabel")</span><span class="sxs-lookup"><span data-stu-id="e9bbd-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e9bbd-130">Vælg det krav, der kun har projektnavnet som navn og har en varighed på nul (0).</span><span class="sxs-lookup"><span data-stu-id="e9bbd-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="e9bbd-131">Vælg fanen **Find tilgængelighed**, der vises i rækken.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="e9bbd-132">Dette aktiverer tilstanden Planlægningsassistent i planlægningsområdet og viser tilgængelige ressourcer, der kan reserveres til projektet.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="e9bbd-133">Da et **Primært krav** er et tomt krav med nul (0) varighed, skal du angive varigheden i panelet **Opret ressourcereservation**, når du vælger og reserverer en ressource.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="e9bbd-134">Du kan også vælge det **primære projektkrav** nederst i planlægningsområdet og trække og slippe det på en ressource for at reservere det.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="e9bbd-135">Da **Primært krav** er et tomt krav med nul (0) varighed, skal du angive varigheden i panelet **Opret ressourcereservation**, når du vælger og reserverer en ressource.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="e9bbd-136">Når du reserverer en ressource ved hjælp af **Primært krav** i planlægningsområdet, kan du tilføje det i projektteamet uden tildelinger.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="e9bbd-137">Reservere fra et nyt ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="e9bbd-137">Book from a new resource requirement</span></span>
<span data-ttu-id="e9bbd-138">Benyt følgende fremgangsmåde til at reservere fra et nyt ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="e9bbd-139">Gå til **Ressourcekrav**, og vælg derefter **Ny** for at oprette et nyt ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="e9bbd-140">Vælg et projekt, som kravet skal knyttes til i projektet, under fanen **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="e9bbd-141">Det nyoprettede krav vises i planlægningsområdet som et **åbent krav**, som du kan opfylde.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="e9bbd-142">Reservér ressourcen for at føje den til projektteamet.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="e9bbd-143">Nu, hvor ressourcen er reserveret, skal du tildele opgaver manuelt.</span><span class="sxs-lookup"><span data-stu-id="e9bbd-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]