---
title: Administrer kundeemner
description: Dette emne indeholder oplysninger om styring af projektbaserede kundeemner.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a10be42f4ae1ecc8ae5613ed8fdc669304e0ec72
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898614"
---
# <a name="manage-leads"></a>Administrer kundeemner

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Projektbaserede kundeemner kan administreres og kvalificeres i Project Operations. Processen med kundeemnestyring omfatter oprettelse af arbejdsbaserede kundeemner og kvalificering af kundeemnerne. 

## <a name="project-sales-leads"></a>Projektbaserede kundeemner

I sektionen **Salg** i venstre navigationsrude skal du åbne listesiden **Kundeemner** for at få vist en liste over alle kundeemneposter i systemet. Listen over de viste kundeemner er arbejdsbaserede og andre typer af kundeemner, der kan oprettes, hvis du også har programmerne Dynamics 365 Sales eller Dynamics 365 Field Service.

Du kan oprette en filtreret visning, hvis du kun vil se projektbaserede kundeemner, når du opretter et filter for værdien **Type**. Du kan f.eks. vælge kun at få vist arbejdsbaserede kundeemner.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Opret et nyt kundeemne for en projektbaseret handel

Når der kvalificeres et projektbaseret kundeemne, oprettes der en salgsmulighed og et firma. En projektbaseret salgsmulighed er udgangspunktet for forfølgelsen af salgsaktiviteter i salgsmulighedsfasen. Projektbaserede salgsmuligheder har særlige egenskaber, der er nødvendige for at sælge projektarbejde. Disse funktioner omfatter:

- Faktureringsmetoder for tids- og materiale samt fast pris
- Adskillige prislister gældende pr. dato for personale, udgifter og materiale anvendt på projekter

Hvis et kvalificeret kundeemne automatisk skal oprette en salgsmulighed, skal du angive attributten **Type** til **Arbejdsbaseret**, når du opretter kundeemnet. Hvis du vælger en anden type, oprettes der ikke en projektbaseret salgsmulighed i kundeemnet, når den kvalificeres. Hvis den projektbaserede salgsmulighed ikke oprettes, vil de projektspecifikke funktioner ikke være tilgængelige i de efterfølgende salgsprocesser.

Følgende tabel indeholder vigtige feltoplysninger for et kundeemne og de downstream-konsekvenser for disse felter.
 
| **Felt** | **Placering** | **Relevans, formål og vejledning** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Emne | Fanen Generelt | Dette tekstfelt skal indeholde en kort beskrivelse af handlen. | Emnet for kundeemnet vil som standard være emnet for salgsmuligheden og navnet på tilbud og projektkontrakt. |
| Skriv | Fanen Generelt | Feltet med grupperet indstilling har følgende indstillinger:</br>- Arbejdsbaseret (kun tilgængelig, når Project Operations er installeret)</br>- Enhedsbaseret (kun tilgængelig, når Project Operations og Sales er installeret)</br>- Servicevedligeholdelsesbaseret (tilgængelig, når Field Service er installeret) | Når værdien i dette felt er angivet til **Arbejdsbaseret** i kundeemnet, kvalificeres kundeemnet til at oprette en projektbaseret salgsmulighed. Der kræves en projektbaseret salgsmulighed for at aktivere alle projektspecifikke udvidelser og funktioner i den efterfølgende salgsproces for denne aftale. |
| Fornavn | Fanen Generelt | Fornavnet på det potentielle emnes kontakt | Når kundeemnet kvalificeres, oprettes der et firma, en kontrakt og en salgsmulighed. Fornavnet for kontaktværdien er den værdi, der angives her. |
| Efternavn | Fanen Generelt | Efternavnet på det potentielle emnes kontakt | Når kundeemnet kvalificeres, oprettes der et firma, en kontrakt og en salgsmulighed. Efternavnet for kontaktværdien angives her. |
| Firma | Fanen Generelt | Navn på det potentielle kundeemnes virksomhed | Når kundeemnet kvalificeres, oprettes der et firma, en kontrakt og en salgsmulighed. Navnet på den oprettede konto resulterer i denne værdi. |
| Valuta | Fanen Detaljer | Det potentielle kundeemnes valuta | Når kundeemnet kvalificeres, oprettes der et firma, en kontrakt og en salgsmulighed. Valutaen for det oprettede firma er den værdi, der angives her. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalificer et nyt projektbaseret kundeemne

De kundeemner, der har værdien **Type** angivet til **Arbejdsbaseret**, kaldes projektbaserede kundeemner. Når et projektbaseret kundeemne er kvalificeret, oprettes følgende:

- Et firma, der bruger kundeemnets felt **Virksomhed**.
- En kontaktpersonpost, der er knyttet til firmaet, baseret på værdierne i felterne **Fornavn** og **Efternavn** for kundeemnet.
- En projektbaseret salgsmulighed, der har feltet **Type** angivet til &quot;**Arbejdsbaseret**.

Du kan finde mere detaljerede oplysninger om kvalificering af kundeemner i[Kvalificer eller konverter kundeemner](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Kvalificering af kundeemne og juridiske enhedsoplysninger 

Når du kører Project Operations ved hjælp af udrulningstilstanden Project Operations for ressource-/ikke-lagerbaserede scenarier skal hver kunde og salgsmulighed have angivet feltet **Ejerselskab**. Ejerselskabet er den juridiske enhed i din organisation, der ejer leveringen af projektet. De enkelte kunder eller firmaer med relationstypen kunde skal i feltet **Ejerselskab** have værdien angivet til den juridiske enhed, der indgår kontrakter og forhandler med kunden. En kunde kan kun være i én juridisk enhed.

Når et kundeemne er kvalificeret, vil de kunde- og salgsmulighedsposter, der er oprettet, have feltet **Ejerselskab** angivet til firmaet i den aktuelle brugers reserverbare ressourcepost.

Hvis den aktuelle brugers eksisterende ressourcepost er tom, bruges feltværdien i **Ejerselskab** på brugerposten som standard for kunde- og salgsmulighedsposterne.

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
