---
title: Fastsættelse af kostpriser for estimater og faktiske tal
description: Dette emne indeholder oplysninger om, hvordan kostpriser for estimater og faktiske oplysninger fastsættes.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c2fe2a15d38ab5a1f2a93c6db4ed6b7eb9bbd33d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275666"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Fastsættelse af kostpriser for estimater og faktiske tal

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

For at kunne fastsætte kostpriser og kostprislisten til estimater og faktiske oplysninger bruger systemet oplysningerne i felterne **Dato**, **Valuta** og **Kontraktenhed** i det relaterede projekt. Når kostprislisten er fastsat, fastsætter programmet omkostningssatsen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Fastsættelse af omkostningssatser for faktiske og estimerede linjer for tid

Estimatlinjer for tid refererer til tilbuds- og kontraktlinjeoplysninger om tid- og ressourcetildelinger i et projekt.

Når en kostprisliste er blevet fastsat, bruger systemet felterne **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed** på estimatlinjen for tid for at matche dem med rollens prislinjer i prislisten. Denne afstemning antager, at du bruger standardprisfastsættelsesdimensionerne for arbejdsomkostninger. Hvis du har konfigureret systemet til at matche felter i stedet for eller som supplement til **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, bruges der en anden kombination til at hente en tilsvarende rolleprislinje. Hvis programmet finder en rolleprislinje, der har en omkostningssats for kombinationen **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, vil den være standardomkostningssatsen. Hvis programmet ikke kan matche værdierne for **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, hentes det rolleprislinjer med en tilsvarende rolle, men der vises ikke null-værdier for **Ressourceenheden**. Når det har en tilsvarende rolleprispost, vil omkostningssatsen som standard stamme fra den pågældende post. 

> [!NOTE]
> Hvis du konfigurerer en anden prioritering af **Rolle**, **Ressourcevirksomhed** og **Ressourceenhed**, eller hvis du har andre dimensioner med en højere prioritet, ændres denne funktionsmåde tilsvarende. Systemet henter rolleprisposter med værdier, der svarer til hver af prisfastsættelsesdimensionsværdierne i prioriteret rækkefølge med rækker, der har null-værdier for de pågældende dimensioner, der kommer sidst.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsættelse af omkostningssatser for faktiske og estimerede linjer for udgifter

Estimatlinjer for udgifter refererer til tilbuds- og kontraktlinjeoplysninger om udgifter og udgiftsestimatlinjer i et projekt.

Når en kostprisliste er blevet fastsat, bruger systemet en kombination af felterne **Kategori** og **Enhed** på estimatlinjen for en udgift for at matche dem med linjerne med **Kategoripris** på den fastsatte prisliste. Hvis systemet finder en kategorisprislinje, der har en omkostningssats for feltkombinationen **Kategori** og **Enhed**, konverteres omkostningssatsen til standarden. Hvis systemet ikke kan matche værdierne i **Kategori** og **Enhed**, eller hvis det kan finde en tilsvarende kategoriprislinje, men prissætningsmetoden ikke er **Pris pr. enhed**, konverteres omkostningssatsen som standard til nul (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]