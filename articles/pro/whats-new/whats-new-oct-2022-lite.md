---
title: Nyheder i oktober 2022 – Project Operations lille udrulning
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i oktober 2022-udgivelsen af Microsoft Dynamics 365 Project Operations lille udrulning.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806609"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Nyheder i oktober 2022 – Project Operations lille udrulning

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.57.0.176

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

| Funktionsområde | Funktionsnavn | Mere information |
| --- | --- | --- |
| Projektplanlægning og -sporing | **Ekstern planlægning til Project Operations**<br>I den eksterne planlægningstilstand kan kunder oprette, opdatere og slette indbyggede objekter, der er relateret til WBS'er (arbejdsopgavehierarkier) ved hjælp af de indbyggede Dataverse-API'er, men uden de aktuelle grænser, der håndhæves af Project for the Web. | [Ekstern planlægning](/dynamics365/project-operations/project-management/external-scheduling) |
| Udrulning og konfiguration | <p>**Giv kunder mulighed for at vælge installationstypen**<br>Produktbaserede opdateringer af Project Operations bruges til automatisk at installere Project Operations-løsningen med dobbeltskrivning, når kerne- og orkestreringsløsninger med dobbeltskrivning er installeret i miljøet.</p><p>Med denne funktion introduceres en ny parameter, **Funktion af løsningsopgradering**, i projektparametre. Når denne parameter er indstillet til **Lite only**, installerer produktbaserede opdateringer ikke længere automatisk Project Operations-løsningen med dobbeltskrivning, heller ikke selvom kerne- og orkestreringsløsninger med dobbeltskrivning er installeret i miljøet. Denne funktionsmåde vil være til fordel for kunder, der planlægger at bruge løsninger med dobbeltskrivning til at integrere salgsordrer i programmer til finans og drift, men som ønsker at bruge Project Operations i Lite-tilstand (dvs. uden integration med programmer til finans og drift).</p> | |

## <a name="quality-updates"></a>Kvalitetsopdateringer

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2316317 | Systemet gør det muligt at oprette en faktura, der ikke har fakturerbare transaktioner. |
| Fakturering og prisfastsættelse | 2737300 | Undersøg, om kundefeltet er tilgængeligt, før formularen åbnes. |
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
| Ressourcestyring | 2751560 | Inkonsistente foretrukne afdelinger i ressourcekrav. |
| Underentrepriser | 2907231 | Procesfasen i leverandørfakturaer kan ikke fortsætte. |
| Tid og udgift | 2867363 | Poster forsvinder ikke fra visningen Fravær/ferier til godkendelse, når de sættes i kø til godkendelse. |
| Tid og udgift | 2894405 | TESA: Den ubrugte POC-mappe forårsager problemer i forbindelse med overholdelse af angivne standarder. |
