---
title: Konfigurer automatisk oprettelse af fakturaer
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer systemet til at oprette fakturaer automatisk.
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898119"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="5c417-103">Konfigurer automatisk oprettelse af fakturaer</span><span class="sxs-lookup"><span data-stu-id="5c417-103">Configure automated invoice creation</span></span>

<span data-ttu-id="5c417-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5c417-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5c417-105">Benyt følgende fremgangsmåde for at konfigurere en automatiseret fakturakørsel i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5c417-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="5c417-106">Gå til **Indstillinger** \> **Batchjobs**.</span><span class="sxs-lookup"><span data-stu-id="5c417-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="5c417-107">Opret et batchjob, og kald det **Opret fakturaer i Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="5c417-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="5c417-108">Navnet på batchjobbet skal indeholde udtrykket "opret fakturaer".</span><span class="sxs-lookup"><span data-stu-id="5c417-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="5c417-109">I feltet **Jobtype** skal du vælge **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="5c417-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="5c417-110">Som standard skal indstillingerne **Hyppighed: Dagligt** og **Er aktiv** angives til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5c417-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="5c417-111">Vælg **Kør arbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="5c417-111">Select **Run Workflow**.</span></span> <span data-ttu-id="5c417-112">I dialogboksen **Slå post op** kan du se tre arbejdsprocesser:</span><span class="sxs-lookup"><span data-stu-id="5c417-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="5c417-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="5c417-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="5c417-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="5c417-114">ProcessRunner</span></span>
    - <span data-ttu-id="5c417-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="5c417-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="5c417-116">Vælg **ProcessRunCaller** og derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5c417-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="5c417-117">I den næste dialogboks skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c417-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="5c417-118">En **slumre**-arbejdsproces efterfølges af en **proces**-arbejdsproces.</span><span class="sxs-lookup"><span data-stu-id="5c417-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="5c417-119">Du kan også vælge **ProcessRunner** i trin 5.</span><span class="sxs-lookup"><span data-stu-id="5c417-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="5c417-120">Når du derefter vælger **OK**, efterfølges en **proces**-arbejdsproces af en **slumre**-arbejdsproces.</span><span class="sxs-lookup"><span data-stu-id="5c417-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="5c417-121">Begge arbejdsprocesserne **ProcessRunCaller** og **ProcessRunner** opretter fakturaer.</span><span class="sxs-lookup"><span data-stu-id="5c417-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="5c417-122">**ProcessRunCaller** kalder på **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="5c417-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="5c417-123">**ProcessRunner** er den arbejdsproces, der rent faktisk opretter fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="5c417-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="5c417-124">Denne proces gennemgår alle de kontraktlinjer, der skal oprettes fakturaer for, og den opretter fakturaer for disse linjer.</span><span class="sxs-lookup"><span data-stu-id="5c417-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="5c417-125">Hvis du vil fastlægge, hvilke kontraktlinjer der skal oprettes fakturaer for, kigger jobbet på fakturaernes kørselsdatoer for kontraktlinjerne.</span><span class="sxs-lookup"><span data-stu-id="5c417-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="5c417-126">Hvis kontraktlinjer, der er knyttet til en kontrakt, har samme fakturakørselsdato, samles transaktionerne i én faktura, der indeholder to fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="5c417-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="5c417-127">Hvis der ikke findes transaktioner, som der skal oprettes fakturaer til, ignorerer jobbet fakturaoprettelse.</span><span class="sxs-lookup"><span data-stu-id="5c417-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="5c417-128">Når **ProcessRunner** er færdig med at køre, kalder processen på **ProcessRunCaller**, angiver sluttidspunktet og lukkes.</span><span class="sxs-lookup"><span data-stu-id="5c417-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="5c417-129">**ProcessRunCaller** starter derefter en timer, der kører i 24 timer fra det angivne sluttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="5c417-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="5c417-130">Når timeren afsluttes, lukkes **ProcessRunCaller**.</span><span class="sxs-lookup"><span data-stu-id="5c417-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="5c417-131">Batchprocesjobbet til oprettelse af fakturaer er et tilbagevendende job.</span><span class="sxs-lookup"><span data-stu-id="5c417-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="5c417-132">Hvis denne batchproces køres mange gange, oprettes der flere forekomster af jobbet, og der opstår fejl.</span><span class="sxs-lookup"><span data-stu-id="5c417-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="5c417-133">Du bør derfor kun starte batchprocessen én gang, og du bør kun genstarte den, hvis den holder op med at køre.</span><span class="sxs-lookup"><span data-stu-id="5c417-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="5c417-134">Batchfakturering kører kun for projektkontrakt linjer, der er konfigureret af fakturaplaner.</span><span class="sxs-lookup"><span data-stu-id="5c417-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="5c417-135">Der skal være konfigureret målepæle for en kontraktlinje med en faktureringsmetode med fast pris.</span><span class="sxs-lookup"><span data-stu-id="5c417-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="5c417-136">Der skal konfigureres en datobaseret fakturaplan for en projektkontraktlinje med en metode til fakturering af time og materiale.</span><span class="sxs-lookup"><span data-stu-id="5c417-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="5c417-137">Det samme gælder for en projektbaseret kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="5c417-137">The same applies to a project-based contract line.</span></span>     
