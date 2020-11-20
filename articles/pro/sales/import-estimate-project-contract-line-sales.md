---
title: Importer et estimat til en projektbaseret kontraktlinje - lille
description: Dette emne indeholder oplysninger om, hvordan du importerer økonomiske estimater fra et projekt til en kontraktlinje.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b462af163fef1bfcbbc4f945df722d4e8a71fb1a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177459"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importer et estimat til en projektbaseret kontraktlinje - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I Dynamics 365 Project Operations kan du importere estimater fra et projekt til en projektbaseret kontraktlinje.

1. Kontroller, at feltet **Projekt** på den projektbaserede kontraktlinje er blevet udfyldt.
2. På fanen **Detaljer om kontraktlinje** skal du i undergitteret vælge **Importér fra projektestimat**. Der vises en dialogboks med opsummeringsindstillinger. De tilgængelige opsummeringsindstillinger er **Transaktionsklasse**, **Kategori**, **Rolle** og **Projektopgave**.
3. Afhængigt af dit valg i opsummering kopieres estimatet fra projektet for alle de transaktionsklasser og opgaver, der indgår i kontraktlinjen. Hvis du vil kontrollere, hvilke transaktionsklasser der er inkluderet, skal du vælge fanen **Generelt** på den projektbaserede kontraktlinje og kontrollere værdierne i felterne **Inkluder tid**, **Inkluder udgifter** og **Inkluder gebyrer**. 
4. Hvis du vil se, hvilke opgaver der er inkluderet, skal du vælge fanen **Fakturerbare opgaver** på kontraktlinjen. Afhængigt af de tilknyttede opgaver, hvor feltet **Inkludering af transaktionsklasser** er angivet til **Ja**, importeres alle estimater for disse kombinationer af opgaver og transaktionsklasser til kontraktlinjen.

Når du importerer estimater, vil systemet som standard angive prisfastsættelsen baseret på de projektprislister, der er knyttet til kontrakten, og den faktureringstype, der er konfigureret på den projektbaserede kontraktlinje. Hvis en opgave, rolle eller kategori er konfigureret på kontraktlinjen som ikke-fakturerbar, vil den importerede estimatlinje være ikke-fakturerbar og vil ikke svare til den aftalte værdi i kontraktlinjen.

Når en kontraktlinje indeholder linjedetaljer, opsummeres felterne **Kontraktværdi** og **Estimeret moms** i kontraktlinjen og kan ikke redigeres.

Hvis du har valgt flere opsummeringsindstillinger, forsøger systemet at opsummere efter alle de valgte indstillinger. Opsummeringsresultatet giver flere importerede kontraktlinjer, end hvis du kun vælger én opsummeringsindstilling.

Hvis et projekt f.eks. har følgende estimatlinjer for udgifter:

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| Opgave B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Opgave C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Når brugeren vælger at opsummere efter **Transaktionsklasse**, importeres følgende oplysninger:

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Når brugeren vælger at opsummere efter **Transaktionsklasse** og **Kategori**, importeres følgende oplysninger:

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 10/1/2020 | 6 | 200 | 1200 |

Når brugeren vælger at opsummere efter **Transaktionsklasse**, **Kategori** og **Bladnodeopgave**, importeres følgende. Bemærk, at dette resultat er det samme som på projektet:

| Opgave | Kategori | Dato | Antal | Enhedspris | Beløb |
| --- | --- | --- | --- | --- | --- |
| Opgave A | Flybilletter | 10/1/2020 | 4 | 400 | 1600 |
| Opgave B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Opgave C | Hotel | 11/1/2020 | 2 | 200 | 400 |
