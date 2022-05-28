---
title: Konfigurer udgiftspolitikker
description: Du kan konfigurere udgiftspolitikker, som medarbejderne skal følge, når de registrerer og sender rejserekvisitioner og udgiftsrapporter i Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3dc5d1768b57baa68f134af318dd9d2d7cdd756
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684727"
---
# <a name="set-up-expense-policies"></a>Konfigurer udgiftspolitikker

Du kan definere de politikker, som dine medarbejder skal følge, når de angiver og indsender udgiftsrapporter og rejserekvisitioner.         
Implementering af udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt.         

Du kan f.eks. angive en politik for hoteludgifter i New York City, hvor det angives, at udgifterne pr. nat ikke må overstige 250 USD.       
Hvis en arbejder indsender en udgiftsrapport eller rejserekvisition, hvori værelsestaksten overstiger dette beløb, vil systemet underrette den        
arbejder, som har overskredet politikbeløbet. Du kan konfigurere den meddelelse, som arbejderen modtager, når du        
definere politikken.      
        
Du kan definere tre typer politikker:         
        
- Advarsel – Gør det muligt for arbejderen at indsende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og        
  til senere rapportering.        

- Fejl – Arbejderen skal revidere udgiften for at overholde politikken, før denne indsender udgiftsrapporten eller rejserekvisitionen.       
 
 - Begrundelse – Arbejderen eller en leder skal angive en begrundelse for at overskride politikbeløbet, før udgiftsrapporten eller rejserekvisitionen indsendes.        

## <a name="policy-tips"></a>Politiktips
Her er et par forslag, der kan hjælpe dig med at oprette nye politikker for udgiftsstyring. 
* Politikker træder i kraft på en angiven dato og træder ikke i kraft, hvis en politik oprettes med en dato efter den dato, hvor udgiften fandt sted. Hvis du f.eks. opretter en ny politik i dag for at gennemtvinge et loft over udgifter til måltider på 50 $, kontrolleres eventuelle eksisterende udgifter, der blev angivet pr. gårsdagens dato, ikke i forhold til denne politik.
* Når du opretter en politik for en udgiftskategori, der kan specificeres, skal du overveje at tilføje en betingelse for udgiftslinjetype. Nogle politikker, som f.eks. kræver en kvittering, giver muligvis ikke mening for specificerede linjer og skal kun anvendes på hovedlinjen eller en ikke-specificeret linje. 
* Politikker for udgiftsstyring evalueres som standard i forhold til kildeobjektet. I forbindelse med interne scenarier kan du i stedet angive den politik, der skal evalueres i forhold til destinationsenheden (lånt enhed). Hvis du vil køre politikkerne i forhold til destinationsenheden, skal du aktivere funktionen "Evaluer udgiftspolitik i forhold til den juridiske låneenhed" i arbejdsområdet **Funktionsstyring**.

## <a name="when-to-evaluate-policies"></a>Tidspunkt for evaluering af politikker

I parametre for udgiftsstyring findes en indstillingen, hvor du kan evaluere politikker for udgiftsstyring, enten når en linje gemmes, eller når der indsendes en udgiftsrapport. Hvis du vælger at evaluere, når en linje gemmes, sikrer dette, at brugerne får tidligere indsigt i, hvad de skal gøre for at fuldføre deres udgiftsrapporter på én gang. Ellers kan du udskyde evalueringen af politikker og spare tid, hvis du validerer til slut i forbindelse med indsendelsen til arbejdsprocessen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]