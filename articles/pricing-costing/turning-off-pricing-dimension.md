---
title: Deaktivering af en prisdimension
description: Dette emne indeholder oplysninger om, hvordan du deaktiverer prisfastsættelsesdimensioner.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 54e02726138f7306481ca50d5204ee29a3b68549
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896499"
---
# <a name="turning-off-a-pricing-dimension"></a>Deaktivering af en prisdimension

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Det kan være nødvendigt at gennemgå og opdatere din prisstrategi hvert andet eller tredje år. Eventuelle opdateringer, du foretager, kræver måske, at du deaktiverer en eksisterende prisdimension og opretter en ny. Du kan f.eks. tidligere have prissat ud fra **Rolle**, men nu har du besluttet at prissætte ud fra **Arbejdserfaring**. Det kan kræve, at du deaktiverer **Rolle** som en prisfastsættelsesdimension og opretter **Arbejdserfaring** som en ny prisfastsættelsesdimension. 

Du deaktiverer en prisdimension, uanset om den er standard eller brugerdefineret, ved at indstille felterne **Gælder for Omkostning** og **Gælder for Salg** i prisdimensionen til **Nej**.

Men når du gør det, kan du få vist fejlmeddelelsen **Prisfastsættelsesdimensionen kan ikke opdateres eller slettes, hvis der er tilknyttede prisposter.**

Denne fejlmeddelelse angiver, at der findes prisposter, der tidligere var konfigureret for den dimension, som bliver deaktiveret. Alle poster for **Rollepris** og **Rolleprisavance**, der refererer til en dimension, skal slettes, før dimensionens anvendelighed kan indstilles til **Nej**. Denne regel gælder både for standardprisdimensioner og eventuelle brugerdefinerede prisdimensioner, som du kan have oprettet. Årsagen til denne validering er, at hver enkelt **Rollepris**-post skal have en entydig kombination af dimensioner. På en prisliste, der hedder **US Cost Rates 2018**, har du f.eks. følgende **Rollepris**-rækker. 

| Standardtitel         | Afdeling    |Enhed   |Pris  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Systemtekniker|Contoso USA|Hour| 100|USD|
| Seniorsystemtekniker|Contoso USA|Hour| 150| USD|


Når du deaktiverer **Standardtitel** som prisfastsættelsesdimension, og prisfastsættelsesfunktionen søger efter en pris, bruger den kun værdien **Afdeling** fra inputkonteksten. Hvis **Afdeling** i inputkonteksten er "Contoso US", er resultatet ikke-deterministisk, da begge rækker stemmer overens. Hvis du vil undgå dette scenario, validerer systemet, at kombinationen af dimensioner er entydig, når du opretter **Rollepris**-poster. Hvis dimensionen er blevet deaktiveret, efter at **Rollepris**-posterne er oprettet, kan denne begrænsning blive overtrådt. Det er derfor nødvendigt, at du sletter alle rækker med **Rollepris** og **Rolleprisavance**, der har den pågældende dimensionsværdi udfyldt, før du deaktiverer en dimension.
