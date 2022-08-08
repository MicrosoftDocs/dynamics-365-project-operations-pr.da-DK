---
title: Standardprislister
description: Denne artikel indeholder oplysninger om standardsalgs- og standardkostprislister i Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 99af12577abeb0b77dc5d8a117d1e3b292bf0b80
ms.sourcegitcommit: 260368e1d0751db713da073a641c63c04876fcdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2022
ms.locfileid: "9036404"
---
# <a name="default-price-lists"></a>Standardprislister

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

## <a name="sales-price-lists"></a>Salgsprislister

Alle projekttilbud og kontrakter i Dynamics 365 Project Operations indeholder en standardsalgsprisliste. 

### <a name="price-list-default-on-project-quotes"></a>Prisliste hentes som standard fra projekttilbud
Systemet udfører følgende proces for at afgøre, hvilken prisliste der skal være standard for et projekttilbud:

1. Systemet ser på de prislister, der er knyttet til firmaets projektprislister. 
2. Hvis der ikke er knyttet projektprislister til firmaposten, kigger systemet på de salgsprislister, der er knyttet til de projektparametre, der passer til med valutaen i projekttilbuddet.
3. Derefter kontrollerer systemet ikrafttrædelsesdatoen for de prislister, der stemmer overens med datointervallet for projekttilbuddet. Mere specifikt den dato, hvor tilbuddet blev oprettet.
4. Hvis der er flere prislister, som gælder på datoen for projekttilbuddet, bruges alle prislisterne som standard i projekttilbuddet.
5. Hvis der ikke er nogen prislister gældende på datoen for projekttilbuddet, er der ingen standardprojektprisliste i projekttilbuddet. Der vises en advarsel i projekttilbuddet. Meddelelsen angiver, at de faktiske og estimerede værdier på projektet ikke bliver prisfastsat, idet der ikke er nogen projektprislister tilknyttet.

### <a name="price-list-default-on-project-contracts"></a>Prisliste hentes som standard fra projektkontrakter 
Systemet udfører følgende proces for at afgøre, hvilken prisliste der skal være standard for en projektkontrakt:

1. Hvis kontrakten oprettes på baggrund af et tilbud, kopieres projektprislisterne i tilbuddet over hver for sig og knyttes til projektkontrakten.
2. Hvis kontrakten oprettes fra bunden af, ser systemet på de prislister, der er knyttet til firmaets projektprislister. Hvis der ikke er knyttet projektprislister til firmaposten, vil systemet lede efter salgsprislister, der er knyttet til de projektparametre, som stemmer overens med valutaen i projektkontrakten.
4. Derefter kontrollerer systemet ikrafttrædelsesdatoen for de prislister, der stemmer overens med datointervallet for projektkontrakten. Mere specifikt den dato, hvor kontrakten blev oprettet.
5. Hvis der er flere prislister, som gælder på datoen for kontrakten, bruges alle prislisterne som standard i kontrakten.
6. Hvis der ikke er nogen prislister gældende på datoen for kontrakten, er der ingen projektprisliste, der kan angives som standard i kontrakten. Der vises en advarsel i projektkontrakten. Meddelelsen angiver, at de faktiske og estimerede værdier på projektet ikke bliver prisfastsat, idet der ikke er nogen projektprislister tilknyttet.

## <a name="cost-price-lists"></a>Kostprislister

Kostprislister hentes ikke som standard for nogen objekter i Project Operations. Fastsættelse af den kostprisliste, der skal bruges til projektomkostninger, udføres altid med det samme. Systemet udfører følgende proces for at afgøre, hvilken prisliste der skal bruges til projektomkostninger:

1. Systemet ser først på de prislister, der er knyttet til projektets kontraherende organisationsenhed.
2. Systemet ser derefter på ikrafttrædelsesdatoen for de prislister, der stemmer overens med datoen for den indgående estimatlinje eller faktiske linje. I denne situation refererer *estimatlinjen* til alle tre kontekster for estimeringen i Project Operations:

    - Projektestimatlinje
    - Tilbudslinjedetaljer
    - Kontraktlinjedetalje
  
3. Hvis der er flere prislister, som er gældende på datoen for det indgående estimat eller faktiske oplysning, vælges den senest oprettede prisliste.
4. Hvis der ikke er knyttet prislister til den kontraherende organisationsenhed for projektet, vil systemet se på de omkostningsprislister, der er knyttet til de projektparametre, der stemmer overens med valutaen i projektet.
5. Systemet ser dernæst på ikrafttrædelsesdatoen for de prislister, der stemmer overens med datoen for den indgående estimatlinje eller faktiske linje. 
6. Hvis der er flere prislister, som er gældende på datoen for det indgående estimat eller faktiske oplysning, vælges den senest oprettede prisliste.
7. Hvis der ikke er tilknyttet kostprislister til projektparametrene, som stemmer overens med valutaen og ikrafttrædelsesdatoen, anvendes som standard en omkostningssats på nul (0) på den indgående estimatlinje eller den faktiske linje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
