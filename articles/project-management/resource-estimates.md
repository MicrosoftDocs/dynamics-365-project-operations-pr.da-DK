---
title: Ressourceestimater
description: Dette emne indeholder oplysninger om, hvordan ressourceestimater beregnes i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928554"
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
