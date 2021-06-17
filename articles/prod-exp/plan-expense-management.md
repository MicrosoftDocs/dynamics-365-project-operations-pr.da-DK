---
title: Konfigurer udgiftsstyring
description: I denne artikel beskrives de overvejelser og beslutninger, du skal foretage under planlægningsprocessen, før du konfigurerer udgiftsstyring i Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52538946c7260fad4076a64e8dc34fecf08b90cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005379"
---
# <a name="configure-expense-management"></a><span data-ttu-id="64a72-103">Konfigurer udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="64a72-103">Configure expense management</span></span>

<span data-ttu-id="64a72-104">Dette emne beskriver de overvejelser og beslutninger, du skal foretage under planlægningsprocessen, før du konfigurerer udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="64a72-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="64a72-105">I udgiftsstyring kan du gemme oplysninger om betalingsmetoder, rejserekvisitioner, udgiftsrapporter, politikker osv.</span><span class="sxs-lookup"><span data-stu-id="64a72-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="64a72-106">Da mange af de beslutninger, du foretager, når du planlægger din konfiguration af udgiftsstyring, er baseret på organisationens hierarki og økonomiske struktur, skal du referere til planlægningsdokumenterne for de pågældende områder.</span><span class="sxs-lookup"><span data-stu-id="64a72-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="64a72-107">Interne udgifter</span><span class="sxs-lookup"><span data-stu-id="64a72-107">Intercompany expenses</span></span>

<span data-ttu-id="64a72-108">Når du aktiverer interne udgifter, giver du juridiske enheder og medarbejdere mulighed for at betale udgifter på vegne af en anden juridisk enhed og opkræve betaling fra den juridiske enhed i organisationen, hvor de er ansat.</span><span class="sxs-lookup"><span data-stu-id="64a72-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="64a72-109">En medarbejder i den juridiske enhed A fuldfører f.eks. et projekt for den juridiske enhed B, og projektet har resulteret i rejserelaterede udgifter.</span><span class="sxs-lookup"><span data-stu-id="64a72-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="64a72-110">Hvis interne udgifter er aktiveret, kan medarbejderen derefter arkivere en udgiftsrapport, der skal bogføre udgiften i den juridiske enhed B, og udgiften skal derefter betales af den juridiske enhed A. Hvis organisationen ikke har flere juridiske enheder, behøver du ikke at aktivere interne udgifter.</span><span class="sxs-lookup"><span data-stu-id="64a72-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="64a72-111">**Beslutning:** Vil du aktivere interne udgifter?</span><span class="sxs-lookup"><span data-stu-id="64a72-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="64a72-112">Økonomistyring</span><span class="sxs-lookup"><span data-stu-id="64a72-112">Financial management</span></span>

<span data-ttu-id="64a72-113">Udgiftsstyring er tæt integreret med organisationens økonomiske styring.</span><span class="sxs-lookup"><span data-stu-id="64a72-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="64a72-114">Mange af dine konfigurationer i udgiftsstyring er baseret på de beslutninger, du har træffet i relation til organisationens økonomi.</span><span class="sxs-lookup"><span data-stu-id="64a72-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="64a72-115">I følgende afsnit beskrives de forskellige områder, der kræver planlægning og beslutninger, baseret på organisationens økonomiske beslutninger og vejledninger fra dit lederteam.</span><span class="sxs-lookup"><span data-stu-id="64a72-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="64a72-116">Pr. dag</span><span class="sxs-lookup"><span data-stu-id="64a72-116">Per diems</span></span>

<span data-ttu-id="64a72-117">Du skal definere medarbejderens diæter, som organisationen kan tilbyde.</span><span class="sxs-lookup"><span data-stu-id="64a72-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="64a72-118">Da diæter typisk bruges til at dække udgifter såsom måltider, logi og andre uforudsete udgifter, kan du oprette regler for de diætgodtgørelser, som organisationen tilbyder.</span><span class="sxs-lookup"><span data-stu-id="64a72-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="64a72-119">diætsatser kan være baseret på tidspunktet for året, rejselokationen eller begge.</span><span class="sxs-lookup"><span data-stu-id="64a72-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="64a72-120">Når du definerer en diætregel, kan du angive, at en procentdel af diætsatsen skal tilbageholdes, hvis en arbejder modtager gratis måltider eller servicer.</span><span class="sxs-lookup"><span data-stu-id="64a72-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="64a72-121">Du kan også definere diætsatser med en nedre og øvre grænse for antallet af timer, hvor diætsatsen kan finde anvendelse på en arbejders rejse.</span><span class="sxs-lookup"><span data-stu-id="64a72-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="64a72-122">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="64a72-122">**Decisions:**</span></span>

- <span data-ttu-id="64a72-123">Standarddiætregler for første og sidste dag:</span><span class="sxs-lookup"><span data-stu-id="64a72-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="64a72-124">Hvad er det mindste antal timer, en medarbejder har krav på på en dag og stadig modtage en diæt?</span><span class="sxs-lookup"><span data-stu-id="64a72-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="64a72-125">Sker der reduktion i det beløb, der tilbydes til måltider for den første dag og den sidste dag?</span><span class="sxs-lookup"><span data-stu-id="64a72-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="64a72-126">Hvis der er en reduktion, hvad er procentdelen af reduktionen?</span><span class="sxs-lookup"><span data-stu-id="64a72-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="64a72-127">Sker der reduktion i det beløb, der tilbydes til hotelophold for den første dag og den sidste dag?</span><span class="sxs-lookup"><span data-stu-id="64a72-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="64a72-128">Hvis der er en reduktion, hvad er procentdelen af reduktionen?</span><span class="sxs-lookup"><span data-stu-id="64a72-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="64a72-129">Sker der reduktion i det beløb, der tilbydes til andre udgifter, som er afholdt den første dag og den sidste dag?</span><span class="sxs-lookup"><span data-stu-id="64a72-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="64a72-130">Hvis der er en reduktion, hvad er procentdelen af reduktionen?</span><span class="sxs-lookup"><span data-stu-id="64a72-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="64a72-131">Standarddiætregler:</span><span class="sxs-lookup"><span data-stu-id="64a72-131">Default per diem rules:</span></span>

    - <span data-ttu-id="64a72-132">Er der en procentvis reduktion i diætgodtgørelsen for de enkelte måltider, hvis der f.eks. er et gratis måltid?</span><span class="sxs-lookup"><span data-stu-id="64a72-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="64a72-133">Hvis der er en reduktion, hvad er procentdelen af reduktionen for hvert måltid?</span><span class="sxs-lookup"><span data-stu-id="64a72-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="64a72-134">Er reduktionen af måltid beregnet pr. dag, pr. rejse eller efter antallet af måltider pr. dag?</span><span class="sxs-lookup"><span data-stu-id="64a72-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="64a72-135">Skal diætbeløb afrundes på normal måde eller rundes op?</span><span class="sxs-lookup"><span data-stu-id="64a72-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="64a72-136">Beregnes diæter for en periode på 24 timer eller for en kalenderdag?</span><span class="sxs-lookup"><span data-stu-id="64a72-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="64a72-137">Regler for diæter, der er baseret på placering:</span><span class="sxs-lookup"><span data-stu-id="64a72-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="64a72-138">Skal diætsatser variere afhængigt af lokationen?</span><span class="sxs-lookup"><span data-stu-id="64a72-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="64a72-139">Hvilke lokationer inkluderes?</span><span class="sxs-lookup"><span data-stu-id="64a72-139">What locations are included?</span></span>
    - <span data-ttu-id="64a72-140">Hvis diæter varierer i forhold til lokation, skal du for hver lokation finde ud af, hvilket procentvist beløb der er angivet for følgende typer udgifter:</span><span class="sxs-lookup"><span data-stu-id="64a72-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="64a72-141">Måltider</span><span class="sxs-lookup"><span data-stu-id="64a72-141">Meals</span></span>
        - <span data-ttu-id="64a72-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="64a72-142">Hotel</span></span>
        - <span data-ttu-id="64a72-143">Andre udgifter</span><span class="sxs-lookup"><span data-stu-id="64a72-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="64a72-144">Kladder og konti til udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="64a72-144">Expense management journals and accounts</span></span>

<span data-ttu-id="64a72-145">Udgiftsstyring kræver, at du bruger flere kladder og konti.</span><span class="sxs-lookup"><span data-stu-id="64a72-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="64a72-146">Du skal f.eks. beslutte, om den samme konto skal bruges til kontantforskud og uoverensstemmelser vedrørende kreditkort.</span><span class="sxs-lookup"><span data-stu-id="64a72-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="64a72-147">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="64a72-147">**Decisions:**</span></span>

- <span data-ttu-id="64a72-148">Hvilken finanskladde er godkendte udgiftsrapporter bogført i?</span><span class="sxs-lookup"><span data-stu-id="64a72-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="64a72-149">Hvilken konto bruges til kontantforskud?</span><span class="sxs-lookup"><span data-stu-id="64a72-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="64a72-150">Skal kontantforskud bogføres omgående?</span><span class="sxs-lookup"><span data-stu-id="64a72-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="64a72-151">Betalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="64a72-151">Payment methods</span></span>

<span data-ttu-id="64a72-152">Når du giver medarbejdere mulighed for at afholde udgifter på vegne af din virksomhed, skal du definere de betalingsmetoder, som medarbejderne har lov til at bruge.</span><span class="sxs-lookup"><span data-stu-id="64a72-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="64a72-153">Du kan f.eks. give medarbejdere mulighed for at bruge kontanter eller en virksomheds kreditkort.</span><span class="sxs-lookup"><span data-stu-id="64a72-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="64a72-154">Du kan også give medarbejderne mulighed for at bruge personlige kreditkort og derefter refundere medarbejderne.</span><span class="sxs-lookup"><span data-stu-id="64a72-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="64a72-155">Du skal træffe følgende beslutninger for hver betalingsmetode, du tillader.</span><span class="sxs-lookup"><span data-stu-id="64a72-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="64a72-156">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="64a72-156">**Decisions:**</span></span>

- <span data-ttu-id="64a72-157">Hvilke betalingsmetoder er tilladt?</span><span class="sxs-lookup"><span data-stu-id="64a72-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="64a72-158">Hvem ejer betalingsmetodeudgifterne?</span><span class="sxs-lookup"><span data-stu-id="64a72-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="64a72-159">Er der en modkontotype?</span><span class="sxs-lookup"><span data-stu-id="64a72-159">Is there an offset account type?</span></span> <span data-ttu-id="64a72-160">Hvis der er angivet en modkontotype, hvad er det så?</span><span class="sxs-lookup"><span data-stu-id="64a72-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="64a72-161">Hvis der er angivet en modkonto, hvad er kontoen?</span><span class="sxs-lookup"><span data-stu-id="64a72-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="64a72-162">Hvis betalingsmetoden er et kreditkort, skal betalingsmetoden kun bruges til importerede transaktioner?</span><span class="sxs-lookup"><span data-stu-id="64a72-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="64a72-163">Udgiftskategorier og delte kategorier</span><span class="sxs-lookup"><span data-stu-id="64a72-163">Expense categories and shared categories</span></span>

<span data-ttu-id="64a72-164">Når medarbejdere opretter en udgiftsrapport, skal hver enkelt udgift, de registrerer, være knyttet til en udgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="64a72-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="64a72-165">Udgiftskategorier afledes af delte kategorier, der kan deles på tværs af de juridiske enheder i organisationen.</span><span class="sxs-lookup"><span data-stu-id="64a72-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="64a72-166">Disse kategorier kan også deles i Projektstyring og regnskab, afhængigt af den måde, som organisationen er defineret på.</span><span class="sxs-lookup"><span data-stu-id="64a72-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="64a72-167">Afhængigt af definitionen af din organisation og vejledning fra implementeringsteamet skal du afgøre, om de kategorier, der bruges i udgiftsstyring, kun skal bruges i udgiftsstyring, eller om de skal deles mellem Projektstyring og regnskab og Udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="64a72-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="64a72-168">Bemærk, at disse kategorier kan deles mellem projekt og udgift eller projekt og produktion, men ikke mellem udgift og produktion.</span><span class="sxs-lookup"><span data-stu-id="64a72-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="64a72-169">Du skal træffe følgende beslutninger for hver udgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="64a72-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="64a72-170">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="64a72-170">**Decisions:**</span></span>

- <span data-ttu-id="64a72-171">Hvad er udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="64a72-171">What is the expense category?</span></span> <span data-ttu-id="64a72-172">Som eksempel kan nævnes kategorier for fly, hotel eller kørsel.</span><span class="sxs-lookup"><span data-stu-id="64a72-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="64a72-173">Kan udgiftskategorien også bruges i projektstyring og regnskab?</span><span class="sxs-lookup"><span data-stu-id="64a72-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="64a72-174">Hvad er udgiftstypen?</span><span class="sxs-lookup"><span data-stu-id="64a72-174">What is the expense type?</span></span>
- <span data-ttu-id="64a72-175">Hvad er standardbetalingsmetoden for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="64a72-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="64a72-176">Skal udgifter i udgiftskategorien specificeres?</span><span class="sxs-lookup"><span data-stu-id="64a72-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="64a72-177">Hvad er den primære standardkonto for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="64a72-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="64a72-178">Hvad er standardvaremomsgruppen for udgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="64a72-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="64a72-179">Er yderligere betalingsmetoder for udgiftskategorien tilladt?</span><span class="sxs-lookup"><span data-stu-id="64a72-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="64a72-180">Hvis der er flere betalingsmetoder tilladt, hvad er de så?</span><span class="sxs-lookup"><span data-stu-id="64a72-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="64a72-181">Er der underkategorier i denne udgiftskategori?</span><span class="sxs-lookup"><span data-stu-id="64a72-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="64a72-182">I så fald skal du også træffer følgende beslutninger:</span><span class="sxs-lookup"><span data-stu-id="64a72-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="64a72-183">Er nogen af underkategorierne undtaget fra momsopkrævning?</span><span class="sxs-lookup"><span data-stu-id="64a72-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="64a72-184">Hvad er varemomsgruppen for underkategorierne?</span><span class="sxs-lookup"><span data-stu-id="64a72-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="64a72-185">Hvis udgiftsarten også bruges i Projektstyring og regnskab, skal du besvare de resterende spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="64a72-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="64a72-186">I modsat fald skal du gå til næste sektion.</span><span class="sxs-lookup"><span data-stu-id="64a72-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="64a72-187">Hvilke omkostningskonti skal bruges til følgende udgifter?</span><span class="sxs-lookup"><span data-stu-id="64a72-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="64a72-188">Omkostning</span><span class="sxs-lookup"><span data-stu-id="64a72-188">Cost</span></span>
    - <span data-ttu-id="64a72-189">Lønfordeling</span><span class="sxs-lookup"><span data-stu-id="64a72-189">Payroll allocation</span></span>
    - <span data-ttu-id="64a72-190">Værdi af omkostningerne ved IGVA</span><span class="sxs-lookup"><span data-stu-id="64a72-190">WIP-cost value</span></span>
    - <span data-ttu-id="64a72-191">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="64a72-191">Cost-item</span></span>
    - <span data-ttu-id="64a72-192">Værdielement for omkostning ved IGVA</span><span class="sxs-lookup"><span data-stu-id="64a72-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="64a72-193">Periodiseret tab</span><span class="sxs-lookup"><span data-stu-id="64a72-193">Accrued loss</span></span>
    - <span data-ttu-id="64a72-194">Periodiseret tab for IGVA</span><span class="sxs-lookup"><span data-stu-id="64a72-194">WIP-accrued loss</span></span>

- <span data-ttu-id="64a72-195">Hvilke omsætningskonti skal bruges til følgende?</span><span class="sxs-lookup"><span data-stu-id="64a72-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="64a72-196">Faktureret omsætning</span><span class="sxs-lookup"><span data-stu-id="64a72-196">Invoiced revenue</span></span>
    - <span data-ttu-id="64a72-197">Periodiseret omsætning - salgsværdi</span><span class="sxs-lookup"><span data-stu-id="64a72-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="64a72-198">IGVA - salgsværdi</span><span class="sxs-lookup"><span data-stu-id="64a72-198">WIP-sales value</span></span>
    - <span data-ttu-id="64a72-199">Periodiseret omsætning - produktion</span><span class="sxs-lookup"><span data-stu-id="64a72-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="64a72-200">IGVA - produktion</span><span class="sxs-lookup"><span data-stu-id="64a72-200">WIP-production</span></span>
    - <span data-ttu-id="64a72-201">Periodiseret omsætning - overskud</span><span class="sxs-lookup"><span data-stu-id="64a72-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="64a72-202">IGVA - overskud</span><span class="sxs-lookup"><span data-stu-id="64a72-202">WIP-profit</span></span>
    - <span data-ttu-id="64a72-203">Periodiseret omsætning - abonnement</span><span class="sxs-lookup"><span data-stu-id="64a72-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="64a72-204">IGVA - abonnement</span><span class="sxs-lookup"><span data-stu-id="64a72-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="64a72-205">Skatter</span><span class="sxs-lookup"><span data-stu-id="64a72-205">Taxes</span></span>

<span data-ttu-id="64a72-206">I forbindelse med udgiftsrelateret moms skal du angive, hvad der er medtaget eller aktiveret i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="64a72-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="64a72-207">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="64a72-207">**Decisions:**</span></span>

- <span data-ttu-id="64a72-208">Er moms inkluderet i udgiftsbeløbene?</span><span class="sxs-lookup"><span data-stu-id="64a72-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="64a72-209">Skal momsopkrævning aktiveres for udgifter?</span><span class="sxs-lookup"><span data-stu-id="64a72-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="64a72-210">Når du planlægger finanskontoen, og såfremt du besluttede dig for at anvende de amerikanske regler for moms og importmoms, kan du ikke aktivere momsopkrævning for udgifter.</span><span class="sxs-lookup"><span data-stu-id="64a72-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="64a72-211">(Hvis du vil anvende de amerikanske regler for moms og importmoms, skal du angive indstillingen **Anvend regler for momsbeskatning** til **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="64a72-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="64a72-212">Politikker</span><span class="sxs-lookup"><span data-stu-id="64a72-212">Policies</span></span>

<span data-ttu-id="64a72-213">Ved at oprette politikker for udgiftsrapporter kan du hjælpe din organisation med at spare tid og penge, når medarbejderne afholder udgifter på dennes vegne.</span><span class="sxs-lookup"><span data-stu-id="64a72-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="64a72-214">Politikker er med til at sikre, at medarbejdere holder sig indenfor budgettet, stiller alle påkrævede oplysninger til rådighed og kun bruger penge, når de har brug for det.</span><span class="sxs-lookup"><span data-stu-id="64a72-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="64a72-215">Du skal træffe følgende beslutninger for hver udgiftsrapportpolitik og de enkelte politikker for godkendelse af udgiftsrapporter, som du opretter.</span><span class="sxs-lookup"><span data-stu-id="64a72-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="64a72-216">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="64a72-216">**Decisions:**</span></span>

- <span data-ttu-id="64a72-217">Hvad er navnet på politikken?</span><span class="sxs-lookup"><span data-stu-id="64a72-217">What is the name of the policy?</span></span>
- <span data-ttu-id="64a72-218">Hvad er udgiftspolitikken for?</span><span class="sxs-lookup"><span data-stu-id="64a72-218">What is the expense policy for?</span></span>
- <span data-ttu-id="64a72-219">Hvis du tidligere har besluttet dig for at aktivere interne udgifter, hvilke virksomheder i organisationen, gælder denne politik så for?</span><span class="sxs-lookup"><span data-stu-id="64a72-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="64a72-220">Hvornår træder politikken i kraft?</span><span class="sxs-lookup"><span data-stu-id="64a72-220">When does the policy become effective?</span></span>
- <span data-ttu-id="64a72-221">Hvornår udløber politikken?</span><span class="sxs-lookup"><span data-stu-id="64a72-221">When does the policy expire?</span></span>
- <span data-ttu-id="64a72-222">Hvad er politikreglen?</span><span class="sxs-lookup"><span data-stu-id="64a72-222">What is the policy rule?</span></span>
- <span data-ttu-id="64a72-223">Hvad er udfaldet af politikreglen?</span><span class="sxs-lookup"><span data-stu-id="64a72-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]