---
title: Administrer tidszoner
description: Når et projekt oprettes, er tidszonen baseret på den tidszone, der er angivet i den anvendte arbejdstidsskabelon.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e0cf24a9916f7ceedee0e9d6fa9399a88c3e4b91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279536"
---
# <a name="manage-time-zones"></a><span data-ttu-id="f9ea7-103">Administrer tidszoner</span><span class="sxs-lookup"><span data-stu-id="f9ea7-103">Manage time zones</span></span>

<span data-ttu-id="f9ea7-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="f9ea7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="f9ea7-105">Projekter</span><span class="sxs-lookup"><span data-stu-id="f9ea7-105">Projects</span></span>

<span data-ttu-id="f9ea7-106">Når et projekt oprettes, er tidszonen baseret på den tidszone, der er angivet i den anvendte arbejdstidsskabelon.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="f9ea7-107">På **Projektet** for er datoerne altid relative i forhold til den brugers tidszone, der er logget på de enkelte faner, undtagen fanen **Opgave**. Når du får vist arbejdsopgavehierarkiet, vises datoerne altid i projektets tidszone.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="f9ea7-108">Opgaver</span><span class="sxs-lookup"><span data-stu-id="f9ea7-108">Tasks</span></span>

<span data-ttu-id="f9ea7-109">Når en opgave er oprettet, styres starttidspunktet, sluttidspunktet og tider/dag af projektets arbejdstid.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="f9ea7-110">Hvis en opgave f.eks. er oprettet ved hjælp af et projekt, hvor tidszonen er -8 PST, og hvor de efterfølgende arbejdstider er: 9:00 til 17:00 mandag til fredag, vil alle opgaver, der er oprettet uden en tildeling, respektere starttidspunktet og sluttidspunktet for projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="f9ea7-111">Administrer ressourcer med tidszoner</span><span class="sxs-lookup"><span data-stu-id="f9ea7-111">Manage resources with time zones</span></span>

<span data-ttu-id="f9ea7-112">Hvis du vil have præcise og forudsigelige resultater, når du bruger **Forlæng reservation**, er der to nøgleforudsætninger, der skal overholdes:</span><span class="sxs-lookup"><span data-stu-id="f9ea7-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="f9ea7-113">Brugeren skal konfigurere enhedens tidszone, så den stemmer overens med den tidszone, der er angivet i systemets **Indstillinger for personlig tilpasning**.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Tidszoneindstillinger i Windows 10](media/reconcile-assignments-03.png)

  ![Tidszoneindstillinger i tilpasningsindstillinger](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="f9ea7-116">Den reserverbare ressource skal have mindst ét minuts arbejdstid, som overlapper med de profiler, der bruges til at definere den ønskede udvidelse.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="f9ea7-117">Følgende ressourcer kan f.eks. have arbejdstid mellem kl. 9:00 og 19:00.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Sammenligning af ressourceprofiler](media/reconcile-assignments-05.png)

<span data-ttu-id="f9ea7-119">Følgende tabel viser:</span><span class="sxs-lookup"><span data-stu-id="f9ea7-119">The following table shows:</span></span>

- <span data-ttu-id="f9ea7-120">En projektkalenderskabelon</span><span class="sxs-lookup"><span data-stu-id="f9ea7-120">A project calendar template</span></span>
- <span data-ttu-id="f9ea7-121">Ressource A: Denne ressource har samme kalender og er i den samme tidszone som projektet.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="f9ea7-122">Starttidspunktet for reservationerne er kl. 9:00.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="f9ea7-123">Ressource B: Denne ressource er placeret i en anden tidszone end projektet og starter kl. 7:00 i deres tidszone.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="f9ea7-124">Reservationerne starter dog kl. 9:00, som er det tidligste starttidspunkt for tildelingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="f9ea7-125">Ressourcer C og D: Ressourcerne er placeret i forskellige tidszoner, som både varierer i forhold til hinanden og projektet, og deres reservationer starter tidligst de respektive ledige starttider.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="f9ea7-126">Objekt</span><span class="sxs-lookup"><span data-stu-id="f9ea7-126">Entity</span></span>  |<span data-ttu-id="f9ea7-127">Kalender</span><span class="sxs-lookup"><span data-stu-id="f9ea7-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="f9ea7-128">Projektkalenderskabelon</span><span class="sxs-lookup"><span data-stu-id="f9ea7-128">Project calendar template</span></span>   | ![projektkalender](media/reconcile-assignments-06.png) |
|<span data-ttu-id="f9ea7-130">Ressource A</span><span class="sxs-lookup"><span data-stu-id="f9ea7-130">Resource A</span></span>  | ![Kalender for ressource A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="f9ea7-132">Ressource B</span><span class="sxs-lookup"><span data-stu-id="f9ea7-132">Resource B</span></span>  |  ![Kalender for ressource B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="f9ea7-134">Ressource C</span><span class="sxs-lookup"><span data-stu-id="f9ea7-134">Resource C</span></span>  |  ![Kalender for ressource C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="f9ea7-136">Ressource D</span><span class="sxs-lookup"><span data-stu-id="f9ea7-136">Resource D</span></span>  | ![Kalender for ressource D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="f9ea7-138">Når du navigerer til visningen **Afstemning**, vises ressourcetildelingerne og de manglende tilknyttede reservationer.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Afstemningsvisning før udvidelse](media/reconcile-assignments-10.png)

<span data-ttu-id="f9ea7-140">Når funktionen til forlængelse af reservation er blevet brugt for de enkelte ressourcer, forlænges reservationerne for hver ressource, da hver ressources arbejdstid overlappede med underskudsprofilerne.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Afstemningsvisning efter reservationsudvidelse](media/reconcile-assignments-11.png) 

<span data-ttu-id="f9ea7-142">Bemærk, hvis du kigger nærmere på detaljerne for reservationerne, kan du se forskelle på starttidspunkterne for reservationerne.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="f9ea7-143">Reservationernes startdato er ikke tidligere end starttidspunktet for tildelingsprofilen og kan ikke være før ressourcens tilgængelige starttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="f9ea7-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nye reservationer af ressourcerne i planlægningsområdet](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]