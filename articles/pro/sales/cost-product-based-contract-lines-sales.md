---
title: Produktbaserede kontraktlinjer for omkostningsfastsættelse
description: Dette emne indeholder oplysninger om oprettelse
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074403"
---
# <a name="costing-product-based-contract-lines"></a>Produktbaserede kontraktlinjer for omkostningsfastsættelse

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Produktbaserede kontraktlinjer i Dynamics 365 Project Operations omfatter feltet **Kostpris** , som indeholder kostprisen på produktet i relation til beregning af den afledte rentabilitet.

Når der oprettes en produktbaseret kontaktlinje for et katalogprodukt, hentes omkostningen for den produktbaserede kontraktlinje som standard fra feltet **Standardomkostning** i produktkataloget. Feltet **Standardomkostning** i produktkataloget konfigureres i organisationens grundvaluta. Når enhedsomkostningen konverteres til standarden på kontraktlinjen, konverteres den til salgsvalutaen i kontrakten.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Enhedsomkostning på en produktbaseret kontraktlinje

Med en enhedsomkostning på en produktbaseret kontraktlinje kan du have forskellige produktomkostninger ved hvert salg af en enhed. Selvom det ikke altid er nødvendigt, er der visse scenarier, hvor produktets omkostninger kan diskonteres for kunden af leverandøren. Overvej følgende scenarie:

Fabrikam Robotics installerer robotarme i montagelinjerne hos Adatum Corporation. Fabrikam leverer Installationstjenester, men robotarme indkøbes fra Trey Research. Hvis installationen af robotarme i Adatum Corporation åbner en ny vertikalbranche for Trey Reserarch, kan de tilbyde Fabrikam en særlig rabat i denne aftale. I dette tilfælde opretter Fabrikam en produktbaseret kontraktlinje for Robotic Arms og angiver en omkostning pr. enhed for denne kontrakt, som adskiller sig fra standardomkostningerne ved robotarme fra Trey Research.
