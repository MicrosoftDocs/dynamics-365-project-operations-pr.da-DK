---
title: Nyheder februar 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i februar 2021-udgivelsen af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029608"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder februar 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Dynamics 365 Project Operations:

- Project Operations på Dataverse-miljø 4.7.0.95
- Projektstyring og regnskab i Dynamics 365 Finance-miljø version 10.0.16 

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| **Fakturering og prisfastsættelse** | 2053736 | Du kan nu tilgå detaljer om fakturalinjen ved at gå til **Faktura** > **Relaterede oplysninger**. |
| **Fakturering og prisfastsættelse** | 2122613 | Handlingerne **Aktivér** og **Deaktivér** blev fjernet fra de tilknyttede objekter for **Prisliste**. |
| **Fakturering og prisfastsættelse** | 2128606 | Løste problemet med **ullReferenceException** i tilføjelsesprogrammet **GetEstimatesForProject**. |
| **Udrulning og konfiguration** | 2139346 | Løste problemet med import af en ikke-administreret **Dynamics365ProjectOperationsDualWrite**-løsning. |
| **Udrulning og konfiguration** | 2140569 | Projektløsningen må ikke installeres i Dataverse Teams-miljøerne. |
| **Udrulning og konfiguration** | 2086991 | Begrænset brugertilpasning af lokalisering af webressourcer. |
| **Styring af salgsmuligheder** | 2136794 | Vis den korrekte fejlmeddelelse, når processerne for **Bekræft faktura** eller **Markér fakturaen som betalt** mislykkes. |
| **Styring af salgsmuligheder** | 2139330 | Hvis du ændrer projektlederen i et projekt, må den virksomhed, der ejer det, ikke nulstilles til standardværdien. |
| **Styring af salgsmuligheder** | 2146376 | Det korrigerede momsbeløb i en ikke-fakturerbar værdi oprettes ud fra fakturabekræftelsen. |
| **Projektplanlægning og -sporing** | 2099879 | Udrulningen af Dataverse-miljøet skal oprette en standardtransaktionskategori med et statisk ID og ikke oprette et tilfældigt ID pr. miljø. |
| **Projektplanlægning og -sporing** | 2128577 | Brugerrettighederne for Project Service er ændret, således at de opdaterer transaktionskategorien i en ressourcetildeling. |
| **Projektplanlægning og -sporing** | 2164035 | Løste problemer med funktionen **Kopiér projekt**. |
| **Tidsregistrering** | 2129161 | Der anvendes mere stramme begrænsninger for at sikre, at brugere ikke kan ændre og opdatere en tidsregistrering, der er indsendt eller godkendt. |
| **Tidsregistrering** | 2103572 | Godkendelse af tid for tidsregistreringer, der ikke er relaterede til projektet, må ikke søge efter rollen for projektgodkender. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Project Management and Accounting i Dynamics 365 Finance 

Du kan finde flere oplysninger om projektstyring og regnskab i Dynamics 365 Finance i [Nyheder i januar 2021 – Project Operations til ressource/ikke-lagerbaserede scenarier](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Lovgivningsmæssige opdateringer

Du kan finde oplysninger om lovgivningsmæssige opdateringer til programmer til finans og drift under [Lovgivningsmæssige opdateringer](/dynamics365/finance/localizations/regulatory-updates). En anden måde at lære om lovgivningsmæssige opdateringer på er at logge på Lifecycle Services (LCS) og se de planlagte lovgivningsmæssige opdateringer ved hjælp af værktøjet til problemsøgning. Fejlsøgning giver dig mulighed for at søge efter land, funktionstype og udgivelse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]