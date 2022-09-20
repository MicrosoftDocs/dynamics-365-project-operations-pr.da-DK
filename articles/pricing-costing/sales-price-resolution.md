---
title: Fastsætte salgspriser for projektbaserede estimater og faktiske værdier
description: Denne artikel indeholder oplysninger om, hvordan salgspriser til projektbaserede estimater og faktiske værdier fastlægges.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475362"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Fastsætte salgspriser for projektbaserede estimater og faktiske værdier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når salgspriserne på estimater og faktiske værdier bestemmes i Microsoft Dynamics 365 Project Operations, bruger systemet først datoen og valutaen i den indgående estimatkontekst eller faktiske kontekst til at fastlægge salgsprislisten. Specifikt i den faktiske kontekst bruges feltet **Transaktionsdato** til at bestemme, hvilken prisliste der skal anvendes. Værdien af **Transaktionsdato** for det indgående estimat eller den faktiske værdi sammenlignes med værdierne af **Faktisk startdato (tidszoneuafhængig)** og **Faktisk slutdato (tidszoneuafhængig)** på prislisten. Når salgsprislisten er blevet fastlagt, fastsætter systemet salgs- eller faktureringssatsen.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Fastsætte salgssatser for faktiske og estimerede linjer for tid

Estimatkontekst for **Tid** refererer til:

- Tilbudslinjedetaljer for **Tid**.
- Kontraktlinjedetaljer for **Tid**.
- Ressourcetildelinger på et projekt.

Faktisk kontekst for **Tid** refererer til:

- Indtastnings- og rettelseskladdelinjer for **Tid**.
- Kladdelinjer, der oprettes, når der sendes en tidspost.
- Fakturalinjedetaljer for **Tid**. 

Når en prisliste for salg er fastsat, fuldfører systemet følgende trin for at angive standarden for faktureringssatsen.

1. Systemet matcher kombinationen af felterne **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed** i estimatet eller den faktiske kontekst for **Tid** med rolleprislinjerne på prislisten. Denne afstemning antager, at standardprisfastsættelsesdimensionerne for faktureringssatser anvendes. Hvis du har konfigureret prisfastsættelse på grundlag af andre felter end eller som supplement til **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, bruges denne kombination af felter til at hente en tilsvarende rolleprislinje.
1. Hvis systemet finder en rolleprislinje, der har en faktureringssats for feltkombinationen **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, vil den pågældende faktureringssats blive brugt som standard.

> [!NOTE]
> Hvis du konfigurerer en anden prioritering af **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, eller hvis du har andre dimensioner med en højere prioritet, ændres ovenstående funktionsmåde tilsvarende. I systemet hentes rolleprisposter, der har værdier, som svarer til de enkelte prissætningsdimensionsværdier i prioritetsrækkefølge. Rækker med null-værdier for disse dimensioner kommer sidst.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsætte salgssatser for faktiske og estimerede linjer for udgifter

Estimatkontekst for **Udgift** refererer til:

- Tilbudslinjedetaljer for **Udgift**.
- Kontraktlinjedetaljer for **Udgift**.
- Udgiftsestimatlinjer på et projekt.

Faktisk kontekst for **Udgift** refererer til:

- Indtastnings- og rettelseskladdelinjer for **Udgift**.
- Kladdelinjer, der oprettes, når der sendes en udgiftspost.
- Fakturalinjedetaljer for **Udgift**. 

Når en prisliste for salg er fastsat, fuldfører systemet følgende trin for at angive standarden for enhedens salgspris.

1. Systemet bruger feltkombinationen **Kategori** og **Enhed** på estimatlinjen for **Udgift** for at matche dem med linjerne med kategoripris på prislisten.
1. Hvis systemet finder en kategoriprislinje, der har en salgssats for feltkombinationen **Kategori** og **Enhed**, bruges den pågældende salgssats som standard.
1. Hvis systemet finder en tilsvarende kategoriprislinje, kan prissætningsmetoden bruges til at angive standardsalgsprisen. I nedenstående tabel vises standardfunktionaliteten af udgiftspriser i Project Operations.

    | Sammenhæng | Prissætningsmetode | Standardpris |
    | --- | --- | --- |
    | Estimat | Pris pr. enhed | Baseret på kategoriprislinjen. |
    |        | Til kostpris | 0.00 |
    |        | Avance i forhold til omkostning | 0.00 |
    | Faktisk | Pris pr. enhed | Baseret på kategoriprislinjen. |
    |        | Til kostpris | Baseret på de relaterede faktiske omkostninger. |
    |        | Avance i forhold til omkostning | Anvender en avance, der er defineret af kategoriprislinjen, i enhedsomkostningssatsen for den relaterede faktiske omkostning. |

1. Hvis systemet ikke kan matche værdierne af **Kategori** og **Enhed**, angives salgssatsen som standard til **0** (nul).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Fastsætte salgspriser på faktiske og anslåede linjer for materialer

Estimatkontekst for **Materiale** refererer til:

- Tilbudslinjedetaljer for **Materiale**.
- Kontraktlinjedetaljer for **Materiale**.
- Materialeestimatlinjer på et projekt.

Faktisk kontekst for **Materiale** refererer til:

- Indtastnings- og rettelseskladdelinjer for **Materiale**.
- Kladdelinjer, der oprettes, når der sendes en materialeforbrugslog.
- Fakturalinjedetaljer for **Materiale**. 

Når en prisliste for salg er fastsat, fuldfører systemet følgende trin for at angive standarden for enhedens salgspris.

1. Systemet bruger kombinationen af felterne **Produkt** og **Enhed** på estimatlinjen for **Materiale** til at matche med prislisteelementlinjerne på prislisten.
1. Hvis systemet finder en prislisteelementlinje, der har en salgspris for feltkombinationen **Produkt** og **Enhed**, og prissætningsmetoden er **Valutabeløb**, bruges den salgspris, der er angivet på prislistelinjen. 
1. Hvis værdierne i feltet **Produkt** og **Enhed** ikke stemmer overens, eller hvis prissætningsmetoden er noget andet end **Valutabeløb**, angives salgssatsen som standard til **0** (nul). Dette forekommer, fordi Project Operations kun understøtter prissætningsmetoden **Valutabeløb** for materiale, der bruges på et projekt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
