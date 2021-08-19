---
title: Estimér en projekttilbudslinje
description: Dette emne giver oplysninger om, hvordan du opretter et estimat på en projekttilbudslinje.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 84283ac055aea802fadbd6814ea65a6d3dc01d29e1e3c6290ef11f72f6a75692
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003944"
---
# <a name="estimate-a-project-quote-line"></a>Estimér en projekttilbudslinje

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

En projektbaseret tilbudslinje indeholder oplysninger, der kan hjælpe dig med at vurdere omkostningerne og den potentielle omsætning for det arbejde, der er involveret i at levere tilbudslinjen.

Hvis du vil estimere en projektbaseret tilbudslinje, skal du på tilbudslinjen vælge fanen **Tilbudslinjedetaljer**. Du kan oprette en estimatlinje på en projektbaseret tilbudslinje på to måder:

   - Manuel oprettelse af estimatet direkte på tilbudslinjen ved hjælp af oplysninger om tilbudslinje. 
   - Oprettelse af et projekt og en projektplan og efterfølgende tilknytning af projektet og opgaverne i projektet til tilbudslinjen. Den proces, der skal bruges til at importere estimaterne på projektplanen til tilbudslinjen på baggrund af de oplysninger, som du har angivet, aktiveres.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Opret estimater direkte på en projektbaseret tilbudslinje

Hvis du vil oprette estimater direkte på en projektbaseret tilbudslinje, skal du følge disse trin:

1. Hvis du vil oprette et estimat på en projektbaseret tilbudslinje, skal du vælge fanen **Tilbudslinjedetaljer**. Det linjeelement, du opretter under denne fane, opsummerer den citerede værdi for tilbudslinjen. 
2. Hvis du vil oprette tilbudslinjedetaljer, skal du vælge **Nye tilbudslinjedetalje** i undergitteret **Tilbudslinjedetaljer**. En hurtig oprettelsesskyder åbnes. Følgende felter på siden **Tilbudslinje**.

| **Felt** | **Lokation** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Beskrivelse | Hurtig oprettelse | En beskrivelse af det specifikke estimat. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Transaktionsklasse | Hurtig oprettelse | Denne rulleliste indeholder de transaktionsklasser, der findes under fanen **Generelt** for den projektbaserede tilbudslinje.  | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Vælg produkt | Hurtig oprettelse | Anvendes, når transaktionsklassen er **Materiale**. Du kan vælge at angive, at denne estimatlinje er for et **Eksisterende** (katalog)produkt eller et produkt, der skal **Rekvireres**. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Produkt | Hurtig oprettelse | Id'et for produktet fra produktkataloget. Dette felt er kun aktivt, når du vælger **Eksisterende** i feltet **Vælg produkt**. Id'et bruges til at hente salgsprisen fra projektprislisten i tilbuddet. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Produkt, der skal rekvireres | Hurtig oprettelse | Et tekstfelt, som produktnavnet skal skrives i. Dette felt er kun aktivt, når du vælger **Rekvireres** i feltet **Vælg produkt**.| Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Rolle | Hurtig oprettelse | Rollen for den person, der skal udføre dette arbejde, eller som afholder denne omkostning. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Kategori | Hurtig oprettelse | Kategorien for arbejdet eller udgiften. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Startdato | Hurtig oprettelse | Arbejdets startdato. | Dette felt bruges som standard til tilbudslinjedetaljen for omkostninger, der oprettes automatisk. |
| Slutdato | Hurtig oprettelse | Arbejdets slutdato. | Dette felt bruges som standard til tilbudslinjedetaljen for omkostninger, der oprettes automatisk. |
| Ressourcevirksomhed | Hurtig oprettelse | Den virksomhed eller juridiske enhed, der afholder denne omkostning og leverer ressourcen, som skal arbejde på den. | Værdien bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk og bruges i hentning af kostpriser. |
| Ressourceenhed | Hurtig oprettelse | Den enhed, der afholder denne omkostning og leverer ressourcen, som skal arbejde på den. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk og bruges i hentning af kostpriser. |
| Enhedsplan | Hurtig oprettelse | Enhedsgruppen for arbejdet, produktet eller udgiften. Enheder tilhører en enhedsplan eller en gruppe af enheder. F.eks. er mil og kilometer enheder, der tilhører en gruppe af enheder, som beskriver afstanden. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Enhed | Hurtig oprettelse | Enheden for arbejdet, produktet eller udgiften. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Antal | Hurtig oprettelse | Mængden af arbejde, produkter eller udgifter. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Enhedspris | Hurtig oprettelse |Fakturahyppigheden for den rolle, der udfører arbejdet, enhedsprisen på produktet, salgsprisen på produktet eller udgiftskategorien. Standarden for **Klokkeslæt** er baseret på en kombination af værdier for prisfastsættelsesdimensioner på rolleprislinjen i den projektprisliste, der gælder for startdatoen. For **Udgifter** hentes standardværdien fra priskonfigurationen for transaktionskategorien i den projektprisliste, der gælder for startdatoen. Hvis prisfastsættelsesmetoden for transaktionskategorien ikke er en pris pr. enhed, er der ikke angivet nogen standardværdi, og dette felt er tomt. For produkter er dette felts standard baseret på linjen for **Prislisteelementet** i projektprislisten, der gælder for startdatoen.| Omkostningssatsen for den rolle, der udfører arbejdet, omkostningen pr. enhed for udgiftskategorien eller enhedsomkostningen for produktet. Standarden for **Klokkeslæt** er baseret på en kombination af værdier for prisfastsættelsesdimensioner på rolleprislinjen i den omkostningsprisliste, der er tilknyttet den kontraherende enhed, og som gælder for startdatoen. Standarden for omkostninger er baseret på kategoriprislinjen i den omkostningsprisliste, der er tilknyttet den kontraherende enhed, og som gælder for startdatoen. Hvis prissætningsmetoden for transaktionskategorien ikke er pris pr. enhed, er der ingen standard, og feltet udfyldes ikke. Standarden for dette felt er for produkter baseret på linjen for **Prislisteelementet** i den omkostningsprisliste, der er tilknyttet den kontraherende enhed, og som gælder for startdatoen.|
| Anslået moms | Hurtig oprettelse | Du kan angive den anslåede moms manuelt for dette arbejde eller denne udgift. | Dette felt har ingen afledt virkning. |
| Beløb | Hurtig oprettelse | Du kan angive oplysninger manuelt i dette felt, hvis felterne **Antal** og **Pris** ikke er udfyldt. Hvis disse felter ikke er tomme, bliver dette felt skrivebeskyttet og beregnet som (antal \* enhedspris) + moms. | Dette felt har ingen afledt virkning. |

## <a name="update-prices-on-quote-line-details"></a>Opdater priser på tilbudslinjedetaljer

Hvis du har ændret priserne på den projektprisliste, der er knyttet til tilbuddet, eller på omkostningsprislisten for ordren, kan du vælge **Genberegn** på siden **Tilbud** for at opdatere priserne på de enkelte tilbudslinjedetaljer, så de afspejler denne ændring. Når du vælger **Genberegn**, vises der en advarsel om, at priser på tilbudslinjedetaljer for alle tilbudslinjer i dette tilbud nulstilles. Vælg **Ja**, hvis du vil opdatere priser for både salgs- og omkostningstilbudslinjedetaljer.

## <a name="access-quote-line-details-for-cost"></a>Få adgang til tilbudslinjedetaljer for omkostninger

Hvis du vil have adgang til tilbudslinjedetaljer for omkostninger, skal du følge disse trin:

1. På fanen **Tilbudslinjedetaljer** skal du vælge en række i gitteret for at aktivere handlinger på værktøjslinjen i undergitteret. 
2. Vælg **Åbne omkostningsdetaljer** for at se den relaterede omkostningssats og det tilknyttede beløb for denne tilbudslinje.

> [!NOTE]
> Hvis du ændrer værdierne for ressourceenhed, antal, datoer, rolle eller kategori på tilbudslinjedetaljerne for omkostningen, ændres de tilsvarende værdier i tilbudslinjedetaljerne for salg.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta i tilbudslinjedetaljer for omkostninger og salg

Valutaen i tilbudslinjedetaljerne for salgsstandarden hentes som standard fra den projektprisliste, der gælder for startdatoen for detaljerne i tilbudslinjen.

Valutaen i tilbudslinjedetaljerne for omkostninger hentes som standard fra prislisten for den kontraherende enhed i tilbuddet, der gælder for startdatoen for detaljerne i tilbudslinjen for omkostninger.

> [!NOTE]
> Rentabilitetsberegninger konverterer beløb i tilbudslinjedetaljer for omkostninger og salg til grundvalutaen for omkostninger og salg for miljøet for at rapportere den samlede anslåede margen for tilbuddet. Fejl i valutaafrunding og ændrede margener kan opstå på grund af manglende angivelse af ikrafttrædelsesdatoen for en valutakurs. Du kan kun bruge disse beregninger på projekttilbud, da disse er estimater og ikke et egentligt krav eller andre indberetninger, der kræver en højere afrundingspræcision og større indsigt i valutakurser.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
