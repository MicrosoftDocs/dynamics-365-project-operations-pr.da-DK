---
title: Produktprislister
description: Dette emne indeholder oplysninger om prislisterne i katalogprisfastsættelse, der bruges til projekttilbud og kontrakter.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4feb7638dd7b6826e575d83457ae7f74ef6793bf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593237"
---
# <a name="product-price-lists"></a>Produktprislister

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

 I Project Operations understøtter **Produktprislister** og relaterede prislisteelementobjekter funktionaliteten for prisfastsættelse af produkter i produktbaserede tilbuds- og kontraktlinjer. For produkter, der bruges på projekter, anvendes prislisteelementposterne for projektprislister. 

Produkterne skal konfigureres, så de har standardomkostnings- og prislister i produktkataloget. Anvend listeprisen, standardomkostningerne og de aktuelle omkostninger til at konfigurere standardomkostninger og listepriser. Standardlistepriserne bruges kun i en tilbudslinje eller en projektkontraktlinje, hvis systemet ikke kan finde en prislistelinje for det pågældende produkt på produktprislisten for tilbuddet eller projektkontrakten.

Kostprisen for produktkataloglinjer kan ændres mellem tilbud. Denne funktion er vigtig, for hvis du ikke præcist kan spore omkostninger, kan du ikke beregne driftsoverskuddet for projektaftaler. Som standard bruges produktets standardomkostning som kostprisen. Standardkostprisen kan dog opdateres i tilbudslinjen, hvis der findes en anden kostpris for det pågældende tilbud.

## <a name="price-list-items"></a>Prislisteelementer

Du kan føje produkter fra et produktkatalog til forskellige prislister. Prislistelinjer for produkter refererer altid til en bestemt enhed. Du kan konfigurere prislisteelementer for et produkt som et valutabeløb. Alternativt kan den konfigureres som en funktion af listepris, aktuelle omkostninger eller standardomkostninger.

Funktionen prisfastsættelse understøtter forskellige afrundingsindstillinger, når produktpriser er konfigureret som en funktion af listeprisen, standardomkostninger eller aktuelle omkostninger. Ud over at udnytte flere prisfastsættelsesmetoder og afrundingsindstillinger kan du knytte rabatlister til prislisteelementer. 

 
## <a name="default-product-price-list"></a>Standardproduktprisliste
Hver kundepost indeholder feltet **Standardprisliste**, hvor du kan angive en prisliste, der stemmer overens med den valuta, der er angivet for kunden. Der angives ikke automatisk en standardværdi i dette felt. Når der findes en brugerdefineret prisaftale med en bestemt kunde, kan du bruge dette felt til at knytte en prisliste til den pågældende kunde.

For objekterne for salgsmulighed, tilbud og projektkontrakt bruges følgende rækkefølge til at angive standardproduktprislister. Den samme rækkefølge bruges til projektprislister.

1.  Tilbud
2.  Salgsmulighed
3.  Kunde
4.  Globale indstillinger 

Som standard viser feltet **Produkt** på tilbudslinjen en liste over alle de aktive produkter i tilbuddets produktprisliste. Hvis et produkt er blevet deaktiveret, eller hvis det er et kladdeprodukt, vises det ikke på listen, heller ikke selvom det er på prislisten. 

Produktkataloglinjer tilføjes som fakturalinjer i den første faktura, der oprettes for en projektkontrakt. På en kladdefaktura kan de pågældende fakturalinjer slettes. Hvis det er tilfældet, vil linjerne blive vist på en efterfølgende faktura, indtil de faktureres, eller indtil fakturaen er sendt til kunden. Du kan ikke fakturere et delvist antal på en produktfakturalinje. Når produktlinjerne fra projektkontrakten faktureres, oprettes der faktiske oplysninger. Disse faktiske tal er dog ikke kædet sammen med det relaterede projektobjekt. Det vil sige, at produktbaserede projektkontraktlinjer er uafhængige af projektbaseret brug. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
