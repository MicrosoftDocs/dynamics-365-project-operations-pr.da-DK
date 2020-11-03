---
title: Navigation i brugergrænsefladen
description: Dette emne indeholder oplysninger om projektstyring i Dynamics 365 Project-operationer.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074090"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="b7748-103">Navigation i brugergrænsefladen</span><span class="sxs-lookup"><span data-stu-id="b7748-103">Navigating the user interface</span></span>

<span data-ttu-id="b7748-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b7748-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="b7748-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b7748-105">Overview</span></span>

<span data-ttu-id="b7748-106">Den primære projektformular er opdelt i flere faner.</span><span class="sxs-lookup"><span data-stu-id="b7748-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="b7748-107">De enkelte faner repræsenterer et andet detaljeringsniveau i projektet.</span><span class="sxs-lookup"><span data-stu-id="b7748-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="b7748-108">**Oversigt** : Angiver en beskrivelse af projektet og sammenfatter både projektets planlagte og faktiske præstation.</span><span class="sxs-lookup"><span data-stu-id="b7748-108">**Summary** : Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Oversigtsfane og felter](media/navigation7.png)

- <span data-ttu-id="b7748-110">**Opgaver** : Indeholder detaljer om arbejdsopgavehierarkiet, der repræsenteres af en gittervisning, en kortvisning og et Gantt-diagram.</span><span class="sxs-lookup"><span data-stu-id="b7748-110">**Tasks** : Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Opgavefane og felter](media/navigation8.png)

- <span data-ttu-id="b7748-112">**Team** : Indeholder oplysninger om projektdeltagere.</span><span class="sxs-lookup"><span data-stu-id="b7748-112">**Team** : Provides details regarding the project participants.</span></span> <span data-ttu-id="b7748-113">De enkelte teammedlemmers tildelte indsats opsummeres også i denne visning.</span><span class="sxs-lookup"><span data-stu-id="b7748-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Teamfane og felter](media/navigation9.png)

- <span data-ttu-id="b7748-115">**Ressourcetildelinger** : Indeholder en tidsfaseinddelt visning af indsatsen for hver ressource på et projekt.</span><span class="sxs-lookup"><span data-stu-id="b7748-115">**Resource assignments** : Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Fanen ressourcetildelinger og felter](media/navigation10.png)

- <span data-ttu-id="b7748-117">**Ressourceafstemning** : Angiver en tidsfaseinddelt visning af forskellene mellem tildelingerne af hver navngivet ressource og deres reservationer.</span><span class="sxs-lookup"><span data-stu-id="b7748-117">**Resource reconciliation** : Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Fanen ressourceafstemning og felter](media/navigation11.png)

- <span data-ttu-id="b7748-119">**Estimater** : Angiver en tidsfaseinddelt visning af omkostnings- og salgsestimater for et projekt.</span><span class="sxs-lookup"><span data-stu-id="b7748-119">**Estimates** : Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Fane for estimater og felter](media/navigation12.png)

- <span data-ttu-id="b7748-121">**Sporing** : Indeholder en visning, der viser opgavers fremgang i arbejdsopgavehierarkiet i forbindelse med indsats, omkostninger og salg.</span><span class="sxs-lookup"><span data-stu-id="b7748-121">**Tracking** : Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Sporingsfane og felter](media/navigation13.png)

- <span data-ttu-id="b7748-123">**Salg** : Indeholder dybdegående links til tilbud og kontrakter, der er knyttet til projektet.</span><span class="sxs-lookup"><span data-stu-id="b7748-123">**Sales** : Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="b7748-124">**Udgiftsestimater** : Indeholder et gitter, der definerer projektudgifter baseret på organisationens omkostningskategorier.</span><span class="sxs-lookup"><span data-stu-id="b7748-124">**Expense Estimates** : Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Fane for udgiftsestimater og felter](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="b7748-126">Gitterkontrolelementer</span><span class="sxs-lookup"><span data-stu-id="b7748-126">Grid controls</span></span>

<span data-ttu-id="b7748-127">Nedenstående er en kort oversigt over de typiske kontrolelementer, der findes under de forskellige projektplanlægningsfaner.</span><span class="sxs-lookup"><span data-stu-id="b7748-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="b7748-128">Opdater</span><span class="sxs-lookup"><span data-stu-id="b7748-128">Refresh</span></span>

<span data-ttu-id="b7748-129">**Opdatering** : Henter de nyeste data fra serveren, hvis der er foretaget ændringer, efter at gitteret blev indlæst.</span><span class="sxs-lookup"><span data-stu-id="b7748-129">**Refresh** : Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Knappen Opdater](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="b7748-131">Gruppér efter</span><span class="sxs-lookup"><span data-stu-id="b7748-131">Group by</span></span>

<span data-ttu-id="b7748-132">**Grupper efter** : Opdaterer grupperingen af rækkerne i gitteret for at afspejle enten ressourcer, roller eller kategorier, afhængigt af brugerens behov.</span><span class="sxs-lookup"><span data-stu-id="b7748-132">**Group by** : Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Grupper ved hjælp af knap](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="b7748-134">Forrige/næste</span><span class="sxs-lookup"><span data-stu-id="b7748-134">Previous/Next</span></span>

<span data-ttu-id="b7748-135">**Forrige**/**næste** : Opdater de synlige tidsperioder på tidsfaseinddelte gitre.</span><span class="sxs-lookup"><span data-stu-id="b7748-135">**Previous**/**Next** : Update the visible time periods on the time-phased grids.</span></span>

![Knapperne forrige og næste](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="b7748-137">Tidsskala</span><span class="sxs-lookup"><span data-stu-id="b7748-137">Timescale</span></span>

<span data-ttu-id="b7748-138">**Tidsskala** : Rediger sammenlægningen af tidsfaseinddelte data mellem dage, uger, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="b7748-138">**Timescale** : Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Tidsskalaknap](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="b7748-140">Udvid</span><span class="sxs-lookup"><span data-stu-id="b7748-140">Expand</span></span>

<span data-ttu-id="b7748-141">**Udvid** : Gengiv det synlige gitter til fuldskærmsvisning for at kunne se flere roller.</span><span class="sxs-lookup"><span data-stu-id="b7748-141">**Expand** : Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![knappen Udvid](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="b7748-143">Tidsfase efter</span><span class="sxs-lookup"><span data-stu-id="b7748-143">Time-phase by</span></span>

<span data-ttu-id="b7748-144">**Tidsfase efter** : Opdater grupperingen af rækkerne i gitteret for at afspejle omkostningsestimater for salgsestimater.</span><span class="sxs-lookup"><span data-stu-id="b7748-144">**Time-phase by** : Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="b7748-145">Dette kontrolelement finder også anvendelse på det estimerede script og sporingsgitteret.</span><span class="sxs-lookup"><span data-stu-id="b7748-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Knap til tidsfase efter](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="b7748-147">Tilføj kolonne</span><span class="sxs-lookup"><span data-stu-id="b7748-147">Add column</span></span>

<span data-ttu-id="b7748-148">**Tilføj kolonne** : Giver brugeren mulighed for at definere de synlige kolonner i gitteret.</span><span class="sxs-lookup"><span data-stu-id="b7748-148">**Add column** : Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="b7748-149">Det er kun de foruddefinerede kolonner, der kan tilføjes til gitrene i formularen **Projektplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="b7748-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Tilføj kolonneknap](media/navigation5.png)
