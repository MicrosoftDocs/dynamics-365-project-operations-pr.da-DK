---
title: Faktiske
description: Dette emne indeholder oplysninger om, hvordan du arbejder med faktiske oplysninger i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126296"
---
# <a name="actuals"></a><span data-ttu-id="4ae99-103">Faktiske</span><span class="sxs-lookup"><span data-stu-id="4ae99-103">Actuals</span></span> 

<span data-ttu-id="4ae99-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="4ae99-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4ae99-105">Faktiske oplysninger er mængden af arbejde, der er udført på et projekt.</span><span class="sxs-lookup"><span data-stu-id="4ae99-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="4ae99-106">De oprettes som et resultat af tids- og udgiftsposter samt kladdeposteringer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="4ae99-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="4ae99-107">Kladdelinjer og tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="4ae99-107">Journal lines and time submission</span></span>

<span data-ttu-id="4ae99-108">Du kan finde flere oplysninger om tidsregistrering under [Oversigt over tidsregistrering](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4ae99-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="4ae99-109">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="4ae99-109">Time and materials</span></span>

<span data-ttu-id="4ae99-110">Når en afsendt tidsregistrering hænger sammen med et projekt, der er knyttet til en tids- og materialekontraktlinje, oprettes der to kladdelinjer i systemet, en for kostpris og én for ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="4ae99-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="4ae99-111">Fast pris</span><span class="sxs-lookup"><span data-stu-id="4ae99-111">Fixed price</span></span>

<span data-ttu-id="4ae99-112">Når en indsendt tidsregistrering er forbundet med et projekt, der er knyttet til en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostninger.</span><span class="sxs-lookup"><span data-stu-id="4ae99-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="4ae99-113">Standardprisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="4ae99-113">Default pricing</span></span>

<span data-ttu-id="4ae99-114">Logikken for oprettelse af standardpriser findes på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="4ae99-115">Feltværdierne fra tidsregistreringen kopieres til kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="4ae99-116">Disse værdier inkluderer datoen for transaktionen, den kontraktlinje, som projektet er knyttet til, og valutaresultatet i den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="4ae99-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="4ae99-117">De felter, der påvirker standardprisfastsættelser som f.eks **Rolle** og **Organisationsenhed**, anvendes til at fastsætte en passende pris på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="4ae99-118">Du kan tilføje et brugerdefineret felt på tidsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="4ae99-119">Hvis du ønsker, at feltværdien skal overføres til faktiske værdier, skal du oprette feltet på objektet Faktiske og bruge felttilknytninger til at kopiere feltet fra tidsregistreringen til den faktiske værdi.</span><span class="sxs-lookup"><span data-stu-id="4ae99-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="4ae99-120">Kladdelinjer og indsendelse af grundlæggende udgifter</span><span class="sxs-lookup"><span data-stu-id="4ae99-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="4ae99-121">Du kan finde flere oplysninger om udgiftsregistrering under [Oversigt over udgifter](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4ae99-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="4ae99-122">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="4ae99-122">Time and materials</span></span>

<span data-ttu-id="4ae99-123">Når en grundlæggende udgiftspost hænger sammen med et projekt, der er knyttet til en tids- og materialekontraktlinje, oprettes der to kladdelinjer i systemet, en for kostpris og én for ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="4ae99-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="4ae99-124">Fast pris</span><span class="sxs-lookup"><span data-stu-id="4ae99-124">Fixed price</span></span>

<span data-ttu-id="4ae99-125">Når en grundlæggende udgiftspost er forbundet med et projekt, der er knyttet til en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostninger.</span><span class="sxs-lookup"><span data-stu-id="4ae99-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="4ae99-126">Standardprisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="4ae99-126">Default pricing</span></span>

<span data-ttu-id="4ae99-127">Logikken for angivelse af standardpriser for udgifter er baseret på udgiftskategorien.</span><span class="sxs-lookup"><span data-stu-id="4ae99-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="4ae99-128">Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="4ae99-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="4ae99-129">Det beløb, som brugeren har indtastet, for selve prisen er dog som standard angivet direkte på de relaterede udgiftskladdelinjer for omkostning og salg.</span><span class="sxs-lookup"><span data-stu-id="4ae99-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="4ae99-130">Den kategoribaserede angivelse af standardpriser pr. enhed for udgiftsposter er ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="4ae99-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="4ae99-131">Brug posteringskladder til registrering af omkostninger</span><span class="sxs-lookup"><span data-stu-id="4ae99-131">Use entry journals to record costs</span></span>

<span data-ttu-id="4ae99-132">Du kan anvende posteringskladder til at registrere omkostningerne eller indtægterne i materiale-, gebyr-, time-, udgifts- eller momstransaktionsklasser.</span><span class="sxs-lookup"><span data-stu-id="4ae99-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="4ae99-133">Kladder kan bruges til følgende formål:</span><span class="sxs-lookup"><span data-stu-id="4ae99-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="4ae99-134">Registrering af de faktiske omkostninger til materialer og salg i et projekt.</span><span class="sxs-lookup"><span data-stu-id="4ae99-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="4ae99-135">Flyt faktiske transaktionsoplysninger fra et andet system til Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4ae99-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="4ae99-136">Registrer omkostninger, der er opstået i et andet system.</span><span class="sxs-lookup"><span data-stu-id="4ae99-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="4ae99-137">Disse omkostninger kan inkludere udgifter til indkøb eller underleverandører.</span><span class="sxs-lookup"><span data-stu-id="4ae99-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ae99-138">Applikationen validerer ikke kladdelinjetypen eller den relaterede prisfastsættelse, der er angivet på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="4ae99-139">Derfor er det kun en bruger, der er fuldt bekendt med den regnskabsmæssige indvirkning, som faktiske værdier har på projektet, der skal bruge posteringskladder til at oprette faktiske værdier.</span><span class="sxs-lookup"><span data-stu-id="4ae99-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="4ae99-140">Som følge af virkningen af denne kladdetype skal du omhyggeligt vælge, hvem der har adgang til at oprette posteringskladder.</span><span class="sxs-lookup"><span data-stu-id="4ae99-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="4ae99-141">Registrer faktiske oplysninger baseret på projekthændelser</span><span class="sxs-lookup"><span data-stu-id="4ae99-141">Record actuals based on project events</span></span>

<span data-ttu-id="4ae99-142">Project Operations registrerer de økonomiske transaktioner, der sker i løbet af et projekt.</span><span class="sxs-lookup"><span data-stu-id="4ae99-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="4ae99-143">Disse transaktioner registreres som faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="4ae99-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="4ae99-144">I følgende tabel vises de forskellige typer af faktiske oplysninger, der oprettes, afhængigt af, om projektet er tid-og-materiale- eller fastprisprojekt, er i fasen presales eller er et internt projekt.</span><span class="sxs-lookup"><span data-stu-id="4ae99-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="4ae99-145">Ressourcen tilhører samme afdeling som projektets kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4ae99-146">Hændelse</span><span class="sxs-lookup"><span data-stu-id="4ae99-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4ae99-147">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="4ae99-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4ae99-148">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="4ae99-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4ae99-149">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="4ae99-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4ae99-150">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="4ae99-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4ae99-151">Fast pris</span><span class="sxs-lookup"><span data-stu-id="4ae99-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4ae99-152">Faktiske</span><span class="sxs-lookup"><span data-stu-id="4ae99-152">Actuals</span></span></th>
<th><span data-ttu-id="4ae99-153">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-153">Transaction currency</span></span></th>
<th><span data-ttu-id="4ae99-154">Fast pris</span><span class="sxs-lookup"><span data-stu-id="4ae99-154">Fixed price</span></span></th>
<th><span data-ttu-id="4ae99-155">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4ae99-156">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="4ae99-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4ae99-157">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="4ae99-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-158">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="4ae99-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4ae99-159">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="4ae99-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4ae99-160">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4ae99-161">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-161">Cost actual</span></span></td>
<td><span data-ttu-id="4ae99-162">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-163">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-164">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="4ae99-165">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-166">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-167">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="4ae99-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4ae99-168">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4ae99-169">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4ae99-170">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-170">Cost actual</span></span></td>
<td><span data-ttu-id="4ae99-171">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-172">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-173">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-174">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-175">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-176">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="4ae99-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4ae99-177">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-178">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="4ae99-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4ae99-179">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4ae99-180">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="4ae99-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4ae99-181">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4ae99-182">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-183">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="4ae99-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-184">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-185">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-186">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-187">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-187">Billed sales</span></span></td>
<td><span data-ttu-id="4ae99-188">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4ae99-189">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="4ae99-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4ae99-190">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4ae99-191">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-192">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-193">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-194">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-195">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-196">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="4ae99-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4ae99-197">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-198">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="4ae99-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4ae99-199">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4ae99-200">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="4ae99-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4ae99-201">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="4ae99-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4ae99-202">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4ae99-203">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="4ae99-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4ae99-204">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="4ae99-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4ae99-205">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4ae99-206">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4ae99-207">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-208">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-208">Billed sales</span></span></td>
<td><span data-ttu-id="4ae99-209">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4ae99-210">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="4ae99-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4ae99-211">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="4ae99-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4ae99-212">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-213">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="4ae99-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4ae99-214">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-215">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="4ae99-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4ae99-216">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="4ae99-217">Ressourcen tilhører en afdeling, som er forskellig fra projektets kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4ae99-218">Hændelse</span><span class="sxs-lookup"><span data-stu-id="4ae99-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4ae99-219">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="4ae99-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4ae99-220">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="4ae99-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4ae99-221">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="4ae99-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4ae99-222">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="4ae99-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4ae99-223">Fast pris</span><span class="sxs-lookup"><span data-stu-id="4ae99-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4ae99-224">Faktiske</span><span class="sxs-lookup"><span data-stu-id="4ae99-224">Actuals</span></span></th>
<th><span data-ttu-id="4ae99-225">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-225">Transaction currency</span></span></th>
<th><span data-ttu-id="4ae99-226">Fast pris</span><span class="sxs-lookup"><span data-stu-id="4ae99-226">Fixed price</span></span></th>
<th><span data-ttu-id="4ae99-227">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4ae99-228">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="4ae99-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4ae99-229">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="4ae99-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-230">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="4ae99-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4ae99-231">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="4ae99-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="4ae99-232">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4ae99-233">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-233">Cost actual</span></span></td>
<td><span data-ttu-id="4ae99-234">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4ae99-235">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4ae99-236">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4ae99-237">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4ae99-238">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-239">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="4ae99-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4ae99-240">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-241">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4ae99-242">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-243">Internt salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4ae99-244">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="4ae99-245">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="4ae99-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4ae99-246">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-246">Cost actual</span></span></td>
<td><span data-ttu-id="4ae99-247">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4ae99-248">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4ae99-249">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4ae99-250">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4ae99-251">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-252">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="4ae99-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4ae99-253">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-254">Internt salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4ae99-255">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="4ae99-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-256">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="4ae99-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4ae99-257">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-258">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="4ae99-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4ae99-259">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4ae99-260">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="4ae99-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4ae99-261">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4ae99-262">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-263">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="4ae99-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-264">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-265">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4ae99-266">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-267">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-267">Billed sales</span></span></td>
<td><span data-ttu-id="4ae99-268">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4ae99-269">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="4ae99-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4ae99-270">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4ae99-271">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-272">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-273">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-274">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4ae99-275">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-276">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="4ae99-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4ae99-277">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-278">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="4ae99-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4ae99-279">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4ae99-280">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="4ae99-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4ae99-281">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="4ae99-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4ae99-282">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4ae99-283">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="4ae99-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4ae99-284">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="4ae99-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4ae99-285">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4ae99-286">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4ae99-287">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="4ae99-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-288">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="4ae99-288">Billed sales</span></span></td>
<td><span data-ttu-id="4ae99-289">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4ae99-290">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="4ae99-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4ae99-291">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="4ae99-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4ae99-292">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-293">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="4ae99-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4ae99-294">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4ae99-295">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="4ae99-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4ae99-296">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="4ae99-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
