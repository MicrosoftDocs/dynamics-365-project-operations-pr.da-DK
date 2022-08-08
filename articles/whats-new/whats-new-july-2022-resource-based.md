---
title: Nyheder juli 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel giver oplysninger om de kvalitative opdateringer, der er tilgængelige i juli 2022-udgivelsen af Microsoft Dynamics 365 Project Operations til ressource/ikke-lagerbaserede scenarier.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183884"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder juli 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.44.0.22
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Der er ingen opdateringer til Project Operations-tilknytninger med dobbelt skrivning i denne udgivelse. Du kan få vist en aktuel liste og aktuelle versioner af Project Operations-tilknytninger med dobbelt skrivning i [Project Operations-versioner med tilknytning af dobbelt skrivning](../environment/resource-dual-write-maps.md).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Udrulning og konfiguration | 2761472 | En installationsfejl i Project Operations er under behandling. |
| Fakturering og prisfastsættelse | 2746940 | Navnet på underleverandørlinjen bør højst bestå af 100 tegn. |
| Fakturering og prisfastsættelse | 2739162 | Kunder skal kunne se knapper på båndet i gittervisningen for faktiske værdier. |
| Projektplanlægning og -sporing | 2730318 | Opdateret validering for ikke-understøttede tegn i projektemnet. |
| Fakturering og prisfastsættelse | 2705361 | Fakturerede faktiske milepælssalg skal inkluderes i felter til projektsporing. |
| Fakturering og prisfastsættelse | 2675880 | Forebyg, at et projekt knyttes til en kontraktlinje, der ikke er arbejdsbaseret. |
| Fakturering og prisfastsættelse | 2664396 | Hvis en tilbudsprisliste gemmes uden et tilbud, skal der være en fejl, som oplyser, at tilbuddet ikke må være tomt. |
| Fakturering og prisfastsættelse | 2184019 | Fanen **Opgavebaseret fakturering** skal ikke vises for projekter, der ikke har nogen bagvedliggende kontrakt eller tilbud. |

### <a name="project-management-and-accounting-in-finance"></a>Oversigt over projektstyring og regnskab i Finance

Du kan få flere oplysninger om de fejlrettelser, der er inkluderet i denne opdatering, ved at logge på Microsoft Dynamics Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktioner, der som standard slået til i den kommende udgivelse

I følgende tabel vises de funktioner, der som standard er slået til i version 10.0.29. De fleste funktioner, der automatisk er slået til, kan slås fra i [Funktionsstyring](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). I fremtiden kan nogle funktioner, der er blevet slået til automatisk, blive fjernet fra Funktionsadministration og blive obligatoriske. Denne ændring sikrer, at kunderne bruger den aktuelle funktionalitet, så forbedringerne kan bygge på den aktuelle funktionalitet, efterhånden som de tilføjes. Funktioner aktiveres aldrig automatisk på under et år, medmindre de antages at være afgørende.

| Funktionsnavn | Dato for aktivering | Tilføjet funktion | Funktionstilstand | Modul |
| --- | --- | --- |--- |--- |
| Aktivér tilpasning af timetransaktion på grundlag af ændring i finansieringsregelallokering | 16. september 2022 | 7. oktober 2020 | Til som standard | Projektstyring og regnskab |
| Funktionen til rettelse af forudbetalte fakturaer på projektindkøbsordrer | 16. september 2022 | 6. oktober 2021 | Til som standard | Projektstyring og regnskab |
| Sket fakturaforslagslinjer ved hjælp af Project Operations i ressourcebaserede/ikke-lagerbaserede scenarier | 16. september 2022 | 6. oktober 2021 | Til som standard | Projektstyring og regnskab |
| Justér regnskab på en bogført projekttransaktion | 16. september 2022 | 10. maj 2020 | Til som standard | Projektstyring og regnskab |
| Aktivér standardkonfigurationen af regnskab for projekt | 16. september 2022 | 19. februar 2020 | Til som standard | Projektstyring og regnskab |
| Aktiver flere kontraktlinjer for et projekt | 16. september 2022 | 29. juni 2020 | Til som standard | Projektstyring og regnskab |
| Gør Project Hour-kladder skrivebeskyttede, hvis den aktuelle godkendelsesstatus ikke tillader redigering | 16. september 2022 | 6. oktober 2021 | Til som standard | Projektstyring og regnskab |
| Aktivér synkronisering af salgslinjer fra indkøbslinjer, når indkøbslinjer opdateres, og parameteren for administration af ændrede indkøbsordre er slået til | 16. september 2022 | 7. oktober 2020 | Til som standard | Projektstyring og regnskab |
| Aktiver Project Operations til Dynamics 365 Customer Engagement | 16. september 2022 | 29. juni 2020 | Til som standard | Projektstyring og regnskab |
| Funktionen til rettelse af projektransaktion | 16. september 2022 | 13. juli 2020 | Til som standard | Projektstyring og regnskab |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funktioner, der bliver obligatoriske i den kommende udgivelse

I følgende tabel vises de funktioner, der er obligatoriske fra version 10.0.29 og fremefter.

| Funktionsnavn | Dato for aktivering | Tilføjet funktion | Funktionstilstand | Modul |
| --- | --- | --- | --- | --- |
| Beregning af den bundne værdi på finansieringskilde uden afrunding af valutakursen | 16. september 2022 | 14. juni 2020 | Obligatorisk | Projektstyring og regnskab |
| Aktivér bogføring af projektjustering med samme hovedkonto som den oprindelige transaktion | 16. september 2022 | 14. juni 2020 | Obligatorisk | Projektstyring og regnskab |
| Detaljer om det bundne beløb i projektkontrakten | 16. september 2022 | 31. august 2019 | Obligatorisk | Projektstyring og regnskab |
| Aktivér sortering efter ressource i forbindelse med oprettelse af projektfakturaforslag | 16. september 2022 | 31. august 2019 | Obligatorisk | Projektstyring og regnskab |
