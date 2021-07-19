---
title: Oversigt over projektbaserede kontraktlinjer
description: Dette emne indeholder oplysninger om at arbejde med projektbaserede kontraktlinjer.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369909"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="28a67-103">Oversigt over projektbaserede kontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="28a67-103">Project-based contract lines overview</span></span>

<span data-ttu-id="28a67-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="28a67-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="28a67-105">Projektbaserede kontraktlinjer i Dynamics 365 Project Operations er designet til at rumme estimat- og faktureringsaftaler for specifikke komponenter i projektarbejde på en aftale.</span><span class="sxs-lookup"><span data-stu-id="28a67-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="28a67-106">Strukturen i en projektbaseret kontraktlinje udvides for projektestimater og faktureringsscenarier med følgende koncepter:</span><span class="sxs-lookup"><span data-stu-id="28a67-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="28a67-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="28a67-107">Billing method</span></span>
- <span data-ttu-id="28a67-108">Projekt- og opgavetilknytning</span><span class="sxs-lookup"><span data-stu-id="28a67-108">Project and task mapping</span></span>
- <span data-ttu-id="28a67-109">Inkluderede transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="28a67-109">Included transaction classes</span></span>
- <span data-ttu-id="28a67-110">Grænse, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="28a67-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="28a67-111">Opsætning af fakturerbarhed</span><span class="sxs-lookup"><span data-stu-id="28a67-111">Chargeability setup</span></span>
- <span data-ttu-id="28a67-112">Estimater ved hjælp af kontraktlinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="28a67-112">Estimates using contract line details</span></span>
- <span data-ttu-id="28a67-113">Kontraktlinjekunder</span><span class="sxs-lookup"><span data-stu-id="28a67-113">Contract line customers</span></span>

<span data-ttu-id="28a67-114">I følgende tabel medtages felterne under fanen **Generelt** for projektbaserede kontraktlinjer, som hjælper med at konfigurere grundlaget for et detaljeret, grundlæggende estimat og faktureringsaftaler for projektbaseret arbejde.</span><span class="sxs-lookup"><span data-stu-id="28a67-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="28a67-115">Felt</span><span class="sxs-lookup"><span data-stu-id="28a67-115">Field</span></span> | <span data-ttu-id="28a67-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="28a67-116">Description</span></span> | <span data-ttu-id="28a67-117">Downstream-virkning</span><span class="sxs-lookup"><span data-stu-id="28a67-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="28a67-118">**Navn**</span><span class="sxs-lookup"><span data-stu-id="28a67-118">**Name**</span></span> | <span data-ttu-id="28a67-119">Navn på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="28a67-119">Name of the contract line.</span></span> <span data-ttu-id="28a67-120">Dette identificerer den diskrete komponent i kontrakten, der skal estimeres.</span><span class="sxs-lookup"><span data-stu-id="28a67-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="28a67-121">I en projektkontrakt, der er oprettet ud fra et tilbud, kopieres denne værdi fra en tilsvarende værdi for den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="28a67-122">Navnet kopieres til den projektfakturalinje, der oprettes fra denne kontraktlinje, når fakturaen oprettes.</span><span class="sxs-lookup"><span data-stu-id="28a67-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="28a67-123">**Faktureringsmetode**</span><span class="sxs-lookup"><span data-stu-id="28a67-123">**Billing Method**</span></span> | <span data-ttu-id="28a67-124">På en projektkontrakt, der er oprettet ud fra et tilbud, kopieres denne værdi fra det tilsvarende felt på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="28a67-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="28a67-125">Dette er en grupperet indstilling, der repræsenterer de to primære kontraktmodeller, som understøttes af Project Operations:</span><span class="sxs-lookup"><span data-stu-id="28a67-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="28a67-126">- **Fast pris**</span><span class="sxs-lookup"><span data-stu-id="28a67-126">- **Fixed Price**</span></span></br><span data-ttu-id="28a67-127">- **Tid og materiale**</span><span class="sxs-lookup"><span data-stu-id="28a67-127">- **Time and Material**</span></span> | <span data-ttu-id="28a67-128">Den faktiske transaktion behandles på grundlag af faktureringsmetoden for den kontrakt, der henvises til.</span><span class="sxs-lookup"><span data-stu-id="28a67-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="28a67-129">Hvis den kontraktlinje, der henvises til af den faktiske værdi, har en faktureringsmetode for tid og materialer, oprettes der poster for omkostninger og ikke-faktureret faktisk salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="28a67-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="28a67-130">Hvis den kontraktlinje, der henvises til af den faktiske værdi, har en faktureringsmetode for fast pris, oprettes der kun en faktisk omkostningsværdi.</span><span class="sxs-lookup"><span data-stu-id="28a67-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="28a67-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="28a67-131">**Project**</span></span> | <span data-ttu-id="28a67-132">Brug dette felt til at identificere det projekt, der skal bruges til at levere arbejdet på denne aftale.</span><span class="sxs-lookup"><span data-stu-id="28a67-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="28a67-133">Denne værdi bruges sammen med **Inkluderede opgaver** og **Inkluderede transaktionsklasser** til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost.</span><span class="sxs-lookup"><span data-stu-id="28a67-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="28a67-134">**Inkluderede opgaver**</span><span class="sxs-lookup"><span data-stu-id="28a67-134">**Included Tasks**</span></span> | <span data-ttu-id="28a67-135">Angiver, om denne kontraktlinje inkluderer alle projektopgaver for det valgte projekt eller kun et undersæt af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="28a67-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="28a67-136">Dette er en grupperet indstilling, der har følgende mulige værdier:</span><span class="sxs-lookup"><span data-stu-id="28a67-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="28a67-137">- **Alle projektopgaver**</span><span class="sxs-lookup"><span data-stu-id="28a67-137">- **All Project Tasks**</span></span></br><span data-ttu-id="28a67-138">- **Kun markerede projektopgaver**.</span><span class="sxs-lookup"><span data-stu-id="28a67-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="28a67-139">En tom værdi i dette felt svarer til at vælge **Alle projektopgaver**.</span><span class="sxs-lookup"><span data-stu-id="28a67-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="28a67-140">Hvis du har valgt **Kun markerede opgaver**, kan du vælge bestemte opgaver og knytte dem til denne kontraktlinje under fanen **Opsætning af opgavefakturering** på siden **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="28a67-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="28a67-141">Værdien anvendes sammen med klasserne **Projekt** og **Inkluderet transaktion** til at fortolke kontraktlinjereferencen på en post for en faktisk værdi eller en estimatlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="28a67-142">**Medtag tid**</span><span class="sxs-lookup"><span data-stu-id="28a67-142">**Include Time**</span></span> | <span data-ttu-id="28a67-143">Værdien **Ja**/**Nej** angiver, om tidstransaktioner eller arbejdsomkostninger for det valgte projekt skal medtages på denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="28a67-144">En værdi angivet til **Nej** medfører, at tidstransaktionerne eller arbejdsomkostninger ikke medtages på denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="28a67-145">Hvis værdien **Ja** er angivet, betyder det, at de bliver medtaget.</span><span class="sxs-lookup"><span data-stu-id="28a67-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="28a67-146">Denne værdi bruges sammen med projektet til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost.</span><span class="sxs-lookup"><span data-stu-id="28a67-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="28a67-147">**Medtag udgift**</span><span class="sxs-lookup"><span data-stu-id="28a67-147">**Include Expense**</span></span> | <span data-ttu-id="28a67-148">Værdien **Ja**/**Nej** angiver, om udgiftsomkostninger for det valgte projekt skal medtages på denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="28a67-149">En værdi angivet til **Nej** medfører, at udgiftsomkostningen ikke medtages på denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="28a67-150">Hvis værdien **Ja** er angivet, betyder det, at den bliver medtaget.</span><span class="sxs-lookup"><span data-stu-id="28a67-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="28a67-151">Denne værdi bruges sammen med projektet til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost.</span><span class="sxs-lookup"><span data-stu-id="28a67-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="28a67-152">**Medtag materialer**</span><span class="sxs-lookup"><span data-stu-id="28a67-152">**Include Materials**</span></span> | <span data-ttu-id="28a67-153">Værdien **Ja**/**Nej** angiver, om materialeomkostninger for det valgte projekt skal medtages på denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="28a67-154">En værdi angivet som **Nej** indikerer, at materialeomkostningerne ikke bliver medtaget på denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="28a67-155">Hvis værdien **Ja** er angivet, betyder det, at den bliver medtaget.</span><span class="sxs-lookup"><span data-stu-id="28a67-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="28a67-156">Denne værdi bruges sammen med projektet til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost.</span><span class="sxs-lookup"><span data-stu-id="28a67-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="28a67-157">**Medtag gebyr**</span><span class="sxs-lookup"><span data-stu-id="28a67-157">**Include Fee**</span></span> | <span data-ttu-id="28a67-158">Værdien **Ja**/**Nej** angiver, om gebyrer for det valgte projekt skal medtages på denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="28a67-159">En værdi angivet til **Nej** medfører, at gebyrerne ikke medtages på denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="28a67-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="28a67-160">Hvis værdien **Ja** er angivet, betyder det, at de bliver medtaget.</span><span class="sxs-lookup"><span data-stu-id="28a67-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="28a67-161">Denne værdi bruges sammen med projektet til at fastsætte kontraktlinjereferencen for en faktisk eller estimeret linjepost.</span><span class="sxs-lookup"><span data-stu-id="28a67-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="28a67-162">**Kontraktbeløb**</span><span class="sxs-lookup"><span data-stu-id="28a67-162">**Contracted Amount**</span></span> | <span data-ttu-id="28a67-163">På en kontraktlinje med fast pris er dette beløb den aftalte værdi, der skal faktureres kunden for alle de arbejdskomponenter, der er knyttet til kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="28a67-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="28a67-164">På en kontraktlinje med tid og materialer er dette beløb en estimeret værdi for det, der skal faktureres kunden for alle de arbejdskomponenter, der er knyttet til kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="28a67-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="28a67-165">På en projektkontrakt, som er oprettet ud fra et tilbud, kopieres denne værdi fra det tilsvarende felt på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="28a67-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="28a67-166">Når en projektbaseret kontraktlinje indeholder linjeoplysninger, er dette felt låst mod redigering og opsummeres i på grundlag af beløbet i kontraktlinjeoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="28a67-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="28a67-167">Når kontraktlinjen indeholder linjeoplysninger, kan denne værdi ændres ved at ændre beløbene på linjedetaljerne.</span><span class="sxs-lookup"><span data-stu-id="28a67-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="28a67-168">På en kontraktlinje med fast pris bruges denne værdi til at oprette beløbet før moms på periodiske faktureringsmilepæle.</span><span class="sxs-lookup"><span data-stu-id="28a67-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="28a67-169">**Anslået moms**</span><span class="sxs-lookup"><span data-stu-id="28a67-169">**Estimated Tax**</span></span> | <span data-ttu-id="28a67-170">Brugeren kan redigere dette felt for at angive det estimerede momsbeløb på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="28a67-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="28a67-171">Når en projektbaseret kontraktlinje indeholder linjeoplysninger, er dette felt låst mod redigering og opsummeres i på grundlag af momsbeløbet i kontraktlinjeoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="28a67-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="28a67-172">Når kontraktlinjen indeholder linjeoplysninger, kan denne værdi ændres ved at ændre momsbeløbene på linjedetaljerne.</span><span class="sxs-lookup"><span data-stu-id="28a67-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="28a67-173">På en kontraktlinje med fast pris bruges denne værdi til at oprette momsen på periodiske faktureringsmilepæle.</span><span class="sxs-lookup"><span data-stu-id="28a67-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="28a67-174">**Kontraktbeløb efter moms**</span><span class="sxs-lookup"><span data-stu-id="28a67-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="28a67-175">Beløbet på kontraktlinjen efter moms.</span><span class="sxs-lookup"><span data-stu-id="28a67-175">The contract line amount after tax.</span></span> <span data-ttu-id="28a67-176">Dette felt er skrivebeskyttet og beregnes som **Kontraktbeløb + moms**.</span><span class="sxs-lookup"><span data-stu-id="28a67-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="28a67-177">På en kontraktlinje med fast pris bruges denne værdi til at oprette periodiske faktureringsmilepæle.</span><span class="sxs-lookup"><span data-stu-id="28a67-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="28a67-178">**Grænse, der ikke må overskrides**</span><span class="sxs-lookup"><span data-stu-id="28a67-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="28a67-179">Brugeren kan redigere dette felt, og det er kun tilgængeligt for projektbaserede kontraktlinjer, der har faktureringsmetoden angivet som tid og materialer.</span><span class="sxs-lookup"><span data-stu-id="28a67-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="28a67-180">Brugeren kan redigere dette felt.</span><span class="sxs-lookup"><span data-stu-id="28a67-180">The user can edit this field.</span></span> <span data-ttu-id="28a67-181">Når en faktisk værdi for tid og materialer refererer til denne kontraktlinje for tid og materiale, evalueres beløbet på den faktiske værdi i forhold til grænsen, der ikke må overskrides, på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="28a67-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="28a67-182">Denne evaluering fuldføres, når der redegøres for de allerede brugte og forpligtede beløb.</span><span class="sxs-lookup"><span data-stu-id="28a67-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="28a67-183">**Kundebudget**</span><span class="sxs-lookup"><span data-stu-id="28a67-183">**Customer Budget**</span></span> | <span data-ttu-id="28a67-184">Dette felt kan redigeres og kopieres fra det tilsvarende felt på tilbudslinjen, hvis kontrakten er blevet oprettet på grundlag af et tilbud.</span><span class="sxs-lookup"><span data-stu-id="28a67-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="28a67-185">Dette felt bruges kun til orientering, og det har ingen afledede virkninger.</span><span class="sxs-lookup"><span data-stu-id="28a67-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="28a67-186">Valideringsregler for indstillingerne under fanen Generelt på projektbaserede kontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="28a67-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="28a67-187">Regel 1: Hvis feltet **Inkluderede opgaver** er tomt eller angivet til **Alle projektopgaver**, medtages alle opgaver i projektet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="28a67-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="28a67-188">Regel 2: Når feltet **Inkluderede opgaver** er tomt eller eksplicit angivet til **Alle projektopgaver**, kan et projekt og en bestemt transaktionsklasse kun inkluderes på én projektbaseret kontraktlinje i en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="28a67-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="28a67-189">Regel 3: Når feltet **Inkluderede opgaver** er angivet til **Kun markerede projektopgaver**, kan et projekt og en bestemt transaktionsklasse inkluderes på flere projektbaserede kontraktlinjer i en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="28a67-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="28a67-190">
                    <strong>Kontrakt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28a67-191">
                    <strong>Kontraktlinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="28a67-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="28a67-193">
                    <strong>Inkluderede opgaver</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="28a67-194">
                    <strong>Medtag tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="28a67-195">
                    <strong>Medtag udgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="28a67-196">
                    <strong>Medtag materialer</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="28a67-197">
                    <strong>Inkluder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="28a67-198">
                    <strong>Gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="28a67-199">
                    <strong>Gyldig/ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="28a67-200">
                    <strong>Årsag</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28a67-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-201">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-202">CL1</span><span class="sxs-lookup"><span data-stu-id="28a67-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-203">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-204">Tom</span><span class="sxs-lookup"><span data-stu-id="28a67-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-205">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-206">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-207">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-208">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-209">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="28a67-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-210">Overtrædelse af regel #2.</span><span class="sxs-lookup"><span data-stu-id="28a67-210">Violation of Rule #2.</span></span> <span data-ttu-id="28a67-211">Tid, udgifter, materialer og gebyrer på P1-projektet medtages på både tilbudslinjerne CL1 og CL2.</span><span class="sxs-lookup"><span data-stu-id="28a67-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-212">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-213">CL2</span><span class="sxs-lookup"><span data-stu-id="28a67-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-214">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-215">Tom</span><span class="sxs-lookup"><span data-stu-id="28a67-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-216">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-217">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-218">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-219">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-220">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-221">CL1</span><span class="sxs-lookup"><span data-stu-id="28a67-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-222">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-223">Tom</span><span class="sxs-lookup"><span data-stu-id="28a67-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-224">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-225">Nr.</span><span class="sxs-lookup"><span data-stu-id="28a67-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-226">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-227">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-228">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="28a67-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-229">Overtrædelse af regel #2.</span><span class="sxs-lookup"><span data-stu-id="28a67-229">Violation of Rule #2.</span></span> <span data-ttu-id="28a67-230">Tid, materialer og gebyrer på P1-projektet medtages på både tilbudslinjerne CL1 og CL2.</span><span class="sxs-lookup"><span data-stu-id="28a67-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-231">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-232">CL2</span><span class="sxs-lookup"><span data-stu-id="28a67-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-233">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-234">Tom</span><span class="sxs-lookup"><span data-stu-id="28a67-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-235">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-236">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-237">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-238">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-239">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-240">CL1</span><span class="sxs-lookup"><span data-stu-id="28a67-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-241">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-242">Tom</span><span class="sxs-lookup"><span data-stu-id="28a67-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-243">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-244">Nr.</span><span class="sxs-lookup"><span data-stu-id="28a67-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-245">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-246">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-247">Gyldig</span><span class="sxs-lookup"><span data-stu-id="28a67-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-248">Tid, materialer og gebyrer på P1-projektet medtages på CL1.</span><span class="sxs-lookup"><span data-stu-id="28a67-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="28a67-249">Udgift til P1-projekt er inkluderet i CL2.</span><span class="sxs-lookup"><span data-stu-id="28a67-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="28a67-250">Der er ingen overlapningen i det, der inkluderes på de enkelte kontraktlinjer, og derfor er det gyldigt.</span><span class="sxs-lookup"><span data-stu-id="28a67-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-251">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-252">CL2</span><span class="sxs-lookup"><span data-stu-id="28a67-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-253">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-254">Tom</span><span class="sxs-lookup"><span data-stu-id="28a67-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-255">Nr.</span><span class="sxs-lookup"><span data-stu-id="28a67-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-256">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-257">Nr.</span><span class="sxs-lookup"><span data-stu-id="28a67-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-258">Nr.</span><span class="sxs-lookup"><span data-stu-id="28a67-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-259">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-260">CL1</span><span class="sxs-lookup"><span data-stu-id="28a67-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-261">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-262">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="28a67-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-263">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-264">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-265">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-266">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-267">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="28a67-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-268">Overtrædelse af regel nr. 2</span><span class="sxs-lookup"><span data-stu-id="28a67-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="28a67-269">C1 omfatter tid, materialer, udgifter og gebyrer på et undersæt af opgaver på projekt P1.</span><span class="sxs-lookup"><span data-stu-id="28a67-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="28a67-270">CL2 inkluderer tid, materialer, udgifter og gebyrer for hele projekt P1 og overlapper derfor med det, der er medtaget i C1.</span><span class="sxs-lookup"><span data-stu-id="28a67-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-271">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-272">CL2</span><span class="sxs-lookup"><span data-stu-id="28a67-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-273">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-274">Tom</span><span class="sxs-lookup"><span data-stu-id="28a67-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-275">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-276">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-277">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-278">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-279">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-280">CL1</span><span class="sxs-lookup"><span data-stu-id="28a67-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-281">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-282">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="28a67-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-283">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-284">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-285">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-286">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-287">Gyldig</span><span class="sxs-lookup"><span data-stu-id="28a67-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28a67-288">I henhold til regel nr. 3</span><span class="sxs-lookup"><span data-stu-id="28a67-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="28a67-289">C1 omfatter tid, udgifter, materialer og gebyrer på et undersæt af opgaver på projekt P1.</span><span class="sxs-lookup"><span data-stu-id="28a67-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="28a67-290">CL2 omfatter tid, udgifter, materialer og gebyrer for et undersæt af opgaver på projekt P1.</span><span class="sxs-lookup"><span data-stu-id="28a67-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="28a67-291">Den eneste yderligere validering er omkring det undersæt af opgaver på CL1, som er forskellig fra undersættet af opgaver i CL2 for at sikre, at der ikke er nogen overlapning.</span><span class="sxs-lookup"><span data-stu-id="28a67-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="28a67-292">Dette gøres af systemet, når opgaverne er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="28a67-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28a67-293">C1</span><span class="sxs-lookup"><span data-stu-id="28a67-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28a67-294">CL2</span><span class="sxs-lookup"><span data-stu-id="28a67-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-295">P1</span><span class="sxs-lookup"><span data-stu-id="28a67-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="28a67-296">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="28a67-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-297">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="28a67-298">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-299">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="28a67-300">Ja</span><span class="sxs-lookup"><span data-stu-id="28a67-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
