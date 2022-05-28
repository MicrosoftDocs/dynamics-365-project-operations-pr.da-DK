---
title: Synkroniser faktiske projektværdier direkte fra Project Service Automation med projektintegrationskladden til bogføring i Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere faktiske projektoplysninger direkte fra Microsoft Dynamics 365 Project Service Automation til Finance and Operations.
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
ms.openlocfilehash: 12929c324bb3a7c344edc9be2e3a8f4941ff9ea4
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683531"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synkroniser faktiske projektværdier direkte fra Project Service Automation med projektintegrationskladden til bogføring i Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere faktiske projektoplysninger direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

Skabelonen synkroniserer transaktioner fra Project Service Automation i en midlertidig tabel i Finance. Når synkroniseringen er fuldført, **skal** du importere dataene fra den midlertidige lagringstabel til integrationskladden.

> [!NOTE]
> - Integration af projektets faktiske oplysninger er tilgængelig fra version 8.0.1.
> - Hvis du bruger Enterprise Edition 7.3.0, kan du, efter at du har installeret KB 4132657 og KB 4132660, bruge skabelonerne til at integrere projektopgaver, kategorier for udgiftstransaktioner, timeestimater, udgiftsestimater og faktiske oplysninger samt konfigurere funktionslåsning. Hvis du vil nulstille regnskabsfordelingerne, anbefales det, at du også installerer KB 4131710.
> - Hvis du bruger version 7.3.0, og du sender gebyrtransaktioner over fra Project Service Automation, skal du installere KB 4345320 for at inkludere disse gebyrer i projektfakturaen.
> - Hvis der angives momsbeløb for tids- eller udgiftstransaktioner i Project Service Automation, skal du installere den 7. opdatering til Project Service Automation. Ellers knyttes de faktiske momsværdier ikke sammen med de tilknyttede faktiske oplysninger for tids eller udgifter, og de synkroniseres ikke med Finance. Hvis du ønsker flere oplysninger, skal du kontakte support.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflow for Project Service Automation til Finance

Integrationsløsningen for Project Service Automation til Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster med Project Service Automation og Finance. De integrationsskabeloner, der er tilgængelige i forbindelse med funktionen til dataintegration, muliggør dataflow om projekters faktiske oplysninger fra Project Service Automation til Finance.

I følgende illustration vises, hvordan dataene synkroniseres mellem Project Service Automation og Finance.

[![Dataflow for Project Service Automation-integration med Finance and Operations.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projektets faktiske oplysninger fra Project Service Automation

### <a name="template-and-tasks"></a>Skabelon og opgaver

Hvis du vil have adgang til den tilgængelige skabelon, skal du i Microsoft Power Apps Administration vælge **Projekter** og derefter vælge **Nyt projekt** i øverste højre hjørne for at vælge offentligt tilgængelige skabeloner.

Følgende skabelon og underliggende opgaver bruges til at synkronisere projekters faktiske oplysninger fra Project Service Automation til Finance:

- **Navn på skabelonen i dataintegration:** Projektets faktiske oplysninger (PSA til Fin og Ops)
- **Navnet på opgaverne i projektet:**

    - Faktiske værdier
    - TransactionConnections

### <a name="entity-set"></a>Objektsæt

| Project Service Automation | Økonomi                                   |
|----------------------------|----------------------------------------------------------|
| Faktiske værdier                    | Objekt til integration af projekters faktiske oplysninger                   |
| Transaktionsforbindelser    | Integrationsobjekt for projekttransaktionsrelationer |

### <a name="entity-flow"></a>Objektflow

Projektets faktiske oplysninger administreres i Project Service Automation, og de synkroniseres med kladden til projektintegration i Finance. Regnskabet anvendes på basis af økonomiske standarddimensioner og konteringsopsætningen.

### <a name="prerequisites"></a>Forudsætninger

Inden synkronisering af de faktiske oplysninger kan ske, skal du konfigurere integrationsparametrene for Project Service Automation og synkroniser projekter, projektopgaver og kategorierne for projekters udgiftstransaktioner.

### <a name="power-query"></a>Power Query

I skabelonen for faktiske projektværdier skal du bruge Microsoft Power Query til Excel til at udføre disse opgaver:

- Transformer transaktionsarten i Project Service Automation til den rigtige transaktionstype i Finance. Denne transformering er allerede defineret i skabelonen for projektets faktiske oplysninger (PSA til Fin og Ops).
- Transformer faktureringstypen i Project Service Automation til den rigtige faktureringstype i Finance. Denne transformering er allerede defineret i skabelonen for projektets faktiske oplysninger (PSA til Fin og Ops). Faktureringstypen knyttes derefter til linjeegenskaben baseret på konfigurationen på siden **Integrationsparametre for Project Service Automation**.
- Filtrer på bestemte ressourceorganisationsenheder, der skal synkroniseres med denne skabelon.
- Hvis den faktiske interne tid eller de faktiske interne udgifter synkroniseres med Finance, skal du transformere kontraktorganisationsenheden til den korrekte juridiske enhed i Finance. I skabelonen for projektets faktiske oplysninger (PSA til Fin og Ops) defineres der en betinget kolonne ud fra demonstrationsdata. Du skal opdatere den senest indsatte betingelseskolonne til de korrekte juridiske enheder. I modsat fald kan der enten opstå en integrationsfejl, eller de forkerte faktiske transaktioner kan blive importeret til Finance.
- Hvis den faktiske interne tid eller de faktiske interne udgifter ikke synkroniseres til Finance, skal du slette den senest indsatte betingede kolonne i skabelonen. I modsat fald kan der enten opstå en integrationsfejl, eller de forkerte faktiske transaktioner kan blive importeret til Finance.

#### <a name="contract-organizational-unit"></a>Kontraktorganisationsenhed
Hvis du vil opdatere den indsatte betingede kolonne i skabelonen, skal du klikke på pilen **Tilknyt** for at åbne tilknytningen. Vælg linket **Avanceret forespørgsel og filtrering** for at åbne Power Query.

- Hvis du bruger standardskabelonen Faktiske projektværdier (PSA til Fin and Ops) i Power Query, skal du vælge den sidste **Indsatte betingelse** i sektionen **Anvendte trin**. I feltet **Funktion** skal du erstatte **USSI** med navnet på den juridiske enhed, der skal bruges sammen med integrationen. Tilføj efter behov yderligere betingelser til feltet **Funktion**, og opdater betingelse **eller** fra **USMF** til den korrekte juridiske enhed.
- Hvis du opretter en ny skabelon, skal du tilføje kolonnen for at understøtte internt tid og udgifter. Vælg **Tilføj betinget kolonne**, og angiv et navn for kolonnen, som f.eks **LegalEntity**. Angiv en betingelse for kolonnen "hvor" hvis **msdyn\_contractorganizationalunitid.msdyn\_navn** er \<organizational unit\> og \<enter the legal entity\>; ellers null.

### <a name="template-mapping-in-data-integration"></a>Skabelon for tilknytning i dataintegration

I følgende illustrationer vises et eksempel på tilknytningen mellem skabelonopgaver i dataintegration. I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Skabelontilknytning – faktiske oplysninger.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Skabelontilknytning - transaktionsforbindelser.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importér fra midlertidig lagringstabel efter integrationen fra Project Service Automation

En periodisk proces for import fra midlertidig lagringstabel skal køres efter synkronisering af faktiske oplysninger fra Project Service Automation til Finance. Denne proces importerer projekttransaktioner fra den midlertidige lagringstabel til integrationskladden for Project Service Automation, hvor regnskabet anvendes, og de importerede transaktioner kan bogføres. Det anbefales, at du kører denne proces i batchtilstand. Den kan også konfigureres til at køre som en tilbagevendende batch.

## <a name="update-actuals-from-finance"></a>Opdater faktiske oplysninger fra Finance

### <a name="template-and-tasks"></a>Skabelon og opgaver

Følgende skabelon og underliggende opgaver bruges til at synkronisere bilagsnummeret og momsen for bogførte projekttransaktioner fra Finance til Project Service Automation:

- **Navn på skabelonen i dataintegration:** Opdatering af projektets faktiske oplysninger (Fin Ops til PSA)
- **Navnet på opgaverne i projektet:**

    - Faktiske værdier 
    - TransactionConnections

### <a name="entity-set"></a>Objektsæt

| Økonomi                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Objekt til integration af projekters faktiske oplysninger                   | Faktiske værdier                    |
| Integrationsobjekt for projekttransaktionsrelationer | Transaktionsforbindelser    |

### <a name="entity-flow"></a>Objektflow

Projektets faktiske oplysninger administreres i Project Service Automation, og de synkroniseres med kladden til projektintegration i Finance. Når de faktiske oplysninger er bogført i Finance, opdateres de i Project Service Automation med bilagsnummeret fra Finance. Hvis der er tilføjet moms i Finance, oprettes der nye faktiske momsoplysninger i Project Service Automation.

### <a name="power-query"></a>Power Query

I den opdaterede skabelon for faktiske projektværdier skal du bruge Power Query til at udføre disse opgaver:

- Transformer transaktionsarten i Finance til den rigtige transaktionstype i Project Service Automation. Denne transformering er allerede defineret i skabelonen for opdatering af projektets faktiske oplysninger (Fin Ops til PSA).
- Transformer faktureringstypen i Finance til den rigtige faktureringstype i Project Service Automation. Denne transformering er allerede defineret i skabelonen for opdatering af projektets faktiske oplysninger (Fin Ops til PSA).

### <a name="template-mapping-in-data-integration"></a>Skabelon for tilknytning i dataintegration

I følgende illustrationer vises eksempler på tilknytninger mellem skabelonopgaver i dataintegration. I tilknytningen vises de feltoplysninger, der synkroniseres fra Finance til Project Service Automation.

[![Skabelontilknytning – opdatering af faktiske oplysninger.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Skabelontilknytning – opdatering af transaktion.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]