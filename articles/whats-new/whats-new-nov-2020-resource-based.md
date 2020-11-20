---
title: Nyheder november 2020 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Dette emne indeholder oplysninger om de kvalitetsopdateringer, der er tilgængelige i udgivelsen i november 2020 af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367258"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder november 2020 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

- Project Operations på CDS-miljø version 4.4.0.70
- Projektstyring og regnskab i Dynamics 365 Finance-miljø version 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Opdateringer til Project Operations for ressource-/ikke-lagerbaserede scenarier

### <a name="project-operations-on-cds"></a>Project Operations på CDS

| Funktionsområde                 | Referencenummer | Kvalitetsopdatering                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Styring af salgsmuligheder       | 2036993          | Estimatlinje og kontraktlinjer for ressourcetildeling opdateres på vindende tilbud, når tilbudslinjetypen er **Alle opgaver**.                                                 |
| Fakturering og prisfastsættelse          | 2070392          | Projektkontraktlinjer på fakturaen øges, hver gang **Opdater fakturatransaktioner** vælges.                                                                         |
| Projektplanlægning             | 2043336          | Det er ikke muligt at slette en post for et medlem af et projektteam.                                                                                                                                  |
| Projektplanlægning             | 2046013          | Ustabil funktionsmåde for estimatmærkers kolonner under belastning i forhold til ændring af tidsfasetypen.                                                                                   |
| Projektplanlægning             | 2046647          | Start- og sluttidspunkterne afviger med en time, når ressourcekraveme genereres fra projektteammedlemmer.                                                                      |
| Projektplanlægning             | 2053879          | (Ifølge den forestående CDS-udrulning) UdgivUtilknytttedeTildelinger bryder et forsøg på at gemme en opgave, når fejlen "Den værdi, der blev overført for ConditionOperator.In, er tom" opstår.                       |
| Projektplanlægning             | 2055501          | Hvis **Projektets startdato** ikke er udfyldt, opstår der en fejl i tidsplanen.                                                                                                      |
| Projektplanlægning             | 2066817          | Kan ikke oprette en generisk ressource ved hjælp af personvælgeren under fanen **Opgaver**.                                                                                                   |
| Projektplanlægning             | 2067034          | Knappen **Vis detaljer** er ikke tilgængelig på siden **Opgaveoplysninger**.                                                                                                       |
| Ressourcestyring          | 2046667          | Generiske teammedlemmer slettes ikke, selvom alle ressourcer er opfyldt.                                                                                                    |
| Hurtig registrering af tid og udgifter | 2047499          | Knappen **Ny** på siden med tidsregistrering åbner siden **Ny mailsignatur**.                                                                                               |
| Hurtig registrering af tid og udgifter | 2059859          | Der åbnes uventede pop op-vinduer, når der oprettes en udgiftspost.                                                                                                                         |
| Anden                        | 2044181          | (Afinstallation af indkøbsordre) - Fejlen "Posten er ikke tilgængelig" vises, når du forsøger at afinstallere kerneløsningerne msdyn_ProjectServiceCore_Patch og msdyn Project Service.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Oversigt over projektstyring og regnskab i Dynamics 365 Finance

| Funktionsområde        | Referencenummer | Kvalitetsopdatering                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indtægtsanerkendelse | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Den estimerede gennemførelsesprocent for projektet er forkert, når kontrakten bruger en fremmed valuta og procenten for fuldtført arbejde for den færdige metode.                     |
| Indtægtsanerkendelse | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Det er ikke muligt at bogføre estimater med fuldførelsesmetoden **Faktisk omkostninger**.                                                                                                    |
| Indtægtsanerkendelse | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminering mislykkes på grund af en fejl i bilagene, når firmavalutaen og transaktionsvalutaen er forskellige.                                              |
| Udgiftsstyring  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | For brugere, der ikke er administratorer, vises opslagsværdierne for udgiftslinjekolonner som f.eks **Projekt-id** og **Udgiftskategori** ikke korrekt i dataforbindelsesrammen. |
| Udgiftsstyring  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Standardlinjeegenskaben vises ikke for udgiftskategorier.                                                                                                         |
| Udgiftsstyring  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Udgiftsintegration skal inkludere linjeegenskaben fra udgiftsrapporten.                                                                                             |
| Fakturering           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Projektfakturaforslag kan ikke bogføres på grund af en fejlmeddelelse om, at kombinationen af FD ikke blev valideret.                                                    |
| Fakturering           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Det er ikke muligt at få vist transaktioner fra detaljesiden for **Faktura**.                                                                                                              |
| Fakturering           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Fakturaforslagslinjer kan slettes.                                                                                                                                  |
| Projektregnskab  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Menuelementer for **Prognose** er ikke synlige på listesiden for **Projekter**.                                                                                                   |
| Projektregnskab  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Kan ikke åbne **Projektopgørelse**   > **Transaktioner og prognoser**.                                                                                                       |
| Projektregnskab  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Juster regnskab** er ikke aktiveret for fakturerede projekttransaktioner.                                                                                                  |
| Projektregnskab  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Der inkluderes ingen regnskabsdetaljer i tabellen **ProjCDSActualsImport**, når kladden **Integration** bogføres.                                                  |
| Projektregnskab  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Projektprognoseregistreringen fordobles, når du fjerner og derefter tilføjer en ressourcetildeling på ny.                                                                            |
| Projektregnskab  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Valg af et link til projekt-ID åbner ikke Deep Link URL-adressen til CDS.                                                                                                         |
| Projektregnskab  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Det er ikke muligt at opdatere startdato på en opgave i CDS.                                                                                                                           |
| Projektregnskab  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Det er ikke muligt at aktivere funktionen for flere kontraktlinjer uden integration af CDS.                                                                                   |

### <a name="regulatory-updates"></a>Lovgivningsmæssige opdateringer
Du kan finde oplysninger om lovgivningsmæssige opdateringer til Finance and Operations-apps under [Lovgivningsmæssige opdateringer](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på LCS og få vist de planlagte lovgivningsmæssige opdateringer ved hjælp af værktøjet til fejlsøgning. Fejlsøgning giver dig mulighed for at søge efter land, funktionstype og udgivelse.
