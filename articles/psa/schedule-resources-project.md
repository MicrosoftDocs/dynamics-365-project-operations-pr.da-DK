---
title: Planlægge ressourcer til et projekt
description: Sådan planlægger du ressourcer til et projekt i Project Service
author: JohnPBurrows
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
ms.openlocfilehash: f0a234f96419bac58cd932a082010da672e7dcb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282641"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="9a40b-103">Planlægge ressourcer til et projekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9a40b-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9a40b-104">Du kan kontrollere ressourcetilgængelighed for at få et generelt overblik over reservationer af dine ressourcer, eller du kan filtrere visningen efter færdigheder, team, placering og andre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="9a40b-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="9a40b-105">Planlægningsområdet viser en liste over ressourcer og deres tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="9a40b-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="9a40b-106">Vælg en visningstilstand for at få vist tilgængelighed efter **timer**, **dag**, **uge** eller **måned**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="9a40b-107">Før du bruger planlægningsområdet, er det vigtigt at konfigurere det.</span><span class="sxs-lookup"><span data-stu-id="9a40b-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="9a40b-108">Du kan finde flere oplysninger under [Konfigurering af planlægningsområdet (Field Service eller Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="9a40b-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="9a40b-109">Hvis du bruger en ældre version, kan du finde oplysninger om ressourcetilgængelighed under [Få vist ressourcetilgængelighed](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="9a40b-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="9a40b-110">For at bruge reservationsfunktionerne for planlægningsområde, geokodnings- og placeringstjenester skal du aktivere kort.</span><span class="sxs-lookup"><span data-stu-id="9a40b-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="9a40b-111">I hovedmenuen skal du vælge **Ressourceplanlægning** > **Administration**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="9a40b-112">Klik på **Planlægningsparametre**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="9a40b-113">Åbn posten, og rul ned til afsnittet **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="9a40b-114">I feltet **Opret forbindelse til kort** skal du vælge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="9a40b-115">Acceptér vilkårene, og gem posten.</span><span class="sxs-lookup"><span data-stu-id="9a40b-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="9a40b-116">I hovedmenuen skal du vælge **Project Service** > **Planlægningsområde**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="9a40b-117">Herfra er der flere måder at planlægge et reservationskrav på manuelt.</span><span class="sxs-lookup"><span data-stu-id="9a40b-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="9a40b-118">Vælg den metode, der fungerer for dig.</span><span class="sxs-lookup"><span data-stu-id="9a40b-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="9a40b-119">Find tilgængelige ressourcer</span><span class="sxs-lookup"><span data-stu-id="9a40b-119">Find available resources</span></span>

1.  <span data-ttu-id="9a40b-120">På listen **Krav til reservationer** skal du højreklikke på en ikke-planlagt reservation og vælge en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="9a40b-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="9a40b-121">Vælg **Søg efter Tilgængelighed – Aktuelle ressourcer** for at finde en tilgængelig ressource på listen i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="9a40b-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="9a40b-122">Vælg **Søg efter Tilgængelighed – Alle ressourcer** for at finde en tilgængelig ressource blandt ressourcerne i systemet.</span><span class="sxs-lookup"><span data-stu-id="9a40b-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="9a40b-123">Når du gør dette, viser filtrene indstillinger for det valgte reservationskrav.</span><span class="sxs-lookup"><span data-stu-id="9a40b-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="9a40b-124">Når du ser en tilgængelige rubrik, skal du højreklikke på tidsrubrikken i planlægningsområdet og vælge **Reservér her**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="9a40b-125">Eller træk og slip reservationskravet til den ledige tidsrubrik.</span><span class="sxs-lookup"><span data-stu-id="9a40b-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="9a40b-126">Reservere en ressource ved hjælp af visningen daglig og finde ud af, hvem der er underreserveret</span><span class="sxs-lookup"><span data-stu-id="9a40b-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="9a40b-127">I planlægningsområdet skal du vælge **Visningstilstand**, og derefter vælge **Dage**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="9a40b-128">Der åbnes en gittervisning over, hvor mange timer en ressource er reserveret pr. dag, og hvilke dage ressourcen er ledig.</span><span class="sxs-lookup"><span data-stu-id="9a40b-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="9a40b-129">Klik på navnet på den ressource, du vil reservere, og vælg derefter **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="9a40b-130">I dialogboksen **Ressourcereservation (opret)** skal du vælge det projekt, du vil reservere ressourcen til, sammen med en reservationsmetode og start- og sluttidspunkter.</span><span class="sxs-lookup"><span data-stu-id="9a40b-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="9a40b-131">Når du er færdig, skal du vælge **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="9a40b-132">Visning til planlægningsområdet</span><span class="sxs-lookup"><span data-stu-id="9a40b-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="9a40b-133">Vælg et ikke-planlagt reservationskrav på listen nederst.</span><span class="sxs-lookup"><span data-stu-id="9a40b-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="9a40b-134">Træk reservationskravet til en tilgængelig ressource eller tidsrubrik i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="9a40b-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="9a40b-135">Når du er færdig, skal du vælge **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="9a40b-136">Flere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9a40b-136">Additional resources</span></span>  
 [<span data-ttu-id="9a40b-137">Ressourcestyringsvejledning</span><span class="sxs-lookup"><span data-stu-id="9a40b-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]