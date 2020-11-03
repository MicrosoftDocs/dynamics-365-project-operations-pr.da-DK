---
title: Slå en prisdimension fra
description: I dette emne vises, hvordan du kan konfigurere prisdimensioner i Project Service-løsningen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074257"
---
# <a name="turn-off-a-pricing-dimension"></a>Slå en prisdimension fra

Det kan være nødvendigt at gennemgå og opdatere din prisstrategi hvert andet eller tredje år. Eventuelle opdateringer, du foretager, kræver måske, at du deaktiverer en eksisterende prisdimension og opretter en ny. Du kan f.eks. tidligere have prissat ud fra **Rolle** , men nu har du besluttet at prissætte ud fra **Arbejdserfaring**. Det kan kræve, at du deaktiverer **Rolle** som en prisdimension og opretter **Arbejdserfaring** som en ny prisdimension. 

Du deaktiverer en prisdimension, uanset om den er standard eller brugerdefineret, ved at indstille felterne **Gælder for Omkostning** og **Gælder for Salg** i prisdimensionen til **Nej**.

Men når du gør dette, modtager du måske følgende fejlmeddelelse.

![Forretningsprocesfejl er sandsynlig, når du deaktiverer en prisdimension](media/Business-Process-Error.png)


Denne fejlmeddelelse angiver, at der findes prisposter, der tidligere var konfigureret for den dimension, som bliver deaktiveret. Alle poster for **Rollepris** og **Rolleprisavance** , der refererer til en dimension, skal slettes, før dimensionens anvendelighed kan indstilles til **Nej**. Denne regel gælder både for standardprisdimensioner og eventuelle brugerdefinerede prisdimensioner, som du kan have oprettet. Årsagen til denne validering er, at Project Service har den begrænsning, at hver enkelt **Rollepris** -post skal have en entydig kombination af dimensioner. På en prisliste, der hedder **US Cost Rates 2018** , har du f.eks. følgende **Rollepris** -rækker. 

| Standardtitel         | Afdeling    |Enhed   |Pris  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Systemtekniker|Contoso USA|Hour| 100|USD|
| Seniorsystemtekniker|Contoso USA|Hour| 150| USD|


Når du slår **Standardtitel** fra som prisdimension, og prissætningsfunktionen i Project Service søger efter en pris, bruger den kun værdien **Afdeling** fra inputkonteksten. Hvis **Afdeling** i inputkonteksten er "Contoso US", er resultatet ikke-deterministisk, da begge rækker stemmer overens. Hvis du vil undgå dette scenario, validerer Project Service, at kombinationen af dimensioner er entydig, når du opretter **Rollepris** -poster. Hvis dimensionen er blevet deaktiveret, efter at **Rollepris** -posterne er oprettet, kan denne begrænsning blive overtrådt. Det er derfor nødvendigt, at du sletter alle rækker med **Rollepris** og **Rolleprisavance** , der har den pågældende dimensionsværdi udfyldt, før du deaktiverer en dimension.

