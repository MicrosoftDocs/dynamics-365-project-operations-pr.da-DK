---
title: Forespørgsel om plan for udgifter til føderale priser
description: Dette emne indeholder oplysninger om forespørgsel om planen for udgifter til føderale priser.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074156"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4d6e7-103">Forespørgsel om plan for udgifter til føderale priser</span><span class="sxs-lookup"><span data-stu-id="4d6e7-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d6e7-104">Ifølge cirkulære A-133 fra Office of Management and Budget (kontoret for styring og kontrol) er de agenturer, der modtager føderale midler, underlagt overvågningskrav, også kaldet enkelte overvågninger.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="4d6e7-105">Overvågningsprocessen anvendes til at rapportere om indtægter og udgifter for føderale tilskud på et tilbagevendende grundlag.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="4d6e7-106">En del af den enkelte overvågningsrapport omfatter planen for udgifter til føderale priser (SEFA).</span><span class="sxs-lookup"><span data-stu-id="4d6e7-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="4d6e7-107">Forespørgsel om planen for udgifter til føderale priser omfatter kataloget over titlen og nummeret på Federal Domestic Assistance (CFDA), tilskudsnummer, tilskudsåret, navnet på det føderale agentur, der stiller midlerne til rådighed, samt navnet på pass-through-objektet.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="4d6e7-108">Forespørgslen gælder for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="4d6e7-109">Denne periode er som regel den samme som regnskabsperioden, som er et regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="4d6e7-110">Forespørgslen inkluderer de tilskud, der har projektionsdatoer i det valgte datointerval.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="4d6e7-111">I kolonnen **Tilskudsgivende agentur** i forespørgslen vises tilskudskunden eller, for et pass-through-tilskud, det tilskudsgivende agentur.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="4d6e7-112">I forbindelse med pass-through-tilskud viser kolonnen **Pass-through-agentur** tilskudskunden.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="4d6e7-113">Hvis tilskuddet ikke er et pass-through-tilskud, er kolonnen **Pass-through-agentur** tom.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="4d6e7-114">Konfigurer CFDA-klyngerne</span><span class="sxs-lookup"><span data-stu-id="4d6e7-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="4d6e7-115">Du skal konfigurere CFDA-klyngerne, der kan knyttes til CFDA-numre i forespørgsel om planen for udgifter til føderale priser.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="4d6e7-116">Gå til **Projektstyring og regnskab \> Opsætning \> Tilskud \> Katalog over klynger af Federal Domestic Assistance**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="4d6e7-117">Vælg **Ny** for at oprette en CFDA-klynge.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="4d6e7-118">Angiv klyngens navn.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="4d6e7-119">Vælg **Gem** for at gemme dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="4d6e7-120">Konfigurer CFDA-numre</span><span class="sxs-lookup"><span data-stu-id="4d6e7-120">Set up CFDA numbers</span></span>

<span data-ttu-id="4d6e7-121">Du skal konfigurere CFDA-numre, der kan tilføjes til tilskud og medtages i forespørgsel om planen for udgifter til føderale priser.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="4d6e7-122">Gå til **Projektstyring og regnskab \> Opsætning \> Tilskud \> Katalog over numre til Federal Domestic Assistance**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="4d6e7-123">Vælg **Ny** for at oprette et CFDA-nummer.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="4d6e7-124">Angiv CFDA-nummeret i kolonnen **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="4d6e7-125">Tryk på tasten **Tab**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="4d6e7-126">Angiv CFDA-titlen i kolonnen **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="4d6e7-127">Tryk på tasten **Tab**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="4d6e7-128">Valgfrit: I feltet **Programklynge** kan du tilføje den relevante CFDA-klynge.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="4d6e7-129">Vælg **Gem** for at gemme dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4d6e7-130">Konfigurer tilskud, der skal rapporteres i forespørgsel om planen for udgifter til føderale priser</span><span class="sxs-lookup"><span data-stu-id="4d6e7-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="4d6e7-131">Gå til **Projektstyring og regnskab \> Tilskud \> Tilskud** , og vælg et eksisterende tilskud.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="4d6e7-132">I oversigtspanelet **Opsætning** skal du i feltet **Katalog over Federal Domestic Assistance** tildele CFDA-nummeret.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="4d6e7-133">CFDA-nummeret på tilskuddet bestemmer CFDA-klyngen med henblik på rapportering.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="4d6e7-134">I oversigtspanelet **Kontaktoplysninger** skal du angive oplysningerne på tilskudsgiver ved at benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="4d6e7-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="4d6e7-135">I feltet **Tilskudskunde** skal du angive den kunde, der er ansvarlig for tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="4d6e7-136">For et eksisterende tilskud er disse oplysninger muligvis allerede angivet.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="4d6e7-137">Angiv, om tilskudskunden er stifteren.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="4d6e7-138">Hvis tilskudskunden er stifteren, skal du fjerne markeringen i afkrydsningsfeltet **Pass-through**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="4d6e7-139">Hvis en anden kunde er stifteren, og tilskudskunden er ansvarlig for forbrug og sporing af pengene, skal du markere afkrydsningsfeltet **Pass-through**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="4d6e7-140">Hvis du har markeret afkrydsningsfeltet **Pass-through** i forrige trin, skal du i feltet **Tilskudsgivende agentur** angive den kunde, der har ydet tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="4d6e7-141">Det tilskudsgivende agentur og tilskudskunden må ikke være den samme kunde.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="4d6e7-142">Her er et eksempel på et pass-through-tilskud:</span><span class="sxs-lookup"><span data-stu-id="4d6e7-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="4d6e7-143">De føderale offentlige myndigheder finansierede et infrastrukturprojekt for en stat.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="4d6e7-144">De føderale offentlige myndigheder gav penge til staten, som den kunne bruge.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="4d6e7-145">I dette tilfælde er de føderale offentlige myndigheder det tilskudsgivende agentur, og staten er tilskudskunden.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="4d6e7-146">Første gang du aktiverer funktionen, angives de oprindelige CFDA-numre ved hjælp af de eksisterende numre, der findes på tilskuddene.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="4d6e7-147">Udeluk tilskud fra SEFA-rapportering baseret på tilskudstype</span><span class="sxs-lookup"><span data-stu-id="4d6e7-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="4d6e7-148">Gå til **Projektstyring og regnskab \> Opsætning \> Tilskud \> Tilskudstyper**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="4d6e7-149">I oversigtspanelet **Standardoplysninger** skal du vælge afkrydsningsfeltet **Udeluk fra plan for udgifter til føderale priser**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="4d6e7-150">Vælg **Gem** for at gemme dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4d6e7-151">Kør forespørgslen for planen for udgifter til føderale priser</span><span class="sxs-lookup"><span data-stu-id="4d6e7-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="4d6e7-152">Gå til **Projektstyring og regnskab \> Forespørgsler og rapporter \> Tilskudsforespørgsel \> Plan for udgifter til føderale priser**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="4d6e7-153">I sektionen **Parametre** skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="4d6e7-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="4d6e7-154">I feltet **Datointerval** skal du vælge koden for datointervallet.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="4d6e7-155">Du kan også definere datointervallet i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="4d6e7-156">Valgfrit: Hvis du kun vil inkludere de fakturerede transaktioner som indtægt i forespørgslen, skal du angive indstillingen **Inkluder kun fakturerede indtægter** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="4d6e7-157">Kolonner</span><span class="sxs-lookup"><span data-stu-id="4d6e7-157">Columns</span></span>

<span data-ttu-id="4d6e7-158">Forespørgsel om planen for udgifter til føderale priser omfatter følgende kolonner:</span><span class="sxs-lookup"><span data-stu-id="4d6e7-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="4d6e7-159">Klyngenavn for katalog over Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="4d6e7-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="4d6e7-160">Tilskudsgivende agentur</span><span class="sxs-lookup"><span data-stu-id="4d6e7-160">Grantor agency</span></span>
- <span data-ttu-id="4d6e7-161">Gennemgående agentur</span><span class="sxs-lookup"><span data-stu-id="4d6e7-161">Pass-through agency</span></span>
- <span data-ttu-id="4d6e7-162">Navn på tilskud</span><span class="sxs-lookup"><span data-stu-id="4d6e7-162">Grant name</span></span>
- <span data-ttu-id="4d6e7-163">Tilskuds-id</span><span class="sxs-lookup"><span data-stu-id="4d6e7-163">Grant ID</span></span>
- <span data-ttu-id="4d6e7-164">Id for tilskudsansøgning</span><span class="sxs-lookup"><span data-stu-id="4d6e7-164">Grant application ID</span></span>
- <span data-ttu-id="4d6e7-165">Katalog over Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="4d6e7-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="4d6e7-166">Kvitteringer</span><span class="sxs-lookup"><span data-stu-id="4d6e7-166">Receipts</span></span>
- <span data-ttu-id="4d6e7-167">Udgifter</span><span class="sxs-lookup"><span data-stu-id="4d6e7-167">Expenditures</span></span>
