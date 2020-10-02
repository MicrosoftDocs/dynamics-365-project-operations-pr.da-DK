---
title: Gennemse foreslåede ressourcer
description: Dette emne indeholder oplysninger om, hvordan du foreslår projektressourcer.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897354"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="b882a-103">Gennemse foreslåede ressourcer</span><span class="sxs-lookup"><span data-stu-id="b882a-103">Review proposed resources</span></span>

<span data-ttu-id="b882a-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b882a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b882a-105">Personalechefer kan foreslå en ressource til projektlederen ved hjælp af en ressourceanmodning.</span><span class="sxs-lookup"><span data-stu-id="b882a-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="b882a-106">Vælg **Find ressourcer** i anmodningsgitteret eller i selve anmodningen.</span><span class="sxs-lookup"><span data-stu-id="b882a-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="b882a-107">På siden **Planlægningsassistent** skal du vælge ressourcen og derefter i ruden **Opret ressourcereservation** i feltet **Reservationsstatus** vælge **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="b882a-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="b882a-108">Følgende statusopdateringer forekommer:</span><span class="sxs-lookup"><span data-stu-id="b882a-108">The following status updates occur:</span></span>

- <span data-ttu-id="b882a-109">På siden **Planlægningsassistent** opdateres statusindikatorerne for at indikere, at reservationen er foreslået, ikke definitivt reserveret.</span><span class="sxs-lookup"><span data-stu-id="b882a-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="b882a-110">På ressourceanmodningen ændres status til **Skal gennemses**.</span><span class="sxs-lookup"><span data-stu-id="b882a-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="b882a-111">På fanen **Team** for projektet er det generiske teammedlems værdi for **Anmodningsstatus** ændret til **Skal gennemses**.</span><span class="sxs-lookup"><span data-stu-id="b882a-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="b882a-112">Projektlederen kan enten acceptere eller afvise forslaget.</span><span class="sxs-lookup"><span data-stu-id="b882a-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="b882a-113">Når personalechefer behandler ressourceanmodninger, kan de benytte en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="b882a-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="b882a-114">Foreslå flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig for at imødekomme de påkrævede timer.</span><span class="sxs-lookup"><span data-stu-id="b882a-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="b882a-115">De foreslåede timer deles derefter mellem flere ressourcer, der kan opfylde de krævede timer.</span><span class="sxs-lookup"><span data-stu-id="b882a-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="b882a-116">I dette scenario må timerne ikke overlappe hinanden.</span><span class="sxs-lookup"><span data-stu-id="b882a-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="b882a-117">Foreslå færre ressourcer end nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="b882a-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="b882a-118">I dette scenario er den foreslåede ressourcekapacitet mindre end de krævede timer, som anmoderen har angivet.</span><span class="sxs-lookup"><span data-stu-id="b882a-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="b882a-119">Når anmoderen accepterer de foreslåede ressourcer, oprettes der derfor et uopfyldt ressourcekrav for at registrere det resterende behov.</span><span class="sxs-lookup"><span data-stu-id="b882a-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="b882a-120">Reservér flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig til udførelse af arbejdet.</span><span class="sxs-lookup"><span data-stu-id="b882a-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="b882a-121">Reservere færre ressourcer end nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="b882a-121">Book fewer resources than are required.</span></span> <span data-ttu-id="b882a-122">I dette scenario er de reserverede timer færre end de krævede timer.</span><span class="sxs-lookup"><span data-stu-id="b882a-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="b882a-123">Systemet hjælper dig med at foreslå ressourcer i stedet for reservationer, så anmoderen kan kontrollere og holde styr på det resterende behov.</span><span class="sxs-lookup"><span data-stu-id="b882a-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="b882a-124">Fakturerbart tidsforbrug</span><span class="sxs-lookup"><span data-stu-id="b882a-124">Billable utilization</span></span>

<span data-ttu-id="b882a-125">Ressourcer kan have et fakturerbart tidsforbrug for et mål.</span><span class="sxs-lookup"><span data-stu-id="b882a-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="b882a-126">Dette mål-tidsforbrug er enten defineret som en attribut i en ressources standardrolle eller angivet på posten for den individuelle, reserverbare ressource.</span><span class="sxs-lookup"><span data-stu-id="b882a-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="b882a-127">Beregningerne af tidsforbrug er baseret på det faktiske antal timer, som ressourcer har rapporteret ved hjælp af godkendte tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="b882a-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="b882a-128">Følgende formler bruges til at beregne forbrug:</span><span class="sxs-lookup"><span data-stu-id="b882a-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="b882a-129">Fakturerbart tidsforbrug = fakturerbare faktiske timer ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="b882a-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="b882a-130">Ikke-fakturerbar tidsforbrug = faktisk tid med faktureringstype-ID = ikke-fakturerbar, komplementær eller ikke tilgængelig ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="b882a-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="b882a-131">Intern = faktisk tid uden salgskontrakt ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="b882a-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="b882a-132">Ressourcekapacitet = ressourcens arbejdstimer – ikke til stede – fridage</span><span class="sxs-lookup"><span data-stu-id="b882a-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="b882a-133">Du kan finde visningen **Ressourceforbrug** i ruden **Ressourcer.**</span><span class="sxs-lookup"><span data-stu-id="b882a-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="b882a-134">Hver celle i gitteret repræsenterer den fakturerbare udnyttelsesprocent for ressourcen i en periode, f.eks. en dag, uge eller måned.</span><span class="sxs-lookup"><span data-stu-id="b882a-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="b882a-135">Følgende formler bruges til farvning af cellerne:</span><span class="sxs-lookup"><span data-stu-id="b882a-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="b882a-136">**Grøn:** Fakturerbart tidsforbrug \>= Resourcens måltidsforbrug</span><span class="sxs-lookup"><span data-stu-id="b882a-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="b882a-137">**Gul:** Mål-tidsforbrug – 20 \<= Fakturerbart tidsforbrug \< Mål-tidsforbrug</span><span class="sxs-lookup"><span data-stu-id="b882a-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="b882a-138">**Rød:** Fakturerbart tidsforbrug \< Mål-tidsforbrug – 20</span><span class="sxs-lookup"><span data-stu-id="b882a-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="b882a-139">Da visningen **Ressourceforbrug** er baseret på planlægningsområdet, kan du bruge filtreringsfunktionerne i planlægningsområdet til at filtrere resultaterne.</span><span class="sxs-lookup"><span data-stu-id="b882a-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="b882a-140">Gitteret kræver, at du angiver et mål-tidsforbrug for enten rolle eller den enkelte ressource.</span><span class="sxs-lookup"><span data-stu-id="b882a-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="b882a-141">Du konfigurerer dette ved at gå til **Ressourcer** \> **Ressourceroller**.</span><span class="sxs-lookup"><span data-stu-id="b882a-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="b882a-142">Derudover skal der tildeles en standardrolle til hver af de pågældende reserverbare ressourcer.</span><span class="sxs-lookup"><span data-stu-id="b882a-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="b882a-143">Gå til **Ressourcer** \> **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="b882a-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="b882a-144">På fanen **Project Service** skal du kontrollere, at der er defineret en ressourcerolle, og at feltet **Er standard** herfor er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b882a-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="b882a-145">Du kan tilføje flere roller, hvor **Er standard =** nej.</span><span class="sxs-lookup"><span data-stu-id="b882a-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="b882a-146">Den rolle, hvor **Er standard = Ja**, bruges til at evaluere ressourcens tidsforbrug i forhold til destinationen for den pågældende rolle.</span><span class="sxs-lookup"><span data-stu-id="b882a-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="b882a-147">På fanen **Project Service** kan du også angive en individuel mål-tidsforbrug for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b882a-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="b882a-148">I beregningen af tidsforbruget bruger derefter denne mål-tidsforbrug til at evaluere ressourcens mål i stedet for målet for ressourcens standardrolle.</span><span class="sxs-lookup"><span data-stu-id="b882a-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="b882a-149">Tidsforbrug vises kun for en ressource, hvis den pågældende ressource har godkendt fakturerbar tid i løbet af den periode, der vises i gitteret.</span><span class="sxs-lookup"><span data-stu-id="b882a-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="b882a-150">Ressourcetilgængelighed</span><span class="sxs-lookup"><span data-stu-id="b882a-150">Resource availability</span></span>

<span data-ttu-id="b882a-151">Det er vigtigt, at personalechefer kan få vist tilgængeligheden af ressourcer og opdatere reservationer.</span><span class="sxs-lookup"><span data-stu-id="b882a-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="b882a-152">I visse tilfælde er der ingen formel efterspørgsel (ressourceanmodning), men ressourcestyringen skal reagere på et ikke-planlagt behov, der kommer gennem kanaler, f.eks. e-mail, telefonopkald eller onlinemeddelelse.</span><span class="sxs-lookup"><span data-stu-id="b882a-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="b882a-153">Personalechefer bruger planlægningsområdet til at opdatere ressourcer og reservationer.</span><span class="sxs-lookup"><span data-stu-id="b882a-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="b882a-154">Ressourcens arbejdstimer bruges som udgangspunkt for beregning af tilgængeligheden af en ressource.</span><span class="sxs-lookup"><span data-stu-id="b882a-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="b882a-155">Ressourcereservationer forbruger ressourcernes kapacitet.</span><span class="sxs-lookup"><span data-stu-id="b882a-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="b882a-156">I planlægningsområdet bruges farver og skygge til at vise reservationer, tilgængelighed og overreservationer samt statussen for reservationer.</span><span class="sxs-lookup"><span data-stu-id="b882a-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="b882a-157">En indstilling i indstillingerne for planlægningsområdet giver dig mulighed for at få vist en forklaring.</span><span class="sxs-lookup"><span data-stu-id="b882a-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="b882a-158">Hvis der vises en højrepil ud for en enkeltstående ressource i planlægningsområdet, kan ressourcen udvides til at få vist oplysninger om det arbejde, som ressourcen er reserveret til.</span><span class="sxs-lookup"><span data-stu-id="b882a-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="b882a-159">Da Dynamics 365 Project Operations bruger Universal Resource Scheduling-programmet, og du også har Dynamics 365 Field Service installeret, kan du få vist oplysninger om ressourcereservationer for projekter, arbejdsordrer og andre objekter, som du har udvidet planlægningen til.</span><span class="sxs-lookup"><span data-stu-id="b882a-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="b882a-160">Hvis du vil have vist flere oplysninger om en enkelt ressource, skal du højreklikke på den for at åbne ressourcekortet.</span><span class="sxs-lookup"><span data-stu-id="b882a-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

