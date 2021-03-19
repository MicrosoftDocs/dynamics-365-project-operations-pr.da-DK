---
title: Enhedsgrupper og enheder
description: Dette emne indeholder oplysninger om enhedsgrupper og enheder.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 45e4a95b429cd9d1f174653bd28cf567f690676d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291612"
---
# <a name="unit-groups-and-units"></a>Enhedsgrupper og enheder

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Enhedsgrupper og enheder er basisenhederne i Microsoft Dynamics 365. En enhed er en enkelt måleenhed, og flere enheder kan grupperes i enhedsgrupper. En enhedsgruppe kaldes undertiden en enhedsplan i brugergrænsefladen i Dynamics 365. 

Her er nogle eksempler på enheder og enhedsgrupper:
 
- **Enhedsgruppe**: afstand 
    - **Enheder**: mile, kilometer, osv.
- **Enhedsgruppe**: Tid
    - **Enheder**: time, day, uge osv. 

Når du konfigurerer flere enheder i en enhedsgruppe, skal du også konfigurere en konverteringsfaktor mellem dem ved at angive den første enhed, du konfigurerer, som standardenhed eller den primære enhed for enhedsgruppen. 

Hvis du f.eks. i en **Tid**-enhedsgruppe konfigurerer **Time** som første enhed, definerer systemet **Time** som standardenhed. Hvis den næste enhed, du konfigurerer, er **Dag**, skal du konfigurere en konverteringsfaktor for **Dag** til **Time**. Hvis du derefter tilføjer **Uge** som en tredje enhed, skal du konfigurere en konverteringsfaktor for **Uge** i forhold til **Dag** eller **Time**. 

I følgende billede vises et eksempel på en opsætning af enheden **Dag** , hvor feltet **Antal** viser det antal timer, der er på en dag, og **Uge**, hvor feltet **Antal** indeholder antallet af dage i en uge.

> ![Enhedsgruppe: siden Oplysninger](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Brug af enheder og enhedsgrupper

Dynamics 365 Project Service Automation bruger enheder og enhedsgrupper til at behandle estimater og poster for både udgifter og tid. 

For udgifter har de enkelte udgiftskategorier en standardenhedsgruppe og -enhed. Disse værdier angives som standardværdier på prislisteposter for udgiftskategorier. 

Du kan f.eks have en udgiftskategori med navnet **Kørsel**. Den har en enhedsgruppe med navnet **Afstand** og en standardenhed med navnet **Kilometer**. Hvis du konfigurerer **Afstand**-enhedsgruppen, så den har to enheder (**Mile** og **Kilometer**), kan du oprette to priser for **Kørsel**-kategorien på én prisliste: pris pr. mile og pris pr. kilometer.

| Udgiftskategori  | Enhedsgruppe  | Enhed      | Prissætningsmetode  | Pris pr. enhed  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kørsel           | Afstand      | Mile      | Pris pr. enhed    | 10 USD            |
| Kørsel           | Afstand      | Kilometer | Pris pr. enhed    |  6 USD            |

Når du angiver en udgift på et projekt, bestemmer systemet prisen via kombinationen af kategorien og enheden på udgiften. 

| Beskrivelse af udgift        | Udgiftskategori  | Enhed  | Antal  | Enhedspris   |
|----------------------------|---------------------|-------|-----------|----------------|
| Kørsel til kundeadresse | Kørsel             | Mile  | 10        | 10 USD         |

For tiden indeholder hver prislisteoverskrift et **Standardtidsenhed**-felt. Værdien angives, når du opretter prislisteoverskriften. Denne enhed bruges derefter til at angive alle rollebaserede priser på prislisten.

Der kan udtrykkes estimatlinjer for feltet **Tid på tilbud** i en hvilken som helst tidsenhed. Dog kan der kun bruges **Time** som tidsenhed i estimatlinjer og tidsregistreringer på projekter. Hvis enheden på tidsregistreringen eller estimatlinjen ikke stemmer overens med enheden på prislistelinjen for den pågældende rolle, vil systemet konvertere prisen til de enheder, der er defineret i projektestimatet eller den faktiske transaktion for projektet.

I følgende eksempel vises, hvordan PSA bruger enhedsgruppe, enheder og konverteringsfaktorer.
- Enheder

   - **Enhedsgruppe**: Tid 
   - **Enheder**: time 
    
    - **Dag** – Konverteringsfaktor: 8 timer       
    - **Uge** – Konverteringsfaktor: 40 timer  
        
- Opsætning af prisliste i projekt A:

    - **Navn**: Britiske salgspriser 2016 
    - **Standardtidsenhed**: dag 
    - **Valuta**: GBP

| Rolle      | Enhedsgruppe | Enhed | Afdeling: | Pris   |
|-----------|------------|------|---------------------|---------|
| Udvikler | Tidspunkt       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Tidsregistrering

I tabellen nedenfor vises den endelige transaktion på salgssiden, der er oprettet af PSA for et tre timers projekt.


| Projekt   | Opgave    | Rolle      | Antal | Enhed  | Enhedspris | Ikke-faktureret salgsbeløb |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Design  | Udvikler | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Ofte stillede spørgsmål til tidsenhed

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Konverteres PSA til forskellige enheder i forbindelse med udgifter?
Nej. Enhedskonvertering kan kun bruges til tid. Hvis systemet ikke kan finde en udgiftspris for kombinationen af udgiftskategorien og enheden, angives prisen til 0,00 som standard.

### <a name="why-does-psa-convert-time-units"></a>Hvorfor konverteres tidsenheder af PSA?
I visse lande eller områder er der et juridisk krav om, at fakturasatser er konfigureret i antal dage. Prisforhandling og rabatgivning i løbet af tilbudsforløbet sker ved hjælp af dagstakster for hver fakturerbar rolle. Estimeret tidsplan og tidsregistrering udføres i timer. For at understøtte denne forskel i tidsenheder konverteres tidsenheder i PSA.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Kan tidsenheder ændres i projektestimater?
Nej. Estimeret tidsplan er i øjeblikket begrænset til timer og kan ikke ændres.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Kan enheder og enhedsgrupper redigeres, slettes og tilføjes?
Ja. Med undtagelse af enhedsgruppen **Tid** og enheden **Time** kan alle enheder slettes eller redigeres, og der kan tilføjes nye enheder. I PSA kan enhedsgruppen **Tid** og enheden **Time** ikke slettes. De kan dog opdateres med en oversat tekst til feltet **Navn**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]