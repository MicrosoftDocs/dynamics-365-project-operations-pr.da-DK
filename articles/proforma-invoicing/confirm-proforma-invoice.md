---
title: Bekræft en proformafaktura
description: Dette emne indeholder oplysninger om, hvordan du bekræfter en proformafaktura.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128096"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="04851-103">Bekræft en proformafaktura</span><span class="sxs-lookup"><span data-stu-id="04851-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="04851-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="04851-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="04851-105">Når en proforma-faktura er bekræftet, opdateres statussen for projektfakturaens til **Bekræftet**.</span><span class="sxs-lookup"><span data-stu-id="04851-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="04851-106">Når en faktura er blevet bekræftet, bliver den skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="04851-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="04851-107">Fakturaen kan fremadrettet kun rettes i tilfælde af rettelser ansporet af kunden eller kreditter, eller når den er markeret som betalt.</span><span class="sxs-lookup"><span data-stu-id="04851-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="04851-108">I følgende tabel vises de faktiske oplysninger, som systemet opretter.</span><span class="sxs-lookup"><span data-stu-id="04851-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="04851-109">Disse faktiske oplysninger oprettes, når bestemte operationer udføres på kladdeprojektfakturaen, før den bekræftes.</span><span class="sxs-lookup"><span data-stu-id="04851-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="04851-110">
                    <strong>Scenarie</strong>
                </span><span class="sxs-lookup"><span data-stu-id="04851-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="04851-111">
                    <strong>De faktiske oplysninger, der blev oprettet i forbindelse med bekræftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="04851-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04851-112">Fakturering af en tidstransaktion uden ændringer på kladdefakturaen.</span><span class="sxs-lookup"><span data-stu-id="04851-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-113">Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="04851-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-114">En faktureret faktisk salgsværdi af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="04851-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="04851-115">Fakturering af en tidstransaktion, der blev redigeret for at reducere antallet.</span><span class="sxs-lookup"><span data-stu-id="04851-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-116">Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="04851-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-117">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="04851-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-118">En ny ikke-faktureret faktisk salgsværdi, der ikke er fakturerbar for de resterende timer og beløb efter at have fratrukket de rettede tal på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="04851-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04851-119">Fakturering af en tidstransaktion, der blev redigeret for at øge antallet.</span><span class="sxs-lookup"><span data-stu-id="04851-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-120">Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="04851-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-121">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="04851-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04851-122">Fakturering af en udgiftstransaktion uden ændringer på kladdefakturaen.</span><span class="sxs-lookup"><span data-stu-id="04851-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-123">Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="04851-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-124">En faktureret faktisk salgsværdi for antallet og beløbet på den oprindelige udgiftsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="04851-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="04851-125">Fakturering af en udgiftstransaktion, der blev redigeret for at reducere antallet.</span><span class="sxs-lookup"><span data-stu-id="04851-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-126">Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="04851-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-127">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for det pågældende antal og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="04851-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-128">En ny ikke-faktureret faktisk salgsværdi, der ikke er fakturerbar for det resterende antal og beløb efter at have fratrukket de rettede tal på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="04851-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04851-129">Fakturering af en udgiftstransaktion, der blev redigeret for at øge antallet.</span><span class="sxs-lookup"><span data-stu-id="04851-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-130">Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="04851-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-131">En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antal og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.</span><span class="sxs-lookup"><span data-stu-id="04851-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04851-132">Fakturering af et gebyr.</span><span class="sxs-lookup"><span data-stu-id="04851-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-133">Tilbageførelse af gebyrbeløbet for ikke-faktureret salg på den oprindelige kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="04851-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-134">En faktureret faktisk salgsværdi for antallet og beløbet på den oprindelige gebyrkladdelinje.</span><span class="sxs-lookup"><span data-stu-id="04851-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="04851-135">Fakturering af en milepæl.</span><span class="sxs-lookup"><span data-stu-id="04851-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04851-136">Fakturering af en faktisk salgsværdi for milepælsbeløbet på den oprindelige milepæl på projektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="04851-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
