---
title: Opret og bekræft rettelseskladder
description: Dette emne indeholder oplysninger om, hvordan du opretter og bekræfter en rettelseskladde.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896949"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="1d92e-103">Opret og bekræft rettelseskladder</span><span class="sxs-lookup"><span data-stu-id="1d92e-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="1d92e-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="1d92e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d92e-105">Det kan ske, at en tids- eller udgiftspost registreres forkert.</span><span class="sxs-lookup"><span data-stu-id="1d92e-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="1d92e-106">En konsulent kan f.eks. vælge den forkerte dato, når han/hun opretter en tidspost, eller konsulenten kan transponere tallene, når der angives en udgift.</span><span class="sxs-lookup"><span data-stu-id="1d92e-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="1d92e-107">Hvis en konsulent ikke kan opdatere de indtastede poster, kan en administrator rette i posten for et projekt direkte.</span><span class="sxs-lookup"><span data-stu-id="1d92e-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="1d92e-108">For at fuldføre procedurerne i dette emne skal du have administratortilladelser.</span><span class="sxs-lookup"><span data-stu-id="1d92e-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="1d92e-109">Ret godkendte tidsposter</span><span class="sxs-lookup"><span data-stu-id="1d92e-109">Correct approved time entries</span></span>     

<span data-ttu-id="1d92e-110">Benyt følgende fremgangsmåde for at rette enkelte eller flere tidsangivelser for et projekt.</span><span class="sxs-lookup"><span data-stu-id="1d92e-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="1d92e-111">I området **Salg** skal du vælge **Transaktioner** og dernæst vælge **Godkendt tid**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="1d92e-112">På listen **Godkendt tid** skal du finde og vælge en eller flere af de godkendte tidsposter, der skal rettes.</span><span class="sxs-lookup"><span data-stu-id="1d92e-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="1d92e-113">Du kan bruge filteret til at finde relaterede poster.</span><span class="sxs-lookup"><span data-stu-id="1d92e-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="1d92e-114">Du kan f.eks. filtrere efter et projekt-id og vælge alle de godkendte tidsposter med det pågældende projekt-id.</span><span class="sxs-lookup"><span data-stu-id="1d92e-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="1d92e-115">Vælg **Ret poster**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-115">Select **Correct entries**.</span></span> <span data-ttu-id="1d92e-116">Der oprettes automatisk en ny rettelseskladde med den tildelte type **Tidskorrektion**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="1d92e-117">De valgte poster føjes til kladden.</span><span class="sxs-lookup"><span data-stu-id="1d92e-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="1d92e-118">På siden **Ny kladde** skal du angive en **Beskrivelse** af rettelseskladden og derefter vælge fanen **Rettelser af tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="1d92e-119">I sektionen **Nye værdier for tidsposter** skal du opdatere felterne med de korrekte oplysninger efter behov.</span><span class="sxs-lookup"><span data-stu-id="1d92e-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="1d92e-120">Du kan f.eks. ændre det tildelte projekt eller den reserverbare ressource.</span><span class="sxs-lookup"><span data-stu-id="1d92e-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="1d92e-121">Vælg **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-121">Select **Preview**.</span></span> <span data-ttu-id="1d92e-122">Vælg **OK** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="1d92e-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="1d92e-123">Under fanen **Kladdelinjer** kan du få vist en liste over de oprindelige faktiske værdier, der er relateret til de valgte tidsposter, som er blevet tilbageført, samt de tilsvarende ændrede linjer, der er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="1d92e-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="1d92e-124">Hvis der skal foretages yderligere rettelser, skal du gentage trin 5 og 6.</span><span class="sxs-lookup"><span data-stu-id="1d92e-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="1d92e-125">Alle de korrigerede faktiske værdier får de samme værdier, som du har valgt i sektionen **Nye værdier for tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="1d92e-126">Hvis rettelserne vises som forventet, skal du vælge **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="1d92e-127">Vælg **OK** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="1d92e-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="1d92e-128">Gå tilbage til området **Salg**, og vælg **Projekter**, og åbn derefter det projekt, som du lige har opdateret tidsposterne for.</span><span class="sxs-lookup"><span data-stu-id="1d92e-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="1d92e-129">På siden **Projekter** kan du under fanen **Faktiske værdier** få vist de ændringer, du har foretaget.</span><span class="sxs-lookup"><span data-stu-id="1d92e-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="1d92e-130">Hvis fanen **Faktiske værdier** ikke er synlig, skal du vælge **Relaterede** > **Faktiske værdier**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="1d92e-131">På listen **Visning af faktisk tilknytning** kan du se, at de oprindelige tidsposter, der er blevet tilbageført, stadig findes på listen, hvilket også er tilfældet for de tilsvarende rettede tidsposter.</span><span class="sxs-lookup"><span data-stu-id="1d92e-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="1d92e-132">I følgende illustration er der f.eks. to linjeelementer med et antal på 8,00, som har angivet debiteringer i kolonnen "Beløb".</span><span class="sxs-lookup"><span data-stu-id="1d92e-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="1d92e-133">Derudover er der to linjeelementer med et antal på -8,00, som viser de krediterede beløb i kolonnen "Beløb".</span><span class="sxs-lookup"><span data-stu-id="1d92e-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="1d92e-134">De rettelser ændrer mængden til nul.</span><span class="sxs-lookup"><span data-stu-id="1d92e-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="1d92e-135">Ret godkendte udgiftsposter</span><span class="sxs-lookup"><span data-stu-id="1d92e-135">Correct approved expense entries</span></span>

<span data-ttu-id="1d92e-136">Benyt følgende fremgangsmåde for at rette en eller flere udgiftsposter.</span><span class="sxs-lookup"><span data-stu-id="1d92e-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="1d92e-137">I området **Salg** skal du under **Transaktioner** i venstre navigationsrude vælge **Godkendte udgifter**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="1d92e-138">På listen **Godkendte udgifter** skal du vælge det projekt, som du ønsker at rette, og dernæst vælge **Ret poster**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="1d92e-139">Der oprettes automatisk en ny rettelseskladde med den tildelte type **Udgiftsrettelse**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="1d92e-140">På siden **Ny kladde** skal du angive en **Beskrivelse** for rettelsen, og på fanen **Udgiftsrettelse** i sektionen **Nye værdier for udgifter** skal du vælge de datafelter, som du ønsker at rette for de valgte udgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="1d92e-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="1d92e-141">Du kan f.eks. tildele udgiften til et andet **Projekt** eller rette **Udgiftskategorien**, **Udgiftsdatoen** eller den **Reserverbare ressource**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="1d92e-142">Vælg **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-142">Select **Preview**.</span></span> <span data-ttu-id="1d92e-143">Vælg **OK** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="1d92e-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="1d92e-144">Verificer rettelserne på fanen **Kladdelinjer**. Du kan få vist en liste over de oprindelige faktiske værdier, der er relateret til de valgte udgiftsposter, som er blevet tilbageført, samt de tilsvarende ændrede linjer, der er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="1d92e-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="1d92e-145">Hvis de rettede værdier er som forventede, skal du vælge **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="1d92e-146">Vælg **OK** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="1d92e-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="1d92e-147">Hvis værdierne ikke vises som forventet, skal du vælge **Annuller** for at vende tilbage til listen med **Godkendte udgifter**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="1d92e-148">Gentag trin 2-5.</span><span class="sxs-lookup"><span data-stu-id="1d92e-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="1d92e-149">De korrigerede faktiske værdier får de samme værdier, som du har valgt i sektionen **Nye værdier for udgifter**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="1d92e-150">Når du har bekræftet rettelsesjournalen, skal du gå tilbage til det projekt eller de projekter, du har opdateret, for at få vist ændringerne.</span><span class="sxs-lookup"><span data-stu-id="1d92e-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="1d92e-151">På projektsiden skal du under fanen **Faktiske værdier** gennemse **Oversigt over faktiske tilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="1d92e-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="1d92e-152">De oprindelige poster og de rettede poster vises på listen.</span><span class="sxs-lookup"><span data-stu-id="1d92e-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="1d92e-153">I følgende illustration vises de oprindelige beløb for udgiftsposter og de tilsvarende korrigerede udgiftsposter.</span><span class="sxs-lookup"><span data-stu-id="1d92e-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


