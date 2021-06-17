---
title: Integration af udgiftsstyring
description: Dette emne indeholder oplysninger om integration af udgiftsrapporter i Project Operations ved hjælp af dobbeltskrivning.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7fff69f062bf09fe7ceca61d951b535d2e010bfd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999979"
---
# <a name="expense-management-integration"></a>Integration af udgiftsstyring

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne indeholder oplysninger om integration af udgiftsrapporter i Project Operations [fuld udgiftsudrulning](../expense/expense-overview.md) ved hjælp af dobbeltskrivning.

## <a name="expense-categories"></a>Udgiftskategorier

I en fuld udgiftsudrulning oprettes og vedligeholdes udgiftskategorier i Finance and Operations-apps. Hvis du vil oprette en ny udgiftskategori, skal du udføre følgende trin:

1. I Microsoft Dataverse skal du oprette en kategori kaldet **Transaktion**. Integration med dobbeltskrivning synkroniserer denne transaktionskategori med Finance and Operations-apps. Du kan finde flere oplysninger i [Konfigurer projektkategorier](/dynamics365/project-operations/project-accounting/configure-project-categories) og [Dataintegration for opsætning og konfiguration af Project Operations](resource-dual-write-setup-integration.md). Som følge af denne integration opretter systemet fire delte kategoriposter i Finance and Operations-apps.
2. I Finance skal du gå til **Udgiftsstyring** > **Opsætning** > **Delte kategorier** og vælge en delt kategori med en transaktionsklasse kaldet **Udgift**. Angiv parameteren **Kan bruges i udgifter** til **Sand**, og definer den udgiftstype, der skal bruges.
3. Brug denne delte kategoripost til at oprette en ny udgiftskategori ved at gå til **Udgiftsstyring** > **Opsætning** > **Udgiftskategorier** og vælge **Ny**. Når posten gemmes, bruger dobbeltskrivning-tabeltilknytningen **Eksportobjekt for integration af projektudgiftskategorier i Project Operations(msdyn\_expensecategories)** til at synkronisere denne post med Dataverse.

  ![Integration af udgiftskategorier](./media/DW6ExpenseCategories.png)

Udgiftskategorier i Finance and Operations-apps er virksomhedsspecifikke eller juridiske enhedsspecifikke. Der findes separate tilsvarende poster, der er specifikke for juridiske enheder, i Dataverse. Når en projektleder estimerer udgifter, kan vedkommende ikke vælge udgiftskategorier, der er oprettet for et projekt, som ejes af en anden virksomhed end den virksomhed, der ejer det projekt, vedkommende arbejder på. 

## <a name="expense-reports"></a>Udgiftsrapporter

Udgiftsrapporter oprettes og godkendes i Finance and Operations-apps. Du kan finde flere oplysninger i [Opret og behandl udgiftsrapporter i Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Når udgiftsrapporten er godkendt af projektlederen, bogføres den i hovedbogen. I Project Operations bogføres projektrelaterede udgiftsrapportlinjer ved hjælp af særlige bogføringsregler:

  - Projektrelaterede omkostninger (herunder moms, der ikke kan inddrives) bogføres ikke straks til projektomkostningskontoen i hovedbogen, men bogføres i stedet for på udgiftsintegrationskontoen. Denne konto er konfigureret på fanen **Projektstyring og regnskab** > **Opsætning** > **Projektstyrings- og regnskabsparametre**, **Project Operations på Dynamics 365 Customer Engagement**.
  - Dobbeltskrivning synkroniseres med Dataverse ved hjælp af tabeltilknytningen **Integrationsobjekt for eksport af projektudgifter i Project Operations (msdyn\_udgifter)**.
  - Momsunderkonto, underkonto for leverandør og anden økonomisk bogføring registreres som gældende på tidspunktet for bogføringen af udgiftsrapporten.

  ![Integration af udgiftsrapporter](./media/DW6ExpenseReports.png)

Når en post skrives til objektet **Udgift** i Dataverse, udløser systemet den automatiserede godkendelsesproces for posten. Den automatiserede godkendelsesprocesstatus kan gennemses i Dataverse, hvis det er nødvendigt, ved at gå til **Avancerede indstillinger** > **System** > **Systemjob**. Når godkendelsen er fuldført, oprettes der udgiftstransaktionsklasseposter i objektet **Faktiske værdier**.

Udgiftsrelaterede faktiske værdier behandles derefter ved hjælp af dobbeltskrivning-tabeltilknytningen **Integration af faktiske værdier i Project Operations (msdyn\_faktiske)**. Du kan finde flere oplysninger under [Projektestimater og faktiske værdier](resource-dual-write-estimates-actuals.md).

Den periodiske proces **Importér fra midlertidig lagring** opretter udgiftsrapportrelaterede kladdelinjer i integrationskladden til Project Operations. Modregningskontoen bruges som standard til udgiftsintegrationskontoen. Bogføringsintegrationskladden rydder kontosaldoen for udgiftstransaktionen, og udgiftsbeløbet flyttes til projektomkostningskontoen. Systemet opretter også underkonto til projekttransaktioner til downstream-fakturering og omsætningsgenkendelse.
