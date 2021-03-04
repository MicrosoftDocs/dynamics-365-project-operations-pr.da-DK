---
title: Oversigt over faktiske
description: Dette emne indeholder oplysninger om faktiske projektoplysninger.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146116"
---
# <a name="actuals-overview"></a><span data-ttu-id="b81d8-103">Oversigt over faktiske</span><span class="sxs-lookup"><span data-stu-id="b81d8-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b81d8-104">Faktiske oplysninger er mængden af arbejde, der er udført på et projekt.</span><span class="sxs-lookup"><span data-stu-id="b81d8-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="b81d8-105">Faktiske projektoplysninger kan spores tilbage til deres kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="b81d8-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="b81d8-106">De pågældende kildedokumenter omfatter tids-, udgifts- og kladdeposteringer samt fakturaer.</span><span class="sxs-lookup"><span data-stu-id="b81d8-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Sådan spores faktiske projektoplysninger til kildedokumenter](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="b81d8-108">Indsendelse af en tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="b81d8-108">Submitting a time entry</span></span>

<span data-ttu-id="b81d8-109">Når der i PSA indsendes en tidsregistrering for et projekt, der er knyttet til en tids-og-materiale-kontraktlinje, oprettes der to kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="b81d8-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="b81d8-110">Én linje er til omkostning, og den anden linje er til ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="b81d8-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="b81d8-111">Når der indsendes en tidsregistrering for et projekt, der er knyttet til en kontraktlinje med fastpris, oprettes der kun en kladdelinje for omkostning.</span><span class="sxs-lookup"><span data-stu-id="b81d8-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="b81d8-112">Logikken for angivelse af standardpriser findes på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="b81d8-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="b81d8-113">Samtlige feltværdier fra en tidsregistrering kopieres til kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="b81d8-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="b81d8-114">Disse felter inkluderer datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaresultatet i den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="b81d8-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="b81d8-115">De felter, der påvirker standardpriser som f.eks **Rolle** og **Organisationsenhed**, medfører, at der som standard angives en passende pris på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="b81d8-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="b81d8-116">Hvis du tilføjer et brugerdefineret felt på tidsregistreringen, og feltværdien skal overføres til faktiske værdier, skal du oprette feltet på objektet Faktiske og bruge felttilknytninger til at kopiere feltet fra tidsregistreringen til den faktiske værdi.</span><span class="sxs-lookup"><span data-stu-id="b81d8-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="b81d8-117">Indsendelse af en udgiftspost</span><span class="sxs-lookup"><span data-stu-id="b81d8-117">Submitting an expense entry</span></span>

<span data-ttu-id="b81d8-118">Når der i PSA indsendes en udgiftspost for et projekt, der er knyttet til en tids-og-materiale-kontraktlinje, oprettes der to kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="b81d8-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="b81d8-119">Én linje er til omkostning, og den anden linje er til ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="b81d8-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="b81d8-120">Når der indsendes en udgiftsposten for et projekt, der er knyttet til en kontraktlinje med fastpris, oprettes der kun en kladdelinje for omkostning.</span><span class="sxs-lookup"><span data-stu-id="b81d8-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="b81d8-121">Logikken for angivelse af standardpriser for udgifter er baseret på den udgiftskategori, der er valgt på siden **Udgiftspost**.</span><span class="sxs-lookup"><span data-stu-id="b81d8-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="b81d8-122">Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="b81d8-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="b81d8-123">Men for selve prisen er det beløb, som brugeren har indtastet, som standard angivet direkte på de relaterede udgiftskladdelinjer for omkostning og salg.</span><span class="sxs-lookup"><span data-stu-id="b81d8-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="b81d8-124">I den aktuelle version af PSA er kategoribaseret angivelse af standardpriser pr. enhed for udgiftsposter ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="b81d8-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="b81d8-125">Brug af Registreringskladder til registrering af omkostninger</span><span class="sxs-lookup"><span data-stu-id="b81d8-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="b81d8-126">I PSA giver Registreringskladder dig mulighed for at registrere omkostningen eller indtægten i materiale-, gebyr-, time-, udgifts- eller momstransaktionsklasser.</span><span class="sxs-lookup"><span data-stu-id="b81d8-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="b81d8-127">En kladde indeholder et hoved, linjer og en **Bekræft**-handling.</span><span class="sxs-lookup"><span data-stu-id="b81d8-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="b81d8-128">Her er nogle scenarier, hvor du kan bruge en kladde:</span><span class="sxs-lookup"><span data-stu-id="b81d8-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="b81d8-129">Du skal registrere de faktiske omkostninger og salget af materialer i et projekt.</span><span class="sxs-lookup"><span data-stu-id="b81d8-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="b81d8-130">Du skal flytte faktiske transaktionsoplysninger fra et andet system til PSA.</span><span class="sxs-lookup"><span data-stu-id="b81d8-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="b81d8-131">Du skal registrere omkostninger, der er opstået i et andet system, f.eks. omkostninger til indkøb eller underleverandørarbejde.</span><span class="sxs-lookup"><span data-stu-id="b81d8-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b81d8-132">Brug af Registreringskladder til at oprette faktiske oplysninger bør kun ske af en bruger, der fuldt ud bevidst om den regnskabsmæssige indvirkning, de faktiske oplysninger har på projektet.</span><span class="sxs-lookup"><span data-stu-id="b81d8-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="b81d8-133">Dette skyldes, at programmet ikke validerer kladdelinjetypen eller de relaterede priser, der angives på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="b81d8-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="b81d8-134">På grund af virkningen af denne kladdetype skal du udvise behørig omhu med, hvem der har adgang til at oprette Registreringskladder.</span><span class="sxs-lookup"><span data-stu-id="b81d8-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="b81d8-135">Registrering af faktiske oplysninger baseret på projekthændelser</span><span class="sxs-lookup"><span data-stu-id="b81d8-135">Recording actuals based on project events</span></span>

<span data-ttu-id="b81d8-136">PSA registrerer de økonomiske transaktioner, der sker i løbet af et projekt.</span><span class="sxs-lookup"><span data-stu-id="b81d8-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="b81d8-137">Disse transaktioner registreres som **faktiske oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="b81d8-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="b81d8-138">I følgende tabel vises de forskellige typer af faktiske oplysninger, der oprettes, afhængigt af, om projektet er tid-og-materiale- eller fastprisprojekt, er i fasen presales eller er et internt projekt.</span><span class="sxs-lookup"><span data-stu-id="b81d8-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="b81d8-139">**Ressourcen tilhører samme afdeling som projektets kontraktenhed**</span><span class="sxs-lookup"><span data-stu-id="b81d8-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b81d8-140">Hændelse</span><span class="sxs-lookup"><span data-stu-id="b81d8-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b81d8-141">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="b81d8-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b81d8-142">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="b81d8-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b81d8-143">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="b81d8-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b81d8-144">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="b81d8-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b81d8-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b81d8-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b81d8-146">Faktiske</span><span class="sxs-lookup"><span data-stu-id="b81d8-146">Actuals</span></span></th>
<th><span data-ttu-id="b81d8-147">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-147">Transaction currency</span></span></th>
<th><span data-ttu-id="b81d8-148">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b81d8-148">Fixed price</span></span></th>
<th><span data-ttu-id="b81d8-149">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b81d8-150">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="b81d8-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b81d8-151">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="b81d8-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-152">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="b81d8-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b81d8-153">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="b81d8-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b81d8-154">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="b81d8-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b81d8-155">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-155">Cost actual</span></span></td>
<td><span data-ttu-id="b81d8-156">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-157">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-158">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="b81d8-159">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-160">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-161">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="b81d8-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b81d8-162">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b81d8-163">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="b81d8-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b81d8-164">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-164">Cost actual</span></span></td>
<td><span data-ttu-id="b81d8-165">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-166">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-167">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-168">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-169">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-170">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="b81d8-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b81d8-171">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-172">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="b81d8-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b81d8-173">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b81d8-174">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="b81d8-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b81d8-175">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b81d8-176">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-177">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="b81d8-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-178">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-179">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-180">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-181">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-181">Billed sales</span></span></td>
<td><span data-ttu-id="b81d8-182">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b81d8-183">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="b81d8-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b81d8-184">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b81d8-185">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-186">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-187">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-188">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-189">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-190">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="b81d8-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b81d8-191">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-192">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="b81d8-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b81d8-193">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b81d8-194">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="b81d8-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b81d8-195">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="b81d8-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b81d8-196">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b81d8-197">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="b81d8-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b81d8-198">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="b81d8-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b81d8-199">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b81d8-200">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b81d8-201">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-202">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-202">Billed sales</span></span></td>
<td><span data-ttu-id="b81d8-203">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b81d8-204">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="b81d8-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b81d8-205">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="b81d8-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b81d8-206">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-207">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="b81d8-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b81d8-208">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-209">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="b81d8-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b81d8-210">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b81d8-211">**Ressourcen tilhører en afdeling, som er forskellig fra projektets kontraktenhed**</span><span class="sxs-lookup"><span data-stu-id="b81d8-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b81d8-212">Hændelse</span><span class="sxs-lookup"><span data-stu-id="b81d8-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b81d8-213">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="b81d8-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b81d8-214">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="b81d8-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b81d8-215">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="b81d8-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b81d8-216">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="b81d8-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b81d8-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b81d8-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b81d8-218">Faktiske</span><span class="sxs-lookup"><span data-stu-id="b81d8-218">Actuals</span></span></th>
<th><span data-ttu-id="b81d8-219">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-219">Transaction currency</span></span></th>
<th><span data-ttu-id="b81d8-220">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b81d8-220">Fixed price</span></span></th>
<th><span data-ttu-id="b81d8-221">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b81d8-222">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="b81d8-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b81d8-223">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="b81d8-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-224">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="b81d8-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b81d8-225">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="b81d8-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b81d8-226">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="b81d8-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b81d8-227">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-227">Cost actual</span></span></td>
<td><span data-ttu-id="b81d8-228">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b81d8-229">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b81d8-230">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b81d8-231">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b81d8-232">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-233">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="b81d8-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b81d8-234">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-235">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b81d8-236">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-237">Internt salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b81d8-238">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b81d8-239">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="b81d8-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b81d8-240">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-240">Cost actual</span></span></td>
<td><span data-ttu-id="b81d8-241">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b81d8-242">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b81d8-243">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b81d8-244">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b81d8-245">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-246">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="b81d8-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b81d8-247">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-248">Internt salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b81d8-249">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="b81d8-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-250">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="b81d8-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b81d8-251">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-252">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="b81d8-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b81d8-253">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b81d8-254">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="b81d8-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b81d8-255">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b81d8-256">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-257">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="b81d8-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-258">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-259">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b81d8-260">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-261">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-261">Billed sales</span></span></td>
<td><span data-ttu-id="b81d8-262">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b81d8-263">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="b81d8-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b81d8-264">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b81d8-265">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-266">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-267">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-268">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b81d8-269">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-270">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="b81d8-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b81d8-271">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-272">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="b81d8-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b81d8-273">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b81d8-274">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="b81d8-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b81d8-275">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="b81d8-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b81d8-276">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b81d8-277">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="b81d8-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b81d8-278">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="b81d8-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b81d8-279">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b81d8-280">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b81d8-281">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b81d8-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-282">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="b81d8-282">Billed sales</span></span></td>
<td><span data-ttu-id="b81d8-283">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b81d8-284">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="b81d8-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b81d8-285">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="b81d8-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b81d8-286">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-287">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="b81d8-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b81d8-288">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b81d8-289">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="b81d8-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b81d8-290">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="b81d8-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
