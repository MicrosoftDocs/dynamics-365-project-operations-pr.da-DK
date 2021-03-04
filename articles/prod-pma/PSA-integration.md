---
title: Oversigt over Project Service Automation
description: Dette emne indeholder oplysninger om løsningen til integration af Dynamics 365 Project Service Automation i Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642446"
---
# <a name="project-service-automation-overview"></a>Oversigt over Project Service Automation

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Integrationsløsningen for Project Service Automation til Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster med Dynamics 365 Finance og Dynamics 365 Project Service Automation via Common Data Service. De integrationsskabeloner, der er tilgængelige sammen med dataintegrationsfunktionen, aktiverer flowet af projekter, projektkontrakter, projektkontraktlinjer, milepæle for projektkontraktlinjer, projektopgaver, udgiftstransaktionskategorier, tidsestimater samt udgiftsestimater fra Project Service Automation til Finance.

> [!NOTE]
> - Hvis du bruger version 7.3.0, skal du installere KB 4074835. Du kan derefter integrere fastprisprojekter.
> - Hvis du bruger version 7.3.0, og du sender gebyrtransaktioner over fra Project Service Automation, skal du installere KB 4345320 for at inkludere disse gebyrer i projektfakturaen.
> - Hvis du bruger versoin 8.0, vil du kunne anvende integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner.
> - Hvis du bruger version 8.0.1 eller nyere, kan du synkronisere de faktiske oplysninger.

Før du kan integrere Project Service Automation Finance, skal du konfigurere integrationsparametrene for Project Service Automation. Du kan finde flere oplysninger i [Integrationsparametrene for Project Service Automation](PSA-parameters.md).

Denne integrationsløsning aktiverer direkte synkronisering i følgende scenarier:

- Vedligehold projektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opret projekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Vedligehold projektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Vedligehold milepæle for projektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Vedligehold projektopgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Vedligehold udgiftstransaktionskategorier i Finance, og synkroniser dem direkte fra Finance til Project Service Automation.
- Opret timeestimater for projekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opret udgiftsestimater for projekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opret faktiske oplysninger for projekttid, udgifter og gebyrer i Project Service Automation, og opret projekttransaktioner i integrationskladden for Project Service Automation, så de kan bogføres i Finance.

## <a name="data-synchronization"></a>Datasynkronisering

I følgende illustration vises, hvordan data synkroniseres som led i integrationen mellem Project Service Automation og Finance.

> [!NOTE]
> Ikke alle skabeloner er tilgængelige i øjeblikket. Skabelonerne udgives, efterhånden som de er fuldført.

[![Integration af Project Service Automation med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systemkrav til Finance

Hvis du vil bruge integrationsløsningen Project Service Automation til Finance, skal du installere Enterprise Edition 7.3 med platformsopdatering 12 eller nyere.

## <a name="system-requirements-for-project-service-automation"></a>Systemkrav for Project Service Automation

Hvis du vil bruge integrationsløsningen Project Service Automation til Finance, skal du installere følgende komponenter:

- Dynamics 365 Project Service Automation version 9.0.0.0 eller en nyere version
- Kundeemne til kontantløsning til Dynamics 365 Sales, version 1.14.0.0 (v14) eller nyere
- Project Service Automation til Finance-løsningen til Dynamics 365 Project Service Automation version 1.0.0.0 eller nyere

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installer integrationsløsningen Project Service Automation til Finance i din forekomst af Project Service Automation

Hent integrationsløsningen Project Service Automation til Finance fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg instruktionerne, der leveres sammen med løsningen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]