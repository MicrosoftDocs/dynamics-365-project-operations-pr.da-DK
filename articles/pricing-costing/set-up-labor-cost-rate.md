---
title: Konfigurer satser for arbejdskraftomkostninger
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer satser for arbejdskraftomkostninger i Project Operations
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d17f266b6e34fc2a2743fe19fd18b15fb992ceef
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074069"
---
# <a name="set-up-labor-cost-rates"></a><span data-ttu-id="dbbd3-103">Konfigurer satser for arbejdskraftomkostninger</span><span class="sxs-lookup"><span data-stu-id="dbbd3-103">Set up labor cost rates</span></span>

<span data-ttu-id="dbbd3-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="dbbd3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="dbbd3-105">Hver prisliste har et sæt satser for arbejdskraft (rollepriser), der stemmer overens med indholdet og ikrafttrædelsesdatoen for prislisten.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-105">Each price list has a set of labor rates (role prices) that align with the content and date effectivity of the price list.</span></span>

1. <span data-ttu-id="dbbd3-106">Opret en prislisten og vælge derefter i undergitteret på fanen **Rollepriser** **+ Ny rolle**.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-106">Create a price list and on the **Role Price** tab, in the sub-grid, select **New Role**.</span></span>
2. <span data-ttu-id="dbbd3-107">På siden **Hurtig oprettelse** skal du vælge rollen og organisationsenheden.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-107">On the **Quick Create** page, select the role and organization unit.</span></span>
3. <span data-ttu-id="dbbd3-108">Angiv eventuelle andre krævede feltoplysninger.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-108">Enter any other required field information.</span></span>

<span data-ttu-id="dbbd3-109">Følgende tabel indeholder nogle af de felter, der er vigtige, når du opretter arbejdskraftsatser på en kostprisliste.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-109">The following table includes some of the fields that are important when creating labor rates on a cost price list.</span></span>

| <span data-ttu-id="dbbd3-110">Felt</span><span class="sxs-lookup"><span data-stu-id="dbbd3-110">Field</span></span> | <span data-ttu-id="dbbd3-111">Lokation</span><span class="sxs-lookup"><span data-stu-id="dbbd3-111">Location</span></span> | <span data-ttu-id="dbbd3-112">Relevans, formål og vejledning</span><span class="sxs-lookup"><span data-stu-id="dbbd3-112">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="dbbd3-113">Downstream-virkning</span><span class="sxs-lookup"><span data-stu-id="dbbd3-113">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="dbbd3-114">Rolle</span><span class="sxs-lookup"><span data-stu-id="dbbd3-114">Role</span></span> | <span data-ttu-id="dbbd3-115">Fanen **Generelt** og siderne **Hurtig oprettelse**</span><span class="sxs-lookup"><span data-stu-id="dbbd3-115">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="dbbd3-116">Vælg den rolle, som omkostningssatsen finder anvendelse for.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-116">Select the role that the cost rate applies to.</span></span> | <span data-ttu-id="dbbd3-117">Rollen på det indgående estimat eller den faktiske oplysning sammenholdelse med denne linje for at angive standarden for rollens omkostning.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-117">The role on the incoming estimate or actual will be matched against this line to default the cost of the role.</span></span> |
| <span data-ttu-id="dbbd3-118">Ressourcevirksomhed</span><span class="sxs-lookup"><span data-stu-id="dbbd3-118">Resourcing Company</span></span> | <span data-ttu-id="dbbd3-119">Fanen **Generelt** og siderne **Hurtig oprettelse**</span><span class="sxs-lookup"><span data-stu-id="dbbd3-119">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="dbbd3-120">Vælg den juridiske enhed, som rollen tildeles.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-120">Select the legal entity that the role is assigned to.</span></span> <span data-ttu-id="dbbd3-121">En udvikler fra Fabrikam i Indien eller en udvikler fra Fabrikam i USA.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-121">For example, a developer from Fabrikam India or a developer from Fabrikam USA.</span></span> | <span data-ttu-id="dbbd3-122">Ressourcevirksomheden på det indgående estimat eller den faktiske oplysning sammenholdelse med denne linje for at angive standarden for rollens omkostningssats.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-122">The resourcing company on the incoming estimate or actual will be matched against this line to default the cost rate of the role.</span></span> |
| <span data-ttu-id="dbbd3-123">Ressourceenhed</span><span class="sxs-lookup"><span data-stu-id="dbbd3-123">Resourcing Unit</span></span> | <span data-ttu-id="dbbd3-124">Fanen **Generelt** og siderne **Hurtig oprettelse**</span><span class="sxs-lookup"><span data-stu-id="dbbd3-124">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="dbbd3-125">Vælg organisationsenheden eller afdelingen i den virksomhed, hvor denne rollen skal anvendes.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-125">Select the organizational unit or division of the company from where this role will be used.</span></span> <span data-ttu-id="dbbd3-126">En udvikler fra Fabrikams Robotics-afdeling i Indien eller en udvikler fra Fabrikams softwareafdeling i USA.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-126">For example, a developer from the Robotics division of Fabrikam India or a developer from the Software division of Fabrikam USA.</span></span> | <span data-ttu-id="dbbd3-127">Ressourceenheden på det indgående estimat eller den faktiske oplysning sammenholdelse med denne linje for at angive standarden for rollens omkostning.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-127">The resourcing unit on the incoming estimate or actual will be matched against this line to default the cost of the role.</span></span> |
| <span data-ttu-id="dbbd3-128">Pris</span><span class="sxs-lookup"><span data-stu-id="dbbd3-128">Price</span></span> | <span data-ttu-id="dbbd3-129">Fanen **Generelt** og siderne **Hurtig oprettelse**</span><span class="sxs-lookup"><span data-stu-id="dbbd3-129">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="dbbd3-130">Konfigurer omkostningssatsen for kombinationen rolle, ressourcevirksomhed og ressourceenhed.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-130">Set up the cost rate for the role, resourcing company, and resourcing unit combination.</span></span> <span data-ttu-id="dbbd3-131">En udvikler fra Fabrikam i Indien koster eksempelvis 1.000 INR eller en udvikler fra Fabrikam i USA, som koster 150 USD.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-131">For example, a developer from Fabrikam India costs 1000 INR or a developer from Fabrikam USA costs 150 USD.</span></span> | <span data-ttu-id="dbbd3-132">Prisen er den omkostningssats, hvis standard er baseret på pr. enhedsomkostning for det indgående estimat eller den faktiske linje for transaktionsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-132">The price is the cost rate that defaults on the per unit cost of the incoming estimate or actual line for the **Time** transaction class.</span></span> |
| <span data-ttu-id="dbbd3-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="dbbd3-133">Currency</span></span> | <span data-ttu-id="dbbd3-134">Fanen **Generelt** og siderne **Hurtig oprettelse**</span><span class="sxs-lookup"><span data-stu-id="dbbd3-134">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="dbbd3-135">Valutaen hentes som standard fra valutaen i overskriften til omkostningsprislisten, men kan tilsidesættes.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-135">By default, the currency value comes from the currency on the header of the cost price list but can be overridden.</span></span> <span data-ttu-id="dbbd3-136">En udvikler fra Fabrikam i Indien koster f.eks. 1.000 INR.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-136">For example, a developer from Fabrikam India costs 1000 INR.</span></span> <span data-ttu-id="dbbd3-137">En udvikler fra Fabrikam i USA koster 150 USD.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-137">A developer from Fabrikam USA costs 150 USD.</span></span> | <span data-ttu-id="dbbd3-138">Denne valutas standard hentes fra pr. enhedsomkostningen for den indgående faktiske omkostningsbasis for transaktionsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-138">This currency defaults on the per unit cost of the incoming actual cost line for the **Time** transaction class.</span></span> <span data-ttu-id="dbbd3-139">I et projektestimat konverteres valutaværdien til projektvalutaen og vises på estimatets tidsinddelte visning.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-139">On a project estimate, the currency value is converted to the project currency and shown on the Time-phased view of the estimate.</span></span> |
| <span data-ttu-id="dbbd3-140">Enhedsplan</span><span class="sxs-lookup"><span data-stu-id="dbbd3-140">Unit Schedule</span></span> | <span data-ttu-id="dbbd3-141">Fanen **Generelt** og siderne **Hurtig oprettelse**</span><span class="sxs-lookup"><span data-stu-id="dbbd3-141">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="dbbd3-142">Standarden for enhedsplanen er tid, og dette kan ikke ændres på rollens prisobjekt, da det bruges til at udtrykke satser pr. tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-142">The unit schedule defaults to Time and can't be changed on the Role price entity because it is used express rates by units of time.</span></span> | <span data-ttu-id="dbbd3-143">Dette har ingen afledt indvirkning.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-143">There is no downstream impact.</span></span> |
| <span data-ttu-id="dbbd3-144">Enhed</span><span class="sxs-lookup"><span data-stu-id="dbbd3-144">Unit</span></span> | <span data-ttu-id="dbbd3-145">Fanen **Generelt** og siderne **Hurtig oprettelse**</span><span class="sxs-lookup"><span data-stu-id="dbbd3-145">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="dbbd3-146">Værdien hentes som standard fra feltet **Tidsenhed** i overskriften til omkostningsprislisten.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-146">By default, the value comes from the **Time Unit** field on the header of the cost price list.</span></span> <span data-ttu-id="dbbd3-147">Værdien kan tilsidesættes.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-147">The value can be overridden.</span></span> <span data-ttu-id="dbbd3-148">En udvikler fra Fabrikam i Indien koster f.eks. 1.000 INR pr. **dag i Indien**.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-148">For example, a developer from Fabrikam India costs 1000 INR per **India Day**.</span></span> <span data-ttu-id="dbbd3-149">En udvikler fra Fabrikam USA koster 150 USD pr. **dag i USA**.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-149">A developer from Fabrikam USA costs 150 USD per **US Day**.</span></span> | <span data-ttu-id="dbbd3-150">Systemet bruger systemet med enheder og konvertering i basisenheder til at beregne en pris pr. enhed for at beregne standardprisen pr. enhed på en indgående estimatlinje eller en faktisk linje.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-150">The system uses the system of units and conversion in base units to compute a per unit cost to calculate the default price per unit on an incoming estimate or actual line.</span></span> <span data-ttu-id="dbbd3-151">Et estimat er f.eks. arbejde i 10 **dage i Indien** for en udvikler fra Indien, og enheden **dag i Indien** er angivet til 10 timer.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-151">For example, an estimate is for 10 **India Days** worth of work for a developer from India, and the unit, **India Day** is defined as 10 hours.</span></span> <span data-ttu-id="dbbd3-152">I forbindelse med omkostningsfastsættelse af den pågældende estimatlinje beregner programmet enhedsomkostningen på estimatet som: 1.000 INR/10 timer = 100 INR pr. time, hvilket konverteres til USD og vises som enhedsomkostningen på siden **Projektestimater**.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-152">When costing that estimate line, the application calculates the unit cost on the estimate as: 1000 INR/ 10 hours = 100 INR per hour which is converted into USD and shown as the unit cost on the **Project Estimates** page.</span></span> |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a><span data-ttu-id="dbbd3-153">Overførsel af priser og omkostninger for ressourcer uden for din afdeling eller juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="dbbd3-153">Transfer pricing and costs for resources outside of your division or legal entity</span></span>

<span data-ttu-id="dbbd3-154">I projektbaserede virksomheder er det almindeligt at anvende medarbejdere fra andre juridiske enheder eller afdelinger på projekter.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-154">In project-based companies, it's common to use employees from different legal entities or divisions on projects.</span></span> <span data-ttu-id="dbbd3-155">Et projekt kan udføres af en bestemt juridisk enhed, men medarbejdere eller konsulenter, der arbejder på projektet, kan komme fra samme juridiske enhed eller en anden eller måske en kombination af begge.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-155">A project can be executed by one legal entity, but the employees or consultants that work on the project could come from the same legal entity or from a different one, or there may be a combination of both.</span></span> <span data-ttu-id="dbbd3-156">I Dynamics 365 Project Operations er den juridiske enhed, der ejer leveringen af projektet, den **Ejende virksomhed** , og den afdeling, der ejer leveringen, er **Kontraktenheden**.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-156">In Dynamics 365 Project Operations, the legal entity that owns the delivery of the project is the **Owning Company** and the division that owns the delivery is the **Contracting Unit**.</span></span> <span data-ttu-id="dbbd3-157">Andre juridiske enheder, der leverer ressourcer, kaldes **Ressourcevirksomheder** , og de afdelinger, der leverer ressourcer, kaldes **Ressourceenheder**.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-157">Other legal entities that provide resources are the **Resourcing companies** and divisions that provide resources are the **Resourcing Units**.</span></span> <span data-ttu-id="dbbd3-158">I de fleste lande er virksomheder forpligtet til at sikre, at den juridiske ressourceenhed eller afdeling opkræver betaling ved den ejende virksomhed og kontraktenheden for at bruge ressourcerne.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-158">In most countries, companies are required to ensure that the resourcing legal entity or division, charge the owning company and the contracting unit for the use of resources.</span></span>

<span data-ttu-id="dbbd3-159">Fabrikam-koncernen skal f.eks. sikre, at Fabrikam Robotics i Indien har forhandlet en omkostningssatstabel med Fabrikam Robotics i USA eller Fabrikam Robotics i Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-159">For example, the Fabrikam corporation must ensure that Fabrikam India-Robotics has a negotiated a cost rate card with Fabrikam US-Robotics or Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="dbbd3-160">En udvikler fra Fabrikam Robotics i Indien opkræver 100 $, når denne udlånes til Fabrikam Robotics i USA, og 150 $, når denne udlånes til Fabrikam Robotics i Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-160">A developer from Fabrikam India-Robotic charges $100 when lent to Fabrikam US-Robotics and $150 when lent to Fabrikam U-Robotics.</span></span>

### <a name="set-up-costs-for-outside-resources"></a><span data-ttu-id="dbbd3-161">Konfigurer omkostninger for eksterne ressourcer</span><span class="sxs-lookup"><span data-stu-id="dbbd3-161">Set up costs for outside resources</span></span>

1. <span data-ttu-id="dbbd3-162">Opret en kostprisliste kaldet *Omkostningssatser for Fabrikam Robotics i USA* , og angiv et interval for ikrafttrædelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-162">Create a cost price list called, *Fabrikam US-Robotics cost rates* and set a date effective range.</span></span>
2. <span data-ttu-id="dbbd3-163">Konfigurer satser i kostpriselisten ved hjælp af oplysninger fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-163">In the cost price list, set up rates using information from the following table.</span></span> 

| <span data-ttu-id="dbbd3-164">Rolle</span><span class="sxs-lookup"><span data-stu-id="dbbd3-164">Role</span></span> | <span data-ttu-id="dbbd3-165">Ressourcevirksomhed</span><span class="sxs-lookup"><span data-stu-id="dbbd3-165">Resourcing Company</span></span> | <span data-ttu-id="dbbd3-166">Ressourceenhed</span><span class="sxs-lookup"><span data-stu-id="dbbd3-166">Resourcing Unit</span></span> | <span data-ttu-id="dbbd3-167">Omkostningssats</span><span class="sxs-lookup"><span data-stu-id="dbbd3-167">Cost rate</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="dbbd3-168">Udvikler</span><span class="sxs-lookup"><span data-stu-id="dbbd3-168">Developer</span></span> | <span data-ttu-id="dbbd3-169">Fabrikam i Indien</span><span class="sxs-lookup"><span data-stu-id="dbbd3-169">Fabrikam India</span></span> | <span data-ttu-id="dbbd3-170">Fabrikam i Indien-Robotics</span><span class="sxs-lookup"><span data-stu-id="dbbd3-170">Fabrikam India-Robotics</span></span> | <span data-ttu-id="dbbd3-171">100 $</span><span class="sxs-lookup"><span data-stu-id="dbbd3-171">$100</span></span> |
| <span data-ttu-id="dbbd3-172">Udvikler</span><span class="sxs-lookup"><span data-stu-id="dbbd3-172">Developer</span></span> | <span data-ttu-id="dbbd3-173">Fabrikam i Filippinerne</span><span class="sxs-lookup"><span data-stu-id="dbbd3-173">Fabrikam Philippines</span></span> | <span data-ttu-id="dbbd3-174">Fabrikam i Filippinerne-Robotics</span><span class="sxs-lookup"><span data-stu-id="dbbd3-174">Fabrikam Philippines-Robotics</span></span> | <span data-ttu-id="dbbd3-175">90 $</span><span class="sxs-lookup"><span data-stu-id="dbbd3-175">$90</span></span> |
| <span data-ttu-id="dbbd3-176">Udvikler</span><span class="sxs-lookup"><span data-stu-id="dbbd3-176">Developer</span></span> | <span data-ttu-id="dbbd3-177">Fabrikam i USA</span><span class="sxs-lookup"><span data-stu-id="dbbd3-177">Fabrikam US</span></span> | <span data-ttu-id="dbbd3-178">Fabrikam i USA-Robotics</span><span class="sxs-lookup"><span data-stu-id="dbbd3-178">Fabrikam US-Robotics</span></span> | <span data-ttu-id="dbbd3-179">150 $</span><span class="sxs-lookup"><span data-stu-id="dbbd3-179">$150</span></span> |

3. <span data-ttu-id="dbbd3-180">Knyt denne kostprisliste til organisationsenheden Fabrikam Robotics i USA.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-180">Attach this cost price list to the Fabrikam US-Robotics organization unit.</span></span>

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a><span data-ttu-id="dbbd3-181">Konfigurer prisfastsættelse af overførsler for en ressource i den relevante valuta</span><span class="sxs-lookup"><span data-stu-id="dbbd3-181">Set up transfer pricing for a resource in the appropriate currency</span></span> 

<span data-ttu-id="dbbd3-182">I Project Operations er det muligt at konfigurere prisfastsættelse af ressourcer i alle valutaer.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-182">In Project Operations, resource pricing can be set up in any currency.</span></span> <span data-ttu-id="dbbd3-183">Valutaen er som standard angivet til det, der er angivet i prislistens overskriften, men den kan ændres.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-183">The currency defaults to what is on the price list header, but can be changed.</span></span>

<span data-ttu-id="dbbd3-184">Når eksemplet med overførselspriser er konfigureret, kan oplysningerne ændres til:</span><span class="sxs-lookup"><span data-stu-id="dbbd3-184">Using the example for transfer price set up, the information could be changed to:</span></span>

<span data-ttu-id="dbbd3-185">Fabrikam-koncernen skal at Fabrikam Robotics i Indien har forhandlet en omkostningssats med Fabrikam Robotics i USA eller Fabrikam Robotics i Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-185">Fabrikam corporation must ensure that Fabrikam India-Robotics has a negotiated a cost rate with Fabrikam US-Robotics or Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="dbbd3-186">En udvikler fra Fabrikam Robotics i Indien koster 5.000 INR, når denne udlånes til Fabrikam Robotics i USA, og 5.500 INR, når denne udlånes til Fabrikam Robotics i Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-186">A developer from Fabrikam India-Robotics costs 5000 INR when lent to Fabrikam US-Robotics and 5500 INR when lent to Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="dbbd3-187">På kostprislisten for Fabrikam i USA-Robotics kan omkostningssatser udtrykkes som:</span><span class="sxs-lookup"><span data-stu-id="dbbd3-187">In the cost price list for Fabrikam US-Robotics, cost rates can be expressed as:</span></span>

| <span data-ttu-id="dbbd3-188">Rolle</span><span class="sxs-lookup"><span data-stu-id="dbbd3-188">Role</span></span> | <span data-ttu-id="dbbd3-189">Ressourcevirksomhed</span><span class="sxs-lookup"><span data-stu-id="dbbd3-189">Resourcing Company</span></span> | <span data-ttu-id="dbbd3-190">Omkostning</span><span class="sxs-lookup"><span data-stu-id="dbbd3-190">Cost</span></span> |
| --- | --- | --- |
| <span data-ttu-id="dbbd3-191">Udvikler</span><span class="sxs-lookup"><span data-stu-id="dbbd3-191">Developer</span></span> | <span data-ttu-id="dbbd3-192">Fabrikam i Indien</span><span class="sxs-lookup"><span data-stu-id="dbbd3-192">Fabrikam India</span></span> | <span data-ttu-id="dbbd3-193">5.000 INR</span><span class="sxs-lookup"><span data-stu-id="dbbd3-193">5000 INR</span></span> |
| <span data-ttu-id="dbbd3-194">Udvikler</span><span class="sxs-lookup"><span data-stu-id="dbbd3-194">Developer</span></span> | <span data-ttu-id="dbbd3-195">Fabrikam i USA</span><span class="sxs-lookup"><span data-stu-id="dbbd3-195">Fabrikam US</span></span> | <span data-ttu-id="dbbd3-196">115 USD</span><span class="sxs-lookup"><span data-stu-id="dbbd3-196">115 USD</span></span> |

<span data-ttu-id="dbbd3-197">På kostprislisten for Fabrikam i Storbritannien-Robotics kan omkostningssatser udtrykkes som nedenfor angivet:</span><span class="sxs-lookup"><span data-stu-id="dbbd3-197">In the cost price list for Fabrikam UK-Robotics, cost rates can be expressed below:</span></span>

| <span data-ttu-id="dbbd3-198">Rolle</span><span class="sxs-lookup"><span data-stu-id="dbbd3-198">Role</span></span> | <span data-ttu-id="dbbd3-199">Ressourcevirksomhed</span><span class="sxs-lookup"><span data-stu-id="dbbd3-199">Resourcing company</span></span> | <span data-ttu-id="dbbd3-200">Omkostning</span><span class="sxs-lookup"><span data-stu-id="dbbd3-200">Cost</span></span> |
| --- | --- | --- |
| <span data-ttu-id="dbbd3-201">Udvikler</span><span class="sxs-lookup"><span data-stu-id="dbbd3-201">Developer</span></span> | <span data-ttu-id="dbbd3-202">Fabrikam i Indien</span><span class="sxs-lookup"><span data-stu-id="dbbd3-202">Fabrikam India</span></span> | <span data-ttu-id="dbbd3-203">5.500 INR</span><span class="sxs-lookup"><span data-stu-id="dbbd3-203">5500 INR</span></span> |
| <span data-ttu-id="dbbd3-204">Udvikler</span><span class="sxs-lookup"><span data-stu-id="dbbd3-204">Developer</span></span> | <span data-ttu-id="dbbd3-205">Fabrikam i Storbritannien</span><span class="sxs-lookup"><span data-stu-id="dbbd3-205">Fabrikam UK</span></span> | <span data-ttu-id="dbbd3-206">115 GBP</span><span class="sxs-lookup"><span data-stu-id="dbbd3-206">115 GBP</span></span> |

<span data-ttu-id="dbbd3-207">Kostprislisten kan levere satser for arbejdskraft i flere valutaer.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-207">The cost price list can provide labor rates in multiple currencies.</span></span> <span data-ttu-id="dbbd3-208">Når der genereres et omkostningsestimat for projektet, konverterer Project Operations disse omkostningssatser til projektvalutaen og viser dem til brugeren.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-208">When generating a cost estimate on the project, Project Operations will convert these cost rates into the project currency and display it to the user.</span></span> <span data-ttu-id="dbbd3-209">Når en tidsregistrering godkendes, og der oprettes et faktisk omkostningsbeløb, prisfastsættes den faktiske omkostning i den valuta, der gælder for den tilsvarende rolleprislinje på kostprislisten.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-209">When a time entry is approved and a cost actual is created, the cost actual is priced in the currency of that matching role price line on the cost price list.</span></span> <span data-ttu-id="dbbd3-210">Faktiske omkostninger for tid på et enkelt projekt kan registreres i flere valutaer.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-210">Cost actuals for time on a single project can be recorded in multiple currencies.</span></span> <span data-ttu-id="dbbd3-211">Når Project Operations akkumulerer eller opsummerer de faktiske omkostninger til arbejdskraft på projektniveau, konverteres alle omkostninger til arbejdskraft til projektvalutaen, som brugeren kan få vist.</span><span class="sxs-lookup"><span data-stu-id="dbbd3-211">However, when rolling up or summarizing the actual labor costs at the project level, Project Operations will convert all labor cost amounts into the project currency, which the user can view.</span></span>