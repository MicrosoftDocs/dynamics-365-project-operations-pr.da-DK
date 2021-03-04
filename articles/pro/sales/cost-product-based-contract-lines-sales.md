---
title: Produktbaserede kontraktlinjer for omkostninger - lille
description: Dette emne indeholder oplysninger om oprettelse
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764452"
---
# <a name="cost-product-based-contract-lines---lite"></a>Produktbaserede kontraktlinjer for omkostninger - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Produktbaserede kontraktlinjer i Dynamics 365 Project Operations omfatter feltet **Kostpris**, som gemmer kostprisen for produktet til beregninger af downstream-rentabilitet.

Når der oprettes en produktbaseret kontraktlinje for et katalogprodukt, hentes omkostningen for linjen som standard fra feltet **Standardomkostning** i produktkataloget. Feltet **Standardomkostning** i produktkataloget konfigureres i organisationens grundvaluta. Når enhedsomkostningen konverteres til standarden på kontraktlinjen, konverteres den til salgsvalutaen i kontrakten.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Enhedsomkostning på en produktbaseret kontraktlinje

Med en enhedsomkostning på en produktbaseret kontraktlinje kan du have forskellige produktomkostninger ved hvert salg af en enhed. Selvom det ikke altid er nødvendigt, er der visse scenarier, hvor produktets omkostninger kan diskonteres for kunden af leverandøren. Overvej følgende scenarie:

Fabrikam Robotics installerer robotarme i montagelinjerne hos Adatum Corporation. Fabrikam leverer installationstjenester, men robotarmene er fra Trey Research. Hvis installationen af robotarme i Adatum Corporation åbner en ny vertikalbranche for Trey Reserarch, kan de tilbyde Fabrikam en særlig rabat i denne aftale. I dette tilfælde opretter Fabrikam en produktbaseret kontraktlinje for Robotic Arms. Der angives en omkostning pr. enhed for denne kontrakt. Omkostningen er forskellig fra omkostningen ved robotarme fra Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]