---
title: Projektestimater og integration af faktiske tal
description: Dette emne indeholder oplysninger om integration med dobbeltskrivning i Project Operations for projektestimerede og faktiske værdier.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006284"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektestimater og integration af faktiske tal

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne indeholder oplysninger om integration med dobbeltskrivning i Project Operations for projektestimerede og faktiske værdier.

## <a name="project-estimates"></a>Projektestimater

Projektarbejde, udgifter og materialeestimater oprettes og vedligeholdes i Microsoft Dataverse og synkroniseres med Finance and Operations-apps til regnskabsformål. Handlinger til oprettelse, opdatering og sletning understøttes ikke via Finance and Operations-applikationerne.

Oprettelse af estimater kræver en gyldig regnskabskonfiguration for projektet. Projekter, der er knyttet til kontraktlinjer, skal have en gyldig projektomkostnings- og indtægtsprofil defineret i reglerne for projektomkostninger og omsætningsprofil. Du kan finde flere oplysninger under [Konfiguration af regnskab for fakturerbare projekter](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Arbejdsestimater

Arbejdsestimats oprettes af projektlederen eller Resource Manager, som også tildeler en generisk eller navngivet ressource til projektopgaven. Ressourcetildelingsposter kan gennemses under fanen **Ressourcetildelinger** på siden **Projektdetaljer** i Dataverse. Ressourcetildelingsposter i Dataverse opretter timeprognoseposter i Finance and Operations-apps ved hjælp af **Integrationsobjektet for timeestimater i Project Operations (msdyn\_resourceassignments)**.

   ![Integration af arbejdsestimater.](./Media/DW4LaborEstimates.png)

Med dobbeltskrivning synkroniseres ressourcetildelingsposter med den midlertidige tabel (**ProjCDSEstisymmetriHoursImport**), og derefter bruges forretningslogik til at oprette og opdatere timeprognoseposter (**ProjForecastEmpl**).

Projektrevisoren gennemgår prognosetimeposter, der er oprettet i Finance and Operations-apps, at gå til **Projektstyring og regnskab** > **Alle projekter** > **Planlæg** > **Timeprognoser**.

## <a name="expense-estimates"></a>Udgiftsestimater

Udgiftsestimater oprettes af projektlederen under fanen **Udgiftsestimater** på siden **Projektdetaljer** i Dataverse. Udgiftsestimatposter gemmes i objektet **Estimatlinje** i Dataverse. Disse estimerede poster har transaktionsklasse, **Udgifter** og synkroniseres med udgiftsprognoseposter i Finance and Operations-apps ved hjælp af objektet **Integrationsobjekt til udgiftsestimater i Project Operations (msdyn\_estimatelines)**.

   ![Integration af udgiftsestimater.](./Media/DW4ExpenseEstimates.png)

Med dobbeltskrivning synkroniseres udgiftsestimatposter med den midlertidige tabel **ProjCDSEstimateExpenseImport**, og derefter bruges forretningslogik til at oprette og opdatere udgiftsprognoseposter (**ProjForecastCost**). Estimatlinjer lagrer salgsestimat- og omkostningsestimatposter hver for sig. Forretningslogikken i Finance and Operations-apps udfylder en enkelt udgiftsprognosepost ved hjælp af denne detalje i den midlertidige tabel.

Projektrevisoren kan gennemgå udgiftsprognoseposter i Finance and Operations-apps ved at gå til **Projektstyring og regnskab** > **Alle projekter** > **Planlæg** > **Udgiftsprognoser**.

## <a name="material-estimates"></a>Materialeestimater

Materialeestimater oprettes af projektlederen under fanen **Materialeestimater** på siden **Projektdetaljer** i Dataverse. Materialeestimatposter gemmes i objektet **Estimatlinje** i Dataverse. Disse estimerede poster har transaktionsklassen **Materiale** og synkroniseres med vareprognoseposter i Finance and Operations-apps ved hjælp af objektet **Projektintegrationstabel for materialeestimater (msdyn\_estimatelines)**.

   ![Integration af materialeestimater.](./Media/DW4MaterialEstimates.png)

Med dobbeltskrivning synkroniseres materialeestimatposter med den midlertidige tabel **ProjForecastSalesImpor**, og derefter bruges forretningslogik til at oprette og opdatere vareprognoseposter (**ForecastSales**). Estimatlinjer lagrer salgsestimat- og omkostningsestimatposter hver for sig. Forretningslogikken i Finance and Operations-apps udfylder en enkelt vareprognosepost ved hjælp af denne detalje i den midlertidige tabel.

Projektrevisoren kan gennemgå vareprognoseposter i Finance and Operations-apps ved at gå til **Projektstyring og regnskab** > **Alle projekter** > **Planlæg** > **Vareprognoser**.

## <a name="project-actuals"></a>Projektets faktiske værdier

De faktiske projektværdier oprettes i Dataverse på baggrund af tid, udgifter, materialer og faktureringsaktiviteter. Alle driftsattributter for disse transaktioner, herunder mængde, kostpris, salgspris og projekt, registreres i dette Dataverse-objekt. Du kan finde yderligere oplysninger under [Faktiske værdier](../actuals/actuals-overview.md). Faktiske poster synkroniseres med Finance and Operations-apps ved hjælp af dobbeltskrivning-tabeltilknytningen **Integration af faktiske værdier i Project Operations (msdyn\_actuals)** til downstream-regnskab.

   ![Integration af faktiske værdier.](./Media/DW4Actuals.png)

Tabeltilknytningen **Integration af faktiske værdier i Project Operations** synkroniserer alle posterne fra objektet **Faktiske værdier** i Dataverse med attributten **Spring synkronisering over (kun intern brug)** angivet til **Falsk**. Attributværdien angives automatisk i Dataverse, når posten oprettes. Eksempler på, hvor attributten er angivet til **Sand**, er:

  - Faktiske projektomkostninger for interne transaktioner. Du kan finde flere oplysninger under [Opret interne transaktioner](../project-accounting/create-intercompany-transactions.md). Disse poster springes over, fordi systemet genskaber de faktiske projektomkostninger i Finance and Operations-apps, når den interne leverandørfaktura bogføres.
  - Negative ikke-fakturerede salgsposter, der blev oprettet, da proformafakturaen blev bekræftet. Disse poster springes over, fordi projektets underkonto i Finance and Operations-apps ikke tilbagefører den ikke-fakturerede salgspost ved fakturering, men ændrer statussen til fuldt faktureret.

Du kan bruge dobbeltskrivning-tabeltilknytningen til at synkronisere de faktiske poster med den midlertidige tabel **ProjCDSActualsImport**. Disse poster behandles af den periodiske proces **Importér fra midlertidig tabel**, når du opretter integrationslinjer i Project og forslagslinjer for projektfakturaer i Project Operations. Du kan finde flere oplysninger under [Integrationskladde i Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse registrerer også linkene mellem de faktiske projekttransaktioner i objektet **Transaktionsforbindelse**. Du kan finde flere oplysninger i [Knyt faktiske poster til oprindelige poster](../actuals/linkingactuals.md). Links mellem faktiske transaktioner synkroniseres også med Finance and Operations-apps ved hjælp af dobbeltskrivning-tabeltilknytningen **Integrationsobjektet for projekttransaktioners forhold (msdyn\_transactionconnections)**. Disse poster anvendes af den periodiske proces **Importér fra midlertidig tabel**, når du opretter integrationslinjer i Project og forslagslinjer for projektfakturaer i Project Operations.

Hvis du sender en integrationskladde i Project Operations og et forslag til en projektfaktura, udløses der en opdatering i de respektive poster i den midlertidige tabel **ProjCDSActualsImport**. Systemet henter og registrerer følgende regnskabsattributter for faktiske transaktioner:

- Regnskabsvalutabeløb
- Valutakurs
- Bilagsnummer
- Momsbeløb

Tabellen **Integration af faktiske værdier i Project Operations** knyttes de respektive faktiske poster i Dataverse sammen med disse oplysninger.
