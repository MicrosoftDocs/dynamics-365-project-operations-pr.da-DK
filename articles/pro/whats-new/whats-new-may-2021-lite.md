---
title: Nyheder maj 2021 – Project Operations lille udrulning
description: Dette emne giver oplysninger om kvaliteten af de opdateringer, der er tilgængelige i maj 2021-udgivelsen af Project Operations lille udrulning.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 854a8c2290281b4d11a045321a334d8866806041
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583669"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Nyheder maj 2021 – Project Operations lille udrulning

_Gælder for: Lille udrulning - aftale til proformafakturering_

Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

   - Project Operations på Dataverse-miljø version 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Følgende funktioner er omfattet af denne udgivelse:

- [Planlægningstilstande](../../project-management/scheduling-modes.md): Projektledere kan nu definere, om et projekt skal administreres ved hjælp af planlægningstilstanden fast varighed, fast arbejde eller faste enheder.

## <a name="quality-updates"></a>Kvalitetsopdateringer

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2224568 | Logik tilføjet for at aktivere tilpasninger, der indebærer aktivering af plug-in'et til bekræftelse af faktura. |
| Fakturering og prisfastsættelse | 2101098 | Forbedrede logikken i standardfelter i en proformafaktura. Disse felter omfatter **Faktureringsadresse**, **Faktureringsnavn** og **Betalingsvilkår**. Felterne bruges nu som standard fra den tilsvarende projektkontraktkundepost. |
| Fakturering og prisfastsættelse | 2021413 | Du kan opdatere felterne **Faktiske omkostninger** og **Salg** i objektet **Opgave**, så de inkluderer salgsværdier fra ikke-fakturerede og fakturerede udgifter på opgaver. |
| Fakturering og prisfastsættelse | 2182110 | Når du kopierer en projektkontrakt, gendannes kontraktlinje-id'et i destinationsprojektkontrakten for at sikre, at det er entydigt. |
| Styring af salgsmuligheder | 2186741 | Valideringer tilføjet for at sikre, at feltet **Oprindelse** og transaktionstype ikke kan opdateres på eksisterende tilbudslinjedetaljer. |
| Styring af salgsmuligheder | 2191353 | Der må ikke oprettes milepæle på en tids- og materialekontraktlinje. |
| Styring af salgsmuligheder | 2216956 | Løst problemer med **Opdatér priser**. |
| Planlægning og sporing | 2182979 | Funktionen projektkopiering er forbedret for at sikre, at omkostningsestimatlinjer kopieres fra det oprindelige projekt. |
| Planlægning og sporing | 2184144 | Funktionen projektkopiering er forbedret for at sikre, at ressourcepositionsnavnet kopieres fra det oprindelige projekt. |
| Planlægning og sporing | 2184799 | Strengere kontrol for at sikre, at den anslåede startdato ikke ændres, mens kopieringen er i gang, når et projekt kopieres. |
| Planlægning og sporing | 2185134 | Når et projekt kopieres, angives den anslåede startdato for destinationsprojektet til dags dato. |
| Planlægning og sporing | 2196373 | Sikrer, at projektleder- og teammedlemsposter ikke duplikeres i projektteamet, når et projekt kopieres. |
| Planlægning og sporing | 2211833 | Ressourcetildelinger kopieres fra kildeprojektopgaven til destinationsprojektet. |
| Planlægning og sporing | 2186541 | Løste problemer i gitteret **Estimater**, når der grupperes efter **Ressource**. |
| Planlægning og sporing | 2166906 | Transaktionskategorien fra en opgave skal kopieres til objektet **Ressourcetildeling**. |
| Ressourcestyring | 2125362 | Løste problemer med oprettelse af et generisk teammedlem ved hjælp af den timebaserede allokeringsmetode. |
| Tid og udgift | 2113603 | Løste tilpasningsrelateret problem med at fjerne attributter fra siden **Tidsregistrering**. Systemet kontrollerer, om attributten findes på siden, inden attributterne tilgås ved hjælp af et script. |
| Tid og udgift | 2204377 | Kopierede timesedler skal vises automatisk, når du vælger **Kopiér uge**. |
| Tid og udgift | 2209059 | Feltet **Status** kan redigeres med henblik på tidsregistrering i Dynamics 365 Field Service. |
