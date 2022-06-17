---
title: Nyheder eller ændringer i Project Operations i juli 2021 for lagerbaserede/produktionsbaserede scenarier
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i juli 2021-udgivelsen af Project Operations for lagerførte/produktionsbaserede scenarier.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: df9a68c5a12e6aec140867eb1db3d88279c05795
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933623"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Nyheder eller ændringer i Project Operations i juli 2021 for lagerbaserede/produktionsbaserede scenarier

_**Gælder for:** Project Operations for lagerbaserede/produktionsbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Dynamics 365 Project Operations:

- Projektstyring og regnskab i Dynamics 365 Finance-miljø version 10.0.20
 
### <a name="quality-updates"></a>Kvalitetsopdateringer
                                                                                                                                                                                  
| Funktionsområde                      | Referencenummer| Kvalitetsopdatering                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektstyring og regnskab | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Fejl med bundne omkostningsposter fra en købsrekvisition ryddes, så snart købsordren er frigivet fra købsrekvisitionen.                                                                           |
| Projektstyring og regnskab | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Budgetvalidering sker to gange på en købsrekvisition. Denne duplikering betyder, at rekvisitionen ikke kan lukkes, og at den tilsvarende købsordre ikke oprettes.                                                                                                                        |
| Projektstyring og regnskab | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Faktureringsreglen om **Faktureringsprocent** kan ikke fuldføres på grund af et afrundingsproblem.                                                                              |
| Projektstyring og regnskab | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Når du justerer transaktionen, og procentdelen har decimaler, justeres omkostningen og salgsprisen ikke korrekt.                                      |
| Projektstyring og regnskab | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | I kildeoversigten for regnskab vises timer for en enkelt timeseddellinje for flere timeseddellinjer med forskellige aktiviteter.                                      |
| Projektstyring og regnskab | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Brugertilpasning af gemte oversigter og timeseddellinjedetaljer medfører, at systemet altid åbner detaljerne for den første timeseddel på listen, når der forsøges at åbne en timeseddel.  |
| Projektstyring og regnskab | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Projektrodnoden forsvinder, og poster for arbejdsopgavehierarki slettes efter importen.                                                                                             |
| Projektstyring og regnskab | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Når varer modtages og udstedes delvist fra elementkravet, opdaterer systemet den forkerte budgetforbrugssaldo. |
| Projektstyring og regnskab | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Projektbeholdning for købsordrer viser ikke totaler korrekt i ruden **Totaler** eller i gitteret **Afventende faktura**.                                                                  |
| Projektstyring og regnskab | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Når lageret lukkes, bogføres tilpasninger af projekters vareomkostning på saldokontoen i stedet for på resultatkontoen.                                                            |
| Projektstyring og regnskab | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Et projekt med bogført transaktionsbilag og et estimatbilag bruger USD som regnskabsvalutaen, men beløbet viser, hvad det tilsvarende CAD ville være.              |
| Projektstyring og regnskab | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Bundne omkostninger med et varekrav og købsordrer er forkerte i processen til købsordrefaktura med til dels en produktkvittering og til dels en faktura.       |
| Projektstyring og regnskab | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Projekttilpasning opdaterer ikke salgsbeløbet korrekt med indirekte omkostninger.                                                                                    |
| Projektstyring og regnskab | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabellen **Timeseddel** mangler en defineret relation med visningen **Arbejder/ressource**.                                                                                   |
| Projektstyring og regnskab | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Feltet **Aktivitetsnummer** kan ikke udfyldes, når du vælger det i rullemenuen for en intern timeseddel.                                                                 |
| Projektstyring og regnskab | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Du kan ikke tilføje et tilpasset felt for **Formål** eller **Aktivitetsbeskrivelse** på følgende sider: **Bogførte projekttransaktioner**, **Oprettelse af fakturaforslag** eller **Fakturaforslag**.  |
| Projektstyring og regnskab | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Det forkerte kontrolelement for leveringsdato angives, når du opretter varekrav ved hjælp af dataadministration (**ProjSalesItemRequirementEntity**).                                              |
| Projektstyring og regnskab | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Når du vælger et projektkontrakt-id i Finance, åbnes siden i det integrerede Project Operations-miljø for at oprette en ny post i stedet for at åbne den eksisterende projektkontrakt.                                                                                                                 |
| Projektstyring og regnskab | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Etiketten "@SYS4083080" ("Der kunne ikke findes en entydig arbejderpost svarende til de angivne værdier") er ikke oversat til dansk.                                |
| Projektstyring og regnskab | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Feltet **Varesalgsmomsgruppe** kan ikke redigeres i et fakturaforslag.                                                                               |
| Projektstyring og regnskab | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Bundne omkostninger overdrives med ikke-fradragsberettigede momsbeløb.                                                                                                    |
| Projektstyring og regnskab | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Hvis du opretter en intern timeseddel med flere projekter og forskellige økonomiske dimensioner, genereres der uventede værdier i hovedbogen.                             |
| Projektstyring og regnskab | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Fakturaforslagslinjer duplikeres på grund af flere tilfælde af den periodiske proces **Importér fra midlertidige lagring**, der kører samtidig.                                      |
| Projektstyring og regnskab | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Der opstår en fejl i fakturaforslaget til kreditnotaen, så transaktionerne på bilaget ikke stemmer.    |
| Projektstyring og regnskab | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Bundne projektomkostninger bliver forkerte, når afventende fakturaer frigives.                                                                             |
| Projektstyring og regnskab | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Du kan ikke oprette en kreditnota for en projektsalgsordre, når momsen er angivet i en anden valuta end firmavalutaen.                                      |
| Projektstyring og regnskab | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Sletning af en kontrakt sletter også den adresse, der er knyttet til kunden.                                                                                     |
| Projektstyring og regnskab | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Et fakturaforslag, der er resultatet af en negativ ændring af tidstransaktionen, kan ikke bogføres.                                                                    |
| Rejser og udgifter                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Moms beregnes forskelligt i udgiftsrapporter.                                                                                                                  |
| Rejser og udgifter                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Frigivelsesopdatering **DB72_Expense.updateTrvExpTransProjTransId()** tillader ikke, at **trvExpTrans.ReferenceDataAreaId** opretter den nye nummerserie.                    |
| Rejser og udgifter                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Det arkiverede beløb vises ikke i det obligatoriske felt.                                                                                                             |
| Rejser og udgifter                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Forbedringer i ydeevnen ved vedhæftning af en omkostning i udgiftsrapporten ved hjælp af den ny brugergrænseflade for udgifter.                                                            |
| Rejser og udgifter                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Du kan slette bogførte udgiftsrapporter.                                                                                           |
| Rejser og udgifter                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Meddelelsen om udgiftspolitik vises flere gange.                                                                                                       |
| Rejser og udgifter                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Feltet **Betalingsmetode** er inkluderet i ruden **Ny udgift**.                                                                                                      |
| Rejser og udgifter                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Værktøjet **Nulstil status for udgiftsdokument** bør nulstille udgiftsrapportens status til **Kladde**, hvis arbejdsprocessen ikke blev fundet. 

### <a name="regulatory-updates"></a>Lovgivningsmæssige opdateringer
Du kan finde oplysninger om lovgivningsmæssige opdateringer til programmer til finans og drift under [Lovgivningsmæssige opdateringer](/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på Lifecycle Services (LCS) og se de planlagte lovgivningsmæssige opdateringer ved hjælp af fejlfindingsværktøjet. Fejlsøgning giver dig mulighed for at søge efter land, funktionstype og udgivelse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
