---
title: Startside med dimensioner for prisfastsættelse og efterkalkulation
description: Dette emne indeholder en oversigt over prisdimensioner.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074213"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="bcdc0-103">Startside med dimensioner for prisfastsættelse og efterkalkulation</span><span class="sxs-lookup"><span data-stu-id="bcdc0-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="bcdc0-104">De dimensioner, der bruges til at angive prisfastsættelsen af arbejdskraft og omkostninger i projektbaserede organisationer, påvirkes af følgende attributter:</span><span class="sxs-lookup"><span data-stu-id="bcdc0-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="bcdc0-105">Personer, der arbejder med opgaver svarende til deres erfaring, rolle eller geografi</span><span class="sxs-lookup"><span data-stu-id="bcdc0-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="bcdc0-106">Arbejde, der skal udføres på en måde, som svarer til dets kompleksitet eller tidspunkt på dagen</span><span class="sxs-lookup"><span data-stu-id="bcdc0-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="bcdc0-107">Som følge af disse attributters typiske karakteristika for arbejdet og de personer, der er nødvendige for at udføre arbejdet, findes der to typer prisfastsættelsesdimensionsværdier i Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="bcdc0-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="bcdc0-108">**Grupperede indstillinger** : - Attributter, der er fasttekster for et værdisæt.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="bcdc0-109">**Objektbaserede værdier** - Attributter, der kan have varierende værdisæt, som er begrænsede, men som kan ændres med tiden.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="bcdc0-110">Dimensioner for prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="bcdc0-110">Pricing dimensions</span></span>

<span data-ttu-id="bcdc0-111">PSA-leverancer med et standardsæt af prisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="bcdc0-112">Du kan få vist disse ved at gå til **Project Service** > **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="bcdc0-113">I parameterposten på fanen **Beløbsbaserede prisdimensioner** skal du kontrollere, at rollen **msdyn_resourcecategory** og ressourceafdelingen, **msdyn_organizationalunit** har felterne **Gælder for Salg** og **Gælder for Omkostning** angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="bcdc0-114">Det giver dig mulighed for at konfigurere prisen og omkostningerne for de enkelte kombinationer af rolle og afdeling.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Skærmbillede af Project Service-parametre, hvor "Gælder for Salg" er markeret](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="bcdc0-116">Hvis du har brugt standardfelterne for både rolle og afdeling som prisdimensioner før version 3 af PSA, er der ingen bemærkelsesværdige ændringer.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="bcdc0-117">Du kan fortsætte med at bruge Project Service, som du plejer.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="bcdc0-118">Hvis du har brug for at fastsætte priser eller omkostninger for dine ressourcer ved hjælp af ekstra attributter, kan du oprette brugerdefinerede felter, objekter og dimensioner.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="bcdc0-119">Du kan finde flere oplysninger i følgende emner, men vær opmærksom på, at du skal udføre procedurerne i den rækkefølge, der er angivet nedenfor:</span><span class="sxs-lookup"><span data-stu-id="bcdc0-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="bcdc0-120">Oprette brugerdefinerede felter og objekter</span><span class="sxs-lookup"><span data-stu-id="bcdc0-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="bcdc0-121">Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter</span><span class="sxs-lookup"><span data-stu-id="bcdc0-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="bcdc0-122">Konfigurer brugerdefinerede felter som prisfastsættelsesdimensioner </span><span class="sxs-lookup"><span data-stu-id="bcdc0-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="bcdc0-123">Opdatere plug-in-attributter, så de indeholder nye prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="bcdc0-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="bcdc0-124">Prisfastsættelse af HR-tid</span><span class="sxs-lookup"><span data-stu-id="bcdc0-124">Pricing human resource time</span></span>
<span data-ttu-id="bcdc0-125">Hvordan en organisation prisfastsætter HR-tid er ofte en vigtig strategisk overvejelse, der direkte påvirker organisationens rentabilitet.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="bcdc0-126">Arbejd sammen med økonomiteamene og praksischeferne, når organisationen er klar til at identificere, hvordan man vil konfigurere fakturerings- og omkostningssatser for HR-tid.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="bcdc0-127">Andre overvejelser i forbindelse med prisfastsættelse omfatter, om du vil genbruge felter eller objekter, der ikke i øjeblikket er prisdimensioner, men gælder som en prisdimension for organisationen.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="bcdc0-128">Felter som **Transaktionskategori** ( **msdyn_transactioncategory** ) og **Reserverbar ressource** ( **bookableresource** ) er eksempler på kandidatdimensioner.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="bcdc0-129">Overvej, om din prisfastsættelsesdimension skal være en tabel eller en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="bcdc0-130">Hvis du forventer at foretage ændringer af værdierne i en dimension, som vil overstige 10 eller 12, og du har brug for flere attributter til disse værdier, skal du oprette et objekt i stedet for en grupperet indstilling.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="bcdc0-131">Hvis du bevarer en grupperet indstilling, f.eks. tilføjelse eller fjernelse af værdier, kræver det en administrator eller udvikler, og det er derfor muligt for de fleste erhvervsbrugere at tilføje nye rækker i en tabel.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="bcdc0-132">I følgende eksempel vises de fakturarater, der er konfigureret på baggrund af den rolle og den organisationsenhed, som ressourcen tilhører.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="bcdc0-133">Omkostningssatser er typisk baseret på medarbejderens lønområde og den afdeling, de er knyttet til.</span><span class="sxs-lookup"><span data-stu-id="bcdc0-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="bcdc0-134">I dette eksempel vil tabellerne over faktura- og omkostningssatser se ud som følger:</span><span class="sxs-lookup"><span data-stu-id="bcdc0-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="bcdc0-135">**Eksempler på fakturasatser**</span><span class="sxs-lookup"><span data-stu-id="bcdc0-135">**Sample bill rates**</span></span>

| <span data-ttu-id="bcdc0-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="bcdc0-136">Role</span></span>        | <span data-ttu-id="bcdc0-137">Afdeling</span><span class="sxs-lookup"><span data-stu-id="bcdc0-137">Org Unit</span></span>    |<span data-ttu-id="bcdc0-138">Enhed</span><span class="sxs-lookup"><span data-stu-id="bcdc0-138">Unit</span></span>      |<span data-ttu-id="bcdc0-139">Pris</span><span class="sxs-lookup"><span data-stu-id="bcdc0-139">Price</span></span>      |<span data-ttu-id="bcdc0-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="bcdc0-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="bcdc0-141">Udvikler</span><span class="sxs-lookup"><span data-stu-id="bcdc0-141">Developer</span></span>   | <span data-ttu-id="bcdc0-142">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="bcdc0-142">Contoso US</span></span>  |<span data-ttu-id="bcdc0-143">Hour</span><span class="sxs-lookup"><span data-stu-id="bcdc0-143">Hour</span></span> | <span data-ttu-id="bcdc0-144">200</span><span class="sxs-lookup"><span data-stu-id="bcdc0-144">200</span></span>|<span data-ttu-id="bcdc0-145">USD</span><span class="sxs-lookup"><span data-stu-id="bcdc0-145">USD</span></span>     |
| <span data-ttu-id="bcdc0-146">Udvikler</span><span class="sxs-lookup"><span data-stu-id="bcdc0-146">Developer</span></span>   | <span data-ttu-id="bcdc0-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="bcdc0-147">Contoso India</span></span> |<span data-ttu-id="bcdc0-148">Hour</span><span class="sxs-lookup"><span data-stu-id="bcdc0-148">Hour</span></span>|   <span data-ttu-id="bcdc0-149">112</span><span class="sxs-lookup"><span data-stu-id="bcdc0-149">112</span></span>|<span data-ttu-id="bcdc0-150">USD</span><span class="sxs-lookup"><span data-stu-id="bcdc0-150">USD</span></span>     |


<span data-ttu-id="bcdc0-151">**Eksempel på omkostningssatser**</span><span class="sxs-lookup"><span data-stu-id="bcdc0-151">**Sample cost rates**</span></span>

| <span data-ttu-id="bcdc0-152">Lønområde</span><span class="sxs-lookup"><span data-stu-id="bcdc0-152">Salary Band</span></span>     | <span data-ttu-id="bcdc0-153">Afdeling</span><span class="sxs-lookup"><span data-stu-id="bcdc0-153">Org Unit</span></span>    |<span data-ttu-id="bcdc0-154">Enhed</span><span class="sxs-lookup"><span data-stu-id="bcdc0-154">Unit</span></span>      |<span data-ttu-id="bcdc0-155">Pris</span><span class="sxs-lookup"><span data-stu-id="bcdc0-155">Price</span></span>      |<span data-ttu-id="bcdc0-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="bcdc0-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="bcdc0-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="bcdc0-157">My company_Band1</span></span> | <span data-ttu-id="bcdc0-158">Contoso USA</span><span class="sxs-lookup"><span data-stu-id="bcdc0-158">Contoso US</span></span>  |<span data-ttu-id="bcdc0-159">Hour</span><span class="sxs-lookup"><span data-stu-id="bcdc0-159">Hour</span></span> | <span data-ttu-id="bcdc0-160">145</span><span class="sxs-lookup"><span data-stu-id="bcdc0-160">145</span></span>|<span data-ttu-id="bcdc0-161">USD</span><span class="sxs-lookup"><span data-stu-id="bcdc0-161">USD</span></span>     |
| <span data-ttu-id="bcdc0-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="bcdc0-162">My company_Band2</span></span> | <span data-ttu-id="bcdc0-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="bcdc0-163">Contoso India</span></span> |<span data-ttu-id="bcdc0-164">Hour</span><span class="sxs-lookup"><span data-stu-id="bcdc0-164">Hour</span></span>|   <span data-ttu-id="bcdc0-165">67</span><span class="sxs-lookup"><span data-stu-id="bcdc0-165">67</span></span>|<span data-ttu-id="bcdc0-166">USD</span><span class="sxs-lookup"><span data-stu-id="bcdc0-166">USD</span></span>     |