---
title: Synkroniser projekters udgiftskategorier mellem Finance and Operations og Project Service Automation
description: Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere projekters udgiftskategorier mellem Microsoft Dynamics 365 Finance og Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074311"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synkroniser projekters udgiftskategorier mellem Finance and Operations og Project Service Automation

[!include[banner](../includes/banner.md)]

Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere projekters udgiftskategorier mellem Dynamics 365 Finance og Dynamics 365 Project Service Automation.

> [!NOTE]
> - Integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.
> - Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.
> - Hvis du bruger Enterprise Edition 7.3.0, kan du, efter at du har installeret KB 4132657 og KB 4132660, bruge skabelonerne til at integrere projektopgaver, kategorier for udgiftstransaktioner, timeestimater, udgiftsestimater og faktiske oplysninger samt konfigurere funktionslåsning. Hvis du vil nulstille regnskabsfordelingerne, anbefales det, at du også installerer KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Dataflow til Project Service Automation og Finance

Integrationsløsningen til Project Service Automation og Finance bruger funktionen dataintegration til at synkronisere data på tværs af forekomster med Project Service Automation og Finance. De integrationsskabeloner, der er tilgængelige i forbindelse med funktionen til dataintegration, muliggør dataflow om kategorier for projekters udgiftstransaktioner mellem Finance og Project Service Automation.

Hvis projekters udgiftskategorier er håndteret i Finance, foretages integrationsflowet først fra Finance til Project Service Automation. Integrations-id'erne for projekters udgiftskategorierne opdateres derefter automatisk via synkronisering fra Project Service Automation til Finance.

Hvis projekters udgiftskategorier er håndteret i Project Service Automation, foretages integrationsflowet først fra Project Service Automation til Finance. Projektkategorierne skal allerede være konfigureret i Finance, før der synkroniseres fra Project Service Automation. Synkroniser derefter fra Finance tilbage til Project Service Automation, og derefter fra Project Service Automation til Finance igen. På denne måde kan du være med til at sikre, at kategorierne er sammenkædet, og at der ikke er oprettet dubletter.

> [!NOTE]
> Projekters udgiftskategorier håndteres som regel i Finance. Men hvis de ikke gør, eller hvis der allerede er oprettet udgiftskategorier i Project Service Automation, skal du først synkronisere ved hjælp af skabelonen for kategorierne for projekters udgiftstransaktioner (PSA til Fin og Ops). Synkroniser derefter ved hjælp af skabelonen for kategorier for projekters udgiftstransaktioner (Fin og Ops til PSA). Derefter skal du køre synkroniseringen fra Project Service Automation til Finance én gang mere.
>
> Hvis du først synkroniserer fra Project Service Automation, skal følgende krav være opfyldt i Finance, før synkroniseringen køres:
>
> - Den delte kategori, der stemmer overens med den projektkategori, der er konfigureret i Project Service Automation, skal findes, og den skal være aktiveret for både **Projekt** og **Udgift**.
> - For hver af de enkelte juridiske enheder i Finance, der skal integreres med, skal følgende projektkategorier findes:
>
>     - **Projektkategori** findes. 
>     - **Brug i udgift** er aktiveret.
>     - **Aktiv i kladde** er aktiveret.
>     - **Transaktionstype** er angivet til **Udgift**.

I følgende illustration vises, hvordan dataene synkroniseres mellem Project Service Automation og Finance.

[![Dataflow til integration af Project Service Automation med Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synkronisering af projekters udgiftskategorier mellem Finance og Project Service Automation

### <a name="template-and-task"></a>Skabelon og opgave

Hvis du vil have adgang til skabelonen, skal du i Microsoft Power Apps Administration vælge **Projekter** og derefter vælge **Nyt projekt** i øverste højre hjørne for at vælge offentligt tilgængelige skabeloner.

Følgende skabelon og underliggende opgave bruges til at synkronisere projekters udgiftskategorier fra Finance til Project Service Automation:

- **Navnet på skabelonen i dataintegration:** Kategorierne for projektets udgiftstransaktioner (Fin og Ops til PSA)
- **Navnet på opgaven i projektet:** Synkroniser kategorier til PSA

### <a name="entity-set"></a>Objektsæt

| Økonomi                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrationsobjekt for kategorier | Transaktionskategorier     |

### <a name="entity-flow"></a>Objektflow

Projektets udgiftskategorier administreres i Finance, og de synkroniseres med Project Service Automation som transaktionskategorier.

### <a name="power-query"></a>Power Query

Når du synkroniserer med Project Service Automation, skal du bruge Microsoft Power-forespørgsel til Excel til at angive faktureringstypen for transaktionskategorien. Skabelonerne for kategorierne for projektets udgiftstransaktioner (Fin og Ops til PSA) indeholder en standardkolonne og tilknytning. Hvis du opretter din egen skabelon, skal du tilføje en betinget kolonne i Power Query. Følg disse trin.

1. Klik på pilen for at åbne tilknytningen mellem opgaven for projektets udgiftskategorier i skabelonen for kategorierne for projektets udgiftstransaktioner (Fin og Ops til PSA).
2. Klik på linket **Avanceret forespørgsel og filtrering** for at åbne Power Query.
2. Vælg **Tilføj betinget kolonne**.
3. Angiv et navn til den nye kolonne, f.eks. **Faktureringstype**.
4. Angiv følgende betingelse: **Hvis KATEGORIID ikke er lig med null, så 19235001, ellers null**.
5. Klik på **OK** i kolonnen.
6. Sørg for at tilknytte denne nye kolonne på tilknytningssiden.

I følgende illustration vises et eksempel på tilknytningen mellem skabelonopgaver i dataintegration. I tilknytningen vises de feltoplysninger, der synkroniseres fra Finance til Project Service Automation.

[![Skabelontilknytning af projekters udgiftskategorier til Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synkronisering af projekters udgiftskategorier fra Project Service Automation til Finance

### <a name="template-and-task"></a>Skabelon og opgave

Følgende skabelon og underliggende opgave bruges til at synkronisere projekters udgiftskategorier fra Project Service Automation til Finance:

- **Navnet på skabelonen i dataintegration:** Kategorierne for projektets udgiftstransaktioner (PSA til Fin og Ops)
- **Navnet på opgaven i projektet:** Synkroniser kategorier til Fin Ops

### <a name="entity-set"></a>Objektsæt

| Project Service Automation | Økonomi                           |
|----------------------------|-----------------------------------|
| Transaktionskategorier     | Integrationsobjekt for kategorier |

### <a name="entity-flow"></a>Objektflow

Projektets udgiftskategorier administreres i Finance, og de synkroniseres med Project Service Automation som transaktionskategorier. Synkroniseringen tilbage til Finance opdaterer projektets kategori i Finance med integrations-id'et fra Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Skabelon for tilknytning i dataintegration

I følgende illustration vises et eksempel på tilknytningen mellem skabelonopgaver i dataintegration.

> [!NOTE]
> I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Skabelontilknytning for Project Service Automation til Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]