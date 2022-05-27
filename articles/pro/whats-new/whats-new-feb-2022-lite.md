---
title: Nyheder i februar 2022 – Project Operations lille udrulning
description: Dette emne giver oplysninger om de kvalitative opdateringer, der er tilgængelige i februar 2022-udgivelsen af Project Operations lille udrulning.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: af66a5f61adf4f016f3fa547bbdfc75d06b2711b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574561"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Nyheder i februar 2022 – Project Operations lille udrulning

_Gælder for: Lille udrulning - aftale til proformafakturering_

Dette emne gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

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
