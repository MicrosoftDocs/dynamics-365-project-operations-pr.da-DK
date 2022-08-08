---
title: Nyheder i juni 2022 – Project Operations lille udrulning
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i juni 2022-udgivelsen af Microsoft Dynamics 365 Project Operations lille udrulning.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031186"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Nyheder i juni 2022 – Project Operations lille udrulning

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.43.0.77 eller 4.43.0.119

## <a name="quality-updates"></a>Kvalitetsopdateringer

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Underentrepriser | 2708885 | Løste fejlmeddelelsen, der vises, når en bruger opretter en overskriftspost for en reserverbar ressource, hvis der ikke er udfyldt en ressource, der kan reserveres. |
| Projektplanlægning og -sporing | 2629441 | Rettede arbejdsprocesudløsende logik for at forhindre en uendelig løkke, når projektopgaver opdateres. |
| Tid og udgift | 2641209 | Import af tidsregistreringer fra tildelinger/reservationer skal bibeholde en ressourcereference, der kan reserveres. |
| Projektplanlægning og -sporing | 2651148 | Projektdokumentoverskriften skal beskyttes.|
| Projektplanlægning og -sporing | 2653145 | Tilføjede valideringer for at sikre, at der ikke kan oprettes en projektpost, som har ugyldige tegn i navnet. |
| Tid og udgift | 2654710 | Rettede filtreringen på siden **Godkendelser**. |
| Fakturering og prisfastsættelse | 2667805 | Tilføjede valideringer for at forhindre, at faktiske fakturerede salgsværdier oprettes, hvis der ikke findes understøttende ikke-fakturerede faktiske salgsværdier. |
| Fakturering og prisfastsættelse | 2668378 | Der er tilføjet valideringer for at forhindre, at der tilføjes en brugerdefineret prisfastsættelsesdimension, medmindre der er udfyldt et logisk navn og et feltnavn. |
| Tid og udgift | 2700428 | Forbedrede godkendelseslogikken for at sikre, at andre godkendelsessæt på projektet kan behandles, også selvom et af godkendelsessættene sidder fast i systemjob. |
