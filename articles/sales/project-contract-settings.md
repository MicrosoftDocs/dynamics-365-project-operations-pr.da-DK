---
title: Indstillinger for projektkontrakt
description: Dette emne indeholder oplysninger om de felter, der påvirker kontraktlinjer, og de oplysninger om kontrakten, der opsummeres på tværs af alle linjeelementer.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f34d6c6b92f164cc95405147356c34bb03eb127284aba7a92712b8eec42d792f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996294"
---
# <a name="header-details-for-project-based-contracts"></a>Overskriftsdetaljer for projektbaserede kontrakter

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne indeholder oplysninger om de felter, der gælder for hele projektkontrakten, herunder de indstillinger, der påvirker alle kontraktlinjer. Der medtages også oplysninger om den kontrakt, der opsummeres på tværs af alle de linjeelementer, der skal bruges til at anspore nøgletallene i projektkontrakten.

I følgende tabel vises felterne i en projektkontrakt, der er entydige for Dynamics 365 Project Operations eller har visse vigtige ændringer i funktionsmåden i forhold til salgsordrer i Dynamics 365 Sales.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| Skriv | Fanen **Oversigt** (skjult) | Dette er et grupperet indstillingsfelt med følgende indstillinger:</br>- **Arbejdsbaseret** (kun tilgængelig, når Project Operations er installeret)</br>- **Enhedsbaseret** (kun tilgængelig, når Project Operations og Sales er installeret)</br>- **Servicevedligeholdelsesbaseret** (tilgængelig, når Dynamics 365 Field Service er installeret) | I Project Operations er værdien i dette felt som standard **Arbejdsbaseret** og klassificerer kontrakten som en projektbaseret kontrakt. En kontrakt skal være projektbaseret, for at alle projektspecifikke udvidelser og funktioner kan aktiveres. |
| Ejende virksomhed | Fanen **Oversigt** | Den juridiske enhed, der holder regnskab med de omkostninger og indtægter, der påløber fra de projekter, der er knyttet til projektkontrakten. Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten. | Ejerselskabet svarer til begrebet juridisk enhed i modulet **Projektstyring og regnskab** under Project Operations. Der redegøres for alle påløbne omkostninger og indtægter i forbindelse med dette projekt i finanskladden i ejerselskabet. |
| Kunde | Fanen **Oversigt** | En reference til kundens firma eller firmapost. Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten. | Valutaen i projektkontrakten angives som standard på grundlag af kundens valuta. Valutaen kan ændres, før kontrakten gemmes. |
| Account manager | Fanen **Oversigt** | Navnet på account manageren for denne handel. Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten. | Account manageren er ansvarlig for at administrere relationen til kunden ved at fuldføre projektet. På basis af den reserverbare ressourcepost, der er knyttet til account manageren, angives standarden for kontraktenheden på projektkontrakten. |
| Kontraktenhed | Fanen **Oversigt** | Den organisationsenhed, der er ansvarlig for leveringen af de projekter, der er knyttet til denne kontrakt. Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten. | Kontraktenheden er afdelingen i det firma, der udfører projekterne. Alle kontraherende enheder har en valuta, og denne valuta bruges til at rapportere de anslåede og faktiske omkostninger, der er påløbet i løbet af projektet. |
| Produktprisliste | Fanen **Oversigt** | Denne prisliste bruges som standard for priser i produktbaserede kontraktlinjer. Listen over indstillinger i rullemenuen for dette felt indeholder en liste over prislister, hvor valutaen for prislisten stemmer overens med valutaen i kontrakten. Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten. I projektkontrakten er dette felt som standard hentet fra firmaposten, men den kan ændres. | Dette felt har ingen afledt relevans. |
| Valuta | Fanen **Oversigt** | Den valuta, der bruges til at rapportere værdien i denne handel, samt den valuta, som kunden bliver faktureret i. Når en kontrakt oprettes ud fra et tilbud, kopieres dette felt fra det tilsvarende felt på tilbudsposten. I projektkontrakten hentes dette felt som standard fra firmaposten, men den kan ændres. | Når en kontrakt er gemt, kan du ikke længere redigere dette felt. Dette felt anvendes som standard for produkt- og projektprislister på kontrakten. Valutaen på kontrakten anvendes til at periodisere valutaen på prislisten. |
| Grænse, der ikke må overskrides | Fanen **Oversigt** | Dette felt angiver den aftalte maksimumsværdi for den slutværdi, som kunden har indvilliget i at betale i forbindelse med denne aftale. | Maksimumsværdien evalueres under udførelsen og er gældende på tværs af alle linjeelementer og projekter, der er knyttet til denne handel. |
| Anmodet leveringsdato | Fanen **Oversigt** | Når en kontrakt oprettes ud fra et projekttilbud, kopieres dette felt fra det tilsvarende felt på projekttilbuddet. | Denne dato bruges som slutdatoen for at generere fakturaplaner. |

Følgende nøgletal er tilgængelige under fanen **Kontraktens ydeevne** i en projektkontrakt.

| Felt | Lokation | Beskrivelse |
| --- | --- | --- |
| Kontraktværdi | Overordnet kontrakt | Den samlede værdi af projektkontrakten. |
| Faktureret beløb | Overordnet kontrakt | Summen af beløbene på alle fakturaer i forhold til denne kontrakt. |
| Påløbne omkostninger | Overordnet kontrakt | Summen af alle de faktiske omkostninger, der er logført i alle de projekter, som er knyttet til kontrakten. |
| Bruttoavance | Overordnet kontrakt | Faktureret beløb – omkostninger, der er påløbet frem til dags dato/faktureret beløb |
| Anslået avance | Overordnet kontrakt | (Kontraktværdi – estimerede omkostninger)/KontraktværdiEstimerede omkostninger = summen af alle estimerede omkostninger for alle projekter, der er knyttet til kontrakten.|
| Kontraktværdi | Projektbaserede linjer | Værdien for kontraktlinjen. |
| Faktureret beløb | Projektbaserede linjer | For kontraktlinjer med fast pris: Summen af beløbene på alle fakturerede milepæle for faktiske salgsværdier i forhold til denne kontraktlinje på de forskellige fakturaer, der er oprettet for denne kontrakt. For kontraktlinjer med tid og materiale: Summen af beløbene på alle fakturerbare fakturerede faktiske salgsværdier i forhold til denne kontraktlinje på de forskellige fakturaer, der er oprettet for denne kontrakt. |
| Påløbne omkostninger | Projektbaserede linjer | Summen af alle de faktiske omkostninger, der er logført i alle de projekter, som er knyttet til kontraktlinjen. |
| Bruttoavance | Projektbaserede linjer | (Faktureret beløb – omkostninger, der er påløbet frem til dags dato) / Faktureret beløb |
| Anslået avance | Projektbaserede linjer | (Beløb på kontraktlinje i grundvaluta – Estimerede omkostninger for kontraktlinjen i grundvaluta) / Beløb på kontraktlinje i grundvaluta |
| Påløbne omkostninger | Detaljer for en projektbaseret linje | Tid: Summen af beløbet for faktiske tidsomkostninger logført for denne rolle på det projekt, der er knyttet til kontraktlinjen. Udgifter: Summen af beløbet for faktiske udgiftsomkostninger logført for denne kategori på det projekt, der er knyttet til kontraktlinjen. |
| Registreret antal | Detaljer for en projektbaseret linje | Tid: Alle tidsangivelser på en rolles faktiske tidsomkostninger på det projekt, der er knyttet til denne kontraktlinje. Udgifter: Alle mængder for denne udgiftskategori på de faktiske udgiftsomkostningsværdier på det projekt, der er knyttet til denne kontraktlinje. |
| Faktureret beløb | Detaljer for en projektbaseret linje | Hvis der er tale om en kontraktlinje med fast pris, er dette felt tomt på detaljeniveau og vises kun på kontraktlinjeniveau. Hvis der er tale om en kontraktlinje med tid og materiale, udføres beregninger på detaljeniveau. Detaljerne viser summen af beløbet på alle de fakturerede indtægtslinjer i forhold til denne kontraktlinje, som er fakturerbar. |
| Faktureret antal | Detaljer for en projektbaseret linje | Hvis der er tale om en kontraktlinje med fast pris, er dette felt tomt på detaljeniveau og vises kun på kontraktlinjeniveau. Hvis der er tale om en kontraktlinje med tid og materiale, udføres beregninger på detaljeniveau for tid og udgifter. Tid: Summen af antal timer på alle de fakturerede indtægtslinjer for denne rolle i forhold til denne kontraktlinje, som er fakturerbar. Udgifter: Alle mængder for denne udgiftskategori på de faktiske udgiftsomkostningsværdier på det projekt, der er knyttet til denne kontraktlinje. |
| Kontraktværdi | Produktbaserede linjer | Kontraktlinjeværdien for denne produktbaserede kontraktlinje. |
| Faktureret beløb | Produktbaserede linjer | Summen af beløbene på alle fakturalinjer i forhold til denne produktbaserede kontraktlinje på forskellige fakturaer, der oprettes for denne kontrakt. |
| Påløbne omkostninger | Produktbaserede linjer | Summen af alle de faktiske omkostninger for den produktbaserede kontraktlinje. |
| Bruttoavance | Projektbaserede linjer | Faktureret beløb – omkostninger, der er påløbet frem til dags dato/faktureret beløb |
| Anslået avance | Produktbaserede linjer | (Kontraktlinjeværdi - estimerede omkostninger for kontraktlinjen) / Kontraktlinjeværdi |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
