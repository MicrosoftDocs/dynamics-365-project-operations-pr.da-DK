---
title: Oversigt over projektbaserede tilbudslinjer
description: Dette emne indeholder oplysninger om, hvordan du bruger projektbaserede tilbudslinjer til projektarbejde.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994849"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="13944-103">Oversigt over projektbaserede tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="13944-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="13944-104">_**Gælder for:** Lille udrulning - aftale om proformafakturering, Project Operations for ressource/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="13944-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="13944-105">Projektbaserede tilbudslinjer er udviklet til at hjælpe med at vurdere projektarbejdet på en aftale.</span><span class="sxs-lookup"><span data-stu-id="13944-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="13944-106">Strukturen for en projektbaseret tilbudslinje forlænges for projektestimater med følgende koncepter:</span><span class="sxs-lookup"><span data-stu-id="13944-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="13944-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="13944-107">Billing Method</span></span>
- <span data-ttu-id="13944-108">Projekt- og opgavetilknytning</span><span class="sxs-lookup"><span data-stu-id="13944-108">Project and Task Mapping</span></span>
- <span data-ttu-id="13944-109">Inkluderede transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="13944-109">Included Transaction classes</span></span>
- <span data-ttu-id="13944-110">Grænse, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="13944-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="13944-111">Opsætning af fakturerbarhed</span><span class="sxs-lookup"><span data-stu-id="13944-111">Chargeability setup</span></span>
- <span data-ttu-id="13944-112">Estimering ved hjælp af tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="13944-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="13944-113">Tilbudslinjekunder</span><span class="sxs-lookup"><span data-stu-id="13944-113">Quote line Customers</span></span>

<span data-ttu-id="13944-114">Følgende tabel indeholder oplysninger om felterne under fanen **Generelt** på den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="13944-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="13944-115">Disse felter bruges til at konfigurere grundlaget for en detaljeret estimering overslag af projektarbejdet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="13944-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="13944-116">**Felt**</span><span class="sxs-lookup"><span data-stu-id="13944-116">**Field**</span></span> | <span data-ttu-id="13944-117">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="13944-117">**Description**</span></span> | <span data-ttu-id="13944-118">**Downstream-virkning**</span><span class="sxs-lookup"><span data-stu-id="13944-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="13944-119">Navn</span><span class="sxs-lookup"><span data-stu-id="13944-119">Name</span></span> | <span data-ttu-id="13944-120">Navnet på tilbudslinjen, der hjælper dig med at identificere det diskrete komponent i det tilbud, der estimeres.</span><span class="sxs-lookup"><span data-stu-id="13944-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="13944-121">Kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="13944-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-122">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="13944-122">Billing Method</span></span> | <span data-ttu-id="13944-123">På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt på salgsmulighedslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="13944-124">Feltet omfatter de to primære kontraktmodeller, der understøttes af Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="13944-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="13944-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="13944-125">- Fixed price</span></span></br><span data-ttu-id="13944-126">- Tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="13944-126">- Time and material.</span></span>| <span data-ttu-id="13944-127">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-128">Project</span><span class="sxs-lookup"><span data-stu-id="13944-128">Project</span></span> | <span data-ttu-id="13944-129">Brug dette valgfrie felt til at identificere det projekt, der skal bruges til at levere arbejdet på denne aftale.</span><span class="sxs-lookup"><span data-stu-id="13944-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="13944-130">Når et projekt knyttes til en tilbudslinje, kan det hjælpe med konfigurationen af fakturerbare opgaver og også til at udarbejde et projektbaseret estimat over tilbudslinjen som tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="13944-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="13944-131">Når et projekt ikke er knyttet til en projektbaseret tilbudslinje, skal estimatet oprettes manuelt ved at oprette hver enkelt tilbudslinjedetalje.</span><span class="sxs-lookup"><span data-stu-id="13944-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="13944-132">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="13944-133">Inkluderede opgaver</span><span class="sxs-lookup"><span data-stu-id="13944-133">Included Tasks</span></span> | <span data-ttu-id="13944-134">Angiver, om denne tilbudslinje bruges til alle eller nogle af projektopgaverne for det valgte projekt.</span><span class="sxs-lookup"><span data-stu-id="13944-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="13944-135">Dette felt har følgende mulige værdier:</span><span class="sxs-lookup"><span data-stu-id="13944-135">This field has the following possible values:</span></span></br><span data-ttu-id="13944-136">- Alle projektopgaver</span><span class="sxs-lookup"><span data-stu-id="13944-136">- All project tasks</span></span></br><span data-ttu-id="13944-137">- Kun valgte projektopgaver</span><span class="sxs-lookup"><span data-stu-id="13944-137">- Selected project tasks only</span></span></br><span data-ttu-id="13944-138">En tom værdi i dette felt svarer til indstillingen **Alle projektopgaver**.</span><span class="sxs-lookup"><span data-stu-id="13944-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="13944-139">Når **Kun valgte projektopgaver** vælges på projektsiden, kan du under fanen **Konfiguration af opgavefakturering** vælge bestemte opgaver, som du vil knytte sammen med tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="13944-140">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-141">Medtag tid</span><span class="sxs-lookup"><span data-stu-id="13944-141">Include Time</span></span> | <span data-ttu-id="13944-142">Værdien **Ja**/**Nej** angiver, om tidstransaktioner eller arbejdsomkostninger for det valgte projekt skal medtages i estimatet på denne tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="13944-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="13944-143">En værdi med **Nej** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="13944-144">En værdi med **Ja** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="13944-145">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-146">Medtag udgift</span><span class="sxs-lookup"><span data-stu-id="13944-146">Include Expense</span></span> | <span data-ttu-id="13944-147">Værdien **Ja**/**Nej** angiver, om udgiftsomkostninger for det valgte projekt skal medtages i estimatet på denne tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="13944-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="13944-148">En værdi med **Nej** indikerer, at udgiftsomkostningerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="13944-149">En værdi med **Ja** indikerer, at udgiftsomkostningerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="13944-150">Værdien kopieres over til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-151">Medtag materiale</span><span class="sxs-lookup"><span data-stu-id="13944-151">Include Material</span></span> | <span data-ttu-id="13944-152">Værdien **Ja**/**Nej** angiver, om materialeomkostninger for det valgte projekt skal medtages i estimatet på denne tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="13944-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="13944-153">En værdi angivet som **Nej** indikerer, at materialeomkostningerne ikke bliver medtaget i estimatet på denne tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="13944-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="13944-154">En værdi angivet som **Ja** indikerer, at materialeomkostningerne bliver medtaget i estimatet på denne tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="13944-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="13944-155">Værdien kopieres over til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-156">Medtag gebyr</span><span class="sxs-lookup"><span data-stu-id="13944-156">Include Fee</span></span> | <span data-ttu-id="13944-157">Værdien **Ja**/**Nej** angiver, om gebyrer for det valgte projekt skal medtages i estimatet på denne tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="13944-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="13944-158">En værdi med **Nej** indikerer, at gebyrerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="13944-159">En værdi med **Ja** indikerer, at gebyrerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="13944-160">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-161">Tilbudsbeløb</span><span class="sxs-lookup"><span data-stu-id="13944-161">Quoted Amount</span></span> | <span data-ttu-id="13944-162">Dette er det beløb, der oplyses kunden for alt det budgetterede arbejde med denne projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="13944-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="13944-163">På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt **Kundebudget** på salgsmulighedslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="13944-164">Når den projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til beløbet i detaljerne i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="13944-165">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-166">Anslået moms</span><span class="sxs-lookup"><span data-stu-id="13944-166">Estimated Tax</span></span> | <span data-ttu-id="13944-167">Dette felt er et redigerbart felt, hvor brugeren kan tilføje det anslåede momsbeløb på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="13944-168">Når en projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til momsbeløbet i detaljerne i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="13944-169">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-170">Tilbudsbeløb efter moms</span><span class="sxs-lookup"><span data-stu-id="13944-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="13944-171">Dette felt er tilbudslinjebeløbet efter moms og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="13944-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="13944-172">Beløbet i dette felt beregnes som *Tilbudsbeløb + moms*.</span><span class="sxs-lookup"><span data-stu-id="13944-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="13944-173">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-174">Grænse, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="13944-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="13944-175">Dette felt kan redigeres og er kun tilgængeligt for projektbaserede tilbudslinjer med faktureringsmetoden **Tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="13944-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="13944-176">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="13944-177">Kundebudget</span><span class="sxs-lookup"><span data-stu-id="13944-177">Customer Budget</span></span> | <span data-ttu-id="13944-178">Dette felt kan redigeres og kopieres fra det tilsvarende felt på salgsmulighedslinjen, hvis tilbuddet blev oprettet ud fra en salgsmulighed.</span><span class="sxs-lookup"><span data-stu-id="13944-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="13944-179">Værdien kopieres til den projektkontraktlinje, der oprettes fra denne tilbudslinje, når tilbuddet vindes.</span><span class="sxs-lookup"><span data-stu-id="13944-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="13944-180">Valideringsregler for felter under fanen Generelt på projektbaserede tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="13944-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="13944-181">**Regel 1**: Hvis feltet **Inkluderede opgaver** er tomt, eller hvis det er angivet til **Alle projektopgaver**, medtages der et projekt i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="13944-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="13944-182">**Regel 2**: Hvis feltet **Inkluderede opgaver** er tomt, eller hvis det er angivet til **Alle projektopgaver**, kan et projekt og en bestemt transaktionsklasse kun inkluderes på én projektbaseret tilbudslinje for et tilbud.</span><span class="sxs-lookup"><span data-stu-id="13944-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="13944-183">**Regel 3**: Hvis feltet **Inkluderede opgaver** er angivet til **Kun valgte projektopgaver**, kan et projekt og en bestemt transaktionsklasse inkluderes på flere projektbaseret tilbudslinjer for et tilbud.</span><span class="sxs-lookup"><span data-stu-id="13944-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="13944-184">**Regel 4**: Hvis en salgsmulighed har flere tilbud, kan der være tilbudslinjer fra forskellige tilbud, der alle refererer til det samme projekt, og som inkluderer samme transaktionsklasse.</span><span class="sxs-lookup"><span data-stu-id="13944-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="13944-185">**Regel 5**: Hvis de pågældende tilbud ikke hører til samme salgsmulighed, kan de ikke indeholde samme projekt- og transaktionsklasse.</span><span class="sxs-lookup"><span data-stu-id="13944-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="13944-186">
                    <strong>Salgsmulighed</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="13944-187">
                    <strong>Tilbud</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="13944-188">
                    <strong>Tilbudslinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="13944-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="13944-190">
                    <strong>Inkluderede opgaver</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="13944-191">
                    <strong>Medtag tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="13944-192">
                    <strong>Medtag udgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="13944-193">
                    <strong>Medtag materiale</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="13944-194">
                    <strong>Inkluder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="13944-195">
                    <strong>Gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="13944-196">
                    <strong>Gyldig/ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="13944-197">
                    <strong>Årsag</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13944-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-198">O1</span><span class="sxs-lookup"><span data-stu-id="13944-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-199">K1</span><span class="sxs-lookup"><span data-stu-id="13944-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-200">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-201">P1</span><span class="sxs-lookup"><span data-stu-id="13944-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-202">Tom</span><span class="sxs-lookup"><span data-stu-id="13944-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-203">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-204">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-205">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-206">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-207">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="13944-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-208">Overtrædelse af regel #2.</span><span class="sxs-lookup"><span data-stu-id="13944-208">Violation of Rule #2.</span></span> <span data-ttu-id="13944-209">Tid, udgifter og gebyrer på P1-projektet medtages på tilbudslinjerne QL1 og QL2</span><span class="sxs-lookup"><span data-stu-id="13944-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-210">O1</span><span class="sxs-lookup"><span data-stu-id="13944-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-211">K1</span><span class="sxs-lookup"><span data-stu-id="13944-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-212">QL2</span><span class="sxs-lookup"><span data-stu-id="13944-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-213">P1</span><span class="sxs-lookup"><span data-stu-id="13944-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-214">Tom</span><span class="sxs-lookup"><span data-stu-id="13944-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-215">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-216">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-217">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-218">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-219">O1</span><span class="sxs-lookup"><span data-stu-id="13944-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-220">K1</span><span class="sxs-lookup"><span data-stu-id="13944-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-221">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-222">P1</span><span class="sxs-lookup"><span data-stu-id="13944-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-223">Tom</span><span class="sxs-lookup"><span data-stu-id="13944-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-224">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-225">Nr.</span><span class="sxs-lookup"><span data-stu-id="13944-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-226">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-227">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-228">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="13944-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-229">Overtrædelse af regel #2.</span><span class="sxs-lookup"><span data-stu-id="13944-229">Violation of Rule #2.</span></span> <span data-ttu-id="13944-230">Tid, materialer og gebyrer på P1-projektet medtages på tilbudslinjerne QL1 og QL2</span><span class="sxs-lookup"><span data-stu-id="13944-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-231">O1</span><span class="sxs-lookup"><span data-stu-id="13944-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-232">K1</span><span class="sxs-lookup"><span data-stu-id="13944-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-233">QL2</span><span class="sxs-lookup"><span data-stu-id="13944-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-234">P1</span><span class="sxs-lookup"><span data-stu-id="13944-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-235">Tom</span><span class="sxs-lookup"><span data-stu-id="13944-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-236">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-237">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-238">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-239">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-240">O1</span><span class="sxs-lookup"><span data-stu-id="13944-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-241">K1</span><span class="sxs-lookup"><span data-stu-id="13944-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-242">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-243">P1</span><span class="sxs-lookup"><span data-stu-id="13944-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-244">Tom</span><span class="sxs-lookup"><span data-stu-id="13944-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-245">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="13944-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-247">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-248">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-249">Gyldig</span><span class="sxs-lookup"><span data-stu-id="13944-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-250">Tid, materialer og gebyrer på P1-projektet medtages på QL1</span><span class="sxs-lookup"><span data-stu-id="13944-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="13944-251">Udgift til P1-projekt er inkluderet i QL2</span><span class="sxs-lookup"><span data-stu-id="13944-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="13944-252">Der er ingen overlapningen i det, der inkluderes på de enkelte tilbudslinjer, og derfor er det gyldigt.</span><span class="sxs-lookup"><span data-stu-id="13944-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-253">O1</span><span class="sxs-lookup"><span data-stu-id="13944-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-254">K1</span><span class="sxs-lookup"><span data-stu-id="13944-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-255">QL2</span><span class="sxs-lookup"><span data-stu-id="13944-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-256">P1</span><span class="sxs-lookup"><span data-stu-id="13944-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-257">Tom</span><span class="sxs-lookup"><span data-stu-id="13944-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-258">Nr.</span><span class="sxs-lookup"><span data-stu-id="13944-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-259">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-260">Nr.</span><span class="sxs-lookup"><span data-stu-id="13944-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="13944-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-262">O1</span><span class="sxs-lookup"><span data-stu-id="13944-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-263">K1</span><span class="sxs-lookup"><span data-stu-id="13944-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-264">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-265">P1</span><span class="sxs-lookup"><span data-stu-id="13944-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-266">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="13944-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-267">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-268">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-269">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-270">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-271">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="13944-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-272">Overtrædelse af regel nr. 2</span><span class="sxs-lookup"><span data-stu-id="13944-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="13944-273">Q1 omfatter Tid, Materialer, Udgifter og Gebyrer på et undersæt af opgaver på projekt P1</span><span class="sxs-lookup"><span data-stu-id="13944-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="13944-274">QL2 inkluderer Tid, Udgifter og Gebyrer for hele projekt P1 og overlapper derfor med det, der er medtaget i Q1.</span><span class="sxs-lookup"><span data-stu-id="13944-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-275">O1</span><span class="sxs-lookup"><span data-stu-id="13944-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-276">K1</span><span class="sxs-lookup"><span data-stu-id="13944-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-277">QL2</span><span class="sxs-lookup"><span data-stu-id="13944-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-278">P1</span><span class="sxs-lookup"><span data-stu-id="13944-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-279">Tom</span><span class="sxs-lookup"><span data-stu-id="13944-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-280">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-281">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-282">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-283">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-284">O1</span><span class="sxs-lookup"><span data-stu-id="13944-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-285">K1</span><span class="sxs-lookup"><span data-stu-id="13944-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-286">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-287">P1</span><span class="sxs-lookup"><span data-stu-id="13944-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-288">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="13944-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-289">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-290">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-291">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-292">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-293">Gyldig</span><span class="sxs-lookup"><span data-stu-id="13944-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-294">I henhold til regel nr. 3,</span><span class="sxs-lookup"><span data-stu-id="13944-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="13944-295">Q1 omfatter Tid, Materialer, Udgifter og Gebyrer på et undersæt af opgaver på projekt P1.</span><span class="sxs-lookup"><span data-stu-id="13944-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="13944-296">QL2 omfatter Tid, Materialer, Udgifter og Gebyrer for et undersæt af opgaver på projekt P1.</span><span class="sxs-lookup"><span data-stu-id="13944-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="13944-297">Den eneste yderligere validering er omkring det undersæt af opgaver på QL1, som er forskellig fra undersættet af opgaver i QL2 for at sikre, at der ikke sker overlapning.</span><span class="sxs-lookup"><span data-stu-id="13944-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="13944-298">Dette gøres af systemet, når opgaverne er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="13944-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-299">O1</span><span class="sxs-lookup"><span data-stu-id="13944-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-300">K1</span><span class="sxs-lookup"><span data-stu-id="13944-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-301">QL2</span><span class="sxs-lookup"><span data-stu-id="13944-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-302">P1</span><span class="sxs-lookup"><span data-stu-id="13944-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-303">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="13944-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-304">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-305">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-306">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-307">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-308">O1</span><span class="sxs-lookup"><span data-stu-id="13944-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-309">K1</span><span class="sxs-lookup"><span data-stu-id="13944-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-310">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-311">P1</span><span class="sxs-lookup"><span data-stu-id="13944-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-312">Alle projektopgaver eller tomme</span><span class="sxs-lookup"><span data-stu-id="13944-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-313">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-314">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-315">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-316">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-317">Gyldig</span><span class="sxs-lookup"><span data-stu-id="13944-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-318">I henhold til regel nr. 5 er Q1 og Q2 to tilbud på samme salgsmulighed, så de kan begge estimere for de samme komponenter i et projekt.</span><span class="sxs-lookup"><span data-stu-id="13944-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-319">O1</span><span class="sxs-lookup"><span data-stu-id="13944-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-320">K2</span><span class="sxs-lookup"><span data-stu-id="13944-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-321">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-322">P1</span><span class="sxs-lookup"><span data-stu-id="13944-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-323">Alle projektopgaver eller tomme</span><span class="sxs-lookup"><span data-stu-id="13944-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-324">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-325">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-326">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-327">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-328">O1</span><span class="sxs-lookup"><span data-stu-id="13944-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-329">K1</span><span class="sxs-lookup"><span data-stu-id="13944-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-330">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-331">P1</span><span class="sxs-lookup"><span data-stu-id="13944-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-332">Alle projektopgaver eller tomme</span><span class="sxs-lookup"><span data-stu-id="13944-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-333">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-334">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-335">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-336">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-337">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="13944-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13944-338">I henhold til regel nr. 4 er Q1 og Q2 to tilbud på forskellige salgsmuligheder, så de kan ikke estimere for de samme komponenter i samme projekt.</span><span class="sxs-lookup"><span data-stu-id="13944-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="13944-339">O2</span><span class="sxs-lookup"><span data-stu-id="13944-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="13944-340">K1</span><span class="sxs-lookup"><span data-stu-id="13944-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="13944-341">QL1</span><span class="sxs-lookup"><span data-stu-id="13944-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-342">P1</span><span class="sxs-lookup"><span data-stu-id="13944-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="13944-343">Alle projektopgaver eller tomme</span><span class="sxs-lookup"><span data-stu-id="13944-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="13944-344">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="13944-345">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="13944-346">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="13944-347">Ja</span><span class="sxs-lookup"><span data-stu-id="13944-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
