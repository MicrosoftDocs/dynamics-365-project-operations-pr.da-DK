---
title: Nyheder november 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel giver oplysninger om de kvalitative opdateringer, der er tilgængelige i november 2022-udgivelsen af Microsoft Dynamics 365 Project Operations til ressource/ikke-lagerbaserede scenarier.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831075"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder november 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.58.0.119
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Der er ingen opdateringer til Project Operations-tilknytninger med dobbelt skrivning i denne udgivelse. Du kan få vist en aktuel liste og aktuelle versioner af Project Operations-tilknytninger med dobbelt skrivning i [Project Operations-versioner med tilknytning af dobbelt skrivning](../environment/resource-dual-write-maps.md).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2781818 | Fejlen Nøglen blev ikke fundet under angivelse af standardpris for logfilen for materialeforbrug. |
| Fakturering og prisfastsættelse | 2922373 | Tilbudslinje kan ikke knyttes til et projekt, der er lukket som et tabt tilbud. |
| Fakturering og prisfastsættelse | 2943206 | Feltet **Kontraktlinje** i projektobjektet skal være valgfrit. |
| Fakturering og prisfastsættelse | 2953182 | Forbedr fejlmeddelelsen i forbindelse med rettelse af fakturaer.|
| Fakturering og prisfastsættelse | 2959500 | Tilbudslinje kan ikke knyttes til en projektopgave, der allerede er knyttet til et tabt tilbud.|
| Fakturering og prisfastsættelse | 2959560 | Meddelelsen "Denne kunde findes allerede i projektkontrakten" blev modtaget, mens tilbuddet blev lukket som vundet i visse landestandarder. |
| Fakturering og prisfastsættelse | 3031727 | Ressourcetildelinger mislykkes, og det påkrævede felt 'msdyn_Company' mangler. |
| Fakturering og prisfastsættelse | 3036905 | Ejende virksomhed initialiseres aldrig i ProjectTeamMember. |
| Styring af salgsmuligheder | 2763519 | Null-referencefejl i EnsureProjectContractAllowsUpdates. |
| Styring af salgsmuligheder | 2783798 | Når der importeres projektestimater på en tilbudslinje, mangler opgavebeskrivelser for udgifts- og materialeestimater.|
| Styring af salgsmuligheder | 2988635 | Angiv en bedre beskrivelse af fejlmeddelelse under sletning af kunde i tilbud. |
| Styring af salgsmuligheder | 3001191 | Tilbud kan ikke oprettes fra salgsmulighed, hvor faktureringsmetoden er angivet som null. |
| Opgrader | 3012324 | Projektkonvertering mislykkedes i et projekt med styretegn som f.eks. Tab i navnet. || Projektplanlægning og -sporing | 2790384 | Timeout for ventende OperationSet er for kort. |
| Projektplanlægning og -sporing | 3044275 | Der mangler en lokalisering for: missingProjectSchedulerErrorMessage. |
| Projektplanlægning og -sporing | 3044277 | Projektafstemningsgitter indlæses ikke, når planlæggeren ikke er angivet.|
| Ressourcestyring | 2943153 | Opdater fanen Sporing til at vise to decimaler for Varighed.|
| Underentrepriser | 2932774 | Skrivebeskyttet leverandørfakturalinje viser ikke fejl korrekt. |
| Underentrepriser | 2939556 | Status for kreditorfakturahoved skal ikke angives til Kladde på linje. Slettes, hvis den ikke er aktiv. |
| Tid og udgift | 2939998 | Inddrag ny TESA-version i ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Oversigt over projektstyring og regnskab i Finance

Du kan få flere oplysninger om de fejlrettelser, der er inkluderet i denne opdatering, ved at logge på Microsoft Dynamics Lifecycle Services og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
