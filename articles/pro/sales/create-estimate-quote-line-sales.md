---
title: Estimering af en projektbaseret tilbudslinje
description: Dette emne indeholder oplysninger om, hvordan du opretter et estimat på en projektbaseret tilbudslinje.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966759"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimering af en projektbaseret tilbudslinje

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

En projektbaseret tilbudslinje indeholder oplysninger, der kan hjælpe dig med at vurdere omkostningerne og den potentielle omsætning for det arbejde, der er involveret i at levere tilbudslinjen.

Hvis du vil estimere en projektbaseret tilbudslinje på den projektbaserede tilbudslinje, skal du vælge fanen **Tilbudslinjedetaljer**. Du kan oprette et estimat på en projektbaseret tilbudslinje på to måder:

- Manuel oprettelse af estimatet direkte på tilbudslinjen ved hjælp af oplysninger om tilbudslinje 
- Oprettelse af et projekt og en projektplan og efterfølgende tilknytning af projektet og opgaverne i projektet til tilbudslinjen. Den proces, der skal bruges til at importere estimaterne på projektplanen til tilbudslinjen på baggrund af de oplysninger, som du har angivet, aktiveres.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Opret estimater direkte på en projektbaseret tilbudslinje

Hvis du vil oprette et estimat på en projektbaseret tilbudslinje, skal du vælge fanen **Tilbudslinjedetaljer**. Det linjeelement, du opretter under denne fane, opsummerer den citerede værdi for tilbudslinjen. 

Hvis du vil oprette detaljer om tilbudslinjer, skal du vælge **+ Ny tilbudslinjedetalje** i undergitteret **Tilbudslinjedetaljer**. En hurtig oprettelsesskyder åbnes. Følgende felter i formularen **Tilbudslinje**:

| **Felt** | **Placering** | **Relevans, formål og vejledning** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Beskrivelse | Hurtig oprettelse | En beskrivelse af det specifikke estimat. | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Transaktionsklasse | Hurtig oprettelse | Denne rulleliste indeholder de transaktionsklasser, der findes under fanen **Generelt** for den projektbaserede tilbudslinje.  | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Rolle | Hurtig oprettelse | Den person, der udfører dette arbejde eller afholder denne udgift. | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Kategori | Hurtig oprettelse | Kategorien for arbejdet eller udgiften. | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Startdato | Hurtig oprettelse | Arbejdets startdato. | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Slutdato | Hurtig oprettelse | Arbejdets slutdato. | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Ressourceenhed | Hurtig oprettelse | Ressourceenhed, der afholder denne omkostning og giver ressourcen mulighed for at arbejde med den. | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. Dette felt bruges også til indhentelse af kostpris. |
| Enhedsplan | Hurtig oprettelse | Enhedsgruppe for arbejdet eller udgiften. Enheder tilhører en enhedsplan eller en gruppe af enheder. Kilometer og km.'er er f.eks. enheder, der tilhører en gruppe af enheder, som beskriver distancen. | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Enhed | Hurtig oprettelse | Enhed for arbejdet eller udgiften. | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Antal | Hurtig oprettelse | Mængden af arbejdet eller udgiften | Dette felt er som standard angivet til den relaterede tilbudslinje for omkostninger, der oprettes automatisk. |
| Enhedspris | Hurtig oprettelse | Faktureringshyppighed for den rolle, der udfører arbejdet eller salgsprisen for udgiftskategorien. Feltet bruges som standard for Tid baseret på kombinationen af rolle og ressourceenhed på den projektprisliste, der er gældende for startdatoen. I forbindelse med udgifter er dette felt som standard angivet til prisopsætningen for transaktionskategorien i den projektprisliste, der er gældende i forhold til startdatoen. Hvis prisfastsættelsesmetoden for transaktionskategorien ikke er en pris pr. enhed, er der ikke angivet nogen standardværdi, og dette felt er tomt. | Omkostningssats for den rolle, der udfører arbejdet eller omkostning pr. enhed for udgiftskategorien. Feltet bruges som standard for Tid baseret på kombinationen af rolle og ressourceenhed på prisen for kontraktenheden i den tilbudsprisliste, der er gældende for startdatoen. I forbindelse med udgifter er dette felt som standard angivet til prisopsætningen for transaktionskategorien i omkostningsprislisten for kontraktenheden, der er gældende i forhold til startdatoen. Hvis prisfastsættelsesmetoden for transaktionskategorien ikke er en pris pr. enhed, er der ikke angivet nogen standardværdi, og dette felt er tomt. |
| Anslået moms | Hurtig oprettelse | Du kan angive den anslåede moms manuelt for dette arbejde eller denne udgift. | Dette felt har ingen downstream-virkning. |
| Beløb | Hurtig oprettelse | Du kan angive oplysninger manuelt i dette felt, hvis felterne **Antal** og **Pris** ikke er udfyldt. Hvis disse felter ikke er tomme, bliver dette felt skrivebeskyttet og beregnet som (antal \* enhedspris) + moms. | Dette felt har ingen downstream-virkning. |

## <a name="update-prices-on-quote-line-details"></a>Opdater priser på tilbudslinjedetaljer

Hvis du har ændret priserne på den projektprisliste, der er knyttet til tilbuddet, eller på omkostningsprislisten for ordren, kan du vælge **Genberegn** på siden **Tilbud** for at opdatere priserne på de enkelte tilbudslinjedetaljer, så de afspejler denne ændring. Når du vælger **Genberegn**, vises der en advarsel, der oplyser om, at priser på tilbudslinjedetaljer for alle tilbudslinjer i tilbuddet bliver nulstillet. Vælg **Ja**, hvis du vil opdatere priser for både salgs- og omkostningstilbudslinjedetaljer.

## <a name="access-quote-line-details-for-cost"></a>Få adgang til tilbudslinjedetaljer for omkostninger

På fanen **Tilbudslinjedetaljer** skal du vælge en række i gitteret for at aktivere nogle handlinger på værktøjslinjen i undergitteret. Den første handling på undergitters værktøjslinje, når en tilbudslinjedetalje er valgt, er **Åbne omkostningsdetaljer**. Vælg **Åbne omkostningsdetaljer** for at se den relaterede omkostningssats og det tilknyttede beløb for denne tilbudslinje.

> [!NOTE]
> Hvis du ændrer værdierne for ressourceenhed, antal, datoer, rolle eller kategori på tilbudslinjedetaljerne for omkostningen, ændres de tilsvarende værdier i tilbudslinjedetaljerne for salg.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta i tilbudslinjedetaljer for omkostninger og salg

Valuta i tilbudslinjedetaljer for salg er som standard hentet fra den projektprisliste, der er gældende for startdatoen for tilbudslinjedetaljerne.

Valuta i tilbudslinjedetaljer for omkostninger er som standard hentet fra den prisliste i den kontraktenhed i tilbuddet, der er gældende for startdatoen for tilbudslinjedetaljerne for omkostninger.

Rentabilitetsberegninger konverterer beløb i tilbudslinjedetaljer for omkostninger og salg til grundvalutaen for omkostninger og salg for miljøet for at rapportere den samlede anslåede margen for tilbuddet.

Dette kan resultere i fejl i valutaafrunding og ændrede margener på grund af manglende valutakurser, der er gældende på datoen. Du skal kun bruge disse beregninger på projekttilbud som tilnærmelsesvise og ikke faktiske, velegnede eller anden rapportering, der kræver større præcision i forbindelse med afrunding og bevidsthed om valutakurser, der er gældende på datoen.
