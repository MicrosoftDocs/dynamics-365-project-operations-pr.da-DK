---
title: Overskriftsdetaljer for projektbaserede tilbud
description: Denne artikel indeholder oplysninger om de oplysninger og indstillinger, der gælder for og påvirker projekttilbud.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7e2b625476508d781b9f3f2440cde1f7374372c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825213"
---
# <a name="header-details-for-project-based-quotes"></a>Overskriftsdetaljer for projektbaserede tilbud

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_


Denne artikel indeholder en beskrivelse af de oplysninger, der er relevante for et projekttilbud. Dette omfatter de indstillinger, der påvirker alle tilbudslinjer, og oplysninger om det tilbud, der opsummeres på tværs af alle linjeelementer, til at drive nøgletal i projekttilbuddet.

I følgende tabel vises opsummeringsfelterne i et projekttilbud der er entydige for Dynamics 365 Project Operations eller har visse vigtige ændringer i funktionsmåden i forhold til tilbud i Dynamics 365 Sales.

| **Felt** | **Placering** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Skriv | Oversigtsfanen (skjult) | Feltet med grupperet indstilling har følgende indstillinger:</br>- Arbejdsbaseret (kun tilgængelig, når Project Operations er installeret)</br>- Enhedsbaseret (kun tilgængelig, når Project Operations og Sales er installeret)</br>- Servicevedligeholdelsesbaseret (tilgængelig, når Dynamics 365 Field Service er installeret) | Når du bruger programmet Project Operations, angives værdien i dette felt automatisk til **Arbejdsbaseret**. Dette klassificerer tilbuddet som et projektbaseret tilbud. Et tilbud skal være projektbaseret, for at alle projektspecifikke udvidelser og funktioner kan aktiveres. |
| Ejende virksomhed | Resumé | Den juridiske enhed, der skal holde regnskab med de omkostninger og indtægter, der påløber fra dette projekt eller de projekter, der er knyttet til tilbuddet. Når tilbud oprettes ud fra en salgsmulighed, kopieres dette felt fra det tilsvarende felt på salgsmuligheden. | Ejerselskabet svarer til begrebet juridisk enhed i modulet **Projektstyring og regnskab** under Project Operations. Der redegøres for alle påløbne omkostninger og indtægter i forbindelse med dette projekt i finanskladden i ejerselskabet. |
| Kundeemne | Fanen Oversigt | Reference til kundens firma eller firmapost. Der skal refereres en gyldig kunde på projekttilbuddet, som er konfigureret som en kunde i tilbuddets ejerselskab. Ejerselskabet viser listen med juridiske enheder, og disse konfigureres i modulet **Projektstyring og regnskab** under Project Operations. Når et tilbud oprettes ud fra en salgsmulighed, kopieres dette felt fra det tilsvarende felt på salgsmuligheden. | Valutaen i projekttilbuddet angives som standard på grundlag af kundens valuta. Dette kan dog ikke ændres, før tilbuddet er blevet gemt. |
| Account manager | Fanen Oversigt | Navnet på account manageren for denne handel. Når et tilbud oprettes ud fra en salgsmulighed, kopieres dette felt fra det tilsvarende felt på salgsmuligheden. | Account manageren er ansvarlig for at administrere relationen til kunden ved at fuldføre dette projekt. På basis af den reserverbare ressourcepost, der er knyttet til Account manager, angives standarden for kontraktenheden på projekttilbuddet.|
| Kontraktenhed | Fanen Oversigt | Den afdeling, der er ansvarlig for leveringen af det projekt eller de projekter, der er knyttet til dette tilbud. Når et tilbud oprettes ud fra en salgsmulighed, kopieres dette felt fra det tilsvarende felt på salgsmuligheden. | Kontraktenheden er afdelingen i det firma, som skal udføre projekterne, når handlen er indgået. Alle kontraherende enheder har en valuta, og denne valuta bruges til at rapportere de anslåede og faktiske omkostninger, der er påløbet i løbet af projektets fuldførelse. |
| Produktprisliste | Fanen Oversigt | Det er den prisliste, der bruges som standard for priser i de produktbaserede tilbudslinjer. Listen over indstillinger for dette felt indeholder en liste over prislister, hvor valutaen for prislisten stemmer overens med valutaen i tilbuddet. Når et tilbud oprettes ud fra en salgsmulighed, kopieres dette felt fra det tilsvarende felt på salgsmuligheden. Dette felt i salgsmuligheden hentes som standard fra firmaposten, men den kan ændres. | Når et tilbuddet bliver vundet, kopieres denne feltværdi til den projektkontrakt, der er oprettet. |
| Valuta | Fanen Oversigt | Angiver den valuta, der skal bruges til rapportering af værdien for denne handel. Dette er også den valuta, som kunden faktureres i, hvis handlen vindes. Når et tilbud oprettes ud fra en salgsmulighed, kopieres dette felt fra det tilsvarende felt på salgsmuligheden. Dette felt i salgsmuligheden hentes som standard fra firmaposten, men den kan ændres af brugeren.  | Når et tilbud er gemt, kan du ikke længere redigere dette felt. Dette anvendes som standard for produkt- og projektprislister på tilbuddet. Valutaen på tilbuddet anvendes til at periodisere valutaen på prislisten. |
| Grænse, der ikke må overskrides | Fanen Oversigt | Dette angiver den aftalte maksimumsværdi for den slutværdi, som kunden er villig til at betale i forbindelse med denne aftale. | Denne maksimumsværdi evalueres under udførelsen og er gældende på tværs af alle linjeelementer og projekter, der er knyttet til denne handel. |
| Anmodet leveringsdato | Fanen Oversigt | Når et tilbud oprettes ud fra en salgsmulighed, kopieres dette felt fra det tilsvarende felt på salgsmuligheden. | Denne dato bruges som slutdato for generering af fakturaplaner. |

Nedenfor vises de faner og nøgletal, der er tilgængelige i et projekttilbud, som er entydigt for Project Operations, eller som er vigtige ændringer af funktionsmåden i forhold til tilbud i Sales:

| **Felt** | **Placering** | **Beskrivelse** |
| --- | --- | --- |
| Rentabilitetsanalyse | Tilbudsfanen | Fanen viser følgende målepunkter:</br>- Samlede fakturerbar omkostninger</br></br>- Samlede ikke-fakturerbare omkostninger</br>- Omsætning i alt</br>- Samlet omsætning (basis)</br>- Bruttoavance</br>- Justeret bruttoavance|
| Sammenligning med kundernes forventninger | Tilbudsfanen | Denne fane viser følgende målepunkter:</br>- Estimeret fuldførelse</br>- Ønsket fuldførelse</br>- Kundebudget</br>- Værdi i tilbud |
| Tilbudsanalyse | Tilbudsfanen | Under denne fane opsummeres følgende vigtigste nøgletal for et projekttilbud</br>- Sammenligning med kundernes forventninger til budget og planlægning</br>- Bruttoavance</br>- Justeret bruttoavance |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
