---
title: Oversigt over faktiske
description: Dette emne indeholder oplysninger om faktiske projektoplysninger.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368154"
---
# <a name="actuals-overview"></a><span data-ttu-id="cb4c0-103">Oversigt over faktiske</span><span class="sxs-lookup"><span data-stu-id="cb4c0-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cb4c0-104">Faktiske oplysninger er mængden af arbejde, der er udført på et projekt.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="cb4c0-105">Faktiske projektoplysninger kan spores tilbage til deres kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="cb4c0-106">De pågældende kildedokumenter omfatter tids-, udgifts- og kladdeposteringer samt fakturaer.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Sådan spores faktiske projektoplysninger til kildedokumenter](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="cb4c0-108">Indsendelse af en tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="cb4c0-108">Submitting a time entry</span></span>

<span data-ttu-id="cb4c0-109">Når der i PSA indsendes en tidsregistrering for et projekt, der er knyttet til en tids-og-materiale-kontraktlinje, oprettes der to kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cb4c0-110">Én linje er til omkostning, og den anden linje er til ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cb4c0-111">Når der indsendes en tidsregistrering for et projekt, der er knyttet til en kontraktlinje med fastpris, oprettes der kun en kladdelinje for omkostning.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="cb4c0-112">Logikken for angivelse af standardpriser findes på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="cb4c0-113">Samtlige feltværdier fra en tidsregistrering kopieres til kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="cb4c0-114">Disse felter inkluderer datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaresultatet i den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="cb4c0-115">De felter, der påvirker standardpriser som f.eks **Rolle** og **Organisationsenhed**, medfører, at der som standard angives en passende pris på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="cb4c0-116">Hvis du tilføjer et brugerdefineret felt på tidsregistreringen, og feltværdien skal overføres til faktiske værdier, skal du oprette feltet på objektet Faktiske og bruge felttilknytninger til at kopiere feltet fra tidsregistreringen til den faktiske værdi.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="cb4c0-117">Indsendelse af en udgiftspost</span><span class="sxs-lookup"><span data-stu-id="cb4c0-117">Submitting an expense entry</span></span>

<span data-ttu-id="cb4c0-118">Når der i PSA indsendes en udgiftspost for et projekt, der er knyttet til en tids-og-materiale-kontraktlinje, oprettes der to kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cb4c0-119">Én linje er til omkostning, og den anden linje er til ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cb4c0-120">Når der indsendes en udgiftsposten for et projekt, der er knyttet til en kontraktlinje med fastpris, oprettes der kun en kladdelinje for omkostning.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="cb4c0-121">Logikken for angivelse af standardpriser for udgifter er baseret på den udgiftskategori, der er valgt på siden **Udgiftspost**.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="cb4c0-122">Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="cb4c0-123">Men for selve prisen er det beløb, som brugeren har indtastet, som standard angivet direkte på de relaterede udgiftskladdelinjer for omkostning og salg.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="cb4c0-124">I den aktuelle version af PSA er kategoribaseret angivelse af standardpriser pr. enhed for udgiftsposter ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="cb4c0-125">Brug af Registreringskladder til registrering af omkostninger</span><span class="sxs-lookup"><span data-stu-id="cb4c0-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="cb4c0-126">I PSA giver Registreringskladder dig mulighed for at registrere omkostningen eller indtægten i materiale-, gebyr-, time-, udgifts- eller momstransaktionsklasser.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="cb4c0-127">En kladde indeholder et hoved, linjer og en **Bekræft**-handling.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="cb4c0-128">Her er nogle scenarier, hvor du kan bruge en kladde:</span><span class="sxs-lookup"><span data-stu-id="cb4c0-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="cb4c0-129">Du skal registrere de faktiske omkostninger og salget af materialer i et projekt.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="cb4c0-130">Du skal flytte faktiske transaktionsoplysninger fra et andet system til PSA.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="cb4c0-131">Du skal registrere omkostninger, der er opstået i et andet system, f.eks. omkostninger til indkøb eller underleverandørarbejde.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb4c0-132">Brug af Registreringskladder til at oprette faktiske oplysninger bør kun ske af en bruger, der fuldt ud bevidst om den regnskabsmæssige indvirkning, de faktiske oplysninger har på projektet.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="cb4c0-133">Dette skyldes, at programmet ikke validerer kladdelinjetypen eller de relaterede priser, der angives på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="cb4c0-134">På grund af virkningen af denne kladdetype skal du udvise behørig omhu med, hvem der har adgang til at oprette Registreringskladder.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="cb4c0-135">Registrering af faktiske oplysninger baseret på projekthændelser</span><span class="sxs-lookup"><span data-stu-id="cb4c0-135">Recording actuals based on project events</span></span>

<span data-ttu-id="cb4c0-136">PSA registrerer de økonomiske transaktioner, der sker i løbet af et projekt.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="cb4c0-137">Disse transaktioner registreres som **faktiske oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="cb4c0-138">I følgende tabel vises de forskellige typer af faktiske oplysninger, der oprettes, afhængigt af, om projektet er tid-og-materiale- eller fastprisprojekt, er i fasen presales eller er et internt projekt.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="cb4c0-139">**Ressourcen tilhører samme afdeling som projektets kontraktenhed**</span><span class="sxs-lookup"><span data-stu-id="cb4c0-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cb4c0-140">Hændelse</span><span class="sxs-lookup"><span data-stu-id="cb4c0-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cb4c0-141">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="cb4c0-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cb4c0-142">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="cb4c0-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cb4c0-143">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="cb4c0-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cb4c0-144">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="cb4c0-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cb4c0-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="cb4c0-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cb4c0-146">Faktiske</span><span class="sxs-lookup"><span data-stu-id="cb4c0-146">Actuals</span></span></th>
<th><span data-ttu-id="cb4c0-147">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-147">Transaction currency</span></span></th>
<th><span data-ttu-id="cb4c0-148">Fast pris</span><span class="sxs-lookup"><span data-stu-id="cb4c0-148">Fixed price</span></span></th>
<th><span data-ttu-id="cb4c0-149">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cb4c0-150">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cb4c0-151">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="cb4c0-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-152">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cb4c0-153">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="cb4c0-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb4c0-154">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cb4c0-155">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-155">Cost actual</span></span></td>
<td><span data-ttu-id="cb4c0-156">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-157">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-158">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="cb4c0-159">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-160">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-161">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="cb4c0-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cb4c0-162">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb4c0-163">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cb4c0-164">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-164">Cost actual</span></span></td>
<td><span data-ttu-id="cb4c0-165">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-166">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-167">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-168">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-169">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-170">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="cb4c0-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cb4c0-171">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-172">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="cb4c0-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb4c0-173">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb4c0-174">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cb4c0-175">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cb4c0-176">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-177">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="cb4c0-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-178">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-179">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-180">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-181">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-181">Billed sales</span></span></td>
<td><span data-ttu-id="cb4c0-182">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb4c0-183">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cb4c0-184">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cb4c0-185">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-186">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-187">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-188">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-189">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-190">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="cb4c0-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cb4c0-191">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-192">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="cb4c0-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb4c0-193">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb4c0-194">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cb4c0-195">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="cb4c0-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cb4c0-196">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cb4c0-197">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="cb4c0-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cb4c0-198">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="cb4c0-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cb4c0-199">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cb4c0-200">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cb4c0-201">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-202">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-202">Billed sales</span></span></td>
<td><span data-ttu-id="cb4c0-203">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb4c0-204">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cb4c0-205">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="cb4c0-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cb4c0-206">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-207">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="cb4c0-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cb4c0-208">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-209">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="cb4c0-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb4c0-210">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cb4c0-211">**Ressourcen tilhører en afdeling, som er forskellig fra projektets kontraktenhed**</span><span class="sxs-lookup"><span data-stu-id="cb4c0-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cb4c0-212">Hændelse</span><span class="sxs-lookup"><span data-stu-id="cb4c0-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cb4c0-213">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="cb4c0-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cb4c0-214">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="cb4c0-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cb4c0-215">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="cb4c0-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cb4c0-216">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="cb4c0-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cb4c0-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="cb4c0-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cb4c0-218">Faktiske</span><span class="sxs-lookup"><span data-stu-id="cb4c0-218">Actuals</span></span></th>
<th><span data-ttu-id="cb4c0-219">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-219">Transaction currency</span></span></th>
<th><span data-ttu-id="cb4c0-220">Fast pris</span><span class="sxs-lookup"><span data-stu-id="cb4c0-220">Fixed price</span></span></th>
<th><span data-ttu-id="cb4c0-221">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cb4c0-222">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cb4c0-223">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="cb4c0-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-224">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cb4c0-225">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="cb4c0-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cb4c0-226">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cb4c0-227">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-227">Cost actual</span></span></td>
<td><span data-ttu-id="cb4c0-228">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cb4c0-229">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cb4c0-230">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cb4c0-231">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cb4c0-232">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-233">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="cb4c0-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cb4c0-234">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-235">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cb4c0-236">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-237">Internt salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cb4c0-238">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cb4c0-239">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cb4c0-240">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-240">Cost actual</span></span></td>
<td><span data-ttu-id="cb4c0-241">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cb4c0-242">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cb4c0-243">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cb4c0-244">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cb4c0-245">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-246">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="cb4c0-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cb4c0-247">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-248">Internt salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cb4c0-249">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="cb4c0-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-250">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="cb4c0-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cb4c0-251">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-252">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="cb4c0-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb4c0-253">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb4c0-254">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cb4c0-255">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cb4c0-256">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-257">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="cb4c0-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-258">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-259">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cb4c0-260">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-261">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-261">Billed sales</span></span></td>
<td><span data-ttu-id="cb4c0-262">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb4c0-263">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cb4c0-264">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cb4c0-265">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-266">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-267">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-268">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cb4c0-269">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-270">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="cb4c0-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cb4c0-271">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-272">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="cb4c0-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb4c0-273">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cb4c0-274">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cb4c0-275">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="cb4c0-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cb4c0-276">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cb4c0-277">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="cb4c0-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cb4c0-278">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="cb4c0-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cb4c0-279">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cb4c0-280">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cb4c0-281">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="cb4c0-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-282">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="cb4c0-282">Billed sales</span></span></td>
<td><span data-ttu-id="cb4c0-283">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cb4c0-284">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cb4c0-285">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="cb4c0-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cb4c0-286">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-287">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="cb4c0-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cb4c0-288">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb4c0-289">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="cb4c0-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cb4c0-290">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="cb4c0-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]