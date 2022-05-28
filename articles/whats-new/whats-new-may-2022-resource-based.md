---
title: Nyheder maj 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Dette emne giver oplysninger om de kvalitative opdateringer, der er tilgængelige i maj 2022-udgivelsen af Microsoft Dynamics 365 Project Operations til ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709970"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder maj 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.42.0.70
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Der er ingen opdateringer til Project Operations-tilknytninger med dobbelt skrivning i denne udgivelse. Du kan få vist en aktuel liste og aktuelle versioner af Project Operations-tilknytninger med dobbelt skrivning i [Project Operations-versioner med tilknytning af dobbelt skrivning](../environment/resource-dual-write-maps.md).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer
### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Ressourcestyring | 2634019 | Forbedrede fejlmeddelelser til forretningsvalidering, når generiske teammedlemmer tilføjes som ressourcer. |
| Projektplanlægning og -sporing | 2648515 | Begrænsede opdateringer af **ownerid**, **tilstand** og **status** i planlægningsobjekter. |
| Fakturering og prisfastsættelse | 2653167 | Decimalseparatoren i gitteret **Estimater** skal følge formatindstillingerne i **Personlige indstillinger**. |
| Fakturering og prisfastsættelse| 2662251 | Værdierne i felterne **Korrigeret enhed** og **Enhedsgruppe** bruges som standard, når der oprettes poster i materialeestimater. |
| Fakturering og prisfastsættelse| 2571408 | Ikke-fakturerede faktiske salgsværdier stemples med et proformafaktura-id, når der oprettes en kladdefaktura. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Project Management and Accounting i Dynamics 365 Finance

Du kan få flere oplysninger om de fejlrettelser, der er inkluderet i denne opdatering, ved at logge på Microsoft Dynamics Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
