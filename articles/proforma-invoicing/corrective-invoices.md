---
title: Korrigerende projektbaserede fakturaer
description: Dette emne indeholder oplysninger om, hvordan du opretter og bekræfter korrigerende projektbaserede fakturaer i Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012264"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="891e6-103">Korrigerende projektbaserede fakturaer</span><span class="sxs-lookup"><span data-stu-id="891e6-103">Corrective project-based invoices</span></span>

<span data-ttu-id="891e6-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="891e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="891e6-105">En bekræftet projektfaktura kan rettes for at behandle ændringer eller kreditter i henhold til forhandlinger mellem kunden og projektlederen.</span><span class="sxs-lookup"><span data-stu-id="891e6-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="891e6-106">Hvis du vil foretage ændringer af en bekræftet faktura, skal du åbne den bekræftede faktura og vælge **Ret denne faktura**.</span><span class="sxs-lookup"><span data-stu-id="891e6-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="891e6-107">Dette valg er ikke tilgængeligt, medmindre en projektfaktura er bekræftet, eller den projektbaserede faktura har forskud eller forskudshonorarer eller afstemninger af forskud eller forskudshonorarer.</span><span class="sxs-lookup"><span data-stu-id="891e6-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="891e6-108">Der oprettes en ny kladdefaktura ud fra den bekræftede faktura.</span><span class="sxs-lookup"><span data-stu-id="891e6-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="891e6-109">Alle fakturalinjedetaljer fra den tidligere bekræftede faktura kopieres til den nye kladde.</span><span class="sxs-lookup"><span data-stu-id="891e6-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="891e6-110">Her følger nogle af de vigtigste punkter om linjedetaljerne i den nye rettede faktura:</span><span class="sxs-lookup"><span data-stu-id="891e6-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="891e6-111">Alle mængder opdateres til nul.</span><span class="sxs-lookup"><span data-stu-id="891e6-111">All quantities are updated to zero.</span></span> <span data-ttu-id="891e6-112">Dynamics 365 Project Operations antager, at alle fakturerede elementer er fuldt krediteret.</span><span class="sxs-lookup"><span data-stu-id="891e6-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="891e6-113">Hvis det er nødvendigt, kan du opdatere mængderne manuelt, så det afspejler det antal, der er ved at blive faktureret, og ikke det antal, der krediteres.</span><span class="sxs-lookup"><span data-stu-id="891e6-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="891e6-114">På baggrund af det antal, du angiver, beregner programmet det krediterede antal.</span><span class="sxs-lookup"><span data-stu-id="891e6-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="891e6-115">Beløbet afspejles i de faktiske tal, der oprettes, når den rettede faktura bekræftes.</span><span class="sxs-lookup"><span data-stu-id="891e6-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="891e6-116">Hvis du foretager ændringer i momsbeløbet, skal du angive det korrekte momsbeløb og ikke det momsbeløb, der krediteres.</span><span class="sxs-lookup"><span data-stu-id="891e6-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="891e6-117">Rettelser i relation til milepæle behandles altid som komplette kreditter.</span><span class="sxs-lookup"><span data-stu-id="891e6-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="891e6-118">Hvis det drejer sig om fakturalinjedetaljer, der er rettelser til andre allerede fakturerede opkrævninger, angives feltet **Korrektion** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="891e6-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="891e6-119">For så vidt angår fakturaer med korrigerede fakturalinjedetaljer, angives feltet **Indeholder rettelser** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="891e6-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="891e6-120">Faktiske tal, der blev oprettet, da en korrigerende faktura blev bekræftet</span><span class="sxs-lookup"><span data-stu-id="891e6-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="891e6-121">I følgende tabel vises de faktiske værdier, der oprettes, når en korrigerende faktura bekræftes.</span><span class="sxs-lookup"><span data-stu-id="891e6-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="891e6-122">
                    <strong>Scenarie</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891e6-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="891e6-123">
                    <strong>De faktiske oplysninger, der blev oprettet i forbindelse med bekræftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="891e6-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891e6-124">Fakturering af den fulde kredit for en tidligere faktureret tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="891e6-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-125">En tilbageførelse af faktureret salg for tiden og beløbet på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="891e6-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-126">En ny ikke-faktureret faktisk salgsværdi for tiden og beløbet på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="891e6-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="891e6-127">Fakturering af den delvise kredit på en tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="891e6-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-128">En tilbageførelse af faktureret salg for tiden og beløbet faktureret på den oprindelige fakturalinjedetalje for tid.</span><span class="sxs-lookup"><span data-stu-id="891e6-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-129">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="891e6-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-130">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for de resterende timer og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.</span><span class="sxs-lookup"><span data-stu-id="891e6-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891e6-131">Fakturering af den fulde kredit for en tidligere faktureret udgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="891e6-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-132">En tilbageførelse af faktureret salg for antallet og beløbet på den oprindelige fakturalinjedetalje for udgiften.</span><span class="sxs-lookup"><span data-stu-id="891e6-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-133">En ny ikke-faktureret faktisk salgsværdi salg for antallet og beløbet på den oprindelige fakturalinjedetalje for udgiften.</span><span class="sxs-lookup"><span data-stu-id="891e6-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="891e6-134">Fakturering af den delvise kredit for en tidligere faktureret udgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="891e6-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-135">En tilbageførelse af faktureret salg for antallet og beløbet faktureret på den oprindelige fakturalinjedetalje for en udgift.</span><span class="sxs-lookup"><span data-stu-id="891e6-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-136">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antallet og beløbet på den rettede fakturalinjedetalje, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="891e6-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-137">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for det resterende antal og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.</span><span class="sxs-lookup"><span data-stu-id="891e6-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891e6-138">Fakturering af den fulde kredit for en tidligere faktureret materialetransaktion.</span><span class="sxs-lookup"><span data-stu-id="891e6-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-139">En tilbageførsel af et faktureret salg for mængden og beløbet på den oprindelige fakturalinjedetaljer for materiale.</span><span class="sxs-lookup"><span data-stu-id="891e6-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-140">En ny faktisk værdi for ikke-faktureret salg for mængden og beløbet på den oprindelige fakturalinjedetaljer for materiale.</span><span class="sxs-lookup"><span data-stu-id="891e6-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="891e6-141">Fakturering af den delvise kredit på en materialetransaktion.</span><span class="sxs-lookup"><span data-stu-id="891e6-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-142">En tilbageførsel af et faktureret salg for den fakturerede mængde og beløb på den oprindelige fakturalinjedetaljer for materiale.</span><span class="sxs-lookup"><span data-stu-id="891e6-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-143">En ny faktisk værdi for ikke-faktureret salg, der kan faktureres for mængden og beløbet på den redigerede fakturalinjedetalje, en tilbageførsel heraf, og et tilsvarende faktureret faktisk salg.</span><span class="sxs-lookup"><span data-stu-id="891e6-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-144">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for det resterende antal og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.</span><span class="sxs-lookup"><span data-stu-id="891e6-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891e6-145">Fakturering af den fulde kredit for en tidligere faktureret gebyrtransaktion.</span><span class="sxs-lookup"><span data-stu-id="891e6-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-146">En tilbageførelse af faktureret salg for antallet og beløbet på den oprindelige fakturalinjedetalje for gebyret.</span><span class="sxs-lookup"><span data-stu-id="891e6-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-147">En ny ikke-faktureret faktisk salgsværdi salg for antallet og beløbet på den oprindelige fakturalinjedetalje for gebyret.</span><span class="sxs-lookup"><span data-stu-id="891e6-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="891e6-148">Fakturering af den delvise kredit for en tidligere faktureret gebyrtransaktion.</span><span class="sxs-lookup"><span data-stu-id="891e6-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-149">En tilbageførelse af faktureret salg for antallet og beløbet faktureret på den oprindelige fakturalinjedetalje for gebyr.</span><span class="sxs-lookup"><span data-stu-id="891e6-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-150">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antallet og beløbet på den redigerede rettede fakturalinjedetalje, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="891e6-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="891e6-151">Fakturering af den fulde kredit for en tidligere faktureret milepæl.</span><span class="sxs-lookup"><span data-stu-id="891e6-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-152">En tilbageførelse af faktureret salg for beløbet på den oprindelige fakturalinjedetalje for milepælen.</span><span class="sxs-lookup"><span data-stu-id="891e6-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="891e6-153">Fakturastatussen for milepælen opdateres fra <b>Bogført kundefaktura</b> til <b>Klar til fakturering</b>.</span><span class="sxs-lookup"><span data-stu-id="891e6-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="891e6-154">Fakturering af den delvise kredit for en tidligere faktureret milepæl.</span><span class="sxs-lookup"><span data-stu-id="891e6-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="891e6-155">Dette scenarie understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="891e6-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
