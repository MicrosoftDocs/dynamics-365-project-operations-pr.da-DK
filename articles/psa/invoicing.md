---
title: Fakturering i Project Service Automation
description: Dette emne indeholder oplysninger om fakturering.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: f8107a660f9993c7b6a32d69047a81fb7e0abef8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074236"
---
# <a name="invoicing-in-project-service-automation"></a><span data-ttu-id="39ce2-103">Fakturering i Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="39ce2-103">Invoicing in Project Service Automation</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="39ce2-104">Fakturering i Dynamics 365 Project Service Automation er nyttig, fordi den giver projektledere et niveau til godkendelse på et andet niveau, før de opretter fakturaer til kunderne.</span><span class="sxs-lookup"><span data-stu-id="39ce2-104">Invoicing in Dynamics 365 Project Service Automation is useful because it gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="39ce2-105">Det første godkendelsesniveau fuldføres, når de tids- og udgiftsposter, som medlemmer af projektteamet sender, godkendes.</span><span class="sxs-lookup"><span data-stu-id="39ce2-105">The first level of approval is completed when the time and expense entries that project team members submit are approved.</span></span>

<span data-ttu-id="39ce2-106">PSA er ikke designet til at generere kundefokuserede fakturaer af følgende årsager:</span><span class="sxs-lookup"><span data-stu-id="39ce2-106">PSA isn't designed to generate customer-facing invoices, for the following reasons:</span></span>

- <span data-ttu-id="39ce2-107">Den indeholder ikke skatteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="39ce2-107">It doesn't contain tax information.</span></span>
- <span data-ttu-id="39ce2-108">Det er ikke muligt at konvertere andre valutaer til faktureringsvalutaen ved hjælp af korrekt konfigurerede valutakurser.</span><span class="sxs-lookup"><span data-stu-id="39ce2-108">It can't convert other currencies to the invoicing currency by using correctly configured exchange rates.</span></span>
- <span data-ttu-id="39ce2-109">Det er ikke muligt at formatere fakturaer korrekt, så de kan udskrives.</span><span class="sxs-lookup"><span data-stu-id="39ce2-109">It can't correctly format invoices so that they can be printed.</span></span>

<span data-ttu-id="39ce2-110">Du kan i stedet bruge et regnskabssystem til at oprette kundefokuserede fakturaer, der bruger oplysninger fra fakturaforslag, som er genereret i PSA.</span><span class="sxs-lookup"><span data-stu-id="39ce2-110">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information from invoice proposals that are generated in PSA.</span></span>

## <a name="creating-project-invoices-in-psa"></a><span data-ttu-id="39ce2-111">Oprettelse af projektfakturaer i PSA.</span><span class="sxs-lookup"><span data-stu-id="39ce2-111">Creating project invoices in PSA</span></span>

<span data-ttu-id="39ce2-112">Der kan oprettes projektfakturaer én eller flere ad gangen.</span><span class="sxs-lookup"><span data-stu-id="39ce2-112">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="39ce2-113">Du kan oprette dem manuelt, eller de kan konfigureres, så de genereres i automatiserede kørsler.</span><span class="sxs-lookup"><span data-stu-id="39ce2-113">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices-in-psa"></a><span data-ttu-id="39ce2-114">Manuelt oprettede projektfakturaer i PSA</span><span class="sxs-lookup"><span data-stu-id="39ce2-114">Manually create project invoices in PSA</span></span>

<span data-ttu-id="39ce2-115">På siden med listen **Projektkontrakter** kan du oprette projektfakturaer separat for hver projektkontrakt, eller du kan oprette fakturaer samlet for flere projektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="39ce2-115">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="39ce2-116">Følg dette trin for at oprette en faktura for en bestemt projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="39ce2-116">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="39ce2-117">Åbn siden med listen **Projektkontrakter** , åbn en projektkontrakt, og vælg derefter **Opret faktura**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-117">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    ![Oprettelse af projektfakturaer for en bestemt projektkontrakt](media/CreateProjectInvoicesOneByOne.png)

    <span data-ttu-id="39ce2-119">Der genereres en faktura for alle transaktioner for den valgte projektkontrakt, der har statussen **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="39ce2-120">Disse transaktioner omfatter tid, udgifter, milepæle og produktbaserede kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-120">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

<span data-ttu-id="39ce2-121">Følg disse trin for at oprette flere fakturaer samlet.</span><span class="sxs-lookup"><span data-stu-id="39ce2-121">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="39ce2-122">På siden med listen **Projektkontrakter** skal du vælge en eller flere projektkontrakter, som du skal oprette en faktura for, og derefter vælge **Opret projektfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-122">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    ![Oprettelse af flere projektfakturaer samlet.](media/CreateProjectInvoicesBulk.png)

    <span data-ttu-id="39ce2-124">Der vises en advarsel om, at der kan være en forsinkelse, inden der oprettes fakturaer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-124">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="39ce2-125">Processen vises også.</span><span class="sxs-lookup"><span data-stu-id="39ce2-125">The process is also shown.</span></span>

2. <span data-ttu-id="39ce2-126">Vælg **OK** for at lukke meddelelsesfeltet.</span><span class="sxs-lookup"><span data-stu-id="39ce2-126">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="39ce2-127">Der genereres en faktura for alle transaktioner på en kontraktlinje, der har statussen **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-127">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="39ce2-128">Disse transaktioner omfatter tid, udgifter, milepæle og produktbaserede kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-128">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

3. <span data-ttu-id="39ce2-129">Hvis du vil have vist de fakturaer, der er genereret, skal du gå til **Salg** \> **Fakturering** \> **Fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-129">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="39ce2-130">Der vises én faktura for hver projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="39ce2-130">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a><span data-ttu-id="39ce2-131">Konfigurere automatisk oprettelse af projektfakturaer i PSA</span><span class="sxs-lookup"><span data-stu-id="39ce2-131">Set up automated creation of project invoices in PSA</span></span>

<span data-ttu-id="39ce2-132">Følg disse trin for at konfigurere en automatiseret fakturakørsel i PSA.</span><span class="sxs-lookup"><span data-stu-id="39ce2-132">Follow these steps to configure an automated invoice run in PSA.</span></span>

1. <span data-ttu-id="39ce2-133">Gå til **Project Service** \> **lndstillinger** \> **Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-133">Go to **Project Service** \> **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="39ce2-134">Opret et batchjob, og kald det **Opret fakturaer i PSA .**</span><span class="sxs-lookup"><span data-stu-id="39ce2-134">Create a batch job, and name it **PSA Create Invoices**.</span></span> <span data-ttu-id="39ce2-135">Navnet på batchjobbet skal indeholde udtrykket "Opret fakturaer".</span><span class="sxs-lookup"><span data-stu-id="39ce2-135">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="39ce2-136">I feltet **Jobtype** skal du vælge **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-136">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="39ce2-137">Som standard skal indstillingerne **Hyppighed: Dagligt** og **Er aktiv** angives til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-137">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="39ce2-138">Vælg **Kør arbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-138">Select **Run Workflow**.</span></span> <span data-ttu-id="39ce2-139">I dialogboksen **Slå post op** kan du se tre arbejdsprocesser:</span><span class="sxs-lookup"><span data-stu-id="39ce2-139">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="39ce2-140">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="39ce2-140">ProcessRunCaller</span></span>
    - <span data-ttu-id="39ce2-141">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="39ce2-141">ProcessRunner</span></span>
    - <span data-ttu-id="39ce2-142">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="39ce2-142">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="39ce2-143">Vælg **ProcessRunCaller** og derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-143">Select **ProcessRunCaller** , and then select **Add**.</span></span>
6. <span data-ttu-id="39ce2-144">I den næste dialogboks skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-144">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="39ce2-145">En **slumre** -arbejdsproces efterfølges af en **proces** -arbejdsproces.</span><span class="sxs-lookup"><span data-stu-id="39ce2-145">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="39ce2-146">Du kan også vælge **ProcessRunner** i trin 5.</span><span class="sxs-lookup"><span data-stu-id="39ce2-146">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="39ce2-147">Når du derefter vælger **OK** , efterfølges en **proces** -arbejdsproces af en **slumre** -arbejdsproces.</span><span class="sxs-lookup"><span data-stu-id="39ce2-147">Then, when you select **OK** , a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="39ce2-148">Begge arbejdsprocesserne **ProcessRunCaller** og **ProcessRunner** opretter fakturaer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-148">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="39ce2-149">**ProcessRunCaller** kalder på **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-149">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="39ce2-150">**ProcessRunner** er den arbejdsproces, der rent faktisk opretter fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="39ce2-150">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="39ce2-151">Denne proces gennemgår alle de kontraktlinjer, der skal oprettes fakturaer for, og den opretter fakturaer for disse linjer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-151">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="39ce2-152">Hvis du vil fastlægge, hvilke kontraktlinjer der skal oprettes fakturaer for, kigger jobbet på fakturaernes kørselsdatoer for kontraktlinjerne.</span><span class="sxs-lookup"><span data-stu-id="39ce2-152">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="39ce2-153">Hvis kontraktlinjer, der er knyttet til en kontrakt, har samme fakturakørselsdato, samles transaktionerne i én faktura, der indeholder to fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-153">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="39ce2-154">Hvis der ikke findes transaktioner, som der skal oprettes fakturaer til, ignorerer jobbet fakturaoprettelse.</span><span class="sxs-lookup"><span data-stu-id="39ce2-154">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="39ce2-155">Når **ProcessRunner** er færdig med at køre, kalder processen på **ProcessRunCaller** , angiver sluttidspunktet og lukkes.</span><span class="sxs-lookup"><span data-stu-id="39ce2-155">After **ProcessRunner** has finished running, it calls **ProcessRunCaller** , provides the end time, and is closed.</span></span> <span data-ttu-id="39ce2-156">**ProcessRunCaller** starter derefter en timer, der kører i 24 timer fra det angivne sluttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="39ce2-156">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="39ce2-157">Når timeren afsluttes, lukkes **ProcessRunCaller**.</span><span class="sxs-lookup"><span data-stu-id="39ce2-157">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="39ce2-158">Batchprocesjobbet til oprettelse af fakturaer er et tilbagevendende job.</span><span class="sxs-lookup"><span data-stu-id="39ce2-158">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="39ce2-159">Hvis denne batchproces køres mange gange, oprettes der flere forekomster af jobbet, og der opstår fejl.</span><span class="sxs-lookup"><span data-stu-id="39ce2-159">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="39ce2-160">Du bør derfor kun starte batchprocessen én gang, og du bør kun genstarte den, hvis den holder op med at køre.</span><span class="sxs-lookup"><span data-stu-id="39ce2-160">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="39ce2-161">Batchfakturering i Project Service Automation kører kun for projektkontraktlinjer, der er konfigureret af fakturaplaner.</span><span class="sxs-lookup"><span data-stu-id="39ce2-161">Batch invoicing in Project Service Automation only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="39ce2-162">Der skal være konfigureret målepæle for en kontraktlinje med en faktureringsmetode med fast pris.</span><span class="sxs-lookup"><span data-stu-id="39ce2-162">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="39ce2-163">Der skal konfigureres en datobaseret fakturaplan for en projektkontraktlinje med en metode til fakturering af time og materiale.</span><span class="sxs-lookup"><span data-stu-id="39ce2-163">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="39ce2-164">Oplysninger om konfiguration af faktureringsfrekvenser i forbindelse med et projekt, der er baseret på en tilbudslinje, findes i emne, [Tilbud og tilbudslinjer](basic-quote-lines.md#invoice-schedule).</span><span class="sxs-lookup"><span data-stu-id="39ce2-164">Information about setting up invoicing frequencies in the context of a project that is based on a quote line, is provided in the topic, [Quotes and quote lines](basic-quote-lines.md#invoice-schedule).</span></span> <span data-ttu-id="39ce2-165">Det samme gælder for en projektbaseret kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="39ce2-165">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-psa-invoice"></a><span data-ttu-id="39ce2-166">Redigere en kladde af PSA-faktura</span><span class="sxs-lookup"><span data-stu-id="39ce2-166">Edit a draft PSA invoice</span></span>

<span data-ttu-id="39ce2-167">Når du opretter en kladde til en projektfaktura, medtages alle ikke-fakturerede salgstransaktioner, der blev oprettet, da tids-og udgiftsposterne blev godkendt, på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="39ce2-167">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="39ce2-168">Du kan foretage følgende justeringer, mens fakturaen stadig er i kladdefasen:</span><span class="sxs-lookup"><span data-stu-id="39ce2-168">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="39ce2-169">Slette eller redigere oplysninger om fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-169">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="39ce2-170">Redigere og justere antal og faktureringstype.</span><span class="sxs-lookup"><span data-stu-id="39ce2-170">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="39ce2-171">Tilføje tid, udgifter og gebyrer direkte som transaktioner på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="39ce2-171">Directly add time, expense, and fees as transactions on the invoice.</span></span> <span data-ttu-id="39ce2-172">Du kan bruge denne funktion, hvis fakturalinjen er knyttet til en kontraktlinje, der tillader disse transaktionsklasser.</span><span class="sxs-lookup"><span data-stu-id="39ce2-172">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="39ce2-173">Vælg **Bekræft** for at bekræfte en faktura.</span><span class="sxs-lookup"><span data-stu-id="39ce2-173">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="39ce2-174">Handlingen Bekræft er en envejshandling.</span><span class="sxs-lookup"><span data-stu-id="39ce2-174">The Confirm action is a one-way action.</span></span> <span data-ttu-id="39ce2-175">Når du vælger **Bekræft** , bliver fakturaen skrivebeskyttet i systemet, og der oprettes fakturerede faktiske salgstal ud fra hver fakturalinjedetalje for hver fakturalinje.</span><span class="sxs-lookup"><span data-stu-id="39ce2-175">When you select **Confirm** , the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="39ce2-176">Hvis fakturalinjedetaljen refererer til et ikke-faktureret faktisk salgstal, vil systemet også tilbageføre det ikke-fakturerede faktiske salgstal.</span><span class="sxs-lookup"><span data-stu-id="39ce2-176">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="39ce2-177">Alle de fakturalinjedetaljer, der er oprettet ud fra en tids- eller udgiftspost, refererer til et ikke-faktureret faktisk salgstal. Integrationssystemer for generelle hovedbøger kan bruge denne tilbageførsel til at tilbageføre igangværende projektarbejde (WIP) til regnskabsmæssig brug.</span><span class="sxs-lookup"><span data-stu-id="39ce2-177">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-psa-invoice"></a><span data-ttu-id="39ce2-178">Rette en bekræftet PSA-faktura</span><span class="sxs-lookup"><span data-stu-id="39ce2-178">Correct a confirmed PSA invoice</span></span>

<span data-ttu-id="39ce2-179">Bekræftede PSA-fakturaer kan redigeres (korrigeres).</span><span class="sxs-lookup"><span data-stu-id="39ce2-179">Confirmed PSA invoices can be edited (corrected).</span></span> <span data-ttu-id="39ce2-180">Når en bekræftet faktura rettes, oprettes der en ny rettelsesfakturakladde.</span><span class="sxs-lookup"><span data-stu-id="39ce2-180">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="39ce2-181">Da det er en forudsætning, at du vil tilbageføre alle transaktioner og mængder fra den oprindelige faktura, inkluderer denne rettelsesfaktura alle transaktioner fra den oprindelige faktura, og alle mængder på den er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="39ce2-181">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="39ce2-182">Hvis der ikke skal rettes i nogen transaktioner, kan du fjerne dem fra rettelsesfakturakladden.</span><span class="sxs-lookup"><span data-stu-id="39ce2-182">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="39ce2-183">Hvis du kun vil tilbageføre eller returnere en delmængde, kan du redigere feltet **Antal** i linjedetaljen.</span><span class="sxs-lookup"><span data-stu-id="39ce2-183">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="39ce2-184">Hvis du åbner fakturalinjedetaljen, kan du se det oprindelige fakturaantal.</span><span class="sxs-lookup"><span data-stu-id="39ce2-184">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="39ce2-185">Du kan derefter redigere det aktuelle fakturaantal, så det er mindre eller større end det oprindelige fakturaantal.</span><span class="sxs-lookup"><span data-stu-id="39ce2-185">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="39ce2-186">Når du bekræfter en rettelsesfaktura, tilbageføres det oprindeligt fakturerede salgstal, og der oprettes et nyt faktureret faktisk salgstal.</span><span class="sxs-lookup"><span data-stu-id="39ce2-186">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="39ce2-187">Hvis mængden blev reduceret, medfører differencen, at der også oprettes et nyt ikke-faktureret faktisk salgstal.</span><span class="sxs-lookup"><span data-stu-id="39ce2-187">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="39ce2-188">Hvis det oprindelige fakturerede salg f.eks. var otte timer, og linjedetaljen i rettelsesfakturaen har et reduceret antal på seks timer, tilbagefører PSA den oprindeligt fakturerede salgslinje og opretter to nye faktiske salgstal:</span><span class="sxs-lookup"><span data-stu-id="39ce2-188">For example, if the original billed sales was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, PSA reverses the original billed sales line and creates two new actuals:</span></span>

- <span data-ttu-id="39ce2-189">Et faktureret faktisk salgstal for seks timer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-189">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="39ce2-190">Et ikke-faktureret faktisk salgstal for de resterende to timer.</span><span class="sxs-lookup"><span data-stu-id="39ce2-190">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="39ce2-191">Denne transaktion kan enten faktureres senere eller markeres som ikke-fakturerbar, afhængigt af forhandlingerne med kunden.</span><span class="sxs-lookup"><span data-stu-id="39ce2-191">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>