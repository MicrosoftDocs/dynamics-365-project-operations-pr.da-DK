---
title: Nyheder oktober 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel giver oplysninger om de kvalitative opdateringer, der er tilgængelige i oktober 2022-udgivelsen af Microsoft Dynamics 365 Project Operations til ressource/ikke-lagerbaserede scenarier.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806608"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder oktober 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.57.0.176
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.30

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

| Funktionsområde | Funktionsnavn | Mere information |
| --- | --- | --- |
| Projektplanlægning og -sporing | **Ekstern planlægning til Project Operations**<br>I den eksterne planlægningstilstand kan kunder oprette, opdatere og slette indbyggede objekter, der er relateret til WBS'er (arbejdsopgavehierarkier) ved hjælp af de indbyggede Dataverse-API'er, men uden de aktuelle grænser, der håndhæves af Project for the Web. | [Ekstern planlægning](/dynamics365/project-operations/project-management/external-scheduling) |
| Udrulning og konfiguration | <p>**Giv kunder mulighed for at vælge installationstypen**<br>Produktbaserede opdateringer af Project Operations bruges til automatisk at installere Project Operations-løsningen med dobbeltskrivning, når kerne- og orkestreringsløsninger med dobbeltskrivning er installeret i miljøet.</p><p>Med denne funktion introduceres en ny parameter, **Funktion af løsningsopgradering**, i projektparametre. Når denne parameter er indstillet til **Lite only**, installerer produktbaserede opdateringer ikke længere automatisk Project Operations-løsningen med dobbeltskrivning, heller ikke selvom kerne- og orkestreringsløsninger med dobbeltskrivning er installeret i miljøet. Denne funktionsmåde vil være til fordel for kunder, der planlægger at bruge løsninger med dobbeltskrivning til at integrere salgsordrer i programmer til finans og drift, men som ønsker at bruge Project Operations i Lite-tilstand (dvs. uden integration med programmer til finans og drift).</p> | |
| Fakturering og prisfastsættelse | <p>**Valutakonvertering for ikke-faktureret salgstransaktion med udgifter i integrerede miljøer**<br>For kunder, der bruger Project Operations integreret med programmer til finans og drift (dvs. i ressource-/ikke-lagerlagerinstallationstypen), håndteres valutakurser typisk i programmer til finans og drift. Men hvis en udgiftskategori skal prissættes ved hjælp af beregningsmetoden for "kostpris" eller "avance i forhold til omkostning", når kunden faktureres, bruger den valutakurs, der bruges til at beregne salgsbeløb, valutakurserne i Dataverse, ikke valutakurserne fra programmer til finans og drift.</p><p>Med denne funktion introduceres en ny parameter, **Funktionsmåde for valutakonvertering**, i projektparametre. Når denne parameter angives til **Udvidet med fallback**, beregnes ikke-fakturerede salgsbeløb på udgiftstransaktioner ved hjælp af valutakurserne fra programmer til finans og drift.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Der er ingen opdateringer til Project Operations-tilknytninger med dobbelt skrivning i denne udgivelse. Du kan få vist en aktuel liste og aktuelle versioner af Project Operations-tilknytninger med dobbelt skrivning i [Project Operations-versioner med tilknytning af dobbelt skrivning](../environment/resource-dual-write-maps.md).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2316317 | Systemet gør det muligt at oprette en faktura, der ikke har fakturerbare transaktioner. |
| Fakturering og prisfastsættelse | 2737300 | Undersøg, om feltet **Kunde** er tilgængeligt, før formularen åbnes. |
| Fakturering og prisfastsættelse | 2744948 | Tilføj et null-tjek for faktureringsmetode. |
| Fakturering og prisfastsættelse | 2763515 | Håndtering af null-referencefejl, når salgskontrakten for fakturaen mangler. |
| Fakturering og prisfastsættelse | 2844301 | Oprettelse af batchfaktura mislykkes på grund af en fejl. |
| Fakturering og prisfastsættelse | 2845869 | Forkert lager for organisationstjenesten. |
| Fakturering og prisfastsættelse | 2853729 | Oplysninger om rolle og pris opdateres, når faktureringstypen ændres. |
| Fakturering og prisfastsættelse | 2940350 | Når de faktiske priser beregnes, er det kun aktive prislister, der skal angives automatisk. |
| Udrulning og konfiguration | 3001206 | Objektet msdyn\_replaylogheader forhindrer opgraderinger af kundeorganisationer. |
| Styring af salgsmuligheder | 2755582 | Håndtering af null-referenceundtagelser i hjælpen til reglen for opdeling af fakturering. |
| Styring af salgsmuligheder | 2761477 | Når fakturering opdeles, efterlader sletning af en milepæl (header) uafhængige milepæle. |
| Styring af salgsmuligheder | 2767595 | Når der åbnes en materialeforbrugspost i hovedformularen, ændres den ressource, der kan reserveres for posten, til den bruger, der i øjeblikket er logget på. |
| Projektplanlægning og -sporing | 2790384 | Timeout for ventende OperationSet er for kort. |
| Projektplanlægning og -sporing | 2957840 | Opgaver kan ikke gemmes, og kolonner kan ikke føjes til siden **Opgaver** i integreret Project Operations. |
| Ressourcestyring | 2751560 | Inkonsistente foretrukne afdelinger i ressourcekrav. |
| Underentrepriser | 2853245 | Sammenholdning af faktiske leverandørfakturalinjer opdaterer ikke bekræftelsesstatus, hvis der allerede er knyttet en kontraktlinje til leverandørens fakturalinje. |
| Underentrepriser | 2907231 | Procesfasen i leverandørfakturaer kan ikke fortsætte. |
| Tid og udgift | 2867363 | Poster forsvinder ikke fra visningen Fravær/ferier til godkendelse, når de sættes i kø til godkendelse. |
| Tid og udgift | 2894405 | TESA: Den ubrugte POC-mappe forårsager problemer i forbindelse med overholdelse af angivne standarder. |

### <a name="project-management-and-accounting-in-finance"></a>Oversigt over projektstyring og regnskab i Finance

Du kan få flere oplysninger om de fejlrettelser, der er inkluderet i denne opdatering, ved at logge på Microsoft Dynamics Lifecycle Services og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
