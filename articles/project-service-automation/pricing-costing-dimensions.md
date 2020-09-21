---
title: Startside med dimensioner for prisfastsættelse og efterkalkulation
description: Dette emne indeholder en oversigt over prisdimensioner.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750526"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="f4bc3-103">Startside med dimensioner for prisfastsættelse og efterkalkulation</span><span class="sxs-lookup"><span data-stu-id="f4bc3-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="f4bc3-104">De dimensioner, der bruges i de menneskelige ressourcer til at konfigurere priser og omkostninger, falder i to kategorier:</span><span class="sxs-lookup"><span data-stu-id="f4bc3-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="f4bc3-105">Personer</span><span class="sxs-lookup"><span data-stu-id="f4bc3-105">People</span></span>
- <span data-ttu-id="f4bc3-106">Planlagt arbejde</span><span class="sxs-lookup"><span data-stu-id="f4bc3-106">Planned work</span></span>

<span data-ttu-id="f4bc3-107">Derfor findes der to typer dimensionsværdier for prisfastsættelse i PSA (Project Service Automation):</span><span class="sxs-lookup"><span data-stu-id="f4bc3-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="f4bc3-108">**Grupperede indstillinger** – Indstillinger, der er fasttekster for et værdisæt.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="f4bc3-109">**Objektbaserede værdier** – Dimensioner, der kan være et varieret sæt værdier.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="f4bc3-110">Prisdimensioner</span><span class="sxs-lookup"><span data-stu-id="f4bc3-110">Pricing dimensions</span></span>

<span data-ttu-id="f4bc3-111">PSA-leverancer med et standardsæt af prisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="f4bc3-112">Du kan få vist disse ved at gå til **Project Service** > **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="f4bc3-113">I parameterposten på fanen **Beløbsbaserede prisdimensioner** skal du kontrollere, at rollen **msdyn_resourcecategory** og ressourceafdelingen, **msdyn_organizationalunit** har felterne **Gælder for Salg** og **Gælder for Omkostning** angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="f4bc3-114">Det giver dig mulighed for at konfigurere prisen og omkostningerne for de enkelte kombinationer af rolle og afdeling.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Skærmbillede af Project Service-parametre, hvor "Gælder for Salg" er markeret](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="f4bc3-116">Hvis du har brugt standardfelterne for både rolle og afdeling som prisdimensioner før version 3 af PSA, er der ingen bemærkelsesværdige ændringer.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="f4bc3-117">Du kan fortsætte med at bruge Project Service, som du plejer.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="f4bc3-118">Hvis du har brug for at fastsætte priser eller omkostninger for dine ressourcer ved hjælp af ekstra attributter, kan du oprette brugerdefinerede felter, objekter og dimensioner.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="f4bc3-119">Du kan finde flere oplysninger i følgende emner, men vær opmærksom på, at du skal udføre procedurerne i den rækkefølge, der er angivet nedenfor:</span><span class="sxs-lookup"><span data-stu-id="f4bc3-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="f4bc3-120">Oprette brugerdefinerede felter og objekter</span><span class="sxs-lookup"><span data-stu-id="f4bc3-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="f4bc3-121">Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter</span><span class="sxs-lookup"><span data-stu-id="f4bc3-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="f4bc3-122">Konfigurere brugerdefinerede felter som prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="f4bc3-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="f4bc3-123">Opdatere plug-in-attributter, så de indeholder nye prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="f4bc3-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="f4bc3-124">Prisfastsættelse af HR-tid</span><span class="sxs-lookup"><span data-stu-id="f4bc3-124">Pricing human resource time</span></span>
<span data-ttu-id="f4bc3-125">Hvordan en organisation prisfastsætter HR-tid er ofte en vigtig strategisk overvejelse, der direkte påvirker organisationens rentabilitet.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="f4bc3-126">Arbejd sammen med økonomiteamene og praksischeferne, når organisationen er klar til at identificere, hvordan man vil konfigurere fakturerings- og omkostningssatser for HR-tid.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="f4bc3-127">Andre overvejelser i forbindelse med prisfastsættelse omfatter, om du vil genbruge felter eller objekter, der ikke i øjeblikket er prisdimensioner, men gælder som en prisdimension for organisationen.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="f4bc3-128">Felter som **Transaktionskategori** (**msdyn_transactioncategory**) og **Reserverbar ressource** (**bookableresource**) er eksempler på kandidatdimensioner.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="f4bc3-129">Du skal også overveje, om prisdimensionen skal være en tabel eller en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="f4bc3-130">Hvis du forventer ændringer af værdierne i en dimension, som vil overstige 10 eller 12, og du har brug for flere attributter til disse værdier, kan du oprette et objekt i stedet for en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="f4bc3-131">Hvis du vedligeholder en grupperet indstilling, f.eks. tilføjelse eller fjernelse af værdier, kræves en administrator eller udvikler, og det er derfor muligt for de fleste brugere at tilføje nye rækker i en tabel.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="f4bc3-132">I følgende eksempel vises de fakturarater, der er konfigureret på baggrund af den rolle og den organisationsenhed, som ressourcen tilhører.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="f4bc3-133">Omkostningssatser er typisk baseret på medarbejderens lønområde og den afdeling, de er knyttet til.</span><span class="sxs-lookup"><span data-stu-id="f4bc3-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="f4bc3-134">I dette eksempel vil tabellerne over faktura- og omkostningssatser se ud som følger:</span><span class="sxs-lookup"><span data-stu-id="f4bc3-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="f4bc3-135">**Eksempler på fakturasatser**</span><span class="sxs-lookup"><span data-stu-id="f4bc3-135">**Sample bill rates**</span></span>

| <span data-ttu-id="f4bc3-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="f4bc3-136">Role</span></span>        | <span data-ttu-id="f4bc3-137">Afdeling</span><span class="sxs-lookup"><span data-stu-id="f4bc3-137">Org Unit</span></span>    |<span data-ttu-id="f4bc3-138">Enhed</span><span class="sxs-lookup"><span data-stu-id="f4bc3-138">Unit</span></span>      |<span data-ttu-id="f4bc3-139">Pris</span><span class="sxs-lookup"><span data-stu-id="f4bc3-139">Price</span></span>      |<span data-ttu-id="f4bc3-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4bc3-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f4bc3-141">Udvikler</span><span class="sxs-lookup"><span data-stu-id="f4bc3-141">Developer</span></span>   | <span data-ttu-id="f4bc3-142">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="f4bc3-142">Contoso US</span></span>  |<span data-ttu-id="f4bc3-143">Hour</span><span class="sxs-lookup"><span data-stu-id="f4bc3-143">Hour</span></span> | <span data-ttu-id="f4bc3-144">200</span><span class="sxs-lookup"><span data-stu-id="f4bc3-144">200</span></span>|<span data-ttu-id="f4bc3-145">USD</span><span class="sxs-lookup"><span data-stu-id="f4bc3-145">USD</span></span>     |
| <span data-ttu-id="f4bc3-146">Udvikler</span><span class="sxs-lookup"><span data-stu-id="f4bc3-146">Developer</span></span>   | <span data-ttu-id="f4bc3-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f4bc3-147">Contoso India</span></span> |<span data-ttu-id="f4bc3-148">Hour</span><span class="sxs-lookup"><span data-stu-id="f4bc3-148">Hour</span></span>|   <span data-ttu-id="f4bc3-149">112</span><span class="sxs-lookup"><span data-stu-id="f4bc3-149">112</span></span>|<span data-ttu-id="f4bc3-150">USD</span><span class="sxs-lookup"><span data-stu-id="f4bc3-150">USD</span></span>     |


<span data-ttu-id="f4bc3-151">**Eksempel på omkostningssatser**</span><span class="sxs-lookup"><span data-stu-id="f4bc3-151">**Sample cost rates**</span></span>

| <span data-ttu-id="f4bc3-152">Lønområde</span><span class="sxs-lookup"><span data-stu-id="f4bc3-152">Salary Band</span></span>     | <span data-ttu-id="f4bc3-153">Afdeling</span><span class="sxs-lookup"><span data-stu-id="f4bc3-153">Org Unit</span></span>    |<span data-ttu-id="f4bc3-154">Enhed</span><span class="sxs-lookup"><span data-stu-id="f4bc3-154">Unit</span></span>      |<span data-ttu-id="f4bc3-155">Pris</span><span class="sxs-lookup"><span data-stu-id="f4bc3-155">Price</span></span>      |<span data-ttu-id="f4bc3-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4bc3-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f4bc3-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="f4bc3-157">My company_Band1</span></span> | <span data-ttu-id="f4bc3-158">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="f4bc3-158">Contoso US</span></span>  |<span data-ttu-id="f4bc3-159">Hour</span><span class="sxs-lookup"><span data-stu-id="f4bc3-159">Hour</span></span> | <span data-ttu-id="f4bc3-160">145</span><span class="sxs-lookup"><span data-stu-id="f4bc3-160">145</span></span>|<span data-ttu-id="f4bc3-161">USD</span><span class="sxs-lookup"><span data-stu-id="f4bc3-161">USD</span></span>     |
| <span data-ttu-id="f4bc3-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="f4bc3-162">My company_Band2</span></span> | <span data-ttu-id="f4bc3-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f4bc3-163">Contoso India</span></span> |<span data-ttu-id="f4bc3-164">Hour</span><span class="sxs-lookup"><span data-stu-id="f4bc3-164">Hour</span></span>|   <span data-ttu-id="f4bc3-165">67</span><span class="sxs-lookup"><span data-stu-id="f4bc3-165">67</span></span>|<span data-ttu-id="f4bc3-166">USD</span><span class="sxs-lookup"><span data-stu-id="f4bc3-166">USD</span></span>     |
