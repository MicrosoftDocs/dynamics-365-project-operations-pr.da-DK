---
title: Opsætning af Project Operations og konfiguration af dataintegration
description: Denne artikel indeholder oplysninger om, hvordan du opsætter og konfigurerer tilknytninger med dobbeltskrivning i Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914533"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Opsætning af Project Operations og konfiguration af dataintegration

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel indeholder oplysninger om integration af dobbeltskrivning i Project Operations til opsætnings- og konfigurationsenheder.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektkontrakter, kontraktlinjer og projekter

Projektkontrakter, kontraktlinjer og projekter oprettes i Dataverse og synkroniseres med programmer til finans og drift med henblik på ekstra regnskab. Posterne i disse objekter kan kun oprettes og slettes i Dataverse. Der kan dog tilføjes regnskabsattributter, f.eks. momsgruppestandarder og økonomiske dimensioner, til disse poster i programmer til finans og drift.

  ![Begreber i projektkontraktintegration.](./media/1ProjectContract.jpg)

Salgsaktivitetsemner, salgsmuligheder og tilbud spores i Dataverse og synkroniseres ikke med programmer til finans og drift, da der ikke er knyttet noget downstream-regnskab til denne aktivitet.

Projektkontraktfunktionaliteten i Dataverse opretter en projektkontraktpost i programmerne til finans og drift ved hjælp af tabeltilknytningen **Overskrifter til projektkontrakter (salgsordrer)**. Når du gemmer en projektkontrakt, starter Dataverse også oprettelsen af en objektpost for projektkontraktkunden. Denne post synkroniseres med programmer til finans og drift ved hjælp af tabeltilknytningen **Projektfinansieringskilde (msdyn\_projectcontractsspbillingrules)**. Denne tilknytning synkroniserer også tilføjelser, opdateringer og sletninger i projektkontraktkunder. Du kan kun dele faktureringsprocenter mellem projektkontraktkunder i Dataverse, og de synkroniseres ikke med programmer til finans og drift.

Når en projektkontrakt er oprettet i Dataverse, kan projektrevisoren opdatere regnskabsattributterne for denne projektkontrakt i programmer til finans og drift ved at gå til **Projektstyring og regnskab** > **Projektkontrakter** > **Konfiguration** > **Vis standardregnskab**. Regnskabsafdelingen kan gennemse attributterne for driftsprojektkontrakter, f.eks. ønsket leveringsdato og kontraktbeløb, ved at vælge projektkontrakt-id'et i programmer til finans og drift, som åbner den relaterede projektkontraktpost i Dataverse.

Projektobjektet synkroniseres med programmer til finans og drift ved hjælp af tabeltilknytningen **Projects V2 (msdyn\_projects)**. Projektrevisoren kan:

  - Gennemse projekter i programmer til finans og drift ved at gå til **Projektstyring og regnskab** > **Alle projekter**. 
  - Opdater regnskabsattributter for projektet i programmer til finans og drift ved at gå til **Projektstyring og regnskab** > **Alle projekter** > **Konfiguration** > **Vis standardregnskab**.  
  - Gennemse attributter for driftsprojektet, f.eks. anslåede start- og slutdatoer, ved at vælge projekt-id'et i programmer til finans og drift, som åbner den relaterede projektpost i Dataverse.

Et projekt knyttes til en projektkontrakt via objektet **Projektkontraktlinje**.

Projektkontraktlinjer i Dataverse opretter en projektkontraktfaktureringsregel i programmer til finans og drift ved hjælp af tabeltilknytningen **Projektkontraktlinjer (salesorderdetails)**. Faktureringsmetoden definerer typen af projektkontraktfaktureringsregler i programmer til finans og drift:

  - Projektkontraktlinjer med en faktureringsmetode for tid og materialer opretter en faktureringsregel for tid og materialetype.
  - Kontraktlinjer for fast prisfaktureringsmetode opretter en faktureringsregel for milepæle.

Projektkontraktlinjer kan gennemses af projektrevisoren i programmer til finans og drift ved at gå til **Projektstyring og regnskab** > **Projektkontrakter** > **Konfiguration** > **Vis standardregnskab** og gennemgå detaljerne under fanen **Kontraktlinjer**. Regnskabskontoen kan også angive økonomiske standardmål for kontraktlinjerne for fastprisfaktureringsmetode under denne fane.

## <a name="billing-milestones"></a>Faktureringsmilepæle

Projektkontraktlinjer, som bruger faktureringsmetoden med fast pris, faktureres via faktureringsmilepæle. Faktureringsmilepæle synkroniseres med projekttransaktioner i programmer til finans og drift ved hjælp af tabeltilknytningen **Milepæle for integration af kontraktlinje i Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integration af faktureringsmilepæle.](./media/2Milestones.jpg)

Revisoren kan gennemse acontotransaktioner og justere regnskabsattributterne for disse transaktioner ved at gå til **Projektstyring og regnskab** > **Projektkontrakter** > **Vedligeholdelse** > **Acontotransaktioner** eller **Projektstyring og regnskab** > **Alle projekter** > **Vedligeholdelse** > **Acontotransaktioner**.

Når du lige opretter en faktureringsmilepæl for en bestemt projektkontraktlinje, opretter systemet automatisk et projekt med et fast prisomsætningsestimat for det projekt, der er knyttet til denne kontraktlinje. Projekter med fastprisomsætningsestimat kan gennemses ved at gå til **Projektstyring og regnskab** > **Projekter med fastprisomsætningsestimat**.

### <a name="project-tasks"></a>Projektopgaver

Projektopgaver synkroniseres alene med programmer til finans og drift via tabeltilknytningen **Projektopgaver (msdyn\_projecttasks)** af hensyn til referencer. Handlinger for oprettelse, opdatering og sletning understøttes ikke via programmer til finans og drift.

  ![Integration af projektopgaver.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektressourcer

Objektet **Projektressourceroller** synkroniseres alene med programmer til finans og drift ved hjælp af tilknytningen **Projektressourceroller for alle firmaer (bookableresourcecategories)** af hensyn til referencer. Da ressourcerollerne i Dataverse ikke er virksomhedsspecifikke, opretter systemet automatisk respektive virksomhedsspecifikke ressourcerolleposter i programmer til finans og drift for alle retlige enheder, der er omfattet af integration med dobbelt skrivning.

![Integration af ressourceroller.](./media/5Resources.jpg)

Projektressourcer i Project Operations vedligeholdes i Dataverse og synkroniseres ikke med programmer til finans og drift.

### <a name="transaction-categories"></a>Transaktionskategorier

Transaktionskategorier vedligeholdes i Dataverse og synkroniseres med programmer til finans og drift ved hjælp af tabeltilknytningen **Projekttransaktionskategorier (msdyn\_transactioncategories)**. Når transaktionskategoriposten er synkroniseret, oprette systemet automatisk fire delte kategoriposter. Hver post svarer til en transaktionstype i programmer til finans og drift og knytter dem til transaktionskategoriposten.

![Integration af transaktionskategorier.](./media/4TransactionCategories.jpg)

Brugen af transaktionskategorier til estimater og faktiske værdier kræver, at projektrevisoren eller systemadministratoren opretter tilsvarende projektkategorier i alle juridiske enheder. Du kan finde flere oplysninger under [Konfiguration af produktkategorier](../project-accounting/configure-project-categories.md).
