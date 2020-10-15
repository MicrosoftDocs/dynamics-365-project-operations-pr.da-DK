---
title: Projektbaserede tilbudslinjer (Pro)
description: Dette emne indeholder oplysninger om, hvordan du bruger projektbaserede tilbudslinjer til projektarbejde. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908013"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="c0f38-104">Projektbaserede tilbudslinjer (Pro)</span><span class="sxs-lookup"><span data-stu-id="c0f38-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="c0f38-105">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c0f38-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c0f38-106">Projektbaserede tilbudslinjer er udviklet til at hjælpe med at vurdere projektarbejdet på en aftale.</span><span class="sxs-lookup"><span data-stu-id="c0f38-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="c0f38-107">Strukturen for en projektbaseret tilbudslinje forlænges for projektestimater med følgende koncepter:</span><span class="sxs-lookup"><span data-stu-id="c0f38-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="c0f38-108">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="c0f38-108">Billing Method</span></span>
- <span data-ttu-id="c0f38-109">Projekt- og opgavetilknytning</span><span class="sxs-lookup"><span data-stu-id="c0f38-109">Project and Task Mapping</span></span>
- <span data-ttu-id="c0f38-110">Inkluderede transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="c0f38-110">Included Transaction classes</span></span>
- <span data-ttu-id="c0f38-111">Grænse, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="c0f38-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="c0f38-112">Opsætning af fakturerbarhed</span><span class="sxs-lookup"><span data-stu-id="c0f38-112">Chargeability setup</span></span>
- <span data-ttu-id="c0f38-113">Estimering ved hjælp af tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="c0f38-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="c0f38-114">Tilbudslinjekunder</span><span class="sxs-lookup"><span data-stu-id="c0f38-114">Quote line Customers</span></span>

<span data-ttu-id="c0f38-115">Følgende tabel indeholder oplysninger om felterne under fanen **Generelt** på den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="c0f38-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="c0f38-116">Disse felter bruges til at konfigurere grundlaget for en detaljeret estimering overslag af projektarbejdet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="c0f38-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="c0f38-117">**Felt**</span><span class="sxs-lookup"><span data-stu-id="c0f38-117">**Field**</span></span> | <span data-ttu-id="c0f38-118">**Relevans, formål og vejledning**</span><span class="sxs-lookup"><span data-stu-id="c0f38-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="c0f38-119">**Downstream-virkning**</span><span class="sxs-lookup"><span data-stu-id="c0f38-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c0f38-120">Navn</span><span class="sxs-lookup"><span data-stu-id="c0f38-120">Name</span></span> | <span data-ttu-id="c0f38-121">Navnet på tilbudslinjen, som kan hjælpe dig med at identificere den diskrete komponent i det tilbud, der estimeres.</span><span class="sxs-lookup"><span data-stu-id="c0f38-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="c0f38-122">Kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-123">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="c0f38-123">Billing Method</span></span> | <span data-ttu-id="c0f38-124">På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt på salgsmulighedslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="c0f38-125">Dette felt indeholder de to primære kontraherende modeller, der understøttes af Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="c0f38-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="c0f38-126">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="c0f38-126">- Fixed price</span></span></br><span data-ttu-id="c0f38-127">- Tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="c0f38-127">- Time and material.</span></span>| <span data-ttu-id="c0f38-128">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-129">Project</span><span class="sxs-lookup"><span data-stu-id="c0f38-129">Project</span></span> | <span data-ttu-id="c0f38-130">Brug dette valgfrie felt til at identificere det projekt, der skal bruges til at levere arbejdet på denne aftale.</span><span class="sxs-lookup"><span data-stu-id="c0f38-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="c0f38-131">Når et projekt knyttes til en tilbudslinje, kan det hjælpe med konfigurationen af fakturerbare opgaver og også til at udarbejde et projektbaseret estimat over tilbudslinjen som tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="c0f38-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="c0f38-132">Når et projekt ikke er knyttet til en projektbaseret tilbudslinje, skal estimatet oprettes manuelt ved at oprette hver enkelt tilbudslinjedetalje.</span><span class="sxs-lookup"><span data-stu-id="c0f38-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="c0f38-133">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="c0f38-134">Inkluderede opgaver</span><span class="sxs-lookup"><span data-stu-id="c0f38-134">Included Tasks</span></span> | <span data-ttu-id="c0f38-135">Angiver, om denne tilbudslinje bruges til alle eller nogle af projektopgaverne for det valgte projekt.</span><span class="sxs-lookup"><span data-stu-id="c0f38-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="c0f38-136">Dette felt har følgende mulige værdier:</span><span class="sxs-lookup"><span data-stu-id="c0f38-136">This field has the following possible values:</span></span></br><span data-ttu-id="c0f38-137">- Alle projektopgaver</span><span class="sxs-lookup"><span data-stu-id="c0f38-137">- All project tasks</span></span></br><span data-ttu-id="c0f38-138">- Kun valgte projektopgaver</span><span class="sxs-lookup"><span data-stu-id="c0f38-138">- Selected project tasks only</span></span></br><span data-ttu-id="c0f38-139">En tom værdi i dette felt svarer til indstillingen **Alle projektopgaver**.</span><span class="sxs-lookup"><span data-stu-id="c0f38-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="c0f38-140">Når du har valgt **Kun valgte projektopgaver** på projektsiden, kan du på fanen **Opsætning af opgavefakturering** vælge specifikke opgaver, der skal tilknyttes disse tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="c0f38-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="c0f38-141">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-142">Medtag tid</span><span class="sxs-lookup"><span data-stu-id="c0f38-142">Include Time</span></span> | <span data-ttu-id="c0f38-143">Et flag med **Ja**/**Nej** indikerer, om tidstransaktioner eller arbejdskraftomkostninger på de valgte projekter inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0f38-144">En værdi med **Nej** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0f38-145">En værdi med **Ja** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c0f38-146">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-147">Medtag udgift</span><span class="sxs-lookup"><span data-stu-id="c0f38-147">Include Expense</span></span> | <span data-ttu-id="c0f38-148">Et flag med **Ja**/**Nej** indikerer, om udgiftsomkostningerne på de valgte projekter inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0f38-149">En værdi med **Nej** indikerer, at udgiftsomkostningerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0f38-150">En værdi med **Ja** indikerer, at udgiftsomkostningerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c0f38-151">Denne feltværdi kopieres over i den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-152">Medtag gebyr</span><span class="sxs-lookup"><span data-stu-id="c0f38-152">Include Fee</span></span> | <span data-ttu-id="c0f38-153">Et flag med **Ja**/**Nej** indikerer, om gebyrerne på de valgte projekter inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0f38-154">En værdi med **Nej** indikerer, at gebyrerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0f38-155">En værdi med **Ja** indikerer, at gebyrerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c0f38-156">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-157">Tilbudsbeløb</span><span class="sxs-lookup"><span data-stu-id="c0f38-157">Quoted Amount</span></span> | <span data-ttu-id="c0f38-158">Dette er det beløb, som vil blive tilbudt kunden for alt arbejde, der er anslået for denne projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="c0f38-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="c0f38-159">På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt **Kundebudget** på salgsmulighedslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="c0f38-160">Når den projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til beløbet i detaljerne i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="c0f38-161">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-162">Anslået moms</span><span class="sxs-lookup"><span data-stu-id="c0f38-162">Estimated Tax</span></span> | <span data-ttu-id="c0f38-163">Dette felt er et redigerbart felt, hvor brugeren kan tilføje det anslåede momsbeløb på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="c0f38-164">Når en projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til momsbeløbet i detaljerne i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="c0f38-165">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-166">Tilbudsbeløb efter moms</span><span class="sxs-lookup"><span data-stu-id="c0f38-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="c0f38-167">Dette felt er tilbudslinjebeløbet efter moms og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="c0f38-168">Beløbet i dette felt beregnes som *Tilbudsbeløb + moms*.</span><span class="sxs-lookup"><span data-stu-id="c0f38-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="c0f38-169">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-170">Grænse, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="c0f38-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="c0f38-171">Dette felt kan redigeres og er kun tilgængeligt for projektbaserede tilbudslinjer med faktureringsmetoden **Tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="c0f38-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="c0f38-172">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0f38-173">Kundebudget</span><span class="sxs-lookup"><span data-stu-id="c0f38-173">Customer Budget</span></span> | <span data-ttu-id="c0f38-174">Dette felt kan redigeres og kopieres fra det tilsvarende felt på salgsmulighedslinjen, hvis tilbuddet blev oprettet ud fra en salgsmulighed.</span><span class="sxs-lookup"><span data-stu-id="c0f38-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="c0f38-175">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="c0f38-176">Valideringsregler for felter under fanen Generelt på projektbaserede tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="c0f38-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="c0f38-177">**Regel 1**: Hvis feltet **Inkluderede opgaver** er tomt, eller hvis det er angivet til **Alle projektopgaver**, medtages der et projekt i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c0f38-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="c0f38-178">**Regel 2**: Hvis feltet **Inkluderede opgaver** er tomt, eller hvis det er angivet til **Alle projektopgaver**, kan et projekt og en bestemt transaktionsklasse kun inkluderes på én projektbaseret tilbudslinje for et tilbud.</span><span class="sxs-lookup"><span data-stu-id="c0f38-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="c0f38-179">**Regel 3**: Hvis feltet **Inkluderede opgaver** er angivet til **Kun valgte projektopgaver**, kan et projekt og en bestemt transaktionsklasse inkluderes på flere projektbaseret tilbudslinjer for et tilbud.</span><span class="sxs-lookup"><span data-stu-id="c0f38-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="c0f38-180">**Regel 4**: Hvis en salgsmulighed har flere tilbud, kan der være tilbudslinjer fra forskellige tilbud, der alle refererer til det samme projekt, og som inkluderer samme transaktionsklasse.</span><span class="sxs-lookup"><span data-stu-id="c0f38-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="c0f38-181">**Regel 5**: Hvis de pågældende tilbud ikke hører til samme salgsmulighed, kan de ikke indeholde samme projekt- og transaktionsklasse.</span><span class="sxs-lookup"><span data-stu-id="c0f38-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="c0f38-182">
                    <strong>Salgsmulighed</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c0f38-183">
                    <strong>Tilbud</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c0f38-184">
                    <strong>Tilbudslinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c0f38-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="c0f38-186">
                    <strong>Inkluderede opgaver</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c0f38-187">
                    <strong>Medtag tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c0f38-188">
                    <strong>Medtag udgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c0f38-189">
                    <strong>Medtag</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="c0f38-190">
                    <strong>Gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="c0f38-191">
                    <strong>Gyldig/ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="c0f38-192">
                    <strong>Årsag</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0f38-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-193">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-194">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-195">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-196">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-197">Tom</span><span class="sxs-lookup"><span data-stu-id="c0f38-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-198">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-199">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-200">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-201">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="c0f38-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-202">Overtrædelse af regel #2.</span><span class="sxs-lookup"><span data-stu-id="c0f38-202">Violation of Rule #2.</span></span> <span data-ttu-id="c0f38-203">Tid, udgifter og gebyrer på P1-projektet medtages på tilbudslinjerne QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="c0f38-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-204">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-205">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-206">QL2</span><span class="sxs-lookup"><span data-stu-id="c0f38-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-207">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-208">Tom</span><span class="sxs-lookup"><span data-stu-id="c0f38-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-209">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-210">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-211">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-212">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-213">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-214">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-215">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-216">Tom</span><span class="sxs-lookup"><span data-stu-id="c0f38-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-217">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-218">Nr.</span><span class="sxs-lookup"><span data-stu-id="c0f38-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-219">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-220">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="c0f38-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-221">Overtrædelse af regel #2.</span><span class="sxs-lookup"><span data-stu-id="c0f38-221">Violation of Rule #2.</span></span> <span data-ttu-id="c0f38-222">Tid og gebyrer på P1-projektet medtages på tilbudslinjerne QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="c0f38-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-223">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-224">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-225">QL2</span><span class="sxs-lookup"><span data-stu-id="c0f38-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-226">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-227">Tom</span><span class="sxs-lookup"><span data-stu-id="c0f38-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-228">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-229">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-230">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-231">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-232">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-233">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-234">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-235">Tom</span><span class="sxs-lookup"><span data-stu-id="c0f38-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-236">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-237">Nr.</span><span class="sxs-lookup"><span data-stu-id="c0f38-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-238">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-239">Gyldig</span><span class="sxs-lookup"><span data-stu-id="c0f38-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="c0f38-240">Tid og gebyrer på P1-projektet er medtaget i QL1.</span><span class="sxs-lookup"><span data-stu-id="c0f38-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="c0f38-241">Udgift til P1-projekt er inkluderet i QL2.</span><span class="sxs-lookup"><span data-stu-id="c0f38-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="c0f38-242">Der findes ingen overlapning i det, der medtages på hver tilbudslinje og er gyldig.</span><span class="sxs-lookup"><span data-stu-id="c0f38-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-243">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-244">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-245">QL2</span><span class="sxs-lookup"><span data-stu-id="c0f38-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-246">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-247">Tom</span><span class="sxs-lookup"><span data-stu-id="c0f38-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-248">Nr.</span><span class="sxs-lookup"><span data-stu-id="c0f38-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-249">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-250">Nr.</span><span class="sxs-lookup"><span data-stu-id="c0f38-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-251">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-252">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-253">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-254">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-255">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="c0f38-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-256">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-257">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-258">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-259">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="c0f38-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-260">Overtrædelse af regel #2 ovenfor</span><span class="sxs-lookup"><span data-stu-id="c0f38-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="c0f38-261">Q1 inkluderer tid, udgifter og gebyrer i et undersæt af opgaver på projektet P1.</span><span class="sxs-lookup"><span data-stu-id="c0f38-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c0f38-262">QL2 inkluderer tid, udgifter og gebyrer for hele P1-projektet P1 og overlapper med det, der er inkluderet i Q1.</span><span class="sxs-lookup"><span data-stu-id="c0f38-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-263">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-264">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-265">QL2</span><span class="sxs-lookup"><span data-stu-id="c0f38-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-266">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-267">Tom</span><span class="sxs-lookup"><span data-stu-id="c0f38-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-268">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-269">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-270">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-271">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-272">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-273">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-274">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-275">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="c0f38-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-276">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-277">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-278">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-279">Gyldig</span><span class="sxs-lookup"><span data-stu-id="c0f38-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-280">I henhold til regel #3 ovenfor,</span><span class="sxs-lookup"><span data-stu-id="c0f38-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="c0f38-281">Q1 inkluderer tid, udgifter og gebyrer i et undersæt af opgaver på projektet P1.</span><span class="sxs-lookup"><span data-stu-id="c0f38-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c0f38-282">QL2 inkluderer tid, udgifter og gebyrer for et undersæt af opgaver på projektet P1.</span><span class="sxs-lookup"><span data-stu-id="c0f38-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c0f38-283">Den eneste yderligere validering sker ved hjælp af undersættet af opgaver i QL1, som er forskellige fra undersættet af opgaver i QL2.</span><span class="sxs-lookup"><span data-stu-id="c0f38-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="c0f38-284">Dette sikrer, at der ikke er overlap.</span><span class="sxs-lookup"><span data-stu-id="c0f38-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="c0f38-285">Dette gøres af systemet, når opgaverne er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="c0f38-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-286">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-287">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-288">QL2</span><span class="sxs-lookup"><span data-stu-id="c0f38-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-289">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-290">Kun valgte opgaver</span><span class="sxs-lookup"><span data-stu-id="c0f38-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-291">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-292">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-293">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-294">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-295">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-296">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-297">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-298">Alle projektopgaver eller tomme</span><span class="sxs-lookup"><span data-stu-id="c0f38-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-299">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-300">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-301">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c0f38-302">Gyldig</span><span class="sxs-lookup"><span data-stu-id="c0f38-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-303">Afhængigt af regel #5, Q1 og Q2 er der to tilbud på samme salgsmulighed, så de begge kan estimerer for de samme komponenter i et projekt.</span><span class="sxs-lookup"><span data-stu-id="c0f38-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-304">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-305">K2</span><span class="sxs-lookup"><span data-stu-id="c0f38-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-306">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-307">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-308">Alle projektopgaver eller tomme</span><span class="sxs-lookup"><span data-stu-id="c0f38-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-309">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-310">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-311">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-312">O1</span><span class="sxs-lookup"><span data-stu-id="c0f38-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-313">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-314">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-315">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-316">Alle projektopgaver eller tomme</span><span class="sxs-lookup"><span data-stu-id="c0f38-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-317">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-318">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-319">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c0f38-320">Gyldig</span><span class="sxs-lookup"><span data-stu-id="c0f38-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0f38-321">Afhængigt af regel #4, Q1 og Q2 er der to tilbud på forskellige salgsmuligheder, så de kan ikke estimerer for de samme komponenter i det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="c0f38-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0f38-322">O2</span><span class="sxs-lookup"><span data-stu-id="c0f38-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0f38-323">K1</span><span class="sxs-lookup"><span data-stu-id="c0f38-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-324">QL1</span><span class="sxs-lookup"><span data-stu-id="c0f38-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-325">P1</span><span class="sxs-lookup"><span data-stu-id="c0f38-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c0f38-326">Alle projektopgaver eller tomme</span><span class="sxs-lookup"><span data-stu-id="c0f38-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-327">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0f38-328">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0f38-329">Ja</span><span class="sxs-lookup"><span data-stu-id="c0f38-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c0f38-330">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="c0f38-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

