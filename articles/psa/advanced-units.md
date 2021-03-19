---
title: Enhedsgrupper og enheder
description: Dette emne indeholder oplysninger om enhedsgrupper og enheder.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 45e4a95b429cd9d1f174653bd28cf567f690676d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291612"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="888e9-103">Enhedsgrupper og enheder</span><span class="sxs-lookup"><span data-stu-id="888e9-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="888e9-104">Enhedsgrupper og enheder er basisenhederne i Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="888e9-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="888e9-105">En enhed er en enkelt måleenhed, og flere enheder kan grupperes i enhedsgrupper.</span><span class="sxs-lookup"><span data-stu-id="888e9-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="888e9-106">En enhedsgruppe kaldes undertiden en enhedsplan i brugergrænsefladen i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="888e9-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="888e9-107">Her er nogle eksempler på enheder og enhedsgrupper:</span><span class="sxs-lookup"><span data-stu-id="888e9-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="888e9-108">**Enhedsgruppe**: afstand</span><span class="sxs-lookup"><span data-stu-id="888e9-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="888e9-109">**Enheder**: mile, kilometer, osv.</span><span class="sxs-lookup"><span data-stu-id="888e9-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="888e9-110">**Enhedsgruppe**: Tid</span><span class="sxs-lookup"><span data-stu-id="888e9-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="888e9-111">**Enheder**: time, day, uge osv.</span><span class="sxs-lookup"><span data-stu-id="888e9-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="888e9-112">Når du konfigurerer flere enheder i en enhedsgruppe, skal du også konfigurere en konverteringsfaktor mellem dem ved at angive den første enhed, du konfigurerer, som standardenhed eller den primære enhed for enhedsgruppen.</span><span class="sxs-lookup"><span data-stu-id="888e9-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="888e9-113">Hvis du f.eks. i en **Tid**-enhedsgruppe konfigurerer **Time** som første enhed, definerer systemet **Time** som standardenhed.</span><span class="sxs-lookup"><span data-stu-id="888e9-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="888e9-114">Hvis den næste enhed, du konfigurerer, er **Dag**, skal du konfigurere en konverteringsfaktor for **Dag** til **Time**.</span><span class="sxs-lookup"><span data-stu-id="888e9-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="888e9-115">Hvis du derefter tilføjer **Uge** som en tredje enhed, skal du konfigurere en konverteringsfaktor for **Uge** i forhold til **Dag** eller **Time**.</span><span class="sxs-lookup"><span data-stu-id="888e9-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="888e9-116">I følgende billede vises et eksempel på en opsætning af enheden **Dag** , hvor feltet **Antal** viser det antal timer, der er på en dag, og **Uge**, hvor feltet **Antal** indeholder antallet af dage i en uge.</span><span class="sxs-lookup"><span data-stu-id="888e9-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Enhedsgruppe: siden Oplysninger](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="888e9-118">Brug af enheder og enhedsgrupper</span><span class="sxs-lookup"><span data-stu-id="888e9-118">Using units and unit groups</span></span>

<span data-ttu-id="888e9-119">Dynamics 365 Project Service Automation bruger enheder og enhedsgrupper til at behandle estimater og poster for både udgifter og tid.</span><span class="sxs-lookup"><span data-stu-id="888e9-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="888e9-120">For udgifter har de enkelte udgiftskategorier en standardenhedsgruppe og -enhed.</span><span class="sxs-lookup"><span data-stu-id="888e9-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="888e9-121">Disse værdier angives som standardværdier på prislisteposter for udgiftskategorier.</span><span class="sxs-lookup"><span data-stu-id="888e9-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="888e9-122">Du kan f.eks have en udgiftskategori med navnet **Kørsel**.</span><span class="sxs-lookup"><span data-stu-id="888e9-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="888e9-123">Den har en enhedsgruppe med navnet **Afstand** og en standardenhed med navnet **Kilometer**.</span><span class="sxs-lookup"><span data-stu-id="888e9-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="888e9-124">Hvis du konfigurerer **Afstand**-enhedsgruppen, så den har to enheder (**Mile** og **Kilometer**), kan du oprette to priser for **Kørsel**-kategorien på én prisliste: pris pr. mile og pris pr. kilometer.</span><span class="sxs-lookup"><span data-stu-id="888e9-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="888e9-125">Udgiftskategori</span><span class="sxs-lookup"><span data-stu-id="888e9-125">Expense category</span></span>  | <span data-ttu-id="888e9-126">Enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="888e9-126">Unit group</span></span>  | <span data-ttu-id="888e9-127">Enhed</span><span class="sxs-lookup"><span data-stu-id="888e9-127">Unit</span></span>      | <span data-ttu-id="888e9-128">Prissætningsmetode</span><span class="sxs-lookup"><span data-stu-id="888e9-128">Pricing method</span></span>  | <span data-ttu-id="888e9-129">Pris pr. enhed</span><span class="sxs-lookup"><span data-stu-id="888e9-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="888e9-130">Kørsel</span><span class="sxs-lookup"><span data-stu-id="888e9-130">Mileage</span></span>           | <span data-ttu-id="888e9-131">Afstand</span><span class="sxs-lookup"><span data-stu-id="888e9-131">Distance</span></span>      | <span data-ttu-id="888e9-132">Mile</span><span class="sxs-lookup"><span data-stu-id="888e9-132">Mile</span></span>      | <span data-ttu-id="888e9-133">Pris pr. enhed</span><span class="sxs-lookup"><span data-stu-id="888e9-133">Price per unit</span></span>    | <span data-ttu-id="888e9-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="888e9-134">10 USD</span></span>            |
| <span data-ttu-id="888e9-135">Kørsel</span><span class="sxs-lookup"><span data-stu-id="888e9-135">Mileage</span></span>           | <span data-ttu-id="888e9-136">Afstand</span><span class="sxs-lookup"><span data-stu-id="888e9-136">Distance</span></span>      | <span data-ttu-id="888e9-137">Kilometer</span><span class="sxs-lookup"><span data-stu-id="888e9-137">Kilometer</span></span> | <span data-ttu-id="888e9-138">Pris pr. enhed</span><span class="sxs-lookup"><span data-stu-id="888e9-138">Price per unit</span></span>    |  <span data-ttu-id="888e9-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="888e9-139">6 USD</span></span>            |

<span data-ttu-id="888e9-140">Når du angiver en udgift på et projekt, bestemmer systemet prisen via kombinationen af kategorien og enheden på udgiften.</span><span class="sxs-lookup"><span data-stu-id="888e9-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="888e9-141">Beskrivelse af udgift</span><span class="sxs-lookup"><span data-stu-id="888e9-141">Expense description</span></span>        | <span data-ttu-id="888e9-142">Udgiftskategori</span><span class="sxs-lookup"><span data-stu-id="888e9-142">Expense category</span></span>  | <span data-ttu-id="888e9-143">Enhed</span><span class="sxs-lookup"><span data-stu-id="888e9-143">Unit</span></span>  | <span data-ttu-id="888e9-144">Antal</span><span class="sxs-lookup"><span data-stu-id="888e9-144">Quantity</span></span>  | <span data-ttu-id="888e9-145">Enhedspris</span><span class="sxs-lookup"><span data-stu-id="888e9-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="888e9-146">Kørsel til kundeadresse</span><span class="sxs-lookup"><span data-stu-id="888e9-146">Drive to client location</span></span> | <span data-ttu-id="888e9-147">Kørsel</span><span class="sxs-lookup"><span data-stu-id="888e9-147">Mileage</span></span>             | <span data-ttu-id="888e9-148">Mile</span><span class="sxs-lookup"><span data-stu-id="888e9-148">Mile</span></span>  | <span data-ttu-id="888e9-149">10</span><span class="sxs-lookup"><span data-stu-id="888e9-149">10</span></span>        | <span data-ttu-id="888e9-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="888e9-150">10 USD</span></span>         |

<span data-ttu-id="888e9-151">For tiden indeholder hver prislisteoverskrift et **Standardtidsenhed**-felt.</span><span class="sxs-lookup"><span data-stu-id="888e9-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="888e9-152">Værdien angives, når du opretter prislisteoverskriften.</span><span class="sxs-lookup"><span data-stu-id="888e9-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="888e9-153">Denne enhed bruges derefter til at angive alle rollebaserede priser på prislisten.</span><span class="sxs-lookup"><span data-stu-id="888e9-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="888e9-154">Der kan udtrykkes estimatlinjer for feltet **Tid på tilbud** i en hvilken som helst tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="888e9-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="888e9-155">Dog kan der kun bruges **Time** som tidsenhed i estimatlinjer og tidsregistreringer på projekter.</span><span class="sxs-lookup"><span data-stu-id="888e9-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="888e9-156">Hvis enheden på tidsregistreringen eller estimatlinjen ikke stemmer overens med enheden på prislistelinjen for den pågældende rolle, vil systemet konvertere prisen til de enheder, der er defineret i projektestimatet eller den faktiske transaktion for projektet.</span><span class="sxs-lookup"><span data-stu-id="888e9-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="888e9-157">I følgende eksempel vises, hvordan PSA bruger enhedsgruppe, enheder og konverteringsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="888e9-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="888e9-158">Enheder</span><span class="sxs-lookup"><span data-stu-id="888e9-158">Units</span></span>

   - <span data-ttu-id="888e9-159">**Enhedsgruppe**: Tid</span><span class="sxs-lookup"><span data-stu-id="888e9-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="888e9-160">**Enheder**: time</span><span class="sxs-lookup"><span data-stu-id="888e9-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="888e9-161">**Dag** – Konverteringsfaktor: 8 timer</span><span class="sxs-lookup"><span data-stu-id="888e9-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="888e9-162">**Uge** – Konverteringsfaktor: 40 timer</span><span class="sxs-lookup"><span data-stu-id="888e9-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="888e9-163">Opsætning af prisliste i projekt A:</span><span class="sxs-lookup"><span data-stu-id="888e9-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="888e9-164">**Navn**: Britiske salgspriser 2016</span><span class="sxs-lookup"><span data-stu-id="888e9-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="888e9-165">**Standardtidsenhed**: dag</span><span class="sxs-lookup"><span data-stu-id="888e9-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="888e9-166">**Valuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="888e9-166">**Currency**: GBP</span></span>

| <span data-ttu-id="888e9-167">Rolle</span><span class="sxs-lookup"><span data-stu-id="888e9-167">Role</span></span>      | <span data-ttu-id="888e9-168">Enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="888e9-168">Unit group</span></span> | <span data-ttu-id="888e9-169">Enhed</span><span class="sxs-lookup"><span data-stu-id="888e9-169">Unit</span></span> | <span data-ttu-id="888e9-170">Afdeling:</span><span class="sxs-lookup"><span data-stu-id="888e9-170">Organizational unit</span></span> | <span data-ttu-id="888e9-171">Pris</span><span class="sxs-lookup"><span data-stu-id="888e9-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="888e9-172">Udvikler</span><span class="sxs-lookup"><span data-stu-id="888e9-172">Developer</span></span> | <span data-ttu-id="888e9-173">Tidspunkt</span><span class="sxs-lookup"><span data-stu-id="888e9-173">Time</span></span>       | <span data-ttu-id="888e9-174">Day</span><span class="sxs-lookup"><span data-stu-id="888e9-174">Day</span></span>  | <span data-ttu-id="888e9-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="888e9-175">Contoso UK</span></span>          | <span data-ttu-id="888e9-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="888e9-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="888e9-177">Tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="888e9-177">Time entry</span></span>

<span data-ttu-id="888e9-178">I tabellen nedenfor vises den endelige transaktion på salgssiden, der er oprettet af PSA for et tre timers projekt.</span><span class="sxs-lookup"><span data-stu-id="888e9-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="888e9-179">Projekt</span><span class="sxs-lookup"><span data-stu-id="888e9-179">Project</span></span>   | <span data-ttu-id="888e9-180">Opgave</span><span class="sxs-lookup"><span data-stu-id="888e9-180">Task</span></span>    | <span data-ttu-id="888e9-181">Rolle</span><span class="sxs-lookup"><span data-stu-id="888e9-181">Role</span></span>      | <span data-ttu-id="888e9-182">Antal</span><span class="sxs-lookup"><span data-stu-id="888e9-182">Quantity</span></span> | <span data-ttu-id="888e9-183">Enhed</span><span class="sxs-lookup"><span data-stu-id="888e9-183">Unit</span></span>  | <span data-ttu-id="888e9-184">Enhedspris</span><span class="sxs-lookup"><span data-stu-id="888e9-184">Unit price</span></span> | <span data-ttu-id="888e9-185">Ikke-faktureret salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="888e9-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="888e9-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="888e9-186">Project A</span></span> | <span data-ttu-id="888e9-187">Design</span><span class="sxs-lookup"><span data-stu-id="888e9-187">Design</span></span>  | <span data-ttu-id="888e9-188">Udvikler</span><span class="sxs-lookup"><span data-stu-id="888e9-188">Developer</span></span> | <span data-ttu-id="888e9-189">3</span><span class="sxs-lookup"><span data-stu-id="888e9-189">3</span></span>        | <span data-ttu-id="888e9-190">Hour</span><span class="sxs-lookup"><span data-stu-id="888e9-190">Hour</span></span>  | <span data-ttu-id="888e9-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="888e9-191">100 GBP</span></span>    | <span data-ttu-id="888e9-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="888e9-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="888e9-193">Ofte stillede spørgsmål til tidsenhed</span><span class="sxs-lookup"><span data-stu-id="888e9-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="888e9-194">Konverteres PSA til forskellige enheder i forbindelse med udgifter?</span><span class="sxs-lookup"><span data-stu-id="888e9-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="888e9-195">Nej.</span><span class="sxs-lookup"><span data-stu-id="888e9-195">No.</span></span> <span data-ttu-id="888e9-196">Enhedskonvertering kan kun bruges til tid.</span><span class="sxs-lookup"><span data-stu-id="888e9-196">Unit conversion works only for time.</span></span> <span data-ttu-id="888e9-197">Hvis systemet ikke kan finde en udgiftspris for kombinationen af udgiftskategorien og enheden, angives prisen til 0,00 som standard.</span><span class="sxs-lookup"><span data-stu-id="888e9-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="888e9-198">Hvorfor konverteres tidsenheder af PSA?</span><span class="sxs-lookup"><span data-stu-id="888e9-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="888e9-199">I visse lande eller områder er der et juridisk krav om, at fakturasatser er konfigureret i antal dage.</span><span class="sxs-lookup"><span data-stu-id="888e9-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="888e9-200">Prisforhandling og rabatgivning i løbet af tilbudsforløbet sker ved hjælp af dagstakster for hver fakturerbar rolle.</span><span class="sxs-lookup"><span data-stu-id="888e9-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="888e9-201">Estimeret tidsplan og tidsregistrering udføres i timer.</span><span class="sxs-lookup"><span data-stu-id="888e9-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="888e9-202">For at understøtte denne forskel i tidsenheder konverteres tidsenheder i PSA.</span><span class="sxs-lookup"><span data-stu-id="888e9-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="888e9-203">Kan tidsenheder ændres i projektestimater?</span><span class="sxs-lookup"><span data-stu-id="888e9-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="888e9-204">Nej.</span><span class="sxs-lookup"><span data-stu-id="888e9-204">No.</span></span> <span data-ttu-id="888e9-205">Estimeret tidsplan er i øjeblikket begrænset til timer og kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="888e9-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="888e9-206">Kan enheder og enhedsgrupper redigeres, slettes og tilføjes?</span><span class="sxs-lookup"><span data-stu-id="888e9-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="888e9-207">Ja.</span><span class="sxs-lookup"><span data-stu-id="888e9-207">Yes.</span></span> <span data-ttu-id="888e9-208">Med undtagelse af enhedsgruppen **Tid** og enheden **Time** kan alle enheder slettes eller redigeres, og der kan tilføjes nye enheder.</span><span class="sxs-lookup"><span data-stu-id="888e9-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="888e9-209">I PSA kan enhedsgruppen **Tid** og enheden **Time** ikke slettes.</span><span class="sxs-lookup"><span data-stu-id="888e9-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="888e9-210">De kan dog opdateres med en oversat tekst til feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="888e9-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]