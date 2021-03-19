---
title: Administrer komplekse undermoduler til produktbaserede kontraktlinjer - lille
description: Dette emne indeholder oplysninger om support af salget af abonnementsbaserede produkter.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273326"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Administrer komplekse undermoduler til produktbaserede kontraktlinjer - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dynamics 365 Project Operations bruger mængdefaktorer til at understøtte salget af abonnementsbaserede produkter. I forbindelse med abonnementsbaserede produkter udtrykkes antallet i kontrakten eller projektkontraktlinjen som antallet af brugermåneder.

Prisen for abonnementsprogrammer gemmes i kataloget som pris pr. bruger pr. måned. Under salgsprocessen er prisen i kontraktlinjen som regel den pris pr. bruger, pris pr. måned, som blev forhandlet og fratrukket af salgsagenten. Hver handel har et forskelligt antal brugere og et forskelligt antal abonnementsmåneder. Det antal, der bruges til at beregne beløbet i kontraktlinjen, er et produkt af antallet af brugere og antallet af abonnementsmåneder.

For at understøtte denne type salg understøtter Project Operations konceptet *mængdefaktorer*. Mængdefaktorer er baseret på produktattributter. Når du konfigurerer bestemte egenskaber for et produkt, kan du markere et undersæt af disse egenskaber eller alle egenskaberne som mængdefaktorer.

Project Operations validerer, at kun numeriske egenskaber eller produktegenskaber med numerisk datatype markeres som mængdefaktorer. Når der tilføjes et produkt med konfigurerede mængdefaktorer til en kontraktlinje, bliver feltet **Antal** skrivebeskyttet. Når du har angivet værdier for produktegenskaber, der er mængdefaktorer, beregner Project Operations antallet i kontraktlinjen.

Dynamics 365 Sales kan f.eks. have følgende egenskaber:

- **Antal brugere**: Antallet af brugere.
- **Antal måneder**: Antallet af abonnementsmåneder.
- **Produktvarenummer**: Produktets lagerbeholdningsenhed (varenummer).

Egenskaberne **Antal brugere** og **Antal måneder** kan mærkes som mængdefaktorer ved at redigere egenskaberne for produktlinjen.

Hvis du vil oprette mængdefaktorer fra produktegenskaber, skal du benytte følgende fremgangsmåde.

1. I **Project Operations** skal du vælge **Salgsprodukter**.
2. Åbn det produkt, som du vil konfigurere mængdefaktorer for. Kontroller, at produktet har egenskaber, der allerede er konfigureret.
3. På siden **Projektoplysninger** skal du vælge fanen **Mængdefaktorer**.
4. I undergitteret skal du vælge **Beregning af + nyt felt**.
5. Angiv navnet på **Mængdefaktoren**, og vælg den egenskabsværdi, der er knyttet til feltets beregning.
6. Gem og luk formularen.
7. Gentag trin 2-6 for alle de egenskaber, der tilsammen udgør antallet i den produktbaserede kontraktlinje.

Hvis mængdefaktorer er konfigureret, og brugeren opretter en kontraktlinje for dette produkt, låses antallet på kontraktlinjen. Antallet beregnes derefter som et produkt af egenskabsværdierne for den pågældende kontraktlinje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]