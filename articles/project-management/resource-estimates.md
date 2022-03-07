---
title: Ressourceestimater
description: Dette emne indeholder oplysninger om, hvordan ressourceestimater beregnes i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286511"
---
# <a name="resource-estimates"></a>Ressourceestimater

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Ressourceestimater hentes fra faseinddelt tidsforbrug, der er defineret i arbejdsopgavehierarkiet sammen med de gældende dimensioner for prisfastsættelse. Beregningen er som regel **pris/time for hver rolle x timer.** Tidsfaseinddelt arbejdsindsats for de enkelte ressourcer gemmes i posten for ressourcetildelingen. Prisfastsættelsen gemmes i en foruddefineret prisliste. Enhedsomregning anvendes på baggrund af den gældende prisliste.

![Ressourceestimater](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standarder for kostpris og omkostningsvaluta

Kostpriser hentes som standard fra afdelingen.

## <a name="default-bill-rate-and-sales-currency"></a>Standarder for faktureringshyppighed og salgsvaluta

Salgspriser anvendes én gang pr. handel. Hierarkiet for standardprislisten er som følger:

1. Organisation
2. Kunde
3. Tilbud/kontrakt


[!INCLUDE[footer-include](../includes/footer-banner.md)]