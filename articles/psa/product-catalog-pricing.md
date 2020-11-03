---
title: Prisfastsættelse i produktkatalog.
description: Dette emne indeholder oplysninger om, hvordan prisfastsættelse i produktkataloget Dynamics 365 Project Service Automation fungerer i (PSA).
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: e6d9266cfee996b68608c99f77d1b0c053985b3d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074203"
---
# <a name="product-catalog-pricing"></a>Prisfastsættelse i produktkatalog. 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Prislister og objekter for prislisteelementer understøtter prisfastsættelse i produktkataloget. I de fleste tilfælde bruges denne funktion i forbindelse med katalogbaserede linjer i projekttilbud og projektkontrakter.

I forbindelse med projektbaserede linjer repræsenterer en kontrakt handlen, efter at den blev vundet. Da forhandlingsprocessen sædvanligvis ligger før den vundne handel, kopieres den prisfastsættelse, der er knyttet til tilbuddet, altid som den er til en ny prisliste og knyttes til kontrakten. Denne nye prisliste kan ikke ændres uden for kontraktens omfang. Denne begrænsning er med til at beskytte den satstabel, der er blevet forhandlet om, mod eventuelle prisændringer, der opstår på den overordnede prisliste.

Produkterne skal konfigureres, så de har standardomkostnings- og prislister i produktkataloget. Du skal bruge listeprisen, standardomkostningerne og de aktuelle omkostninger til at konfigurere standardomkostninger og listepriser. Standardlistepriserne bruges kun i en tilbudslinje eller en projektkontraktlinje, hvis systemet ikke kan finde en prislistelinje for det pågældende produkt på produktprislisten for tilbuddet eller projektkontrakten.

Kostprisen for produktkataloglinjer kan ændres mellem tilbud. Denne funktion er vigtig, for hvis du ikke præcist kan spore omkostninger, kan du ikke beregne driftsoverskuddet for projektaftaler. Som standard bruges produktets standardomkostning som kostprisen. Standardkostprisen kan dog opdateres i tilbudslinjen, hvis der findes en anden kostpris for det pågældende tilbud.

## <a name="price-list-items"></a>Prislisteelementer

Du kan føje produkter fra et produktkatalog til forskellige prislister. Prislistelinjer for produkter refererer altid til en bestemt enhed. Du kan konfigurere prislisteelementer for et produkt som et valutabeløb. Alternativt kan den konfigureres som en funktion af listepris, aktuelle omkostninger eller standardomkostninger.

PSA understøtter forskellige afrundingsindstillinger, når priser er konfigureret som en funktion af listeprisen, standardomkostninger eller aktuelle omkostninger. Ud over at udnytte flere prisfastsættelsesmetoder og afrundingsindstillinger kan du knytte rabatlister til prislisteelementer. 

> ![Tilføjelse af produkter fra et katalog til forskellige prislister](media/basic-guide-16.png)

Når du opretter en ny brugerdefineret prisliste for et tilbud ved at vælge **Opret brugerdefineret prissætning** på siden **Projekttilbud** , opretter PSA en kopi af prislisten, og feltet **Objekt** i overskriften for den nye prisliste angives til **Salgsobjekt**. Navnet på den nye prisliste tilføjes sammen med navnet på tilbuddet og et tidsstempel. Du kan også bruge navnet på den nye prisliste og navnet på tilbuddet i brugerdefinerede arbejdsprocesser til at udløse yderligere gennemgang og godkendelse for tilbud, der bruger brugerdefineret prissætning.

 
## <a name="default-product-price-list"></a>Standardproduktprisliste
Hver kundepost indeholder feltet **Standardprisliste** , hvor du kan angive en prisliste, der stemmer overens med den valuta, der er angivet for kunden. I PSA angives der ikke automatisk en standardværdi i dette felt. Når der findes en brugerdefineret prisaftale med en bestemt kunde, kan du bruge dette felt til at knytte en prisliste til den pågældende kunde.

For objekterne for salgsmulighed, tilbud og projektkontrakt bruges følgende rækkefølge til at angive standardproduktprislister. Den samme rækkefølge bruges til projektprislister.

1.  Tilbud
2.  Salgsmulighed
3.  Kunde
4.  Globale indstillinger for PSA

Som standard viser feltet **Produkt** på tilbudslinjen en liste over alle de aktive produkter i tilbuddets produktprisliste. Hvis et produkt er blevet deaktiveret, eller hvis det er et kladdeprodukt, vises det ikke på listen, heller ikke selvom det er på prislisten. 

Produktkataloglinjer tilføjes som fakturalinjer i den første faktura, der oprettes for en projektkontrakt. På en kladdefaktura kan de pågældende fakturalinjer slettes. Hvis det er tilfældet, vil linjerne blive vist på en efterfølgende faktura, indtil de faktureres, eller indtil fakturaen er sendt til kunden. I PSA kan du ikke fakturere et delvist antal på en produktfakturalinje. Når produktlinjerne fra projektkontrakten faktureres, oprettes der faktiske oplysninger. Disse faktiske tal er dog ikke kædet sammen med det relaterede projektobjekt. Det vil sige, at produktbaserede projektkontraktlinjer er uafhængige af projektbaseret brug. PSA sporer ikke materialeforbrug på projekter.
