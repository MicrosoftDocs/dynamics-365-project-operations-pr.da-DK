---
title: Opret avancerede kontrakter for fakturering, der er baseret på status
description: I dette emne forklares det, hvordan du opretter projektkontrakter, så du kan oprette fakturaer for kunder på baggrund af en procentdel af det fuldførte arbejde.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074301"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="5747b-103">Opret avancerede kontrakter for fakturering, der er baseret på status</span><span class="sxs-lookup"><span data-stu-id="5747b-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="5747b-104">I dette emne forklares det, hvordan du opretter projektkontrakter, så du kan oprette fakturaer for kunder på baggrund af en procentdel af det fuldførte arbejde.</span><span class="sxs-lookup"><span data-stu-id="5747b-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="5747b-105">Fakturabeløb beregnes automatisk for de budgetkategorier for arbejde, som du konfigurerer for et projekt.</span><span class="sxs-lookup"><span data-stu-id="5747b-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="5747b-106">Tidspunktet for fakturering angives, når du forhandler projektkontrakten med kunden.</span><span class="sxs-lookup"><span data-stu-id="5747b-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="5747b-107">Brug procedurerne i dette emne til at oprette en kontrakt, et tilknyttet projekt og de faktureringsregler, der beregner fakturabeløb for de budgetkategorier af arbejde, som du konfigurerer for projektet.</span><span class="sxs-lookup"><span data-stu-id="5747b-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="5747b-108">Når du har oprettet kontrakten og projektet, kan du konfigurerer oplysningerne om projektet.</span><span class="sxs-lookup"><span data-stu-id="5747b-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="5747b-109">Du kan f.eks. definere aktiviteter og tildele arbejdere til projektet.</span><span class="sxs-lookup"><span data-stu-id="5747b-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="5747b-110">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5747b-110">Example</span></span>

<span data-ttu-id="5747b-111">Din organisation er et firma, som arbejder med softwareudvikling.</span><span class="sxs-lookup"><span data-stu-id="5747b-111">Your organization is a software development firm.</span></span> <span data-ttu-id="5747b-112">Du indvilliger i at udarbejde en lønningsregnskabspakke for en kunde til en samlet pris på 20.000 dollars (USD).</span><span class="sxs-lookup"><span data-stu-id="5747b-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="5747b-113">Din organisation indvilliger i at fakturere kunden, efterhånden som du færdiggør projekt på grundlag af procenter.</span><span class="sxs-lookup"><span data-stu-id="5747b-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="5747b-114">Du skal konfigurere følgende projektkategorier for arbejdet, så du kan bruge dem i faktureringsprocessen:</span><span class="sxs-lookup"><span data-stu-id="5747b-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="5747b-115">Konsulentvirksomhed</span><span class="sxs-lookup"><span data-stu-id="5747b-115">Consulting</span></span>
- <span data-ttu-id="5747b-116">Design</span><span class="sxs-lookup"><span data-stu-id="5747b-116">Design</span></span>
- <span data-ttu-id="5747b-117">Installation</span><span class="sxs-lookup"><span data-stu-id="5747b-117">Installation</span></span>

<span data-ttu-id="5747b-118">Du konfigurerer også faktureringsregler, der automatisk beregner fakturabeløbene for den procentdel af projektarbejdet, der er fuldført i de enkelte kategorier.</span><span class="sxs-lookup"><span data-stu-id="5747b-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="5747b-119">Budgetadministratoren opretter et budget for projektkategorierne.</span><span class="sxs-lookup"><span data-stu-id="5747b-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="5747b-120">Beløbet for fuldført arbejde beregnes automatisk som en procentdel af det faktiske arbejde i forhold til de budgetterede beløb.</span><span class="sxs-lookup"><span data-stu-id="5747b-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5747b-121">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="5747b-121">Prerequisites</span></span>

<span data-ttu-id="5747b-122">Før du opretter et projekt, der bruger faktureringsregler, skal du oprette nummerserierne til faktureringsregler og en gebyrkladde, der bruges til at bogføre fakturaer, efterhånden som arbejdet færdiggøres.</span><span class="sxs-lookup"><span data-stu-id="5747b-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="5747b-123">Gå til **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="5747b-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="5747b-124">På siden **Parametre for projektstyring og regnskab** skal du på fanen **Nummerserier** konfigurere den nummerserie, som du vil bruge, når der oprettes faktureringsregler.</span><span class="sxs-lookup"><span data-stu-id="5747b-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="5747b-125">Gå til **Projektstyring og regnskab** \> **Kladder** \> **Gebyr**.</span><span class="sxs-lookup"><span data-stu-id="5747b-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="5747b-126">På siden **Gebyrkladde** skal du vælge **Ny** og angive navnet på kladden.</span><span class="sxs-lookup"><span data-stu-id="5747b-126">On the **Fee journal** page, select **New** , and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="5747b-127">Opret en kontrakt for statusfaktureringer</span><span class="sxs-lookup"><span data-stu-id="5747b-127">Create a contract for progress billings</span></span>

<span data-ttu-id="5747b-128">Benyt denne fremgangsmåde til at oprette en projektkontrakt for et fastprisprojekt.</span><span class="sxs-lookup"><span data-stu-id="5747b-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="5747b-129">Du kan oprette en projektfaktura, når det arbejde, der er færdiggjort på projektet, når en bestemt procentdel.</span><span class="sxs-lookup"><span data-stu-id="5747b-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="5747b-130">Gå til **Projektstyring og regnskab** \> **Projekter** \> **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="5747b-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="5747b-131">På siden **Projektkontrakter** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5747b-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="5747b-132">I dialogboksen **Ny projektkontrakt** skal du indstille følgende felter:</span><span class="sxs-lookup"><span data-stu-id="5747b-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="5747b-133">**Navn**</span><span class="sxs-lookup"><span data-stu-id="5747b-133">**Name**</span></span>
    - <span data-ttu-id="5747b-134">**Finansieringstype**</span><span class="sxs-lookup"><span data-stu-id="5747b-134">**Funding type**</span></span>
    - <span data-ttu-id="5747b-135">**Finansieringskilde**</span><span class="sxs-lookup"><span data-stu-id="5747b-135">**Funding source**</span></span>
    - <span data-ttu-id="5747b-136">**Salgsvaluta** – Denne valuta bruges som standard til kundefakturaer, der er knyttet til projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="5747b-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="5747b-137">Du kan dog ændre salgsvalutaen på en bestemt kundefaktura.</span><span class="sxs-lookup"><span data-stu-id="5747b-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="5747b-138">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5747b-138">Select **OK**.</span></span> <span data-ttu-id="5747b-139">Oplysningerne kopieres til overskriften på siden **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="5747b-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="5747b-140">På siden **Projektkontrakter** skal du udfylde resten af de påkrævede oplysninger for projektet.</span><span class="sxs-lookup"><span data-stu-id="5747b-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="5747b-141">Opret et projekt for statusfaktureringer</span><span class="sxs-lookup"><span data-stu-id="5747b-141">Create a project for progress billings</span></span>

<span data-ttu-id="5747b-142">Benyt følgende fremgangsmåde for at oprette et projekt og eventuelle underprojekter, der er knyttet til en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="5747b-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="5747b-143">Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="5747b-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="5747b-144">På siden **Alle projekter** skal du vælge **Nyt**.</span><span class="sxs-lookup"><span data-stu-id="5747b-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="5747b-145">I dialogboksen **Nyt projekt** skal du i feltet **Projekttype** vælge **Tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="5747b-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="5747b-146">Vælg en projektgruppe.</span><span class="sxs-lookup"><span data-stu-id="5747b-146">Select a project group.</span></span> <span data-ttu-id="5747b-147">En projektgruppe definerer bogføringsoplysningerne for de projekter, der er tildelt til gruppen.</span><span class="sxs-lookup"><span data-stu-id="5747b-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="5747b-148">Vælg **Opret projekt**.</span><span class="sxs-lookup"><span data-stu-id="5747b-148">Select **Create project**.</span></span>
6. <span data-ttu-id="5747b-149">Når projektet er oprettet, skal du angive projektstadiet til **Igangværende**.</span><span class="sxs-lookup"><span data-stu-id="5747b-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="5747b-150">Opret et budget for et projekt</span><span class="sxs-lookup"><span data-stu-id="5747b-150">Create a budget for a project</span></span>

<span data-ttu-id="5747b-151">Budgetkategorier anvendes til automatisk at beregne fakturabeløbene for den procentdel af arbejdet, der er fuldført for de enkelte kategorier.</span><span class="sxs-lookup"><span data-stu-id="5747b-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="5747b-152">Følg disse trin for at oprette budgetkategorier for de estimerede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5747b-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="5747b-153">Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="5747b-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="5747b-154">På siden **Alle projekter** skal du vælge og åbne det ønskede projekt.</span><span class="sxs-lookup"><span data-stu-id="5747b-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="5747b-155">På siden **Projekter** skal du i handlingsruden på fanen **Plan** i gruppen **Budget** vælge **Projektbudget**.</span><span class="sxs-lookup"><span data-stu-id="5747b-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="5747b-156">På siden **Projektbudget** skal du angive en estimeret omkostning for hver kategori i projektet.</span><span class="sxs-lookup"><span data-stu-id="5747b-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="5747b-157">Opret faktureringsregler for statusfaktureringer</span><span class="sxs-lookup"><span data-stu-id="5747b-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="5747b-158">Gå til **Projektstyring og regnskab** \> **Projekter** \> **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="5747b-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="5747b-159">Åbn siden med listen **Projektkontrakter** , vælg og åbn en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="5747b-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="5747b-160">På siden med projektkontrakten skal du i oversigtspanelet **Faktureringsregler** vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5747b-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="5747b-161">På siden **Faktureringsregel** skal du i feltet **Linjetype** vælge **Fremgang**.</span><span class="sxs-lookup"><span data-stu-id="5747b-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="5747b-162">I oversigtspanelet **Linjedetaljer om faktureringsregel** skal du i feltet **Kontraktværdi** angive kontraktens samlede værdi.</span><span class="sxs-lookup"><span data-stu-id="5747b-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="5747b-163">I feltet **Kategori** skal du vælge den kategori, som gebyrtransaktionen skal bogføres i.</span><span class="sxs-lookup"><span data-stu-id="5747b-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="5747b-164">I feltet **Projekt** skal du vælge det projekt, der bruger denne faktureringsregel.</span><span class="sxs-lookup"><span data-stu-id="5747b-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="5747b-165">Valgfrit: Tildel faktureringsreglen til flere projekter.</span><span class="sxs-lookup"><span data-stu-id="5747b-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="5747b-166">I oversigtspanelet **Projekter** skal du i sektionen **Tilgængelige projekter** vælge et projekt og derefter vælge den højre piletast for at tilføje projektet til sektionen **Valgte projekter**.</span><span class="sxs-lookup"><span data-stu-id="5747b-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="5747b-167">Valgfrit: Beregn det procentuelle beløb, som kunden tilbageholder fra betalinger på en faktura.</span><span class="sxs-lookup"><span data-stu-id="5747b-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="5747b-168">I oversigtspanelet **Betingelser for tilbageholdelse af betaling** skal du vælge finansieringskilden og derefter i feltet **Tilbageholdelsesprocent** angive tilbageholdelsesprocenten.</span><span class="sxs-lookup"><span data-stu-id="5747b-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="5747b-169">Gentag disse trin for at oprette flere faktureringsregler for projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="5747b-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
