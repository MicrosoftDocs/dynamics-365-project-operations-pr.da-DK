---
title: Hvorfor anvendes en standardpris på nul for faktiske tidsrelaterede omkostninger?
description: Fejlfinding af, hvorfor en pris får standardværdien 0 for faktiske tidsrelaterede omkostninger.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146251"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Hvorfor anvendes en standardpris på nul for faktiske tidsrelaterede omkostninger?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse ofte stillede spørgsmål gælder for faktiske værdier, hvor transaktionsklassen er indstillet til Tid, og transaktionstypen er Omkostning. Følgende tre kontroller hjælper dig med at foretage fejlfinding af grunden til, at standardprisen på 0 anvendes til faktiske tidsrelaterede omkostninger.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Kontrol 1: Find kostprislisten for projektet

Find projektet fra projektfeltet for den faktiske værdi, og gå derefter til projektsiden. Klik på linket til kontraktenheden i feltet. Kontroller, om kontraktenheden har en prisliste i gitteret Kostprislister, på siden Kontraktenhed.

Hvis der er mere end én prisliste, har du isoleret problemet. Project Service understøtter kun én prisliste pr. afdeling. Fjern alle prislister fra dette objekt, indtil der kun én prisliste tilknyttet i gitteret Kostprislister for afdelingen.

Hvis der ikke er en prisliste knyttet til afdelingen, skal du notere valutaen i afdelingen. Gå til Project Service og til Parametre, og åbn fanen Prislister. Kontroller, om der er nogen prislister, hvor konteksten er indstillet til Omkostninger og valuta, og som stemmer overens med valutaen i afdelingen.
 
Hvis der ikke er nogen prislister, der svarer til de pågældende kriterier, har du isoleret problemet. Sørg for, at du har mindst én prisliste, hvis kontekst er indstillet til Omkostninger, og hvis valuta svarer til valutaen i afdelingen.

Hvis der findes mere end én prisliste, der svarer til de pågældende kriterier, skal du fortsætte med at læse dette dokument for at foretage yderligere kontrol.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Kontrol 2: Er der nogen af de prislister, der er angivet ovenfor, gyldige for den specifikke dato for den faktiske tidsrelaterede omkostning?

Hvis Project Service skal tage en prisliste for standardprisen i betragtning, skal denne prisliste gælde for datoen i den faktiske tidsrelaterede omkostning. Kontroller følgende for at se, om de prislister, der er identificeret overfor, gælder:

- Kontroller, at start- og slutdatoer under fanen Generelt for de prislister, der er tilknyttet, ikke er tomme. Hvis start- og slutdatoerne til i prislisterne ovenfor, er tomme, har du isoleret problemet. 
- Noter startdatofeltet i den faktiske tidsrelaterede omkostning, og kontroller, om en eller flere af de prislister, der er identificeret, er relevant for denne dato. Eksempelvis skal datoen for den faktiske tidsrelaterede omkostning ligge inden for start- og slutdatoen på prislisten. 
    - Hvis der ikke er en prisliste, der dækker denne dato på den faktiske tidsrelaterede omkostning, har du isoleret problemet. Du skal ændre start- og slutdatoer på prislisten for at sikre, at prislisten omfatter datoen for den faktiske tidsrelaterede omkostning. 
    - Hvis der er mere end én prisliste, der dækker datoen for den faktiske tidsrelaterede omkostning, har du isoleret problemet. Du kan løse dette problem ved at redigere start- og slutdatoerne på prislisterne, så der er kun én prisliste, der dækker datoen for den faktiske tidsrelaterede omkostning. 
    - Hvis der kun er én prisliste, der dækker denne dato for den faktiske tidsrelaterede omkostning, skal du gå til den næste kontrol i dokumentet.
Når du har foretaget de nødvendige rettelser, skal du genoprette en tidsrelateret post, godkende den og kontrollere, at den faktiske tidsrelaterede omkostning viser en gyldig pris.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Kontrol 3: Findes der en pris på prislisten for prissætningsdimensionerne i den faktiske tidsrelaterede omkostning?

Hvis du har fuldført kontrol 1 og kontrol 2, bør du kun have én prisliste, der gælder for datoen for den faktiske tidsrelaterede omkostning, nu. Åbn denne projektprisliste, og gå til fanen Rollepriser. Kontroller, at der er en række i gitteret til prissætningsdimensionerne i den faktiske tidsrelaterede omkostning.

Hvis der ikke er en række i rolleprisgitteret for prissætningsdimensionerne i den faktiske tidsrelaterede omkostning, har du isoleret problemet. Opret en række i gitteret Rollepriser til prissætningsdimensionerne i din faktiske tidsrelaterede omkostning. Når du har gjort det, skal du genoprette en tidsrelateret post, godkende den og kontrollere, at den faktiske tidsrelaterede omkostning viser en gyldig pris.
 
Hvis du stadig ikke kan se en gyldig pris i din faktiske tidsrelaterede omkostning, skal du anmode om support.





[!INCLUDE[footer-include](../includes/footer-banner.md)]