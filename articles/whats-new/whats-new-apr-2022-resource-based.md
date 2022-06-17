---
title: Nyheder april 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel giver oplysninger om de kvalitative opdateringer, der er tilgængelige i april 2022-udgivelsen af Microsoft Dynamics 365 Project Operations til ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912371"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder april 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.41.0.45
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.26

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Indkøbskategorier kan bruges sammen med projektkøbsordrer og afventende leverandørfakturaer. For flere oplysninger se [Brug indkøbskategorier sammen med projektkøbsordrer og afventende leverandørfakturaer](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Følgende tabel viser de tilknytninger med dobbelt skrivning, der er ændret eller tilføjet i Project Operations-versionen fra marts 2022.

| Objekttilknytning | Opdateret version | Kommentarer |
| -------------- | ------------------- | ------------|
| Integrationsobjekt for eksport af projektleverandørfakturalinje i Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Denne tilknytning understøtter brugen af indkøbskategorier sammen med projektkøbsordrer og afventende leverandørfakturaer. |

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| ------------ | ---------------- | -------------- |
| Tid og udgift | 2573900 | Funktionen **Moderne godkendelse** skal som standard aktiveres. |
| Fakturering og prisfastsættelse | 2603313 | Rettede en fejl om dubletpost, hvor tilbud og kontraktlinjer, der har et produkt, ikke tilføjes. |
| Udrulning og konfiguration | 2611368 | Kunderne skal kunne tilføje op til fem brugerdefinerede objekter til løsningen ved hjælp af den moderne appdesigner. |
| Tid og udgift | 2628285 | Løste et problem, der påvirkede muligheden for at angive den rette ressourcekategori under import af tid. |
| Styring af salgsmuligheder| 2628815 | Opdater tegnbegrænsningen i beskrivelsen af tilbudslinjen, så den svarer til tegnbegrænsningen i opgaveemnet, således at importen lykkes for opgaver, hvor emnet indeholder mere end 100 tegn. |
| Tid og udgift| 2629547 | Feltet **Indsendt af** i projektgodkendelser skal pege på den bruger, der har sendt posten. |
| Tid og udgift| 2629865 | Feltet **Kopiér kategori** på opgaver, når projekter kopieres. |
| Tid og udgift| 2636463 | Løste problem med filtrene for godkendelser i moderne godkendelsesformularer. |
| Projektplanlægning og -sporing | 2648300 | Løste et problem, der forhindrede, at projektejeren ændres. |
| Fakturering og prisfastsættelse | 2563000 | Det er ikke muligt at angive linjer for et ikke-faktureret salg, hvis valutaen er forskellig fra kontraktvalutaen. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Project Management and Accounting i Dynamics 365 Finance

Du kan få flere oplysninger om de fejlrettelser, der er inkluderet i denne opdatering, ved at logge på Microsoft Dynamics Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
