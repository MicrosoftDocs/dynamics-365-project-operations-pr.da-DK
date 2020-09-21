---
title: Synkroniser projektopgaver direkte fra Project Service Automation til Finance and Operations
description: Dette emne beskriver den skabelon og den underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
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
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750609"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synkroniser projektopgaver direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emne beskriver den skabelon og den underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE]
> - Integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.
> - Hvis du bruger Enterprise Edition 7.3.0, kan du, efter at du har installeret KB 4132657 og KB 4132660, bruge skabelonerne til at integrere projektopgaver, kategorier for udgiftstransaktioner, timeestimater, udgiftsestimater og faktiske oplysninger samt konfigurere funktionslåsning. Hvis du vil nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.
> - Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflow for Project Service Automation til Finance

Integrationsløsningen for Project Service Automation til Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster med Project Service Automation og Finance. Den integrationsskabelon, der er tilgængelig i forbindelse med funktionen til dataintegration, aktiverer dataflow om projektopgaver fra Project Service Automation til Finance.

I følgende illustration vises, hvordan dataene synkroniseres mellem Project Service Automation og Finance.

[![Dataflow til integration af Project Service Automation med Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Skabelon og opgave

Hvis du vil have adgang til skabelonen, skal du i Microsoft Power Apps Administration vælge **Projekter** og derefter vælge **Nyt projekt** i øverste højre hjørne for at vælge offentligt tilgængelige skabeloner.

Følgende skabelon og underliggende opgave bruges til at synkronisere projektopgaver fra Project Service Automation til Finance:

- **Navnet på skabelonen i dataintegration:** Projektopgaver (PSA til Fin og Ops)
- **Navnet på opgaven i projektet:** Projektopgaver

Inden synkroniseringen mellem projektopgaver kan ske, skal du synkronisere projektkontrakterne og projekterne.

## <a name="entity-set"></a>Objektsæt

| Project Service Automation | Økonomi                             |
|----------------------------|-------------------------------------|
| Projektopgaver              | Objekt til integration af projektopgave |

## <a name="entity-flow"></a>Objektflow

'Projektopgaver administreres i Project Service Automation, og de synkroniseres med Finance som projektaktiviteter.

## <a name="prerequisites-and-mapping-setup"></a>Opsætning af forudsætninger og tilknytning

Inden synkroniseringen mellem projektopgaver kan ske, skal du synkronisere projektkontrakterne og projekterne.

## <a name="power-query"></a>Power Query

Du skal bruge Microsoft Power-forespørgsel til Excel til at filtrere data, hvis denne betingelse er opfyldt:

- Der er ressourcespecifikke poster i en projektopgave.

Hvis du skal bruge Power Query, skal du følge denne retningslinje:

- Skabelonen for projektopgaver (PSA til Fin og Ops) har et standardfilter, der udelukker ressourcespecifikke poster fra en projektopgave ved at indstille filteret i **ErLinjenFalsk** til **Falsk**. Hvis du opretter din egen skabelon, skal du tilføje dette filter.

## <a name="template-mapping-in-data-integration"></a>Skabelon for tilknytning i dataintegration

I følgende illustration vises et eksempel på tilknytningerne mellem skabelonopgaver i dataintegration. I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Skabelontilknytning](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
