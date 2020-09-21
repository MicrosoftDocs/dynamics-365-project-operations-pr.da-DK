---
title: Faktiske
description: Dette emne indeholder oplysninger om faktiske projektoplysninger.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750607"
---
# <a name="actuals"></a><span data-ttu-id="0c53b-103">Faktiske</span><span class="sxs-lookup"><span data-stu-id="0c53b-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0c53b-104">Faktiske oplysninger er mængden af arbejde, der er udført på et projekt.</span><span class="sxs-lookup"><span data-stu-id="0c53b-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0c53b-105">Faktiske projektoplysninger kan spores tilbage til deres kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="0c53b-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="0c53b-106">De pågældende kildedokumenter omfatter tids-, udgifts- og kladdeposteringer samt fakturaer.</span><span class="sxs-lookup"><span data-stu-id="0c53b-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Sådan spores faktiske projektoplysninger til kildedokumenter](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="0c53b-108">Indsendelse af en tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="0c53b-108">Submitting a time entry</span></span>

<span data-ttu-id="0c53b-109">Når der i PSA indsendes en tidsregistrering for et projekt, der er knyttet til en tids-og-materiale-kontraktlinje, oprettes der to kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="0c53b-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0c53b-110">Én linje er til omkostning, og den anden linje er til ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="0c53b-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0c53b-111">Når der indsendes en tidsregistrering for et projekt, der er knyttet til en kontraktlinje med fastpris, oprettes der kun en kladdelinje for omkostning.</span><span class="sxs-lookup"><span data-stu-id="0c53b-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="0c53b-112">Logikken for angivelse af standardpriser findes på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="0c53b-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="0c53b-113">Samtlige feltværdier fra en tidsregistrering kopieres til kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="0c53b-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="0c53b-114">Disse felter inkluderer datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaresultatet i den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="0c53b-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="0c53b-115">De felter, der påvirker standardpriser som f.eks **Rolle** og **Organisationsenhed**, medfører, at der som standard angives en passende pris på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="0c53b-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="0c53b-116">Hvis du tilføjer et brugerdefineret felt på tidsregistreringen, og feltværdien skal overføres til faktiske værdier, skal du oprette feltet på objektet Faktiske og bruge felttilknytninger til at kopiere feltet fra tidsregistreringen til den faktiske værdi.</span><span class="sxs-lookup"><span data-stu-id="0c53b-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="0c53b-117">Indsendelse af en udgiftspost</span><span class="sxs-lookup"><span data-stu-id="0c53b-117">Submitting an expense entry</span></span>

<span data-ttu-id="0c53b-118">Når der i PSA indsendes en udgiftspost for et projekt, der er knyttet til en tids-og-materiale-kontraktlinje, oprettes der to kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="0c53b-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0c53b-119">Én linje er til omkostning, og den anden linje er til ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="0c53b-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0c53b-120">Når der indsendes en udgiftsposten for et projekt, der er knyttet til en kontraktlinje med fastpris, oprettes der kun en kladdelinje for omkostning.</span><span class="sxs-lookup"><span data-stu-id="0c53b-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="0c53b-121">Logikken for angivelse af standardpriser for udgifter er baseret på den udgiftskategori, der er valgt på siden **Udgiftspost**.</span><span class="sxs-lookup"><span data-stu-id="0c53b-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="0c53b-122">Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="0c53b-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0c53b-123">Men for selve prisen er det beløb, som brugeren har indtastet, som standard angivet direkte på de relaterede udgiftskladdelinjer for omkostning og salg.</span><span class="sxs-lookup"><span data-stu-id="0c53b-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="0c53b-124">I den aktuelle version af PSA er kategoribaseret angivelse af standardpriser pr. enhed for udgiftsposter ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="0c53b-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="0c53b-125">Brug af kladder til registrering af omkostninger</span><span class="sxs-lookup"><span data-stu-id="0c53b-125">Using journals to record costs</span></span>

<span data-ttu-id="0c53b-126">I PSA giver kladder dig mulighed for at registrere omkostninger eller indtægter i materiale-, gebyr-, time-, udgifts- eller momstransaktionsklasser.</span><span class="sxs-lookup"><span data-stu-id="0c53b-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0c53b-127">En kladde indeholder et hoved, linjer og en **Bekræft**-handling.</span><span class="sxs-lookup"><span data-stu-id="0c53b-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="0c53b-128">Her er nogle scenarier, hvor du kan bruge en kladde:</span><span class="sxs-lookup"><span data-stu-id="0c53b-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="0c53b-129">Du skal registrere de faktiske omkostninger og salget af materialer i et projekt.</span><span class="sxs-lookup"><span data-stu-id="0c53b-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="0c53b-130">Du skal flytte faktiske transaktionsoplysninger fra et andet system til PSA.</span><span class="sxs-lookup"><span data-stu-id="0c53b-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="0c53b-131">Du skal registrere omkostninger, der er opstået i et andet system, f.eks. omkostninger til indkøb eller underleverandørarbejde.</span><span class="sxs-lookup"><span data-stu-id="0c53b-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="0c53b-132">Registrering af faktiske oplysninger baseret på projekthændelser</span><span class="sxs-lookup"><span data-stu-id="0c53b-132">Recording actuals based on project events</span></span>

<span data-ttu-id="0c53b-133">PSA registrerer de økonomiske transaktioner, der sker i løbet af et projekt.</span><span class="sxs-lookup"><span data-stu-id="0c53b-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0c53b-134">Disse transaktioner registreres som **faktiske oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="0c53b-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="0c53b-135">I følgende tabel vises de forskellige typer af faktiske oplysninger, der oprettes, afhængigt af, om projektet er tid-og-materiale- eller fastprisprojekt, er i fasen presales eller er et internt projekt.</span><span class="sxs-lookup"><span data-stu-id="0c53b-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="0c53b-136">**Ressourcen tilhører samme afdeling som projektets kontraktenhed**</span><span class="sxs-lookup"><span data-stu-id="0c53b-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0c53b-137">Hændelse</span><span class="sxs-lookup"><span data-stu-id="0c53b-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0c53b-138">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="0c53b-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0c53b-139">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="0c53b-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0c53b-140">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="0c53b-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0c53b-141">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="0c53b-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0c53b-142">Fast pris</span><span class="sxs-lookup"><span data-stu-id="0c53b-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0c53b-143">Faktiske</span><span class="sxs-lookup"><span data-stu-id="0c53b-143">Actuals</span></span></th>
<th><span data-ttu-id="0c53b-144">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-144">Transaction currency</span></span></th>
<th><span data-ttu-id="0c53b-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="0c53b-145">Fixed price</span></span></th>
<th><span data-ttu-id="0c53b-146">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0c53b-147">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="0c53b-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0c53b-148">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="0c53b-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-149">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="0c53b-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0c53b-150">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="0c53b-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c53b-151">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="0c53b-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0c53b-152">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-152">Cost actual</span></span></td>
<td><span data-ttu-id="0c53b-153">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-154">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-155">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0c53b-156">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-157">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-158">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="0c53b-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0c53b-159">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c53b-160">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="0c53b-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0c53b-161">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-161">Cost actual</span></span></td>
<td><span data-ttu-id="0c53b-162">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-163">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-164">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-165">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-166">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-167">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="0c53b-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0c53b-168">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-169">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="0c53b-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c53b-170">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c53b-171">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="0c53b-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0c53b-172">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0c53b-173">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-174">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="0c53b-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-175">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-176">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-177">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-178">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-178">Billed sales</span></span></td>
<td><span data-ttu-id="0c53b-179">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c53b-180">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="0c53b-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0c53b-181">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0c53b-182">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-183">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-184">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-185">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-186">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-187">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="0c53b-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0c53b-188">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-189">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="0c53b-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c53b-190">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c53b-191">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="0c53b-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0c53b-192">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="0c53b-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0c53b-193">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0c53b-194">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="0c53b-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0c53b-195">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="0c53b-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0c53b-196">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0c53b-197">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0c53b-198">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-199">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-199">Billed sales</span></span></td>
<td><span data-ttu-id="0c53b-200">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c53b-201">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="0c53b-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0c53b-202">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="0c53b-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0c53b-203">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-204">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="0c53b-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0c53b-205">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-206">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="0c53b-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c53b-207">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0c53b-208">**Ressourcen tilhører en afdeling, som er forskellig fra projektets kontraktenhed**</span><span class="sxs-lookup"><span data-stu-id="0c53b-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0c53b-209">Hændelse</span><span class="sxs-lookup"><span data-stu-id="0c53b-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0c53b-210">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="0c53b-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0c53b-211">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="0c53b-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0c53b-212">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="0c53b-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0c53b-213">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="0c53b-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0c53b-214">Fast pris</span><span class="sxs-lookup"><span data-stu-id="0c53b-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0c53b-215">Faktiske</span><span class="sxs-lookup"><span data-stu-id="0c53b-215">Actuals</span></span></th>
<th><span data-ttu-id="0c53b-216">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-216">Transaction currency</span></span></th>
<th><span data-ttu-id="0c53b-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="0c53b-217">Fixed price</span></span></th>
<th><span data-ttu-id="0c53b-218">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0c53b-219">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="0c53b-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0c53b-220">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="0c53b-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-221">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="0c53b-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0c53b-222">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="0c53b-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0c53b-223">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="0c53b-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0c53b-224">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-224">Cost actual</span></span></td>
<td><span data-ttu-id="0c53b-225">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0c53b-226">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0c53b-227">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0c53b-228">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0c53b-229">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-230">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="0c53b-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0c53b-231">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-232">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0c53b-233">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-234">Internt salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0c53b-235">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0c53b-236">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="0c53b-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0c53b-237">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-237">Cost actual</span></span></td>
<td><span data-ttu-id="0c53b-238">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0c53b-239">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0c53b-240">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0c53b-241">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0c53b-242">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-243">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="0c53b-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0c53b-244">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-245">Internt salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0c53b-246">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="0c53b-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-247">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="0c53b-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0c53b-248">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-249">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="0c53b-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c53b-250">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c53b-251">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="0c53b-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0c53b-252">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0c53b-253">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-254">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="0c53b-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-255">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-256">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0c53b-257">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-258">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-258">Billed sales</span></span></td>
<td><span data-ttu-id="0c53b-259">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c53b-260">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="0c53b-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0c53b-261">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0c53b-262">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-263">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-264">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-265">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c53b-266">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-267">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="0c53b-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0c53b-268">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-269">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="0c53b-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c53b-270">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c53b-271">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="0c53b-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0c53b-272">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="0c53b-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0c53b-273">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0c53b-274">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="0c53b-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0c53b-275">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="0c53b-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0c53b-276">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0c53b-277">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0c53b-278">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="0c53b-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-279">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="0c53b-279">Billed sales</span></span></td>
<td><span data-ttu-id="0c53b-280">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c53b-281">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="0c53b-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0c53b-282">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="0c53b-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0c53b-283">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-284">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="0c53b-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0c53b-285">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c53b-286">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="0c53b-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c53b-287">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="0c53b-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
