---
title: Produktbaserede tilbudslinjer for omkostningsfastsættelse
description: Denne artikel indeholder oplysninger om, hvordan du anvender en kostpris på en produktbaseret tilbudslinje.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825604"
---
# <a name="costing-product-based-quote-lines"></a>Produktbaserede tilbudslinjer for omkostningsfastsættelse

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Produktbaserede tilbudslinjer i Dynamics 365 Project Operations indeholder også feltet **Kostpris**. Dette felt bruges til at spore kostprisen for produktet på tilbudslinjen og til beregninger downstream-rentabilitet.

Når der oprettes en produktbaseret tilbudslinje for et katalogprodukt, hentes omkostningen for den produktbaserede tilbudslinje fra feltet **Standardomkostning** i produktkataloget. Feltet standardomkostning i produktkataloget konfigureres i organisationens grundvaluta. Standardomkostningen for en enhed på den produkt baserede tilbudslinje konverteres til salgsvalutaen i tilbuddet.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Enhedsomkostning på en produktbaseret tilbudslinje

Formålet med en enhedsomkostning på en produktbaseret tilbudslinje er at give mulighed for at have forskellige omkostninger for et produkt for hvert salg. Dette er ikke et typisk scenario, men nogle gange diskonteres omkostningen for produktet af leverandøren, afhængigt af den kunde i det endelige salg.

Eksempel:

Fabrikam Robotics installerer robotarme i montagelinjer i A Datum Corporation. Fabrikam leverer Installationstjenester, men robotarme indkøbes fra Trey Robotics. Hvis installationen af robotarme i A Datum Corporation åbner en ny vertikalbranche for arme fra Trey Robotics, kan Trey tilbyde en særlig rabat for denne aftale til Fabrikam.

I dette tilfælde vil Fabrikam oprette produktbaseret tilbudslinje for robotarme og angive en særlig omkostning pr. enhed for dette tilbud. Denne omkostning adskiller sig fra standardomkostningen for arme fra Trey Robotics.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
