---
title: Behandling af udgiftskvittering
description: Dette emne indeholder oplysninger om behandling af kvitteringer ved hjælp af optisk tegngenkendelse (OCR). Denne funktion er udviklet til at forbedre brugeroplevelsen ved oprettelse af udgiftsrapporter i Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993499"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="6934a-104">Behandling af udgiftskvittering</span><span class="sxs-lookup"><span data-stu-id="6934a-104">Expense receipt processing</span></span>

<span data-ttu-id="6934a-105">Udgiftsposten er blevet forbedret via introduktionen af behandling af kvitteringer ved hjælp af optisk tegngenkendelse (OCR).</span><span class="sxs-lookup"><span data-stu-id="6934a-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="6934a-106">Denne funktion er udviklet til at forbedre brugeroplevelsen ved oprettelse af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="6934a-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="6934a-107">Nøglefunktioner</span><span class="sxs-lookup"><span data-stu-id="6934a-107">Key features</span></span>

- <span data-ttu-id="6934a-108">Forhandlernavnet, datoen og det samlede beløb udtrækkes fra kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="6934a-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="6934a-109">Denne funktion forsøger at sammenholde ikke-tilknyttede kvitteringer med ikke-tilknyttede udgiftstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6934a-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="6934a-110">Brugere kan oprette manuelt indtastede udgiftstransaktioner på grundlag af kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="6934a-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="6934a-111">Eksempler på brug</span><span class="sxs-lookup"><span data-stu-id="6934a-111">Usage examples</span></span>

<span data-ttu-id="6934a-112">Hvis du automatisk vil vedhæfte kvitteringer, der omfatter kreditkorttransaktioner, når en udgiftsrapport oprettes, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="6934a-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="6934a-113">Åbn arbejdsområdet **Udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="6934a-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="6934a-114">På fanen **Kvitteringer** skal du kontrollere, at der findes ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="6934a-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="6934a-115">Du kan også overføre kvitteringer under fanen **Kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="6934a-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="6934a-116">På fanen **Udgifter** skal du kontrollere, at der findes ikke-tilknyttede udgifter.</span><span class="sxs-lookup"><span data-stu-id="6934a-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="6934a-117">Udgiftsadministratoren importerer typisk disse udgifter fra kreditkortudbyderen.</span><span class="sxs-lookup"><span data-stu-id="6934a-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="6934a-118">Vælg **Ny udgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="6934a-118">Select **New expense report**.</span></span> <span data-ttu-id="6934a-119">Bemærk, at du nu også kan inkludere udgifter og kvitteringer, når du opretter en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="6934a-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="6934a-120">Hvis du tilføjer både udgifter og kvitteringer, udløses automatisk afstemning af kvitteringer i forhold til udgifterne.</span><span class="sxs-lookup"><span data-stu-id="6934a-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="6934a-121">Hvis du vil oprette en udgift eller afstemme en udgift fra en kvittering, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="6934a-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="6934a-122">På en udgiftsrapport skal du på fanen **Kvitteringer** tilknytte en kvittering ved at vælge **Tilføj kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="6934a-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="6934a-123">Læg mærke til indstillingerne **Opret** og **Afstem** under det overførte billede af kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="6934a-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="6934a-124">Vælg **Opret** for at oprette en manuelt angivet udgiftstransaktioner, og angiv de værdier, der er udtrukket fra kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="6934a-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="6934a-125">Hvis du vælger **Afstem**, vil systemet forsøge at afstemme en eksisterende udgift med kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="6934a-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="6934a-126">Installation</span><span class="sxs-lookup"><span data-stu-id="6934a-126">Installation</span></span>

<span data-ttu-id="6934a-127">Denne funktion fungerer sammen med funktionen for **Nye udgiftsrapporter**, som hjælper med at forenkle udgiftsoplevelsen.</span><span class="sxs-lookup"><span data-stu-id="6934a-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="6934a-128">Denne funktion er kun tilgængelig for miljøer over niveau 2, hvilke er sandkasse- og produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="6934a-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="6934a-129">Hvis du vil bruge disse avancerede udgiftsfunktioner, skal du installere tilføjelsesprogrammet til tjenesten for udgiftsstyring i Microsoft Dynamics 365 Finance og aktivere funktionerne i din forekomst.</span><span class="sxs-lookup"><span data-stu-id="6934a-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="6934a-130">Du kan få adgang til tilføjelsesprogrammet fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6934a-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="6934a-131">Log på LCS, og åbn det ønskede miljø.</span><span class="sxs-lookup"><span data-stu-id="6934a-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="6934a-132">Gå til **Komplette detaljer**.</span><span class="sxs-lookup"><span data-stu-id="6934a-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="6934a-133">Vælg **Bevar** eller rul ned til oversigtspanelet **Tilføjelsesprogrammer i miljøet**.</span><span class="sxs-lookup"><span data-stu-id="6934a-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="6934a-134">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="6934a-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="6934a-135">Vælg **Tjeneste til udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="6934a-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="6934a-136">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="6934a-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="6934a-137">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="6934a-137">Select **Install**.</span></span>

<span data-ttu-id="6934a-138">I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="6934a-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="6934a-139">Nye udgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="6934a-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="6934a-140">Automatisk afstemning og opret udgift fra kvittering</span><span class="sxs-lookup"><span data-stu-id="6934a-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="6934a-141">Når du aktiverer disse funktioner, udføres følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="6934a-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="6934a-142">Det eksisterende arbejdsområde for **Udgiftsstyring** erstattes med det nye arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="6934a-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="6934a-143">Der tilføjes et nyt menupunkt for synligheden af udgiftsfeltet.</span><span class="sxs-lookup"><span data-stu-id="6934a-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="6934a-144">Du kan stadig åbne den tidligere side med **Udgiftsrapport** ved at gå til **Udgiftsstyring > Mine udgifter > Udgiftsrapporter**.</span><span class="sxs-lookup"><span data-stu-id="6934a-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="6934a-145">Arbejdsprocesser og eventuelle godkendelser fører dig stadig til siden med den eksisterende udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="6934a-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="6934a-146">Kvitteringer vil blive behandlet via Microsoft Azure Cognitive Services, og metadata udtrækkes og tilføjes.</span><span class="sxs-lookup"><span data-stu-id="6934a-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="6934a-147">Der tilføjes en indstilling, som giver dig mulighed for at oprette en udgiftsrapport, der indeholder afstemte ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="6934a-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="6934a-148">En indstilling, der tilføjes til udgiftsrapporter, giver dig mulighed for at oprette en udgiftslinje på grundlag af en kvittering eller forsøger at afstemme en eksisterende kvittering med en eksisterende udgiftslinje.</span><span class="sxs-lookup"><span data-stu-id="6934a-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="6934a-149">Du kan finde flere oplysninger om funktionen for nye udgiftsrapporter under [Nye udgiftsrapporter](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="6934a-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6934a-150">Ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="6934a-150">Frequently asked questions</span></span>

<span data-ttu-id="6934a-151">**Bruger Microsoft mine data til sine modeller?**</span><span class="sxs-lookup"><span data-stu-id="6934a-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="6934a-152">Nej, Microsoft har udviklet en generel maskinel indlæringsmodel til sin tjeneste for behandling af kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="6934a-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="6934a-153">Denne model er ikke baseret på de kvitteringer, du overfører.</span><span class="sxs-lookup"><span data-stu-id="6934a-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="6934a-154">**Hvor er denne funktion tilgængelig og behandlet?**</span><span class="sxs-lookup"><span data-stu-id="6934a-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="6934a-155">USA understøttes i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="6934a-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="6934a-156">**Hvor forsvinder mine kvitteringer hen?**</span><span class="sxs-lookup"><span data-stu-id="6934a-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="6934a-157">Finance kontakter Cognitive Services for at udtrække feltdataene.</span><span class="sxs-lookup"><span data-stu-id="6934a-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="6934a-158">Cognitive Services opbevarer en kopi af din kvittering i op til 24 timer, mens behandlingen pågår.</span><span class="sxs-lookup"><span data-stu-id="6934a-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="6934a-159">Når behandlingen er fuldført, fjerner Cognitive Services kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="6934a-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="6934a-160">Kvitteringer gemmes stadig i Finance.</span><span class="sxs-lookup"><span data-stu-id="6934a-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="6934a-161">Du kan finde flere oplysninger under [Aktiver forståelse af kvitteringer med Form Recognizers nye funktion](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="6934a-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]