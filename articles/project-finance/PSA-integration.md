---
title: Oversigt over Project Service Automation
description: Dette emne indeholder oplysninger om løsningen til integration af Dynamics 365 Project Service Automation i Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750567"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="014e7-103">Oversigt over Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="014e7-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="014e7-104">Integrationsløsningen for Project Service Automation til Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster med Dynamics 365 Finance og Dynamics 365 Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="014e7-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="014e7-105">De integrationsskabeloner, der er tilgængelige sammen med dataintegrationsfunktionen, aktiverer flowet af projekter, projektkontrakter, projektkontraktlinjer, milepæle for projektkontraktlinjer, projektopgaver, udgiftstransaktionskategorier, tidsestimater samt udgiftsestimater fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="014e7-106">Hvis du bruger version 7.3.0, skal du installere KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="014e7-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="014e7-107">Du kan derefter integrere fastprisprojekter.</span><span class="sxs-lookup"><span data-stu-id="014e7-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="014e7-108">Hvis du bruger version 7.3.0, og du sender gebyrtransaktioner over fra Project Service Automation, skal du installere KB 4345320 for at inkludere disse gebyrer i projektfakturaen.</span><span class="sxs-lookup"><span data-stu-id="014e7-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="014e7-109">Hvis du bruger versoin 8.0, vil du kunne anvende integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner.</span><span class="sxs-lookup"><span data-stu-id="014e7-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="014e7-110">Hvis du bruger version 8.0.1 eller nyere, kan du synkronisere de faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="014e7-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="014e7-111">Før du kan integrere Project Service Automation Finance, skal du konfigurere integrationsparametrene for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="014e7-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="014e7-112">Du kan finde flere oplysninger i [Integrationsparametrene for Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="014e7-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="014e7-113">Denne integrationsløsning aktiverer direkte synkronisering i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="014e7-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="014e7-114">Vedligehold projektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="014e7-115">Opret projekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="014e7-116">Vedligehold projektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="014e7-117">Vedligehold milepæle for projektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="014e7-118">Vedligehold projektopgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="014e7-119">Vedligehold udgiftstransaktionskategorier i Finance, og synkroniser dem direkte fra Finance til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="014e7-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="014e7-120">Opret timeestimater for projekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="014e7-121">Opret udgiftsestimater for projekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="014e7-122">Opret faktiske oplysninger for projekttid, udgifter og gebyrer i Project Service Automation, og opret projekttransaktioner i integrationskladden for Project Service Automation, så de kan bogføres i Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="014e7-123">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="014e7-123">Data synchronization</span></span>

<span data-ttu-id="014e7-124">I følgende illustration vises, hvordan data synkroniseres som led i integrationen mellem Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="014e7-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="014e7-125">Ikke alle skabeloner er tilgængelige i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="014e7-125">Not all templates are currently available.</span></span> <span data-ttu-id="014e7-126">Skabelonerne udgives, efterhånden som de er fuldført.</span><span class="sxs-lookup"><span data-stu-id="014e7-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="014e7-127">[![Integration af Project Service Automation med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="014e7-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="014e7-128">Systemkrav til Finance</span><span class="sxs-lookup"><span data-stu-id="014e7-128">System requirements for Finance</span></span>

<span data-ttu-id="014e7-129">Hvis du vil bruge integrationsløsningen Project Service Automation til Finance, skal du installere Enterprise Edition 7.3 med platformsopdatering 12 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="014e7-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="014e7-130">Systemkrav for Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="014e7-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="014e7-131">Hvis du vil bruge integrationsløsningen Project Service Automation til Finance, skal du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="014e7-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="014e7-132">Dynamics 365 Project Service Automation version 9.0.0.0 eller en nyere version</span><span class="sxs-lookup"><span data-stu-id="014e7-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="014e7-133">Kundeemne til kontantløsning til Dynamics 365 Sales, version 1.14.0.0 (v14) eller nyere</span><span class="sxs-lookup"><span data-stu-id="014e7-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="014e7-134">Project Service Automation til Finance-løsningen til Dynamics 365 Project Service Automation version 1.0.0.0 eller nyere</span><span class="sxs-lookup"><span data-stu-id="014e7-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="014e7-135">Installer integrationsløsningen Project Service Automation til Finance i din forekomst af Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="014e7-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="014e7-136">Hent integrationsløsningen Project Service Automation til Finance fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg instruktionerne, der leveres sammen med løsningen.</span><span class="sxs-lookup"><span data-stu-id="014e7-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
