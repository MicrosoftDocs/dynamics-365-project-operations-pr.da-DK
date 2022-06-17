---
title: Nyheder i februar 2022 – Project Operations lille udrulning
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i februar 2022-udgivelsen af Project Operations lille udrulning.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922813"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Nyheder i februar 2022 – Project Operations lille udrulning

_Gælder for: Lille udrulning - aftale til proformafakturering_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.28.0.120

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

I denne version kan du tilføje op til 300 teammedlemmer på et enkelt projekt. Tidligere var grænsen for antallet af teammedlemmer 150. Du kan finde flere oplysninger under [Projektbegrænsninger](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Kvalitetsopdateringer

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2497369 | Væsentlig rettelse skal følge datoværdien i parametrene **Rettelse**. |
| Fakturering og prisfastsættelse | 2498697 | Forbedret sikkerhedskonfigurationen for **Tilbagekaldelse af tidsregistrering**. |
| Fakturering og prisfastsættelse | 2517455 | Handlingen **Opdateret fakturalinjetransaktioner** må ikke udløses flere samtidige gange for den samme faktura. |
| Fakturering og prisfastsættelse | 2517465 | Handlingen **Deaktiver fakturalinjedetaljer** blokeres, fordi den ikke understøttes. |
| Fakturering og prisfastsættelse | 2556660 | Løste problemet med kontroller af datoeffektivitet, der foretages på den prisliste, som er knyttet til en projektparameterpost. |
| Styring af salgsmuligheder | 2369202 | Korrigerede den forretningslogik, der kontrollerer, at prislister med overlappende ikrafttrædelsesdatoer kan knyttes til den samme projektkontrakt. |
| Styring af salgsmuligheder | 2385965 | Korrigerede funktionsmåden under fanen **Kunder** på siden **Projektkontrakt**, når du vælger **Gem og luk**. |
