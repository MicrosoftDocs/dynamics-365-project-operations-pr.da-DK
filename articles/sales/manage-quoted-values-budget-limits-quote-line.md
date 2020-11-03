---
title: Projektbaserede tilbudslinjer
description: Dette emne indeholder oplysninger om, hvordan du bruger projektbaserede tilbudslinjer til projektarbejde.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074039"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="be2a2-103">Projektbaserede tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="be2a2-103">Project-based quote lines</span></span>

<span data-ttu-id="be2a2-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="be2a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="be2a2-105">Projektbaserede tilbudslinjer er udviklet til at hjælpe med at vurdere projektarbejdet på en aftale.</span><span class="sxs-lookup"><span data-stu-id="be2a2-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="be2a2-106">Strukturen for en projektbaseret tilbudslinje forlænges for projektestimater med følgende koncepter:</span><span class="sxs-lookup"><span data-stu-id="be2a2-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="be2a2-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="be2a2-107">Billing Method</span></span>
- <span data-ttu-id="be2a2-108">Projekttilknytning</span><span class="sxs-lookup"><span data-stu-id="be2a2-108">Project Mapping</span></span>
- <span data-ttu-id="be2a2-109">Inkluderede transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="be2a2-109">Included Transaction classes</span></span>
- <span data-ttu-id="be2a2-110">Grænse, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="be2a2-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="be2a2-111">Opsætning af fakturerbarhed</span><span class="sxs-lookup"><span data-stu-id="be2a2-111">Chargeability setup</span></span>
- <span data-ttu-id="be2a2-112">Estimering ved hjælp af tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="be2a2-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="be2a2-113">Tilbudslinjekunder</span><span class="sxs-lookup"><span data-stu-id="be2a2-113">Quote line Customers</span></span>

<span data-ttu-id="be2a2-114">Følgende tabel indeholder oplysninger om felterne under fanen **Generelt** på den projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="be2a2-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="be2a2-115">Disse felter bruges til at konfigurere grundlaget for en detaljeret estimering overslag af projektarbejdet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="be2a2-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="be2a2-116">**Felt**</span><span class="sxs-lookup"><span data-stu-id="be2a2-116">**Field**</span></span> | <span data-ttu-id="be2a2-117">**Relevans, formål og vejledning**</span><span class="sxs-lookup"><span data-stu-id="be2a2-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="be2a2-118">**Downstream-virkning**</span><span class="sxs-lookup"><span data-stu-id="be2a2-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="be2a2-119">Navn</span><span class="sxs-lookup"><span data-stu-id="be2a2-119">Name</span></span> | <span data-ttu-id="be2a2-120">Navnet på tilbudslinjen, som kan hjælpe dig med at identificere den diskrete komponent i det tilbud, der estimeres.</span><span class="sxs-lookup"><span data-stu-id="be2a2-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="be2a2-121">Kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-122">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="be2a2-122">Billing Method</span></span> | <span data-ttu-id="be2a2-123">På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt på salgsmulighedslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="be2a2-124">Dette felt indeholder de to primære kontraherende modeller, der understøttes af Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="be2a2-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="be2a2-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="be2a2-125">- Fixed price</span></span></br><span data-ttu-id="be2a2-126">- Tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="be2a2-126">- Time and material.</span></span>| <span data-ttu-id="be2a2-127">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-128">Project</span><span class="sxs-lookup"><span data-stu-id="be2a2-128">Project</span></span> | <span data-ttu-id="be2a2-129">Brug dette valgfrie felt til at identificere det projekt, der skal bruges til at levere arbejdet på denne aftale.</span><span class="sxs-lookup"><span data-stu-id="be2a2-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="be2a2-130">Når et projekt knyttes til en tilbudslinje, kan det hjælpe med konfigurationen af fakturerbare opgaver og også til at udarbejde et projektbaseret estimat over tilbudslinjen som tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="be2a2-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="be2a2-131">Når et projekt ikke er knyttet til en projektbaseret tilbudslinje, skal estimatet oprettes manuelt ved at oprette hver enkelt tilbudslinjedetalje.</span><span class="sxs-lookup"><span data-stu-id="be2a2-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="be2a2-132">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-133">Medtag tid</span><span class="sxs-lookup"><span data-stu-id="be2a2-133">Include Time</span></span> | <span data-ttu-id="be2a2-134">Et flag med **Ja**/**Nej** indikerer, om tidstransaktioner eller arbejdskraftomkostninger på de valgte projekter inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="be2a2-135">En værdi med **Nej** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="be2a2-136">En værdi med **Ja** indikerer, at tidstransaktionerne eller arbejdskraftomkostningerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="be2a2-137">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-138">Medtag udgift</span><span class="sxs-lookup"><span data-stu-id="be2a2-138">Include Expense</span></span> | <span data-ttu-id="be2a2-139">Et flag med **Ja**/**Nej** indikerer, om udgiftsomkostningerne på de valgte projekter inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="be2a2-140">En værdi med **Nej** indikerer, at udgiftsomkostningerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="be2a2-141">En værdi med **Ja** indikerer, at udgiftsomkostningerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="be2a2-142">Denne feltværdi kopieres over i den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-143">Medtag gebyr</span><span class="sxs-lookup"><span data-stu-id="be2a2-143">Include Fee</span></span> | <span data-ttu-id="be2a2-144">Et flag med **Ja**/**Nej** indikerer, om gebyrerne på de valgte projekter inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="be2a2-145">En værdi med **Nej** indikerer, at gebyrerne ikke inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="be2a2-146">En værdi med **Ja** indikerer, at gebyrerne inkluderes i estimatet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="be2a2-147">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-148">Tilbudsbeløb</span><span class="sxs-lookup"><span data-stu-id="be2a2-148">Quoted Amount</span></span> | <span data-ttu-id="be2a2-149">Dette er det beløb, som vil blive tilbudt kunden for alt arbejde, der er anslået for denne projektbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="be2a2-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="be2a2-150">På et tilbud, der er oprettet ud fra en salgsmulighed, kopieres denne værdi fra det tilsvarende felt **Kundebudget** på salgsmulighedslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="be2a2-151">Når den projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til beløbet i detaljerne i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="be2a2-152">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-153">Anslået moms</span><span class="sxs-lookup"><span data-stu-id="be2a2-153">Estimated Tax</span></span> | <span data-ttu-id="be2a2-154">Dette felt er et redigerbart felt, hvor brugeren kan tilføje det anslåede momsbeløb på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="be2a2-155">Når en projektbaserede tilbudslinje indeholder linjedetaljer, er dette felt låst mod redigering og opsummeres i forhold til momsbeløbet i detaljerne i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="be2a2-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="be2a2-156">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-157">Tilbudsbeløb efter moms</span><span class="sxs-lookup"><span data-stu-id="be2a2-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="be2a2-158">Dette felt er tilbudslinjebeløbet efter moms og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="be2a2-159">Beløbet i dette felt beregnes som *Tilbudsbeløb + moms*.</span><span class="sxs-lookup"><span data-stu-id="be2a2-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="be2a2-160">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-161">Grænse, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="be2a2-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="be2a2-162">Dette felt kan redigeres og er kun tilgængeligt for projektbaserede tilbudslinjer med faktureringsmetoden **Tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="be2a2-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="be2a2-163">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="be2a2-164">Kundebudget</span><span class="sxs-lookup"><span data-stu-id="be2a2-164">Customer Budget</span></span> | <span data-ttu-id="be2a2-165">Dette felt kan redigeres og kopieres fra det tilsvarende felt på salgsmulighedslinjen, hvis tilbuddet blev oprettet ud fra en salgsmulighed.</span><span class="sxs-lookup"><span data-stu-id="be2a2-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="be2a2-166">Denne feltværdi kopieres til den projektkontraktlinje, der er oprettet ud fra denne tilbudslinje, når tilbuddet er vundet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="be2a2-167">Valideringsregler for felter under fanen Generelt på projektbaserede tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="be2a2-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="be2a2-168">**Regel 1** : En bestemt transaktionsklasse i det valgte projekt kan kun inkluderes på én projektbaseret tilbudslinje i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="be2a2-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="be2a2-169">**Regel 2** : Hvis en salgsmulighed har flere tilbud, kan der være tilbudslinjer fra forskellige tilbud, der alle refererer til det samme projekt, og som inkluderer samme transaktionsklasse.</span><span class="sxs-lookup"><span data-stu-id="be2a2-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="be2a2-170">**Regel 3** : Hvis de pågældende tilbud ikke hører til samme salgsmulighed, kan de ikke indeholde samme projekt- og transaktionsklasse.</span><span class="sxs-lookup"><span data-stu-id="be2a2-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="be2a2-171">
                    <strong>Salgsmulighed</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="be2a2-172">
                    <strong>Tilbud</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="be2a2-173">
                    <strong>Tilbudslinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="be2a2-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="be2a2-175">
                    <strong>Medtag tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="be2a2-176">
                    <strong>Medtag udgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="be2a2-177">
                    <strong>Medtag</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="be2a2-178">
                    <strong>gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="be2a2-179">
                    <strong>Gyldig/ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="be2a2-180">
                    <strong>Årsag</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be2a2-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="be2a2-181">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-182">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-183">QL1</span><span class="sxs-lookup"><span data-stu-id="be2a2-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-184">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-185">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-186">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-187">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-188">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="be2a2-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-189">Overtrædelse af regel #1.</span><span class="sxs-lookup"><span data-stu-id="be2a2-189">Violation of Rule #1.</span></span> <span data-ttu-id="be2a2-190">Tid, udgifter og gebyrer på P1-projektet medtages på både tilbudslinjer, QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="be2a2-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="be2a2-191">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-192">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-193">QL2</span><span class="sxs-lookup"><span data-stu-id="be2a2-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-194">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-195">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-196">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-197">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-197">Yes</span></span> </p>
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
<span data-ttu-id="be2a2-198">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-199">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-200">QL1</span><span class="sxs-lookup"><span data-stu-id="be2a2-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-201">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-202">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-203">Nr.</span><span class="sxs-lookup"><span data-stu-id="be2a2-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-204">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-205">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="be2a2-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-206">Overtrædelse af regel #1.</span><span class="sxs-lookup"><span data-stu-id="be2a2-206">Violation of Rule #1.</span></span> <span data-ttu-id="be2a2-207">Tid og gebyrer på P1-projektet medtages på både tilbudslinjer, QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="be2a2-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="be2a2-208">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-209">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-210">QL2</span><span class="sxs-lookup"><span data-stu-id="be2a2-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-211">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-212">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-213">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-214">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-214">Yes</span></span> </p>
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
<span data-ttu-id="be2a2-215">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-216">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-217">QL1</span><span class="sxs-lookup"><span data-stu-id="be2a2-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-218">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-219">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-220">Nr.</span><span class="sxs-lookup"><span data-stu-id="be2a2-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-221">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-222">Gyldig</span><span class="sxs-lookup"><span data-stu-id="be2a2-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="be2a2-223">Tid og gebyrer på P1-projektet er medtaget i QL1.</span><span class="sxs-lookup"><span data-stu-id="be2a2-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="be2a2-224">Udgift til P1-projekt er inkluderet i QL2.</span><span class="sxs-lookup"><span data-stu-id="be2a2-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="be2a2-225">Der findes ingen overlapning i det, der medtages på hver tilbudslinje, så den er gyldig.</span><span class="sxs-lookup"><span data-stu-id="be2a2-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="be2a2-226">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-227">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-228">QL2</span><span class="sxs-lookup"><span data-stu-id="be2a2-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-229">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-230">Nr.</span><span class="sxs-lookup"><span data-stu-id="be2a2-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-231">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="be2a2-232">No</span></span> </p>
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
<span data-ttu-id="be2a2-233">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-234">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-235">QL1</span><span class="sxs-lookup"><span data-stu-id="be2a2-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-236">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-237">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-238">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-239">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-240">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="be2a2-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-241">Overtrædelse af regel #1 ovenfor</span><span class="sxs-lookup"><span data-stu-id="be2a2-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="be2a2-242">Q1 inkluderer tid, udgifter og gebyrer for hele P1-projektet.</span><span class="sxs-lookup"><span data-stu-id="be2a2-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="be2a2-243">QL2 inkluderer tid, udgifter og gebyrer for hele P1-projektet P1 og overlapper med det, der er inkluderet i Q1.</span><span class="sxs-lookup"><span data-stu-id="be2a2-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="be2a2-244">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-245">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-246">QL2</span><span class="sxs-lookup"><span data-stu-id="be2a2-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-247">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-248">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-249">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-250">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-250">Yes</span></span> </p>
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
<span data-ttu-id="be2a2-251">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-252">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-253">QL1</span><span class="sxs-lookup"><span data-stu-id="be2a2-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-254">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-255">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-256">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-257">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="be2a2-258">Gyldig</span><span class="sxs-lookup"><span data-stu-id="be2a2-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-259">Afhængigt af regel #2, Q1 og Q2 er der to tilbud på samme salgsmulighed, så de begge kan estimerer for de samme komponenter i et projekt.</span><span class="sxs-lookup"><span data-stu-id="be2a2-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="be2a2-260">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-261">K2</span><span class="sxs-lookup"><span data-stu-id="be2a2-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-262">QL1 på Q2</span><span class="sxs-lookup"><span data-stu-id="be2a2-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-263">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-264">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-265">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-266">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-266">Yes</span></span> </p>
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
<span data-ttu-id="be2a2-267">O1</span><span class="sxs-lookup"><span data-stu-id="be2a2-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-268">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-269">QL1</span><span class="sxs-lookup"><span data-stu-id="be2a2-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-270">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-271">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-272">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-273">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="be2a2-274">Gyldig</span><span class="sxs-lookup"><span data-stu-id="be2a2-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be2a2-275">Afhængigt af regel #3, Q1 og Q2 er der to tilbud på forskellige salgsmuligheder, så de kan ikke estimerer for de samme komponenter i det samme projekt.</span><span class="sxs-lookup"><span data-stu-id="be2a2-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="be2a2-276">O2</span><span class="sxs-lookup"><span data-stu-id="be2a2-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="be2a2-277">K1</span><span class="sxs-lookup"><span data-stu-id="be2a2-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-278">QL1</span><span class="sxs-lookup"><span data-stu-id="be2a2-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-279">P1</span><span class="sxs-lookup"><span data-stu-id="be2a2-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-280">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="be2a2-281">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="be2a2-282">Ja</span><span class="sxs-lookup"><span data-stu-id="be2a2-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="be2a2-283">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="be2a2-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

