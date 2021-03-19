---
title: Fastsæt kostpriser for estimater og faktiske tal - lille
description: Dette emne indeholder oplysninger om, hvordan kostpriser for estimater og faktiske oplysninger fastsættes.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bbb79fdc5c68d67530b5aa34fe6105211eff1768
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274542"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Fastsæt kostpriser for estimater og faktiske tal - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

For at kunne fastsætte kostpriser og kostprislisten til estimater og faktiske oplysninger bruger systemet oplysningerne i felterne **Dato**, **Valuta** og **Kontraktenhed** i det relaterede projekt. Når kostprislisten er fastsat, fastsætter programmet omkostningssatsen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Fastsættelse af omkostningssatser for faktiske og estimerede linjer for tid

Estimatlinjer for tid refererer til tilbuds- og kontraktlinjeoplysninger om tid- og ressourcetildelinger i et projekt.

Når en kostprisliste er løst, sammenholdes felterne **Rolle** og **Ressourceenhed** på estimatlinjen for Tid med rolleprislinjerne i prislisten. Denne sammenligning forudsætter, at du bruger standarddimensionerne for prisfastsættelse af lønomkostninger. Hvis du har konfigureret systemet til at matche felter i stedet for eller som supplement til **Rolle** og **Ressourceenhed**, bruges der en anden kombination til at hente en tilsvarende rolleprislinje. Hvis programmet finder en rolleprislinje, der har en omkostningssats for kombinationen **Rolle** og **Ressourceenhed**, vil den være standardomkostningssatsen. Hvis programmet ikke kan matche værdierne for **Rolle** og **Ressourceenhed**, hentes det rolleprislinjer med en tilsvarende rolle, men der vises ikke null-værdier for **Ressourceenheden**. Når det har en tilsvarende rolleprispost, vil omkostningssatsen som standard stamme fra den pågældende post. 

> [!NOTE]
> Hvis du konfigurerer en anden prioritering af **Rolle** og **Ressourceenhed**, eller hvis du har andre dimensioner med en højere prioritet, ændres denne funktionsmåde tilsvarende. Systemet henter rolleprisposter med værdier, der svarer til hver af prisfastsættelsesdimensionsværdierne i prioriteret rækkefølge med rækker, der har null-værdier for de pågældende dimensioner, der kommer sidst.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsættelse af omkostningssatser for faktiske og estimerede linjer for udgifter

Estimatlinjer for udgifter refererer til tilbuds- og kontraktlinjeoplysninger om udgifter og udgiftsestimatlinjer i et projekt.

Når en kostprisliste er løst, bruger systemet en kombination af felterne **Kategori** og **Enhed** på udgiftsestimatlinjen til at sammenligne med linjerne **Kategoripris** i den løste prisliste. Hvis systemet finder en kategorisprislinje, der har en omkostningssats for feltkombinationen **Kategori** og **Enhed**, konverteres omkostningssatsen til standarden. Hvis systemet ikke kan sammenholde værdierne for **Kategori** og **Enhed**, eller hvis det kan finde en tilsvarende kategoriprislinje, men prisfastsættelsesmetoden ikke er **Pris pr. enhed**, vil omkostningssatsen som standard være nul (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]