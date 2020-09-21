---
title: Synkroniser projektestimater direkte fra Project Service Automation til Finance and Operations
description: Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere estimater for projekttimer og projektudgifter direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750533"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="283d4-103">Synkroniser projektestimater direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="283d4-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="283d4-104">Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere estimater for projekttimer og projektudgifter direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="283d4-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="283d4-105">Integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.</span><span class="sxs-lookup"><span data-stu-id="283d4-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="283d4-106">Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="283d4-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="283d4-107">Dataflow for Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="283d4-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="283d4-108">Integrationsløsningen for Project Service Automation til Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster med Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="283d4-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="283d4-109">De integrationsskabeloner, der er tilgængelige i forbindelse med funktionen til dataintegration, muliggør dataflow om timeestimater og estimater for projektudgifter fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="283d4-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="283d4-110">I følgende illustration vises, hvordan dataene synkroniseres mellem Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="283d4-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="283d4-111">[![Dataflow til integration af Project Service Automation med Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="283d4-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="283d4-112">Projektets timeestimater</span><span class="sxs-lookup"><span data-stu-id="283d4-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="283d4-113">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="283d4-113">Template and tasks</span></span>

<span data-ttu-id="283d4-114">Hvis du vil have adgang til den tilgængelige skabelon, skal du i Microsoft Power Apps Administration vælge **Projekter** og derefter vælge **Nyt projekt** i øverste højre hjørne for at vælge offentligt tilgængelige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="283d4-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="283d4-115">Følgende skabelon og underliggende opgaver bruges til at synkronisere projekters timeestimater fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="283d4-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="283d4-116">**Navnet på skabelonen i dataintegration:** Projektets timeestimater (PSA til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="283d4-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="283d4-117">**Navnet på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="283d4-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="283d4-118">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="283d4-118">Transaction relationships</span></span>
    - <span data-ttu-id="283d4-119">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="283d4-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="283d4-120">Objektsæt</span><span class="sxs-lookup"><span data-stu-id="283d4-120">Entity set</span></span>

| <span data-ttu-id="283d4-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="283d4-121">Project Service Automation</span></span> | <span data-ttu-id="283d4-122">Økonomi</span><span class="sxs-lookup"><span data-stu-id="283d4-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="283d4-123">Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="283d4-123">Project tasks</span></span>              | <span data-ttu-id="283d4-124">Integrationsobjekt for projektets timeestimater</span><span class="sxs-lookup"><span data-stu-id="283d4-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="283d4-125">Objektflow</span><span class="sxs-lookup"><span data-stu-id="283d4-125">Entity flow</span></span>

<span data-ttu-id="283d4-126">Projektets timeestimater administreres i Project Service Automation, og de synkroniseres med Finance som prognose for projektets timer.</span><span class="sxs-lookup"><span data-stu-id="283d4-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="283d4-127">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="283d4-127">Prerequisites</span></span>

<span data-ttu-id="283d4-128">Før der kan ske synkronisering af projektets timeestimater, skal du synkronisere projekter, projektopgaver og projektets udgiftstransaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="283d4-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="283d4-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="283d4-129">Power Query</span></span>

<span data-ttu-id="283d4-130">I skabelonen for projektets timeestimater skal du bruge Microsoft Power-forespørgsel til Excel til at fuldføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="283d4-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="283d4-131">Angiv id'et for standardprognosemodellen, der skal bruges, når integrationen opretter nye timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="283d4-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="283d4-132">Filtrerer alle ressourcespecifikke poster i opgaven, der ikke kan integreres i timeprognoserne.</span><span class="sxs-lookup"><span data-stu-id="283d4-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="283d4-133">Filtrerer eventuelle tomme rækker i transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="283d4-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="283d4-134">Hvis du ikke gør dette, kan det resultere i forkerte timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="283d4-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="283d4-135">Angiv id'et for standardprognosemodellen</span><span class="sxs-lookup"><span data-stu-id="283d4-135">Set the default forecast model ID</span></span>

<span data-ttu-id="283d4-136">Hvis du vil opdatere id'et for standardprognosemodellen i skabelonen, skal du klikke på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="283d4-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="283d4-137">Vælg derefter linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="283d4-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="283d4-138">Hvis du bruger standardtimeestimaterne for projektet (PSA til Fin og Ops), skal du i Power Query markere den sidst **Indsatte betingelse** i listen **Anvendte trin**.</span><span class="sxs-lookup"><span data-stu-id="283d4-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="283d4-139">I feltet **Funktion** skal du erstatte **O\_prognose** med navnet din prognosemodels id, som skal bruges sammen med integrationen.</span><span class="sxs-lookup"><span data-stu-id="283d4-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="283d4-140">Standardskabelonen har et prognosemodel-id fra demonstrationsdataene.</span><span class="sxs-lookup"><span data-stu-id="283d4-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="283d4-141">Hvis du opretter en ny skabelon, skal du tilføje denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="283d4-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="283d4-142">I Power Query skal du vælge **Tilføj betinget kolonne**, og angiv et navn for den nye kolonnen, som f.eks **Model-id**.</span><span class="sxs-lookup"><span data-stu-id="283d4-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="283d4-143">Angiv betingelsen for kolonnen, hvor du, hvis projektopgaven ikke er null, skal \<angive prognosemodel-id'et\>. Ellers null.</span><span class="sxs-lookup"><span data-stu-id="283d4-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="283d4-144">Filtrering af ressourcespecifikke poster</span><span class="sxs-lookup"><span data-stu-id="283d4-144">Filter out resource-specific records</span></span>

<span data-ttu-id="283d4-145">Skabelonen for projektets timeestimater (PSA til Fin og Ops) har et standardfilter, der fjerner alle ressourcespecifikke poster.</span><span class="sxs-lookup"><span data-stu-id="283d4-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="283d4-146">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="283d4-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="283d4-147">Vælg linket **Avanceret forespørgsel og filtrering**, der skal filtreres i kolonnen **msdyn\_erlinjeopgave**, så det kun er poster med **Falsk**, der inkluderes.</span><span class="sxs-lookup"><span data-stu-id="283d4-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="283d4-148">Filtrerer tomme rækker fra i transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="283d4-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="283d4-149">Du skal tilføje et filter for at fjerne alle rækker, der har tomme transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="283d4-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="283d4-150">Denne opgave er obligatorisk, uanset om du bruger standardskabelonen eller opretter din egen skabelon.</span><span class="sxs-lookup"><span data-stu-id="283d4-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="283d4-151">Dette filter fjerner eventuelle oversigtsrækker fra Project Service Automation, hvilket kan medføre, at timeprognoserne i Finance er forkerte.</span><span class="sxs-lookup"><span data-stu-id="283d4-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="283d4-152">Vælg linket **Avanceret forespørgsel og filtrering** for at filtrere null-poster fra i kolonnen **msdyn\_transaktionskategori\_værdi**.</span><span class="sxs-lookup"><span data-stu-id="283d4-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="283d4-153">Skabelon for tilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="283d4-153">Template mapping in Data integration</span></span>

<span data-ttu-id="283d4-154">I følgende illustration vises et eksempel på tilknytningen mellem skabelonopgaver i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="283d4-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="283d4-155">I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="283d4-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="283d4-156">[![Skabelontilknytning](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="283d4-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="283d4-157">Projektets udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="283d4-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="283d4-158">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="283d4-158">Template and tasks</span></span>

<span data-ttu-id="283d4-159">Følgende skabelon og underliggende opgaver bruges til at synkronisere projekters udgiftsestimater fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="283d4-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="283d4-160">**Navnet på skabelonen i dataintegration:** Projektets udgiftsestimater (PSA til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="283d4-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="283d4-161">**Navnet på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="283d4-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="283d4-162">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="283d4-162">Transaction relationships</span></span> 
    - <span data-ttu-id="283d4-163">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="283d4-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="283d4-164">Objektsæt</span><span class="sxs-lookup"><span data-stu-id="283d4-164">Entity set</span></span>

| <span data-ttu-id="283d4-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="283d4-165">Project Service Automation</span></span> | <span data-ttu-id="283d4-166">Økonomi</span><span class="sxs-lookup"><span data-stu-id="283d4-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="283d4-167">Transaktionsforbindelser</span><span class="sxs-lookup"><span data-stu-id="283d4-167">Transaction Connections</span></span>    | <span data-ttu-id="283d4-168">Integrationsobjekt for projekttransaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="283d4-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="283d4-169">Estimatlinjer</span><span class="sxs-lookup"><span data-stu-id="283d4-169">Estimate Lines</span></span>             | <span data-ttu-id="283d4-170">Integrationsobjekt for projektets udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="283d4-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="283d4-171">Objektflow</span><span class="sxs-lookup"><span data-stu-id="283d4-171">Entity flow</span></span>

<span data-ttu-id="283d4-172">Projektets udgiftsestimater administreres i Project Service Automation, og de synkroniseres med Finance som prognose for projektets udgifter.</span><span class="sxs-lookup"><span data-stu-id="283d4-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="283d4-173">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="283d4-173">Prerequisites</span></span>

<span data-ttu-id="283d4-174">Før der kan ske synkronisering af projektets udgiftsestimater, skal du synkronisere projekter, projektopgaver og projektets udgiftstransaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="283d4-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="283d4-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="283d4-175">Power Query</span></span>

<span data-ttu-id="283d4-176">I skabelonen for projektets udgiftsestimater skal du bruge Power Query til at fuldføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="283d4-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="283d4-177">Filter, så det kun omfatter linjeposter for udgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="283d4-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="283d4-178">Angiv id'et for standardprognosemodellen, der skal bruges, når integrationen opretter nye timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="283d4-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="283d4-179">Transformer faktureringstyperne.</span><span class="sxs-lookup"><span data-stu-id="283d4-179">Transform the billing types.</span></span>
- <span data-ttu-id="283d4-180">Transformer transaktionstyperne.</span><span class="sxs-lookup"><span data-stu-id="283d4-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="283d4-181">Filter, så det kun omfatter linjer for udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="283d4-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="283d4-182">Skabelonen for projektets udgiftsestimater (PSA til Fin og Ops) har et standardfilter, der kun indeholder udgiftslinjer i integrationen.</span><span class="sxs-lookup"><span data-stu-id="283d4-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="283d4-183">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="283d4-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="283d4-184">Vælg opgaven **Transaktionsrelationer**, og klik derefter på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="283d4-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="283d4-185">Vælg linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="283d4-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="283d4-186">Filtrer kolonnen **msdyn\_transaktionstype1**, så den kun inkluderer **msdyn\_estimalinje**.</span><span class="sxs-lookup"><span data-stu-id="283d4-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="283d4-187">Angiv id'et for standardprognosemodellen</span><span class="sxs-lookup"><span data-stu-id="283d4-187">Set the default forecast model ID</span></span>

<span data-ttu-id="283d4-188">Hvis du vil opdatere id'et for standardprognosemodellen i skabelonen, skal du vælge opgaven **Udgiftsestimater** og derefter klikke på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="283d4-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="283d4-189">Vælg linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="283d4-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="283d4-190">Hvis du bruger standardskabelonen for projektets udgiftsestimater (PSA til Fin og Ops), skal du i Power Query markere den første **Indsatte betingelse** fra sektionen **Anvendte trin**.</span><span class="sxs-lookup"><span data-stu-id="283d4-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="283d4-191">I feltet **Funktion** skal du erstatte **O\_prognose** med navnet din prognosemodels id, som skal bruges sammen med integrationen.</span><span class="sxs-lookup"><span data-stu-id="283d4-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="283d4-192">Standardskabelonen har et prognosemodel-id fra demonstrationsdataene.</span><span class="sxs-lookup"><span data-stu-id="283d4-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="283d4-193">Hvis du opretter en ny skabelon, skal du tilføje denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="283d4-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="283d4-194">I Power Query skal du vælge **Tilføj betinget kolonne**, og angiv et navn for den nye kolonnen, som f.eks **Model-id**.</span><span class="sxs-lookup"><span data-stu-id="283d4-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="283d4-195">Angiv betingelsen for kolonnen, hvor, hvis Estimatlinje-id'et ikke er null, du skal \<angive prognosemodel-id'et\>. Ellers null.</span><span class="sxs-lookup"><span data-stu-id="283d4-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="283d4-196">Transformer faktureringstyperne</span><span class="sxs-lookup"><span data-stu-id="283d4-196">Transform the billing types</span></span>

<span data-ttu-id="283d4-197">Skabelonen for projektets udgiftsestimater (PSA til Fin og Ops) indeholder en betinget kolonne, der bruges til at transformere de faktureringstyper, der modtages fra Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="283d4-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="283d4-198">Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne.</span><span class="sxs-lookup"><span data-stu-id="283d4-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="283d4-199">Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="283d4-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="283d4-200">Angiv et navn til den nye kolonne, f.eks. **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="283d4-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="283d4-201">Angiv derefter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="283d4-201">Then enter the following condition:</span></span>

<span data-ttu-id="283d4-202">Hvis **msdyn\_faktureringstype** = 192350000, er den ikke **Fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="283d4-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="283d4-203">Hvis **msdyn\_faktureringstype** = 192350001, er den **Fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="283d4-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="283d4-204">Hvis **msdyn\_faktureringstype** = 192350002, er den **Komplementerende**</span><span class="sxs-lookup"><span data-stu-id="283d4-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="283d4-205">ellers **Ikketilgængelige**</span><span class="sxs-lookup"><span data-stu-id="283d4-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="283d4-206">Transformer transaktionstyperne</span><span class="sxs-lookup"><span data-stu-id="283d4-206">Transform the transaction types</span></span>

<span data-ttu-id="283d4-207">Skabelonen for projektets udgiftsestimater (PSA til Fin og Ops) indeholder en betinget kolonne, der bruges til at transformere de transaktionstyper, der modtages fra Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="283d4-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="283d4-208">Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne.</span><span class="sxs-lookup"><span data-stu-id="283d4-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="283d4-209">Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="283d4-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="283d4-210">Angiv et navn til den nye kolonne, f.eks. **Transaktionstype**.</span><span class="sxs-lookup"><span data-stu-id="283d4-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="283d4-211">Angiv derefter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="283d4-211">Then enter the following condition:</span></span>

<span data-ttu-id="283d4-212">Hvis **msdyn\_transaktionstypekode** = 192350000, er det **Omkostninger**</span><span class="sxs-lookup"><span data-stu-id="283d4-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="283d4-213">Hvis **msdyn\_transaktionstypekode** = 192350005, så er det **Salg**</span><span class="sxs-lookup"><span data-stu-id="283d4-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="283d4-214">Ellers er det **null**</span><span class="sxs-lookup"><span data-stu-id="283d4-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="283d4-215">Skabelon for tilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="283d4-215">Template mapping in Data integration</span></span>

<span data-ttu-id="283d4-216">I følgende illustrationer vises eksempler på tilknytninger mellem skabelonopgaver i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="283d4-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="283d4-217">I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="283d4-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="283d4-218">[![Skabelontilknytning](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="283d4-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="283d4-219">[![Skabelontilknytning](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="283d4-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
