---
title: Standardprislister
description: Denne artikel indeholder oplysninger om standardsalgs- og standardkostprislister i Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410255"
---
# <a name="default-price-lists"></a>Standardprislister

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

## <a name="sales-price-lists"></a>Salgsprislister

Alle projekttilbud og kontrakter i Dynamics 365 Project Operations indeholder en standardsalgsprisliste. 

### <a name="price-list-default-on-project-quotes"></a>Prisliste hentes som standard fra projekttilbud
Systemet udfører følgende proces for at afgøre, hvilken prisliste der skal være standard for et projekttilbud:

1. Systemet ser på de prislister, der er knyttet til firmaets projektprislister. 
1. Hvis der ikke er knyttet projektprislister til firmaposten, kigger systemet på de salgsprislister, der er knyttet til de projektparametre, der passer til med valutaen i projekttilbuddet.
1. Derefter kontrollerer systemet ikrafttrædelsesdatoen for de prislister, der stemmer overens med datointervallet for projekttilbuddet. Mere specifikt den dato, hvor tilbuddet blev oprettet.
1. Hvis der er flere prislister, som gælder på datoen for projekttilbuddet, bruges alle prislisterne som standard i projekttilbuddet.
1. Hvis der ikke er nogen prislister gældende på datoen for projekttilbuddet, er der ingen standardprojektprisliste i projekttilbuddet. Der vises en advarsel i projekttilbuddet. Meddelelsen angiver, at de faktiske og estimerede værdier på projektet ikke bliver prisfastsat, idet der ikke er nogen projektprislister tilknyttet.

### <a name="price-list-default-on-project-contracts"></a>Prisliste hentes som standard fra projektkontrakter 
Systemet udfører følgende proces for at afgøre, hvilken prisliste der skal være standard for en projektkontrakt:

1. Hvis kontrakten oprettes på baggrund af et tilbud, kopieres projektprislisterne i tilbuddet over hver for sig og knyttes til projektkontrakten.
1. Hvis kontrakten oprettes fra bunden af, ser systemet på de prislister, der er knyttet til firmaets projektprislister. Hvis der ikke er knyttet projektprislister til firmaposten, vil systemet lede efter salgsprislister, der er knyttet til de projektparametre, som stemmer overens med valutaen i projektkontrakten.
1. Derefter kontrollerer systemet ikrafttrædelsesdatoen for de prislister, der stemmer overens med datointervallet for projektkontrakten. Mere specifikt den dato, hvor kontrakten blev oprettet.
1. Hvis der er flere prislister, som gælder på datoen for kontrakten, bruges alle prislisterne som standard i kontrakten.
1. Hvis der ikke er nogen prislister gældende på datoen for kontrakten, er der ingen projektprisliste, der kan angives som standard i kontrakten. Der vises en advarsel i projektkontrakten. Meddelelsen angiver, at de faktiske og estimerede værdier på projektet ikke bliver prisfastsat, idet der ikke er nogen projektprislister tilknyttet.

## <a name="cost-price-lists"></a>Kostprislister

Kostprislister hentes ikke som standard for nogen objekter i Project Operations. Fastsættelse af den kostprisliste, der skal bruges til projektomkostninger, udføres altid på transaktionsbasis. Systemet udfører følgende proces for at afgøre, hvilken prisliste der skal bruges til projektomkostninger:

1. Systemet ser på de prislister, der er knyttet til projektets kontraherende organisationsenhed.
1. Systemet ser dernæst på ikrafttrædelsesdatoen for de prislister, der stemmer overens med datoen for den indgående estimatkontekst eller faktiske kontekst.

    - *Estimatkontekst* refererer til enhver af tre kontekster for estimeringen i Project Operations:

        - Projektestimatlinje
        - Tilbudslinjedetaljer
        - Kontraktlinjedetalje

    - *Faktisk kontekst* refererer til enhver af tre kilder til faktiske værdier i Project Operations:

       - Indtastningskladdelinjer, der oprettes manuelt, eller rettelseskladdelinjer, der oprettes i en rettelseskladde
       - Kladdelinjer, der oprettes under afsendelse af tids-, udgifts- eller materialeforbrugslogfiler
       - Fakturalinjedetalje

    Når Project Operations matcher datointervallet af den indgående kladdelinje eller fakturalinjedetaljer i den *faktiske kontekst*, bruges feltet **Transaktionsdato**.

    - Hvis der er flere prislister, som er gældende på datoen for den indgående estimatkontekst eller faktiske kontekst, vælges den senest oprettede prisliste.
    - Hvis der ikke er knyttet prislister til den kontraherende organisationsenhed for projektet, vil systemet se på de kostprislister, der er knyttet til de projektparametre, der stemmer overens med valutaen i projektet.

## <a name="enable-multi-currency-cost-price-list"></a>Aktivér brugen af kostprisliste med flere valutaer

Denne indstilling findes under **Indstillinger** \> **Parametre**. Standardværdien er **Nej**.

Når denne indstilling er aktiveret (værdien er angivet til **Ja**), fungerer systemet på følgende måde:

- Tillader, at kostprislister i enhver valuta kan tilknyttes en afdeling. En kostprisliste i valutaen EUR kan f.eks. knyttes til en afdeling i USD-valutaen. Systemet vil fortsat validere, at kostprislister, der er knyttet til en afdeling, ikke har overlappende datointerval.
- Det kontrolleres, at de kostprislister, der er knyttet til projektparametre, ikke har overlappende datointerval, heller ikke selvom de har forskellige valutaer. Denne funktionsmåde adskiller sig fra standardfunktionsmåden (når værdien er angivet til **Nej**). I standardfunktionsmåden er det kun kostprislister, der har **samme** valuta, der valideres for ikke-overlappende datointerval.
- I forbindelse med en indgående transaktionskontekst bestemmer den kun kostprislisten på basis af datointerval. Denne funktionsmåde adskiller sig fra standardfunktionsmåden, hvor systemet vælger den kostprisliste, der både matcher projektets valuta og datointerval.

På grund af disse ændringer i funktionsmåden kan Project Operations-kunder vedligeholde en global kostprisliste, der er relevant for hele virksomheden. De behøver ikke at have prislister i hver driftsvaluta. Den globale prisliste har datointerval og gør det muligt at konfigurere omkostningsrater i alle valutaer for en bestemt kombination af værdier for prissætningsdimension. Valutaen for kostprislisten bruges kun til at angive standardværdier, når der oprettes vareposter af typen **Rollepriser**, **Kategoripriser** og **Prisliste**. Den bruges ikke til at bestemme prislisten.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
