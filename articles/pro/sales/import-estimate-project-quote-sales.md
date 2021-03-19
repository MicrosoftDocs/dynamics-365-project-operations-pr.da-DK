---
title: Importér estimater for et projekt til en projektbaseret tilbudslinje - lille
description: Dette emne indeholder oplysninger om, hvordan du importerer estimater fra et projekt til en tilbudslinje.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f3f18644a51d87cf3bb5b4effba2236eaf3d81a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273416"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line---lite"></a>Importér estimater for et projekt til en projektbaseret tilbudslinje - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Hvis et projekt oprettes i forbindelse med den indledende salgsfase, kan du vælge at importere det økonomiske estimat fra projektet til den projektbaserede tilbudslinje.

1. Kontrollér, at den projektbaserede tilbudslinje indeholder projektoplysningerne i feltet **Projekt**.
2. På fanen **Tilbudslinjedetaljer** skal du vælge **Importer fra projektestimering**.
3. Når dialogboksen åbner, skal du vælge en af følgende opsummerende valgmuligheder.

  - **Transaktionsklasse**
  - **Kategori**
  - **Rolle** 
  - **Projektopgave**

Afhængigt af dit valg kopieres estimatet fra projektet for alle de transaktionsklasser, der indgår i tilbudslinjen, over. Hvis du vil kontrollere, hvilke transaktionsklasser der er inkluderet, skal du vælge fanen **Generelt** på den projektbaserede tilbudslinje og kontrollere værdierne for **Medtag tid**, **Medtag udgifter** og **Inkluder gebyrer**.  Hvis du vil kontrollere, hvilke opgaver der er inkluderet, skal du vælge fanen **Fakturerbare opgaver** på tilbudslinjen.

Afhængigt af de tilknyttede opgaver og inkluderede transaktionsklasser, importeres estimaterne for disse kombinationer af opgaver og transaktionsklasser til tilbudslinjen.

Når du importerer estimater, vil systemet som standard angive prisen baseret på de projektprislister, der er knyttet til tilbuddet, og den faktureringstype, der er konfigureret på den projektbaserede tilbudslinje. Hvis en opgave, rolle eller kategori er konfigureret på den projektbaserede tilbudslinje som ikke-fakturerbar, vil den importerede estimatlinje blive angivet som ikke-fakturerbar og vil ikke svare til den tilbudte værdi i for tilbudslinjen.

Når en tilbudslinje indeholder linjedetaljer, opsummeres felterne **Tilbudsværdi** og **Estimeret skat** i tilbudslinjen og kan ikke redigeres.

Hvis du har valgt flere opsummeringsindstillinger, forsøger systemet at opsummere efter alle valgte indstillinger. Dette betyder, at resultatet af de importerede tilbudslinjer vil være højere, end hvis du kun har valgt én opsummeringsindstilling.

Hvis et projekt f.eks. havde følgende estimatlinjer for udgifter.

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| Opgave B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Opgave C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Når brugeren vælger at opsummere efter transaktionsklasse, importeres følgende oplysninger.

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
|||10/1/2020 | 3.34 | 840 | 2800 |

Når brugeren vælger at opsummere efter transaktionsklasse og -kategori, importeres følgende oplysninger.

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Når brugeren vælger at opsummere efter transaktionsklasse, kategori og bladnodeopgave, importeres følgende oplysninger. Bemærk, at dette resultat er det samme som på projektet.

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| Opgave B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Opgave C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]