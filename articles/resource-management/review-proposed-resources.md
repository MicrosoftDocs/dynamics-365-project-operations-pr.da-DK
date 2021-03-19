---
title: Gennemse foreslåede ressourcer
description: Dette emne indeholder oplysninger om, hvordan du foreslår projektressourcer.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279266"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="2f9f0-103">Gennemse foreslåede ressourcer</span><span class="sxs-lookup"><span data-stu-id="2f9f0-103">Review proposed resources</span></span>

<span data-ttu-id="2f9f0-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="2f9f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2f9f0-105">Personalechefer kan foreslå en ressource til projektlederen ved hjælp af en ressourceanmodning.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="2f9f0-106">Vælg **Find ressourcer** i anmodningsgitteret eller i selve anmodningen.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="2f9f0-107">På siden **Planlægningsassistent** skal du vælge ressourcen og derefter i ruden **Opret ressourcereservation** i feltet **Reservationsstatus** vælge **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="2f9f0-108">Følgende statusopdateringer forekommer:</span><span class="sxs-lookup"><span data-stu-id="2f9f0-108">The following status updates occur:</span></span>

- <span data-ttu-id="2f9f0-109">På siden **Planlægningsassistent** opdateres statusindikatorerne for at indikere, at reservationen er foreslået, ikke definitivt reserveret.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="2f9f0-110">På ressourceanmodningen ændres status til **Skal gennemses**.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="2f9f0-111">På fanen **Team** for projektet er det generiske teammedlems værdi for **Anmodningsstatus** ændret til **Skal gennemses**.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="2f9f0-112">Projektlederen kan enten acceptere eller afvise forslaget.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="2f9f0-113">Når personalechefer behandler ressourceanmodninger, kan de benytte en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="2f9f0-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="2f9f0-114">Foreslå flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig for at imødekomme de påkrævede timer.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="2f9f0-115">De foreslåede timer deles derefter mellem flere ressourcer, der kan opfylde de krævede timer.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="2f9f0-116">I dette scenario må timerne ikke overlappe hinanden.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="2f9f0-117">Foreslå færre ressourcer end nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="2f9f0-118">I dette scenario er den foreslåede ressourcekapacitet mindre end de krævede timer, som anmoderen har angivet.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="2f9f0-119">Når anmoderen accepterer de foreslåede ressourcer, oprettes der derfor et uopfyldt ressourcekrav for at registrere det resterende behov.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="2f9f0-120">Reservér flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig til udførelse af arbejdet.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="2f9f0-121">Reservere færre ressourcer end nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-121">Book fewer resources than are required.</span></span> <span data-ttu-id="2f9f0-122">I dette scenario er de reserverede timer færre end de krævede timer.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="2f9f0-123">Systemet hjælper dig med at foreslå ressourcer i stedet for reservationer, så anmoderen kan kontrollere og holde styr på det resterende behov.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="2f9f0-124">Ressourcetilgængelighed</span><span class="sxs-lookup"><span data-stu-id="2f9f0-124">Resource availability</span></span>

<span data-ttu-id="2f9f0-125">Det er vigtigt, at personalechefer kan få vist tilgængeligheden af ressourcer og opdatere reservationer.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="2f9f0-126">I visse tilfælde er der ingen formel efterspørgsel (ressourceanmodning), men ressourcestyringen skal reagere på et ikke-planlagt behov, der kommer gennem kanaler, f.eks. e-mail, telefonopkald eller onlinemeddelelse.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="2f9f0-127">Personalechefer bruger planlægningsområdet til at opdatere ressourcer og reservationer.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="2f9f0-128">Ressourcens arbejdstimer bruges som udgangspunkt for beregning af tilgængeligheden af en ressource.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="2f9f0-129">Ressourcereservationer forbruger ressourcernes kapacitet.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="2f9f0-130">I planlægningsområdet bruges farver og skygge til at vise reservationer, tilgængelighed og overreservationer samt statussen for reservationer.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="2f9f0-131">En indstilling i indstillingerne for planlægningsområdet giver dig mulighed for at få vist en forklaring.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="2f9f0-132">Hvis der vises en højrepil ud for en enkeltstående ressource i planlægningsområdet, kan ressourcen udvides til at få vist oplysninger om det arbejde, som ressourcen er reserveret til.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="2f9f0-133">Da Dynamics 365 Project Operations bruger Universal Resource Scheduling-programmet, og du også har Dynamics 365 Field Service installeret, kan du få vist oplysninger om ressourcereservationer for projekter, arbejdsordrer og andre objekter, som du har udvidet planlægningen til.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="2f9f0-134">Hvis du vil have vist flere oplysninger om en enkelt ressource, skal du højreklikke på den for at åbne ressourcekortet.</span><span class="sxs-lookup"><span data-stu-id="2f9f0-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]