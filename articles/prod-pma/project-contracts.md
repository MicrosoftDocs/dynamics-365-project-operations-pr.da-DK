---
title: Projektkontrakter
description: Dette emne giver eksempler på de projektkontrakter, som du kan oprette til forskellige typer projekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere projektkunder.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999754"
---
# <a name="project-contracts"></a><span data-ttu-id="4215b-103">Projektkontrakter</span><span class="sxs-lookup"><span data-stu-id="4215b-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4215b-104">Denne artikel giver eksempler på de projektkontrakter, som du kan oprette til forskellige typer projekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere projektkunder.</span><span class="sxs-lookup"><span data-stu-id="4215b-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="4215b-105">Projekttypen, som du har oprettet for en projektkontrakt, bestemmer den metode, der bruges til at fakturere projektkunder.</span><span class="sxs-lookup"><span data-stu-id="4215b-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="4215b-106">Du kan ændre en projektkontrakt og det relaterede projekt, men du kan ikke ændre projekttypen.</span><span class="sxs-lookup"><span data-stu-id="4215b-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="4215b-107">Ved hjælp af en projektkontrakt kan du fakturere et eller flere projekter på samme tid.</span><span class="sxs-lookup"><span data-stu-id="4215b-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="4215b-108">Projektkontrakten er også med til at sikre en ensartet faktureringsprocedure for alle underprojekter i en projektstruktur.</span><span class="sxs-lookup"><span data-stu-id="4215b-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="4215b-109">Alle de projekter, der skal faktureres, skal knyttes til en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="4215b-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="4215b-110">Indstillingerne for en projektkontrakt gælder for alle projekter og underprojekter, der er knyttet til den pågældende projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="4215b-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="4215b-111">En projektkontrakt kan angive en eller flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="4215b-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="4215b-112">Du kan derfor opdele faktureringen mellem flere finansieringskilder, konfigurere finansieringsgrænser, så finansieringskilder ikke faktureres mere end et bestemt beløb, og konfigurere finansieringsregler for opkrævning af udgifter.</span><span class="sxs-lookup"><span data-stu-id="4215b-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="4215b-113">Finansiering til projektkontrakter</span><span class="sxs-lookup"><span data-stu-id="4215b-113">Funding for project contracts</span></span>
<span data-ttu-id="4215b-114">Nogle projektkontrakter angiver, at flere parter deler ansvaret for finansieringen af projektomkostningerne.</span><span class="sxs-lookup"><span data-stu-id="4215b-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="4215b-115">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="4215b-115">Here are some examples:</span></span>

-   <span data-ttu-id="4215b-116">En stor kunde, der har flere inddelinger, anmoder om, at finansieringen af et projekt opdeles efter division.</span><span class="sxs-lookup"><span data-stu-id="4215b-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="4215b-117">Din virksomhed deler omkostningerne ved et stort projekt med en ekstern organisation.</span><span class="sxs-lookup"><span data-stu-id="4215b-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="4215b-118">Et vejprojekt samfinansieres af to kommuner.</span><span class="sxs-lookup"><span data-stu-id="4215b-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="4215b-119">Et bro-projekt finansieres af statsstøtte og en privat virksomhed.</span><span class="sxs-lookup"><span data-stu-id="4215b-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="4215b-120">I Dynamics 365 Finance kan du dele faktureringen for en enkelt transaktion eller et helt projekt op mellem flere kunder, tilskud eller organisationer.</span><span class="sxs-lookup"><span data-stu-id="4215b-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="4215b-121">I projekter, der har flere finansieringskilder, kaldes alle de parter, der bidrager til finansieringen af et avanceret finansieringsprojekt, også for finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="4215b-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="4215b-122">Når en kunde, en organisation eller et tilskud er defineret som en finansieringskilde, kan den tildeles en eller flere finansieringsregler.</span><span class="sxs-lookup"><span data-stu-id="4215b-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="4215b-123">Finansieringsregler indeholder de kriterier, der bestemmer, hvordan opkrævninger tildeles de forskellige finansieringskilder i et projekt.</span><span class="sxs-lookup"><span data-stu-id="4215b-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="4215b-124">Da lagervarer, såsom dem, der vises på indkøbsrekvisitioner og indkøbsordrer, ikke kan opdeles, kan omkostningsbeløbet ikke deles op mellem flere finansieringskilder på distributionstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="4215b-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="4215b-125">Finansieringskildens værdi forbliver derfor 0 (nul), indtil lagerfejlen er bogført.</span><span class="sxs-lookup"><span data-stu-id="4215b-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="4215b-126">Når lagerfejlen bogføres, fordeles omkostningsbeløbet i henhold til projektets distributionsregler for kontoen.</span><span class="sxs-lookup"><span data-stu-id="4215b-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="4215b-127">Her er nogle trin, du kan udføre for at gøre det nemmere at dele faktureringen op mellem flere finansieringskilder:</span><span class="sxs-lookup"><span data-stu-id="4215b-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="4215b-128">Specificer, at alle de transaktioner, der angives for et projekt, skal bruge samme salgsvaluta som projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="4215b-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="4215b-129">Opret finansieringslofter, så en finansieringskilde ikke faktureres mere end et bestemt beløb i et projekt.</span><span class="sxs-lookup"><span data-stu-id="4215b-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="4215b-130">Konfigurer finansieringsregler og finansieringslofter for hver arbejder, vare, kategori, kategorigruppe og transaktionstype (eller for alle transaktionstyper).</span><span class="sxs-lookup"><span data-stu-id="4215b-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="4215b-131">Vælg valgfrie start- og slutdatoer for at definere den periode, hvor de enkelte finansieringsregler er gyldige.</span><span class="sxs-lookup"><span data-stu-id="4215b-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="4215b-132">Angiv den procentdel, som hver finansieringskilde er ansvarlig for.</span><span class="sxs-lookup"><span data-stu-id="4215b-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="4215b-133">Angiv, hvilken finansieringskilde der er ansvarlig for afrundingsdifferencer, som forårsages af beregninger af finansieringsallokering.</span><span class="sxs-lookup"><span data-stu-id="4215b-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="4215b-134">Konfigurer regler, der bestemmer, hvordan eksterne kunder faktureres for projektomkostninger, og disse opkræves ved interne organisationer.</span><span class="sxs-lookup"><span data-stu-id="4215b-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="4215b-135">Registrer transaktioner på en afventende finansieringskonto, indtil der kan opnås yderligere finansiering, eller indtil du beslutter dig for at bære omkostningerne internt.</span><span class="sxs-lookup"><span data-stu-id="4215b-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="4215b-136">Der søges efter en momsgruppetildeling i projektet for at afgøre, hvilken momsgruppe der skal knyttes til en transaktion.</span><span class="sxs-lookup"><span data-stu-id="4215b-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="4215b-137">Hvis der ikke er foretaget nogen momsgruppetildeling på projektniveau, søges der i projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="4215b-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="4215b-138">Eksempel: flere finansieringskilder (simpel)</span><span class="sxs-lookup"><span data-stu-id="4215b-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="4215b-139">Følgende tabel indeholder scenarier til administration af finansieringsallokering mellem flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="4215b-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="4215b-140">Disse scenarier er baseret på følgende forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="4215b-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="4215b-141">Prioritetsindstillingerne indregnes i allokeringen af midler, før andre finansieringsregelkriterier anvendes.</span><span class="sxs-lookup"><span data-stu-id="4215b-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="4215b-142">Der er ikke angivet noget datointerval for at definere perioden d, når finansieringsreglen er gyldig.</span><span class="sxs-lookup"><span data-stu-id="4215b-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4215b-143"><strong>Scenarie</strong></span><span class="sxs-lookup"><span data-stu-id="4215b-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="4215b-144"><strong>Finansieringskilde</strong></span><span class="sxs-lookup"><span data-stu-id="4215b-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="4215b-145"><strong>Fordelingsprocent</strong></span><span class="sxs-lookup"><span data-stu-id="4215b-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="4215b-146"><strong>Fordelingsprioritet</strong></span><span class="sxs-lookup"><span data-stu-id="4215b-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4215b-147">Hvis du vil tildele omkostninger til én finansieringskilde, indtil midlerne er opbrugt, skal du fordele omkostningerne til en anden finansieringskilde, indtil dennes midler er opbrugt, og endelig tildele de resterende omkostninger til en tredje finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="4215b-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4215b-148">Finansieringskilde 1</span><span class="sxs-lookup"><span data-stu-id="4215b-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="4215b-149">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="4215b-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="4215b-150">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="4215b-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4215b-151">100%</span><span class="sxs-lookup"><span data-stu-id="4215b-151">100%</span></span></li>
<li><span data-ttu-id="4215b-152">100%</span><span class="sxs-lookup"><span data-stu-id="4215b-152">100%</span></span></li>
<li><span data-ttu-id="4215b-153">100%</span><span class="sxs-lookup"><span data-stu-id="4215b-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4215b-154">1</span><span class="sxs-lookup"><span data-stu-id="4215b-154">1</span></span></li>
<li><span data-ttu-id="4215b-155">2</span><span class="sxs-lookup"><span data-stu-id="4215b-155">2</span></span></li>
<li><span data-ttu-id="4215b-156">3</span><span class="sxs-lookup"><span data-stu-id="4215b-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4215b-157">Du vil tildele 75 procent af omkostningerne til én finansieringskilde og 25 procent til en anden finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="4215b-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="4215b-158">Når en af disse finansieringskilder er opbrugt, vil du betale de resterende omkostninger fra en tredje finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="4215b-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4215b-159">Finansieringskilde 1</span><span class="sxs-lookup"><span data-stu-id="4215b-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="4215b-160">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="4215b-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="4215b-161">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="4215b-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4215b-162">75 %</span><span class="sxs-lookup"><span data-stu-id="4215b-162">75%</span></span></li>
<li><span data-ttu-id="4215b-163">25 %</span><span class="sxs-lookup"><span data-stu-id="4215b-163">25%</span></span></li>
<li><span data-ttu-id="4215b-164">100%</span><span class="sxs-lookup"><span data-stu-id="4215b-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4215b-165">1</span><span class="sxs-lookup"><span data-stu-id="4215b-165">1</span></span></li>
<li><span data-ttu-id="4215b-166">1</span><span class="sxs-lookup"><span data-stu-id="4215b-166">1</span></span></li>
<li><span data-ttu-id="4215b-167">2</span><span class="sxs-lookup"><span data-stu-id="4215b-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4215b-168">Du vil tildele 75 procent af omkostningerne til én finansieringskilde og 25 procent til en anden finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="4215b-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="4215b-169">Når en af disse finansieringskilder er opbrugt, vil du dele de resterende omkostninger op mellem en tredje og en fjerde finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="4215b-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4215b-170">Finansieringskilde 1</span><span class="sxs-lookup"><span data-stu-id="4215b-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="4215b-171">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="4215b-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="4215b-172">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="4215b-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="4215b-173">Finansieringskilde 4</span><span class="sxs-lookup"><span data-stu-id="4215b-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4215b-174">75 %</span><span class="sxs-lookup"><span data-stu-id="4215b-174">75%</span></span></li>
<li><span data-ttu-id="4215b-175">25 %</span><span class="sxs-lookup"><span data-stu-id="4215b-175">25%</span></span></li>
<li><span data-ttu-id="4215b-176">50 %</span><span class="sxs-lookup"><span data-stu-id="4215b-176">50%</span></span></li>
<li><span data-ttu-id="4215b-177">50 %</span><span class="sxs-lookup"><span data-stu-id="4215b-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4215b-178">1</span><span class="sxs-lookup"><span data-stu-id="4215b-178">1</span></span></li>
<li><span data-ttu-id="4215b-179">1</span><span class="sxs-lookup"><span data-stu-id="4215b-179">1</span></span></li>
<li><span data-ttu-id="4215b-180">2</span><span class="sxs-lookup"><span data-stu-id="4215b-180">2</span></span></li>
<li><span data-ttu-id="4215b-181">2</span><span class="sxs-lookup"><span data-stu-id="4215b-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4215b-182">Du vil tildele de første 25 procent af omkostningerne til én finansieringskilde og de resterende til en anden finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="4215b-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4215b-183">Finansieringskilde 1</span><span class="sxs-lookup"><span data-stu-id="4215b-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="4215b-184">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="4215b-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4215b-185">25 %</span><span class="sxs-lookup"><span data-stu-id="4215b-185">25%</span></span></li>
<li><span data-ttu-id="4215b-186">100%</span><span class="sxs-lookup"><span data-stu-id="4215b-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4215b-187">1</span><span class="sxs-lookup"><span data-stu-id="4215b-187">1</span></span></li>
<li><span data-ttu-id="4215b-188">2</span><span class="sxs-lookup"><span data-stu-id="4215b-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="4215b-189">Eksempel: flere finansieringskilder (kompleks)</span><span class="sxs-lookup"><span data-stu-id="4215b-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="4215b-190">Du har tre finansieringskilder, som du vil bruge i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="4215b-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="4215b-191">Brug finansieringskilde 2 og finansieringskilde 3 ligeligt, indtil finansieringskilde 2 er udtømt.</span><span class="sxs-lookup"><span data-stu-id="4215b-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="4215b-192">Fortsæt med at bruge finansieringskilde 3, indtil den er tømt.</span><span class="sxs-lookup"><span data-stu-id="4215b-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="4215b-193">Brug finansieringskilde 1, når finansieringskilde 3 er udtømt.</span><span class="sxs-lookup"><span data-stu-id="4215b-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="4215b-194">For at opnå dette skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="4215b-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="4215b-195">Opret finansieringslofter for finansieringskilde 2 og finansieringskilde 3 i henhold til deres respektive beløb.</span><span class="sxs-lookup"><span data-stu-id="4215b-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="4215b-196">Opret følgende finansieringsregler:</span><span class="sxs-lookup"><span data-stu-id="4215b-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="4215b-197">Regel 1 (prioritet 1): tildel 50 procent af transaktioner til finansieringskilde 2 og 50 procent til finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="4215b-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="4215b-198">Regel 2 (prioritet 2): tildel 100 procent af transaktioner til finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="4215b-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="4215b-199">Regel 3 (prioritet 3): tildel 100 procent af transaktioner til finansieringskilde 1.</span><span class="sxs-lookup"><span data-stu-id="4215b-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="4215b-200">Denne opsætning virker, fordi transaktionerne holdes op imod regler og begrænsninger for at afgøre, om nogen af dem gælder for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="4215b-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="4215b-201">Hvis der ikke gælder nogen specifikke regler eller grænser for transaktionen, gælder reglen for alle transaktioner.</span><span class="sxs-lookup"><span data-stu-id="4215b-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="4215b-202">Reglen for alle transaktioner passer til alle transaktioner.</span><span class="sxs-lookup"><span data-stu-id="4215b-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="4215b-203">Hvis der findes en regel, der passer til en transaktion, anvendes den procentdel, der er allokeret i reglen, først, men først efter at de pågældende matches er blevet holdt op imod eventuelle grænser, der er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="4215b-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="4215b-204">Hvis en grænse er overskredet, og en finansieringskildes midler er opbrugt, ignoreres finansieringsreglen, der er knyttet til finansieringsloftet, og programmet søger efter den næste regel, der gælder.</span><span class="sxs-lookup"><span data-stu-id="4215b-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="4215b-205">I visse tilfælde kan kun en del af en transaktion allokeres i henhold til en regel.</span><span class="sxs-lookup"><span data-stu-id="4215b-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="4215b-206">Dette kan ske, hvis en grænse nås, når transaktionen allokeres.</span><span class="sxs-lookup"><span data-stu-id="4215b-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="4215b-207">I dette tilfælde er det kun et bestemt beløb, der allokeres i henhold til den pågældende regel, f.eks. 50 procent, til hver enkelt finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="4215b-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="4215b-208">Dette er tilfældet i regel 1, der er beskrevet ovenfor i dette sektion.</span><span class="sxs-lookup"><span data-stu-id="4215b-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="4215b-209">Resten allokeres efter den næste regel i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="4215b-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="4215b-210">Den følgende tabel undersøger dette scenarie mere detaljeret.</span><span class="sxs-lookup"><span data-stu-id="4215b-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4215b-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="4215b-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="4215b-212"><strong>Detaljer</strong></span><span class="sxs-lookup"><span data-stu-id="4215b-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4215b-213">Finansieringsregler</span><span class="sxs-lookup"><span data-stu-id="4215b-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="4215b-214">Regel 1 (prioritet 1): alle transaktioner.</span><span class="sxs-lookup"><span data-stu-id="4215b-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="4215b-215">Tildel finansieringskilde 2 ved 50 % og finansieringskilde 3 ved 50 %.</span><span class="sxs-lookup"><span data-stu-id="4215b-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="4215b-216">Regel 2 (prioritet 2): alle transaktioner.</span><span class="sxs-lookup"><span data-stu-id="4215b-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="4215b-217">Tildel finansieringskilde 3 ved 100 %.</span><span class="sxs-lookup"><span data-stu-id="4215b-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="4215b-218">Regel 3 (prioritet 2): alle transaktioner.</span><span class="sxs-lookup"><span data-stu-id="4215b-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="4215b-219">Tildel finansieringskilde 1 ved 100 %.</span><span class="sxs-lookup"><span data-stu-id="4215b-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4215b-220">Finansieringslofter</span><span class="sxs-lookup"><span data-stu-id="4215b-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="4215b-221">Grænse for finansieringskilde 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="4215b-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="4215b-222">Grænse for finansieringskilde 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="4215b-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="4215b-223">Grænse for finansieringskilde 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="4215b-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4215b-224">Transaktion 1</span><span class="sxs-lookup"><span data-stu-id="4215b-224">Transaction 1</span></span></td>
<td><span data-ttu-id="4215b-225"><strong>Transaktionsbeløb:</strong> 100,00<strong>Finansiering:</strong> Transaktionen betales kun i henhold til regel 1, da transaktionen er fuldt betalt, efter at regel 1 anvendes.</span><span class="sxs-lookup"><span data-stu-id="4215b-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="4215b-226">Transaktionen finansieres ligeligt mellem finansieringskilde 2 og finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="4215b-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="4215b-227">Finansieringskilde 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="4215b-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="4215b-228">Finansieringskilde 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="4215b-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4215b-229">Transaktion 2</span><span class="sxs-lookup"><span data-stu-id="4215b-229">Transaction 2</span></span></td>
<td><span data-ttu-id="4215b-230"><strong>Transaktionsbeløb:</strong> 5.000,00<strong>Finansiering:</strong> Transaktionen betales i henhold til alle tre regler.</span><span class="sxs-lookup"><span data-stu-id="4215b-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="4215b-231"><strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="4215b-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="4215b-232">Finansieringskilde 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="4215b-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="4215b-233">Finansieringskilde 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="4215b-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="4215b-234">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="4215b-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="4215b-235">Finansieringskilde 3: 250,00 (=750,00 - 50,00 - 450,00)</span><span class="sxs-lookup"><span data-stu-id="4215b-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="4215b-236">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="4215b-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="4215b-237">Finansieringskilde 1: 3.850,00 (=5.000,00 - 450,00 - 450,00 - 250,00)</span><span class="sxs-lookup"><span data-stu-id="4215b-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4215b-238">De samlede midler, der distribueres til hver finansieringskilde</span><span class="sxs-lookup"><span data-stu-id="4215b-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="4215b-239">Finansieringskilde 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="4215b-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="4215b-240">Finansieringskilde 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="4215b-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="4215b-241">Finansieringskilde 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="4215b-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="4215b-242">Faktureringsregler</span><span class="sxs-lookup"><span data-stu-id="4215b-242">Billing rules</span></span>
<span data-ttu-id="4215b-243">Når du forhandler en projektkontrakt med en kunde, definerer du, hvordan og hvornår du kan fakturere kunden for det udførte arbejde på et projekt.</span><span class="sxs-lookup"><span data-stu-id="4215b-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="4215b-244">Når du har konfigureret projektkontrakten og projektet, kan du konfigurere faktureringsregler for projektet.</span><span class="sxs-lookup"><span data-stu-id="4215b-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="4215b-245">Faktureringsregler er baseret på de projektbetingelser, der er angivet i projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="4215b-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="4215b-246">De faktureringsregler, du kan oprette, afhænger af vilkårene i projektkontrakten og projekttypen, f.eks. tid og materialer eller fast pris, som du knytter til faktureringsreglen.</span><span class="sxs-lookup"><span data-stu-id="4215b-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="4215b-247">Du kan oprette mere end én faktureringsregel for en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="4215b-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="4215b-248">Du kan også tildele en faktureringsregel til flere projekter, der er knyttet til den samme projektkontrakt og har lignende faktureringsbetingelser.</span><span class="sxs-lookup"><span data-stu-id="4215b-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="4215b-249">Du kan oprette følgende typer faktureringsregler:</span><span class="sxs-lookup"><span data-stu-id="4215b-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="4215b-250">**Leveringsenhed** – Fakturer en kunde, når du har fuldført en leveringsenhed.</span><span class="sxs-lookup"><span data-stu-id="4215b-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="4215b-251">Du kan definere de enheder, der skal leveres, i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="4215b-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="4215b-252">**Fremgang** – Fakturer kunden, når du har fuldført en bestemt procentdel af projektet.</span><span class="sxs-lookup"><span data-stu-id="4215b-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="4215b-253">Du kan konfigurere en faktureringsregel for automatisk at beregne procentdelen af det fuldførte arbejde, eller du kan beregne procentdelen af fuldført arbejde manuelt og det beløb, som kunden skal faktureres.</span><span class="sxs-lookup"><span data-stu-id="4215b-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="4215b-254">**Milepæl** – Fakturer kunden for det fulde beløb for en projektmilepæl, når milepælen er nået.</span><span class="sxs-lookup"><span data-stu-id="4215b-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="4215b-255">**Gebyr** – Fakturer kunden for dine tjenester plus et administrationsgebyr, som normalt er en procentdel af omkostningerne forbundet hermed.</span><span class="sxs-lookup"><span data-stu-id="4215b-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="4215b-256">**Tid og materiale** – Fakturer en kunde for værdien af den tid og de materialer, der bruges på et projekt.</span><span class="sxs-lookup"><span data-stu-id="4215b-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="4215b-257">I forbindelse med alle typer faktureringsregler kan du angive en tilbageholdelsesprocent, som trækkes fra på kundefakturaer, indtil et projekt når et aftalte stadie.</span><span class="sxs-lookup"><span data-stu-id="4215b-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="4215b-258">Der er angivet en procentdel for tilbageholdelse af betaling i projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="4215b-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="4215b-259">Beløbet beregnes på baggrund af, og trækkes fra, den samlede værdi af linjerne i en kundes faktura.</span><span class="sxs-lookup"><span data-stu-id="4215b-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="4215b-260">For så vidt angår faktureringsregler for **Tid og materiale** samt **Fremgang** kan du tildele fakturerbare kategorier.</span><span class="sxs-lookup"><span data-stu-id="4215b-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="4215b-261">Fakturerbare kategorier angiver de transaktioner, der skal inkluderes i kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="4215b-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="4215b-262">Når du er klar til at fakturere kunden, beregnes det beløb, der skal faktureres for projektet, på grundlag af faktureringsreglerne, og der genereres et projektfakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="4215b-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="4215b-263">Følgende sektioner indeholder eksempler, der viser, hvordan du kan konfigurere og administrere faktureringsregler for et projekt.</span><span class="sxs-lookup"><span data-stu-id="4215b-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="4215b-264">Eksempel: Opret en faktureringsregel, der er baseret på antallet af leverede enheder</span><span class="sxs-lookup"><span data-stu-id="4215b-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="4215b-265">Din organisation indgår en aftale om at give i alt fem oplæringssessioner til en kundes medarbejdere til en pris på 10.000 pr. oplæringssession.</span><span class="sxs-lookup"><span data-stu-id="4215b-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="4215b-266">Du fakturerer kunden efter hver enkelt oplæringssession.</span><span class="sxs-lookup"><span data-stu-id="4215b-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="4215b-267">Når du konfigurerer faktureringsreglerne for kontrakten, skal du bruge følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="4215b-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="4215b-268">Leveringsenheden er én oplæringssession.</span><span class="sxs-lookup"><span data-stu-id="4215b-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="4215b-269">Enhedsprisen er 10.000 pr. oplæringssession.</span><span class="sxs-lookup"><span data-stu-id="4215b-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="4215b-270">Det samlede antal enheder er fem oplæringssessioner.</span><span class="sxs-lookup"><span data-stu-id="4215b-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="4215b-271">Når du har fuldført én oplæringssession, kan du oprette en faktura på 10.000 for den første enhed, der blev leveret, og sende fakturaen til kunden.</span><span class="sxs-lookup"><span data-stu-id="4215b-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="4215b-272">Eksempel: Opret en faktureringsregel, der er baseret på en angivet procent for projektets fuldførelse (manuel beregning)</span><span class="sxs-lookup"><span data-stu-id="4215b-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="4215b-273">Din organisation, som yder softwarerådgivning, indgår i en aftale med en kunde om at udvikle en del af et produkt, som kunden udvikler.</span><span class="sxs-lookup"><span data-stu-id="4215b-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="4215b-274">Din organisation indvilliger i at levere softwarekoden over en periode på seks måneder.</span><span class="sxs-lookup"><span data-stu-id="4215b-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="4215b-275">Kunden indvilliger i at betale din organisation i alt 100.000 for arbejdet.</span><span class="sxs-lookup"><span data-stu-id="4215b-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="4215b-276">Du opretter en faktureringsregel for at fakturere kunden på grundlag af den procentdel af arbejdet, der er fuldført på projektet, som angivet i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="4215b-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="4215b-277">I slutningen af den første måned mødes du med kunden for at finde ud af, hvor mange procent af arbejdet der er fuldført.</span><span class="sxs-lookup"><span data-stu-id="4215b-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="4215b-278">Når du og kunden gennemgår projektet, beslutter du, at projektet er 15 procent fuldført.</span><span class="sxs-lookup"><span data-stu-id="4215b-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="4215b-279">Du opretter en faktura på 15.000 (15 procent af 100.000) og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="4215b-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="4215b-280">Eksempel: Opret en faktureringsregel, der er baseret på en angivet procent for projektets fuldførelse (automatisk beregning)</span><span class="sxs-lookup"><span data-stu-id="4215b-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="4215b-281">Din organisation, som er et softwareudviklingsfirma, indgår en aftale om at udvikle en lønafregningspakke til en kunde for 30.000.</span><span class="sxs-lookup"><span data-stu-id="4215b-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="4215b-282">Kunden indvilliger i at betale din organisation på grundlag af procentdelen af fuldført arbejde.</span><span class="sxs-lookup"><span data-stu-id="4215b-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="4215b-283">Du skønner, at projektomkostningerne beløber sig til 20.000.</span><span class="sxs-lookup"><span data-stu-id="4215b-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="4215b-284">Projektkontrakten angiver de arbejdskategorier, der bruges i faktureringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="4215b-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="4215b-285">Du konfigurerer faktureringsregler, der automatisk beregner fakturabeløbene for den procentdel af arbejdet, der er fuldført for de enkelte kategorier.</span><span class="sxs-lookup"><span data-stu-id="4215b-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="4215b-286">Du konfigurerer et budget for hver kategori:</span><span class="sxs-lookup"><span data-stu-id="4215b-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="4215b-287">**Udvikling** – Udgifter på 15.000 og omsætning på 20.000</span><span class="sxs-lookup"><span data-stu-id="4215b-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="4215b-288">**Udrulning** – Udgifter på 5.000 og omsætning på 10.000</span><span class="sxs-lookup"><span data-stu-id="4215b-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="4215b-289">Første gang du opretter en kundefaktura, beregnes fakturabeløbet automatisk på baggrund af følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="4215b-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="4215b-290">Efter en måned sender arbejderen på projektet en timeseddel for projektet.</span><span class="sxs-lookup"><span data-stu-id="4215b-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="4215b-291">Omkostningerne til arbejderens timer er 5.000 for udvikling og 1.000 til installation.</span><span class="sxs-lookup"><span data-stu-id="4215b-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="4215b-292">Udviklingsarbejdet er 33 procent fuldført (5.000 i faktiske omkostninger/15.000 i budgetomkostninger), og installationsarbejdet er 20 procent fuldført (1.000 i faktiske omkostninger/5.000 i budgetomkostninger).</span><span class="sxs-lookup"><span data-stu-id="4215b-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="4215b-293">Fakturabeløbet på 8.667 beregnes automatisk (33 procent af 20.000 + 20 procent af 10.000).</span><span class="sxs-lookup"><span data-stu-id="4215b-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="4215b-294">Du opretter en faktura på 8.667 og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="4215b-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="4215b-295">Eksempel: Opret en faktureringsregel, der er baseret på aftalte milepæle</span><span class="sxs-lookup"><span data-stu-id="4215b-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="4215b-296">Din organisation er et ledelsesrådgivningsfirma, der er med til at udføre markedsundersøgelser for et forbrugerprodukt, som kunden har til hensigt at sælge.</span><span class="sxs-lookup"><span data-stu-id="4215b-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="4215b-297">Kunden indvilliger i at bruge dine tjenester i en periode på tre måneder fra og med marts og accepterer at betale din organisation 50.000.</span><span class="sxs-lookup"><span data-stu-id="4215b-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="4215b-298">Der er tre milepæle i projektet:</span><span class="sxs-lookup"><span data-stu-id="4215b-298">The project has three milestones:</span></span>

-   <span data-ttu-id="4215b-299">Milepæl 1: indsamling af forbrugerdata – 31. marts</span><span class="sxs-lookup"><span data-stu-id="4215b-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="4215b-300">Milepæl 2: analyse af forbrugerdata – 30. april</span><span class="sxs-lookup"><span data-stu-id="4215b-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="4215b-301">Milepæl 3: fremlæggelse af et forslag til produktets levedygtighed – 31. maj</span><span class="sxs-lookup"><span data-stu-id="4215b-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="4215b-302">Kunden indvilliger i at betale din organisation 10.000 for den første milepæl, 20.000 for den anden milepæl og 20.000 for den tredje milepæl.</span><span class="sxs-lookup"><span data-stu-id="4215b-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="4215b-303">Når du konfigurerer projektkontrakten, accepterer du at fakturere kunden på baggrund af den milepæl, der er fuldført.</span><span class="sxs-lookup"><span data-stu-id="4215b-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="4215b-304">Opsætningen af faktureringsreglen omfatter følgende trin:</span><span class="sxs-lookup"><span data-stu-id="4215b-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="4215b-305">Definer projektets milepæle.</span><span class="sxs-lookup"><span data-stu-id="4215b-305">Define the project milestones.</span></span>
-   <span data-ttu-id="4215b-306">Definer det beløb, kunden skal faktureres, når de enkelte milepæle er fuldført.</span><span class="sxs-lookup"><span data-stu-id="4215b-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="4215b-307">Når den første milepæl er fuldført den 31. marts, markerer du milepælen som fuldført og opretter derefter en faktura lydende på 10.000 og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="4215b-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="4215b-308">Du kan ikke oprette en faktura for en milepæl, før du har markeret milepælen som fuldført.</span><span class="sxs-lookup"><span data-stu-id="4215b-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="4215b-309">Eksempel: Opret en faktureringsregel, der er baseret på tjenester plus et administrationsgebyr</span><span class="sxs-lookup"><span data-stu-id="4215b-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="4215b-310">Din organisation, et ledelsesrådgivningsfirma, indgår en aftale om at udføre markedsundersøgelser for at vurdere levedygtigheden for et produkt, som kunden, et detailfirma, udvikler.</span><span class="sxs-lookup"><span data-stu-id="4215b-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="4215b-311">Vilkårene for aftalen angiver, at du vil stille dine tre bedste ledelseskonsulenter til rådighed, som udfører undersøgelsen på tids- og materialebasis.</span><span class="sxs-lookup"><span data-stu-id="4215b-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="4215b-312">Kunden indvilliger i at betale 100 pr. time plus et administrationsgebyr på 10 procent for de konsulenttimer, der tilskrives projektet.</span><span class="sxs-lookup"><span data-stu-id="4215b-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="4215b-313">Når du konfigurerer projektkontrakten, skal du oprette en faktureringsregel for at tilføje et administrationsgebyr på 10 procent til de konsulenttimer, der tilskrives projektet.</span><span class="sxs-lookup"><span data-stu-id="4215b-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="4215b-314">Når du opretter en faktura for kunden, faktureres kunden et administrationsgebyr på 10 procent plus prisen for konsulenttimerne.</span><span class="sxs-lookup"><span data-stu-id="4215b-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="4215b-315">Hvis de tre konsulenter f.eks. har arbejdet i alt 200 timer på projektet, oprettes der en faktura på 22.000, der er baseret på følgende beregning:</span><span class="sxs-lookup"><span data-stu-id="4215b-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="4215b-316">200 timer ved 100 pr. time = 20.000</span><span class="sxs-lookup"><span data-stu-id="4215b-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="4215b-317">10 procent administrationsgebyr = 2.000</span><span class="sxs-lookup"><span data-stu-id="4215b-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="4215b-318">Samlet fakturabeløb = 22.000</span><span class="sxs-lookup"><span data-stu-id="4215b-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="4215b-319">Hvis gebyrer er momspligtige for en kunde, og du vælger en momsgruppe i projektkontrakten, angives momsgruppen automatisk som en faktureringsregel for gebyrer.</span><span class="sxs-lookup"><span data-stu-id="4215b-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="4215b-320">Eksempel: Opret en faktureringsregel for værdien af tid og materialer</span><span class="sxs-lookup"><span data-stu-id="4215b-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="4215b-321">Din organisation, som er en softwarekonsulentvirksomhed, indgår aftale om at stille fem tekniske konsulenter til rådighed til at arbejde på et softwareudviklingsprojekt for en kunde i de næste seks måneder.</span><span class="sxs-lookup"><span data-stu-id="4215b-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="4215b-322">Kunden indvilliger i at betale 150 for hver konsulenttime samt udgifterne til kontorartikler.</span><span class="sxs-lookup"><span data-stu-id="4215b-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="4215b-323">Din organisation sender en faktura til kunden i slutningen af hver måned.</span><span class="sxs-lookup"><span data-stu-id="4215b-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="4215b-324">Når du konfigurerer projektkontrakten, indvilliger du i at fakturere kunden hver måned for tid og materialer anvendt på projektet.</span><span class="sxs-lookup"><span data-stu-id="4215b-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="4215b-325">Du opretter en faktureringsregel, der indeholder følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="4215b-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="4215b-326">Kontraktperioden er på seks måneder.</span><span class="sxs-lookup"><span data-stu-id="4215b-326">The contract period is six months.</span></span>
-   <span data-ttu-id="4215b-327">Konsulenttid beregnes med en sats på 150 pr. time.</span><span class="sxs-lookup"><span data-stu-id="4215b-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="4215b-328">Kontorartikler faktureres til kostpris, og de samlede omkostninger for projektet må ikke overstige 10.000.</span><span class="sxs-lookup"><span data-stu-id="4215b-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="4215b-329">Du opretter en faktura til kunden i slutningen af hver kalendermåned, så længe projektet er i gang.</span><span class="sxs-lookup"><span data-stu-id="4215b-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="4215b-330">I løbet af den første måned registreres der i alt 800 konsulenttimer på projektet.</span><span class="sxs-lookup"><span data-stu-id="4215b-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="4215b-331">Kostprisen for de kontorartikler, der tilskrives projektet, er 2.000.</span><span class="sxs-lookup"><span data-stu-id="4215b-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="4215b-332">I slutningen af måneden opretter du derfor en faktura på 122.000, som beregnes som 800 timer af 150 pr. time, plus 2.000 til kontorartikler.</span><span class="sxs-lookup"><span data-stu-id="4215b-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]