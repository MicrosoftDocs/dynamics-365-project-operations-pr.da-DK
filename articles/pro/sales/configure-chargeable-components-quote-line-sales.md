---
title: Konfigurer de fakturerbare komponenter i en tilbudslinje
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere fakturerbare og ikke-fakturerbare komponenter på en projektbaseret tilbudslinje.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858286"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="913dc-103">Konfigurer de fakturerbare komponenter i en tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="913dc-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="913dc-104">_**Gælder for:** Lille udrulning - aftale om proformafakturering, Project Operations for ressource/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="913dc-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="913dc-105">En projektbaseret tilbudslinje indeholder konceptet for *inkluderede* komponenter og *fakturerbare* komponenter.</span><span class="sxs-lookup"><span data-stu-id="913dc-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="913dc-106">Inkluderede komponenter er underlagt:</span><span class="sxs-lookup"><span data-stu-id="913dc-106">Included components are subject to:</span></span>

  - <span data-ttu-id="913dc-107">Faktureringsmetode og kundeopdelinger</span><span class="sxs-lookup"><span data-stu-id="913dc-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="913dc-108">Grænser, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="913dc-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="913dc-109">Indstillinger for fakturahyppighed, der er defineret på den projektbaserede tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="913dc-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="913dc-110">Et undersæt af de inkluderede komponenter kan markeres som fakturerbart ved hjælp af feltet **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="913dc-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="913dc-111">Feltet **Faktureringstype** er en grupperet indstilling, der gør det muligt at benytte følgende værdier i sammenhæng med en tilbudslinje:</span><span class="sxs-lookup"><span data-stu-id="913dc-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="913dc-112">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-112">Chargeable</span></span>
  - <span data-ttu-id="913dc-113">Ikke-fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-113">Non-chargeable</span></span>

<span data-ttu-id="913dc-114">Der kan defineres fakturerbare komponenter for opgaver, roller og transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="913dc-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="913dc-115">Fakturerbarheden defineres på opgaverne i en tilbudslinje og gælder for alle de transaktionsklasser, der er medtaget på den pågældende linje.</span><span class="sxs-lookup"><span data-stu-id="913dc-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="913dc-116">Hvis feltet **Medtag opgaver** er indstillet til **Hele projektet** eller er tomt, er fanen **Fakturerbare opgaver** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="913dc-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="913dc-117">Fakturerbarhed defineres på roller i en tilbudslinje og gælder kun for transaktionsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="913dc-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="913dc-118">Hvis feltet **Inkluder tid** er indstillet til **Nej** på en projekttilbudslinje, er fanen **Fakturerbare roller** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="913dc-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="913dc-119">Fakturerbarhed defineres på transaktionskategorier i en tilbudslinje og gælder kun for transaktionsklassen **Udgifter**.</span><span class="sxs-lookup"><span data-stu-id="913dc-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="913dc-120">Hvis feltet **Inkluder udgifter** er indstillet til **Nej** på en projekttilbudslinje, er fanen **Fakturerbare kategorier** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="913dc-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="913dc-121">Opdater en projektopgave for at gøre den fakturerbar eller ikke-fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="913dc-122">En projektopgave kan være fakturerbar eller ikke-fakturerbar i sammenhæng med en bestemt projektbaseret tilbudslinje, hvilket gør følgende opsætning mulig.</span><span class="sxs-lookup"><span data-stu-id="913dc-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="913dc-123">Hvis en projektbaseret tilbudslinje indeholder **Tid** og opgaven **T1**, knyttes opgaven til tilbudslinjen som fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="913dc-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="913dc-124">Hvis der findes en anden tilbudslinje, som indeholder **Udgifter**, kan du tilknytte opgaven **T1** på tilbudslinjen som ikke-fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="913dc-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="913dc-125">Resultatet er, at al den tid, der registreres på opgaven, er fakturerbar, og alle udgifter der registreres på opgaven er ikke-fakturerbare.</span><span class="sxs-lookup"><span data-stu-id="913dc-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="913dc-126">En opgaves faktureringstype kan konfigureres på fanen **Fakturerbare opgaver** for en projektbaseret tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Tilbudslinjeopgaver**.</span><span class="sxs-lookup"><span data-stu-id="913dc-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="913dc-127">Du kan også opdatere faktureringstypen for en projektopgave i feltet **Faktureringstype** i undergitteret for opsætningen af opgavefakturering for et projekt, som viser de tilbudslinjer, der er knyttede til en opgave.</span><span class="sxs-lookup"><span data-stu-id="913dc-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="913dc-128">Opdater en rolle til at være fakturerbar eller ikke-fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="913dc-129">En rolle kan være fakturerbar eller ikke-fakturerbar i relation til en bestemt projektbaseret tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="913dc-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="913dc-130">En rolles faktureringstype kan konfigureres på fanen **Fakturerbare roller** for en tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Fakturerbare roller**.</span><span class="sxs-lookup"><span data-stu-id="913dc-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="913dc-131">Opdater en transaktionskategori til at være fakturerbar eller ikke-fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="913dc-132">En transaktionskategori kan være fakturerbar eller ikke-fakturerbar på en bestemt tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="913dc-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="913dc-133">En transaktions faktureringstype kan konfigureres på fanen **Fakturerbare kategorier** for en tilbudslinje ved at opdatere feltet **Faktureringstype** i undergitteret for **Fakturerbare kategorier**.</span><span class="sxs-lookup"><span data-stu-id="913dc-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="913dc-134">Løs fakturerbarhed</span><span class="sxs-lookup"><span data-stu-id="913dc-134">Resolve chargeability</span></span>
<span data-ttu-id="913dc-135">En anslået eller faktisk oprettet tid kan kun opkræves, hvis:</span><span class="sxs-lookup"><span data-stu-id="913dc-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="913dc-136">**Tid** er inkluderet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="913dc-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="913dc-137">**Rolle** konfigureres som fakturerbar på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="913dc-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="913dc-138">**Inkluderede opgaver** angives til **Valgte opgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="913dc-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="913dc-139">Hvis disse tre ting er sande, konfigureres **Opgaven** også som fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="913dc-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="913dc-140">Et estimat eller en faktisk værdi, der oprettes for udgift, kan kun faktureres, hvis:</span><span class="sxs-lookup"><span data-stu-id="913dc-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="913dc-141">**Udgift** er inkluderet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="913dc-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="913dc-142">**Transaktionskategori** konfigureres som fakturerbar på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="913dc-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="913dc-143">**Inkluderede opgaver** angives til **Valgte opgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="913dc-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="913dc-144">Hvis disse tre ting er sande, konfigureres **Opgaven** også som fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="913dc-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="913dc-145">En anslået eller faktisk værdi, der er oprettet for materialer, kan kun faktureres, hvis:</span><span class="sxs-lookup"><span data-stu-id="913dc-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="913dc-146">**Materialer** er inkluderet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="913dc-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="913dc-147">**Inkluderede opgaver** angives til **Valgte opgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="913dc-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="913dc-148">Hvis disse to ting er sande, bør **Opgaven** også være konfigureret som fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="913dc-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="913dc-149">
                    <strong>Inkluderer tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="913dc-150">
                    <strong>Inkluderer udgifter</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="913dc-151">
                    <strong>Materialer er inkluderet</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="913dc-152">
                    <strong>Inkluderede opgaver</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-153">
                    <strong>Rolle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="913dc-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-155">
                    <strong>Opgave</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="913dc-156">
                    <strong>Indvirkning af fakturerbarhed</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-157">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-158">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-159">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-160">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="913dc-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-161">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-162">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-163">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-164">Fakturering af en faktisk værdi for tid: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-165">Faktureringstype på en faktisk værdi for en udgift: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-166">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="913dc-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-167">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-168">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-169">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-170">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="913dc-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-171">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-172">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-173">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-174">Fakturering af en faktisk værdi for tid: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-175">Faktureringstype på en faktisk værdi for en udgift: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-176">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="913dc-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-177">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-178">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-179">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-180">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="913dc-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-181">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-182">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-183">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-184">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-185">Faktureringstype på en faktisk værdi for en udgift: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-186">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="913dc-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-187">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-188">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-189">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-190">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="913dc-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-191">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-192">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-193">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-194">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-195">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-196">Faktureringstype på en faktisk værdi for materialer: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-197">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-198">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-199">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-200">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="913dc-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-201">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-202">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-203">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-204">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-205">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-206">Faktureringstype på en faktisk værdi for materialer: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-207">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-208">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-209">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-210">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="913dc-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-211">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="913dc-212">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-213">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-214">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-215">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-216">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="913dc-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="913dc-217">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-218">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-219">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-220">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="913dc-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-221">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="913dc-222">
                    <strong>Fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-223">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-224">Fakturering af en faktisk værdi for tid: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-225">Faktureringstype på en faktisk værdi for en udgift: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-226">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="913dc-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="913dc-227">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-228">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-229">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-230">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="913dc-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-231">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="913dc-232">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-233">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-234">Fakturering af en faktisk værdi for tid: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-235">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-236">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="913dc-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-237">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="913dc-238">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-239">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-240">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="913dc-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-241">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-242">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-243">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-244">Fakturering af en faktisk værdi for tid: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-245">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-246">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="913dc-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-247">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="913dc-248">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="913dc-249">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-250">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="913dc-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-251">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-252">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-253">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-254">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-255">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-256">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="913dc-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-257">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-258">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="913dc-259">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-260">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="913dc-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-261">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-262">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-263">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-264">Fakturering af en faktisk værdi for tid: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-265">Faktureringstype på en faktisk værdi for en udgift: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="913dc-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="913dc-266">Faktureringstype på en faktisk værdi for materialer: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="913dc-267">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="913dc-268">Ja</span><span class="sxs-lookup"><span data-stu-id="913dc-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="913dc-269">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="913dc-270">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="913dc-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="913dc-271">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="913dc-272">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="913dc-273">Kan ikke konfigureres</span><span class="sxs-lookup"><span data-stu-id="913dc-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="913dc-274">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-275">Faktureringstype på en faktisk værdi for en udgift:<strong> Ikke-fakturerbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="913dc-276">Faktureringstype på en faktisk værdi for materialer:<strong> Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="913dc-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
