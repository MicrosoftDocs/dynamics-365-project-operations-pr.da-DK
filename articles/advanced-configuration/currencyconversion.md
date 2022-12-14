---
title: Konfigurere valutakonvertering til at beregne salgspriser ud fra omkostningssatser
description: I denne artikel forklares, hvordan du kan konfigurere den funktionsmåde for valutakonvertering, der bruges i Microsoft Dynamics 365 Project Operations , når salgstransaktioner oprettes ud fra omkostningstransaktioner.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816662"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Konfigurere valutakonvertering til at beregne salgspriser ud fra omkostningssatser

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

I Microsoft Dynamics 365 Project Operations kan salgspriser for udgiftskategorier konfigureres som numeriske værdier, eller de kan konfigureres, så de beregnes på baggrund af de omkostninger, der er påløbet.

Når de konfigureres til at blive beregnet på baggrund af de påløbne omkostninger, er følgende indstillinger tilgængelige:

- Til kostpris
- Procentdel af avance i forhold til omkostninger

I scenarier, hvor omkostningsudgifter påløber i en valuta, der adskiller sig fra salgsvalutaen i projektkontrakten, skal der bruges valutakonvertering for at beregne salgsprisen på baggrund af omkostningerne.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Funktionsmåde for valutakonvertering, der bruger indbyggede Dataverse-valutakurser

I Project Operations bruges som standard de valutakurser, der er gemt i valutatabellen i Dataverse. Hvis du vil konfigurere Project Operations til at bruge indbyggede valutakurser til at beregne salgspriser ud fra omkostninger, skal du udføre disse trin.

1. Gå til **Project Operations \> Indstillinger \> Parametre**.
1. Åbn detaljesiden **Projektparameter**.
1. Angiv feltet **Logik for valutakonvertering** til en tom værdi.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Funktionsmåde for valutakonvertering, der bruger valutakurser fra programmer til finans og drift

Valutakurserne i den valutatabel, der som standard er tilgængelig i Dataverse, er ikke datoafhængige. De kan derfor ikke altid skaleres til de krav, du har til beregning af salgspriser ud fra omkostningsprocenter.

Du kan bruge valutakurser fra økonomi- og driftsmiljøet til at beregne salgsprisen i salgsvalutaen ud fra en omkostningssats i omkostningsvalutaen. Benyt følgende fremgangsmåde for at konfigurere denne funktionsmåde for valutakonvertering.

1. Tilføj feltet **Logik for valutakonvertering** på siden **Projektparametre**. Gem og publicer derefter tilpasningen.
1. Gå til **Project Operations \> Indstillinger \> Parametre**.
1. Åbn detaljesiden **Projektparameter**. 
1. Angiv feltet **Funktionsmåde for valutakonvertering** til **Udvidet med fallback til standard**.
1. Giv sikkerhedsrollen **Applikationsbruger med dobbeltskrivning** tilladelsen **Læs globalt** til følgende tabeller:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. I økonomi- og driftsmiljøet skal du køre følgende tilknytninger for dobbeltskrivning med første synkronisering:

    - Valutakurstype (msdyn\_exchangeratetypes)
    - Valutapar for valutakurser (msdyn\_currencyexchangeratepairs)
    - CDS-valutakurser (msdyn\_currencyexchangerates)

Når disse ændringer er fuldført, gør dobbeltskrivning valutakurserne fra økonomi- og driftsmiljøet tilgængelige i Dataverse. Project Operations bruger derefter disse valutakurser til at konvertere omkostningssatser til kontraktens salgsvaluta.

> [!NOTE]
> Denne funktionsmåde for valutakonvertering gælder kun for beregning af salgspriser ud fra omkostningssatser. Den bruges ikke til generisk beregning af værdier i grundvalutaen. Værdier i grundvalutaen bruger altid indbyggede Dataverse-valutakurser, uanset om du fuldfører denne procedure.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
