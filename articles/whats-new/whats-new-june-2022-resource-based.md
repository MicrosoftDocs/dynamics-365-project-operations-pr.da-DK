---
title: Nyheder juni 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel giver oplysninger om de kvalitative opdateringer, der er tilgængelige i juni 2022-udgivelsen af Microsoft Dynamics 365 Project Operations til ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959422"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder juni 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.43.0.77
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Følgende tabel viser de tilknytninger med dobbelt skrivning, der er ændret eller tilføjet i udgivelsen til Project Operations fra juni 2022.

| Objekttilknytning | Opdateret version | Kommentarer |
| --- | --- | --- |
| Integrationsobjekt for eksport af projektleverandørfaktura i Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Det ældre felt er blevet udfaset og tilknyttet det nye felt til sporing af status for leverandørfaktura. |

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

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
| Underentrepriser | 2677485 | Opdaterede destinationsversionen af tilknytningen med linjer på leverandørfakturaer med dobbeltskrivning. |
| Tid og udgift | 2700428 | Forbedrede godkendelseslogikken for at sikre, at andre godkendelsessæt på projektet kan behandles, også selvom et af godkendelsessættene sidder fast i systemjob. |

### <a name="project-management-and-accounting-in-finance"></a>Oversigt over projektstyring og regnskab i Finance

Du kan få flere oplysninger om de fejlrettelser, der er inkluderet i denne opdatering, ved at logge på Microsoft Dynamics Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
