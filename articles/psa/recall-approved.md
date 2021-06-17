---
title: Tilbagekalde godkendte tids- eller udgiftsposter
description: Dette emne indeholder oplysninger om, hvordan du kan tilbagekalde en tidligere godkendt tids- eller udgiftstransaktion.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 71f75c1c516ca6e652baf311aa14e0c3fd4ba81e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998179"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="43261-103">Tilbagekalde godkendte tids- eller udgiftsposter</span><span class="sxs-lookup"><span data-stu-id="43261-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="43261-104">Et medlem af et projektteam eller en anden person, der sender en tids- eller udgiftspost, kan tilbagekalde denne tids- eller udgiftspost, efter at den er godkendt.</span><span class="sxs-lookup"><span data-stu-id="43261-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="43261-105">Fremgangsmåden for at tilbagekalde en godkendt tids- eller udgiftspost består af to trin:</span><span class="sxs-lookup"><span data-stu-id="43261-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="43261-106">En afsender anmoder om en tilbagekaldelse.</span><span class="sxs-lookup"><span data-stu-id="43261-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="43261-107">En godkender godkender tilbagekaldelsen.</span><span class="sxs-lookup"><span data-stu-id="43261-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="43261-108">Anmodning om tilbagekaldelse</span><span class="sxs-lookup"><span data-stu-id="43261-108">Request a recall</span></span>

<span data-ttu-id="43261-109">Følg disse trin for at anmode om tilbagekaldelse af en godkendt tids- eller udgiftspost.</span><span class="sxs-lookup"><span data-stu-id="43261-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="43261-110">I forbindelse med tidsposter skal du gå til **Projekter** \> **Mit arbejde** \> **Tidsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="43261-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="43261-111">eller</span><span class="sxs-lookup"><span data-stu-id="43261-111">–or–</span></span>

    <span data-ttu-id="43261-112">I forbindelse med tidsposter skal du gå til **Projekter** \> **Mit arbejde** \> **Udgifter**.</span><span class="sxs-lookup"><span data-stu-id="43261-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="43261-113">Ved tidsposter skal du vælge alle tidsposterne for en bestemt kombination af et projekt og en opgave.</span><span class="sxs-lookup"><span data-stu-id="43261-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="43261-114">Du kan også vælge de enkelte celler for tid på en bestemt dato i forbindelse med et bestemt projekt i gitteret.</span><span class="sxs-lookup"><span data-stu-id="43261-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="43261-115">eller</span><span class="sxs-lookup"><span data-stu-id="43261-115">–or–</span></span>

    <span data-ttu-id="43261-116">I forbindelse med udgiftsposter skal du markere rækken for den udgiftspost, der skal tilbagekaldes.</span><span class="sxs-lookup"><span data-stu-id="43261-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="43261-117">Vælg **Tilbagekalde**.</span><span class="sxs-lookup"><span data-stu-id="43261-117">Select **Recall**.</span></span> <span data-ttu-id="43261-118">En bekræftelsesdialogboks åbnes.</span><span class="sxs-lookup"><span data-stu-id="43261-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="43261-119">Hvis de valgte tids- og udgiftsposter allerede er godkendt, bliver du bedt om at angive en årsag til tilbagekaldelsen.</span><span class="sxs-lookup"><span data-stu-id="43261-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="43261-120">Angiv en årsag til tilbagekaldelsen, og vælg derefter **OK** for at bekræfte handlingen.</span><span class="sxs-lookup"><span data-stu-id="43261-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="43261-121">Systemet sender den person, som godkendte posterne, en anmodning om at godkende tilbagekaldelsen.</span><span class="sxs-lookup"><span data-stu-id="43261-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="43261-122">Selvom det er muligt at tilbagekalde godkendte tids- og udgiftsposter, så kan der ikke oprettes en anmodning om tilbagekaldelse, hvis en godkendt tid eller udgift allerede er faktureret til kunden.</span><span class="sxs-lookup"><span data-stu-id="43261-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="43261-123">En bruger, der forsøger at oprette en anmodning om tilbagekaldelse, modtager en meddelelse om, at tiden eller udgiften ikke kan tilbagekaldes, fordi den allerede er faktureret.</span><span class="sxs-lookup"><span data-stu-id="43261-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="43261-124">Godkende eller afvise en anmodning om tilbagekaldelse</span><span class="sxs-lookup"><span data-stu-id="43261-124">Approve or reject a recall request</span></span>

<span data-ttu-id="43261-125">Følg disse trin for at godkende eller afvise en anmodning om tilbagekaldelse.</span><span class="sxs-lookup"><span data-stu-id="43261-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="43261-126">Gå til **Projekter** \> **Mit arbejde** \> **Godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="43261-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="43261-127">Skift visningen til **Tilbagekald anmodninger om godkendelse** på listesiden **Godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="43261-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="43261-128">Der vises en liste over sendte anmodninger om tilbagekaldelser.</span><span class="sxs-lookup"><span data-stu-id="43261-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="43261-129">Vælg en eller flere poster, og vælg derefter enten **Godkend** eller **Afvis**.</span><span class="sxs-lookup"><span data-stu-id="43261-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="43261-130">Hvis du har valgt **Godkend**, modtager du en advarsel, der forklarer, hvordan godkendelsen virker.</span><span class="sxs-lookup"><span data-stu-id="43261-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="43261-131">Vælg **OK** for at bekræfte handlingen.</span><span class="sxs-lookup"><span data-stu-id="43261-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="43261-132">Anmodningen om tilbagekaldelse er godkendt</span><span class="sxs-lookup"><span data-stu-id="43261-132">The recall request is approved.</span></span>

    <span data-ttu-id="43261-133">eller</span><span class="sxs-lookup"><span data-stu-id="43261-133">–or–</span></span>

    <span data-ttu-id="43261-134">Hvis du har valgt **Afvis**, afvises anmodningen om tilbagekaldelse.</span><span class="sxs-lookup"><span data-stu-id="43261-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="43261-135">Som når der anmodes om tilbagekaldelse, kontrolleres det i systemet, om faktureringsaktiviteten for tids- og udgiftsposterne registreres, når en tilbagekaldelse godkendes.</span><span class="sxs-lookup"><span data-stu-id="43261-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="43261-136">Hvis en post allerede er faktureret, eller hvis den er på en kladdefaktura, modtager godkenderen en fejlmeddelelse, der angiver, at tiden eller udgiften ikke kan godkendes til tilbagekaldelse, da den allerede er blevet faktureret.</span><span class="sxs-lookup"><span data-stu-id="43261-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="43261-137">Virkning af en anmodning om tilbagekaldelse</span><span class="sxs-lookup"><span data-stu-id="43261-137">Impact of a recall request</span></span>

<span data-ttu-id="43261-138">Når en godkendelse tilbagekaldes, har det både driftsmæssige og økonomiske konsekvenser.</span><span class="sxs-lookup"><span data-stu-id="43261-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="43261-139">Driftsmæssig konsekvens</span><span class="sxs-lookup"><span data-stu-id="43261-139">Operational impact</span></span>

<span data-ttu-id="43261-140">Hvis en anmodning om tilbagekaldelse godkendes, markeres godkendelsesposten som **Afvist**.</span><span class="sxs-lookup"><span data-stu-id="43261-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="43261-141">Postens status ændres til enten **Returneret** eller **Afvist**, afhængigt af om det er en tidsregistrering eller en udgiftspost.</span><span class="sxs-lookup"><span data-stu-id="43261-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="43261-142">Projektteammedlemmet kan få vist poster, redigere og derefter sende poster igen eller slette posterne fuldstændigt.</span><span class="sxs-lookup"><span data-stu-id="43261-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="43261-143">Hvis en anmodning om tilbagekaldelse afvises, forbliver statussen for posten **Godkendt**, og posten kan ikke redigeres af projektteammedlemmet eller godkenderen for projektet.</span><span class="sxs-lookup"><span data-stu-id="43261-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="43261-144">Økonomisk konsekvens</span><span class="sxs-lookup"><span data-stu-id="43261-144">Financial impact</span></span>

<span data-ttu-id="43261-145">Hvis en tilbagekaldelse godkendes, opdateres de tilsvarende faktiske værdier for omkostninger og salg på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="43261-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="43261-146">Feltet **Justeringsstatus** opdateres til **Justeret**.</span><span class="sxs-lookup"><span data-stu-id="43261-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="43261-147">Feltet **Faktureringsstatus** opdateres til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="43261-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="43261-148">Dernæst oprettes der tilbageførselsposter i tabellen med faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="43261-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="43261-149">For at oprette tilbageførselsposter kopieres feltværdierne fra de oprindelige faktiske oplysninger i systemet.</span><span class="sxs-lookup"><span data-stu-id="43261-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="43261-150">De eneste værdier, der ikke kopieres over, er antalsværdier.</span><span class="sxs-lookup"><span data-stu-id="43261-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="43261-151">Disse værdier omgøres i stedet.</span><span class="sxs-lookup"><span data-stu-id="43261-151">These values are reversed instead.</span></span> <span data-ttu-id="43261-152">Tilbageførte faktiske værdier oprettes for både faktiske **Omkostninger** og **Ikke-faktureret salg**.</span><span class="sxs-lookup"><span data-stu-id="43261-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="43261-153">Feltet **Justeringsstatus** for de tilbageførte faktiske oplysninger angives til **Ikke-justerbar**, og feltet **Faktureringsstatus** angives til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="43261-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="43261-154">Pga. disse ændringer vil det registrerede beløb og omsætningens ordrebeholdning på projektet ikke længere medtage de beløb, som disse faktiske værdier repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="43261-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="43261-155">Hvis en anmodning om tilbagekaldelse afvises, har det ingen økonomisk indvirkning på projektet.</span><span class="sxs-lookup"><span data-stu-id="43261-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="43261-156">Ændringer af tidsregistreringsposter</span><span class="sxs-lookup"><span data-stu-id="43261-156">Changes to time entry records</span></span>

<span data-ttu-id="43261-157">I den følgende illustration vises de ændringer, der sker for godkendte tidsregistreringer, når de tilbagekaldes.</span><span class="sxs-lookup"><span data-stu-id="43261-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Tilstandsovergange for tidsregistreringer](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="43261-159">Ændringer af udgiftsregistreringsposter</span><span class="sxs-lookup"><span data-stu-id="43261-159">Changes to expense entry records</span></span>

<span data-ttu-id="43261-160">I den følgende illustration vises de ændringer, der sker for godkendte udgiftsposter, når de tilbagekaldes.</span><span class="sxs-lookup"><span data-stu-id="43261-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Tilstandsovergange for udgiftsposter](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]