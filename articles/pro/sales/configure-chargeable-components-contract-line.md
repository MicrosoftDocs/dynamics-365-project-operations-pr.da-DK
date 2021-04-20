---
title: Konfigurer fakturerbare komponenter i en projektbaseret kontraktlinje
description: Dette emne indeholder oplysninger om, hvordan du tilføjer fakturerbare komponenter til kontraktlinjer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858466"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="6e783-103">Konfigurer fakturerbare komponenter i en projektbaseret kontraktlinje</span><span class="sxs-lookup"><span data-stu-id="6e783-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="6e783-104">_**Gælder for:** Lille udrulning - aftale om proformafakturering, Project Operations for ressource/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="6e783-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6e783-105">En projektbaseret kontraktlinje har *inkluderede* komponenter og *fakturerbare* komponenter.</span><span class="sxs-lookup"><span data-stu-id="6e783-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="6e783-106">Inkluderede komponenter er komponenter, der er underlagt:</span><span class="sxs-lookup"><span data-stu-id="6e783-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="6e783-107">Faktureringsmetode og kundeopdelinger</span><span class="sxs-lookup"><span data-stu-id="6e783-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="6e783-108">Grænser, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="6e783-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="6e783-109">Indstillinger for fakturahyppighed, der er defineret på den projektbaserede kontraktlinje</span><span class="sxs-lookup"><span data-stu-id="6e783-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="6e783-110">Et undersæt af de inkluderede komponenter kan markeres som fakturerbart ved hjælp af feltet **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="6e783-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="6e783-111">Feltet **Faktureringstype** er en grupperet indstilling, der gør det muligt at benytte følgende værdier i sammenhæng med en kontraktlinje:</span><span class="sxs-lookup"><span data-stu-id="6e783-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="6e783-112">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-112">Chargeable</span></span>
  - <span data-ttu-id="6e783-113">Ikke-fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-113">Non-chargeable</span></span>

<span data-ttu-id="6e783-114">Der kan defineres fakturerbare komponenter for opgaver, roller og transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="6e783-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="6e783-115">Fakturerbarheden defineres på opgaver i en projektkontraktlinje og gælder for alle de transaktionsklasser, der er medtaget på linjen.</span><span class="sxs-lookup"><span data-stu-id="6e783-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="6e783-116">Hvis feltet **Inkluder opgaver** i en kontraktlinje er tomt eller indstillet til **Hele projektet**, er fanen **Fakturerbare opgaver** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="6e783-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="6e783-117">Den fakturerbarhed, der er defineret på roller i en projektkontraktlinje, gælder kun for transaktionsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="6e783-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="6e783-118">Hvis feltet **Inkluder tid** i en kontraktlinje er indstillet til **Nej**, er fanen **Fakturerbare roller** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="6e783-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="6e783-119">Den fakturerbarhed, der er defineret på transaktionskategorier i en projektkontraktlinje, gælder kun for transaktionsklassen **Udgifter**.</span><span class="sxs-lookup"><span data-stu-id="6e783-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="6e783-120">Hvis feltet **Inkluder udgifter** er indstillet til **Nej**, er fanen **Fakturerbare kategorier** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="6e783-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6e783-121">Opdater en projektopgave som fakturerbar eller ikke-fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="6e783-122">En projektopgave kan være fakturerbar eller ikke-fakturerbar på en bestemt kontraktlinje, hvilket gør følgende opsætning mulig:</span><span class="sxs-lookup"><span data-stu-id="6e783-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="6e783-123">Hvis en projektbaseret kontraktlinje indeholder **Tid** og en bestemt opgave, er **T1** tilknyttet hertil som fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="6e783-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="6e783-124">Hvis der findes en anden kontraktlinje, som indeholder **Udgifter**, kan du tilknytte T1-opgaven på kontraktlinjen som ikke-fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="6e783-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="6e783-125">Resultatet er, at al den tid, der er registreret på opgaven, er fakturerbar, og alle udgifter er ikke-fakturerbare.</span><span class="sxs-lookup"><span data-stu-id="6e783-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="6e783-126">En opgaves faktureringstype kan konfigureres under fanen **Fakturerbare opgaver** på kontraktlinjen ved at opdatere feltet **Faktureringstype** i undergitteret for kontraktlinjeopgaver.</span><span class="sxs-lookup"><span data-stu-id="6e783-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="6e783-127">Du kan også opdatere feltet **Faktureringstype** i undergitteret i opsætningen af opgavefakturering for et projekt, som viser de kontraktlinjer, der er knyttede til en opgave.</span><span class="sxs-lookup"><span data-stu-id="6e783-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6e783-128">Opdater en rolle som fakturerbar eller ikke-fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="6e783-129">En rolle kan være fakturerbar eller ikke-fakturerbar på en bestemt kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="6e783-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="6e783-130">En rolles faktureringstype kan konfigureres under fanen **Fakturerbare roller** på en kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="6e783-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="6e783-131">Det kan du gøre ved at opdatere feltet **Faktureringstype** i undergitteret **Fakturerbare roller**.</span><span class="sxs-lookup"><span data-stu-id="6e783-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6e783-132">Opdater en transaktionskategori som fakturerbar eller ikke-fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="6e783-133">En transaktionskategori kan være fakturerbar eller ikke-fakturerbar på en bestemt kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="6e783-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="6e783-134">En transaktions faktureringstype kan konfigureres under fanen **Fakturerbare kategorier** på en projektbaseret kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="6e783-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="6e783-135">Det kan du gøre ved at opdatere feltet **Faktureringstype** i undergitteret **Fakturerbare kategorier**.</span><span class="sxs-lookup"><span data-stu-id="6e783-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="6e783-136">Løs fakturerbarhed</span><span class="sxs-lookup"><span data-stu-id="6e783-136">Resolve chargeability</span></span>

<span data-ttu-id="6e783-137">Et estimat eller en faktisk værdi, der oprettes for tid, kan kun faktureres, hvis:</span><span class="sxs-lookup"><span data-stu-id="6e783-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="6e783-138">**Tid** er inkluderet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="6e783-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="6e783-139">**Rolle** er konfigureret som fakturerbar på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="6e783-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="6e783-140">**Inkluderede opgaver** er angivet til **Valgte opgaver** på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="6e783-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="6e783-141">Hvis disse tre ting er sande, konfigureres opgaven også som fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="6e783-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="6e783-142">Et estimat eller en faktisk værdi, der oprettes for udgift, kan kun faktureres, hvis:</span><span class="sxs-lookup"><span data-stu-id="6e783-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="6e783-143">**Udgift** er inkluderet på kontraktlinjen</span><span class="sxs-lookup"><span data-stu-id="6e783-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="6e783-144">**Transaktionskategori** er konfigureret som fakturerbar på kontraktlinjen</span><span class="sxs-lookup"><span data-stu-id="6e783-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="6e783-145">**Inkluderede opgaver** er angivet til **Valgte opgaver** på kontraktlinjen</span><span class="sxs-lookup"><span data-stu-id="6e783-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="6e783-146">Hvis disse tre ting er sande, konfigureres **Opgaven** også som fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="6e783-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="6e783-147">Et estimat eller en faktisk værdi, der oprettes for materialer, kan kun faktureres, hvis:</span><span class="sxs-lookup"><span data-stu-id="6e783-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="6e783-148">**Materialer** er inkluderet på kontraktlinjen</span><span class="sxs-lookup"><span data-stu-id="6e783-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="6e783-149">**Inkluderede opgaver** er angivet til **Valgte opgaver** på kontraktlinjen</span><span class="sxs-lookup"><span data-stu-id="6e783-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="6e783-150">Hvis disse to ting er sande, konfigureres **Opgaven** også som fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="6e783-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6e783-151">
                    <strong>Inkluderer tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6e783-152">
                    <strong>Inkluderer udgifter</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6e783-153">
                    <strong>Materialer er inkluderet</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="6e783-154">
                    <strong>Inkluderede opgaver</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-155">
                    <strong>Rolle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6e783-156">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-157">
                    <strong>Opgave</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="6e783-158">
                    <strong>Indvirkning af fakturerbarhed</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-159">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-160">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-161">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-162">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="6e783-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-163">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-164">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-165">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-166">Fakturering af en faktisk værdi for tid: <strong>Fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-167">Faktureringstype på en faktisk værdi for en udgift: <strong>Fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-168">Faktureringstype på faktiske materialer: <strong>Fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-169">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-170">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-171">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-172">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="6e783-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-173">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-174">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-175">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-176">Fakturering af en faktisk værdi for tid: <strong>Fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-177">Faktureringstype på en faktisk værdi for en udgift: <strong>Fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-178">Faktureringstype på faktiske materialer: <strong>Fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-179">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-180">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-181">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-182">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="6e783-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-183">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-184">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-185">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-186">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-187">Faktureringstype på en faktisk værdi for en udgift: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6e783-188">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="6e783-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-189">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-190">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-191">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-192">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="6e783-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-193">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-194">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-195">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-196">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-197">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-198">Faktureringstype på en faktisk værdi for materialer: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-199">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-200">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-201">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-202">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="6e783-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-203">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-204">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-205">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-206">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-207">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-208">Faktureringstype på en faktisk værdi for materialer: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-209">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-210">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-211">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-212">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="6e783-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-213">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6e783-214">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-215">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-216">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-217">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-218">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="6e783-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6e783-219">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-220">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-221">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-222">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="6e783-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-223">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6e783-224">
                    <strong>Fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-225">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-226">Fakturering af en faktisk værdi for tid: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-227">Faktureringstype på en faktisk værdi for en udgift: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6e783-228">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="6e783-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6e783-229">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-230">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-231">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-232">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="6e783-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-233">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6e783-234">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-235">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-236">Fakturering af en faktisk værdi for tid: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-237">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-238">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="6e783-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-239">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6e783-240">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-241">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-242">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="6e783-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-243">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-244">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-245">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-246">Fakturering af en faktisk værdi for tid: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6e783-247">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-248">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="6e783-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-249">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6e783-250">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6e783-251">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-252">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="6e783-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-253">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-254">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-255">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-256">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-257">Faktureringstype på en faktisk værdi for en udgift: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-258">Faktureringstype på faktiske materialer: Kan faktureres</span><span class="sxs-lookup"><span data-stu-id="6e783-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-259">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-260">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6e783-261">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-262">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="6e783-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-263">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-264">Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-265">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-266">Fakturering af en faktisk værdi for tid: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6e783-267">Faktureringstype på en faktisk værdi for en udgift: Fakturerbar</span><span class="sxs-lookup"><span data-stu-id="6e783-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6e783-268">Faktureringstype på en faktisk værdi for materialer: <strong>Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6e783-269">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6e783-270">Ja</span><span class="sxs-lookup"><span data-stu-id="6e783-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6e783-271">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6e783-272">Hele projektet</span><span class="sxs-lookup"><span data-stu-id="6e783-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6e783-273">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6e783-274">
                    <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6e783-275">Kan ikke angives</span><span class="sxs-lookup"><span data-stu-id="6e783-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6e783-276">Fakturering af en faktisk værdi for tid: <strong>Ikke-fakturerbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-277">Faktureringstype på en faktisk værdi for en udgift:<strong> Ikke-fakturerbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6e783-278">Faktureringstype på en faktisk værdi for materialer:<strong> Ikke tilgængelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e783-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
