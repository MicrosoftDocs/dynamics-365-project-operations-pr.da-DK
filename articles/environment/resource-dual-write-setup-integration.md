---
title: Opsætning af Project Operations og konfiguration af dataintegration
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer dobbeltskrivning-tilknytninger i Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986529"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Opsætning af Project Operations og konfiguration af dataintegration

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne indeholder oplysninger om integration med dobbeltskrivning i Project Operations for opsætnings- og konfigurationsenheder.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektkontrakter, kontraktlinjer og projekter

Projektkontrakter, kontraktlinjer og projekter oprettes i Dataverse og synkroniseres med Finance and Operations-apps med henblik på yderligere regnskab. Posterne i disse objekter kan kun oprettes og slettes i Dataverse. Der kan dog føjes regnskabsattributter, som f.eks. momsgruppestandarder og økonomiske dimensioner, til disse poster i Finance and Operations-appsene.

  ![Begreber i projektkontraktintegration.](./media/1ProjectContract.jpg)

Salgsaktivitetsemner, salgsmuligheder og tilbud spores i Dataverse og synkroniseres ikke med Finance and Operations-apps, da der ikke er knyttet noget downstream-regnskab til denne aktivitet.

Projektkontraktfunktionaliteten i Dataverse opretter en projektkontraktpost i Finance and Operations-apps ved hjælp af tabeltilknytningen **Overskrifter til projektkontrakt (salgsordre)**. Når du gemmer en projektkontrakt, starter Dataverse også oprettelsen af en objektpost for projektkontraktkunden. Denne post synkroniseres med Finance and Operations-apps ved hjælp af tabeltilknytningen **Finansieringskilde til projekt (msdyn\_projectcontractsspbillingrules)**. Denne tilknytning synkroniserer også tilføjelser, opdateringer og sletninger i projektkontraktkunder. Procenter for opdelt fakturering mellem projektkontraktkunder kan kun foretages i Dataverse, og de synkroniseres ikke med Finance and Operations-apps.

Når en projektkontrakt er oprettet i Dataverse, kan projektrevisoren opdatere regnskabsattributterne for denne projektkontrakt i Finance and Operations-apps ved at gå til **Projektstyring og regnskab** > **Projektkontrakter** > **Opsætning** > **Vis standardregnskab**. Revisoren kan gennemse driftsattributterne for projektkontrakter, som f.eks. ønsket leveringsdato og kontraktbeløb, ved at vælge projektkontrakt-id'et i Finance and Operations-apps, hvilket åbner den relaterede projektkontraktpost i Dataverse.

Projektobjektet synkroniseres med Finance and Operations-apps ved hjælp af tabeltilknytningen **Projekter V2 (msdyn\_projekter)**. Projektrevisoren kan:

  - Gennemse projekter i Finance and Operations-apps ved at gå til **Projektstyring og regnskab** > **Alle projekter**. 
  - Opdatere regnskabsattributter for projektet i Finance and Operations-apps ved at gå til **Projektstyring og regnskab** > **Alle projekter** > **Opsætning** > **Vis standardregnskab**.  
  - Gennemse driftsattributter for projektet, som f.eks. estimeret start- og slutdatoer, ved at vælge projekt-id'et i Finance and Operations-apps, hvilket åbner den relaterede projektpost i Dataverse.

Et projekt knyttes til en projektkontrakt via objektet **Projektkontraktlinje**.

Projektkontraktlinjer i Dataverse opretter en faktureringsregel for projektkontrakten i Finance and Operations-apps ved hjælp af tabeltilknytningen **Projektkontraktlinjer (salgsordredetaljer)**. Faktureringsmetoden definerer faktureringsregeltypen for projektkontrakten i Finance and Operations-apps:

  - Projektkontraktlinjer med en faktureringsmetode for tid og materialer opretter en faktureringsregel for tid og materialetype.
  - Kontraktlinjer for fast prisfaktureringsmetode opretter en faktureringsregel for milepæle.

Projektkontraktlinjer kan gennemses af projektrevisionen i Finance and Operations-apps ved at gå til **Projektstyring og regnskab** > **Projektkontrakter** > **Opsætning** > **Vis standardregnskab** og gennemse detaljerne under fanen **Kontraktlinjer**. Revisoren kan også angive økonomiske standarddimensioner for kontraktlinjerne for fastprisfaktureringsmetoden under denne fane.

## <a name="billing-milestones"></a>Faktureringsmilepæle

Projektkontraktlinjer, som bruger faktureringsmetoden med fast pris, faktureres via faktureringsmilepæle. Faktureringsmilepæle synkroniseres med acontoprojekttransaktioner i Finance and Operations-apps ved hjælp af tabeltilknytningen **Integration af kontraktlinjemilepæle i Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integration af faktureringsmilepæle.](./media/2Milestones.jpg)

Revisoren kan gennemse acontotransaktioner og justere regnskabsattributterne for disse transaktioner ved at gå til **Projektstyring og regnskab** > **Projektkontrakter** > **Vedligeholdelse** > **Acontotransaktioner** eller **Projektstyring og regnskab** > **Alle projekter** > **Vedligeholdelse** > **Acontotransaktioner**.

Når du lige opretter en faktureringsmilepæl for en bestemt projektkontraktlinje, opretter systemet automatisk et projekt med et fast prisomsætningsestimat for det projekt, der er knyttet til denne kontraktlinje. Projekter med fastprisomsætningsestimat kan gennemses ved at gå til **Projektstyring og regnskab** > **Projekter med fastprisomsætningsestimat**.

### <a name="project-tasks"></a>Projektopgaver

Projektopgaver synkroniseres med Finance and Operations-apps via tabeltilknytningen **Projektopgaver (msdyn\_projecttasks)**, men alene til referenceformål. Handlinger til oprettelse, opdatering og sletning understøttes ikke via Finance and Operations-applikationerne.

  ![Integration af projektopgaver.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektressourcer

Objektet **Projektressourceroller** synkroniseres med Finance and Operations-apps ved hjælp af tabeltilknytningen **Projektressourceroller for alle firmaer (bookableresourcecategories)**, men kun til referenceformål. Da ressourceroller i Dataverse ikke er virksomhedsspecifikke, opretter systemet automatisk respektive virksomhedsspecifikke ressourcerolleposter i Finance and Operations-apps for alle juridiske enheder, der er omfattet af integration med dobbeltskrivning.

![Integration af ressourceroller.](./media/5Resources.jpg)

Projektressourcer i Project Operations vedligeholdes i Dataverse og synkroniseres ikke med Finance and Operations-apps.

### <a name="transaction-categories"></a>Transaktionskategorier

Transaktionskategorier vedligeholdes i Dataverse og synkroniseres med Finance and Operations-apps ved hjælp af tabeltilknytningen **Projekttransaktionskategorier (msdyn\_transactioncategories)**. Når transaktionskategoriposten er synkroniseret, oprette systemet automatisk fire delte kategoriposter. Hver post svarer til en transaktionstype i Finance and Operations-apps og knytter dem til transaktionskategoriposten.

![Integration af transaktionskategorier.](./media/4TransactionCategories.jpg)

Brugen af transaktionskategorier til estimater og faktiske værdier kræver, at projektrevisoren eller systemadministratoren opretter tilsvarende projektkategorier i alle juridiske enheder. Du kan finde flere oplysninger under [Konfiguration af produktkategorier](../project-accounting/configure-project-categories.md).
