---
title: Projektestimater og integration af faktiske tal
description: Denne artikel indeholder oplysninger om integration af dobbeltskrivning i Project Operations til projektestimater og faktiske værdier.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914579"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektestimater og integration af faktiske tal

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel indeholder oplysninger om integration af dobbeltskrivning i Project Operations til projektestimater og faktiske værdier.

## <a name="project-estimates"></a>Projektestimater

Projektarbejde, udgifter og materialeestimat oprettes og vedligeholdes i Microsoft Dataverse og synkroniseres med programmer til finans og drift med henblik på regnskabsformål. Handlinger for oprettelse, opdatering og sletning understøttes ikke via programmerne til finans og drift.

Oprettelse af estimater kræver en gyldig regnskabskonfiguration for projektet. Projekter, der er knyttet til kontraktlinjer, skal have en gyldig projektomkostnings- og indtægtsprofil defineret i reglerne for projektomkostninger og omsætningsprofil. Du kan finde flere oplysninger under [Konfiguration af regnskab for fakturerbare projekter](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Arbejdsestimater

Arbejdsestimats oprettes af projektlederen eller Resource Manager, som også tildeler en generisk eller navngivet ressource til projektopgaven. Ressourcetildelingsposter kan gennemses under fanen **Ressourcetildelinger** på siden **Projektdetaljer** i Dataverse. Ressourcetildelingsposter i Dataverse opretter af timeprognoseposter i programmer til finans og drift ved hjælp af **Objektet til integration af timeestimater i Project Operations (msdyn\_resourceassignments)**.

   ![Integration af arbejdsestimater.](./Media/DW4LaborEstimates.png)

Med dobbeltskrivning synkroniseres ressourcetildelingsposter med den midlertidige tabel (**ProjCDSEstisymmetriHoursImport**), og derefter bruges forretningslogik til at oprette og opdatere timeprognoseposter (**ProjForecastEmpl**).

Projektlederen gennemgår prognosetimeposter, der er oprettet i programmer til finans og drift, ved at gå til **Projektstyring og Regnskab** > **Alle projekter** > **Plan** > **Timeprognose**.

## <a name="expense-estimates"></a>Udgiftsestimater

Udgiftsestimater oprettes af projektlederen under fanen **Udgiftsestimater** på siden **Projektdetaljer** i Dataverse. Udgiftsestimatposter gemmes i objektet **Estimatlinje** i Dataverse. Disse estimerede poster har transaktionsklasse, **Udgifter** og synkroniseres med udgiftsprognoseposter i programmer til finans og drift ved hjælp af **Objektet til integration af udgiftsestimater i Project Operations (msdyn\_estimatelines)**.

   ![Integration af udgiftsestimater.](./Media/DW4ExpenseEstimates.png)

Med dobbeltskrivning synkroniseres udgiftsestimatposter med den midlertidige tabel **ProjCDSEstimateExpenseImport**, og derefter bruges forretningslogik til at oprette og opdatere udgiftsprognoseposter (**ProjForecastCost**). Estimatlinjer lagrer salgsestimat- og omkostningsestimatposter hver for sig. Forretningslogikken i programmer til finans og drift udfylder en enkelt udgiftsprognosepost ved hjælp af denne detalje i den midlertidige tabel.

Projektlederen kan gennemgå udgiftsprognoseoster i programmer til finans og drift ved at gå til **Projektstyring og Regnskab** > **Alle projekter** > **Plan** > **Udgiftsprognose**.

## <a name="material-estimates"></a>Materialeestimater

Materialeestimater oprettes af projektlederen under fanen **Materialeestimater** på siden **Projektdetaljer** i Dataverse. Materialeestimatposter gemmes i objektet **Estimatlinje** i Dataverse. Disse estimerede poster har transaktionsklassen **Materiale** og synkroniseres med vareprognoseposter i programmer til finans og drift ved hjælp af **Tabel til integration af materialeestimater i Project Operations (msdyn\_estimatelines)**.

   ![Integration af materialeestimater.](./Media/DW4MaterialEstimates.png)

Med dobbeltskrivning synkroniseres materialeestimatposter med den midlertidige tabel **ProjForecastSalesImpor**, og derefter bruges forretningslogik til at oprette og opdatere vareprognoseposter (**ForecastSales**). Estimatlinjer lagrer salgsestimat- og omkostningsestimatposter hver for sig. Forretningslogikken i programmer til finans og drift udfylder en enkelt vareprognosepost ved hjælp af denne detalje i den midlertidige tabel.

Projektlederen kan gennemgå vareprognoseoster i programmer til finans og drift ved at gå til **Projektstyring og Regnskab** > **Alle projekter** > **Plan** > **Vareprognose**.

## <a name="project-actuals"></a>Projektets faktiske værdier

De faktiske projektværdier oprettes i Dataverse på baggrund af tid, udgifter, materialer og faktureringsaktiviteter. Alle driftsattributter for disse transaktioner, herunder mængde, kostpris, salgspris og projekt, registreres i dette Dataverse-objekt. Du kan finde yderligere oplysninger under [Faktiske værdier](../actuals/actuals-overview.md). Faktiske poster synkroniseres med programmer til finans og drift ved hjælp af tabeltilknytning med dobbelt skrivning **Integration af faktiske værdier i Project Operations (msdyn\_actuals)** til downstream-regnskab.

   ![Integration af faktiske værdier.](./Media/DW4Actuals.png)

Tabeltilknytningen **Integration af faktiske værdier i Project Operations** synkroniserer alle posterne fra objektet **Faktiske værdier** i Dataverse med attributten **Spring synkronisering over (kun intern brug)** angivet til **Falsk**. Attributværdien angives automatisk i Dataverse, når posten oprettes. Eksempler på, hvor attributten er angivet til **Sand**, er:

  - Faktiske projektomkostninger for interne transaktioner. Du kan finde flere oplysninger under [Opret interne transaktioner](../project-accounting/create-intercompany-transactions.md). Disse poster springes over, fordi systemet genopretter de faktiske projektomkostninger i programmer til finans og drift, når den interne leverandørfaktura bogføres.
  - Negative ikke-fakturerede salgsposter, der blev oprettet, da proformafakturaen blev bekræftet. Disse poster springes over, fordi projektopslaget i programmer til finans og drift ikke ændrer den ikke-fakturerede salgspost ved fakturering, men ændrer status til fuldt faktureret.

Du kan bruge dobbeltskrivning-tabeltilknytningen til at synkronisere de faktiske poster med den midlertidige tabel **ProjCDSActualsImport**. Disse poster behandles af den periodiske proces **Importér fra midlertidig tabel**, når du opretter integrationslinjer i Project og forslagslinjer for projektfakturaer i Project Operations. Du kan finde flere oplysninger under [Integrationskladde i Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse registrerer også linkene mellem de faktiske projekttransaktioner i objektet **Transaktionsforbindelse**. Du kan finde flere oplysninger i [Knyt faktiske poster til oprindelige poster](../actuals/linkingactuals.md). Links mellem faktiske transaktioner synkroniseres også med programmer til finans og drift ved hjælp af den dobbelte tabeltilknytning **Objekt til integration af projekttransaktionsrelationer (msdyn\_transactionconnections)**. Disse poster anvendes af den periodiske proces **Importér fra midlertidig tabel**, når du opretter integrationslinjer i Project og forslagslinjer for projektfakturaer i Project Operations.

Hvis du sender en integrationskladde i Project Operations og et forslag til en projektfaktura, udløses der en opdatering i de respektive poster i den midlertidige tabel **ProjCDSActualsImport**. Systemet henter og registrerer følgende regnskabsattributter for faktiske transaktioner:

- Regnskabsvalutabeløb
- Valutakurs
- Bilagsnummer
- Momsbeløb

Tabellen **Integration af faktiske værdier i Project Operations** knyttes de respektive faktiske poster i Dataverse sammen med disse oplysninger.
