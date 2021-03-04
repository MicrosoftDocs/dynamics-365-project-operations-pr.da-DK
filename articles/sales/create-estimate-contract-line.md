---
title: Estimer en projektbaseret kontraktlinje
description: Dette emne indeholder oplysninger om estimater på en projektbaseret kontraktlinje.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180455"
---
# <a name="estimate-a-projectbased-contract-line"></a>Estimer en projektbaseret kontraktlinje

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_ 

I Dynamics 365 Project Operations indeholder en projektbaseret kontraktlinje oplysninger, der kan hjælpe dig med at estimere omkostningerne og den potentielle omsætning for det arbejde, der indgår i at levere kontraktlinjen.

Hvis du vil estimere en projektbaseret kontraktlinje, skal du gå til fanen **Kontraktlinjedetaljer** på den projektbaserede **Kontraktlinje**.  Du kan oprette et estimat på en projektbaseret kontraktlinje på to måder:

   - Opret et estimat direkte på kontraktlinjen ved manuelt at tilføje oplysninger om kontraktlinjer.
   - Opret et projekt og en projektplan, og knyt derefter projektet og opgaverne til projektets kontraktlinje. Dette aktiverer den proces, som du kan bruge til at importere projektplanestimatet til kontraktlinjen på baggrund af de komponenter, der findes på kontraktlinjen.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Opret et estimat direkte på en projektbaseret kontraktlinje

1. Gå til kontraktlinjen, og vælg fanen **Kontraktlinjedetaljer**. De linjer, du opretter under denne fane, opsummeres og vises som **Kontraktens værdi** for denne **Kontraktlinje**. 
2. I undergitteret **Kontraktlinjedetaljer** skal du vælge **+ Ny kontraktlinjedetalje**. Der åbnes en skyder til hurtig oprettelse. Følgende felter er tilgængelige i formularen **Kontraktlinjedetaljer**:

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| **Beskrivelse** | **Hurtig oprettelse** | En beskrivelse af det specifikke estimat. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. |
| **Transaktionsklasse** | **Hurtig oprettelse** | Denne rulleliste er en oversigt over de transaktionsklasser, der findes under fanen **Generelt** for den projektbaserede kontraktlinje. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. |
| **Rolle** | **Hurtig oprettelse** | Rollen for den person, der udfører dette arbejde, eller som afholder denne udgift. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. |
| **Kategori** | **Hurtig oprettelse** | Kategorien for arbejdet eller udgiften. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. |
| **Startdato** | **Hurtig oprettelse** | Arbejdets startdato. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. |
| **Slutdato** | **Hurtig oprettelse** | Arbejdets slutdato. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for den omkostning, som oprettes automatisk. |
| **Ressourcevirksomhed** | **Hurtig oprettelse** | Ressourcevirksomheden eller den juridiske enhed, der afholder denne omkostning, og under forudsætning af at ressourcen arbejder på den. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. Dette felt bruges også til indhentelse af kostpris. |
| **Ressourceenhed** | **Hurtig oprettelse** | Ressourceenheden, der afholder denne omkostning og leverer den ressource, som skal arbejde på den. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. Dette felt bruges også til indhentelse af kostpris. |
| **Enhedsplan** | **Hurtig oprettelse** | Enhedsgruppen for arbejdet eller udgiften. Enheder tilhører en enhedsplan eller en gruppe af enheder. Enhederne *Mil* og *Kilometer (km)* er f.eks. enheder, der tilhører en gruppe af enheder, som beskriver afstand. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. |
| **Enhed** | **Hurtig oprettelse** | Enheden for arbejde eller udgift. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. |
| **Antal** | **Hurtig oprettelse** | Mængden af arbejde eller udgift. | I dette felt vises der som standard oplysninger om den relaterede kontraktlinje for omkostninger, som oprettes automatisk. |
| **Enhedspris** | **Hurtig oprettelse** | Faktureringshyppigheden for den rolle, der udfører arbejdet, eller salgsprisen for udgiftskategorien. Feltet bruges som standard for **Tid** baseret på kombinationen af rolle og ressourceenhed på den projektprisliste, der er gældende for startdatoen. For udgifter angives dette felt som standard på baggrund af opsætningen af prisen for transaktionskategorien i den projektprisliste, der er gældende for startdatoen. Hvis prisfastsættelsesmetoden for transaktionskategorien ikke er en **pris pr. enhed**, er der ikke angivet nogen standardværdi, og dette felt er tomt. | Omkostningssatsen for den rolle, der udfører arbejdet, eller omkostningen pr. enhed for udgiftskategorien. Dette felt er som standard angivet til **Tid er baseret på rollen** og ressourceenhedskombinationen på den kostprislistes rolleprislinje, der er knyttet til den kontraherende enhed, og som er gældende for startdatoen. For udgifter angives dette felt som standard på baggrund af den kostprislistes kategoriprislinje, der er knyttet til den kontraherende enhed, og som er gældende for startdatoen. Hvis prisfastsættelsesmetoden for transaktionskategorien ikke er en pris pr. enhed, er der ikke angivet nogen standardværdi, og dette felt er tomt. |
| **Anslået moms** | **Hurtig oprettelse** | Den anslåede moms for dette arbejde eller omkostning som indtastet af brugeren. | Den anslåede moms for dette arbejde eller omkostning som indtastet af brugeren. |
| **Beløb** | **Hurtig oprettelse** | Værdien i dette felt kan tilføjes af brugeren, hvis felterne **Antal** og **Pris** ikke er udfyldte. Hvis **Antal** og **Pris** er udfyldt, er feltet **Beløb** skrivebeskyttet og beregnes som **(Antal \* Enhedspris) + moms**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Opdater priser på kontraktlinjedetaljer

Hvis du ændrer priser på den projektprisliste, der er knyttet til kontrakten eller den kontraherende enheds kostprisliste, kan du opdatere priserne på de enkelte kontraktlinjedetaljer, så ændringerne afspejles. På siden **Kontrakt** skal du vælge **Genberegn**. Der vises en advarsel, som giver dig besked om, at priser for alle kontraktlinjer i denne kontrakt nulstilles. Vælg **Ja** for at opdatere priser for både salgs- og omkostningskontraktlinjedetaljer.

## <a name="access-contract-line-details-for-cost"></a>Få adgang til kontraktlinjedetaljer for omkostninger

På fanen **Kontraktlinjedetaljer** skal du vælge en række i gitteret for at få vist handlinger på værktøjslinjen for undergitteret. Den første handling på værktøjslinjen for undergitteret er **Åbn omkostningsdetaljer**. Hvis du vil have vist den relaterede omkostningssats og det tilknyttede beløb for denne kontraktlinjedetalje, skal du vælge **Åbn omkostningsdetaljer**. 

> [!NOTE]
> Hvis du ændrer værdierne for ressourcevirksomhed, ressourceenhed, antal, datoer, rolle eller kategori i kontraktlinjedetaljen for **Omkostninger**, ændres de tilsvarende værdier i kontraktlinjedetaljerne for **Salg** også.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta på kontraktlinjedetaljer for omkostninger og salg

I kontraktlinjedetaljen for **Salg** angives standardvalutaen fra den projektprisliste, der er gældende for kontraktlinjedetaljens startdato.

I kontraktlinjedetaljen for **Omkostning** angives standardvalutaen fra kontraktens kontraherende enheds prisliste, der er gældende for kontraktlinjedetaljens startdato for **Omkostning**.

Rentabilitetsberegninger konverterer beløbene for kontraktlinjedetaljerne for **Omkostning** og **Salg** til miljøets grundvaluta for at rapportere de samlede faktiske og estimerede margener i kontrakten.

> [!NOTE]
> Fejl i valutaafrunding og ændrede margener kan opstå på grund af manglende angivelse af ikrafttrædelsesdatoen for en valutakurs. Brug kun disse beregninger på projektkontrakter som tilnærmelser og ikke for egentlig lovpligtig eller anden rapportering, der kræver større præcision i forbindelse med afrunding og forståelse af valutakursers ikrafttrædelsesdato.


[!INCLUDE[footer-include](../includes/footer-banner.md)]