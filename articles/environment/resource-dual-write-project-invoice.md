---
title: Integration af projektfaktura
description: Dette emne indeholder oplysninger om integration af dobbeltskrivning i Project Operations til kundefakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996559"
---
# <a name="project-invoice-integration"></a>Integration af projektfaktura

Dette emne indeholder oplysninger om integration af dobbeltskrivning i Project Operations til kundefakturering.

I Project Operations administrerer projektlederen efterslæbet af projektfakturering og opretter en proformafaktura for kunden i Microsoft Dataverse. På baggrund af denne proformafaktura opretter kreditormedarbejderen eller projektrevisoren en kundeorienteret faktura. Integration med dobbeltskrivning sikrer, at oplysningerne på proformafakturaen synkroniseres med Finance and Operations-apps. Når den kundeorienterede faktura er bogført, opdaterer systemet de relevante faktiske projekttal i Dataverse med de relevante regnskabsdetaljer. Følgende grafik giver en overordnet begrebsmæssig oversigt over denne integration.

   ![Integration af projektfaktura](./media/DW5Invoicing.png)

Når projektlederen bekræfter proformafakturaen i Dataverse, synkroniseres oplysningerne om proformafakturaens overskrift i til Finance and Operations-apps ved hjælp af dobbelteskrivning-tabeltilknytningen **Projektfakturaforslag V2 (fakturaer)**. Dette er en envejsintegration fra Dataverse til Finance and Operations-apps. Oprettelse eller sletning af projektfakturaforslag direkte i Finance and Operations-apps understøttes ikke.

Fakturabekræftelsen i Dataverse udløser også forretningslogikken, når der oprettes faktureringsrelaterede poster i objektet **Faktiske tal**. Disse poster synkroniseres med Finance and Operations ved hjælp af dobbeltskrivning-tabeltilknytningen **Integration af faktiske værdier i Project Operations (msdyn\_faktiske)**. Du kan finde flere oplysninger under [Projektestimater og faktiske værdier](resource-dual-write-estimates-actuals.md). 

Linjer i forslag til projektfakturaer oprettes af den periodiske proces **Import af midlertidig lagringsformular**. Denne proces er baseret på de faktiske fakturerede salgsdetaljer i tabellen **Faktisk midlertidig lagring**. Du kan finde flere oplysninger i [Administrer forslag til projektfakturaer](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
