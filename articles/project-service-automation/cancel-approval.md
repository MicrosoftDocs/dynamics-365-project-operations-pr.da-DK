---
title: Annullere tidligere godkendte tids- og udgiftsposter
description: Dette emne indeholder oplysninger om, hvordan du kan annullere en godkendt projekttids- og udgiftstransaktion.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750459"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="73e2f-103">Annullere tidligere godkendte tids- eller udgiftsposter</span><span class="sxs-lookup"><span data-stu-id="73e2f-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="73e2f-104">I den nyeste version af Dynamics 365 Project Service Automation kan godkendere annullere tids- eller udgiftsposter, som de tidligere har godkendt.</span><span class="sxs-lookup"><span data-stu-id="73e2f-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="73e2f-105">Annullere en tidligere godkendt tids- eller udgiftspost</span><span class="sxs-lookup"><span data-stu-id="73e2f-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="73e2f-106">Følg disse trin for at annullere en tids- eller udgiftspost, du tidligere har godkendt.</span><span class="sxs-lookup"><span data-stu-id="73e2f-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="73e2f-107">Gå til **Projekter** \> **Mit arbejde** \> **Godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="73e2f-108">Skift visningen til **Mine tidligere godkendelser** på listesiden **Godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="73e2f-109">Der vises en liste over de poster for tid og udgift, som du tidligere har godkendt.</span><span class="sxs-lookup"><span data-stu-id="73e2f-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="73e2f-110">Vælg en eller flere poster, og vælg derefter **Annuller godkendelse**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="73e2f-111">Du modtager en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="73e2f-111">You receive a warning message.</span></span>
4. <span data-ttu-id="73e2f-112">Vælg **OK** for at annullere godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="73e2f-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="73e2f-113">Forstå effekten af at annullere en godkendelse af en tids- eller udgiftspost</span><span class="sxs-lookup"><span data-stu-id="73e2f-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="73e2f-114">Når en godkendelse annulleres, har det både driftsmæssige og økonomiske konsekvenser.</span><span class="sxs-lookup"><span data-stu-id="73e2f-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="73e2f-115">Driftsmæssig konsekvens</span><span class="sxs-lookup"><span data-stu-id="73e2f-115">Operational impact</span></span>

<span data-ttu-id="73e2f-116">Når en godkendelse annulleres på siden handlinger, nulstilles postens status til **Kladde**, og godkendelsen vises ikke længere i visningen **Mine tidligere godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="73e2f-117">I stedet vises den annullerede godkendelse i enten visningen **Tidsregistreringer til godkendelse** eller **Udgiftsposteringer til godkendelse**, afhængigt af om det var en tidspost eller en udgiftspost.</span><span class="sxs-lookup"><span data-stu-id="73e2f-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="73e2f-118">Derudover ændres status for den relaterede tids- eller udgiftspost til **Sendt**, så den relaterede post er i overensstemmelse med godkendelser, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="73e2f-119">Som godkender kan du redigere nogle af felterne i en godkendelse, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="73e2f-120">Disse felter omfatter **Faktureringstype** og **Fakturerbare timer for tidsregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="73e2f-121">Når du har foretaget ændringerne, kan du godkende posten igen.</span><span class="sxs-lookup"><span data-stu-id="73e2f-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="73e2f-122">Du kan også vælge at afvise posten.</span><span class="sxs-lookup"><span data-stu-id="73e2f-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="73e2f-123">Hvis du afviser godkendelsen af en tidsregistrering, ændres dens status til **Returneret**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="73e2f-124">Hvis du afviser godkendelsen af en udgiftspost, ændres dens status til **Afvist**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="73e2f-125">Både returnerede og afviste poster fungerer som en post, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="73e2f-126">Et projektteammedlem kan enten foretage de nødvendige ændringer af posten og derefter sende den til godkendelse igen eller slette posten fuldstændigt.</span><span class="sxs-lookup"><span data-stu-id="73e2f-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="73e2f-127">Økonomisk konsekvens</span><span class="sxs-lookup"><span data-stu-id="73e2f-127">Financial impact</span></span>

<span data-ttu-id="73e2f-128">Et projekt påvirkes også økonomisk, når en godkendelse annulleres.</span><span class="sxs-lookup"><span data-stu-id="73e2f-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="73e2f-129">Først opdateres de tilsvarende faktiske værdier for omkostninger og salg på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="73e2f-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="73e2f-130">Justeringsstatus angives til **Justeret**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="73e2f-131">Faktureringsstatus angives til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="73e2f-132">Dernæst oprettes der tilbageførselsposter i tabellen med faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="73e2f-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="73e2f-133">For at oprette tilbageførselsposter kopieres feltværdierne fra de oprindelige faktiske oplysninger i systemet.</span><span class="sxs-lookup"><span data-stu-id="73e2f-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="73e2f-134">De eneste værdier, der ikke kopieres over, er antalsværdier.</span><span class="sxs-lookup"><span data-stu-id="73e2f-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="73e2f-135">Disse værdier omgøres i stedet.</span><span class="sxs-lookup"><span data-stu-id="73e2f-135">These values are reversed instead.</span></span> <span data-ttu-id="73e2f-136">Tilbageførte faktiske værdier oprettes for både faktiske **Omkostninger** og **Ikke-faktureret salg**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="73e2f-137">Feltet **Justeringsstatus** i de tilbageførte faktiske oplysninger angives til **Ikke-justerbar**, og faktureringsstatussen angives til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="73e2f-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="73e2f-138">Når disse ændringer er foretaget, vil det beløb, der er registreret som brugt på projektet, og omsætningens ordrebeholdning på projektet ikke længere medtage de beløb, som disse faktiske værdier repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="73e2f-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
