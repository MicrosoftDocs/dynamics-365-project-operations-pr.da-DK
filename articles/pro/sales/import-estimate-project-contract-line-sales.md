---
title: Importer estimater fra et projekt til en projektkontraktlinje
description: Denne artikel indeholder oplysninger om import af finansielle estimater fra et projekt til en kontraktlinje.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824667"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Importer estimater fra et projekt til en projektkontraktlinje

_**Gælder for:** Lille udrulning – aftale til håndtering af proformafakturering, Project Operations for scenarier baseret på ressource/ikke-lager_ _

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
