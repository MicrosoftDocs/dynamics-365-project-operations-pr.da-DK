---
title: Overfør projektbudgetter ved afslutning af regnskabsåret
description: Denne artikel indeholder oplysninger om, hvordan du kan overføre resterende budgetbeløb til fremtidige år og oprette detaljer om budgetregistrering.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074305"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="6d851-103">Overfør projektbudgetter ved afslutning af regnskabsåret</span><span class="sxs-lookup"><span data-stu-id="6d851-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d851-104">Når du arbejder på et flerårigt projekt, kan du have et overskydende budget i slutningen af regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="6d851-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="6d851-105">Du kan overføre de resterende budgetbeløb til et fremtidigt år og oprette detaljer budgetregistrering for beløbene i de tilknyttede finanskonti.</span><span class="sxs-lookup"><span data-stu-id="6d851-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="6d851-106">Før du overfører de resterende beløb, skal du gennemgå og analysere de resterende budgetbeløb.</span><span class="sxs-lookup"><span data-stu-id="6d851-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="6d851-107">Gennemgå og analysere de resterende budgetbeløb</span><span class="sxs-lookup"><span data-stu-id="6d851-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="6d851-108">Benyt følgende fremgangsmåde for at gennemgå budgetbeløbene ved årsafslutning for projekter uden at overføre beløbene.</span><span class="sxs-lookup"><span data-stu-id="6d851-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="6d851-109">Gå til **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overfør budgetter**.</span><span class="sxs-lookup"><span data-stu-id="6d851-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="6d851-110">På siden **Proces for overførsel af projektbudget** skal du på fanen **Indstillinger for årsafslutning** kontrollere, at **Overfør de resterende projektbudgetbeløb** ikke er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="6d851-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="6d851-111">På fanen **Parametre** skal du i feltet **Projektbudgetår** vælge det regnskabsår, som du vil have vist det resterende budgetbeløb for.</span><span class="sxs-lookup"><span data-stu-id="6d851-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="6d851-112">I feltet **Første regnskabsår** skal du vælge det regnskabsår, som du vil have vist det resterende budgetbeløb for.</span><span class="sxs-lookup"><span data-stu-id="6d851-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="6d851-113">I feltet **Fra prognosemodel** skal du vælge **Resterende buget**.</span><span class="sxs-lookup"><span data-stu-id="6d851-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="6d851-114">Hvis du vil inkludere projekter, der opfylder de valgte kriterier, og som ikke har et resterende budget, skal du vælge **Vis ingen resterende**.</span><span class="sxs-lookup"><span data-stu-id="6d851-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="6d851-115">På fanen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle budgetter, der opfylder de valgte kriterier og derefter vælge **Behandl**.</span><span class="sxs-lookup"><span data-stu-id="6d851-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="6d851-116">Hvis du vil designe en databaseforespørgsel, der indlæser et bestemt sæt budgetter i ruden, skal du vælge **Hent valgte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="6d851-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="6d851-117">Du kan finde flere oplysninger om en bestemt linje i ruden ved at markere linjen og derefter vælge **Se budgetdetaljer** eller **Se konti**.</span><span class="sxs-lookup"><span data-stu-id="6d851-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="6d851-118">Overfør de resterende budgetbeløb</span><span class="sxs-lookup"><span data-stu-id="6d851-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="6d851-119">Når du behandler de resterende budgetbeløb, kan du oprette transaktioner i finanskladden for de beløb, som du overfører.</span><span class="sxs-lookup"><span data-stu-id="6d851-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="6d851-120">Hvis du vil oprette transaktioner i finanskladden, skal du udføre trinnene i sektionen [Overfør budgetbeløb og opret transaktioner i finanskladden](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="6d851-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="6d851-121">De budgetbeløb, der overføres, overføres til den prognosemodel, der er valgt på siden **Prognosemodeller** som den overførte prognosemodel.</span><span class="sxs-lookup"><span data-stu-id="6d851-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="6d851-122">Overfør budgetbeløb og opret transaktioner i finanskladden</span><span class="sxs-lookup"><span data-stu-id="6d851-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="6d851-123">Vælg **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overfør budgetter**.</span><span class="sxs-lookup"><span data-stu-id="6d851-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="6d851-124">På siden **Proces for overførsel af projektbudget** skal du vælge **Årsafslutning** og derefter aktivere **Overfør de resterende projektbudgetbeløb** og **Opret budgetregisterposter i finanskladden**.</span><span class="sxs-lookup"><span data-stu-id="6d851-124">On the **Project budget carry-forward process** page, select **Year-end** , and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="6d851-125">På fanen **Parametre** skal du i feltgruppen **Projektparametre** vælge følgende:</span><span class="sxs-lookup"><span data-stu-id="6d851-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="6d851-126">**Projektbudgetår** : Vælg starten af det regnskabsår, som du vil have vist de resterende budgetbeløb for.</span><span class="sxs-lookup"><span data-stu-id="6d851-126">**Project budget year** : Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="6d851-127">**Drift** : Opret driftstransaktioner i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="6d851-127">**Profit and loss** : Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="6d851-128">**IGVA** : Opret transaktioner for IGVA (igangværende arbejde) i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="6d851-128">**WIP** : Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="6d851-129">**Løn** : Opret lønfordelingstransaktioner i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="6d851-129">**Payroll** : Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="6d851-130">I feltgruppen **Finanskladde** skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="6d851-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="6d851-131">I feltet **Første regnskabsår** skal du vælge det regnskabsår, som du vil overført det resterende budgetbeløb til for projekterne.</span><span class="sxs-lookup"><span data-stu-id="6d851-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="6d851-132">Standardværdien er ét år efter værdien i feltet **Projektbudgetår**.</span><span class="sxs-lookup"><span data-stu-id="6d851-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="6d851-133">I feltet **Overførelsesperiode** skal du vælge den periode, som du vil oprette budgetregisteroplysningerne for i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="6d851-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="6d851-134">Dette er typisk den første periode i det første regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="6d851-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="6d851-135">I feltgruppen **Kopier fra/til** skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="6d851-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="6d851-136">I feltet **Fra prognosemodel** skal du vælge den prognosemodel for projektbudgettet, der er knyttet til de resterende budgetbeløb, som du vil overføre for projekterne.</span><span class="sxs-lookup"><span data-stu-id="6d851-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="6d851-137">I feltet **til finansbudgetmodel** skal du vælge den finansbudgetmodel, der er knyttet til de budgetbeløb, som du vil overføre til finanskladden.</span><span class="sxs-lookup"><span data-stu-id="6d851-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="6d851-138">Vælg **Overfør salgsvaluta** , hvis du vil bruge projektets salgsvaluta til de transaktioner i finanskladden, der oprettes, når du overfører budgetbeløbene for projekterne.</span><span class="sxs-lookup"><span data-stu-id="6d851-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="6d851-139">Hvis indstillingen ikke er valgt, bruger transaktionerne regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="6d851-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="6d851-140">Vælg **Vis ingen resterende** for at inkludere projekter, der ikke har nogen resterende budgetbeløb, men opfylder de øvrige kriterier, som du har valgt i de projekter, der vises i den nederste rude.</span><span class="sxs-lookup"><span data-stu-id="6d851-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="6d851-141">På fanen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle de budgetter, der opfylder de valgte kriterier.</span><span class="sxs-lookup"><span data-stu-id="6d851-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="6d851-142">Hvis du foretrækker at designe en databaseforespørgsel, der indlæser et bestemt sæt projektbudgetter i ruden, skal du vælge **Hent valgte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="6d851-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="6d851-143">For hvert projekt, du vil behandle, skal du vælge indstillingen i starten af linjen for projektet.</span><span class="sxs-lookup"><span data-stu-id="6d851-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="6d851-144">Hvis du vil markere alle eller de fleste af projekterne, skal du markere afkrydsningsfeltet øverst til venstre.</span><span class="sxs-lookup"><span data-stu-id="6d851-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="6d851-145">Hvis du vil udelade behandlingen af et projekt, skal du fjerne markeringen i dette projekt.</span><span class="sxs-lookup"><span data-stu-id="6d851-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="6d851-146">Hvis du vil overføre de resterende budgetbeløb for de valgte projekter til det valgte regnskabsår og oprette budgetregisterdetaljer i finanskladden, skal du vælge **Behandl**.</span><span class="sxs-lookup"><span data-stu-id="6d851-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="6d851-147">Overfør budgetbeløb uden at oprette transaktioner i finanskladden</span><span class="sxs-lookup"><span data-stu-id="6d851-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="6d851-148">Gå til **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overfør budgetter**.</span><span class="sxs-lookup"><span data-stu-id="6d851-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="6d851-149">På siden **Proces for overførsel af projektbudget** skal du i feltet **Indstillinger for årsafslutning** vælge **Overfør de resterende projektbudgetbeløb**.</span><span class="sxs-lookup"><span data-stu-id="6d851-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="6d851-150">I gruppen **Parametre** skal du i feltet **Projektbudgetår** vælge det regnskabsår, som du vil have vist de resterende budgetbeløb for.</span><span class="sxs-lookup"><span data-stu-id="6d851-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="6d851-151">I gruppen **Kopier fra/til** skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="6d851-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="6d851-152">I feltet **Fra prognosemodel** skal du vælge den prognosemodel for projektbudgettet, der er knyttet til de resterende budgetbeløb, som du vil overføre for projekterne.</span><span class="sxs-lookup"><span data-stu-id="6d851-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="6d851-153">Hvis du vil inkludere projekter, der opfylder de valgte kriterier, og som ikke har et resterende budget, skal du vælge **Vis ingen resterende**.</span><span class="sxs-lookup"><span data-stu-id="6d851-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="6d851-154">I gruppen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle de budgetter, der opfylder de valgte kriterier.</span><span class="sxs-lookup"><span data-stu-id="6d851-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="6d851-155">Hvis du vil designe en databaseforespørgsel, der indlæser et bestemt sæt projektbudgetter i ruden, skal du vælge **Hent valgte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="6d851-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="6d851-156">For hvert projekt, du vil behandle, skal du vælge indstillingen i starten af linjen for projektet.</span><span class="sxs-lookup"><span data-stu-id="6d851-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="6d851-157">Vælg **Behandl** for at overføre de resterende budgetbeløb for de valgte projekter til det valgte regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="6d851-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

