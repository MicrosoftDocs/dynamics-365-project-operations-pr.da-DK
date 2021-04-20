---
title: Faktiske
description: Dette emne indeholder oplysninger om, hvordan du arbejder med faktiske værdier i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852537"
---
# <a name="actuals"></a><span data-ttu-id="5b51e-103">Faktiske</span><span class="sxs-lookup"><span data-stu-id="5b51e-103">Actuals</span></span> 

<span data-ttu-id="5b51e-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5b51e-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5b51e-105">Faktiske værdier repræsenterer den gennemgåede og godkendte økonomiske og planlægningsmæssige status for et projekt.</span><span class="sxs-lookup"><span data-stu-id="5b51e-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="5b51e-106">De oprettes som følge af godkendelse af registreringer af tid, udgifter, materialeforbrug samt kladdeposteringer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="5b51e-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="5b51e-107">Kladdelinjer og tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="5b51e-107">Journal lines and time submission</span></span>

<span data-ttu-id="5b51e-108">Du kan finde flere oplysninger om tidsregistrering under [Oversigt over tidsregistrering](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5b51e-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="5b51e-109">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="5b51e-109">Time and materials</span></span>

<span data-ttu-id="5b51e-110">Når en afsendt tidsregistrering hænger sammen med et projekt, der er knyttet til en tids- og materialekontraktlinje, oprettes der to kladdelinjer i systemet, en for kostpris og én for ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="5b51e-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="5b51e-111">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b51e-111">Fixed price</span></span>

<span data-ttu-id="5b51e-112">Når en indsendt tidsregistrering er forbundet med et projekt, der er knyttet til en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5b51e-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="5b51e-113">Standardprisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="5b51e-113">Default pricing</span></span>

<span data-ttu-id="5b51e-114">Logikken for oprettelse af standardpriser findes på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="5b51e-115">Feltværdierne fra tidsregistreringen kopieres til kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="5b51e-116">Disse værdier inkluderer datoen for transaktionen, den kontraktlinje, som projektet er knyttet til, og valutaresultatet i den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="5b51e-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="5b51e-117">De felter, der påvirker standardprisfastsættelse som f.eks **Rolle** og **Ressourceenhed**, anvendes til at fastsætte den passende pris på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="5b51e-118">Du kan tilføje et brugerdefineret felt på tidsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="5b51e-119">Hvis feltværdien skal overføres til faktiske værdier, skal du oprette feltet i tabellerne **Faktiske** og **Kladdelinje**.</span><span class="sxs-lookup"><span data-stu-id="5b51e-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="5b51e-120">Brug brugerdefineret kode til at overføre den valgte feltværdi fra Tidindtastning til Faktiske via kladdelinjen ved hjælp af transaktionsoprindelser.</span><span class="sxs-lookup"><span data-stu-id="5b51e-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="5b51e-121">Du kan finde flere oplysninger om transaktionsoprindelser og forbindelser under [Tilknytning af faktiske til oprindelige poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="5b51e-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="5b51e-122">Kladdelinjer og indsendelse af grundlæggende udgifter</span><span class="sxs-lookup"><span data-stu-id="5b51e-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="5b51e-123">Du kan finde flere oplysninger om udgiftsregistrering under [Oversigt over udgifter](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5b51e-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="5b51e-124">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="5b51e-124">Time and materials</span></span>

<span data-ttu-id="5b51e-125">Når en grundlæggende udgiftspost hænger sammen med et projekt, der er knyttet til en tids- og materialekontraktlinje, oprettes der to kladdelinjer i systemet, en for kostpris og én for ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="5b51e-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="5b51e-126">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b51e-126">Fixed price</span></span>

<span data-ttu-id="5b51e-127">Når en indsendt grundlæggende udgiftsposten knyttes sammen med et projekt, der er tilknyttet en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostning.</span><span class="sxs-lookup"><span data-stu-id="5b51e-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="5b51e-128">Standardprisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="5b51e-128">Default pricing</span></span>

<span data-ttu-id="5b51e-129">Logikken for angivelse af standardpriser for udgifter er baseret på udgiftskategorien.</span><span class="sxs-lookup"><span data-stu-id="5b51e-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="5b51e-130">Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="5b51e-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5b51e-131">De felter, der påvirker standardprisfastsættelse som f.eks **Transaktionskategori** og **Enhed**, anvendes til at fastsætte den passende pris på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="5b51e-132">Dette fungerer dog kun, når prisfastsættelsesmetoden på prislisten er **Pris pr. enhed**.</span><span class="sxs-lookup"><span data-stu-id="5b51e-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="5b51e-133">Hvis prisfastsættelsesmetoden er **Omkostning** eller **Avance før omkostning**, bruges den pris, der blev angivet ved oprettelse af udgiftsposten, til omkostning, og prisen på salgslinjen beregnes på grundlag af prisfastsættelsesmetoden.</span><span class="sxs-lookup"><span data-stu-id="5b51e-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="5b51e-134">Du kan tilføje et brugerdefineret felt på udgiftsposten.</span><span class="sxs-lookup"><span data-stu-id="5b51e-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="5b51e-135">Hvis feltværdien skal overføres til faktiske værdier, skal du oprette feltet i tabellerne **Faktiske** og **Kladdelinje**.</span><span class="sxs-lookup"><span data-stu-id="5b51e-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="5b51e-136">Brug brugerdefineret kode til at overføre den valgte feltværdi fra Tidindtastning til Faktiske via kladdelinjen ved hjælp af transaktionsoprindelser.</span><span class="sxs-lookup"><span data-stu-id="5b51e-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="5b51e-137">Du kan finde flere oplysninger om transaktionsoprindelser og forbindelser under [Tilknytning af faktiske til oprindelige poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="5b51e-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="5b51e-138">Indsendelse af kladdelinjer og materialeforbrugslog</span><span class="sxs-lookup"><span data-stu-id="5b51e-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="5b51e-139">Du kan finde flere oplysninger om udgiftsregistrering i [Materialeforbrugslog](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="5b51e-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="5b51e-140">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="5b51e-140">Time and materials</span></span>

<span data-ttu-id="5b51e-141">Når en indsendt registrering af en materialeforbrugslog forbindes med et projekt, der er tilknyttet en tids- og materialekontraktlinje, opretter systemet to kladdelinjer, én for omkostning og én for ikke-faktureret salg.</span><span class="sxs-lookup"><span data-stu-id="5b51e-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="5b51e-142">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b51e-142">Fixed price</span></span>

<span data-ttu-id="5b51e-143">Når en indsendt registrering af materialeforbrugslog forbindes med et projekt, der er tilknyttet en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostning.</span><span class="sxs-lookup"><span data-stu-id="5b51e-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="5b51e-144">Standardprisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="5b51e-144">Default pricing</span></span>

<span data-ttu-id="5b51e-145">Logikken for registrering af standardpriser for materiale er baseret på kombinationen af produkt og enhed.</span><span class="sxs-lookup"><span data-stu-id="5b51e-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="5b51e-146">Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste.</span><span class="sxs-lookup"><span data-stu-id="5b51e-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5b51e-147">De felter, der påvirker standardprisfastsættelse som f.eks **Produkt-id** og **Enhed**, anvendes til at fastsætte den passende pris på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="5b51e-148">Dette fungerer dog kun for katalogprodukter.</span><span class="sxs-lookup"><span data-stu-id="5b51e-148">However, this only works for catalog products.</span></span> <span data-ttu-id="5b51e-149">For produkter, der skal rekvireres, anvendes den pris, der blev angivet, da registreringen af materialeforbrugsloggen blev oprettet, som kostpris og salgspris på kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="5b51e-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="5b51e-150">Du kan tilføje et brugerdefineret felt på registreringen af **Materialeforbrugslog**.</span><span class="sxs-lookup"><span data-stu-id="5b51e-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="5b51e-151">Hvis feltværdien skal overføres til faktiske værdier, skal du oprette feltet i tabellerne **Faktiske** og **Kladdelinje**.</span><span class="sxs-lookup"><span data-stu-id="5b51e-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="5b51e-152">Brug brugerdefineret kode til at overføre den valgte feltværdi fra Tidindtastning til Faktiske via kladdelinjen ved hjælp af transaktionsoprindelser.</span><span class="sxs-lookup"><span data-stu-id="5b51e-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="5b51e-153">Du kan finde flere oplysninger om transaktionsoprindelser og forbindelser under [Tilknytning af faktiske til oprindelige poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="5b51e-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="5b51e-154">Brug posteringskladder til registrering af omkostninger</span><span class="sxs-lookup"><span data-stu-id="5b51e-154">Use entry journals to record costs</span></span>

<span data-ttu-id="5b51e-155">Du kan anvende posteringskladder til at registrere omkostningerne eller indtægterne i materiale-, gebyr-, time-, udgifts- eller momstransaktionsklasser.</span><span class="sxs-lookup"><span data-stu-id="5b51e-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="5b51e-156">Kladder kan bruges til følgende formål:</span><span class="sxs-lookup"><span data-stu-id="5b51e-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="5b51e-157">Flyt faktiske transaktionsoplysninger fra et andet system til Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5b51e-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="5b51e-158">Registrer omkostninger, der er opstået i et andet system.</span><span class="sxs-lookup"><span data-stu-id="5b51e-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="5b51e-159">Disse omkostninger kan inkludere udgifter til indkøb eller underleverandører.</span><span class="sxs-lookup"><span data-stu-id="5b51e-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b51e-160">Applikationen validerer ikke kladdelinjetypen eller den relaterede prisfastsættelse, der er angivet på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="5b51e-161">Derfor er det kun en bruger, der er fuldt bekendt med den regnskabsmæssige indvirkning, som faktiske værdier har på projektet, der skal bruge posteringskladder til at oprette faktiske værdier.</span><span class="sxs-lookup"><span data-stu-id="5b51e-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="5b51e-162">Som følge af virkningen af denne kladdetype skal du omhyggeligt vælge, hvem der har adgang til at oprette posteringskladder.</span><span class="sxs-lookup"><span data-stu-id="5b51e-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="5b51e-163">Registrer faktiske oplysninger baseret på projekthændelser</span><span class="sxs-lookup"><span data-stu-id="5b51e-163">Record actuals based on project events</span></span>

<span data-ttu-id="5b51e-164">Project Operations registrerer de økonomiske transaktioner, der sker i løbet af et projekt.</span><span class="sxs-lookup"><span data-stu-id="5b51e-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="5b51e-165">Disse transaktioner registreres som faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="5b51e-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="5b51e-166">I følgende tabel vises de forskellige typer af faktiske oplysninger, der oprettes, afhængigt af, om projektet er tid-og-materiale- eller fastprisprojekt, er i fasen presales eller er et internt projekt.</span><span class="sxs-lookup"><span data-stu-id="5b51e-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="5b51e-167">Ressourcen tilhører samme afdeling som projektets kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5b51e-168">Hændelse</span><span class="sxs-lookup"><span data-stu-id="5b51e-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5b51e-169">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="5b51e-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5b51e-170">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="5b51e-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5b51e-171">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="5b51e-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5b51e-172">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="5b51e-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5b51e-173">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b51e-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5b51e-174">Faktiske</span><span class="sxs-lookup"><span data-stu-id="5b51e-174">Actuals</span></span></th>
<th><span data-ttu-id="5b51e-175">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-175">Transaction currency</span></span></th>
<th><span data-ttu-id="5b51e-176">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b51e-176">Fixed price</span></span></th>
<th><span data-ttu-id="5b51e-177">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5b51e-178">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="5b51e-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5b51e-179">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="5b51e-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-180">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="5b51e-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5b51e-181">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="5b51e-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b51e-182">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5b51e-183">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-183">Cost actual</span></span></td>
<td><span data-ttu-id="5b51e-184">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-185">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-186">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="5b51e-187">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-188">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-189">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="5b51e-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5b51e-190">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b51e-191">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5b51e-192">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-192">Cost actual</span></span></td>
<td><span data-ttu-id="5b51e-193">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-194">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-195">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-196">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-197">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-198">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="5b51e-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5b51e-199">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-200">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="5b51e-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b51e-201">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b51e-202">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="5b51e-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5b51e-203">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5b51e-204">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-205">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="5b51e-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-206">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-207">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-208">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-209">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-209">Billed sales</span></span></td>
<td><span data-ttu-id="5b51e-210">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b51e-211">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="5b51e-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5b51e-212">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5b51e-213">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-214">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-215">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-216">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-217">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-218">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="5b51e-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5b51e-219">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-220">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="5b51e-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b51e-221">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b51e-222">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="5b51e-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5b51e-223">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="5b51e-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5b51e-224">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5b51e-225">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="5b51e-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5b51e-226">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="5b51e-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5b51e-227">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5b51e-228">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5b51e-229">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-230">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-230">Billed sales</span></span></td>
<td><span data-ttu-id="5b51e-231">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b51e-232">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="5b51e-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5b51e-233">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="5b51e-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5b51e-234">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-235">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="5b51e-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5b51e-236">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-237">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="5b51e-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b51e-238">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="5b51e-239">Ressourcen tilhører en afdeling, som er forskellig fra projektets kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5b51e-240">Hændelse</span><span class="sxs-lookup"><span data-stu-id="5b51e-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5b51e-241">Faktureret eller solgt projekt</span><span class="sxs-lookup"><span data-stu-id="5b51e-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5b51e-242">Projekt i fasen presales</span><span class="sxs-lookup"><span data-stu-id="5b51e-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5b51e-243">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="5b51e-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5b51e-244">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="5b51e-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5b51e-245">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b51e-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5b51e-246">Faktiske</span><span class="sxs-lookup"><span data-stu-id="5b51e-246">Actuals</span></span></th>
<th><span data-ttu-id="5b51e-247">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-247">Transaction currency</span></span></th>
<th><span data-ttu-id="5b51e-248">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b51e-248">Fixed price</span></span></th>
<th><span data-ttu-id="5b51e-249">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5b51e-250">Der oprettes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="5b51e-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5b51e-251">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="5b51e-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-252">Der indsendes en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="5b51e-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5b51e-253">Ingen aktivitet i objektet Faktiske</span><span class="sxs-lookup"><span data-stu-id="5b51e-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5b51e-254">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5b51e-255">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-255">Cost actual</span></span></td>
<td><span data-ttu-id="5b51e-256">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5b51e-257">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5b51e-258">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5b51e-259">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5b51e-260">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-261">Faktisk ikke-faktureret salg – Fakturerbart</span><span class="sxs-lookup"><span data-stu-id="5b51e-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5b51e-262">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-263">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5b51e-264">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-265">Internt salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5b51e-266">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5b51e-267">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="5b51e-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5b51e-268">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-268">Cost actual</span></span></td>
<td><span data-ttu-id="5b51e-269">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5b51e-270">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5b51e-271">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5b51e-272">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5b51e-273">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-274">Ressourceenhedsomkostning</span><span class="sxs-lookup"><span data-stu-id="5b51e-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5b51e-275">Ressourceenhedsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-276">Internt salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5b51e-277">Valuta for kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="5b51e-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-278">Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="5b51e-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5b51e-279">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-280">Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="5b51e-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b51e-281">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b51e-282">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="5b51e-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5b51e-283">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5b51e-284">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-285">Faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="5b51e-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-286">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-287">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5b51e-288">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-289">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-289">Billed sales</span></span></td>
<td><span data-ttu-id="5b51e-290">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b51e-291">En faktura bekræftes, og der sker et fald i fakturerbare timer.</span><span class="sxs-lookup"><span data-stu-id="5b51e-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5b51e-292">Tilbageførsel af ikke-faktureret salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5b51e-293">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-294">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-295">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-296">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b51e-297">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-298">Fakturerbart salg – Fakturerbart for det nye antal</span><span class="sxs-lookup"><span data-stu-id="5b51e-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5b51e-299">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-300">Fakturerbart salg – Ikke-fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="5b51e-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b51e-301">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b51e-302">En faktura er blevet rettet for at øge fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="5b51e-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5b51e-303">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="5b51e-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5b51e-304">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5b51e-305">Tilbageførsel af faktureret salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="5b51e-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5b51e-306">Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></span><span class="sxs-lookup"><span data-stu-id="5b51e-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5b51e-307">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5b51e-308">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5b51e-309">Ikke tilgængelig</span><span class="sxs-lookup"><span data-stu-id="5b51e-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-310">Faktureret salg</span><span class="sxs-lookup"><span data-stu-id="5b51e-310">Billed sales</span></span></td>
<td><span data-ttu-id="5b51e-311">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b51e-312">En faktura er blevet rettet for at reducere fakturerbart antal.</span><span class="sxs-lookup"><span data-stu-id="5b51e-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5b51e-313">Faktureret salg – Tilbageførsel</span><span class="sxs-lookup"><span data-stu-id="5b51e-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5b51e-314">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-315">Fakturerbart salg for det nye antal</span><span class="sxs-lookup"><span data-stu-id="5b51e-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5b51e-316">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b51e-317">Ikke-fakturerbart salg – Fakturerbart for differencen</span><span class="sxs-lookup"><span data-stu-id="5b51e-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b51e-318">Projektkontraktvaluta</span><span class="sxs-lookup"><span data-stu-id="5b51e-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
