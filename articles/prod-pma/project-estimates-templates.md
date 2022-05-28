---
title: Synkroniser projektestimater direkte fra Project Service Automation til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 47de3556034227e072d14dc93908edec42cec93c
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684589"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synkroniser projektestimater direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE]
> - Integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.
> - Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflow for Project Service Automation til Finance

Integrationsløsningen for Project Service Automation til Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster med Project Service Automation og Finance. De integrationsskabeloner, der er tilgængelige i forbindelse med funktionen til dataintegration, muliggør dataflow om timeestimater og estimater for projektudgifter fra Project Service Automation til Finance.

I følgende illustration vises, hvordan dataene synkroniseres mellem Project Service Automation og Finance.

[![Dataflow til integration af Project Service Automation med Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projektets timeestimater

### <a name="template-and-tasks"></a>Skabelon og opgaver

Hvis du vil have adgang til den tilgængelige skabelon, skal du i Microsoft Power Apps Administration vælge **Projekter** og derefter vælge **Nyt projekt** i øverste højre hjørne for at vælge offentligt tilgængelige skabeloner.

Følgende skabelon og underliggende opgaver bruges til at synkronisere projekters timeestimater fra Project Service Automation til Finance:

- **Navnet på skabelonen i dataintegration:** Projektets timeestimater (PSA til Fin og Ops)
- **Navnet på opgaverne i projektet:**

    - Transaktionsrelationer
    - Udgiftsestimater

### <a name="entity-set"></a>Objektsæt

| Project Service Automation | Økonomi                                       |
|----------------------------|-----------------------------------------------|
| Projektopgaver              | Integrationsobjekt for projektets timeestimater |

### <a name="entity-flow"></a>Objektflow

Projektets timeestimater administreres i Project Service Automation, og de synkroniseres med Finance som prognose for projektets timer.

### <a name="prerequisites"></a>Forudsætninger

Før der kan ske synkronisering af projektets timeestimater, skal du synkronisere projekter, projektopgaver og projektets udgiftstransaktionskategorier.

### <a name="power-query"></a>Power Query

I skabelonen for projekttimeestimater skal du bruge Microsoft Power Query til Excel til at udføre disse opgaver:

- Angiv id'et for standardprognosemodellen, der skal bruges, når integrationen opretter nye timeprognoser.
- Filtrerer alle ressourcespecifikke poster i opgaven, der ikke kan integreres i timeprognoserne.
- Filtrerer eventuelle tomme rækker i transaktionskategorier. Hvis du ikke gør dette, kan det resultere i forkerte timeprognoser.

#### <a name="set-the-default-forecast-model-id"></a>Angiv id'et for standardprognosemodellen

Hvis du vil opdatere id'et for standardprognosemodellen i skabelonen, skal du klikke på pilen **Tilknyt** for at åbne tilknytningen. Vælg derefter linket **Avanceret forespørgsel og filtrering**.

- Hvis du bruger standardtimeestimaterne for projektet (PSA til Fin og Ops), skal du i Power Query markere den sidst **Indsatte betingelse** i listen **Anvendte trin**. I feltet **Funktion** skal du erstatte **O\_prognose** med navnet din prognosemodels id, som skal bruges sammen med integrationen. Standardskabelonen har et prognosemodel-id fra demonstrationsdataene.
- Hvis du opretter en ny skabelon, skal du tilføje denne kolonne. I Power Query skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**. Angiv betingelsen for kolonnen "hvor" hvis projektopgave ikke er null, og derefter \<enter the forecast model ID\>; ellers null.

#### <a name="filter-out-resource-specific-records"></a>Filtrering af ressourcespecifikke poster

Skabelonen for projektets timeestimater (PSA til Fin og Ops) har et standardfilter, der fjerner alle ressourcespecifikke poster. Hvis du opretter din egen skabelon, skal du tilføje dette filter. Vælg linket **Avanceret forespørgsel og filtrering**, der skal filtreres i kolonnen **msdyn\_erlinjeopgave**, så det kun er poster med **Falsk**, der inkluderes.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrerer tomme rækker fra i transaktionskategorier

Du skal tilføje et filter for at fjerne alle rækker, der har tomme transaktionskategorier. Denne opgave er obligatorisk, uanset om du bruger standardskabelonen eller opretter din egen skabelon. Dette filter fjerner eventuelle oversigtsrækker fra Project Service Automation, hvilket kan medføre, at timeprognoserne i Finance er forkerte. Vælg linket **Avanceret forespørgsel og filtrering** for at filtrere null-poster fra i kolonnen **msdyn\_transaktionskategori\_værdi**.

### <a name="template-mapping-in-data-integration"></a>Skabelon for tilknytning i dataintegration

I følgende illustration vises et eksempel på tilknytningen mellem skabelonopgaver i dataintegration. I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Skabelon for tilknytning af opgave i dataintegration.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projektets udgiftsestimater

### <a name="template-and-tasks"></a>Skabelon og opgaver

Følgende skabelon og underliggende opgaver bruges til at synkronisere projekters udgiftsestimater fra Project Service Automation til Finance:

- **Navnet på skabelonen i dataintegration:** Projektets udgiftsestimater (PSA til Fin og Ops)
- **Navnet på opgaverne i projektet:**

    - Transaktionsrelationer 
    - Udgiftsestimater

### <a name="entity-set"></a>Objektsæt

| Project Service Automation | Økonomi                                                  |
|----------------------------|----------------------------------------------------------|
| Transaktionsforbindelser    | Integrationsobjekt for projekttransaktionsrelationer |
| Estimatlinjer             | Integrationsobjekt for projektets udgiftsestimater         |

### <a name="entity-flow"></a>Objektflow

Projektets udgiftsestimater administreres i Project Service Automation, og de synkroniseres med Finance som prognose for projektets udgifter.

### <a name="prerequisites"></a>Forudsætninger

Før der kan ske synkronisering af projektets udgiftsestimater, skal du synkronisere projekter, projektopgaver og projektets udgiftstransaktionskategorier.

### <a name="power-query"></a>Power Query

I skabelonen til projektudgiftsestimater skal du skal bruge Power Query til at udføre følgende opgaver:

- Filter, så det kun omfatter linjeposter for udgiftsestimater.
- Angiv id'et for standardprognosemodellen, der skal bruges, når integrationen opretter nye timeprognoser.
- Transformer faktureringstyperne.
- Transformer transaktionstyperne.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filter, så det kun omfatter linjer for udgiftsestimater

Skabelonen for projektets udgiftsestimater (PSA til Fin og Ops) har et standardfilter, der kun indeholder udgiftslinjer i integrationen. Hvis du opretter din egen skabelon, skal du tilføje dette filter. Vælg opgaven **Transaktionsrelationer**, og klik derefter på pilen **Tilknyt** for at åbne tilknytningen. Vælg linket **Avanceret forespørgsel og filtrering**. Filtrer kolonnen **msdyn\_transaktionstype1**, så den kun inkluderer **msdyn\_estimalinje**.

#### <a name="set-the-default-forecast-model-id"></a>Angiv id'et for standardprognosemodellen

Hvis du vil opdatere id'et for standardprognosemodellen i skabelonen, skal du vælge opgaven **Udgiftsestimater** og derefter klikke på pilen **Tilknyt** for at åbne tilknytningen. Vælg linket **Avanceret forespørgsel og filtrering**.

- Hvis du bruger standardskabelonen for Estimerede projektværdier (PSA til Fin and Ops) i Power Query, skal du først vælge den sidste **Indsatte betingelse** i sektionen **Anvendte trin**. I feltet **Funktion** skal du erstatte **O\_prognose** med navnet din prognosemodels id, som skal bruges sammen med integrationen. Standardskabelonen har et prognosemodel-id fra demonstrationsdataene.
- Hvis du opretter en ny skabelon, skal du tilføje denne kolonne. I Power Query skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**. Angiv betingelsen for kolonnen "hvor" hvis estimatlinje-id ikke er null, og derefter \<enter the forecast model ID\>; ellers null.

#### <a name="transform-the-billing-types"></a>Transformer faktureringstyperne

Skabelonen for projektets udgiftsestimater (PSA til Fin og Ops) indeholder en betinget kolonne, der bruges til at transformere de faktureringstyper, der modtages fra Project Service Automation under integrationen. Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne. Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**. Angiv et navn til den nye kolonne, f.eks. **Faktureringstype**. Angiv derefter følgende betingelse:

Hvis **msdyn\_faktureringstype** = 192350000, er den ikke **Fakturerbar**  
Hvis **msdyn\_faktureringstype** = 192350001, er den **Fakturerbar**  
Hvis **msdyn\_faktureringstype** = 192350002, er den **Komplementerende**  
ellers **Ikketilgængelige**

#### <a name="transform-the-transaction-types"></a>Transformer transaktionstyperne

Skabelonen for projektets udgiftsestimater (PSA til Fin og Ops) indeholder en betinget kolonne, der bruges til at transformere de transaktionstyper, der modtages fra Project Service Automation under integrationen. Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne. Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**. Angiv et navn til den nye kolonne, f.eks. **Transaktionstype**. Angiv derefter følgende betingelse:

Hvis **msdyn\_transaktionstypekode** = 192350000, er det **Omkostninger**  
Hvis **msdyn\_transaktionstypekode** = 192350005, så er det **Salg**  
Ellers er det **null**

### <a name="template-mapping-in-data-integration"></a>Skabelon for tilknytning i dataintegration

I følgende illustrationer vises eksempler på tilknytninger mellem skabelonopgaver i dataintegration. I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Tilknytning af skabelon for udgiftsestimattransaktioner.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Tilknytning af skabelon af udgiftsestimater.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]