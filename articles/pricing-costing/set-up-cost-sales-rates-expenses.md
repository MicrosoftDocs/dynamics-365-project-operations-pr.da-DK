---
title: Konfigurer satser for omkostninger og salg
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere satserne for omkostninger og salg for transaktions- og udgiftskategorier.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee52daae18c5f9f0b630e54359021fffe1759274
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274901"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Konfigurer satser for omkostninger og salg

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan konfigurere kost- og salgspriser for transaktionskategorier i Dynamics 365 Project Operations. Da kost- og salgspriserne er designet til udgifter, skal de enkelte transaktionskategorier, som indeholder disse, også konfigureres som en udgiftskategori. Med denne konfiguration sikres nøjagtigheden i de afledte funktioner. Kost- og salgspriser for transaktionskategorier kan kun angives i én valuta, hvilket skal være valutaen i prislistens overskriften.

Hvis du vil konfigurere satser for omkostninger og salg for transaktionskategorier, skal du benytte følgende fremgangsmåde. 

1. Opret en prisliste, der er baseret på prislistens overskrift. 
2. I menuen for undergitteret skal du på **Kategoripriser** vælge **+ Ny kategoripris**. 
3. På siden **Hurtig oprettelse** skal du angive den transaktionskategori og enhed, som du opretter den nye pris for.

I følgende tabel vises de felter på fanen **Generelt** og siden **Hurtig oprettelse**, som du skal være opmærksom på, når du opretter kategoripriser på en salgs- eller kostprisliste.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| Transaktionskategori | Fanen **Generelt** og siderne **Hurtig oprettelse** | Vælg den transaktionskategori, som du vil oprette en salgs- eller kostpris for. | Transaktionskategorien i det indgående estimat eller den faktiske udgift sammenholdes med denne linje for at angive standarden for transaktionskategoriens satser for omkostninger eller salg. |
| Enhedsplan | Fanen **Generelt** og siderne **Hurtig oprettelse** | Enhedsplanen er som standard baseret på enhedsplanen for transaktionskategorien. | Dette felt har ingen downstream-virkning. |
| Enhed | Fanen **Generelt** og siderne **Hurtig oprettelse** | Vælg den enhed, som satserne er konfigureret til. | Enheden for det indgående estimat eller faktiske oplysning sammenholdes med enheden på denne linje for at angive standarden for satsen for udgiftsestimatet eller den faktiske oplysning. |
| Prissætningsmetode | Fanen **Generelt** og siderne **Hurtig oprettelse** | Mulige værdier i **Prissætningsmetode** er **Pris pr. enhed**, **Til omkostningsværdi** og **Avance i forhold til omkostninger**. | Hvis du vælge **Pris pr. enhed** under prisopsætningen, låses feltet **Procent** på prislinjen for kategorien. Hvis **Til omkostningsværdi** er valgt, låses felterne **Pris** og **Procent** på salgsprislisten. Hvis du vælger **Avance i forhold til omkostninger**, låses feltet **Pris** på salgsprislisten. På en indgående faktisk linje til udgifter resulterer prissætningsmetoden **Til omkostningsværdi** eller **Avance i forhold til omkostning** i, at den tilsvarende ikke-fakturerede salgslinje tildeles en pris, der er lig med prisen på den faktiske omkostning eller beregnes som en avance i forhold til prisen. |
| Pris | Fanen **Generelt** og siderne **Hurtig oprettelse** | Opret en sats pr. enhed for kombinationen transaktionskategori og enhed. Satsen for kørsel er f.eks. 10 USD pr. mil og 8 USD pr. kilometer. | Kilometersatsen er den sats, der er angivet som standardværdi for pr. enhedspris eller omkostning på det indgående estimatlinje eller faktiske linje for en udgiftstransaktionsklasse.|
| Procent | Fanen **Generelt** og siderne **Hurtig oprettelse** | Konfigurer procent over omkostning for kombinationen transaktionskategori og enhed. Salgssatsen for flybilletter skal f.eks. have en avance på 10 procent over omkostningerne for den påløbne udgift til en flybillet. | Denne procent over omkostning kan kun anvendes på en salgsprisliste, når den valgte prissætningsmetode er **Avance i forhold til omkostning**. |
| Valuta | Fanen **Generelt** og siderne **Hurtig oprettelse** | Værdien hentes som standard fra valutaen i overskriften til prislisten. I forbindelse med prisfastsættelse af transaktionskategorier kan valutaen ikke tilsidesættes. | Denne valutas standard er pr. enhedspris for den indgående faktiske linje for udgiftstransaktionsklassen for omkostninger og salg. |

## <a name="pricing-methods-for-expenses"></a>Prissætningsmetoder for udgifter

Når du konfigurerer kategoripriser, der kun er relevante i forbindelse med prisfastsættelse af omkostninger, kan du bruge en af følgende tre prissætningsmetoder:

- **Pris pr. enhed**
- **Til kostpris**
- **Avance i forhold til omkostning**

### <a name="price-per-unit"></a>Pris pr. enhed
Når denne prissætningsmetode vælges på en kategoriprislinje, der er knyttet til en salgsprisliste, er standardprisen for kombinationen kategori og enhed både estimatet og den faktiske oplysning. Estimatlinjer henviser til projektestimatlinjer for udgifter, tilbudslinjedetaljerne og kontraktlinjedetaljerne for udgifter.

### <a name="at-cost"></a>Til kostpris
Når denne prissætningsmetode vælges på kategoriprislinjen, der er knyttet til en salgsprisliste, angives standardprisen for kombinationen kategori og enhed kun for den faktiske udgift. Eksempelvis ikke-fakturerede faktiske salgsoplysninger for udgiftstransaktionsklassen. Enhedsprisen er konfigureret på grundlag af de ikke-fakturerede faktiske salgsoplysninger fra enhedsprisen på de faktiske omkostningsoplysninger for udgiften. Standardangivelse af pris baseret på omkostninger udføres ikke på projektestimater for udgifter eller tilbudslinjer og kontraktlinjedetaljer for udgifter.

### <a name="markup-over-cost"></a>Avance i forhold til omkostning
Når denne prissætningsmetode vælges på kategoriprislinjen, der er knyttet til en salgsprisliste, angives standardprisen for kombinationen kategori og enhed kun for en faktisk udgift. Eksempelvis ikke-fakturerede faktiske salgsoplysninger for udgiftstransaktionsklassen. Denne enhedspris er konfigureret på grundlag af de ikke-fakturerede faktiske salgsoplysninger og angivet som en beregnet værdi fra enhedsprisen på de faktiske omkostningsoplysninger for den pågældende udgift, når den definerede avanceprocent finder anvendelse. Standardangivelse af pris baseret på omkostninger udføres ikke på projektestimater for udgifter eller tilbudslinjer og kontraktlinjedetaljer for udgifter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]