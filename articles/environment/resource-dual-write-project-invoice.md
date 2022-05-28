---
title: Integration af projektfaktura
description: Dette emne indeholder oplysninger om integration af dobbeltskrivning i Project Operations til kundefakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581231"
---
# <a name="project-invoice-integration"></a>Integration af projektfaktura

Dette emne indeholder oplysninger om integration af dobbeltskrivning i Project Operations til kundefakturering.

I Project Operations administrerer projektlederen efterslæbet af projektfakturering og opretter en proformafaktura for kunden i Microsoft Dataverse. På baggrund af denne proformafaktura opretter kreditormedarbejderen eller projektrevisoren en kundeorienteret faktura. Integration med dobbelt skrivning sikrer, at oplysningerne om proformafakturaen synkroniseres med programmer til finans og drift. Når den kundeorienterede faktura er bogført, opdaterer systemet de relevante faktiske projekttal i Dataverse med de relevante regnskabsdetaljer. Følgende grafik giver en overordnet begrebsmæssig oversigt over denne integration.

   ![Integration af projektfaktura.](./media/DW5Invoicing.png)

Når projektlederen bekræfter proformafakturaen i Dataverse, synkroniseres oplysningerne i proformafakturaens overskrift med programmer til finans og drift ved hjælp af den dobbelte tabeltilknytning **Projektfakturaforslag V2 (fakturaer)**. Dette er en envejsintegration fra Dataverse til programmer til finans og drift. Oprettelse eller sletning af projektfakturaforslag direkte i programmer til finans og drift understøttes ikke.

Fakturabekræftelsen i Dataverse udløser også forretningslogikken, når der oprettes faktureringsrelaterede poster i objektet **Faktiske tal**. Disse poster synkroniseres med Finance and Operations ved hjælp af tabeltilknytning med dobbelt skrivning **Integration af faktiske værdier i Project Operations (msdyn\_actuals)**. Du kan finde flere oplysninger under [Projektestimater og faktiske værdier](resource-dual-write-estimates-actuals.md). 

Linjer i forslag til projektfakturaer oprettes af den periodiske proces **Import af midlertidig lagringsformular**. Denne proces er baseret på de faktiske fakturerede salgsdetaljer i tabellen **Faktisk midlertidig lagring**. Du kan finde flere oplysninger i [Administrer forslag til projektfakturaer](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
