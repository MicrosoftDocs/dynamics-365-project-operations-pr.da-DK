---
title: Foreløbig reservation af krav
description: Dette emne indeholder oplysninger om, hvordan du reserverer krav foreløbigt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124091"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="d0fcb-103">Foreløbig reservation af krav</span><span class="sxs-lookup"><span data-stu-id="d0fcb-103">Soft-book requirements</span></span>

<span data-ttu-id="d0fcb-104">Et ressourcekrav kan reserveres definitivt.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="d0fcb-105">En definitiv reservation opretter et forslag, der forbruger en ressources kapacitet.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="d0fcb-106">Derefter sendes forslaget tilbage til anmoderen til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="d0fcb-107">En foreløbig reservation føjer foreløbigt en ressource til et projektteam og har en anden status i planlægningsområdet, men den forbruger ikke ressourcens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="d0fcb-108">Hvis du reserverer en ressource foreløbigt i planlægningsområdet, skal du angive feltet **Reservationsstatus** til **Foreløbig**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Reservationsstatus indstillet til Foreløbig](media/Resource-Management-image77.png)

<span data-ttu-id="d0fcb-110">Når fanen **Team** er i visningen **Navngivne teammedlemmer**, vises ressourcen her.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="d0fcb-111">Timer der er foreløbigt reserveret i kolonnen **Foreløbigt reserverede timer**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Foreløbigt reserverede timer i visningen Navngivne teammedlemmer](media/Resource-Management-image78.png)

<span data-ttu-id="d0fcb-113">Foreløbigt reserverede teammedlemmer kan tildeles til opgaver.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-113">Soft-booked team members can be assigned to tasks.</span></span>

![Foreløbigt reserveret teammedlem tildelt til en opgave](media/Resource-Management-image79.png)

<span data-ttu-id="d0fcb-115">På fanen **Afstemning** vises der ingen reservationer for en foreløbigt reserveret ressource, da fanen **Afstemning** kun medtager definitive reservationer.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Foreløbigt reserveret ressource uden reservationer på fanen Afstemning](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="d0fcb-117">Du kan ikke reservere en ressource foreløbigt i et krav, der blev genereret i et generisk teammedlem.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="d0fcb-118">I planlægningsområdet bruges der en anden farve til foreløbige reservationer af en ressource.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Foreløbige reservationer i planlægningsområdet](media/Resource-Management-image81.png)

<span data-ttu-id="d0fcb-120">Hvis du vil konvertere en foreløbig reservation til en definitiv reservation, skal du højreklikke på den foreløbige reservation i planlægningsområdet og derefter vælge **Skift status** \> **Definitiv reservation** \> **Definitiv**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Ændring af reservationsstatus til Definitiv](media/Resource-Management-image82.png)

<span data-ttu-id="d0fcb-122">Reservationen ændres, og statussen ændres i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="d0fcb-123">Da reservationsstatussen nu er **Definitiv**, vises ressourcen som reserveret, og dens kapacitet og tilgængelighed justeres.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="d0fcb-124">Du kan bruge samme metode til at annullere en definitiv reservation eller en midlertidig reservation i planlægningsssområdet.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="d0fcb-125">Hvis du vil konvertere en ressource, der er foreløbigt reserveret til definitivt reserveret på projektets fane **Team,** skal du vælge ressourcen og derefter **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Bekræft kommando](media/Resource-Management-image83.png)
