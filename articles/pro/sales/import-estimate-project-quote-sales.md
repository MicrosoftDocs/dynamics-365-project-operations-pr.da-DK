---
title: Importere estimater fra et projekt til en projekttilbudslinje
description: Denne artikel indeholder oplysninger om, hvordan du importerer estimater fra et projekt til en projekttilbudslinje.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 61c9660f18882d12a7da8965c23b65e408256219
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824479"
---
# <a name="import-estimates-from-a-project-to-a-project-quote-line"></a>Importere estimater fra et projekt til en projekttilbudslinje 

_**Gælder for:** Lille udrulning - aftale om proformafakturering, Project Operations for ressource/ikke-lagerbaserede scenarier_

Hvis et projekt oprettes i forbindelse med den indledende salgsfase, kan du vælge at importere det økonomiske estimat fra projektet til den projektbaserede tilbudslinje.

1. Kontrollér, at den projektbaserede tilbudslinje indeholder projektoplysningerne i feltet **Projekt**.
2. På fanen **Tilbudslinjedetaljer** skal du vælge **Importer fra projektestimering**.
3. Når dialogboksen åbner, skal du vælge en af følgende opsummerende valgmuligheder.

  - **Transaktionsklasse**
  - **Kategori**
  - **Rolle** 
  - **Projektopgave**

Afhængigt af dit valg kopieres estimatet fra projektet for alle de transaktionsklasser, der indgår i tilbudslinjen, over. Hvis du vil kontrollere, hvilke transaktionsklasser der er inkluderet, skal du vælge fanen **Generelt** på den projektbaserede tilbudslinje og kontrollere værdierne for **Medtag tid**, **Medtag udgifter**, **Medtag materiale** og **Medtag gebyrer**.  Hvis du vil kontrollere, hvilke opgaver der er inkluderet, skal du vælge fanen **Fakturerbare opgaver** på tilbudslinjen.

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
