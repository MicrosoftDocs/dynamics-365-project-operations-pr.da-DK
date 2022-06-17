---
title: Produktbaserede tilbudslinjer for omkostningsfastsættelse
description: Denne artikel indeholder oplysninger om, hvordan du anvender en kostpris på en produktbaseret tilbudslinje.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 23eb3d29081769347d62098534a9863fd28fa90c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932565"
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