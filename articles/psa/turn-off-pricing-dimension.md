---
title: Slå en prisdimension fra
description: Denne artikel viser, hvordan du kan konfigurere prisfastsættelsesdimensioner i Project Service-løsningen.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 81c3cfaad8dc8d057985b509f20c3ba31de45e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913153"
---
# <a name="turn-off-a-pricing-dimension"></a>Slå en prisdimension fra

[!include [banner](../includes/psa-now-project-operations.md)]

Det kan være nødvendigt at gennemgå og opdatere din prisstrategi hvert andet eller tredje år. Eventuelle opdateringer, du foretager, kræver måske, at du deaktiverer en eksisterende prisdimension og opretter en ny. Du kan f.eks. tidligere have prissat ud fra **Rolle**, men nu har du besluttet at prissætte ud fra **Arbejdserfaring**. Det kan kræve, at du deaktiverer **Rolle** som en prisdimension og opretter **Arbejdserfaring** som en ny prisdimension. 

Du deaktiverer en prisdimension, uanset om den er standard eller brugerdefineret, ved at indstille felterne **Gælder for Omkostning** og **Gælder for Salg** i prisdimensionen til **Nej**.

Men når du gør dette, modtager du måske følgende fejlmeddelelse.

![Forretningsprocesfejl er sandsynlig, når du deaktiverer en prisdimension.](media/Business-Process-Error.png)


Denne fejlmeddelelse angiver, at der findes prisposter, der tidligere var konfigureret for den dimension, som bliver deaktiveret. Alle poster for **Rollepris** og **Rolleprisavance**, der refererer til en dimension, skal slettes, før dimensionens anvendelighed kan indstilles til **Nej**. Denne regel gælder både for standardprisdimensioner og eventuelle brugerdefinerede prisdimensioner, som du kan have oprettet. Årsagen til denne validering er, at Project Service har den begrænsning, at hver enkelt **Rollepris**-post skal have en entydig kombination af dimensioner. På en prisliste, der hedder **US Cost Rates 2018**, har du f.eks. følgende **Rollepris**-rækker. 

| Standardtitel         | Afdeling    |Enhed   |Pris  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Systemtekniker|Contoso USA|Hour| 100|USD|
| Seniorsystemtekniker|Contoso USA|Hour| 150| USD|


Når du slår **Standardtitel** fra som prisdimension, og prissætningsfunktionen i Project Service søger efter en pris, bruger den kun værdien **Afdeling** fra inputkonteksten. Hvis **Afdeling** i inputkonteksten er "Contoso US", er resultatet ikke-deterministisk, da begge rækker stemmer overens. Hvis du vil undgå dette scenario, validerer Project Service, at kombinationen af dimensioner er entydig, når du opretter **Rollepris**-poster. Hvis dimensionen er blevet deaktiveret, efter at **Rollepris**-posterne er oprettet, kan denne begrænsning blive overtrådt. Det er derfor nødvendigt, at du sletter alle rækker med **Rollepris** og **Rolleprisavance**, der har den pågældende dimensionsværdi udfyldt, før du deaktiverer en dimension.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
