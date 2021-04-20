---
title: Opret korrigerende projektbaserede fakturaer
description: Dette emne indeholder oplysninger om korrigerende fakturaer i Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788844"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="dbe21-103">Opret korrigerende projektbaserede fakturaer</span><span class="sxs-lookup"><span data-stu-id="dbe21-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="dbe21-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="dbe21-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dbe21-105">En bekræftet projektfaktura kan rettes for at behandle ændringer eller kreditter i henhold til forhandlinger mellem kunden og projektlederen.</span><span class="sxs-lookup"><span data-stu-id="dbe21-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="dbe21-106">Hvis du vil foretage ændringer af en bekræftet faktura, skal du åbne den bekræftede faktura og vælge **Ret denne faktura**.</span><span class="sxs-lookup"><span data-stu-id="dbe21-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="dbe21-107">Denne markering er ikke tilgængelig, medmindre en projektfaktura er bekræftet.</span><span class="sxs-lookup"><span data-stu-id="dbe21-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="dbe21-108">Der oprettes en ny kladdefaktura ud fra den bekræftede faktura.</span><span class="sxs-lookup"><span data-stu-id="dbe21-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="dbe21-109">Alle fakturalinjedetaljer fra den tidligere bekræftede faktura kopieres til den nye kladde.</span><span class="sxs-lookup"><span data-stu-id="dbe21-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="dbe21-110">Følgende er nogle af de vigtige punkter, der kan hjælpe dig med bedre at forstå linjedetaljerne på den nye korrigerede faktura:</span><span class="sxs-lookup"><span data-stu-id="dbe21-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="dbe21-111">Alle mængder opdateres til nul.</span><span class="sxs-lookup"><span data-stu-id="dbe21-111">All quantities are updated to zero.</span></span> <span data-ttu-id="dbe21-112">Dette forudsætter, at alle fakturerede elementer er fuldt krediteret.</span><span class="sxs-lookup"><span data-stu-id="dbe21-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="dbe21-113">Hvis det er nødvendigt, kan du opdatere mængderne manuelt, så det afspejler det antal, der er ved at blive faktureret, og ikke det antal, der krediteres.</span><span class="sxs-lookup"><span data-stu-id="dbe21-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="dbe21-114">På baggrund af det antal, du angiver, beregner programmet det krediterede antal.</span><span class="sxs-lookup"><span data-stu-id="dbe21-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="dbe21-115">Beløbet afspejles i de faktiske tal, der oprettes, når den rettede faktura bekræftes.</span><span class="sxs-lookup"><span data-stu-id="dbe21-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="dbe21-116">Hvis du foretager ændringer i momsbeløbet, skal du angive det korrekte momsbeløb og ikke det momsbeløb, der krediteres.</span><span class="sxs-lookup"><span data-stu-id="dbe21-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="dbe21-117">Rettelser i relation til milepæle behandles altid som komplette kreditter.</span><span class="sxs-lookup"><span data-stu-id="dbe21-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="dbe21-118">Forskudshonorar eller forskudsbeløb kan rettes, hvis kunden er faktureret et forkert beløb.</span><span class="sxs-lookup"><span data-stu-id="dbe21-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="dbe21-119">Afstemninger af forskudshonorarer og forskud kan rettes, hvis der er brugt et forkert beløb til at afstemme i forhold til gebyrerne på en tidligere bekræftet faktura.</span><span class="sxs-lookup"><span data-stu-id="dbe21-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbe21-120">Fakturalinjedetaljer, der er rettelser til andre allerede fakturerede opkrævninger, har feltet **Korrektion** angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dbe21-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="dbe21-121">Fakturaer, der har rettede fakturalinjedetaljer, har et felt kaldet **Indeholder rettelser**, der også er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dbe21-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="dbe21-122">Faktiske tal, der er oprettede på Bekræftelse af en rettelsesfaktura</span><span class="sxs-lookup"><span data-stu-id="dbe21-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="dbe21-123">I følgende tabel vises de faktiske værdier, der oprettes, når en korrigerende faktura bekræftes.</span><span class="sxs-lookup"><span data-stu-id="dbe21-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="dbe21-124">
                    <strong>Scenarie</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dbe21-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="dbe21-125">
                    <strong>De faktiske oplysninger, der blev oprettet i forbindelse med bekræftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dbe21-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="dbe21-126">Bekræfte rettelsen af et faktureret forskudshonorar eller forskud.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="dbe21-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-127">Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning.</span><span class="sxs-lookup"><span data-stu-id="dbe21-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="dbe21-128">Dette beløb er positivt, fordi det skal annullere det negative beløb, der blev oprettet, da forskudshonoraret eller forskuddet blev faktureret.</span><span class="sxs-lookup"><span data-stu-id="dbe21-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-129">Der oprettes en tilbageførelse af et faktureret faktisk salg lydende på beløbet for forskudshonoraret eller forskuddet for at tilbageføre det oprindelige fakturerede salg.</span><span class="sxs-lookup"><span data-stu-id="dbe21-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-130">Der oprettes en ny fakturering for faktisk salgsværdi for det rettede beløb på den rettede fakturalinje for forskudshonoraret eller forskuddet.</span><span class="sxs-lookup"><span data-stu-id="dbe21-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-131">En ikke-faktureret faktisk salgsværdi med et negativt pålydende beløb for den forskudshonorarbaserede eller forskudsbaserede fakturalinje, som skal anvendes til afstemningen.</span><span class="sxs-lookup"><span data-stu-id="dbe21-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="dbe21-132">Bekræftelse af rettelsen af et tidligere afstemt forskudshonorar eller forskud.</span><span class="sxs-lookup"><span data-stu-id="dbe21-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-133">Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning.</span><span class="sxs-lookup"><span data-stu-id="dbe21-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="dbe21-134">Dette beløb er positivt og skal udligne det negative beløb, der blev oprettet, da den tidligere afstemning blev foretaget.</span><span class="sxs-lookup"><span data-stu-id="dbe21-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-135">Tilbageførelse af fakturering af en faktisk salgsværdi svarende til beløbet på den forrige faktura.</span><span class="sxs-lookup"><span data-stu-id="dbe21-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-136">En ny fakturering for faktisk salgsværdi for det rettede beløb for forskudshonoraret, som anvendes på den rettede faktura.</span><span class="sxs-lookup"><span data-stu-id="dbe21-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-137">En ikke-faktureret faktisk salgsværdi med et negativt pålydende beløb fra det resterende beløb af forskudshonoraret eller forskuddet skal anvendes til afstemning af efterfølgende fakturaer.</span><span class="sxs-lookup"><span data-stu-id="dbe21-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbe21-138">Fakturering af den fulde kredit for en tidligere faktureret tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="dbe21-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-139">En tilbageførelse af faktureret salg for tiden og beløbet på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="dbe21-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-140">En ny ikke-faktureret faktisk salgsværdi for tiden og beløbet på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="dbe21-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="dbe21-141">Fakturering af den delvise kredit på en tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="dbe21-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-142">En tilbageførelse af faktureret salg for tiden og beløbet faktureret på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="dbe21-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-143">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="dbe21-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-144">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for de resterende timer og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.</span><span class="sxs-lookup"><span data-stu-id="dbe21-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbe21-145">Fakturering af den fulde kredit for en tidligere faktureret udgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="dbe21-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-146">En tilbageførelse af faktureret salg for antallet og beløbet på den oprindelige fakturalinjedetalje for udgiften.</span><span class="sxs-lookup"><span data-stu-id="dbe21-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-147">En ny ikke-faktureret faktisk salgsværdi salg for antallet og beløbet på den oprindelige fakturalinjedetalje for udgiften.</span><span class="sxs-lookup"><span data-stu-id="dbe21-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="dbe21-148">Fakturering af den delvise kredit for en tidligere faktureret udgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="dbe21-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-149">En tilbageførelse af faktureret salg for antallet og beløbet faktureret på den oprindelige fakturalinjedetalje for en udgift.</span><span class="sxs-lookup"><span data-stu-id="dbe21-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-150">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antallet og beløbet på den rettede fakturalinjedetalje, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="dbe21-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-151">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for det resterende antal og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.</span><span class="sxs-lookup"><span data-stu-id="dbe21-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbe21-152">Fakturering af den fulde kredit for en tidligere faktureret gebyrtransaktion.</span><span class="sxs-lookup"><span data-stu-id="dbe21-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-153">En tilbageførelse af faktureret salg for antallet og beløbet på den oprindelige fakturalinjedetalje for gebyret.</span><span class="sxs-lookup"><span data-stu-id="dbe21-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-154">En ny ikke-faktureret faktisk salgsværdi salg for antallet og beløbet på den oprindelige fakturalinjedetalje for gebyret.</span><span class="sxs-lookup"><span data-stu-id="dbe21-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbe21-155">Fakturering af den delvise kredit for en tidligere faktureret gebyrtransaktion.</span><span class="sxs-lookup"><span data-stu-id="dbe21-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-156">En tilbageførelse af faktureret salg for antallet og beløbet faktureret på den oprindelige fakturalinjedetalje for gebyr.</span><span class="sxs-lookup"><span data-stu-id="dbe21-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-157">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antallet og beløbet på den redigerede rettede fakturalinjedetalje, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="dbe21-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="dbe21-158">Fakturering af den fulde kredit for en tidligere faktureret milepæl.</span><span class="sxs-lookup"><span data-stu-id="dbe21-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-159">En tilbageførelse af faktureret salg for beløbet på den oprindelige fakturalinjedetalje for milepælen.</span><span class="sxs-lookup"><span data-stu-id="dbe21-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="dbe21-160">Fakturastatussen på milepælen opdateres fra <b>Bogført kundefaktura</b> til <b>Klar til fakturering</b>.</span><span class="sxs-lookup"><span data-stu-id="dbe21-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="dbe21-161">Fakturering af den delvise kredit for en tidligere faktureret milepæl.</span><span class="sxs-lookup"><span data-stu-id="dbe21-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbe21-162">Understøttes ikke</span><span class="sxs-lookup"><span data-stu-id="dbe21-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
