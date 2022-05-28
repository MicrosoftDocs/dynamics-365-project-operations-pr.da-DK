---
title: Estimer en projektbaseret kontraktlinje - lille
description: Dette emne indeholder oplysninger om estimering af en projektbaseret kontraktlinje.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 179994a2515686bce2370964121cbdca08a9d085
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597331"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Estimer en projektbaseret kontraktlinje - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dynamics 365 Project Operations indeholder en projektbaseret kontraktlinje med oplysninger, der kan hjælpe dig med at estimere omkostningerne og den potentielle omsætning for det arbejde, der indgår i at levere kontraktlinjen.

Hvis du vil estimere en projektbaseret kontraktlinje, skal du gå til fanen **Kontraktlinjedetaljer** på den projektbaserede **Kontraktlinje**.  Du kan oprette et estimat på en projektbaseret kontraktlinje på to måder:

   - Opret et estimat direkte på kontraktlinjen ved manuelt at tilføje oplysninger om kontraktlinjer.
   - Opret et projekt og en projektplan, og knyt derefter projektet og opgaverne til projektets kontraktlinje. Dette aktiverer den proces, som du kan bruge til at importere projektplanestimatet til kontraktlinjen på baggrund af de komponenter, der findes på kontraktlinjen.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Opret et estimat direkte på en projektbaseret kontraktlinje

Hvis du vil oprette et estimat direkte på en projektbaseret kontraktlinje, skal du følge disse trin:

1. Gå til kontraktlinjen, og vælg fanen **Kontraktlinjedetaljer**. De linjer, du opretter under denne fane, opsummeres og vises som **Kontraktens værdi** for denne **Kontraktlinje**. 
2. I undergitteret **Kontraktlinjedetaljer** skal du vælge **Ny kontraktlinjedetalje**. Der åbnes en skyder til hurtig oprettelse. Følgende felter er tilgængelige på siden **Kontraktlinjedetaljer**.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| **Beskrivelse** | **Hurtig oprettelse** | En beskrivelse af det specifikke estimat. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Transaktionsklasse** | **Hurtig oprettelse** | Dette er en liste over transaktionsklasser, der er inkluderet på fanen **Generelt** på den projektbaserede kontraktlinje. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Vælg produkt** | **Hurtig oprettelse** | Anvendes, når transaktionsklassen er **Materiale**. Du kan angive, hvorvidt denne estimatlinje er for et **Eksisterende** (katalog)produkt eller et produkt, der skal **Rekvireres**. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Produkt** | **Hurtig oprettelse** | Id'et for produktet fra produktkataloget. Dette felt er kun aktivt, når du vælger **Eksisterende produkt** i feltet **Vælg produkt**. Id'et bruges til at hente salgsprisen fra projektprislisten i kontrakten. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for de omkostninger, der oprettes automatisk. |
| **Produkt, der skal rekvireres** | **Hurtig oprettelse** | Et tekstfelt, hvori produktnavnet skal angives. Dette felt er kun aktivt, når du vælger **Rekvireres** i feltet **Vælg produkt**.| Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Rolle** | **Hurtig oprettelse** | Rollen for den person, der udfører dette arbejde, eller som afholder denne udgift. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk.|
| **Kategori** | **Hurtig oprettelse** | Kategorien for arbejdet eller udgiften. |Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk.|
| **Startdato** | **Hurtig oprettelse** | Arbejdets startdato. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Slutdato** | **Hurtig oprettelse** | Arbejdets slutdato. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Ressourceenhed** | **Hurtig oprettelse** | Den enhed, der afholder denne omkostning og leverer ressourcen, som skal arbejde på den. |Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk og bruges i hentning af kostpriser. |
| **Enhedsplan** | **Hurtig oprettelse** | Enhedsgruppen for arbejdet, produktet eller udgiften. Enheder tilhører en enhedsplan eller en gruppe af enheder. Enhederne *Mil* og *Kilometer (km)* er f.eks. enheder, der tilhører en gruppe af enheder, som beskriver afstand. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Enhed** | **Hurtig oprettelse** | Enheden for arbejde, produkter eller udgifter. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Antal** | **Hurtig oprettelse** | Mængden af arbejde, produkter eller udgifter. | Denne værdi bruges som standard til den relaterede kontraktlinjedetalje for omkostninger, der oprettes automatisk. |
| **Enhedspris** | **Hurtig oprettelse** | Fakturahyppigheden for den rolle, der udfører arbejdet, enhedsprisen på produktet, salgsprisen på produktet eller udgiftskategorien. Dette felt angiver standarden for **Klokkeslæt**, som er baseret på en kombination af værdier for prisfastsættelsesdimensioner på rolleprislinjen i den projektprisliste, der gælder for startdatoen. For **Udgifter** angives dette felt som standard på baggrund af opsætningen af prisen for transaktionskategorien i den projektprisliste, der er gældende for startdatoen. Hvis prisfastsættelsesmetoden for transaktionskategorien ikke er en **pris pr. enhed**, er der ikke angivet nogen standardværdi, og dette felt er tomt. For produkter er dette felts standard baseret på linjen for **Prislisteelementet** i projektprislisten, der gælder for startdatoen.| Omkostningssatsen for den rolle, der udfører arbejdet, eller omkostningen pr. enhed for udgiftskategorien eller enhedsomkostningen for produktet. Dette felt angiver standarden for **Klokkeslæt**, som er baseret på en kombination af værdier for prisfastsættelsesdimensioner på rolleprislinjen i den omkostningsprisliste, der er tilknyttet den kontraherende enhed, og som gælder for startdatoen. For udgifter angives dette felt som standard på baggrund af den kostprislistes kategoriprislinje, der er knyttet til den kontraherende enhed, og som er gældende for startdatoen. Hvis prisfastsættelsesmetoden for transaktionskategorien ikke er en pris pr. enhed, er der ikke angivet nogen standardværdi, og dette felt er tomt. Standarden for dette felt er for produkter baseret på linjen for **Prislisteelementet** i den omkostningsprisliste, der er tilknyttet den kontraherende enhed, og som gælder for startdatoen.|
| **Anslået moms** | **Hurtig oprettelse** | Den anslåede moms for dette arbejde eller denne udgift. | Den anslåede moms for dette arbejde eller denne udgift. |
| **Beløb** | **Hurtig oprettelse** | Du kan tilføje værdien i dette felt, hvis felterne **Mængde** og **Pris** ikke er udfyldt. Hvis **Mængde** og **Pris** er udfyldt, er feltet **Beløb** skrivebeskyttet og beregnes som **(Mængde \*Enhedspris) + moms**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Opdater priser på kontraktlinjedetaljer

Hvis du ændrer priser på den projektprisliste, der er knyttet til kontrakten eller den kontraherende enheds kostprisliste, kan du opdatere priserne på de enkelte kontraktlinjedetaljer, så ændringerne afspejles. På siden **Kontrakt** skal du vælge **Genberegn**. Der vises en advarsel for at fortælle dig, at priserne på alle kontraktlinjer på kontrakten nulstilles. Vælg **Ja** for at opdatere priser for både salgs- og omkostningskontraktlinjedetaljer.

## <a name="access-contract-line-details-for-cost"></a>Få adgang til kontraktlinjedetaljer for omkostninger

På fanen **Kontraktlinjedetaljer** skal du vælge en række i gitteret for at få vist handlinger på værktøjslinjen for undergitteret. Den første handling på værktøjslinjen for undergitteret er **Åbn omkostningsdetaljer**. Hvis du vil have vist den relaterede omkostningssats og det tilknyttede beløb for denne kontraktlinjedetalje, skal du vælge **Åbn omkostningsdetaljer**. 

> [!NOTE]
> Hvis du ændrer værdierne for ressourcevirksomhed, ressourceenhed, antal, datoer, rolle eller kategori i kontraktlinjedetaljen for **Omkostninger**, ændres de tilsvarende værdier i kontraktlinjedetaljerne for **Salg** også.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta på kontraktlinjedetaljer for omkostninger og salg

I kontraktlinjedetaljen for **Salg** angives standardvalutaen fra den projektprisliste, der er gældende for kontraktlinjedetaljens startdato.

I kontraktlinjedetaljen for **Omkostning** angives standardvalutaen fra kontraktens kontraherende enheds prisliste, der er gældende for kontraktlinjedetaljens startdato for **Omkostning**.

Rentabilitetsberegninger konverterer beløbene for kontraktlinjedetaljerne for **Omkostning** og **Salg** til miljøets grundvaluta for at rapportere de samlede faktiske og estimerede margener i kontrakten.

> [!NOTE]
> Fejl i valutaafrunding og ændrede margener kan opstå på grund af manglende angivelse af ikrafttrædelsesdatoen for en valutakurs. Du kan kun bruge disse beregninger på projektkontrakter, da disse er estimater og ikke er et egentligt krav for indberetninger eller andre indberetninger, der kræver en højere afrundingspræcision og større indsigt i valutakurser.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
