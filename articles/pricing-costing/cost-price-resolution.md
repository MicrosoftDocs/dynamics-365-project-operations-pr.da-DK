---
title: Fastsættelse af kostpriser for estimater og faktiske tal
description: Denne artikel indeholder oplysninger om, hvordan kostpriser for estimater og faktiske værdier løses.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af17712f0aef4fe3e6e758edd976cc377e90631d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919961"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Fastsættelse af kostpriser for estimater og faktiske tal

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

For at kunne fastsætte kostpriser og kostprislisten til estimater og faktiske oplysninger bruger systemet oplysningerne i felterne **Dato**, **Valuta** og **Kontraktenhed** i det relaterede projekt. Når kostprislisten er fastsat, fastsætter programmet omkostningssatsen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Fastsættelse af omkostningssatser for faktiske og estimerede linjer for tid

Estimatlinjer for tid refererer til tilbuds- og kontraktlinjeoplysninger om tid- og ressourcetildelinger i et projekt.

Når en kostprisliste er blevet fastsat, bruger systemet felterne **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed** på estimatlinjen for tid for at matche dem med rollens prislinjer i prislisten. Denne afstemning antager, at du bruger standardprisfastsættelsesdimensionerne for arbejdsomkostninger. Hvis du har konfigureret systemet til at matche felter i stedet for eller som supplement til **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, bruges der en anden kombination til at hente en tilsvarende rolleprislinje. Hvis programmet finder en rolleprislinje, der har en omkostningssats for kombinationen **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, vil den være standardomkostningssatsen. Hvis programmet ikke kan matche kombinationen af værdierne **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed** nøjagtigt, henter det rolleprislinjer med en matchende rolleværdi, men som indeholder null-værdier for **Ressourceenhed** og **Ressourcevirksomhed**. Når der er fundet en matchende rolleprispost med en tilsvarende rolleprisværdi, er standarden for kostsatsen baseret på den pågældende post. 

> [!NOTE]
> Hvis du konfigurerer en anden prioritering af **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, eller hvis du har andre dimensioner med en højere prioritet, ændres denne funktionsmåde tilsvarende. Systemet henter rolleprisposter med værdier, der svarer til de enkelte værdier for værdierne for prisfastsættelsesdimensioner i prioritetsrækkefølgen med rækker, der har null-værdier for de dimensioner, der står sidst i prioritetsrækkefølgen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsættelse af omkostningssatser for faktiske og estimerede linjer for udgifter

Estimatlinjer for udgifter refererer til tilbuds- og kontraktlinjeoplysninger om udgifter og udgiftsestimatlinjer i et projekt.

Når en kostprisliste er blevet fastsat, bruger systemet en kombination af felterne **Kategori** og **Enhed** på estimatlinjen for en udgift for at matche dem med linjerne med **Kategoripris** på den fastsatte prisliste. Hvis systemet finder en kategorisprislinje, der har en omkostningssats for feltkombinationen **Kategori** og **Enhed**, konverteres omkostningssatsen til standarden. Hvis systemet ikke kan matche værdierne i **Kategori** og **Enhed**, eller hvis det kan finde en tilsvarende kategoriprislinje, men prissætningsmetoden ikke er **Pris pr. enhed**, konverteres omkostningssatsen som standard til nul (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Fastsættelse af kostpriser på faktiske og anslåede linjer for materialer

Estimatlinjer for materialer henviser til tilbuds- og kontraktlinjedetaljerne for materiale og materialeestimatlinjerne på et projekt.

Når en kostprisliste er fastsat, bruger systemet en kombination af felterne **Produkt** og **Enhed** på estimatlinjen til et materialeestimat, der skal afstemmes mod linjerne **Prislisteelementer** i den fastsatte prisliste. Hvis systemet finder en produktprislinje, der har en kostsats for kombinationsfeltet **Produkt** og **Enhed**, anvendes kostsatsen som standard. Hvis systemet ikke kan matche værdierne for **Produkt** og **Enhed**, angives enhedsomkostningen som standard til nul. Denne standard anvendes også, hvis der er en tilsvarende prislisteelementlinje, men prisfastsættelsesmetoden er baseret på en standardomkostning eller aktuel omkostning, som ikke er defineret i produktet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
