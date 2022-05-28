---
title: Nyheder marts 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Dette emne indeholder oplysninger om de kvalitetsopdateringer, der er tilgængelige i udgivelsen i marts 2021 af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a59aa5591dd5f5ed129ce710196eea572e66ea0b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599447"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder marts 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

- Project Operations på Dataverse-miljø version 4.8.0.91 
- Projektstyring og regnskab på Dynamics 365 Finance-miljø version 10.0.16 

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse


| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2133873 | Fast visning af valutasymbolet for **Enhedssalgspris** i gitteret **Udgiftsestimimat**. |
| Fakturering og prisfastsættelse | 2174616 | Når et tilbud vindes, refereres der til den brugerdefinerede prisliste for kontrakten i kontraktlinjedetaljer, som kopieres fra tilbuddet. |
| Styring af salgsmuligheder | 2167475 | Fast momsbeløb i den rette faktura, der startede som en ikke-faktureret faktisk post. |
| Styring af salgsmuligheder | 2176285 | Momsbeløb må ikke kopieres fra salgskontrakt-/tilbudslinjedetaljer til omkostningskontrakt-/tilbudslinjedetaljer. |
| Styring af salgsmuligheder | 2188079 | Der må ikke oprettes en opdelingsregel for fakturaer på kontrakter, der ikke er arbejdsbaserede. |
| Planlægning og sporing | 2125274 | Attributten **Project Dual Write Map** for **Project Start Date Mapping** er opdateret fra **msdyn\_taskearlieststart** til **msdyn\_actualstart**. |
| Planlægning og sporing | 2138853 | Funktionen Projektkopiering er opdateret for at sikre i henhold til omkostningsestimatlinjer, at referenceopgaver kopieres til destinationsprojektet. |
| Planlægning og sporing | 2154306 | Løst problemer med sletning af udgiftsestimater i Project Operations for ressourcebaserede scenarier. |
| Planlægning og sporing | 2173259 | Projektkopieringsfunktionen er opdateret for at sikre, at fejlmeddelelsen **Kopiering af WBS** ikke vises i visse scenarier. |
| Tid og udgift | 2148910 | Løste visningsproblem med siden **Rediger post** i gitteret **Tidsregistrering**. |
| Tid og udgift | 2159798 | Skærpede kontrolelementer for at sikre, at godkendte udgiftsposter ikke kan redigeres. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Project Management and Accounting på Dynamics 365 Finance

For yderligere oplysninger se [Nyheder januar 2021 - Project Operations for ressource-/ikke-ressource baserede scenarier](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Lovgivningsmæssige opdateringer

Du kan finde oplysninger om lovgivningsmæssige opdateringer til programmer til finans og drift under [Lovgivningsmæssige opdateringer](/dynamics365/finance/localizations/regulatory-updates). En anden måde at lære om lovgivningsmæssige opdateringer på er at logge på LCS og se de planlagte lovgivningsmæssige opdateringer ved hjælp af værktøjet til problemsøgning. Fejlsøgning giver dig mulighed for at søge efter land, funktionstype og udgivelse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]