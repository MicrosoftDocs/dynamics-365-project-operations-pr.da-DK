---
title: Oversigt over produktbaserede tilbudslinjer - lille
description: Dette emne indeholder oplysninger om at arbejde med produktbaserede tilbudslinjer.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6d86bf3ed81dbb69912d0694909aa5448a958666
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574930"
---
# <a name="product-based-quote-lines-overview---lite"></a>Oversigt over produktbaserede tilbudslinjer - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Du kan oprette produktbaserede tilbudslinjer i Dynamics 365 Project Operations. Produktbaserede tilbudslinjer kan tilføjes manuelt, eller de kan være elementer fra produktkataloget.

## <a name="product-catalog"></a>Produktkatalog

Hvert produkt i produktkataloget har en standardenhed og enhedsgruppe. Hvis flere produkter deler det samme sæt attributter, kan du oprette en produktfamilie, der deler de pågældende attributter. 

Et firma sælger f.eks. abonnementslicenser til forskellige typer af software. Alle abonnementsprogrammer har følgende to attributter:

- Antal brugere
- Et abonnements varighed målt i måneder

For at vedligeholde denne type katalog skal du oprette en produktserie med navnet **Abonnementsprogram** og tilføje antallet af brugere og abonnementets varighed som attributter. Derefter kan du tilføje de enkelte produkter til produktfamilien **Abonnementsprogram**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Tilføj produktkatalogelementer til et projekttilbud

Siderne **Projekttilbud** og **Projektkontrakt** indeholder sektioner for projektbaserede linjer og produktbaserede linjer. For produktbaserede linjer indeholder rullelisten på tilbudslinjen eller på projektkontraktlinjen alle produkter og enheder i produktprislisten. Du kan også tilføje produkter, der ikke er en del af produktprislisten.

Derudover kan du vælge produkter fra andre prislister eller direkte fra produktkataloget. Når du vælger produkter direkte fra et produktkatalog, bruges standardprislisten for produktet til at beregne produktets salgspris. Hvis der ikke er angivet en standardprisliste, angives prisen til nul (0).

Når en tilbudslinje er baseret på et produktkatalog, kan du tilsidesætte salgsprisen direkte på tilbudslinjen. En tilbudslinje i feltet **Prisfastsættelse** med to tilgængelige værdier:

- **Tilsidesæt prisfastsættelse**
- **Benyt standard**

Hvis du vælger **Tilsidesæt prisfastsættelse**, er standardprisen ikke angivet. Du skal i stedet angive en pris for produktet på tilbudslinjen. Hvis du vælger **Brug standard**, bruges standardsalgsprisen, og feltet er låst mod redigering.

Standardsalgspriserne angives på de produktbaserede linjer i et tilbud. Feltet **Prisfastsættelse** angives derefter til **Tilsidesæt prisfastsættelse**, så du kan redigere standardprisen i tilbudslinjerne. Dette er en tilsidesættelse af projektbaserede linjers funktion i Dynamics 365 Sales, som er specifik for Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]