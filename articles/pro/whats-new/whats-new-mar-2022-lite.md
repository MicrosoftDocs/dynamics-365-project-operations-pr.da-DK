---
title: Nyheder i marts 2022 – Project Operations lille udrulning
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i marts 2022-udgivelsen af Project Operations lille udrulning.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934221"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Nyheder i marts 2022 – Project Operations lille udrulning

_Gælder for: Lille udrulning - aftale til proformafakturering_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.30.0.99

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

- Underentreprise: Oprettelse og afstemning af erfaringer med leverandørfakturaer

## <a name="quality-updates"></a>Kvalitetsopdateringer

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Tid og udgift | 2388011 | Vis kommentarer for afvisning af indsendere af tidsregistreringer under massegodkendelse. |
| Projektplanlægning og -sporing | 2495294 | Projektdetaljer må ikke kunne redigeres på siden **Opgavedetaljer**. |
| Fakturering og prisfastsættelse | 2499605 | Kontraktmilepæle, der er oprettet ud fra tilbudsmilepæle, er forkert markeret som skrivebeskyttet. |
| Projektplanlægning og -sporing | 2506050 | Handlingssættet afventer i en time, hvis der ikke er ændringer, der skal gemmes. Sættet markeres derefter forkert som **Mislykket**, men det skal fuldføres med det samme. |
| Fakturering og prisfastsættelse | 2507401 | Der angives forkerte standardkontrakter i projekter på grund af forkert cachelagring. |
| Fakturering og prisfastsættelse | 2541660 | **Validering af salgsordrer** med dobbelt skrivning skal kun være for projektbaserede ordrer. |
| Fakturering og prisfastsættelse | 2552745 | Moms er ikke opdelt mellem kunder, der har oprettet opdelte faktureringsregler. |
| Fakturering og prisfastsættelse | 2558859 | Forbedrede fejlmeddelelser, når der konfigureres dimensioner for prisfastsættelse. |
| Fakturering og prisfastsættelse | 2558933 | **Import fra projektestimater** lykkes ikke, når **msdyn\_project** tilføjes som en prisfastsættelsesdimension. |
| Fakturering og prisfastsættelse | 2559101 | Sletning af projektparameter blokeres ikke og giver problemer. |
| Styring af salgsmuligheder | 2570390 | Du kan bruge plug-in'en med dobbelt skrivning til at gennemtvinge, at kontotypen for tilbud, ordrer og salgsmuligheder skal være **Kunde**, selvom den pågældende kontotype ikke er korrekt. |
| Fakturering og prisfastsættelse | 2586097 | Opdelt fakturering af faktiske omkostninger ændres ikke, når et projekt fjernes fra en projektkontraktlinje. |
| Fakturering og prisfastsættelse | 2589619 | Momsen på indkøbt materiale overføres til ikke-fakturerede faktiske salgsværdier og fakturaen. |
| Styring af salgsmuligheder | 2594015 | Et tilbud kan ikke lukkes som vundet for kunder, der har betalingsbetingelserne **Net60**. |
| Projektplanlægning og -sporing | 2595841 | I Project for the Web modtager brugere en fejlmeddelelse om en manglende **msdyn\_actualstart**, når de opretter en ny ressourceanmodning. |
| Tid og udgift | 2602511 | I feltet **Afvist af** for tidsposter vises **System** i stedet for en navngivet bruger som afviser. |
| Tid og udgift | 2602528 | En projektgodkender kan godkende tid på projekter, hvor de ikke er angivet som godkender. |
| Fakturering og prisfastsættelse | 2608550 | En rettelsesfaktura kan bekræftes, selvom originalen ikke ændres. |

## <a name="removed-and-deprecated-features"></a>Fjernede og udfasede funktioner

Artiklen [Fjernede eller udfasede funktioner i Project Operations](../../whats-new/removed-depreciated-features-project.md) beskriver funktioner, der er blevet fjernet eller udfaset for Dynamics 365 Project Operations.

- En fjernet funktion er ikke længere tilgængelig i produktet.
- En udfaset funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

En udfasningsmeddelelse vil blive vist i artiklen [Fjernede eller udfasede funktioner i Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 måneder inden, at en funktion fjernes fra produktet.
