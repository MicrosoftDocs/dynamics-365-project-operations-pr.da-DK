---
title: Konfigurer prislister
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer kost- og salgsprislister.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 77809f63230530e2e6553b76e56d37249b060ab9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584727"
---
# <a name="set-up-price-lists"></a>Konfigurer prislister

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Prislister i Dynamics 365 Project Operations repræsenterer et katalog over satser. Satserne udtrykker omkostningssatser, salgssatser og faktureringssatser. Afhængigt af, om prislisten udtrykker omkostningssatser eller salgs- og faktureringssatser, er konteksten af prislisten **Salg** eller **Omkostninger**.

Følgende udvidelser gælder kun for Project Operations og anvendes på prislister fra Dynamics 365 Sales.

- **Kontekst**: Dette felt har understøttede værdier i form af **Omkostninger** og **Salg**. Værdien **Indkøb** understøttes ikke. Angiv konteksten for **Omkostninger** for at oprette en kostprisliste eller angive konteksten til **Salg** for en salgsprisliste. Kostprislister fastsætter prisen for omkostningstypen på estimater og faktiske poster. Salgsprislister er en oversigt over estimerede og faktiske poster for ikke-fakturerede og fakturerede salgstyper.
- **Tidsenhed**: Dette er den standardtidsenhed, som prisen er konfigureret for i tabellen **Rollepris** for denne prisliste.
- **Prislisteobjekt**: Dette skjulte felt er angivet af Project Operations for at kunne skelne mellem prislister, der er tilbuds- eller kontraktspecifikke, fra prislister, der er standard og globalt gældende.

## <a name="price-list-header"></a>Overskrift til prisliste

Følgende tabel indeholder felterne på fanen **Generelt** for en prisliste og er entydige for Project Operations eller indeholder betydelige ændringer i funktionsmåder i set i forhold til prislister i Sales.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| Navn | Fanen **Generelt** og formularerne til **Hurtig oprettelse** | Prislistens identitet. | Prislisten vises med denne værdi på alle listesider og indstillinger for rullelister.|
| Sammenhæng | Fanen **Generelt** og formularerne til **Hurtig oprettelse** | Dette felt kan angives til **Kostpris** eller **Salg**. | En prisliste angivet med **Omkostninger** bruges til at slå prisen for omkostningsestimater og faktiske omkostningsværdier op. En prisliste angivet med **Salg** bruges til at slå prisen for salgsestimater og faktiske salgsværdier op. Kun prislister med konteksten **Salg** kan tilknyttes projektprislister for kunder, projekttilbud og projektkontrakter. |
| Startdato | Fanen **Generelt** og formularerne til **Hurtig oprettelse** | Startdatoen for den periode, hvor prislisten er gældende. | Sammen med feltet **Slutdato** bruges dette felt til at afgøre, hvilken prisliste der gælder for en bestemt estimatlinje eller faktisk linje. |
| Slutdato | Fanen **Generelt** og formularerne til **Hurtig oprettelse** | Slutdatoen for den periode, hvor prislisten er gældende. | Sammen med feltet **Startdato** bruges dette felt til at afgøre, hvilken prisliste der gælder for en bestemt estimatlinje eller faktisk linje. |
| Valuta | Fanen **Generelt** og formularerne til **Hurtig oprettelse** | Dette felt bruges til at angive standardvalutaen for de enkelte linjer i rollen, kategorien eller prislisteelementet, der er relateret til prislisten. | På prislisterne for **Salg**, roller, kategorier eller prislisteelementer kan der ikke oprettes en anden valuta end denne valuta. På prislister med **Omkostninger** kan du oprette en rolleprislinje i alle valutaer. Den valuta, der er defineret her, bruges som standard. Den brugeropsætning, der er relateret til rollepriser, kan tilsidesætte denne værdi for at give mulighed for opsætning af satser for arbejdskraftomkostninger i en hvilken som helst valuta. Kategoriomkostningssatser og prislisteelementomkostninger kan kun oprettes i den valuta, der er defineret her. |
| Tidsenhed | Fanen **Generelt** og formularerne til **Hurtig oprettelse** | Dette felt bruges til at angive standardtidsenheden for de enkelte rollelinjer, der er relateret til prislisten. | Værdien i dette felt bruges kun i forbindelse med opsætning af en relateret rollepris. På prislister med **Omkostninger** og **Salg** kan du oprette en rolleprislinje i alle tidsenheder. Tidsenheden, der er defineret her, bruges som standard. Den brugeropsætning, der er relateret til rollepriser, kan tilsidesætte denne værdi for at give mulighed for opsætning af satser for arbejdskraftomkostninger og fakturering i en hvilken som helst tidsenhed. |
| Beskrivelse | Fanen **Generelt** og formularerne til **Hurtig oprettelse** | Dette tekstfelt giver dig mulighed for at give en beskrivelse af prislisten på flere linjer. | Dette felt vises i de **Tilknyttede** visninger på prislisten i forskellige objekter, der har relaterede prislister. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]