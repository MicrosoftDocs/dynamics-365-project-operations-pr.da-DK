---
title: Administrer kundeemner - lille
description: Dette emne indeholder oplysninger om styring af projektbaserede kundeemner (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 00fc16b0e723d4df88ceae961d9772e26dd1451e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180500"
---
# <a name="manage-leads---lite"></a>Administrer kundeemner - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Projektbaserede kundeemner kan administreres og kvalificeres i Project Operations. Processen med kundeemnestyring omfatter oprettelse af arbejdsbaserede kundeemner og kvalificering af kundeemnerne. 

## <a name="list-of-project-sales-leads"></a>Liste med projektbaserede kundeemner

I sektionen **Salg** i venstre navigationsrude skal du åbne listesiden **Kundeemner** for at få vist en liste over alle kundeemneposter i systemet. Listen over de viste kundeemner er arbejdsbaserede og andre typer af kundeemner, der kan oprettes, hvis du også har programmerne Dynamics 365 Sales eller Dynamics 365 Field Service.

Du kan oprette en filtreret visning, hvis du kun vil se projektbaserede kundeemner, når du opretter et filter for værdien **Type**. Du kan f.eks. vælge kun at få vist arbejdsbaserede kundeemner.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Oprettelse af et nyt kundeemne for en projektbaseret handel

Når der kvalificeres et projektbaseret kundeemne, oprettes der en salgsmulighed og et firma. En projektbaseret salgsmulighed er udgangspunktet for forfølgelsen af salgsaktiviteter i salgsmulighedsfasen. Projektbaserede salgsmuligheder har særlige egenskaber, der er nødvendige for at sælge projektarbejde. Disse funktioner omfatter:

- Faktureringsmetoder for tids- og materiale samt fast pris
- Adskillige prislister gældende pr. dato for personale, udgifter og materiale anvendt på projekter.

Hvis et kvalificeret kundeemne automatisk skal oprette en salgsmulighed, skal du angive attributten **Type** til **Arbejdsbaseret**, når du opretter kundeemnet. Hvis du vælger en anden type, oprettes der ikke en projektbaseret salgsmulighed i kundeemnet, når den kvalificeres. Hvis den projektbaserede salgsmulighed ikke oprettes, vil de projektspecifikke funktioner ikke være tilgængelige i de efterfølgende salgsprocesser.

Følgende tabel indeholder vigtige feltoplysninger for et kundeemne og de downstream-konsekvenser for disse felter.

| **Felt** | **Placering** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Emne | Fanen Generelt | Dette tekstfelt skal indeholde en kort beskrivelse af handlen. | Emnet for kundeemnet vil som standard være emnet for salgsmuligheden og navnet på tilbud og projektkontrakt. |
| Skriv | Fanen Generelt | Feltet med grupperet indstilling har følgende indstillinger:</br>- Arbejdsbaseret (kun tilgængelig, når Project Operations er installeret)</br>- Enhedsbaseret (kun tilgængelig, når Project Operations og Sales er installeret)</br>- Servicevedligeholdelsesbaseret (tilgængelig, når Field Service er installeret) | Når værdien i dette felt er angivet til **Arbejdsbaseret** i kundeemnet, kvalificeres kundeemnet til at oprette en projektbaseret salgsmulighed. Der kræves en projektbaseret salgsmulighed for at aktivere alle projektspecifikke udvidelser og funktioner i den efterfølgende salgsproces for denne aftale. |
| Fornavn | Fanen Generelt | Fornavnet på det potentielle emnes kontakt | Når kundeemnet kvalificeres, oprettes der et firma, en kontrakt og en salgsmulighed. Fornavnet for kontaktværdien er den værdi, der angives her. |
| Efternavn | Fanen Generelt | Efternavnet på det potentielle emnes kontakt | Når kundeemnet kvalificeres, oprettes der et firma, en kontrakt og en salgsmulighed. Efternavnet for kontaktværdien er den værdi, der angives her. |
| Firma | Fanen Generelt | Navn på det potentielle kundeemnes virksomhed | Når kundeemnet kvalificeres, oprettes der et firma, en kontrakt og en salgsmulighed. Navnet på den oprettede konto er den værdi, der angives her. |
| Valuta | Fanen Detaljer | Det potentielle kundeemnes valuta | Når kundeemnet kvalificeres, oprettes der et firma, en kontrakt og en salgsmulighed. Valutaen for det oprettede firma er den værdi, der angives her. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalificer et nyt projektbaseret kundeemne

De kundeemner, der har værdien **Type** angivet til **Arbejdsbaseret**, kaldes projektbaserede kundeemner. Når et projektbaseret kundeemne er kvalificeret, oprettes følgende:

- Et firma, der bruger kundeemnets felt **Virksomhed**.
- En kontaktpersonpost, der er knyttet til firmaet, baseret på værdierne i felterne **Fornavn** og **Efternavn** for kundeemnet.
- En projektbaseret salgsmulighed, der har feltet **Type** angivet til **Arbejdsbaseret**.

Du kan finde mere detaljerede oplysninger om kvalificering af kundeemner i[Kvalificer eller konverter kundeemner](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Forretningsprocesflow for projektbaserede handler

Følgende forretningsprocesflow understøttes i forbindelse med projektbaserede handler i Project Operations:

- Forretningsproces for kundeemne til salgsmulighed
- Salgsproces for salgsmulighed

Forretningsprocessen for kundeemne til salgsmuligheder understøtter følgende faser:

| Fasenavn | Tilknyttet objekt | Funktionalitet |
| --- | --- | --- |
| Kvalificer | Potentiel kunde | Kvalificering af kundeemnet for at oprette et firma, en kontakt og en salgsmulighed. |
| Opstil tilbud | Salgsmulighed | Udarbejd salgsmuligheden for at tilføje flere oplysninger om det involverede arbejde, interessenter og konkurrenter. |
| Afgiv tilbud | Salgsmulighed | Udarbejd forslaget, og få godkendelse fra det interne vurderingsteam. |
| Luk | Salgsmulighed | Vind salgsmuligheden for lukke handlen. |
