---
title: Hvorfor anvendes en standardpris på nul for faktiske salgsudgifter?
description: Følgende tre kontroller hjælper dig med at foretage fejlfinding af grunden til, at standardprisen på 0 anvendes til faktiske salgsudgifter.
author: rumant
ms.prod: ''
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
ms.openlocfilehash: 6e477b7d5973398d50c6be03469d1c0a792b1b3323522329bc33cba755104968
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000794"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Hvorfor anvendes en standardpris på nul for faktiske salgsudgifter?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse ofte stillede spørgsmål gælder for faktiske udgifter, hvor transaktionsklassen er indstillet til Udgift, og transaktionstypen er Ikke-faktureret salg. Følgende tre kontroller hjælper dig med at foretage fejlfinding af grunden til, at standardprisen (faktureringssatsen) på 0 anvendes til faktiske salgsudgifter.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Kontrol 1: Find salgsprislisten for projektet

Find projektet fra projektfeltet for den faktiske værdi, og gå til projektsiden. Gå derefter til fanen Salg. Klik på linket i feltet Projektkontrakt på gitteret Projektkontraktlinjer. Siden Projektkontrakt åbnes. På siden Projektkontrakt skal du gå til fanen Projektprislister. Se, om der er mindst én prisliste, der er tilknyttet her.

Hvis der ikke er tilknyttet en prisliste i gitteret Projektprislister i Projektkontrakt:

- Tilknyt en prisliste til gitteret Projektprislister. De prislisterne, der kan tilknyttes her, skal have kontekstfeltet indstillet til Salg, og valutafeltet på prislisten skal svare til valutafeltet i projektkontrakten. Når du har foretaget de nødvendige rettelser, skal du genoprette en udgiftspost, godkende den og kontrollere, at de ikke-fakturerede faktiske salgsværdier viser en gyldig pris.
- Hvis du har en eller flere prislister tilknyttet i gitteret Projektprislister for projektkontrakten, kan du gå til Kontrol 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Kontrol 2: Er der nogen af de prislister, der er angivet ovenfor, gyldige for den specifikke dato for den faktiske udgift?

Hvis Project Service skal tage en prisliste for standardprisen i betragtning, skal denne prisliste gælde for datoen i den faktiske salgsudgift. Kontroller følgende for at se, om de prislister, der er identificeret overfor, gælder:

- Start med at kontrollere, at start- og slutdatoer under fanen Generelt for de prislister, der er tilknyttet, ikke er tomme. Hvis start- og slutdatoerne til i prislisterne ovenfor, er tomme, har du isoleret problemet. 
- Noter startdatofeltet i den faktiske salgsudgift, og kontroller, om en eller flere af de prislister, der er identificeret, er relevant for denne dato. Eksempelvis skal datoen for den faktiske udgift ligge inden for start- og slutdatoen på prislisten. 
    - Hvis der ikke er en prisliste, der dækker denne dato på den faktiske salgsudgift, har du isoleret problemet. Du skal ændre start- og slutdatoer på prislisten for at sikre, at prislisten omfatter datoen for den faktiske udgift. 
    - Hvis der er mere end én prisliste, der dækker datoen for den faktiske salgsudgift, har du isoleret problemet. Rediger start- og slutdatoerne på prislisterne, så der er kun én prisliste, der dækker datoen for den faktiske udgift. 
    - Hvis der kun er én prisliste, der dækker datoen for den faktiske udgift, skal du gå til Kontrol 3.
Når du har foretaget de nødvendige rettelser, skal du genoprette en udgiftspost, godkende den og kontrollere, at de ikke-fakturerede faktiske salgsværdier viser en gyldig pris.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Kontrol 3: Findes der en gyldig pris for udgiftskategorien i den aktuelle projektprisliste? 

Hvis du har fuldført kontrol 1 og kontrol 2, bør du kun have én projektprisliste, der gælder for datoen for den faktiske salgsudgift, nu. Åbn denne projektprisliste, og gå til fanen Kategoripriser. Kontroller, at der er en række i gitteret til den specifikke udgiftskategori for den faktiske udgift.
 
- Hvis der ikke er en række, har du isoleret problemet. Opret en række i gitteret Kategoripris for kategorien i den faktiske udgift. Derefter skal du genoprette en udgiftspost, godkende den og kontrollere, at de ikke-fakturerede faktiske salgsværdier viser en gyldig pris. 
- Hvis der findes en række for udgiftskategorien i gitteret Kategoripriser, kan du kontrollere, om den har en gyldig pris.

For at forstå, hvad der er en gyldig pris, skal du bruge følgende metoder:

- Hvis feltet Prissætningsmetode på linjen Kategoripris er indstillet til Til kostpris, vil enhedssatsen på din faktiske salgsudgift have fået standardværdien i udgiftsposten.
- Hvis feltet Prissætningsmetode på linjen Kategoripris er indstillet til Avance som procentdel, skal du kontrollere, om feltet Procent er indstillet til en gyldig værdi. Enhedssatsen i din faktiske salgsudgift er nulstillet til standardværdien, fordi denne avanceprocent er anvendt på prisen i udgiftsposten.
- Hvis feltet Prissætningsmetode på linjen Kategoripris er indstillet til Pris pr. enhed, skal du kontrollere, om feltet Pris er indstillet til en gyldig værdi. Enhedssatsen i den faktiske salgsudgift får standardværdien for det valutabeløb, der er angivet i feltet Pris.

Hvis prisopsætningen for udgiftskategorien ikke er gyldig, har du isoleret problemet. Løsningen er at redigere kategoriprislinjen med en gyldig pris for udgiftskategorien i overensstemmelse med ovenstående regler. Når du har gjort det, skal du genoprette en udgiftspost, godkende den og derefter kontrollere, at de ikke-fakturerede faktiske salgsværdier får en gyldig pris.

Hvis du stadig ikke kan se en gyldig pris i din faktiske salgsudgift, skal du indgive en supportanmodning.




[!INCLUDE[footer-include](../includes/footer-banner.md)]