---
title: Synkroniser projektopgaver direkte fra Project Service Automation til Finance and Operations
description: Dette emne beskriver den skabelon og den underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288912"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f693e-103">Synkroniser projektopgaver direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f693e-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f693e-104">Dette emne beskriver den skabelon og den underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f693e-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="f693e-105">Integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.</span><span class="sxs-lookup"><span data-stu-id="f693e-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="f693e-106">Hvis du bruger Enterprise Edition 7.3.0, kan du, efter at du har installeret KB 4132657 og KB 4132660, bruge skabelonerne til at integrere projektopgaver, kategorier for udgiftstransaktioner, timeestimater, udgiftsestimater og faktiske oplysninger samt konfigurere funktionslåsning.</span><span class="sxs-lookup"><span data-stu-id="f693e-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="f693e-107">Hvis du vil nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="f693e-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="f693e-108">Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="f693e-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="f693e-109">Dataflow for Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="f693e-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="f693e-110">Integrationsløsningen for Project Service Automation til Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster med Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="f693e-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="f693e-111">Den integrationsskabelon, der er tilgængelig i forbindelse med funktionen til dataintegration, aktiverer dataflow om projektopgaver fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f693e-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f693e-112">I følgende illustration vises, hvordan dataene synkroniseres mellem Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="f693e-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="f693e-113">[![Dataflow til integration af Project Service Automation med Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f693e-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="f693e-114">Skabelon og opgave</span><span class="sxs-lookup"><span data-stu-id="f693e-114">Template and task</span></span>

<span data-ttu-id="f693e-115">Hvis du vil have adgang til skabelonen, skal du i Microsoft Power Apps Administration vælge **Projekter** og derefter vælge **Nyt projekt** i øverste højre hjørne for at vælge offentligt tilgængelige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="f693e-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f693e-116">Følgende skabelon og underliggende opgave bruges til at synkronisere projektopgaver fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="f693e-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="f693e-117">**Navnet på skabelonen i dataintegration:** Projektopgaver (PSA til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="f693e-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f693e-118">**Navnet på opgaven i projektet:** Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="f693e-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="f693e-119">Inden synkroniseringen mellem projektopgaver kan ske, skal du synkronisere projektkontrakterne og projekterne.</span><span class="sxs-lookup"><span data-stu-id="f693e-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="f693e-120">Objektsæt</span><span class="sxs-lookup"><span data-stu-id="f693e-120">Entity set</span></span>

| <span data-ttu-id="f693e-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f693e-121">Project Service Automation</span></span> | <span data-ttu-id="f693e-122">Økonomi</span><span class="sxs-lookup"><span data-stu-id="f693e-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="f693e-123">Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="f693e-123">Project Tasks</span></span>              | <span data-ttu-id="f693e-124">Objekt til integration af projektopgave</span><span class="sxs-lookup"><span data-stu-id="f693e-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="f693e-125">Objektflow</span><span class="sxs-lookup"><span data-stu-id="f693e-125">Entity flow</span></span>

<span data-ttu-id="f693e-126">'Projektopgaver administreres i Project Service Automation, og de synkroniseres med Finance som projektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f693e-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f693e-127">Opsætning af forudsætninger og tilknytning</span><span class="sxs-lookup"><span data-stu-id="f693e-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="f693e-128">Inden synkroniseringen mellem projektopgaver kan ske, skal du synkronisere projektkontrakterne og projekterne.</span><span class="sxs-lookup"><span data-stu-id="f693e-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="f693e-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="f693e-129">Power Query</span></span>

<span data-ttu-id="f693e-130">Du skal bruge Microsoft Power-forespørgsel til Excel til at filtrere data, hvis denne betingelse er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="f693e-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="f693e-131">Der er ressourcespecifikke poster i en projektopgave.</span><span class="sxs-lookup"><span data-stu-id="f693e-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="f693e-132">Hvis du skal bruge Power Query, skal du følge denne retningslinje:</span><span class="sxs-lookup"><span data-stu-id="f693e-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="f693e-133">Skabelonen for projektopgaver (PSA til Fin og Ops) har et standardfilter, der udelukker ressourcespecifikke poster fra en projektopgave ved at indstille filteret i **ErLinjenFalsk** til **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="f693e-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="f693e-134">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="f693e-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f693e-135">Skabelon for tilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="f693e-135">Template mapping in Data integration</span></span>

<span data-ttu-id="f693e-136">I følgende illustration vises et eksempel på tilknytningerne mellem skabelonopgaver i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="f693e-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="f693e-137">I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f693e-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f693e-138">[![Skabelontilknytning](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="f693e-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]