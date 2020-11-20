---
title: Definer udgiftspolitikker
description: Du kan definere de udgiftspolitikker, som dine medarbejder skal følge, når de angiver og indsender udgiftsrapporter og rejserekvisitioner.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128411"
---
# <a name="define-expense-policies"></a>Definer udgiftspolitikker

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan definere de politikker, som dine medarbejder skal følge, når de angiver og indsender udgiftsrapporter og rejserekvisitioner.         
Implementering af udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt.         

Du kan f.eks. angive en politik for hoteludgifter i New York City, hvor det angives, at udgifterne pr. nat ikke må overstige 250 USD.       
Hvis en arbejder indsender en udgiftsrapport eller rejserekvisition, hvor værelsestaksten overstiger dette beløb, vil systemet underrette         
arbejder, som har overskredet politikbeløbet. Du kan konfigurere den meddelelse, som arbejderen modtager, når du        
definere politikken.      
        
Du kan definere tre typer politikker:         
        
- **Advarsel**: Gør det muligt for arbejderen at indsende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og         
  til senere rapportering.        

- **Fejl** : Arbejderen skal revidere udgiften for at overholde politikken, før denne indsender udgiftsrapporten eller rejserekvisitionen.        
 
 - **Begrundelse** : Arbejderen eller en leder skal angive en begrundelse for at overskride politikbeløbet, før udgiftsrapporten eller rejserekvisitionen indsendes.        

## <a name="policy-tips"></a>Politiktips
Her er et par forslag, der kan hjælpe dig med at oprette nye politikker for udgiftsstyring: 

- Politikker træder i kraft på en angiven dato, hvilket betyder, at en politik ikke træder i kraft, hvis den oprettes med en dato efter den dato, hvor udgiften fandt sted. Du kan f.eks. oprette en ny politik i dag for at gennemtvinge et maksimalt beløb for udgifter til måltider på 50 USD. Eksisterende udgifter, der er angivet i går, kontrolleres ikke i forhold til denne politik.
- Når du opretter en politik for en udgiftskategori, der kan specificeres, skal du overveje at tilføje en betingelse for udgiftslinjetype. Nogle politikker, f.eks. dem, der kræver en kvittering, giver muligvis ikke mening for specificerede linjer. I denne situation gælder politikken kun for overskriftslinjen eller en ikke-specificeret linje. 
- Politikker for udgiftsstyring evalueres som standard i forhold til kildeobjektet. I forbindelse med interne scenarier kan du i stedet angive den politik, der skal evalueres i forhold til destinationsenheden (lånt enhed). Hvis du vil køre politikkerne i forhold til destinationsenheden, skal du aktivere funktionen **Evaluer udgiftspolitik i forhold til den juridiske låneenhed** i arbejdsområdet **Funktionsstyring**.

## <a name="when-to-evaluate-policies"></a>Tidspunkt for evaluering af politikker

I parametre for udgiftsstyring kan du vælge at evaluere politikker for udgiftsstyring, når en linje gemmes, eller når der indsendes en udgiftsrapport. Hvis du vælger at evaluere, når en linje gemmes, får brugerne tidligere indsigt i, hvad de skal gøre for at fuldføre deres udgiftsrapporter på én gang. Ellers kan du forsinke evalueringen af politikker og spare tid ved at validere den til slut i forbindelse med indsendelsen til arbejdsprocessen.
