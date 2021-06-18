---
title: Hvorfor anvendes en standardpris på nul for faktiske tidsrelaterede salgstal?
description: Fejlfinding af, hvorfor en pris får standardværdien 0 for faktiske tidsrelaterede salgstal.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: e32b4c8113afdc18d9b220b1a8daf5007be93ac8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011634"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Hvorfor anvendes en standardpris på nul for faktiske tidsrelaterede salgstal?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse ofte stillede spørgsmål gælder for faktiske værdier, hvor transaktionsklassen er indstillet til Tid, og transaktionstypen er Ikke-faktureret salg. Følgende tre kontroller hjælper dig med at foretage fejlfinding af grunden til, at standardprisen (faktureringssatsen) på 0 anvendes til faktiske tidsrelaterede salgstal.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Kontrol 1: Find salgsprislisten for projektet

Find projektet fra projektfeltet for den faktiske værdi, og gå til projektsiden. Gå derefter til fanen Salg, og klik på linket i feltet Projektkontrakt på gitteret Projektkontraktlinjer. Siden Projektkontrakt åbnes. På siden Projektkontrakt skal du gå til fanen Projektprislister. Se, om der er mindst én prisliste, der er tilknyttet her. Hvis der ikke er tilknyttet en prisliste i gitteret Projektprislister i Projektkontrakt, har du isoleret problemet. Tilknyt en prisliste til gitteret Projektprislister. De prislisterne, der kan tilknyttes her, skal have kontekstfeltet indstillet til Salg, og valutafeltet på prislisten skal svare til valutafeltet i projektkontrakten. Når du har foretaget de nødvendige rettelser, skal du genoprette en tidsrelateret post, godkende den og kontrollere, at de ikke-fakturerede faktiske salgsværdier viser en gyldig pris. 

Hvis du har en eller flere prislister tilknyttet i gitteret Projektprislister for projektkontrakten, kan du gå til den næste kontrol i dokumentet.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Kontrol 2: Er der nogen af de prislister, der er angivet ovenfor, gyldige for den specifikke dato for faktiske tidsrelaterede salgstal?

Hvis Project Service skal tage en prisliste for standardprisen i betragtning, skal denne prisliste gælde for datoen i de faktiske tidsrelaterede salgstal. Kontroller følgende for at se, om de prislister, der er identificeret overfor, gælder:
- Kontroller, at start- og slutdatoer under fanen Generelt for de prislister, der er tilknyttet, ikke er tomme. Hvis start- og slutdatoerne til i prislisterne ovenfor, er tomme, har du isoleret problemet. 
- Noter startdatofeltet i de faktiske tidsrelaterede salgstal, og kontroller, om en eller flere af de prislister, der er identificeret, er relevant for denne dato. Eksempelvis skal datoen for de faktiske tidsrelaterede salgstal ligge inden for start- og slutdatoen på prislisten. 
    - Hvis der ikke er en prisliste, der dækker denne dato på de faktiske tidsrelaterede salgstal, har du isoleret problemet. Du skal ændre start- og slutdatoer på prislisten for at sikre, at prislisten omfatter datoen for de faktiske tidsrelaterede salgstal. 
    - Hvis der er mere end én prisliste, der dækker datoen for de faktiske tidsrelaterede salgstal, har du isoleret problemet. Du kan løse dette problem ved at redigere start- og slutdatoerne på prislisterne, så der er kun én prisliste, der dækker datoen for de faktiske tidsrelaterede salgstal. 
    - Hvis der kun er én prisliste, der dækker datoen for de faktiske tidsrelaterede salgstal, skal du gå til Kontrol 3.
Når du har foretaget de nødvendige rettelser, skal du genoprette en tidsrelateret post, godkende den og kontrollere, at de faktiske tidsrelaterede salgstal viser en gyldig pris.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Kontrol 3: Findes der en pris på prislisten for prissætningsdimensionerne i de faktiske tidsrelaterede salgstal?

Hvis du har fuldført kontrol 1 og kontrol 2, bør du kun have én prisliste, der gælder for datoen for de faktiske tidsrelaterede salgstal, nu. Åbn denne projektprisliste, og gå til fanen Rollepriser. Kontroller, at der er en række i gitteret til prissætningsdimensionerne i de faktiske tidsrelaterede salgstal.

Hvis der ikke er en række i rolleprisgitteret for prissætningsdimensionerne i de faktiske tidsrelaterede salgstal, har du isoleret problemet. Opret en række i gitteret Rollepriser til prissætningsdimensionerne i dine faktiske tidsrelaterede salgstal. Når du har gjort det, skal du genoprette en tidsrelateret post, godkende den og kontrollere, at de faktiske tidsrelaterede salgstal viser en gyldig pris.

Hvis du stadig ikke kan se en gyldig pris i dine faktiske tidsrelaterede salgstal, skal du anmode om support. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]