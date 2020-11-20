---
title: Bekræft en proformafaktura - lille
description: Dette emne indeholder oplysninger om, hvordan du bekræfter proformafakturaer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176514"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="c8cf8-103">Bekræft en proformafaktura - lille</span><span class="sxs-lookup"><span data-stu-id="c8cf8-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="c8cf8-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c8cf8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c8cf8-105">Når en proforma-faktura er bekræftet, opdateres statussen for projektfakturaens til **Bekræftet**.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="c8cf8-106">Når en faktura er blevet bekræftet, bliver den skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="c8cf8-107">Fakturaen kan fremadrettet kun rettes i tilfælde af rettelser ansporet af kunden eller kreditter, eller når fakturaen er markeret som betalt.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="c8cf8-108">I følgende tabel vises de faktiske oplysninger, som systemet opretter.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="c8cf8-109">Disse faktiske oplysninger oprettes, når bestemte operationer udføres på kladdeprojektfakturaen, før den bekræftes.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="c8cf8-110">
                    <strong>Scenarie</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c8cf8-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="c8cf8-111">
                    <strong>De faktiske oplysninger, der blev oprettet i forbindelse med bekræftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c8cf8-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c8cf8-112">Fakturering af et forskud eller et forskudshonorar</span><span class="sxs-lookup"><span data-stu-id="c8cf8-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-113">Fakturering af faktisk salgsværdi af typen <strong>Forskudshonorar</strong> oprettes for det pålydende beløb for forskuddet eller forskudshonoraret.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-114">En ikke-faktureret faktisk salgsværdi med et negativt pålydende beløb for forskudshonoraret eller forskuddet skal anvendes til afstemningen.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c8cf8-115">Efter at have afstemt et forskudshonorar eller et forskud på en faktura fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-116">Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="c8cf8-117">Dette beløb er positivt, da det skal annullere det negative beløb, der blev oprettet, da forskudshonoraret eller forskuddet blev faktureret.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-118">Fakturering af en faktisk salgsværdi svarende til beløbet på den pågældende faktura.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c8cf8-119">Efter delvist at have afstemt et forskudshonorar eller et forskud på en faktura.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-120">Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="c8cf8-121">Dette beløb er positivt, da det skal annullere det negative beløb, der blev oprettet, da forskudshonoraret eller forskuddet blev faktureret.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-122">Fakturering af en faktisk salgsværdi svarende til beløbet på den pågældende faktura.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-123">En negativ ikke-faktureret faktisk salgsværdi lydende på det resterende beløb for forskudshonoraret eller forskuddet skal anvendes til afstemningen af fremtidige fakturaer.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c8cf8-124">Fakturering af en tidstransaktion uden ændringer på kladdefakturaen.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-125">Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-126">En faktureret faktisk salgsværdi af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c8cf8-127">Fakturering af en tidstransaktion, der blev redigeret for at reducere antallet.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-128">Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-129">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-130">En ny ikke-faktureret faktisk salgsværdi, der ikke er fakturerbar for de resterende timer og beløb efter at have fratrukket de rettede tal på det redigerede fakturalinjeniveau, en tilbageførsel af de faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c8cf8-131">Fakturering af en tidstransaktion, der blev redigeret for at øge antallet.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-132">Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-133">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c8cf8-134">Fakturering af en udgiftstransaktion uden ændringer på kladdefakturaen.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-135">Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-136">En faktureret faktisk salgsværdi for antallet og beløbet på den oprindelige udgiftsgodkendelse</span><span class="sxs-lookup"><span data-stu-id="c8cf8-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c8cf8-137">Fakturering af en udgiftstransaktion, der blev redigeret for at reducere antallet.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-138">Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-139">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for det pågældende antal og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-140">En ny ikke-faktureret faktisk salgsværdi, der ikke er fakturerbar for det resterende antal og beløb efter at have fratrukket de rettede tal på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c8cf8-141">Fakturering af en udgiftstransaktion, der blev redigeret for at øge antallet.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-142">Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-143">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antal og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c8cf8-144">Fakturering af et gebyr.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-145">Tilbageførelse af gebyrbeløbet for ikke-faktureret salg på den oprindelige kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-146">En faktureret faktisk salgsværdi for antallet og beløbet på den oprindelige gebyrkladdelinje.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c8cf8-147">Fakturering af en milepæl.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-148">Fakturering af en faktisk salgsværdi for milepælsbeløbet på den oprindelige milepæl på projektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c8cf8-149">Fakturering af en produktbaseret kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c8cf8-150">Fakturering af en faktisk salgsværdi for produktlinjen med det antal og beløb, der stammer fra den produktbaserede kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="c8cf8-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
