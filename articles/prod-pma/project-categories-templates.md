---
title: Synkroniser projekters udgiftskategorier mellem Finance and Operations og Project Service Automation
description: Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere projekters udgiftskategorier mellem Microsoft Dynamics 365 Finance og Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999844"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="1d215-103">Synkroniser projekters udgiftskategorier mellem Finance and Operations og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1d215-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1d215-104">Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere projekters udgiftskategorier mellem Dynamics 365 Finance og Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1d215-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="1d215-105">Integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.</span><span class="sxs-lookup"><span data-stu-id="1d215-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="1d215-106">Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="1d215-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="1d215-107">Hvis du bruger Enterprise Edition 7.3.0, kan du, efter at du har installeret KB 4132657 og KB 4132660, bruge skabelonerne til at integrere projektopgaver, kategorier for udgiftstransaktioner, timeestimater, udgiftsestimater og faktiske oplysninger samt konfigurere funktionslåsning.</span><span class="sxs-lookup"><span data-stu-id="1d215-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="1d215-108">Hvis du vil nulstille regnskabsfordelingerne, anbefales det, at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="1d215-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="1d215-109">Dataflow til Project Service Automation og Finance</span><span class="sxs-lookup"><span data-stu-id="1d215-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="1d215-110">Integrationsløsningen til Project Service Automation og Finance bruger funktionen dataintegration til at synkronisere data på tværs af forekomster med Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="1d215-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="1d215-111">De integrationsskabeloner, der er tilgængelige i forbindelse med funktionen til dataintegration, muliggør dataflow om kategorier for projekters udgiftstransaktioner mellem Finance og Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1d215-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="1d215-112">Hvis projekters udgiftskategorier er håndteret i Finance, foretages integrationsflowet først fra Finance til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1d215-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="1d215-113">Integrations-id'erne for projekters udgiftskategorierne opdateres derefter automatisk via synkronisering fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="1d215-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1d215-114">Hvis projekters udgiftskategorier er håndteret i Project Service Automation, foretages integrationsflowet først fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="1d215-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="1d215-115">Projektkategorierne skal allerede være konfigureret i Finance, før der synkroniseres fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1d215-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="1d215-116">Synkroniser derefter fra Finance tilbage til Project Service Automation, og derefter fra Project Service Automation til Finance igen.</span><span class="sxs-lookup"><span data-stu-id="1d215-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="1d215-117">På denne måde kan du være med til at sikre, at kategorierne er sammenkædet, og at der ikke er oprettet dubletter.</span><span class="sxs-lookup"><span data-stu-id="1d215-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="1d215-118">Projekters udgiftskategorier håndteres som regel i Finance.</span><span class="sxs-lookup"><span data-stu-id="1d215-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="1d215-119">Men hvis de ikke gør, eller hvis der allerede er oprettet udgiftskategorier i Project Service Automation, skal du først synkronisere ved hjælp af skabelonen for kategorierne for projekters udgiftstransaktioner (PSA til Fin og Ops).</span><span class="sxs-lookup"><span data-stu-id="1d215-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="1d215-120">Synkroniser derefter ved hjælp af skabelonen for kategorier for projekters udgiftstransaktioner (Fin og Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="1d215-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="1d215-121">Derefter skal du køre synkroniseringen fra Project Service Automation til Finance én gang mere.</span><span class="sxs-lookup"><span data-stu-id="1d215-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="1d215-122">Hvis du først synkroniserer fra Project Service Automation, skal følgende krav være opfyldt i Finance, før synkroniseringen køres:</span><span class="sxs-lookup"><span data-stu-id="1d215-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="1d215-123">Den delte kategori, der stemmer overens med den projektkategori, der er konfigureret i Project Service Automation, skal findes, og den skal være aktiveret for både **Projekt** og **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="1d215-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="1d215-124">For hver af de enkelte juridiske enheder i Finance, der skal integreres med, skal følgende projektkategorier findes:</span><span class="sxs-lookup"><span data-stu-id="1d215-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="1d215-125">**Projektkategori** findes.</span><span class="sxs-lookup"><span data-stu-id="1d215-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="1d215-126">**Brug i udgift** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="1d215-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="1d215-127">**Aktiv i kladde** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="1d215-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="1d215-128">**Transaktionstype** er angivet til **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="1d215-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="1d215-129">I følgende illustration vises, hvordan dataene synkroniseres mellem Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="1d215-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="1d215-130">[![Dataflow til integration af Project Service Automation med Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="1d215-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="1d215-131">Synkronisering af projekters udgiftskategorier mellem Finance og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1d215-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="1d215-132">Skabelon og opgave</span><span class="sxs-lookup"><span data-stu-id="1d215-132">Template and task</span></span>

<span data-ttu-id="1d215-133">Hvis du vil have adgang til skabelonen, skal du i Microsoft Power Apps Administration vælge **Projekter** og derefter vælge **Nyt projekt** i øverste højre hjørne for at vælge offentligt tilgængelige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="1d215-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1d215-134">Følgende skabelon og underliggende opgave bruges til at synkronisere projekters udgiftskategorier fra Finance til Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="1d215-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="1d215-135">**Navnet på skabelonen i dataintegration:** Kategorierne for projektets udgiftstransaktioner (Fin og Ops til PSA)</span><span class="sxs-lookup"><span data-stu-id="1d215-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="1d215-136">**Navnet på opgaven i projektet:** Synkroniser kategorier til PSA</span><span class="sxs-lookup"><span data-stu-id="1d215-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="1d215-137">Objektsæt</span><span class="sxs-lookup"><span data-stu-id="1d215-137">Entity set</span></span>

| <span data-ttu-id="1d215-138">Økonomi</span><span class="sxs-lookup"><span data-stu-id="1d215-138">Finance</span></span>                           | <span data-ttu-id="1d215-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1d215-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="1d215-140">Integrationsobjekt for kategorier</span><span class="sxs-lookup"><span data-stu-id="1d215-140">Integration entity for categories</span></span> | <span data-ttu-id="1d215-141">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="1d215-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="1d215-142">Objektflow</span><span class="sxs-lookup"><span data-stu-id="1d215-142">Entity flow</span></span>

<span data-ttu-id="1d215-143">Projektets udgiftskategorier administreres i Finance, og de synkroniseres med Project Service Automation som transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="1d215-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="1d215-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="1d215-144">Power Query</span></span>

<span data-ttu-id="1d215-145">Når du synkroniserer med Project Service Automation, skal du bruge Microsoft Power-forespørgsel til Excel til at angive faktureringstypen for transaktionskategorien.</span><span class="sxs-lookup"><span data-stu-id="1d215-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="1d215-146">Skabelonerne for kategorierne for projektets udgiftstransaktioner (Fin og Ops til PSA) indeholder en standardkolonne og tilknytning.</span><span class="sxs-lookup"><span data-stu-id="1d215-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="1d215-147">Hvis du opretter din egen skabelon, skal du tilføje en betinget kolonne i Power Query.</span><span class="sxs-lookup"><span data-stu-id="1d215-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="1d215-148">Følg disse trin.</span><span class="sxs-lookup"><span data-stu-id="1d215-148">Follow these steps.</span></span>

1. <span data-ttu-id="1d215-149">Klik på pilen for at åbne tilknytningen mellem opgaven for projektets udgiftskategorier i skabelonen for kategorierne for projektets udgiftstransaktioner (Fin og Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="1d215-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="1d215-150">Klik på linket **Avanceret forespørgsel og filtrering** for at åbne Power Query.</span><span class="sxs-lookup"><span data-stu-id="1d215-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="1d215-151">Vælg **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="1d215-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="1d215-152">Angiv et navn til den nye kolonne, f.eks. **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="1d215-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="1d215-153">Angiv følgende betingelse: **Hvis KATEGORIID ikke er lig med null, så 19235001, ellers null**.</span><span class="sxs-lookup"><span data-stu-id="1d215-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="1d215-154">Klik på **OK** i kolonnen.</span><span class="sxs-lookup"><span data-stu-id="1d215-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="1d215-155">Sørg for at tilknytte denne nye kolonne på tilknytningssiden.</span><span class="sxs-lookup"><span data-stu-id="1d215-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="1d215-156">I følgende illustration vises et eksempel på tilknytningen mellem skabelonopgaver i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="1d215-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="1d215-157">I tilknytningen vises de feltoplysninger, der synkroniseres fra Finance til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1d215-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="1d215-158">[![Skabelontilknytning af projekters udgiftskategorier til Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1d215-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="1d215-159">Synkronisering af projekters udgiftskategorier fra Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="1d215-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="1d215-160">Skabelon og opgave</span><span class="sxs-lookup"><span data-stu-id="1d215-160">Template and task</span></span>

<span data-ttu-id="1d215-161">Følgende skabelon og underliggende opgave bruges til at synkronisere projekters udgiftskategorier fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="1d215-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1d215-162">**Navnet på skabelonen i dataintegration:** Kategorierne for projektets udgiftstransaktioner (PSA til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="1d215-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1d215-163">**Navnet på opgaven i projektet:** Synkroniser kategorier til Fin Ops</span><span class="sxs-lookup"><span data-stu-id="1d215-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="1d215-164">Objektsæt</span><span class="sxs-lookup"><span data-stu-id="1d215-164">Entity set</span></span>

| <span data-ttu-id="1d215-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1d215-165">Project Service Automation</span></span> | <span data-ttu-id="1d215-166">Økonomi</span><span class="sxs-lookup"><span data-stu-id="1d215-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="1d215-167">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="1d215-167">Transaction categories</span></span>     | <span data-ttu-id="1d215-168">Integrationsobjekt for kategorier</span><span class="sxs-lookup"><span data-stu-id="1d215-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="1d215-169">Objektflow</span><span class="sxs-lookup"><span data-stu-id="1d215-169">Entity flow</span></span>

<span data-ttu-id="1d215-170">Projektets udgiftskategorier administreres i Finance, og de synkroniseres med Project Service Automation som transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="1d215-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="1d215-171">Synkroniseringen tilbage til Finance opdaterer projektets kategori i Finance med integrations-id'et fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1d215-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1d215-172">Skabelon for tilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="1d215-172">Template mapping in Data integration</span></span>

<span data-ttu-id="1d215-173">I følgende illustration vises et eksempel på tilknytningen mellem skabelonopgaver i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="1d215-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="1d215-174">I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="1d215-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1d215-175">[![Skabelontilknytning for Project Service Automation til Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1d215-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]