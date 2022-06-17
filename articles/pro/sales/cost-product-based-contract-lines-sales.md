---
title: Produktbaserede kontraktlinjer for omkostninger - lille
description: Denne artikel indeholder oplysninger om oprettelse
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922905"
---
# <a name="cost-product-based-contract-lines---lite"></a>Produktbaserede kontraktlinjer for omkostninger - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Produktbaserede kontraktlinjer i Dynamics 365 Project Operations omfatter feltet **Kostpris**, som gemmer kostprisen for produktet til beregninger af downstream-rentabilitet.

Når der oprettes en produktbaseret kontraktlinje for et katalogprodukt, hentes omkostningen for linjen som standard fra feltet **Standardomkostning** i produktkataloget. Feltet **Standardomkostning** i produktkataloget konfigureres i organisationens grundvaluta. Når enhedsomkostningen konverteres til standarden på kontraktlinjen, konverteres den til salgsvalutaen i kontrakten.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Enhedsomkostning på en produktbaseret kontraktlinje

Med en enhedsomkostning på en produktbaseret kontraktlinje kan du have forskellige produktomkostninger ved hvert salg af en enhed. Selvom det ikke altid er nødvendigt, er der visse scenarier, hvor produktets omkostninger kan diskonteres for kunden af leverandøren. Overvej følgende scenarie:

Fabrikam Robotics installerer robotarme i montagelinjerne hos Adatum Corporation. Fabrikam leverer installationstjenester, men robotarmene er fra Trey Research. Hvis installationen af robotarme i Adatum Corporation åbner en ny vertikalbranche for Trey Reserarch, kan de tilbyde Fabrikam en særlig rabat i denne aftale. I dette tilfælde opretter Fabrikam en produktbaseret kontraktlinje for Robotic Arms. Der angives en omkostning pr. enhed for denne kontrakt. Omkostningen er forskellig fra omkostningen ved robotarme fra Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]