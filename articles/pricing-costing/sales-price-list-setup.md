---
title: Opsætning af salgsprisliste
description: Dette emne indeholder oplysninger om salgsprislister til prisfastsættelse af projekter.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074227"
---
# <a name="sales-price-list-setup"></a>Opsætning af salgsprisliste

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I forbindelse med projekttilbud og kontrakter har en projektprisliste et andet mønster for pristilsidesættelse end en produktprisliste. På en produktkatalogbaseret tilbudslinje kan du tilsidesætte prisen på roller og kategorier direkte på tilbudslinjen, da alle tilbudslinjer peger på præcist ét katalogelement. Men på en projektbaseret tilbudslinje kan du dog ikke tilsidesætte prisen for roller og kategorier direkte på tilbudslinjen. Du kan bruge projektprislisten til at arbejde med de to forskellige tilsidesættelses mønstre.

> [!NOTE]
> Det anbefales, at du har en separat prisliste for projektressourcerne og dine katalogelementer på grund af de funktionsmæssige forskelle mellem de to, når du tilsidesætter prissætningen.

Hvert af følgende objekter kan have en eller flere tilknyttede salgsprislister for projektprissætning:

- Kunde (konto) 
- Salgsmulighed 
- Tilbud 
- Projektkontrakt

Tilknytningen af disse objekter til en prisliste angives af listerne over projektpriser. Du kan knytte en eller flere prislister til salgsobjekterne Kunde, Salgsmulighed, Tilbud og Projektkontrakt.

Der angives ikke automatisk en standardprisliste for projekter på en kundepost. Du kan dog manuelt knytte en liste over projektpriser til kundeposten. Du bør dog kun tilknytte en liste med projektpriser manuelt, hvis du har en bestemt prisaftale med kunden. 

Når en projektprisliste er knyttet til et salgsobjekt, valideres følgende oplysninger:

- Prislisten har konteksten **Salg**. 
- Valutaen for prislisten svarer til kundevalutaen. 

I en projektkontrakt bruges følgende prioriteret rækkefølge til automatisk at angive tilknyttede projektprislister:

1. Tilbud
2. Salgsmulighed
3. Kunde 
4. Globale indstillinger 

Når en projektprisliste angives som standard, validerer systemet, om valutaen stemmer overens med kundens valuta, og at de standardprislister, der er angivet, har en kontekst af **Salg**.

Du kan knytte flere projektprislister til objekterne Kunde, Salgsmulighed, Tilbud og Projektkontrakt. Denne funktion understøtter datospecifikke standardpriser for en længerevarende projektkontrakt, hvor der kan kræves mere end én prisliste for at tage højde for prisopdateringer, der opstår på grund af inflation. Men hvis de prislister, du knytter til kunde-, salgsmuligheds-, tilbuds- eller projektkontraktobjektet, har et overlappende datointerval, kan standardpriserne være forkerte. Du skal derfor sikre dig, at de projektprislister, der har overlappende datointerval, ikke er knyttet til disse objekter.
