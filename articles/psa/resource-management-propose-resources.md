---
title: Foreslå projektressourcer
description: Dette emne indeholder oplysninger om forslag til projektressourcer.
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147511"
---
# <a name="propose-project-resources"></a><span data-ttu-id="88ca9-103">Foreslå projektressourcer</span><span class="sxs-lookup"><span data-stu-id="88ca9-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="88ca9-104">Personalechefer kan foreslå en ressource til projektlederen ved hjælp af en ressourceanmodning.</span><span class="sxs-lookup"><span data-stu-id="88ca9-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="88ca9-105">Vælg **Find ressourcer** i anmodningsgitteret eller i selve anmodningen.</span><span class="sxs-lookup"><span data-stu-id="88ca9-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="88ca9-106">På siden **Planlægningsassistent** skal du vælge ressourcen og derefter i ruden **Opret ressourcereservation** i feltet **Reservationsstatus** vælge **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="88ca9-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Foreslået ressource valgt](media/Resource-Management-image62.png)

<span data-ttu-id="88ca9-108">Følgende statusopdateringer forekommer:</span><span class="sxs-lookup"><span data-stu-id="88ca9-108">The following status updates occur:</span></span>

- <span data-ttu-id="88ca9-109">På siden **Planlægningsassistent** opdateres statusindikatorerne for at indikere, at reservationen er foreslået, ikke definitivt reserveret.</span><span class="sxs-lookup"><span data-stu-id="88ca9-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Statusindikatorer for foreslået reservation på siden Planlægningsassistent](media/Resource-Management-image63.png)

- <span data-ttu-id="88ca9-111">På ressourceanmodningen ændres status til **Skal gennemses**.</span><span class="sxs-lookup"><span data-stu-id="88ca9-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Ressourceanmodningsstatus ændret til Skal gennemses.](media/Resource-Management-image64.png)

- <span data-ttu-id="88ca9-113">På fanen **Team** for projektet er det generiske teammedlems værdi for **Anmodningsstatus** ændret til **Skal gennemses**.</span><span class="sxs-lookup"><span data-stu-id="88ca9-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Det generiske teammedlems anmodningsstatus ændret til Skal gennemses på fanen Team.](media/Resource-Management-image48.png)

<span data-ttu-id="88ca9-115">Projektlederen kan enten acceptere eller afvise forslaget.</span><span class="sxs-lookup"><span data-stu-id="88ca9-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="88ca9-116">Når personalechefer behandler ressourceanmodninger, kan de benytte en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="88ca9-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="88ca9-117">Foreslå flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig for at imødekomme de påkrævede timer.</span><span class="sxs-lookup"><span data-stu-id="88ca9-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="88ca9-118">De foreslåede timer deles derefter mellem flere ressourcer, der kan opfylde de krævede timer.</span><span class="sxs-lookup"><span data-stu-id="88ca9-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="88ca9-119">I dette scenario må timerne ikke overlappe hinanden.</span><span class="sxs-lookup"><span data-stu-id="88ca9-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="88ca9-120">Foreslå færre ressourcer end nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="88ca9-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="88ca9-121">I dette scenario er den foreslåede ressourcekapacitet mindre end de krævede timer, som anmoderen har angivet.</span><span class="sxs-lookup"><span data-stu-id="88ca9-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="88ca9-122">Når anmoderen accepterer de foreslåede ressourcer, oprettes der derfor et uopfyldt ressourcekrav for at registrere det resterende behov.</span><span class="sxs-lookup"><span data-stu-id="88ca9-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="88ca9-123">Reservér flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig til udførelse af arbejdet.</span><span class="sxs-lookup"><span data-stu-id="88ca9-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="88ca9-124">Reservere færre ressourcer end nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="88ca9-124">Book fewer resources than are required.</span></span> <span data-ttu-id="88ca9-125">I dette scenario er de reserverede timer færre end de krævede timer.</span><span class="sxs-lookup"><span data-stu-id="88ca9-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="88ca9-126">Systemet hjælper dig med at foreslå ressourcer i stedet for reservationer, så anmoderen kan kontrollere og holde styr på det resterende behov.</span><span class="sxs-lookup"><span data-stu-id="88ca9-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="88ca9-127">Fakturerbart tidsforbrug</span><span class="sxs-lookup"><span data-stu-id="88ca9-127">Billable utilization</span></span>

<span data-ttu-id="88ca9-128">Ressourcer kan have et fakturerbart tidsforbrug for et mål.</span><span class="sxs-lookup"><span data-stu-id="88ca9-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="88ca9-129">Dette mål-tidsforbrug er enten defineret som en attribut i en ressources standardrolle eller angivet på posten for den individuelle, reserverbare ressource.</span><span class="sxs-lookup"><span data-stu-id="88ca9-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="88ca9-130">Beregningerne af tidsforbrug er baseret på det faktiske antal timer, som ressourcer har rapporteret ved hjælp af godkendte tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="88ca9-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="88ca9-131">Følgende formler bruges til at beregne forbrug:</span><span class="sxs-lookup"><span data-stu-id="88ca9-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="88ca9-132">Fakturerbart tidsforbrug = fakturerbare faktiske timer ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="88ca9-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="88ca9-133">Ikke-fakturerbar tidsforbrug = faktisk tid med faktureringstype-ID = ikke-fakturerbar, komplementær eller ikke tilgængelig ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="88ca9-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="88ca9-134">Intern = faktisk tid uden salgskontrakt ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="88ca9-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="88ca9-135">Ressourcekapacitet = ressourcens arbejdstimer – ikke til stede – fridage</span><span class="sxs-lookup"><span data-stu-id="88ca9-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="88ca9-136">Du kan finde visningen **Ressourceforbrug** i ruden **Ressourcer.**</span><span class="sxs-lookup"><span data-stu-id="88ca9-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Visningen Ressourceforbrug](media/Resource-Management-image65.png)

<span data-ttu-id="88ca9-138">Hver celle i gitteret repræsenterer den fakturerbare udnyttelsesprocent for ressourcen i en periode, f.eks. en dag, uge eller måned.</span><span class="sxs-lookup"><span data-stu-id="88ca9-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="88ca9-139">Følgende formler bruges til farvning af cellerne:</span><span class="sxs-lookup"><span data-stu-id="88ca9-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="88ca9-140">**Grøn:** Fakturerbart tidsforbrug \>= Resourcens måltidsforbrug</span><span class="sxs-lookup"><span data-stu-id="88ca9-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="88ca9-141">**Gul:** Mål-tidsforbrug – 20 \<= Fakturerbart tidsforbrug \< Mål-tidsforbrug</span><span class="sxs-lookup"><span data-stu-id="88ca9-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="88ca9-142">**Rød:** Fakturerbart tidsforbrug \< Mål-tidsforbrug – 20</span><span class="sxs-lookup"><span data-stu-id="88ca9-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="88ca9-143">Da visningen **Ressourceforbrug** er baseret på planlægningsområdet, kan du bruge filtreringsfunktionerne i planlægningsområdet til at filtrere resultaterne.</span><span class="sxs-lookup"><span data-stu-id="88ca9-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="88ca9-144">Gitteret kræver, at du angiver et mål-tidsforbrug for enten rolle eller den enkelte ressource.</span><span class="sxs-lookup"><span data-stu-id="88ca9-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="88ca9-145">Du konfigurerer dette ved at gå til **Ressourcer** \> **Ressourceroller**.</span><span class="sxs-lookup"><span data-stu-id="88ca9-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="88ca9-146">Derudover skal der tildeles en standardrolle til hver af de pågældende reserverbare ressourcer.</span><span class="sxs-lookup"><span data-stu-id="88ca9-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="88ca9-147">Gå til **Ressourcer** \> **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="88ca9-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="88ca9-148">På fanen **Project Service** skal du kontrollere, at der er defineret en ressourcerolle, og at feltet **Er standard** herfor er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="88ca9-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="88ca9-149">Du kan tilføje flere roller, hvor **Er standard =** nej.</span><span class="sxs-lookup"><span data-stu-id="88ca9-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="88ca9-150">Den rolle, hvor **Er standard = Ja**, bruges til at evaluere ressourcens tidsforbrug i forhold til destinationen for den pågældende rolle.</span><span class="sxs-lookup"><span data-stu-id="88ca9-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Standardrollesæt](media/Resource-Management-image67.png)

<span data-ttu-id="88ca9-152">På fanen **Project Service** kan du også angive en individuel mål-tidsforbrug for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="88ca9-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="88ca9-153">I beregningen af tidsforbruget bruger derefter denne mål-tidsforbrug til at evaluere ressourcens mål i stedet for målet for ressourcens standardrolle.</span><span class="sxs-lookup"><span data-stu-id="88ca9-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="88ca9-154">Tidsforbrug vises kun for en ressource, hvis den pågældende ressource har godkendt fakturerbar tid i løbet af den periode, der vises i gitteret.</span><span class="sxs-lookup"><span data-stu-id="88ca9-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="88ca9-155">Ressourcetilgængelighed</span><span class="sxs-lookup"><span data-stu-id="88ca9-155">Resource availability</span></span>

<span data-ttu-id="88ca9-156">Det er vigtigt, at personalechefer kan få vist tilgængeligheden af ressourcer og opdatere reservationer.</span><span class="sxs-lookup"><span data-stu-id="88ca9-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="88ca9-157">I visse tilfælde er der ingen formel efterspørgsel (ressourceanmodning), men ressourcestyringen skal reagere på et ikke-planlagt behov, der kommer gennem kanaler, f.eks. e-mail, telefonopkald eller onlinemeddelelse.</span><span class="sxs-lookup"><span data-stu-id="88ca9-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="88ca9-158">Personalechefer bruger planlægningsområdet til at opdatere ressourcer og reservationer.</span><span class="sxs-lookup"><span data-stu-id="88ca9-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="88ca9-159">Ressourcens arbejdstimer bruges som udgangspunkt for beregning af tilgængeligheden af en ressource.</span><span class="sxs-lookup"><span data-stu-id="88ca9-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="88ca9-160">Ressourcereservationer forbruger ressourcernes kapacitet.</span><span class="sxs-lookup"><span data-stu-id="88ca9-160">Resource bookings consume the capacity of the resources.</span></span>

![Planlægningsområde](media/Resource-Management-image68.png)

<span data-ttu-id="88ca9-162">I planlægningsområdet bruges farver og skygge til at vise reservationer, tilgængelighed og overreservationer samt statussen for reservationer.</span><span class="sxs-lookup"><span data-stu-id="88ca9-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="88ca9-163">En indstilling i indstillingerne for planlægningsområdet giver dig mulighed for at få vist en forklaring.</span><span class="sxs-lookup"><span data-stu-id="88ca9-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="88ca9-164">Hvis der vises en højrepil ud for en enkeltstående ressource i planlægningsområdet, kan ressourcen udvides til at få vist oplysninger om det arbejde, som ressourcen er reserveret til.</span><span class="sxs-lookup"><span data-stu-id="88ca9-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Reserverbar ressource udvidet på planlægningsområdet](media/Resource-Management-image69.png)

<span data-ttu-id="88ca9-166">Da Dynamics 365 Project Service Automation bruger Universal Resource Scheduling-programmet, og du også har Dynamics 365 Field Service installeret, kan du få vist oplysninger om ressourcereservationer for projekter, arbejdsordrer og andre objekter, som du har udvidet planlægningen til.</span><span class="sxs-lookup"><span data-stu-id="88ca9-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Oplysninger om ressourcereservationer for projekter og arbejdsordrer](media/Resource-Management-image70.png)

<span data-ttu-id="88ca9-168">Hvis du vil have vist flere oplysninger om en enkelt ressource, skal du højreklikke på den for at åbne ressourcekortet.</span><span class="sxs-lookup"><span data-stu-id="88ca9-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Ressourcekort](media/Resource-Management-image71.png)
