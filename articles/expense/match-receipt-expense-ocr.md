---
title: Afstem en kvittering med en udgift ved hjælp af optisk tegngenkendelse
description: Dette emne indeholder oplysninger om behandling af kvitteringer ved hjælp af optisk tegngenkendelse (OCR).
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124316"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="90e2f-103">Afstem en kvittering med en udgift ved hjælp af optisk tegngenkendelse</span><span class="sxs-lookup"><span data-stu-id="90e2f-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="90e2f-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="90e2f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="90e2f-105">Udgiftsposten er blevet forbedret via introduktionen af behandling af kvitteringer ved hjælp af optisk tegngenkendelse (OCR).</span><span class="sxs-lookup"><span data-stu-id="90e2f-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="90e2f-106">Denne funktionalitet er udviklet til at forbedre brugeroplevelsen ved oprettelse af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="90e2f-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="90e2f-107">Nøglefunktioner</span><span class="sxs-lookup"><span data-stu-id="90e2f-107">Key features</span></span>

- <span data-ttu-id="90e2f-108">I systemet udtrækkes forhandlernavnet, datoen og det samlede beløb fra kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="90e2f-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="90e2f-109">Systemet forsøger at sammenligne ikke-tilknyttede kvitteringer med ikke-tilknyttede udgiftstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="90e2f-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="90e2f-110">Du kan oprette manuelt indtastede udgiftstransaktioner på grundlag af kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="90e2f-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="90e2f-111">Vedhæft kvitteringer til en udgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="90e2f-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="90e2f-112">Hvis du automatisk vil vedhæfte kvitteringer, der omfatter kreditkorttransaktioner, når en udgiftsrapport oprettes, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="90e2f-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="90e2f-113">Åbn arbejdsområdet **Udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="90e2f-114">På fanen **Kvitteringer** skal du kontrollere, at der findes ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="90e2f-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="90e2f-115">Du kan også overføre kvitteringer under fanen **Kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="90e2f-116">På fanen **Udgifter** skal du kontrollere, at der findes ikke-tilknyttede udgifter.</span><span class="sxs-lookup"><span data-stu-id="90e2f-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="90e2f-117">Udgiftsadministratoren importerer typisk disse udgifter fra kreditkortudbyderen.</span><span class="sxs-lookup"><span data-stu-id="90e2f-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="90e2f-118">Vælg **Ny udgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-118">Select **New expense report**.</span></span> <span data-ttu-id="90e2f-119">Bemærk, at du nu også kan inkludere udgifter og kvitteringer, når du opretter en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="90e2f-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="90e2f-120">Hvis du tilføjer både udgifter og kvitteringer, udløses automatisk afstemning af kvitteringer i forhold til udgifterne.</span><span class="sxs-lookup"><span data-stu-id="90e2f-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="90e2f-121">Opret eller afstem kvitteringer til en udgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="90e2f-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="90e2f-122">Hvis du vil oprette en udgift eller afstemme en udgift fra en kvittering, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="90e2f-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="90e2f-123">På en udgiftsrapport skal du på fanen **Kvitteringer** tilknytte en kvittering ved at vælge **Tilføj kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="90e2f-124">Læg mærke til indstillingerne **Opret** og **Afstem** under det overførte billede af kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="90e2f-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="90e2f-125">Vælg **Opret** for at oprette en manuelt angivet udgiftstransaktioner, og angiv de værdier, der er udtrukket fra kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="90e2f-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="90e2f-126">Hvis du vælger **Afstem**, vil systemet forsøge at afstemme en eksisterende udgift med kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="90e2f-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="90e2f-127">Installation</span><span class="sxs-lookup"><span data-stu-id="90e2f-127">Installation</span></span>

<span data-ttu-id="90e2f-128">Hvis du vil bruge disse avancerede udgiftsfunktioner, skal du installere tilføjelsesprogrammet til tjenesten for udgiftsstyring i Microsoft Dynamics 365 Finance og aktivere funktionerne i din forekomst.</span><span class="sxs-lookup"><span data-stu-id="90e2f-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="90e2f-129">Du kan få adgang til tilføjelsesprogrammet fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="90e2f-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="90e2f-130">Log på LCS, og åbn det ønskede miljø.</span><span class="sxs-lookup"><span data-stu-id="90e2f-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="90e2f-131">Gå til **Komplette detaljer**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="90e2f-132">Vælg **Bevar** eller rul ned til oversigtspanelet **Tilføjelsesprogrammer i miljøet**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="90e2f-133">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="90e2f-134">Vælg **Tjeneste til udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="90e2f-135">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="90e2f-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="90e2f-136">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-136">Select **Install**.</span></span>

<span data-ttu-id="90e2f-137">I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="90e2f-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="90e2f-138">Nye udgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="90e2f-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="90e2f-139">Automatisk afstemning og opret udgift fra kvittering</span><span class="sxs-lookup"><span data-stu-id="90e2f-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="90e2f-140">Når du aktiverer disse funktioner, udføres følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="90e2f-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="90e2f-141">Det eksisterende arbejdsområde for **Udgiftsstyring** erstattes med det nye arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="90e2f-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="90e2f-142">Der tilføjes et nyt menupunkt for synligheden af udgiftsfeltet.</span><span class="sxs-lookup"><span data-stu-id="90e2f-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="90e2f-143">Du kan stadig åbne den tidligere side med **Udgiftsrapport** ved at gå til **Udgiftsstyring > Mine udgifter > Udgiftsrapporter**.</span><span class="sxs-lookup"><span data-stu-id="90e2f-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="90e2f-144">Arbejdsprocesser og eventuelle godkendelser fører dig stadig til siden med den eksisterende udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="90e2f-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="90e2f-145">Kvitteringer vil blive behandlet via Microsoft Azure Cognitive Services, og metadata udtrækkes og tilføjes.</span><span class="sxs-lookup"><span data-stu-id="90e2f-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="90e2f-146">Der tilføjes en indstilling, som giver dig mulighed for at oprette en udgiftsrapport, der indeholder afstemte ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="90e2f-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="90e2f-147">En indstilling, der tilføjes til udgiftsrapporter, giver dig mulighed for at oprette en udgiftslinje på grundlag af en kvittering eller forsøger at afstemme en eksisterende kvittering med en eksisterende udgiftslinje.</span><span class="sxs-lookup"><span data-stu-id="90e2f-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="90e2f-148">Ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="90e2f-148">Frequently asked questions</span></span>

<span data-ttu-id="90e2f-149">**Bruger Microsoft mine data til sine modeller?**</span><span class="sxs-lookup"><span data-stu-id="90e2f-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="90e2f-150">Nej, Microsoft har udviklet en generel maskinel indlæringsmodel til sin tjeneste for behandling af kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="90e2f-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="90e2f-151">Denne model er ikke baseret på de kvitteringer, du overfører.</span><span class="sxs-lookup"><span data-stu-id="90e2f-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="90e2f-152">**Hvor er denne funktion tilgængelig og behandlet?**</span><span class="sxs-lookup"><span data-stu-id="90e2f-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="90e2f-153">USA understøttes i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="90e2f-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="90e2f-154">**Hvor forsvinder mine kvitteringer hen?**</span><span class="sxs-lookup"><span data-stu-id="90e2f-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="90e2f-155">Finance kontakter Cognitive Services for at udtrække feltdataene.</span><span class="sxs-lookup"><span data-stu-id="90e2f-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="90e2f-156">Cognitive Services opbevarer en kopi af din kvittering i op til 24 timer, mens behandlingen pågår.</span><span class="sxs-lookup"><span data-stu-id="90e2f-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="90e2f-157">Når behandlingen er fuldført, fjerner Cognitive Services kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="90e2f-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="90e2f-158">Kvitteringer gemmes stadig i Finance.</span><span class="sxs-lookup"><span data-stu-id="90e2f-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="90e2f-159">Du kan finde flere oplysninger under [Aktiver forståelse af kvitteringer med Form Recognizers nye funktion](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="90e2f-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
