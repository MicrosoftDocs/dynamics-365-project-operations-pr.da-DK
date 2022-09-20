---
title: Fastsætte omkostningssatser for projektbaserede estimater og faktiske værdier
description: Denne artikel indeholder oplysninger om, hvordan omkostningssatser til projektbaserede estimater og faktiske værdier fastlægges.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475266"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Fastsætte omkostningssatser for projektbaserede estimater og faktiske værdier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når kostpriserne på estimater og faktiske værdier bestemmes i Microsoft Dynamics 365 Project Operations, bruger systemet først datoen og valutaen i den indgående estimatkontekst eller faktiske kontekst til at fastlægge salgsprislisten. Specifikt i den faktiske kontekst bruges feltet **Transaktionsdato** til at bestemme, hvilken prisliste der skal anvendes. Værdien af **Transaktionsdato** for det indgående estimat eller den faktiske værdi sammenlignes med værdierne af **Faktisk startdato (tidszoneuafhængig)** og **Faktisk slutdato (tidszoneuafhængig)** på prislisten. Når kostprislisten er fastsat, fastsætter systemet omkostningssatsen.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Fastsættelse af omkostningssatser i estimater og faktiske oplysninger for tid

Estimatkontekst for **Tid** refererer til:

- Tilbudslinjedetaljer for **Tid**.
- Kontraktlinjedetaljer for **Tid**.
- Ressourcetildelinger på et projekt.

Faktisk kontekst for **Tid** refererer til:

- Indtastnings- og rettelseskladdelinjer for **Tid**.
- Kladdelinjer, der oprettes, når der sendes en tidspost.

Når en kostprisliste er fastsat, fuldfører systemet følgende trin for at angive standarden for omkostningssatsen.

1. Systemet matcher kombinationen af felterne **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed** i estimatet eller den faktiske kontekst for **Tid** med rolleprislinjerne på prislisten. Denne sammenligning forudsætter, at du bruger standarddimensionerne for prisfastsættelse af lønomkostninger. Hvis du har konfigureret systemet til at matche andre felter end eller som supplement til **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, bruges der en anden kombination til at hente en tilsvarende rolleprislinje.
1. Hvis systemet finder en rolleprislinje, der har en omkostningssats for kombinationen **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, vil den være standardomkostningssatsen.
1. Hvis systemet ikke kan matche værdierne **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, droppes den dimension, der har den laveste prioritet, og der søges efter rolleprislinjer, der matcher de to andre dimensionsværdier, og dimensionerne droppes progressivt, indtil der findes en tilsvarende rolleprisrække. Omkostningssatsen fra den pågældende post bruges som standardomkostningssatsen. Hvis der ikke findes en matchende rolleprisrække, angives prisen som standard til **0** (nul).

> [!NOTE]
> Hvis du konfigurerer en anden prioritering af **Rolle** og **Ressourceenhed**, eller hvis du har andre dimensioner med en højere prioritet, ændres denne funktionsmåde tilsvarende. I systemet hentes rolleprisposter, der har værdier, som svarer til de enkelte prissætningsdimensionsværdier i prioritetsrækkefølge. Rækker med null-værdier for disse dimensioner kommer sidst.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsætte omkostningssatser for faktiske og estimerede linjer for udgifter

Estimatkontekst for **Udgift** refererer til:

- Tilbudslinjedetaljer for **Udgift**.
- Kontraktlinjedetaljer for **Udgift**.
- Udgiftsestimater på et projekt.

Faktisk kontekst for **Udgift** refererer til:

- Indtastnings- og rettelseskladdelinjer for **Udgift**.
- Kladdelinjer, der oprettes, når der sendes en udgiftspost.

Når en kostprisliste er fastsat, fuldfører systemet følgende trin for at angive standarden for omkostningssatsen.

1. Systemet matcher kombinationen af felterne **Kategori** og **Enhed** i estimatet eller den faktiske kontekst for **Udgift** med linjerne med kategoripris på prislisten.
1. Hvis systemet finder en kategorisprislinje, der har en omkostningssats for kombinationen af **Kategori** og **Enhed**, bruges denne omkostningssats som standarden.
1. Hvis systemet ikke kan matche værdierne af **Kategori** og **Enhed**, angives prisen som standard til **0** (nul).
1. Hvis systemet kan finde en matchende kategoriprislinje i estimatkonteksten, men prissætningsmetoden ikke er **Pris pr. enhed**, vil omkostningssatsen som standard være **0** (nul).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Fastsætte kostpriser på faktiske og estimerede linjer for materialer

Estimatkontekst for **Materiale** refererer til:

- Tilbudslinjedetaljer for **Materiale**.
- Kontraktlinjedetaljer for **Materiale**.
- Materialeestimater på et projekt.

Faktisk kontekst for **Materiale** refererer til:

- Indtastnings- og rettelseskladdelinjer for **Materiale**.
- Kladdelinjer, der oprettes, når der sendes en materialeforbrugslog.

Når en kostprisliste er fastsat, fuldfører systemet følgende trin for at angive standarden for omkostningssatsen.

1. Systemet matcher kombinationen af felterne **Produkt** og **Enhed** i estimatet eller den faktiske kontekst for **Materiale** med varelinjerne på prislisten.
1. Hvis systemet finder en prislinjevare, der har en omkostningssats for kombinationen af **Produkt** og **Enhed**, bruges denne omkostningssats som standarden.
1. Hvis systemet ikke kan matche værdierne for **Produkt** og **Enhed**, angives enhedsomkostningen som standard til **0** (nul).
1. Hvis systemet kan finde en matchende prislisteelementlinje i estimatet eller den faktiske kontekst, men prissætningsmetoden ikke er **Valutabeløb**, vil enhedsomkostningen som standard være **0** (nul). Dette forekommer, fordi Project Operations kun understøtter prissætningsmetoden **Valutabeløb** for materiale, der bruges på et projekt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
