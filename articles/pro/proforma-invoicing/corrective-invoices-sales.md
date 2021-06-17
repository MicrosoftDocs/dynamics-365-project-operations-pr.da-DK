---
title: Korrigerende projektfakturaer
description: Dette emne indeholder oplysninger om, hvordan du opretter og bekræfter korrigerende fakturaer i Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004074"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="45dd6-103">Korrigerende projektfakturaer</span><span class="sxs-lookup"><span data-stu-id="45dd6-103">Corrective project invoices</span></span>

<span data-ttu-id="45dd6-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="45dd6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="45dd6-105">En bekræftet projektfaktura kan rettes for at behandle ændringer eller kreditter i henhold til forhandlinger mellem kunden og projektlederen.</span><span class="sxs-lookup"><span data-stu-id="45dd6-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="45dd6-106">Hvis du vil foretage ændringer af en bekræftet faktura, skal du åbne den bekræftede faktura og vælge **Ret denne faktura**.</span><span class="sxs-lookup"><span data-stu-id="45dd6-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="45dd6-107">Denne markering er ikke tilgængelig, medmindre en projektfaktura er bekræftet.</span><span class="sxs-lookup"><span data-stu-id="45dd6-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="45dd6-108">Der oprettes en ny kladdefaktura ud fra den bekræftede faktura.</span><span class="sxs-lookup"><span data-stu-id="45dd6-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="45dd6-109">Alle fakturalinjedetaljer fra den tidligere bekræftede faktura kopieres til den nye kladde.</span><span class="sxs-lookup"><span data-stu-id="45dd6-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="45dd6-110">Her følger nogle af de vigtigste punkter om linjedetaljerne i den nye rettede faktura:</span><span class="sxs-lookup"><span data-stu-id="45dd6-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="45dd6-111">Alle mængder opdateres til nul.</span><span class="sxs-lookup"><span data-stu-id="45dd6-111">All quantities are updated to zero.</span></span> <span data-ttu-id="45dd6-112">Programmet antager, at alle fakturerede varer er helt krediteret.</span><span class="sxs-lookup"><span data-stu-id="45dd6-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="45dd6-113">Hvis det er nødvendigt, kan du opdatere mængderne manuelt, så det afspejler det antal, der er ved at blive faktureret, og ikke det antal, der krediteres.</span><span class="sxs-lookup"><span data-stu-id="45dd6-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="45dd6-114">På baggrund af det antal, du angiver, beregner programmet det krediterede antal.</span><span class="sxs-lookup"><span data-stu-id="45dd6-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="45dd6-115">Beløbet afspejles i de faktiske tal, der oprettes, når den rettede faktura bekræftes.</span><span class="sxs-lookup"><span data-stu-id="45dd6-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="45dd6-116">Hvis du foretager ændringer i momsbeløbet, skal du angive det korrekte momsbeløb og ikke det momsbeløb, der krediteres.</span><span class="sxs-lookup"><span data-stu-id="45dd6-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="45dd6-117">Tidligere bekræftede produktbaserede kontraktlinjer kopieres ikke.</span><span class="sxs-lookup"><span data-stu-id="45dd6-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="45dd6-118">Behandling af rettelser på en produktbaseret projektfaktura understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="45dd6-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="45dd6-119">Rettelser i relation til milepæle behandles altid som komplette kreditter.</span><span class="sxs-lookup"><span data-stu-id="45dd6-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="45dd6-120">Forskudshonorar eller forskudsbeløb kan rettes, hvis kunden er faktureret et forkert beløb.</span><span class="sxs-lookup"><span data-stu-id="45dd6-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="45dd6-121">Afstemninger af forskudshonorarer og forskud kan rettes, hvis der er brugt et forkert beløb til at afstemme i forhold til gebyrerne på en tidligere bekræftet faktura.</span><span class="sxs-lookup"><span data-stu-id="45dd6-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45dd6-122">De fakturalinjedetaljer, der er rettelser til andre allerede fakturerede opkrævninger, har feltet **Rettelse** angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="45dd6-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="45dd6-123">Fakturaer, der har rettede fakturalinjedetaljer, har et felt kaldet **Indeholder rettelser**, der også er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="45dd6-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="45dd6-124">Faktiske tal, der blev oprettet, da en korrigerende faktura blev bekræftet</span><span class="sxs-lookup"><span data-stu-id="45dd6-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="45dd6-125">I følgende tabel vises de faktiske værdier, der oprettes, når en korrigerende faktura bekræftes.</span><span class="sxs-lookup"><span data-stu-id="45dd6-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="45dd6-126">
                    <strong>Scenarie</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45dd6-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="45dd6-127">
                    <strong>De faktiske oplysninger, der blev oprettet i forbindelse med bekræftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45dd6-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="45dd6-128">Bekræfte rettelsen af et faktureret forskudshonorar eller forskud.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="45dd6-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-129">Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning.</span><span class="sxs-lookup"><span data-stu-id="45dd6-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="45dd6-130">Dette beløb er positivt, fordi det skal annullere det negative beløb, der blev oprettet, da forskudshonoraret eller forskuddet blev faktureret.</span><span class="sxs-lookup"><span data-stu-id="45dd6-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-131">Der oprettes en tilbageførelse af et faktureret faktisk salg lydende på beløbet for forskudshonoraret eller forskuddet for at tilbageføre det oprindelige fakturerede salg.</span><span class="sxs-lookup"><span data-stu-id="45dd6-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-132">Der oprettes en ny fakturering for faktisk salgsværdi for det rettede beløb på den rettede fakturalinje for forskudshonoraret eller forskuddet.</span><span class="sxs-lookup"><span data-stu-id="45dd6-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-133">En ikke-faktureret faktisk salgsværdi med et negativt pålydende beløb for den forskudshonorarbaserede eller forskudsbaserede fakturalinje, som skal anvendes til afstemningen.</span><span class="sxs-lookup"><span data-stu-id="45dd6-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="45dd6-134">Bekræftelse af rettelsen af et tidligere afstemt forskudshonorar eller forskud.</span><span class="sxs-lookup"><span data-stu-id="45dd6-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-135">Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning.</span><span class="sxs-lookup"><span data-stu-id="45dd6-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="45dd6-136">Dette beløb er positivt og skal udligne det negative beløb, der blev oprettet, da den tidligere afstemning blev foretaget.</span><span class="sxs-lookup"><span data-stu-id="45dd6-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-137">Tilbageførelse af fakturering af en faktisk salgsværdi svarende til beløbet på den forrige faktura.</span><span class="sxs-lookup"><span data-stu-id="45dd6-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-138">En ny fakturering for faktisk salgsværdi for det rettede beløb for forskudshonoraret, som anvendes på den rettede faktura.</span><span class="sxs-lookup"><span data-stu-id="45dd6-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-139">En ikke-faktureret faktisk salgsværdi med et negativt pålydende beløb fra det resterende beløb af forskudshonoraret eller forskuddet skal anvendes til afstemning af efterfølgende fakturaer.</span><span class="sxs-lookup"><span data-stu-id="45dd6-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45dd6-140">Fakturering af den fulde kredit for en tidligere faktureret tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="45dd6-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-141">En tilbageførelse af faktureret salg for tiden og beløbet på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="45dd6-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-142">En ny ikke-faktureret faktisk salgsværdi for tiden og beløbet på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="45dd6-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="45dd6-143">Fakturering af den delvise kredit på en tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="45dd6-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-144">En tilbageførelse af faktureret salg for tiden og beløbet faktureret på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="45dd6-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-145">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="45dd6-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-146">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for de resterende timer og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.</span><span class="sxs-lookup"><span data-stu-id="45dd6-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45dd6-147">Fakturering af den fulde kredit for en tidligere faktureret udgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="45dd6-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-148">En tilbageførelse af faktureret salg for antallet og beløbet på den oprindelige fakturalinjedetalje for udgiften.</span><span class="sxs-lookup"><span data-stu-id="45dd6-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-149">En ny ikke-faktureret faktisk salgsværdi salg for antallet og beløbet på den oprindelige fakturalinjedetalje for udgiften.</span><span class="sxs-lookup"><span data-stu-id="45dd6-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="45dd6-150">Fakturering af den delvise kredit for en tidligere faktureret udgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="45dd6-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-151">En tilbageførelse af faktureret salg for antallet og beløbet faktureret på den oprindelige fakturalinjedetalje for en udgift.</span><span class="sxs-lookup"><span data-stu-id="45dd6-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-152">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antallet og beløbet på den rettede fakturalinjedetalje, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="45dd6-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-153">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for det resterende antal og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.</span><span class="sxs-lookup"><span data-stu-id="45dd6-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45dd6-154">Fakturering af den fulde kredit for en tidligere faktureret materialetransaktion.</span><span class="sxs-lookup"><span data-stu-id="45dd6-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-155">En tilbageførsel af et faktureret salg for mængden og beløbet på den oprindelige fakturalinjedetaljer for materiale.</span><span class="sxs-lookup"><span data-stu-id="45dd6-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-156">En ny faktisk værdi for ikke-faktureret salg for mængden og beløbet på den oprindelige fakturalinjedetaljer for materiale.</span><span class="sxs-lookup"><span data-stu-id="45dd6-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="45dd6-157">Fakturering af den delvise kredit på en materialetransaktion.</span><span class="sxs-lookup"><span data-stu-id="45dd6-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-158">En tilbageførsel af et faktureret salg for den fakturerede mængde og beløb på den oprindelige fakturalinjedetaljer for materiale.</span><span class="sxs-lookup"><span data-stu-id="45dd6-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-159">En ny faktisk værdi for ikke-faktureret salg, der kan faktureres for mængden og beløbet på den redigerede fakturalinjedetalje, en tilbageførsel heraf, og et tilsvarende faktureret faktisk salg.</span><span class="sxs-lookup"><span data-stu-id="45dd6-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-160">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for det resterende antal og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.</span><span class="sxs-lookup"><span data-stu-id="45dd6-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45dd6-161">Fakturering af den fulde kredit for en tidligere faktureret gebyrtransaktion.</span><span class="sxs-lookup"><span data-stu-id="45dd6-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-162">En tilbageførelse af faktureret salg for antallet og beløbet på den oprindelige fakturalinjedetalje for gebyret.</span><span class="sxs-lookup"><span data-stu-id="45dd6-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-163">En ny ikke-faktureret faktisk salgsværdi salg for antallet og beløbet på den oprindelige fakturalinjedetalje for gebyret.</span><span class="sxs-lookup"><span data-stu-id="45dd6-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="45dd6-164">Fakturering af den delvise kredit for en tidligere faktureret gebyrtransaktion.</span><span class="sxs-lookup"><span data-stu-id="45dd6-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-165">En tilbageførelse af faktureret salg for antallet og beløbet faktureret på den oprindelige fakturalinjedetalje for gebyr.</span><span class="sxs-lookup"><span data-stu-id="45dd6-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-166">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antallet og beløbet på den redigerede rettede fakturalinjedetalje, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="45dd6-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="45dd6-167">Fakturering af den fulde kredit for en tidligere faktureret milepæl.</span><span class="sxs-lookup"><span data-stu-id="45dd6-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-168">En tilbageførelse af faktureret salg for beløbet på den oprindelige fakturalinjedetalje for milepælen.</span><span class="sxs-lookup"><span data-stu-id="45dd6-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="45dd6-169">Fakturastatussen for milepælen opdateres fra <b>Bogført kundefaktura</b> til <b>Klar til fakturering</b>.</span><span class="sxs-lookup"><span data-stu-id="45dd6-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="45dd6-170">Fakturering af den delvise kredit for en tidligere faktureret milepæl.</span><span class="sxs-lookup"><span data-stu-id="45dd6-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-171">Understøttes ikke</span><span class="sxs-lookup"><span data-stu-id="45dd6-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="45dd6-172">Kreditter og korrektioner for en tidligere faktureret produktbaseret kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="45dd6-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="45dd6-173">Understøttes ikke</span><span class="sxs-lookup"><span data-stu-id="45dd6-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
