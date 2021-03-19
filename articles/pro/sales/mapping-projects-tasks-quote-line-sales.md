---
title: Tilknyt projekter og opgaver til en projektbaseret tilbudslinje
description: Dette emne indeholder oplysninger om, hvordan du knytter projekter og opgaver til en projektbaseret opgavelinje.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272741"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="3f59a-103">Tilknyt projekter og opgaver til en projektbaseret tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="3f59a-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="3f59a-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3f59a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3f59a-105">På projektbaserede tilbudslinjer kan du tilknytte de specifikke opgaver for et projekt, der allerede er knyttet til en tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="3f59a-106">Når du knytter opgaver til en tilbudslinje, finder følgende elementer, du har defineret på tilbudslinjen, kun anvendelse for de pågældende opgaver:</span><span class="sxs-lookup"><span data-stu-id="3f59a-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="3f59a-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="3f59a-107">Billing method</span></span>
- <span data-ttu-id="3f59a-108">Indstillinger for fakturerbarhed</span><span class="sxs-lookup"><span data-stu-id="3f59a-108">Chargeability options</span></span>
- <span data-ttu-id="3f59a-109">Grænser, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="3f59a-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="3f59a-110">Kunder</span><span class="sxs-lookup"><span data-stu-id="3f59a-110">Customers</span></span>

<span data-ttu-id="3f59a-111">Du kan f.eks. have et projekt, hvor den ene fase er fast pris, og alle andre faser er tid og materialer.</span><span class="sxs-lookup"><span data-stu-id="3f59a-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="3f59a-112">I dette tilfælde kan du knytte den første fase og alle dens underordnede opgaver til tilbudslinjen for den pågældende fase med en fast pris-faktureringsmetode.</span><span class="sxs-lookup"><span data-stu-id="3f59a-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="3f59a-113">Derefter kan du knytte alle de andre faser til den tids- og materialebaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="3f59a-114">Tilknyt opgaver til projektbaserede tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="3f59a-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="3f59a-115">Du kan tilknytte opgaver til tilbudslinjer fra følgende placeringer:</span><span class="sxs-lookup"><span data-stu-id="3f59a-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="3f59a-116">Siden **Projekt** > fanen **Opgavefakturering** (optimal)</span><span class="sxs-lookup"><span data-stu-id="3f59a-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="3f59a-117">Siden **Tilbudslinje** > fanen **Fakturerbare opgaver**</span><span class="sxs-lookup"><span data-stu-id="3f59a-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="3f59a-118">Fra projektsiden</span><span class="sxs-lookup"><span data-stu-id="3f59a-118">From the Project page</span></span>

<span data-ttu-id="3f59a-119">På siden **Projekt** får du den optimale oplevelse, når du knytter opgaver til tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="3f59a-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="3f59a-120">Du kan bruge denne side til at vælge flere opgaver og knytte dem alle samt deres underordnede opgaver til den valgte tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="3f59a-121">På en projektbaseret tilbudslinjes fane **Generelt** kan du verificere, at feltet **Projekt** er udfyldt.</span><span class="sxs-lookup"><span data-stu-id="3f59a-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="3f59a-122">I feltet **Medtag opgaver** skal du vælge **Kun valgte opgaver**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="3f59a-123">Gem den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-123">Save the project-based quote line.</span></span> <span data-ttu-id="3f59a-124">Når formularen opdateres, vises fanen **Fakturerbare opgaver**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="3f59a-125">På fanen **Generelt** skal du vælge linket til projektet fra feltet **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="3f59a-126">På siden **Projekt** skal du vælge fanen **Opgavefakturering**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="3f59a-127">I det andet gitter, der gælder for opgavespecifik faktureringsopsætning, skal du vælge en eller flere opgaver og derefter vælge **Tilknyt tilbudslinjer**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="3f59a-128">Vælg en tilbudslinje, der viser projektbaserede tilbudslinjer på tilbuddet, på den dialogside, der vises.</span><span class="sxs-lookup"><span data-stu-id="3f59a-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="3f59a-129">I feltet **Faktureringstype** skal du angive, om disse opgaver er fakturerbare eller ikke-fakturerbare.</span><span class="sxs-lookup"><span data-stu-id="3f59a-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="3f59a-130">Markér afkrydsningsfeltet for at angive, om tilknytningen skal omfatte underordnede opgaver for de valgte opgaver.</span><span class="sxs-lookup"><span data-stu-id="3f59a-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="3f59a-131">Hvis du markerer afkrydsningsfeltet, knyttes de underordnede opgaver for de valgte opgaver til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="3f59a-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="3f59a-132">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3f59a-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="3f59a-133">Fra tilbudslinjesiden</span><span class="sxs-lookup"><span data-stu-id="3f59a-133">From the Quote line page</span></span>

<span data-ttu-id="3f59a-134">Du kan knytte projektopgaver til tilbudslinjer fra fanen **Fakturerbare opgaver** på siden **Tilbudslinje**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="3f59a-135">Det optimale sted at knytte projektopgaver til tilbudslinjer findes under fanen **Opgavefakturering** på **Projekt**-siden.</span><span class="sxs-lookup"><span data-stu-id="3f59a-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="3f59a-136">Hvis du knytter opgaver til fanen **Fakturerbare opgaver** på siden med **Tilbudslinje**, skal du tilknytte hvert enkelt projekt manuelt.</span><span class="sxs-lookup"><span data-stu-id="3f59a-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="3f59a-137">På en projektbaseret tilbudslinjes fane **Generelt** kan du verificere, at der er valgt et projekt i feltet **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="3f59a-138">I feltet **Medtag opgaver** skal du vælge **Kun valgte opgaver**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="3f59a-139">Gem den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-139">Save the project-based quote line.</span></span> <span data-ttu-id="3f59a-140">Når formularen opdateres, vises fanen **Fakturerbare opgaver**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="3f59a-141">På fanen **Fakturerbare opgaver** skal du vælge **Tilføj en tilbudslinjeopgave**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="3f59a-142">På siden **Tilbudslinjeopgave** skal du i feltet **Opgaver** markere opgaven, og i feltet **Faktureringstype** skal du vælge **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="3f59a-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3f59a-143">Close the page.</span></span> <span data-ttu-id="3f59a-144">Den valgte opgave er nu knyttet til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="3f59a-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="3f59a-145">Fjer tilknytning mellem opgaver og projektbaserede tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="3f59a-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="3f59a-146">Fra projektsiden</span><span class="sxs-lookup"><span data-stu-id="3f59a-146">From the Project page</span></span>

<span data-ttu-id="3f59a-147">Denne metode giver dig den mest optimale oplevelse, når du fjerner tilknytningen mellem opgaver og tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="3f59a-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="3f59a-148">Du kan vælge flere opgaver og fjerne tilknytningen for dem alle samt deres underordnede opgaver til den valgte tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="3f59a-149">På en projektbaseret tilbudslinjes fane **Generelt** kan du i feltet **Projekt** vælge projektlinket.</span><span class="sxs-lookup"><span data-stu-id="3f59a-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="3f59a-150">På siden **Projekt** skal du vælge fanen **Opgavefakturering**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="3f59a-151">I det andet gitter, der gælder for opgavespecifik faktureringsopsætning, skal du vælge en eller flere opgaver og derefter vælge **Fjern tilknytning til tilbudslinjer**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="3f59a-152">Vælg en tilbudslinje på den viste dialogside.</span><span class="sxs-lookup"><span data-stu-id="3f59a-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="3f59a-153">Markér afkrydsningsfeltet for at angive, hvorvidt tilknytningen også skal fjernes fra underordnede opgaver for de valgte opgaver.</span><span class="sxs-lookup"><span data-stu-id="3f59a-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="3f59a-154">Hvis du markerer afkrydsningsfeltet, fjernes tilknytningen mellem de underordnede opgaver for de valgte opgaver og tilbudslinjen også.</span><span class="sxs-lookup"><span data-stu-id="3f59a-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="3f59a-155">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-155">Select **OK**.</span></span> <span data-ttu-id="3f59a-156">Der vises en advarsel om, at hvis du fjerner denne tilknytning, kan de faktiske oplysninger, der tidligere er registreret for opgaven, blive tilbageført.</span><span class="sxs-lookup"><span data-stu-id="3f59a-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="3f59a-157">Vælg **OK** for at fortsætte og fjerne tilknytningen mellem opgaven og den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="3f59a-158">Fra tilbudslinjesiden</span><span class="sxs-lookup"><span data-stu-id="3f59a-158">From the Quote line page</span></span>

<span data-ttu-id="3f59a-159">Du kan også fjerne tilknytningen mellem projektopgaver og tilbudslinjer fra fanen **Fakturerbare opgaver** på siden **Tilbudslinje**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="3f59a-160">På fanen **Fakturerbare opgaver** skal du vælge **Slet en tilbudslinjeopgave**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="3f59a-161">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f59a-161">Select **OK**.</span></span> <span data-ttu-id="3f59a-162">Der vises en advarsel om, at hvis du fjerner denne tilknytning, kan de faktiske oplysninger, der tidligere er registreret for opgaven, blive tilbageført.</span><span class="sxs-lookup"><span data-stu-id="3f59a-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="3f59a-163">Vælg **OK** for at fortsætte og fjerne tilknytningen mellem opgaven og den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="3f59a-164">Denne procedure sletter ikke opgaven fra projektet.</span><span class="sxs-lookup"><span data-stu-id="3f59a-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="3f59a-165">Det er kun opgavetilknytningen, der fjernes fra den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3f59a-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]