---
title: Fastsæt salgspriser for estimater og faktiske tal - lille
description: Dette emne indeholder oplysninger om fastsættelse af salgspriser for estimater og faktiske oplysninger.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25620704570fa702e1e5e09c83005be50f98f20a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274496"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Fastsæt salgspriser for estimater og faktiske tal - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Når salgspriserne på estimater og faktiske værdier afsluttes i Dynamics 365 Project Operations, bruger systemet først datoen og valutaen for det relaterede projekttilbud eller den relaterede kontrakt til at afslutte salgsprislisten. Når salgsprislisten er blevet fastsat, fastsætter systemet salgs- eller faktureringssatsen.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Fastsættelse af salgssatser for faktiske og estimerede linjer for tid

I Project Operations bruges estimatlinjer for tid til at angive tilbudslinjen og kontraktlinjedetaljerne for tid- og ressourcetildelinger på projektet.

Når en prisliste for salg er blevet fastsat, fuldfører systemet følgende trin for at angive standarden for faktureringssatsen.

1. Systemet bruger felterne **Rolle** og **Ressourceenhed** på estimatlinjen for tid for at matche dem med rollens prislinjer i den fastsatte prisliste. Denne afstemning antager, at standardprisfastsættelsesdimensionerne for faktureringssatser anvendes. Hvis du har konfigureret prisfastsættelse på grundlag af andre felter i stedet for eller som supplement til **Rolle** og **Ressourceenhed**, bruges denne kombination til at hente en tilsvarende rolleprislinje.
2. Hvis systemet finder en rolleprislinje, der har en faktureringssats for feltkombinationen **Rolle** og **Ressourceenhed**, vil den pågældende faktureringssats være angivet som standard.
3. Hvis systemet ikke kan matche feltværdierne for **Rolle** og **Ressourceenhed**, hentes det rolleprislinjer med en tilsvarende rolle, men der vises ikke null-værdier for **Ressourceenhed**. Når systemet finder en tilsvarende rolleprispost, anvendes faktureringssatsen fra den pågældende post som standard. I denne matchende antages det, at der anvendes en standardkonfiguration for den relative prioritet for **Rolle** i forhold til **Ressourceenhed** som en prisfastsættelsesdimension for salg.

> [!NOTE]
> Hvis du konfigurerede en anden prioritering af **Rolle** og **Ressourceenhed**, eller hvis du har andre dimensioner med en højere prioritet, ændres denne funktionsmåde tilsvarende. Systemet henter rolleprisposterne med værdier, der svarer til hver af prisfastsættelsesdimensionsværdierne i prioriteret rækkefølge med rækker, der har null-værdier for de pågældende dimensioner, der kommer sidst.

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
    | &nbsp; | Avance i forhold til omkostning | Anvend en avance, der er defineret af kategoriprislinjen i enhedsomkostningssatsen for den relaterede faktiske omkostning |

4. Hvis det ikke er muligt for systemet at matche feltværdierne **Kategori** og **Enhed**, vil salgssatsen som standard være nul (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]