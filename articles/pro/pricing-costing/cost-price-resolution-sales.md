---
title: Fastsæt kostpriser for estimater og faktiske tal - lille
description: Dette emne indeholder oplysninger om, hvordan kostpriser for estimater og faktiske oplysninger fastsættes.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176784"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Fastsæt kostpriser for estimater og faktiske tal - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

For at kunne fastsætte kostpriser og kostprislisten til estimater og faktiske oplysninger bruger systemet oplysningerne i felterne **Dato**, **Valuta** og **Kontraktenhed** i det relaterede projekt. Når kostprislisten er fastsat, fastsætter programmet omkostningssatsen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Fastsættelse af omkostningssatser for faktiske og estimerede linjer for tid

Estimatlinjer for tid refererer til tilbuds- og kontraktlinjeoplysninger om tid- og ressourcetildelinger i et projekt.

Når en kostprisliste er blevet fastsat, bruger systemet felterne **Rolle** og **Ressourceenhed** på estimatlinjen for tid for at matche dem med rollens prislinjer i prislisten. Denne afstemning antager, at du bruger standardprisfastsættelsesdimensionerne for arbejdsomkostninger. Hvis du har konfigureret systemet til at matche felter i stedet for eller som supplement til **Rolle** og **Ressourceenhed**, bruges der en anden kombination til at hente en tilsvarende rolleprislinje. Hvis programmet finder en rolleprislinje, der har en omkostningssats for kombinationen **Rolle** og **Ressourceenhed**, vil den være standardomkostningssatsen. Hvis programmet ikke kan matche værdierne for **Rolle** og **Ressourceenhed**, hentes det rolleprislinjer med en tilsvarende rolle, men der vises ikke null-værdier for **Ressourceenheden**. Når det har en tilsvarende rolleprispost, vil omkostningssatsen som standard stamme fra den pågældende post. 

> [!NOTE]
> Hvis du konfigurerer en anden prioritering af **Rolle** og **Ressourceenhed**, eller hvis du har andre dimensioner med en højere prioritet, ændres denne funktionsmåde tilsvarende. Systemet henter rolleprisposter med værdier, der svarer til hver af prisfastsættelsesdimensionsværdierne i prioriteret rækkefølge med rækker, der har null-værdier for de pågældende dimensioner, der kommer sidst.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsættelse af omkostningssatser for faktiske og estimerede linjer for udgifter

Estimatlinjer for udgifter refererer til tilbuds- og kontraktlinjeoplysninger om udgifter og udgiftsestimatlinjer i et projekt.

Når en kostprisliste er blevet fastsat, bruger systemet en kombination af felterne **Kategori** og **Enhed** på estimatlinjen for en udgift for at matche dem med linjerne med **Kategoripris** på den fastsatte prisliste. Hvis systemet finder en kategorisprislinje, der har en omkostningssats for feltkombinationen **Kategori** og **Enhed**, konverteres omkostningssatsen til standarden. Hvis systemet ikke kan matche værdierne i **Kategori** og **Enhed**, eller hvis det kan finde en tilsvarende kategoriprislinje, men prissætningsmetoden ikke er **Pris pr. enhed**, konverteres omkostningssatsen som standard til nul (0).
