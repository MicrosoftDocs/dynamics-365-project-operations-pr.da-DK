---
title: Oversigt over dimensioner for prisfastsættelse
description: Dette emne indeholder oplysninger om prisfastsættelsesdimensioner i Dynamics 365 Project Operations.
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898209"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="a7f18-103">Oversigt over dimensioner for prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="a7f18-103">Pricing dimensions overview</span></span>

<span data-ttu-id="a7f18-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a7f18-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a7f18-105">De dimensioner, der bruges i de menneskelige ressourcer til at konfigurere priser og omkostninger, falder i to kategorier:</span><span class="sxs-lookup"><span data-stu-id="a7f18-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="a7f18-106">Personer</span><span class="sxs-lookup"><span data-stu-id="a7f18-106">People</span></span>
- <span data-ttu-id="a7f18-107">Planlagt arbejde</span><span class="sxs-lookup"><span data-stu-id="a7f18-107">Planned work</span></span>

<span data-ttu-id="a7f18-108">Derfor findes der to typer værdier for prisfastsættelsesdimensioner:</span><span class="sxs-lookup"><span data-stu-id="a7f18-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="a7f18-109">**Grupperede indstillinger**: Dimensioner, der er fasttekster for et værdisæt.</span><span class="sxs-lookup"><span data-stu-id="a7f18-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="a7f18-110">**Objektbaserede værdier**: Dimensioner, der kan være et varieret sæt værdier.</span><span class="sxs-lookup"><span data-stu-id="a7f18-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="a7f18-111">Dimensioner for prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="a7f18-111">Pricing dimensions</span></span>

<span data-ttu-id="a7f18-112">Dynamics 365 Project Operations leveres med et standardsæt af prisfastsættelsesdimensioner.</span><span class="sxs-lookup"><span data-stu-id="a7f18-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="a7f18-113">Du kan få vist disse prisfastsættelsesdimensioner ved at gå til **Project Operations** > **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="a7f18-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="a7f18-114">I parameterposten på fanen **Beløbsbaserede prisdimensioner** skal du kontrollere, at rollen **msdyn_resourcecategory** og ressourceafdelingen, **msdyn_organizationalunit** har felterne **Gælder for Salg** og **Gælder for Omkostning** angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a7f18-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="a7f18-115">Ved at aktivere disse felter får du mulighed for at konfigurere prisen og omkostningerne for de enkelte kombinationer af rolle og afdeling.</span><span class="sxs-lookup"><span data-stu-id="a7f18-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="a7f18-116">Hvis du har brug for at fastsætte priser eller omkostninger for dine ressourcer ved hjælp af ekstra attributter, kan du oprette brugerdefinerede felter, objekter og dimensioner.</span><span class="sxs-lookup"><span data-stu-id="a7f18-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="a7f18-117">Prisfastsættelse af HR-tid</span><span class="sxs-lookup"><span data-stu-id="a7f18-117">Pricing human resource time</span></span>
<span data-ttu-id="a7f18-118">Hvordan en organisation prisfastsætter HR-tid er ofte en vigtig strategisk overvejelse, der direkte påvirker organisationens rentabilitet.</span><span class="sxs-lookup"><span data-stu-id="a7f18-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="a7f18-119">Arbejd sammen med økonomiteamene og praksischeferne, når organisationen er klar til at identificere, hvordan man vil konfigurere fakturerings- og omkostningssatser for HR-tid.</span><span class="sxs-lookup"><span data-stu-id="a7f18-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="a7f18-120">Andre overvejelser i forbindelse med prisfastsættelse omfatter, om du vil genbruge felter eller objekter, der ikke i øjeblikket er prisdimensioner, men gælder som en prisdimension for organisationen.</span><span class="sxs-lookup"><span data-stu-id="a7f18-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="a7f18-121">Felter som **Transaktionskategori** (**msdyn_transactioncategory**) og **Reserverbar ressource** (**bookableresource**) er eksempler på kandidatdimensioner.</span><span class="sxs-lookup"><span data-stu-id="a7f18-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="a7f18-122">Overvej, om din prisfastsættelsesdimension skal være en tabel eller en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="a7f18-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="a7f18-123">Hvis du forventer ændringer af værdierne i en dimension, som vil overstige 10 eller 12, og du har brug for flere attributter til disse værdier, kan du oprette et objekt i stedet for en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="a7f18-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="a7f18-124">Hvis du vedligeholder en grupperet indstilling, f.eks. tilføjelse eller fjernelse af værdier, kræves en administrator eller udvikler, og det er derfor muligt for de fleste brugere at tilføje nye rækker i en tabel.</span><span class="sxs-lookup"><span data-stu-id="a7f18-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="a7f18-125">I følgende eksempel vises de fakturarater, der er konfigureret på baggrund af den rolle og den organisationsenhed, som ressourcen tilhører.</span><span class="sxs-lookup"><span data-stu-id="a7f18-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="a7f18-126">Omkostningssatser er typisk baseret på medarbejderens lønområde og den afdeling, de er knyttet til.</span><span class="sxs-lookup"><span data-stu-id="a7f18-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="a7f18-127">I dette eksempel vil tabellerne over faktura- og omkostningssatser se ud som følger:</span><span class="sxs-lookup"><span data-stu-id="a7f18-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="a7f18-128">**Eksempler på fakturasatser**</span><span class="sxs-lookup"><span data-stu-id="a7f18-128">**Sample bill rates**</span></span>

| <span data-ttu-id="a7f18-129">Rolle</span><span class="sxs-lookup"><span data-stu-id="a7f18-129">Role</span></span>        | <span data-ttu-id="a7f18-130">Afdeling</span><span class="sxs-lookup"><span data-stu-id="a7f18-130">Org Unit</span></span>    |<span data-ttu-id="a7f18-131">Enhed</span><span class="sxs-lookup"><span data-stu-id="a7f18-131">Unit</span></span>      |<span data-ttu-id="a7f18-132">Pris</span><span class="sxs-lookup"><span data-stu-id="a7f18-132">Price</span></span>      |<span data-ttu-id="a7f18-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="a7f18-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="a7f18-134">Udvikler</span><span class="sxs-lookup"><span data-stu-id="a7f18-134">Developer</span></span>   | <span data-ttu-id="a7f18-135">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="a7f18-135">Contoso US</span></span>  |<span data-ttu-id="a7f18-136">Hour</span><span class="sxs-lookup"><span data-stu-id="a7f18-136">Hour</span></span> | <span data-ttu-id="a7f18-137">200</span><span class="sxs-lookup"><span data-stu-id="a7f18-137">200</span></span>|<span data-ttu-id="a7f18-138">USD</span><span class="sxs-lookup"><span data-stu-id="a7f18-138">USD</span></span>     |
| <span data-ttu-id="a7f18-139">Udvikler</span><span class="sxs-lookup"><span data-stu-id="a7f18-139">Developer</span></span>   | <span data-ttu-id="a7f18-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="a7f18-140">Contoso India</span></span> |<span data-ttu-id="a7f18-141">Hour</span><span class="sxs-lookup"><span data-stu-id="a7f18-141">Hour</span></span>|   <span data-ttu-id="a7f18-142">112</span><span class="sxs-lookup"><span data-stu-id="a7f18-142">112</span></span>|<span data-ttu-id="a7f18-143">USD</span><span class="sxs-lookup"><span data-stu-id="a7f18-143">USD</span></span>     |


<span data-ttu-id="a7f18-144">**Eksempel på omkostningssatser**</span><span class="sxs-lookup"><span data-stu-id="a7f18-144">**Sample cost rates**</span></span>

| <span data-ttu-id="a7f18-145">Lønområde</span><span class="sxs-lookup"><span data-stu-id="a7f18-145">Salary Band</span></span>     | <span data-ttu-id="a7f18-146">Afdeling</span><span class="sxs-lookup"><span data-stu-id="a7f18-146">Org Unit</span></span>    |<span data-ttu-id="a7f18-147">Enhed</span><span class="sxs-lookup"><span data-stu-id="a7f18-147">Unit</span></span>      |<span data-ttu-id="a7f18-148">Pris</span><span class="sxs-lookup"><span data-stu-id="a7f18-148">Price</span></span>      |<span data-ttu-id="a7f18-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="a7f18-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="a7f18-150">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="a7f18-150">My company_Band1</span></span> | <span data-ttu-id="a7f18-151">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="a7f18-151">Contoso US</span></span>  |<span data-ttu-id="a7f18-152">Hour</span><span class="sxs-lookup"><span data-stu-id="a7f18-152">Hour</span></span> | <span data-ttu-id="a7f18-153">145</span><span class="sxs-lookup"><span data-stu-id="a7f18-153">145</span></span>|<span data-ttu-id="a7f18-154">USD</span><span class="sxs-lookup"><span data-stu-id="a7f18-154">USD</span></span>     |
| <span data-ttu-id="a7f18-155">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="a7f18-155">My company_Band2</span></span> | <span data-ttu-id="a7f18-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="a7f18-156">Contoso India</span></span> |<span data-ttu-id="a7f18-157">Hour</span><span class="sxs-lookup"><span data-stu-id="a7f18-157">Hour</span></span>|   <span data-ttu-id="a7f18-158">67</span><span class="sxs-lookup"><span data-stu-id="a7f18-158">67</span></span>|<span data-ttu-id="a7f18-159">USD</span><span class="sxs-lookup"><span data-stu-id="a7f18-159">USD</span></span>     |
