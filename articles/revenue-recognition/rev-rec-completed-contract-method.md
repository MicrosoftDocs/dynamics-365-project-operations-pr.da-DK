---
title: Administrer omsætningsestimater
description: Dette emne indeholder oplysninger om, hvordan du arbejder med omsætningsestimater for projekter.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531393"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="db19c-103">Administrer omsætningsestimater</span><span class="sxs-lookup"><span data-stu-id="db19c-103">Manage revenue estimates</span></span>

<span data-ttu-id="db19c-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="db19c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="db19c-105">Du kan oprette, beregne, bogføre, tilbageføre eller eliminere omsætningsestimater.</span><span class="sxs-lookup"><span data-stu-id="db19c-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="db19c-106">Du kan gøre dette enten manuelt eller ved hjælp af en periodisk proces.</span><span class="sxs-lookup"><span data-stu-id="db19c-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="db19c-107">Dette emne indeholder oplysninger om, hvordan du arbejder med omsætningsestimater for projekter.</span><span class="sxs-lookup"><span data-stu-id="db19c-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="db19c-108">Administrer omsætningsestimater manuelt</span><span class="sxs-lookup"><span data-stu-id="db19c-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="db19c-109">På projektet med omsætningsestimat for fast pris eller siden **Estimer forespørgsel** (**Projektstyring og regnskab** > **Rapporter og forespørgsler** > **Estimatforespørgsler og rapporter**) skal du vælge **Estimater**.</span><span class="sxs-lookup"><span data-stu-id="db19c-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="db19c-110">Administrer omsætningsestimater ved hjælp af en periodisk proces</span><span class="sxs-lookup"><span data-stu-id="db19c-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="db19c-111">Gå til **Projektstyring og regnskab** > **Periodisk** > **Estimater**, og vælg den tilsvarende proces.</span><span class="sxs-lookup"><span data-stu-id="db19c-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="db19c-112">Opret et omsætningsestimat</span><span class="sxs-lookup"><span data-stu-id="db19c-112">Create a revenue estimate</span></span>

<span data-ttu-id="db19c-113">Fuldfør følgende fremgangsmåde for at oprette et omsætningsestimat.</span><span class="sxs-lookup"><span data-stu-id="db19c-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="db19c-114">Gå til **Projektstyring og regnskab** > **Periodisk** > **Estimater**.</span><span class="sxs-lookup"><span data-stu-id="db19c-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="db19c-115">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="db19c-115">Select **New**.</span></span> <span data-ttu-id="db19c-116">Vælg følgende parametre på siden **Estimatoprettelse**:</span><span class="sxs-lookup"><span data-stu-id="db19c-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="db19c-117">**Periodekode**: Denne kode bestemmer, hvor ofte estimater bogføres.</span><span class="sxs-lookup"><span data-stu-id="db19c-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="db19c-118">**Estimatdato**: Den dato, hvor estimatet behandles.</span><span class="sxs-lookup"><span data-stu-id="db19c-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="db19c-119">**Fortløbende**: Markér dette afkrydsningsfelt for kun at oprette estimater, hvis der er bogført estimater i den forrige periode, eller hvis estimatet er det første estimat, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="db19c-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="db19c-120">Hvis dette ikke er valgt, oprettes der estimater, selvom der ikke er bogført estimater i den forrige periode.</span><span class="sxs-lookup"><span data-stu-id="db19c-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="db19c-121">**Metode til færdiggørelsesomkostninger**: Definer, hvordan det resterende projektarbejde skal estimeres.</span><span class="sxs-lookup"><span data-stu-id="db19c-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="db19c-122">Yderligere oplysninger finder du i [Metoder til færdiggørelsesomkostninger](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="db19c-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="db19c-123">**Færdiggørelsesmetode**: Vælg en færdiggørelsesmetode ud fra følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="db19c-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="db19c-124">**Automatisk**: Færdiggørelsesprocenten beregnes automatisk og på grundlag af de omkostningslinjer, der er inkluderet i beregningen.</span><span class="sxs-lookup"><span data-stu-id="db19c-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="db19c-125">Omkostningsskabelonen definerer de omkostningslinjer, der er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="db19c-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="db19c-126">**Manuel**  Færdiggørelsesprocenten er lig med færdiggørelsesprocenten for det sidste estimat.</span><span class="sxs-lookup"><span data-stu-id="db19c-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="db19c-127">Når estimatet er oprettet, kan du ændre **Manuel beregning** på siden **Estimater**.</span><span class="sxs-lookup"><span data-stu-id="db19c-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="db19c-128">**Fra omkostningsskabelon**: En kombination af de automatiske og manuelle metoder.</span><span class="sxs-lookup"><span data-stu-id="db19c-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="db19c-129">Denne indstilling angives automatisk eller manuelt, afhængigt af standardværdien i omkostningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="db19c-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="db19c-130">**Prognosemodel**: Vælg en prognosemodel for estimatet.</span><span class="sxs-lookup"><span data-stu-id="db19c-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="db19c-131">**Udskriv estimatliste**: Opret og vis en estimatliste.</span><span class="sxs-lookup"><span data-stu-id="db19c-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="db19c-132">Listen indeholder statussen for den aktuelle funktion.</span><span class="sxs-lookup"><span data-stu-id="db19c-132">The list contains the status of the current function.</span></span> <span data-ttu-id="db19c-133">Du kan udskrive eventuelle advarsler om estimatet i rapporten.</span><span class="sxs-lookup"><span data-stu-id="db19c-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="db19c-134">Følgende betingelser medfører, at advarsler vises på estimatlisten:</span><span class="sxs-lookup"><span data-stu-id="db19c-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="db19c-135">En færdiggørelsesprocent på mere end 100 procent.</span><span class="sxs-lookup"><span data-stu-id="db19c-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="db19c-136">En færdiggørelsesprocent på mindre end 0 procent.</span><span class="sxs-lookup"><span data-stu-id="db19c-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="db19c-137">Et negativt beløb i kolonnen **Skal færdiggøres**.</span><span class="sxs-lookup"><span data-stu-id="db19c-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="db19c-138">Et estimat uden tilsvarende kontraktbeløb.</span><span class="sxs-lookup"><span data-stu-id="db19c-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="db19c-139">Et estimat uden vedhæftet omkostningsestimat.</span><span class="sxs-lookup"><span data-stu-id="db19c-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="db19c-140">**Vis infolog**: Vælg denne indstilling for at modtage en meddelelse, der indeholder oplysninger om de estimerede projekter, der blev behandlet, da jobbet blev kørt.</span><span class="sxs-lookup"><span data-stu-id="db19c-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="db19c-141">Bogfør IGVA eller periodiseringer</span><span class="sxs-lookup"><span data-stu-id="db19c-141">Post WIP or accruals</span></span>

<span data-ttu-id="db19c-142">Når estimaterne er evalueret, vedligeholdes, formindskes eller forhøjes de.</span><span class="sxs-lookup"><span data-stu-id="db19c-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="db19c-143">Du kan derefter bogføre IGVA, når du arbejder med vurderingsprincippet **Færdiggjort kontrakt** eller bogføre periodiseringerne, når du arbejder med vurderingsprincippet **Procent for færdiggørelse**.</span><span class="sxs-lookup"><span data-stu-id="db19c-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="db19c-144">Status for estimatperioden ændres fra **Oprettet** til **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="db19c-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="db19c-145">Tilbagefør IGVA eller periodiseringer</span><span class="sxs-lookup"><span data-stu-id="db19c-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="db19c-146">Brug tilbageførelsesindstillingen til at kreditere allerede bogførte IGVA eller periodiseringer, og opret derefter estimater for perioden.</span><span class="sxs-lookup"><span data-stu-id="db19c-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="db19c-147">Hvis du vil tilbageføre en periode, der ligger inden for andre perioder, skal du tilbageføre de nødvendige estimatperioder og derefter bogføre dem igen.</span><span class="sxs-lookup"><span data-stu-id="db19c-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="db19c-148">Da alle efterfølgende perioder er afhængige af estimaterne fra den foregående periode, skal du ikke springe nogle af perioderne over.</span><span class="sxs-lookup"><span data-stu-id="db19c-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="db19c-149">Eliminer det estimerede projekt, og afslut projektet</span><span class="sxs-lookup"><span data-stu-id="db19c-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="db19c-150">Det sidste trin i estimeringsprocessen er at fjerne det estimerede projekt og afslutte projektet med fast pris, når den procentvise færdiggørelse når 100 procent.</span><span class="sxs-lookup"><span data-stu-id="db19c-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="db19c-151">Der sker følgende, når du kører eliminering:</span><span class="sxs-lookup"><span data-stu-id="db19c-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="db19c-152">For et fastprisprojekt med en færdiggjort kontrakt, ryddes IGVA-værdierne fra saldokontiene og bogføres til driftskonti.</span><span class="sxs-lookup"><span data-stu-id="db19c-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="db19c-153">For et fastprisprojekt, der har en færdiggørelsesprocent, fjernes periodiseringerne fra driftskontiene.</span><span class="sxs-lookup"><span data-stu-id="db19c-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="db19c-154">I estimatetet ændres statussen til **Elimineret**.</span><span class="sxs-lookup"><span data-stu-id="db19c-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="db19c-155">I særlige tilfælde kan procentsatsen stige til mere end 100 procent.</span><span class="sxs-lookup"><span data-stu-id="db19c-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="db19c-156">Når dette sker, skal du reducere færdiggørelsesprocenten ved hjælp af **Metoden til angivelse af omkostninger til færdiggørelse til nul** for at få nå 100 procent.</span><span class="sxs-lookup"><span data-stu-id="db19c-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="db19c-157">Tilbagefør eliminering</span><span class="sxs-lookup"><span data-stu-id="db19c-157">Reverse elimination</span></span>

1. <span data-ttu-id="db19c-158">Gå til **Projektstyring og regnskab** > **Periodisk** > **Estimater** > **Tilbagefør eliminering**.</span><span class="sxs-lookup"><span data-stu-id="db19c-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="db19c-159">I handlingsruden skal du på fanen **Behandling** i gruppen **Bevar** vælge **Estimat**.</span><span class="sxs-lookup"><span data-stu-id="db19c-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="db19c-160">Vælg **Tilbagefør eliminering**.</span><span class="sxs-lookup"><span data-stu-id="db19c-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="db19c-161">Brug denne side til at tilbageføre alle elimineringer med en bestemt estimatdato og med estimatstatussen **Elimineret**.</span><span class="sxs-lookup"><span data-stu-id="db19c-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="db19c-162">Transaktionsstatussen ændres, når du har valgt de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="db19c-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="db19c-163">Derved ændres projektstatus også automatisk til **Igangværende**, hvis projektstadiet er angivet til afsluttet.</span><span class="sxs-lookup"><span data-stu-id="db19c-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="db19c-164">Estimatstatus for projektperioden ændres tilbage til **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="db19c-164">The estimate status of the project period changes back to **Posted**.</span></span>
