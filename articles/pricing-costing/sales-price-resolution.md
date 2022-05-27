---
title: Fastsæt salgspriser for estimater og faktiske oplysninger
description: Dette emne indeholder oplysninger om, hvordan du fastsætter salgssatser estimater og faktiske oplysninger.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 697d5e330fec1874e8cb59fb86dd688637860346
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578241"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Fastsæt salgspriser for estimater og faktiske oplysninger

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når salgspriserne på estimater og faktiske værdier afsluttes i Dynamics 365 Project Operations, bruger systemet først datoen og valutaen for det relaterede projekttilbud eller den relaterede kontrakt til at afslutte salgsprislisten. Når salgsprislisten er blevet fastsat, fastsætter systemet salgs- eller faktureringssatsen.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Fastsættelse af salgssatser for faktiske og estimerede linjer for tid

I Project Operations bruges estimatlinjer for tid til at angive tilbudslinjen og kontraktlinjedetaljerne for tid- og ressourcetildelinger på projektet.

Når en prisliste for salg er blevet fastsat, fuldfører systemet følgende trin for at angive standarden for faktureringssatsen.

1. Systemet bruger felterne **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed** på estimatlinjen for tid for at matche dem med rollens prislinjer i den fastsatte prisliste. Denne afstemning antager, at standardprisfastsættelsesdimensionerne for faktureringssatser anvendes. Hvis du har konfigureret prisfastsættelse på grundlag af andre felter i stedet for eller som supplement til **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, bruges denne kombination til at hente en tilsvarende rolleprislinje.
2. Hvis systemet finder en rolleprislinje, der har en faktureringssats for feltkombinationen **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, vil den pågældende faktureringssats være angivet som standard.
3. Hvis systemet ikke kan matche feltværdierne for **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, hentes det rolleprislinjer med en tilsvarende rolle, men der vises ikke null-værdier for **Ressourceenheden**. Når systemet finder en tilsvarende rolleprispost, anvendes faktureringssatsen fra den pågældende post som standard. I denne matchende antages det, at der anvendes en standardkonfiguration for den relative prioritet for **Rolle** i forhold til **Ressourceenhed** som en prisfastsættelsesdimension for salg.

> [!NOTE]
> Hvis du har konfigureret en anden prioritering af **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, eller hvis du har andre dimensioner med en højere prioritet, ændres denne funktionsmåde tilsvarende. Systemet henter rolleprisposterne med værdier, der svarer til hver af prisfastsættelsesdimensionsværdierne i prioriteret rækkefølge med rækker, der har null-værdier for de pågældende dimensioner, der kommer sidst.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsættelse af salgssatser for faktiske og estimerede linjer for udgifter

I Project Operations bruges estimatlinjer for udgifter til at angive tilbudslinjen og kontraktlinjedetaljerne for udgifter og udgiftsestimatlinjerne på projektet.

Når en prisliste for salg er blevet fastsat, fuldfører systemet følgende trin for at angive standarden for enhedens salgspris.

1. Systemet bruger feltkombinationen **Kategori** og **Enhed** på estimatlinjen for en udgift for at matche dem med linjerne med kategoripris i den fastsatte prisliste.
2. Hvis systemet finder en kategoriprislinje, der har en salgssats for feltkombinationen **Kategori** og **Enhed**, angives den pågældende salgssats som standard.
3. Hvis systemet finder en tilsvarende kategoriprislinje, kan prissætningsmetoden bruges som standardsalgspris. I nedenstående tabel vises funktionaliteten for angivelse af standardprisen for udgifter i Project Operations.

    | Sammenhæng | Prissætningsmetode | Pris som standard |
    | --- | --- | --- |
    | Estimat | Pris pr. enhed | Baseret på kategoriprislinjen |
    | &nbsp; | Til kostpris | 0.00 |
    | &nbsp; | Avance i forhold til omkostning | 0.00 |
    | Faktisk | Pris pr. enhed | Baseret på kategoriprislinjen |
    | &nbsp; | Til kostpris | Baseret på de relaterede faktiske omkostninger |
    | &nbsp; | Avance i forhold til omkostning | Ved at anvende en avance, der er defineret af kategoriprislinjen i enhedsomkostningssatsen for den relaterede faktiske omkostning |

4. Hvis det ikke er muligt for systemet at matche feltværdierne **Kategori** og **Enhed**, vil salgssatsen som standard være nul (0).

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Fastsæt salgspriser på faktiske og estimerede linjer for materialer

I Project Operations bruges estimatlinjer for materialer til at angive tilbudslinje- og kontraktlinjedetaljerne for materiale og materialeestimatlinjer på projektet.

Når en prisliste for salg er blevet fastsat, fuldfører systemet følgende trin for at angive standarden for enhedens salgspris.

1. Systemet bruger kombinationsfeltet **Produkt** og **Enhed** på estimatlinjen for materialer til at matche med prislisteelementlinjerne på den prisliste, der blev fastsat.
2. Hvis systemet finder en prislisteelementlinje, der har en salgspris for feltkombinationen **Produkt** og **Enhed**, og prissætningsmetoden er **Valutabeløb**, bruges den salgspris, der er angivet på prislistelinjen.
3. Hvis feltværdierne for **Produkt** og **Enhed** ikke stemmer overens, angives salgssatsen som standard til nul.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
