---
title: Administrer ressourcer
description: Dette emne indeholder oplysninger om, hvordan du kan administrere ressourcer.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 1d47be6c11ced70b94b7497dfbc0c67d1a3f631b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274991"
---
# <a name="manage-resources"></a><span data-ttu-id="c2e1d-103">Administrer ressourcer</span><span class="sxs-lookup"><span data-stu-id="c2e1d-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c2e1d-104">Dynamics 365 Project Service Automation indeholder et ressourcestyringsdashboard, der giver en visuel oversigt over ressourcebehov og tidsforbrug i hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="c2e1d-105">Du kan bruge diagrammerne på dette dashboard til at få vist følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="c2e1d-106">**Ressourcekrav** – diagrammet **Aktive anmodninger om ressourcer** viser de ressourcer, der er sendt.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="c2e1d-107">Ressourcerne samles efter enten rolle eller projekt.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="c2e1d-108">**Ikke sendt ressourcekrav** – diagrammet **Ikke-tildelt ressourcekrav** viser alle de ressourcekrav, der ikke er blevet sendt.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="c2e1d-109">Den hjælper ressourcestyringen til at få vist krav, der ikke er faste, og som muligvis kan sendes via en anmodning om ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="c2e1d-110">**Fakturerbart tidsforbrug for sidste uge** – diagrammet **Tidsforbrug efter rolle** viser procentdelen af organisationens faktiske fakturerbare tidsforbrug efter rolle i forhold til målets fakturerbare tidsforbrug efter rolle.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c2e1d-111">Hvis du vil stille diagrammet **Tidsforbrug efter rolle** til rådighed, skal du oprette et jo, der kører i arbejdsprocessen UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="c2e1d-112">Dette tilbagevendende job kører hver 7. dag for at beregne fakturerbart tidsforbrug for de foregående syv dage.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="c2e1d-113">Resultaterne samles efter rolle.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="c2e1d-114">Administrere projektteammedlemmer</span><span class="sxs-lookup"><span data-stu-id="c2e1d-114">Manage project team members</span></span>

<span data-ttu-id="c2e1d-115">Projektledere kan bruge ressourcestyringsdashboardet til at styre ressourcer i projekter.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="c2e1d-116">De kan f.eks. føje et teammedlem direkte til et projekt og reservere et teammedlem for at opfylde de ressourcekrav, der er registreret af en generisk ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="c2e1d-117">Føje et teammedlem direkte til et projekt</span><span class="sxs-lookup"><span data-stu-id="c2e1d-117">Add a team member directly to a project</span></span>

<span data-ttu-id="c2e1d-118">Hvis du vil føje et teammedlem direkte til et projekt, skal du vælge **Ny** under fanen **Team** på siden **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="c2e1d-119">Dialogboksen **Hurtig oprettelse: Medlem af projektteam** vises.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="c2e1d-120">I denne dialogboks kan du udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="c2e1d-121">**Reservere en navngivet ressource** – vælg navnet på ressourcen i feltet **Reserverbar ressource**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="c2e1d-122">Vælg derefter rollen, angiv perioden, og vælg en fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="c2e1d-123">Den navngivne ressource, du har valgt, føjes til projektet ved hjælp af den valgte fordelingsmetode og ressourcekalenderen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="c2e1d-124">**Tilføj en generisk ressource** – undlad at udfylde feltet **Reserverbar ressource**, og vælg derefter rollen, angiv perioden, og vælg den ønskede fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="c2e1d-125">Der føjes en generisk ressource til teamet som en pladsholder for det kravsmønster, der bruges til at reservere navngivne ressourcer i teamet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="c2e1d-126">Kravet fremsættes i henhold til projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="c2e1d-127">**Føj en navngivet ressource til teamet uden at forbruge ressourcekapacitet** – vælg en ressource i feltet **Reserverbar ressource**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="c2e1d-128">Vælg derefter perioden, og vælg **Ingen** som allokeringsmetode.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="c2e1d-129">Ressourcen føjes til teamet, men ressourcens kapacitet forbruges ikke via en reservation.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="c2e1d-130">Reservere et teammedlem for at opfylde ressourcekravene for en generisk ressource</span><span class="sxs-lookup"><span data-stu-id="c2e1d-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="c2e1d-131">I PSA kan du reservere en generisk ressource i et projektteam, og du kan angive rollen, den nødvendige kapacitet og måden kapaciteten distribueres på.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="c2e1d-132">Du kan angive de attributter, der er knyttet til den generiske ressource, i ressourcekravet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="c2e1d-133">Disse attributter omfatter påkrævede færdigheder, den foretrukne organisationsenhed og de foretrukne ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="c2e1d-134">Følg disse trin for at angive de nødvendige færdigheder for en generisk ressource for en udvikler.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="c2e1d-135">Vælg **Ny** under fanen **Team** på siden **Projekter** for at reservere en generisk ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Generisk ressource, der er reserveret til teamet](media/Resource-Management-image9.png)

2. <span data-ttu-id="c2e1d-137">I kolonnen **Ressourcekrav** i visningen **Alle teammedlemmer** skal du vælge linket for at føje påkrævede færdigheder til den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Link til krav](media/Resource-Management-image10.png)

3. <span data-ttu-id="c2e1d-139">På siden **Ressourcekrav**, der vises, skal du i gitteret **Færdigheder** vælge ellipsen (**...**) og derefter vælge **Tilføj ny kravsegenskab** for at tilføje de påkrævede færdigheder for din udvikler.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Kommandoen Tilføj ny kravsegenskab](media/Resource-Management-image11.png)

4. <span data-ttu-id="c2e1d-141">I dialogboksen **Hurtig oprettelse: Kravsegenskab**, der vises, skal du vælge den påkrævede færdighed i feltet **Egenskab**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="c2e1d-142">Vælg derefter ressourcekundskabsniveauet for den pågældende færdighed i feltet **Klassificeringsværdi**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="c2e1d-143">Endelig skal du i feltet **Ressourcekrav** angive kravet til kildens ressourcer fra organisationsenheder eller endda navngivne ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="c2e1d-144">Vælg **Gem**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-144">When you've finished, select **Save**.</span></span>

    ![Hurtig oprettelse: dialogboksen Kravsegenskab](media/Resource-Management-image12.png)

5. <span data-ttu-id="c2e1d-146">Vælg **Reservér** på siden **Ressourcekrav** for at opfylde ressourcekravet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Reservér-knap på siden Ressourcekrav](media/Resource-Management-image13.png)

    <span data-ttu-id="c2e1d-148">Du kan også vælge den generiske ressource i gitteret **Alle teammedlemmer** og derefter vælge **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Knappen Reservér over gitteret Alle teammedlemmer](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="c2e1d-150">I dette eksempel er der behov for 40 timer, men der er ikke reserveret nogen timer, fordi generiske ressourcer ikke har reservationer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="c2e1d-151">Derudover er der ingen tildelte timer, da den generiske ressource blev føjet direkte til teamet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="c2e1d-152">Den blev ikke tilføjet ved hjælp af opgavetildeling.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="c2e1d-153">På siden **Planlægningsassistent** kan du filtrere tilgængelige ressourcer efter de krav, der er angivet i ressourcekravet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="c2e1d-154">Ressourcer sorteres i henhold til de sorteringsparametre, der er angivet i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Siden Planlægningsassistent](media/Resource-Management-image15.png)

    <span data-ttu-id="c2e1d-156">Her er nogle filtre, der ofte bruges:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="c2e1d-157">**Egenskaber sammen med en klassificering** – filtrér efter færdigheder, certificeringer og andre ressourcekvaliteter ud over klassificeringer af kompetence.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="c2e1d-158">**Roller** – filtrér efter de standardroller, der er tildelt de reserverbare ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="c2e1d-159">**Organisationsenheder** – filtrér de reserverbare ressourcer efter de organisationsenheder, de er tildelt til.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="c2e1d-160">Hvis du ikke er tilfreds med resultaterne af den første søgning efter krav, kan du ændre filterkriterierne.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="c2e1d-161">Udvid ruden **Filtervisning** til venstre, og vælg derefter **Søg** for at søge efter flere ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Ruden Filtervisning](media/Resource-Management-image16.png)

7. <span data-ttu-id="c2e1d-163">Hvis du vil ændre den måde, resultater sorteres på, skal du vælge **Sortér**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Kommandoen Sortér](media/Resource-Management-image17.png)

8. <span data-ttu-id="c2e1d-165">Vælg ressourcer i henhold til det behov, der er angivet for kravet som vist øverst i gitteret.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="c2e1d-166">Du kan fjerne markeringen af celler i gitteret og lade ressourcekapaciteten være åben.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="c2e1d-167">Det er kun muligt at markere én ressource ad gangen som reserveret.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="c2e1d-168">Vælg **Reservér** for at reservere den valgte ressource, og lad planlægningsområdet forblive åbent, så du kan vælge flere ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="c2e1d-169">Du kan også vælge **Reservér og luk** for at reservere den valgte ressource og lukke planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Ressource, der skal reserveres](media/Resource-Management-image19.png)

    <span data-ttu-id="c2e1d-171">Du modtager en meddelelse om besked om reserverede timer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="c2e1d-172">Behovsindikatorerne viser, hvor meget af reservationskravet der er opfyldt, og hvor meget der er tilbage.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="c2e1d-173">Du kan også se, hvor meget af den valgte ressources kapacitet, der er forbrugt.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="c2e1d-174">Vælg **Udvid** for at få vist flere detaljer om ressourcereservationer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="c2e1d-175">Vend tilbage til visningen **Alle teammedlemmer**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="c2e1d-176">Bemærk, at den generiske ressource er blevet erstattet af den navngivne ressource i gitteret, og at 40 timer vises som reserveret for den pågældende ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Opdateret Alle teammedlemmer-gitter](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="c2e1d-178">Der vises ingen tildelte timer, da de er reserveret direkte i teamet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="c2e1d-179">De blev ikke reserveret ved hjælp af opgavetildeling.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="c2e1d-180">Tildele generiske ressourcer til opgaver og oprette ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="c2e1d-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="c2e1d-181">I PSA kan du oprette opgaver og derefter tildele generiske ressourcer til dem.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="c2e1d-182">På denne måde kan ressourcebehov repræsenteres af pladsholdere, mens du vurderer din tidsplan og økonomiske tal.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="c2e1d-183">Du kan derefter oprette ressourcekrav for de generiske ressourcer og opfylde dem.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="c2e1d-184">På siden **Projekter** skal du vælge **Tilføj** under fanen **Tidsplan** for at oprette en opgave.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Ny opgave er oprettet](media/Resource-Management-image21.png)

2. <span data-ttu-id="c2e1d-186">Vælg symbolet for **Ressourcevælger** i feltet **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="c2e1d-187">Ressourcevælgeren vises og viser eksisterende teammedlemmer for projektet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Ressourcevælger](media/Resource-Management-image22.png)

3. <span data-ttu-id="c2e1d-189">Angiv navnet på den nye generiske ressource, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Navnet på en ny generisk ressource er angivet](media/Resource-Management-image23.png)

4. <span data-ttu-id="c2e1d-191">I dialogboksen **Hurtig oprettelse: Medlem af projektteam**, der vises, skal du i feltet **Rolle** vælge rollen for den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="c2e1d-192">I feltet **Ressourceenhed** skal du vælge organisationsenheden for den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="c2e1d-193">Vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-193">Then select **Save**.</span></span>

    ![Dialogboksen Hurtig oprettelse: Medlem af projektteam](media/Resource-Management-image24.png)

    <span data-ttu-id="c2e1d-195">Det generiske teammedlem tildeles nu til opgaven.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-195">The generic team member is now assigned to the task.</span></span>

    ![Generisk teammedlem, der er tildelt til opgaven.](media/Resource-Management-image25.png)

    <span data-ttu-id="c2e1d-197">Under fanen **Team** kan du se det nye generiske teammedlem.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="c2e1d-198">Bemærk, at det kun har tildelte timer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="c2e1d-199">Disse timer er summen af alle opgaver, der er tildelt til det generiske teammedlem.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="c2e1d-200">Det generiske teammedlem har endnu ikke de påkrævede timer eller et ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Generisk teammedlem under fanen Team](media/Resource-Management-image26.png)

5. <span data-ttu-id="c2e1d-202">Du kan nu tildele det generiske teammedlem til andre opgaver ved hjælp af ressourcevælgeren.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Generisk teammedlem i ressourcevælgeren](media/Resource-Management-image27.png)

    <span data-ttu-id="c2e1d-204">Når du er færdig med at tildele den generiske ressource til opgaver, kan du oprette et ressourcekrav for den generiske ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="c2e1d-205">Vælg den generiske ressource, og vælg derefter **Generer krav** under fanen **Team**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Kommandoen Generer krav](media/Resource-Management-image28.png)

    <span data-ttu-id="c2e1d-207">Når behovet er genereret, har det generiske teammedlem de nødvendige timer og et link til ressourcebehovet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Link til ressourcekrav](media/Resource-Management-image29.png)

    <span data-ttu-id="c2e1d-209">Når du har reserveret en navngivet ressource, fjernes den generiske ressource fra teamet og erstattes af den navngivne ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Generisk ressource, der er erstattet af den navngivne ressource](media/Resource-Management-image30.png)

    <span data-ttu-id="c2e1d-211">Under fanen **Tidsplan** fjernes de generiske ressourcetildelinger og erstattes med den navngivne ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Generiske ressourcetildelinger erstattet med den navngivne ressource under fanen Tidsplan](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="c2e1d-213">Denne funktionsmåde forekommer kun, når en navngivet ressource er helt reserveret til det generiske ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="c2e1d-214">Når en navngivet ressource delvist erstatter det generiske ressourcekrav, eller hvis flere navngivne ressourcer erstatter det generiske ressourcekrav, forbliver den generiske ressource tildelt til opgaven.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="c2e1d-215">I følgende illustration er der planlagt en 80 timers opgave med en varighed på fem dage (16 timer pr. dag over fem dage), og den er tildelt den generiske ressource med navnet **Funktionelt**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Fem dages opgave med 80 timer tildelt til den generiske ressource Funktionelt](media/Resource-Management-image32.png)

    <span data-ttu-id="c2e1d-217">Når du opretter kravet, er det for 80 timer fordelt over fem dage.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Krav, der er oprettet for 80 timer fordelt over fem dage](media/Resource-Management-image33.png)

    <span data-ttu-id="c2e1d-219">Da tilgængelige ressourcer kun arbejder otte timer om dagen, skal der bruges to ressourcer til at imødekomme behovet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Anden ressource](media/Resource-Management-image35.png)

    <span data-ttu-id="c2e1d-221">Under fanen **Team** kan du nu se, at den generiske ressource ikke har nogen påkrævede timer, men de tildelte timer vises stadig sammen med de to navngivne ressourcer, der udgør indfrielsen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![To navngivne ressourcer under fanen Team](media/Resource-Management-image36.png)

    <span data-ttu-id="c2e1d-223">Under fanen **Tidsplan** forbliver den generiske ressource tildelt til opgaven.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Generiske ressourcer under fanen Tidsplan](media/Resource-Management-image37.png)

<span data-ttu-id="c2e1d-225">PSA tildeler ikke begge ressourcer til opgaven, da denne funktionsmåde ville resultere i en mindre forudsigelig tidsplan.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="c2e1d-226">I dette enkle eksempel er det nemt at opdele timerne ligeligt mellem to ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="c2e1d-227">I mere komplekse scenarier, der omfatter flere opgaver og flere ressourcer, ville PSA dog være nødt til at antage, hvordan de reservationer, der modtages for flere ressourcer, skal fordeles hen over flere opgaver.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="c2e1d-228">I disse scenarier er projektlederen derfor ansvarlig for at analysere flere reservationer og tildele dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="c2e1d-229">For at kunne fordele reservationerne tildeler projektlederen opgaverne fra de generiske ressourcer til de navngivne ressourcer og bruger derefter visningen **Afstemning** til at sikre, at fordelingen fungerer sammen med reservationerne.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="c2e1d-230">Redigere et ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="c2e1d-230">Edit a resource requirement</span></span>

<span data-ttu-id="c2e1d-231">Når der er oprettet et ressourcekrav, vil en projektleder eller ressourcestyring muligvis redigere oplysningerne for at begrænse søgekriterierne, når planlægningsområdet bruges.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="c2e1d-232">Benyt følgende fremgangsmåde for at redigere ressourcekravet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="c2e1d-233">Vælg linket til et vilkårligt krav for en generisk ressource under fanen **Team** på siden **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="c2e1d-234">På siden **Ressourcekrav**, der vises, kan du opdatere flere attributter.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="c2e1d-235">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-235">Here are some examples:</span></span>

    - <span data-ttu-id="c2e1d-236">Navn</span><span class="sxs-lookup"><span data-stu-id="c2e1d-236">Name</span></span>
    - <span data-ttu-id="c2e1d-237">Fra-dato</span><span class="sxs-lookup"><span data-stu-id="c2e1d-237">From Date</span></span>
    - <span data-ttu-id="c2e1d-238">Til-dato</span><span class="sxs-lookup"><span data-stu-id="c2e1d-238">To Date</span></span>
    - <span data-ttu-id="c2e1d-239">Varighed</span><span class="sxs-lookup"><span data-stu-id="c2e1d-239">Duration</span></span>
    - <span data-ttu-id="c2e1d-240">Ressourcetype</span><span class="sxs-lookup"><span data-stu-id="c2e1d-240">Resource Type</span></span>

<span data-ttu-id="c2e1d-241">På siden **Ressourcekrav** kan projektlederen eller ressourcestyring også definere følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="c2e1d-242">Færdigheder</span><span class="sxs-lookup"><span data-stu-id="c2e1d-242">Skills</span></span>
- <span data-ttu-id="c2e1d-243">Roller</span><span class="sxs-lookup"><span data-stu-id="c2e1d-243">Roles</span></span>
- <span data-ttu-id="c2e1d-244">Ressourcepræferencer</span><span class="sxs-lookup"><span data-stu-id="c2e1d-244">Resource preferences</span></span>
- <span data-ttu-id="c2e1d-245">Foretrukket organisationsenhed</span><span class="sxs-lookup"><span data-stu-id="c2e1d-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="c2e1d-246">Opdatere ressourcereservationer, efter at de er reserveret til et projekt</span><span class="sxs-lookup"><span data-stu-id="c2e1d-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="c2e1d-247">Når du har føjet en generisk eller navngivet ressource til et projektteam, kan du ændre ressourcens reservationer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="c2e1d-248">På siden **Projekter** skal du under fanen **Team** vælge et teammedlem og derefter vælge **Vedligehold reservationer**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Planlægningsområde, der er åbnet for det valgte teammedlem](media/Resource-Management-image40.png)

    <span data-ttu-id="c2e1d-250">Planlægningsområdet vises og angiver projektteammedlemmets reservationer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="c2e1d-251">Udvid teammedlemmets post for at få vist de timer, der er reserveret i forhold til dette projekt og andre projekter, der forbruger teammedlemmets kapacitet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="c2e1d-252">Markér reservationen, og træk den, så den udvides eller forkortes.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="c2e1d-253">Dialogboksen **Opret ressourcereservation** vises, hvor du kan justere reservationen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dialogboksen Opret ressourcereservation](media/Resource-Management-image41.png)

3. <span data-ttu-id="c2e1d-255">Højreklik på reservationen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-255">Right-click the booking.</span></span> <span data-ttu-id="c2e1d-256">Du kan derefter bruge genvejsmenuen til at fuldføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="c2e1d-257">Ændre reservationens status.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-257">Change the booking status.</span></span>
    - <span data-ttu-id="c2e1d-258">Redigere reservationen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-258">Edit the booking.</span></span>
    - <span data-ttu-id="c2e1d-259">Erstatte en ressource i projektteamet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="c2e1d-260">Ændre reservationens status</span><span class="sxs-lookup"><span data-stu-id="c2e1d-260">Change the booking status</span></span>

<span data-ttu-id="c2e1d-261">Du kan ændre en hvilken som helst standardreservationsstatus eller brugerdefineret reservationsstatus.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-261">You can change any default or custom booking status.</span></span>

![Kommandoen Skift status](media/Resource-Management-image42.png)

<span data-ttu-id="c2e1d-263">Følgende statusser findes i PSA:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="c2e1d-264">**Annulleret** – denne status annullerer en ressources reservation og frigør ressourcens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="c2e1d-265">**Reservér definitivt** – denne status forbruger en ressources kapacitet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="c2e1d-266">En reservation har som regel denne status, når du åbner **Vedligehold reservationer** i gitteret **Alle teammedlemmer** på siden **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="c2e1d-267">**Reservér foreløbigt** – denne status føjer en ressource til et team, men forbruger ikke ressourcens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="c2e1d-268">Det angiver, at ressourcen er reserveret til potentielt arbejde, men stadig har kapacitet, hvis det kræves til andre job.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="c2e1d-269">I visningen af den samlede ressourcetilgængelighed har foreløbige reservationer en anden status end definitive reservationer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="c2e1d-270">**Foreslået** – denne status repræsenterer ressourcestyrings eller projektleders forslag til en ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="c2e1d-271">Forslag forbruger ikke en ressources kapacitet, og ressourcen føjes ikke til projektteamet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="c2e1d-272">For at reservere ressourcen definitivt i teamet skal projektlederen acceptere forslaget.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="c2e1d-273">Sende anmodninger om ressourcer</span><span class="sxs-lookup"><span data-stu-id="c2e1d-273">Submit resource requests</span></span>

<span data-ttu-id="c2e1d-274">Anmodninger om ressourcer bruges til at overføre behovet (ressourcekrav), der skal opfyldes af ressourcestyring.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="c2e1d-275">I forbindelse med en generisk ressource, som allerede findes i teamet, kan du sende en anmodning om ressource direkte.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="c2e1d-276">En anmodning om ressource kan opfyldes på to måder:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="c2e1d-277">Ressourcestyring opfylder anmodningen direkte.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="c2e1d-278">I dette tilfælde erstattes den generiske ressource med en definitiv reservation, der har en navngivet ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="c2e1d-279">Ressourcestyring foreslår en ressource til projektlederen, og projektlederen godkender eller afviser den foreslåede ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="c2e1d-280">Direkte opfyldelse af ressourceanmodninger</span><span class="sxs-lookup"><span data-stu-id="c2e1d-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="c2e1d-281">Når der genereres et ressourcekrav, kan en projektleder sende en ressourceanmodning om en generisk ressource ved at markere ressourcen og derefter vælge **Send anmodning**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Knappen Send anmodning](media/Resource-Management-image45.png)

<span data-ttu-id="c2e1d-283">Kommentarer til ressourcen kan gives til ressourcestyringen, der opfylder anmodningen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="c2e1d-284">Når anmodningen er sendt, ændres feltet **Status** for teammedlemmet til **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Indtastning af valgfrie kommentarer](media/Resource-Management-image46.png)

<span data-ttu-id="c2e1d-286">Når ressourcestyringen opfylder anmodningen, erstattes det generiske teammedlem af den navngivne ressource i gitteret **Alle teammedlemmer**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Generisk teammedlem erstattet med den navngivne ressource i gitteret Alle teammedlemmer](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="c2e1d-288">Bruge et ressourceforslag til ressourceanmodninger</span><span class="sxs-lookup"><span data-stu-id="c2e1d-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="c2e1d-289">I stedet for at reservere en ressource direkte i en anmodning om ressource kan ressourcestyring foreslå en ressource til projektlederen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="c2e1d-290">En ressourcestyring kan bruge denne indstilling, når der ikke findes et nøjagtigt match med kravene.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="c2e1d-291">Når ressourcestyring foreslår en ressource, kan projektlederen se, at feltet **Status** for det generiske teammedlem ændres til **Skal gennemses**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Generisk teammedlems status er ændret til Skal gennemses](media/Resource-Management-image48.png)

<span data-ttu-id="c2e1d-293">Hvis du vil have vist den foreslåede ressource sammen med en visualisering af effekten af reservationen for tilbuddet, skal du dobbeltklikke på det teammedlem, der har statussen **Skal gennemses**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="c2e1d-294">Vælg derefter fanen **Foreslåede ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-294">Then select the **Proposed Resources** tab.</span></span>

![Fanen Foreslåede ressourcer](media/Resource-Management-image49.png)

<span data-ttu-id="c2e1d-296">Vælg **Acceptér alle forslag** for at acceptere alle foreslåede ressourcer eller **Afvis alle forslag** for at afvise dem.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="c2e1d-297">Hvis du accepterer de foreslåede ressourcer, bliver de definitivt reserveret til projektet som teammedlemmer og erstatter de generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="c2e1d-298">Du skal enten acceptere eller afvise alle foreslåede ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="c2e1d-299">Du kan ikke acceptere eller afvise dem delvist.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="c2e1d-300">Erstatte en ressource i projektteamet</span><span class="sxs-lookup"><span data-stu-id="c2e1d-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="c2e1d-301">En projektleder må undertiden erstatte et reserveret teammedlem i et projekt.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="c2e1d-302">På siden **Projekter** skal du under fanen **Team** vælge den ressource, der skal erstattes, og derefter vælge **Vedligehold reservationer**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="c2e1d-303">Udvid ressourcen for at få vist de projekter, den er tildelt til.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Udvidet ressourcen, der viser tildelte projekter](media/Resource-Management-image50.png)

3. <span data-ttu-id="c2e1d-305">Højreklik på projektet, og vælg derefter **Erstat ressource**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="c2e1d-306">Hvis du ved, hvilken ressource du vil bruge som erstatning for den aktuelle ressource, skal du vælge eller skrive navnet og derefter vælge **Tildel igen**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Angive en erstatningsressource](media/Resource-Management-image51.png)

    <span data-ttu-id="c2e1d-308">Du kan også benytte denne fremgangsmåde for at søge efter en ressource:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="c2e1d-309">Vælg **Find erstatning**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-309">Select **Find Substitution**.</span></span>

        ![Søgning efter en erstatningsressource](media/Resource-Management-image52.png)

        <span data-ttu-id="c2e1d-311">Planlægningsassistenten returnerer en liste over tilgængelige erstatninger.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="c2e1d-312">I planlægningsassistenten kan du filtrere de tilgængelige ressourcer yderligere for at finde en passende erstatning.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Liste over tilgængelige erstatninger](media/Resource-Management-image53.png)

    2. <span data-ttu-id="c2e1d-314">Når du vil erstatte ressourcen, skal du vælge den ressource, du vil bruge, og derefter vælge **Erstat**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Erstatningsressource valgt](media/Resource-Management-image54.png)

    <span data-ttu-id="c2e1d-316">Reservationerne og tildelingerne erstattes med den nye ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Reservationer og tildelinger erstattet med den nye ressource](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="c2e1d-318">Afstemme teammedlemmers reservationer og tildelinger</span><span class="sxs-lookup"><span data-stu-id="c2e1d-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="c2e1d-319">For teammedlemmer er reservationer og tildelinger løst sammenkædet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="c2e1d-320">Med andre ord kan ressourcer have tildelinger men ingen reservationer, eller de kan have reservationer men ingen tildelinger.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="c2e1d-321">Ideelt set skal reservationer og tildelinger justeres, så ressourcer har bindende kapacitet til at udføre opgavetildelingerne.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="c2e1d-322">Reservationerne kan dog muligvis være baseret på tilgængelighed, og opgavetidspunkter kan ændres, efterhånden som projektet fortsætter.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="c2e1d-323">Derfor giver den løse sammenkædning mellem reservationer og tildelinger fleksibilitet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="c2e1d-324">PSA har fanen **Afstemning**, som projektledere kan bruge til at afstemme teammedlemmernes reservationer og tildelinger af disse til projektgrupper.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Fanen Afstemning](media/Resource-Management-image56.png)

<span data-ttu-id="c2e1d-326">Fanen **Afstemning** viser reservationer og tildelinger helt ned til niveauet for de enkelte opgavetildelinger for hvert teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="c2e1d-327">Den viser timer i celler, der repræsenterer tidsperioder fra måneder ned til dage.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="c2e1d-328">Under fanen vises også en samlet netto i alt for projektet sammen med en kolonnetotal.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="c2e1d-329">For hver ressource beregner fanen forskellen mellem teammedlemmets reservationer og en akkumulering af teammedlemmets opgavetildelinger.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="c2e1d-330">Ideelt skal forskellen være 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="c2e1d-331">Det vil sige, at der ikke bør være nogen forskel mellem reservationer og tildelinger.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="c2e1d-332">Forskelle er farvede og nedtonede for at henlede opmærksomheden på to forhold:</span><span class="sxs-lookup"><span data-stu-id="c2e1d-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="c2e1d-333">**Manglende reservation** – der opstår manglende reservation, når en ressource har flere tildelinger end reservationer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="c2e1d-334">Da denne kapacitet ikke er reserveret, vil en projektleder muligvis rette dette forhold ved at forlænge reservationer af ressourcen for at dække underskuddet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="c2e1d-335">**Overskydende reservationer** – Der forekommer overskydende reservationer, når en ressource er blevet reserveret til projektet, men ikke er tildelt opgaver.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="c2e1d-336">Dette forhold kan være acceptabelt i de tilfælde, hvor ressourcen blev reserveret til projektet, før opgavetildeling fandt sted.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="c2e1d-337">I andre tilfælde er ressourcen dog ikke planlagt til at blive tildelt til opgaver.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="c2e1d-338">I disse tilfælde skal projektlederen overveje at annullere reservationerne af ressourcen, så kapaciteten kan bruges til et andet projekt.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="c2e1d-339">Når du i visse tilfælde får vist tiden på et højere niveau end dagsniveau (f.eks. månedsniveau), kan du muligvis se en nettoforskel på nul for en ressource (med andre ord reservationer = tildelinger).</span><span class="sxs-lookup"><span data-stu-id="c2e1d-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="c2e1d-340">Men hvis du får vist tiden på ugeniveau, kan du muligvis se, at der er tildelinger på 0 timer og reservationer på 40 timer i den første uge, men tildelinger på 40 timer og reservationer på nul timer i løbet af den anden uge.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="c2e1d-341">Generelt afstemmes reservationerne og tildelingerne, men de er forskellige fra den ene uge til den næste.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="c2e1d-342">Når du får vist tiden på højere niveauer, har fanen **Afstemning** en indikator, der giver dig besked om, at der er forskelle på lavere niveauer.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="c2e1d-343">Når du dobbeltklikker på en celle, kan du zoome ind for at få vist forskellen.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="c2e1d-344">Du kan derefter højreklikke for at zoome ud. Hvis du vælger en ressource og derefter bruger kontrolelementet **Næste difference** på værktøjslinjen for gitteret, kan du gå til den næste forskel mellem reservationer og tildelinger for den pågældende ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="c2e1d-345">Du kan derefter bruge kontrolelementet **Forrige difference** til at gå tilbage.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="c2e1d-346">Du kan også slå differenceindikatoren og funktionsmåden for navigation fra under **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Differenceindikator](media/Resource-Management-image57.png)

<span data-ttu-id="c2e1d-348">Hvis du har opgavetildelinger for en ressource men ingen reservationer, skal du under fanen **Afstemning** på siden **Projekter** vælge den manglende reservation og derefter vælge **Udvid reservation**.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="c2e1d-349">Dialogboksen **Udvid reservation** vises og angiver den reservation, der skal bruges for at løse manglen på ressource.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="c2e1d-350">Den viser også ressourcens eksisterende reservationer på tværs af alle projekter eller andre objekter, der kan planlægges.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="c2e1d-351">Hvis du vælger **OK** for at oprette reservationen for ressourcen, uanset den pågældende ressources tilgængelighed, kan det medføre overreservation.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dialogboksen Udvid reservation](media/Resource-Management-image58.png)

<span data-ttu-id="c2e1d-353">Projektlederen eller ressourcestyringen kan derefter bruge planlægningsområdet til at administrere de situationer, hvor en ressource overreserveres i forhold til dens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="c2e1d-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]