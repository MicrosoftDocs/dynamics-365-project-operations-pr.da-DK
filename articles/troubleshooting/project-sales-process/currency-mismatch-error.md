---
title: Fejl i valutauoverensstemmelse
description: Dette emne indeholder fejlfindingsoplysninger om en fejl i en valutauoverensstemmelse, der opstår, når du gemmer bestemte posttyper.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589741"
---
# <a name="currency-mismatch-error"></a>Fejl i valutauoverensstemmelse 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når du gemmer et projekt, en kontrakt, et tilbud eller en ressource, der kan reserveres, modtager du måske fejlmeddelelsen: **Ejende virksomhedsvaluta stemmer ikke overens med kontraktsenhedens valuta. Vælg en anden ejende virksomhed eller kontraktenhed for at fortsætte**. Dette skyldes, at der er en valutauoverensstemmelse mellem den kontraherende enheds valuta for posten og den ejende virksomheds valuta.


## <a name="resolution"></a>Løsning

Du kan løse dette problem ved at gøre følgende:
- Kontrollér valutaen for den kontraherende enhed, der skal bruges for denne post. Du kan se valutaen ved at åbne afdelingsposten og kontrollere værdien under fanen **Generelt** i feltet **Valuta**.
- Kontrollér valutaen for den ejende virksomhed. Du kan se valutaen ved at gå til **Relaterede** > **Hovedbøger** i firmaposten. Dobbeltklik på den hovedbogspost, der er knyttet til virksomheden, og kontrollér værdien under fanen **Generelt** i feltet **Regnskabsvaluta**.

Hvis den valuta, der er angivet i den kontraherende enhed, og posten i hovedbogen ikke stemmer overens, skal du justere konfigurationen eller vælge andre værdier, når du gemmer posten. Systemet kræver, at disse poster stemmer overens for at sikre korrekte interne faktureringsforløb. Du kan finde flere oplysninger om interne konfigurationer under [Oprettelse af interne transaktioner](../../project-accounting/create-intercompany-transactions.md).

Hvis firmaposten ikke har nogen tilknyttet hovedbog, indikerer det, at der mangler en konfigurationen, når miljøet konfigureres. Konfigurationen skal korrigeres af systemadministratoren. Systemadministratoren skal gå til **Konfigurationer af dobbelt skrivning** og stoppe og genstarte **Tilknytning af hovedbøger med dobbelt skrivning** med den første synkronisering af denne tilknytning og dennes forudsætninger. Du kan finde flere oplysninger i [versioner af tilknytning af dobbeltskrivning i Project Operations](../../environment/resource-dual-write-maps.md).
