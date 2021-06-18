---
title: Importer et estimat til en projektbaseret kontraktlinje
description: Dette emne indeholder oplysninger om, hvordan du importerer estimater fra et projekt til en kontraktlinje.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f8d9637e4a8bd09664c43ccc2b02514dc825997e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010239"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importer et estimat til en projektbaseret kontraktlinje

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

I Dynamics 365 Project Operations kan du importere estimater fra et projekt til en projektbaseret kontraktlinje.

1. Kontroller, at feltet **Projekt** på den projektbaserede kontraktlinje er udfyldt.
2. På fanen **Detaljer om kontraktlinje** skal du i undergitteret vælge **Importér fra projektestimat**. Der vises en dialogboks med opsummeringsindstillinger. De tilgængelige opsummeringsindstillinger er **Transaktionsklasse**, **Kategori**, **Rolle** og **Projektopgave**. Afhængigt af dine valg i opsummering kopieres estimatet fra projektet for alle de transaktionsklasser, der indgår i kontraktlinjen, over. 
3. Hvis du vil kontrollere, hvilke transaktionsklasser der er inkluderet, skal du vælge fanen **Generelt** for kontraktlinjen og kontrollere værdierne i felterne **Inkluder tid**, **Inkluder udgifter** og **Inkluder gebyrer**.

Når du importerer estimater, vil programmet som standard angive prisfastsættelsen baseret på de projektprislister, der er knyttet til kontrakten, og den faktureringstype, der er konfigureret på den projektbaserede kontraktlinje. Hvis en rolle eller kategori er konfigureret på kontraktlinjen som ikke-fakturerbar, vil den importerede estimatlinje for den rolle eller kategori være ikke-fakturerbar og vil ikke svare til den aftalte værdi i kontraktlinjen.

Når en kontraktlinje indeholder linjedetaljer, opsummeres felterne **Kontraktværdi** og **Estimeret moms** i kontraktlinjen og kan ikke redigeres.

Hvis du har valgt flere opsummeringsindstillinger, forsøger systemet at opsummere efter alle de valgte indstillinger. Opsummeringsresultatet giver flere importerede kontraktlinjer, end hvis du kun vælger én opsummeringsindstilling.

Hvis et projekt f.eks. havde følgende estimatlinjer for udgifter:

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| Opgave B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Opgave C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Når brugeren vælger at opsummere efter **Transaktionsklasse**, importeres følgende oplysninger:

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Når brugeren vælger at opsummere efter **Transaktionsklasse** og **Kategori**, importeres følgende oplysninger:

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Når brugeren vælger at opsummere efter **Transaktionsklasse**, **Kategori** og **Bladnodeopgave**, importeres følgende. Bemærk, at dette resultat er det samme som på projektet:

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| Opgave B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Opgave C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]