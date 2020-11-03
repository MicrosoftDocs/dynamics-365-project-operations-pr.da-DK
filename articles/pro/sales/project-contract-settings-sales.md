---
title: Projektkontraktfelter og -oplysninger
description: Dette emne indeholder oplysninger om de felter, der påvirker kontraktlinjer, og de oplysninger om kontrakten, der opsummeres på tværs af alle linjeelementer.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 082292c54682022933a4b46b856f9241078a9067
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087864"
---
# <a name="project-contract-fields-and-information"></a><span data-ttu-id="f9c3c-103">Projektkontraktfelter og -oplysninger</span><span class="sxs-lookup"><span data-stu-id="f9c3c-103">Project contract fields and information</span></span> 

<span data-ttu-id="f9c3c-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="f9c3c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f9c3c-105">Dette emne indeholder oplysninger om de felter, der gælder for hele projektkontrakten, herunder de indstillinger, der påvirker alle kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-105">This topic provides information about fields that apply to the entire project contract including settings that impact all contract lines.</span></span> <span data-ttu-id="f9c3c-106">Der medtages også oplysninger om den kontrakt, der opsummeres på tværs af alle de linjeelementer, der skal bruges til at anspore nøgletallene i projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-106">Information about the contract that is summarized across all the line items to drive KPIs of the project contract is also included.</span></span>

<span data-ttu-id="f9c3c-107">I følgende tabel vises felterne for en projektkontrakt, der er entydige for Dynamics 365 Project Operations, eller som har nogle vigtige ændringer i funktionsmåden i forhold til salgsordrer i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-107">The following table lists the fields on a project contract that are unique to Dynamics 365 Project Operations or have some important changes in behavior from sales orders in Dynamics 365 Sales.</span></span>

| <span data-ttu-id="f9c3c-108">Felt</span><span class="sxs-lookup"><span data-stu-id="f9c3c-108">Field</span></span> | <span data-ttu-id="f9c3c-109">Lokation</span><span class="sxs-lookup"><span data-stu-id="f9c3c-109">Location</span></span> | <span data-ttu-id="f9c3c-110">Relevans, formål og vejledning</span><span class="sxs-lookup"><span data-stu-id="f9c3c-110">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="f9c3c-111">Downstream-virkning</span><span class="sxs-lookup"><span data-stu-id="f9c3c-111">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="f9c3c-112">Skriv</span><span class="sxs-lookup"><span data-stu-id="f9c3c-112">Type</span></span> | <span data-ttu-id="f9c3c-113">Fanen **Oversigt** (skjult)</span><span class="sxs-lookup"><span data-stu-id="f9c3c-113">**Summary** tab (hidden)</span></span> | <span data-ttu-id="f9c3c-114">Dette er et grupperet indstillingsfelt med følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f9c3c-114">This is an option set field with the following options:</span></span></br><span data-ttu-id="f9c3c-115">- **Arbejdsbaseret** (kun tilgængelig, når Project Operations er installeret)</span><span class="sxs-lookup"><span data-stu-id="f9c3c-115">- **Work-based** (Available only when Project Operations is installed)</span></span></br><span data-ttu-id="f9c3c-116">- **Enhedsbaseret** (kun tilgængelig, når Project Operations og Sales er installeret)</span><span class="sxs-lookup"><span data-stu-id="f9c3c-116">- **Item-based** (Available only when Project Operations and Sales are installed)</span></span></br><span data-ttu-id="f9c3c-117">- **Servicevedligeholdelsesbaseret** (tilgængelig, når Dynamics 365 Field Service er installeret)</span><span class="sxs-lookup"><span data-stu-id="f9c3c-117">- **Service Maintenance-based** (Available when Dynamics 365 Field Service is installed)</span></span> | <span data-ttu-id="f9c3c-118">I Project Operations er værdien i dette felt som standard **Arbejdsbaseret** og klassificerer kontrakten som en projektbaseret kontrakt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-118">In Project Operations, the value of this field defaults to **Work-based** and classifies the contract as a project-based contract.</span></span> <span data-ttu-id="f9c3c-119">En kontrakt skal være projektbaseret, for at alle projektspecifikke udvidelser og funktioner kan aktiveres.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-119">A contract should be project-based to enable all project-specific extensions and functionality.</span></span> |
| <span data-ttu-id="f9c3c-120">Kundeemne</span><span class="sxs-lookup"><span data-stu-id="f9c3c-120">Potential Customer</span></span> | <span data-ttu-id="f9c3c-121">Fanen **Oversigt**</span><span class="sxs-lookup"><span data-stu-id="f9c3c-121">**Summary** tab</span></span> | <span data-ttu-id="f9c3c-122">Referencen til kundernes firma eller firmapost.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-122">The reference to the customers company or account record.</span></span> <span data-ttu-id="f9c3c-123">Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-123">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="f9c3c-124">Valutaen i projektkontrakten angives som standard på grundlag af kundens valuta.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-124">The currency on the project contract defaults based on the currency of the customer.</span></span> <span data-ttu-id="f9c3c-125">Dette kan ændres, før kontrakten er blevet gemt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-125">This can be changed before the contract is saved.</span></span> |
| <span data-ttu-id="f9c3c-126">Account manager</span><span class="sxs-lookup"><span data-stu-id="f9c3c-126">Account Manager</span></span> | <span data-ttu-id="f9c3c-127">Fanen **Oversigt**</span><span class="sxs-lookup"><span data-stu-id="f9c3c-127">**Summary** tab</span></span> | <span data-ttu-id="f9c3c-128">Navnet på account manageren for denne handel.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-128">The name of the Account Manager for this deal.</span></span> <span data-ttu-id="f9c3c-129">Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-129">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="f9c3c-130">Account manageren er ansvarlig for at administrere relationen til kunden ved at fuldføre projektet.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-130">The Account Manager is responsible for managing the relationship with the customer through the completion of the project.</span></span> <span data-ttu-id="f9c3c-131">På basis af den reserverbare ressourcepost, der er knyttet til account manageren, angives standarden for kontraktenheden på projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-131">Based on the bookable resource record tied to the Account Manager, the contracting unit defaults on the project contract.</span></span> |
| <span data-ttu-id="f9c3c-132">Kontraktenhed</span><span class="sxs-lookup"><span data-stu-id="f9c3c-132">Contracting Unit</span></span> | <span data-ttu-id="f9c3c-133">Fanen **Oversigt**</span><span class="sxs-lookup"><span data-stu-id="f9c3c-133">**Summary** tab</span></span> | <span data-ttu-id="f9c3c-134">Den organisationsenhed, der er ansvarlig for leveringen af de projekter, der er knyttet til denne kontrakt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-134">The organization unit responsible for the delivery of the projects associated with this contract.</span></span> <span data-ttu-id="f9c3c-135">Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-135">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="f9c3c-136">Kontraktenheden er afdelingen i det firma, der udfører projekterne.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-136">The contracting unit is the division of the company that executes the projects.</span></span> <span data-ttu-id="f9c3c-137">Alle kontraherende enheder har en valuta, og denne valuta bruges til at rapportere de anslåede og faktiske omkostninger, der er påløbet i løbet af projektet.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-137">Every contracting unit has a currency, and this currency is used to report estimated and actual costs incurred during the project.</span></span> |
| <span data-ttu-id="f9c3c-138">Produktprisliste</span><span class="sxs-lookup"><span data-stu-id="f9c3c-138">Product Price List</span></span> | <span data-ttu-id="f9c3c-139">Fanen **Oversigt**</span><span class="sxs-lookup"><span data-stu-id="f9c3c-139">**Summary** tab</span></span> | <span data-ttu-id="f9c3c-140">Denne prisliste bruges som standard for priser i produktbaserede kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-140">This price list is used to default prices on product-based contract lines.</span></span> <span data-ttu-id="f9c3c-141">Listen over indstillinger i rullemenuen for dette felt indeholder en liste over prislister, hvor valutaen for prislisten stemmer overens med valutaen i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-141">The list of drop-down options for this field shows a list of price lists where the price list currency matches the currency on the contract.</span></span> <span data-ttu-id="f9c3c-142">Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-142">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> <span data-ttu-id="f9c3c-143">I projektkontrakten er dette felt som standard hentet fra firmaposten, men den kan ændres.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-143">On the project contract, this field is defaulted from the account record but can be changed.</span></span> | <span data-ttu-id="f9c3c-144">Dette felt har ingen afledt relevans.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-144">There is no downstream relevance for this field.</span></span> |
| <span data-ttu-id="f9c3c-145">Valuta</span><span class="sxs-lookup"><span data-stu-id="f9c3c-145">Currency</span></span> | <span data-ttu-id="f9c3c-146">Fanen **Oversigt**</span><span class="sxs-lookup"><span data-stu-id="f9c3c-146">**Summary** tab</span></span> | <span data-ttu-id="f9c3c-147">Den valuta, der bruges til at rapportere værdien i denne handel, samt den valuta, som kunden bliver faktureret i.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-147">The currency used to report the value of this deal and the currency in which the customer will be invoiced.</span></span> <span data-ttu-id="f9c3c-148">Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-148">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> <span data-ttu-id="f9c3c-149">I projektkontrakten hentes dette felt som standard fra firmaposten, men den kan ændres.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-149">On the project contract, this field defaults from the account record but can be changed.</span></span> | <span data-ttu-id="f9c3c-150">Når en kontrakt er gemt, kan du ikke længere redigere dette felt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-150">After a contract is saved, this field is no longer editable.</span></span> <span data-ttu-id="f9c3c-151">Dette felt anvendes som standard for produkt- og projektprislister på kontrakten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-151">This field is used to default the product and project price lists on the contract.</span></span> <span data-ttu-id="f9c3c-152">Valutaen på kontrakten anvendes til at periodisere valutaen på prislisten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-152">The currency on the contract is used to match the currency on the price list.</span></span> |
| <span data-ttu-id="f9c3c-153">Grænse, der ikke må overskrides</span><span class="sxs-lookup"><span data-stu-id="f9c3c-153">Not-to-Exceed Limit</span></span> | <span data-ttu-id="f9c3c-154">Fanen **Oversigt**</span><span class="sxs-lookup"><span data-stu-id="f9c3c-154">**Summary** tab</span></span> | <span data-ttu-id="f9c3c-155">Dette felt angiver den aftalte maksimumsværdi for den slutværdi, som kunden har indvilliget i at betale i forbindelse med denne aftale.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-155">This field indicates the negotiated cap on the final value that the customer has agreed to for this deal.</span></span> | <span data-ttu-id="f9c3c-156">Maksimumsværdien evalueres under udførelsen og er gældende på tværs af alle linjeelementer og projekter, der er knyttet til denne handel.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-156">The cap is evaluated during execution and is applicable across all line items and projects associated with this deal.</span></span> |
| <span data-ttu-id="f9c3c-157">Anmodet leveringsdato</span><span class="sxs-lookup"><span data-stu-id="f9c3c-157">Requested Delivery Date</span></span> | <span data-ttu-id="f9c3c-158">Fanen **Oversigt**</span><span class="sxs-lookup"><span data-stu-id="f9c3c-158">**Summary** tab</span></span> | <span data-ttu-id="f9c3c-159">Når en kontrakt oprettes ud fra et projekttilbud, kopieres dette felt fra det tilsvarende felt på projekttilbuddet.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-159">When a contract is created from a project quote, this field is copied from the corresponding field on the project quote.</span></span> | <span data-ttu-id="f9c3c-160">Denne dato bruges som slutdatoen for at generere fakturaplaner.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-160">This date is used as the end date to generate invoice schedules.</span></span> |

<span data-ttu-id="f9c3c-161">Følgende nøgletal er tilgængelige under fanen **Kontraktens ydeevne** i en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-161">The following KPIs are available on the **Contract Performance** tab of a project contract.</span></span>

| <span data-ttu-id="f9c3c-162">Felt</span><span class="sxs-lookup"><span data-stu-id="f9c3c-162">Field</span></span> | <span data-ttu-id="f9c3c-163">Lokation</span><span class="sxs-lookup"><span data-stu-id="f9c3c-163">Location</span></span> | <span data-ttu-id="f9c3c-164">Relevans, formål og vejledning</span><span class="sxs-lookup"><span data-stu-id="f9c3c-164">Relevance, purpose, and guidance</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f9c3c-165">Kontraktværdi</span><span class="sxs-lookup"><span data-stu-id="f9c3c-165">Contract Value</span></span> | <span data-ttu-id="f9c3c-166">Overordnet kontrakt</span><span class="sxs-lookup"><span data-stu-id="f9c3c-166">Overall contract</span></span> | <span data-ttu-id="f9c3c-167">Den samlede værdi af projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-167">The total value of the Project contract.</span></span> |
| <span data-ttu-id="f9c3c-168">Faktureret beløb</span><span class="sxs-lookup"><span data-stu-id="f9c3c-168">Billed Amount</span></span> | <span data-ttu-id="f9c3c-169">Overordnet kontrakt</span><span class="sxs-lookup"><span data-stu-id="f9c3c-169">Overall contract</span></span> | <span data-ttu-id="f9c3c-170">Summen af beløbene på alle fakturaer i forhold til denne kontrakt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-170">The sum of the amounts on all invoices against this contract.</span></span> |
| <span data-ttu-id="f9c3c-171">Påløbne omkostninger</span><span class="sxs-lookup"><span data-stu-id="f9c3c-171">Cost Incurred</span></span> | <span data-ttu-id="f9c3c-172">Overordnet kontrakt</span><span class="sxs-lookup"><span data-stu-id="f9c3c-172">Overall contract</span></span> | <span data-ttu-id="f9c3c-173">Summen af alle de faktiske omkostninger, der er logført i alle de projekter, som er knyttet til kontrakten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-173">The sum of all cost actuals logged on all projects that are mapped to the contract.</span></span> |
| <span data-ttu-id="f9c3c-174">Bruttoavance</span><span class="sxs-lookup"><span data-stu-id="f9c3c-174">Gross Margin</span></span> | <span data-ttu-id="f9c3c-175">Overordnet kontrakt</span><span class="sxs-lookup"><span data-stu-id="f9c3c-175">Overall contract</span></span> | <span data-ttu-id="f9c3c-176">Faktureret beløb – omkostninger, der er påløbet frem til dags dato/faktureret beløb</span><span class="sxs-lookup"><span data-stu-id="f9c3c-176">Billed amount - Cost incurred till date / Billed amount</span></span> |
| <span data-ttu-id="f9c3c-177">Anslået avance</span><span class="sxs-lookup"><span data-stu-id="f9c3c-177">Expected Margin</span></span> | <span data-ttu-id="f9c3c-178">Overordnet kontrakt</span><span class="sxs-lookup"><span data-stu-id="f9c3c-178">Overall contract</span></span> | <span data-ttu-id="f9c3c-179">(Kontraktværdi – estimerede omkostninger)/KontraktværdiEstimerede omkostninger = summen af alle estimerede omkostninger for alle projekter, der er knyttet til kontrakten.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-179">(Contract value - Estimated costs) / Contract valueEstimated costs = The sum of all estimated costs on all projects mapped to the contract.</span></span>|
| <span data-ttu-id="f9c3c-180">Kontraktværdi</span><span class="sxs-lookup"><span data-stu-id="f9c3c-180">Contract Value</span></span> | <span data-ttu-id="f9c3c-181">Projektbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-181">Project-based lines</span></span> | <span data-ttu-id="f9c3c-182">Værdien for kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-182">The value of the contract line.</span></span> |
| <span data-ttu-id="f9c3c-183">Faktureret beløb</span><span class="sxs-lookup"><span data-stu-id="f9c3c-183">Billed amount</span></span> | <span data-ttu-id="f9c3c-184">Projektbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-184">Project-based lines</span></span> | <span data-ttu-id="f9c3c-185">For kontraktlinjer med fast pris: Summen af beløbene på alle fakturerede milepæle for faktiske salgsværdier i forhold til denne kontraktlinje på de forskellige fakturaer, der er oprettet for denne kontrakt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-185">For fixed price contract line: The sum of the amounts on all billed sales milestone actuals against this contract line on various invoices created for this contract.</span></span> <span data-ttu-id="f9c3c-186">For kontraktlinjer med tid og materiale: Summen af beløbene på alle fakturerbare fakturerede faktiske salgsværdier i forhold til denne kontraktlinje på de forskellige fakturaer, der er oprettet for denne kontrakt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-186">For time and material contract line: The sum of the amounts on all chargeable billed sales actuals against this contract line on various invoices created for this contract.</span></span> |
| <span data-ttu-id="f9c3c-187">Påløbne omkostninger</span><span class="sxs-lookup"><span data-stu-id="f9c3c-187">Cost Incurred</span></span> | <span data-ttu-id="f9c3c-188">Projektbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-188">Project-based lines</span></span> | <span data-ttu-id="f9c3c-189">Summen af alle de faktiske omkostninger, der er logført i alle de projekter, som er knyttet til kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-189">The sum of all cost actuals logged on all projects mapped to the contract line.</span></span> |
| <span data-ttu-id="f9c3c-190">Bruttoavance</span><span class="sxs-lookup"><span data-stu-id="f9c3c-190">Gross Margin</span></span> | <span data-ttu-id="f9c3c-191">Projektbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-191">Project-based lines</span></span> | <span data-ttu-id="f9c3c-192">(Faktureret beløb – omkostninger, der er påløbet frem til dags dato) / Faktureret beløb</span><span class="sxs-lookup"><span data-stu-id="f9c3c-192">(Billed amount - Cost incurred till date) / Billed amount</span></span> |
| <span data-ttu-id="f9c3c-193">Anslået avance</span><span class="sxs-lookup"><span data-stu-id="f9c3c-193">Expected Margin</span></span> | <span data-ttu-id="f9c3c-194">Projektbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-194">Project-based lines</span></span> | <span data-ttu-id="f9c3c-195">(Beløb på kontraktlinje i grundvaluta – Estimerede omkostninger for kontraktlinjen i grundvaluta) / Beløb på kontraktlinje i grundvaluta</span><span class="sxs-lookup"><span data-stu-id="f9c3c-195">(Contract line amount in base currency - Estimated costs for the contract line in base currency) / Contract line amount in base currency</span></span> |
| <span data-ttu-id="f9c3c-196">Påløbne omkostninger</span><span class="sxs-lookup"><span data-stu-id="f9c3c-196">Cost Incurred</span></span> | <span data-ttu-id="f9c3c-197">Detaljer for en projektbaseret linje</span><span class="sxs-lookup"><span data-stu-id="f9c3c-197">Detail of a project-based line</span></span> | <span data-ttu-id="f9c3c-198">Tid: Summen af beløbet for faktiske tidsomkostninger logført for denne rolle på det projekt, der er knyttet til kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-198">Time: The sum of the amount on time cost actuals logged for this role on the project mapped to the contract line.</span></span> <span data-ttu-id="f9c3c-199">Udgifter: Summen af beløbet for faktiske udgiftsomkostninger logført for denne kategori på det projekt, der er knyttet til kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-199">Expenses: The sum of the amount on all expense cost actuals logged for this category on the project mapped to the contract line.</span></span> |
| <span data-ttu-id="f9c3c-200">Registreret antal</span><span class="sxs-lookup"><span data-stu-id="f9c3c-200">Logged Quantity</span></span> | <span data-ttu-id="f9c3c-201">Detaljer for en projektbaseret linje</span><span class="sxs-lookup"><span data-stu-id="f9c3c-201">Detail of a project-based line</span></span> | <span data-ttu-id="f9c3c-202">Tid: Mængden af samlede faktiske tidsomkostninger for en rolle på det projekt, der er knyttet til denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-202">Time: The quantity on total time cost actuals for a role on the project that is mapped to this contract line.</span></span> <span data-ttu-id="f9c3c-203">Udgifter: Alle mængder for denne udgiftskategori på de faktiske udgiftsomkostningsværdier på det projekt, der er knyttet til denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-203">Expenses: All quantities for this expense category on the expense cost actuals on the project are mapped to this contract line.</span></span> |
| <span data-ttu-id="f9c3c-204">Faktureret beløb</span><span class="sxs-lookup"><span data-stu-id="f9c3c-204">Billed Amount</span></span> | <span data-ttu-id="f9c3c-205">Detaljer for en projektbaseret linje</span><span class="sxs-lookup"><span data-stu-id="f9c3c-205">Detail of a project-based line</span></span> | <span data-ttu-id="f9c3c-206">Hvis der er tale om en kontraktlinje med fast pris, er dette felt tomt på detaljeniveau og vises kun på kontraktlinjeniveau.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-206">For a fixed price contract line, this field is left blank on the detail level and is only shown at the contract line level.</span></span> <span data-ttu-id="f9c3c-207">Hvis der er tale om en kontraktlinje med tid og materiale, udføres beregninger på detaljeniveau.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-207">For a time and material contract line, calculations are completed at the details level.</span></span> <span data-ttu-id="f9c3c-208">Detaljerne viser summen af beløbet på alle de fakturerede indtægtslinjer i forhold til denne kontraktlinje, som er fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-208">The details show the sum of the amount on all the billed revenue lines against this contract line that are chargeable.</span></span> |
| <span data-ttu-id="f9c3c-209">Faktureret antal</span><span class="sxs-lookup"><span data-stu-id="f9c3c-209">Billed Quantity</span></span> | <span data-ttu-id="f9c3c-210">Detaljer for en projektbaseret linje</span><span class="sxs-lookup"><span data-stu-id="f9c3c-210">Detail of a project-based line</span></span> | <span data-ttu-id="f9c3c-211">Hvis der er tale om en kontraktlinje med fast pris, er dette felt tomt på detaljeniveau og vises kun på kontraktlinjeniveau.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-211">For a fixed price contract line, this field is left blank on the detail level and is only shown at the contract line level.</span></span> <span data-ttu-id="f9c3c-212">Hvis der er tale om en kontraktlinje med tid og materiale, udføres beregninger på detaljeniveau for tid og udgifter.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-212">For a time and material contract line, calculations are completed at the details level for time and expenses.</span></span> <span data-ttu-id="f9c3c-213">Tid: Summen af antal timer på alle de fakturerede indtægtslinjer for denne rolle i forhold til denne kontraktlinje, som er fakturerbar.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-213">Time: The sum of the hours on all the billed revenue lines for this role against this contract line that are chargeable.</span></span> <span data-ttu-id="f9c3c-214">Udgifter: Alle mængder for denne udgiftskategori på de faktiske udgiftsomkostningsværdier på det projekt, der er knyttet til denne kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-214">Expenses: All quantities for this expense category on the expense cost actuals on the project are mapped to this contract line.</span></span> |
| <span data-ttu-id="f9c3c-215">Kontraktværdi</span><span class="sxs-lookup"><span data-stu-id="f9c3c-215">Contract Value</span></span> | <span data-ttu-id="f9c3c-216">Produktbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-216">Product-based lines</span></span> | <span data-ttu-id="f9c3c-217">Kontraktlinjeværdien for denne produktbaserede kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-217">The contract line value of this product-based contract line.</span></span> |
| <span data-ttu-id="f9c3c-218">Faktureret beløb</span><span class="sxs-lookup"><span data-stu-id="f9c3c-218">Billed Amount</span></span> | <span data-ttu-id="f9c3c-219">Produktbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-219">Product-based lines</span></span> | <span data-ttu-id="f9c3c-220">Summen af beløbene på alle fakturalinjer i forhold til denne produktbaserede kontraktlinje på forskellige fakturaer, der oprettes for denne kontrakt.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-220">The sum of the amounts on all invoice lines against this product-based contract line on various invoices that are created for this contract.</span></span> |
| <span data-ttu-id="f9c3c-221">Påløbne omkostninger</span><span class="sxs-lookup"><span data-stu-id="f9c3c-221">Cost Incurred</span></span> | <span data-ttu-id="f9c3c-222">Produktbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-222">Product-based lines</span></span> | <span data-ttu-id="f9c3c-223">Summen af alle de faktiske omkostninger for den produktbaserede kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="f9c3c-223">The sum of all cost actuals logged for the product-based contract line.</span></span> |
| <span data-ttu-id="f9c3c-224">Bruttoavance</span><span class="sxs-lookup"><span data-stu-id="f9c3c-224">Gross Margin</span></span> | <span data-ttu-id="f9c3c-225">Projektbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-225">Project-based lines</span></span> | <span data-ttu-id="f9c3c-226">Faktureret beløb – omkostninger, der er påløbet frem til dags dato/faktureret beløb</span><span class="sxs-lookup"><span data-stu-id="f9c3c-226">Billed amount - Cost incurred till date / Billed amount</span></span> |
| <span data-ttu-id="f9c3c-227">Anslået avance</span><span class="sxs-lookup"><span data-stu-id="f9c3c-227">Expected Margin</span></span> | <span data-ttu-id="f9c3c-228">Produktbaserede linjer</span><span class="sxs-lookup"><span data-stu-id="f9c3c-228">Product-based lines</span></span> | <span data-ttu-id="f9c3c-229">(Kontraktlinjeværdi - estimerede omkostninger for kontraktlinjen) / Kontraktlinjeværdi</span><span class="sxs-lookup"><span data-stu-id="f9c3c-229">(Contract line value - Estimated costs for the contract line) / Contract line value</span></span> |