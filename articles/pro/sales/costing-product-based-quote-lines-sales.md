---
title: Produktbaserede tilbudslinjer for omkostningsfastsættelse
description: Dette emne indeholder oplysninger om anvendelse af en kostpris på en produktbaseret tilbudslinje.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003444"
---
# <a name="costing-product-based-quote-lines"></a>Produktbaserede tilbudslinjer for omkostningsfastsættelse

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Produktbaserede tilbudslinjer i Dynamics 365 Project Operations indeholder også feltet **Kostpris**. Dette felt bruges til at spore kostprisen for produktet på tilbudslinjen og til beregninger downstream-rentabilitet.

Når der oprettes en produktbaseret tilbudslinje for et katalogprodukt, hentes omkostningen for den produktbaserede tilbudslinje fra feltet **Standardomkostning** i produktkataloget. Feltet standardomkostning i produktkataloget konfigureres i organisationens grundvaluta. Standardomkostningen for en enhed på den produkt baserede tilbudslinje konverteres til salgsvalutaen i tilbuddet.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Enhedsomkostning på en produktbaseret tilbudslinje

Formålet med en enhedsomkostning på en produktbaseret tilbudslinje er at give mulighed for at have forskellige omkostninger for et produkt for hvert salg. Dette er ikke et typisk scenario, men nogle gange diskonteres omkostningen for produktet af leverandøren, afhængigt af den kunde i det endelige salg.

Eksempel:

Fabrikam Robotics installerer robotarme i montagelinjer i A Datum Corporation. Fabrikam leverer Installationstjenester, men robotarme indkøbes fra Trey Robotics. Hvis installationen af robotarme i A Datum Corporation åbner en ny vertikalbranche for arme fra Trey Robotics, kan Trey tilbyde en særlig rabat for denne aftale til Fabrikam.

I dette tilfælde vil Fabrikam oprette produktbaseret tilbudslinje for robotarme og angive en særlig omkostning pr. enhed for dette tilbud. Denne omkostning adskiller sig fra standardomkostningen for arme fra Trey Robotics.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]