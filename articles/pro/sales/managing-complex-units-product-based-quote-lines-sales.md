---
title: Administration af komplekse undermoduler såsom pr. bruger pr. måned i forbindelse med produktbaserede tilbudslinjer - lille
description: Dette emne indeholder oplysninger om, hvordan du administrerer komplekse enheder for projektbaserede tilbudslinjer.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d53dde1d3b2705c5b0283f989d0e2eebfdcb5a0eb5f91cf4bf48e9c07aba79d1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989769"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Administration af komplekse undermoduler såsom pr. bruger pr. måned i forbindelse med produktbaserede tilbudslinjer - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dynamics 365 Project Operations bruger mængdefaktorer til at understøtte salget af abonnementsbaserede produkter. I forbindelse med abonnementsbaserede produkter udtrykkes antallet i tilbuds- eller projektkontraktlinjen som antallet af brugermåneder.

Prisen for abonnementsprogrammer gemmes som regel i kataloget som pris pr. bruger pr. måned. Under salgsprocessen er prisen i tilbudslinjen som regel den pris pr. bruger, pris pr. måned, som blev forhandlet og fratrukket af IT-salgsagenten. Hver handel har et forskelligt antal brugere og et forskelligt antal abonnementsmåneder. Det antal, der bruges til at beregne tilbudslinjen, er et produkt af antallet af brugere og antallet af abonnementsmåneder.

For at understøtte denne type salg introduceres konceptet med mængdefaktorer i Project Operations. Mængdefaktorer er baseret på produktattributterne i Dynamics 365. Når du konfigurerer bestemte egenskaber for et produkt, giver Project Operations dig mulighed for at markere et undersæt eller alle egenskaberne som mængdefaktorer.

Project Operations validerer, at kun numeriske egenskaber eller produktegenskaber med numerisk datatype markeres som mængdefaktorer. Når du tilføjer et produkt med mængdefaktorer til en tilbudslinje, bliver feltet **Antal** skrivebeskyttet. Når du har angivet værdier for produktegenskaber, der er mængdefaktorer, beregner Project Operations antallet i tilbudslinjen.

Dynamics 365 Sales kan f.eks. have følgende egenskaber:

- **Antal brugere**: Antallet af brugere
- **Antal måneder**: Antallet af abonnementsmåneder
- **Produkt-SKU**

Du kan markere egenskaberne **Antal brugere** og **Antal måneder** som mængdefaktorer ved at redigere egenskaberne for produktlinjen.

Hvis du vil oprette mængdefaktorer fra produktegenskaber, skal du følge disse trin:

1. I venstre navigationsrude i Project Operations skal du gå til **Salg** > **Produkter**.
2. Åbn det produkt, som du vil konfigurere mængdefaktorer for. Kontroller, at produktets egenskaber allerede er konfigureret.
3. På projektets side med **Projektoplysninger** skal du vælge fanen **Mængdefaktorer**.
4. I undergitteret skal du vælge **Beregning af + nyt felt**.
5. Angiv navnet på mængdefaktoren, og vælg den egenskabsværdi, der er knyttet til feltets beregning.
6. Gem og luk formularen. Gentag disse trin for alle de egenskaber, der skal bruges til beregning af mængden for den produktbaserede tilbudslinje.

Når du opretter en produktbaseret tilbudslinje for et produkt, låses mængden på tilbudslinjen. Antallet beregnes som et produkt af de egenskabsværdier, du kan angive for den pågældende tilbudslinje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]