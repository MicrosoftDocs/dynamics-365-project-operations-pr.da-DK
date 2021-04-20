---
title: Estimering af en projektbaseret tilbudslinje
description: Dette emne indeholder oplysninger om, hvordan du opretter et estimat på en projektbaseret tilbudslinje.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ef30df2921df7464aa2173161898121dc8e4f440
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858196"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimering af en projektbaseret tilbudslinje

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En projektbaseret tilbudslinje indeholder oplysninger, der kan hjælpe dig med at vurdere omkostningerne og den potentielle omsætning for det arbejde, der er involveret i at levere tilbudslinjen.

Hvis du vil estimere en projektbaseret tilbudslinje på den projektbaserede tilbudslinje, skal du vælge fanen **Tilbudslinjedetaljer**. Du kan oprette et estimat på en projektbaseret tilbudslinje på to måder:

- Manuel oprettelse af estimatet direkte på tilbudslinjen ved hjælp af oplysninger om tilbudslinje. 
- Oprettelse af et projekt og en projektplan og efterfølgende tilknytning af projektet og opgaverne i projektet til tilbudslinjen. Den proces, der skal bruges til at importere estimaterne på projektplanen til tilbudslinjen på baggrund af de oplysninger, som du har angivet, aktiveres.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Opret estimater direkte på en projektbaseret tilbudslinje

Hvis du vil oprette et estimat på en projektbaseret tilbudslinje, skal du vælge fanen **Tilbudslinjedetaljer**. Det linjeelement, du opretter under denne fane, opsummerer den citerede værdi for tilbudslinjen. 

Hvis du vil oprette tilbudslinjedetaljer, skal du vælge **Nye tilbudslinjedetalje** i undergitteret **Tilbudslinjedetaljer**. En hurtig oprettelsesskyder åbnes. Følgende tabel indeholder oplysninger om felterne på siden **Tilbudslinjedetalje**, og hvordan værdierne påvirker funktionaliteten.

| **Felt** | **Lokation** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Beskrivelse | Hurtig oprettelse | En beskrivelse af det specifikke estimat. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Transaktionsklasse | Hurtig oprettelse | Denne rulleliste indeholder de transaktionsklasser, der er inkluderet under fanen **Generelt** på den projektbaserede tilbudslinje.  | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Vælg produkt | Hurtig oprettelse | Anvendes, når transaktionsklassen er **Materiale**. Du kan vælge at angive, at denne estimatlinje er for et **Eksisterende** (katalog)produkt eller et produkt, der skal **Rekvireres**. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Produkt | Hurtig oprettelse | Id'et for produktet fra produktkataloget. Dette felt er kun aktivt, hvis du vælger **Eksisterende** i feltet **Vælg produkt**. Id'et bruges til at hente salgsprisen fra projektprislisten i tilbuddet. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Produkt, der skal rekvireres | Hurtig oprettelse | En tekstboks, som produktnavnet skal skrives i. Dette felt er kun aktivt, hvis du vælger **Rekvireres** i feltet **Vælg produkt**.| Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Rolle | Hurtig oprettelse | Rollen for den person, der skal udføre dette arbejde, eller som afholder denne omkostning. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Kategori | Hurtig oprettelse | Kategorien for arbejdet eller udgiften. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Startdato | Hurtig oprettelse | Arbejdets startdato. | Dette felt bruges som standard til tilbudslinjedetaljen for omkostninger, der oprettes automatisk. |
| Slutdato | Hurtig oprettelse | Arbejdets slutdato. | Dette felt bruges som standard til tilbudslinjedetaljen for omkostninger, der oprettes automatisk. |
| Ressourceenhed | Hurtig oprettelse | Den enhed, der skal afholde denne omkostning og levere ressourcen, som skal arbejde på den. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk og bruges i hentning af kostpriserne. |
| Enhedsplan | Hurtig oprettelse | Enhedsgruppen for arbejdet, produktet eller udgiften. Enheder tilhører en enhedsplan eller en gruppe af enheder. F.eks. er mil og kilometer enheder, der tilhører en gruppe af enheder, som beskriver afstanden. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Enhed | Hurtig oprettelse | Enheden for arbejdet, produktet eller udgiften. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Antal | Hurtig oprettelse | Mængden af arbejde, produkter eller udgifter. | Denne værdi bruges som standard til den relaterede tilbudslinjedetalje for omkostninger, der oprettes automatisk. |
| Enhedspris | Hurtig oprettelse |Fakturahyppigheden for den rolle, der udfører arbejdet, enhedsprisen på produktet, salgsprisen på produktet eller udgiftskategorien. Standarden for dette felt er **Klokkeslæt**, som er baseret på en kombination af værdierne for prisfastsættelsesdimensioner på rolleprislinjen i den projektprisliste, der gælder for startdatoen. For **Udgifter** hentes standardværdien fra priskonfigurationen for transaktionskategorien i den projektprisliste, der gælder for startdatoen. Hvis prissætningsmetoden for transaktionskategorien ikke er pris pr. enhed, er der ingen standard, og feltet udfyldes ikke. For produkter er standarden baseret på linjen for **Prislisteelementet** i projektprislisten, der gælder for startdatoen.| Omkostningssatsen for den rolle, der udfører arbejdet, omkostningen pr. enhed for udgiftskategorien eller enhedsomkostningen for produktet. Standarden for dette felt er **Klokkeslæt**, som er baseret på en kombination af værdierne for prisfastsættelsesdimensioner på rolleprislinjen i den projektprisliste, der gælder for startdatoen. For **Udgifter** hentes standardværdien fra priskonfigurationen for transaktionskategorien i den projektprisliste, der gælder for startdatoen. Hvis prissætningsmetoden for transaktionskategorien ikke er pris pr. enhed, er der ingen standard, og feltet udfyldes ikke. For produkter er standarden baseret på linjen for **Prislisteelementet** i projektprislisten, der gælder for startdatoen.|
| Anslået moms | Hurtig oprettelse | Du kan angive den anslåede moms manuelt for dette arbejde eller denne udgift. | Dette felt har ingen afledt virkning. |
| Beløb | Hurtig oprettelse | Du kan angive oplysninger manuelt i dette felt, hvis felterne **Antal** og **Pris** ikke er udfyldt. Hvis disse felter ikke er tomme, bliver dette felt skrivebeskyttet og beregnet som (antal \* enhedspris) + moms. | Dette felt har ingen afledt virkning. |


## <a name="update-prices-on-quote-line-details"></a>Opdater priser på tilbudslinjedetaljer

Hvis du har ændret priserne på den projektprisliste, der er knyttet til tilbuddet, eller på omkostningsprislisten for den kontraherende enhed, kan du vælge **Genberegn** på siden **Tilbud** for at opdatere priserne på de enkelte tilbudslinjedetaljer, så de afspejler denne ændring. Når du vælger **Genberegn**, vises der en advarsel om, at priser på tilbudslinjedetaljer for alle tilbudslinjer i dette tilbud nulstilles. Vælg **Ja**, hvis du vil opdatere priser for både salgs- og omkostningstilbudslinjedetaljer.

## <a name="access-quote-line-details-for-cost"></a>Få adgang til tilbudslinjedetaljer for omkostninger

På fanen **Tilbudslinjedetaljer** skal du vælge en række i gitteret for at aktivere visse handlinger på værktøjslinjen for undergitteret. Den første handling på værktøjslinjen for undergitter, når en tilbudslinjedetalje er valgt, er **Åbn omkostningsdetalje**. Vælg **Åbne omkostningsdetaljer** for at se den relaterede omkostningssats og det tilknyttede beløb for denne tilbudslinje.

> [!NOTE]
> Hvis du ændrer værdierne for ressourceenhed, antal, datoer, rolle eller kategori på tilbudslinjedetaljerne for omkostningen, ændres de tilsvarende værdier i tilbudslinjedetaljerne for salg.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta i tilbudslinjedetaljer for omkostninger og salg

Valuta i tilbudslinjedetaljer for salg er som standard hentet fra den projektprisliste, der er gældende for startdatoen for tilbudslinjedetaljerne.

Valuta i tilbudslinjedetaljer for omkostninger er som standard hentet fra den prisliste i den kontraktenhed i tilbuddet, der er gældende for startdatoen for tilbudslinjedetaljerne for omkostninger.

Rentabilitetsberegninger konverterer beløb i tilbudslinjedetaljer for omkostninger og salg til grundvalutaen for omkostninger og salg for miljøet for at rapportere den samlede anslåede margen for tilbuddet.

> [!BEMÆRK
> > Fejl i valutaafrunding og ændrede margener kan opstå på grund af manglende angivelse af ikrafttrædelsesdatoen for en valutakurs. Du kan kun bruge disse beregninger på projektkontrakter, da disse er estimater og ikke er et egentligt krav for indberetninger eller andre indberetninger, der kræver en højere afrundingspræcision og større indsigt i valutakurser.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
