---
title: Nyheder juni 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i juni 2021-udgivelsen af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028168"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder juni 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Dynamics 365 Project Operations:

- Project Operations på Dynamics 365 Dataverse-miljø version 4.11.0.156 eller 4.11.0.164.
- Projektstyring og regnskab i miljøer til programmer til finans og drift version 10.0.19.

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Følgende funktioner er omfattet af denne udgivelse:

- Mulighed for at slette [Linjer i forslag til projektfakturaer i tilpasningsscenarier](../invoicing/correct-project-invoice-proposals.md).
- Opdelte udgiftslinjer afspejler navnene på underkategorier i udgiftsrapporten [Nye udgiftsrapporter - nye funktioner](../expense/expense-reports-reimagined.md#new-features).
- Betalingsmetoden er tilgængelig i den nye udgiftsrude, når du opretter en ny udgift.
- Generel tilgængelighed af API'er til projektplanlægning. Denne nye funktionalitet gør det muligt for kunder at udføre programbaserede oprettelses-, opdaterings- og slettehandlinger på projektopgaver, ressourcetildelinger, opgaveafhængigheder og projektteammedlemsposter. Du kan finde flere oplysninger i [Brug API'er for projektplanlægning til at udføre handlinger med planlægningsobjekter](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Der er ingen opdateringer til Project Operations-tilknytninger med dobbelt skrivning i denne udgivelse. 

Du kan få vist en aktuel liste og aktuelle versioner af Project Operations-tilknytninger med dobbelt skrivning i [Project Operations-versioner med tilknytning af dobbelt skrivning](../environment/resource-dual-write-maps.md).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og løsningen til programmer til finans og drift. Visse funktioner fungerer muligvis ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan se den aktive version af tilknytningen på siden **Dobbelt skrivning** i kolonnen **Version**. Aktivér en ny version af tilknytningen ved at vælge **Tabeltilknytningsversioner** og dernæst vælge den nyeste version samt gemme den valgte version. Hvis du har brugertilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du begynder at tilknytte, skal du følge instruktionerne i sektionen [Problemer med mangler tabelkolonner på tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i vejledningen til fejlfinding af dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2281417 | Løste problemet vedrørende fejlen i handlingen for automatisk oprettelse af faktura via fakturaplanen. |
| Fakturering og prisfastsættelse | 2287835 | Forbedret ydeevne for bekræftelse af faktura. |
| Styring af salgsmuligheder | 2222555 | Materialeestimaters fakturerbarhed skal kopieres korrekt til tilbudslinjedetaljer ved brug af **Importér fra projektestimering**. |
| Styring af salgsmuligheder | 2223427 | Det er nu muligt at tilpasse handlingen **GenerateReoptionersImportreimporterScheduleOptions**. |
| Styring af salgsmuligheder | 2277528 | Løste problem med beregning af værdi for faktureringsmilepæl for projektkontraktlinjer med flere kunder. |
| Projektplanlægning og -sporing | 2226110 | Løste den periodiske fejl med funktionen **Opret krav** i gitteret **Projektteam**. |
| Projektplanlægning og -sporing | 2208109 | Brugere kan ikke oprette et projekt i én valuta med relaterede opgaver i en anden valuta. |
| Projektplanlægning og -sporing | 2258228 | Listen over felter, der kan ændres i med objekter **Planlægning** ved hjælp af Planlægnings-API'en, er blevet opdateret. |
| Projektplanlægning og -sporing | 2293989 | De korrekte sprogindstillinger og regionale indstillinger skal overføres til gitteret **Projektopgaver**. |
| Ressourcestyring | 2220493 | Løste problem med brugeroplevelsen i gitteret **Opgave**, når man hurtigt markerer en ressourceanmodning som fuldført. |
| Ressourcestyring | 2330496 | Løste fejlen med indlæsning af **Planlægningsoversigt**. (Kvalitetsopdatering er tilgængelig i version 4.11.0.164) |
| Tid og udgift | 2194431 | Gitteret **Tidsregistrering** skal overholde ugens begyndelse som angivet i **Systemindstillinger**. |
| Tid og udgift | 2277311 | Når du har slettet værdien i en celle i gitteret **Tidsregistrering**, forbliver markøren i gitteret. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Project Management and Accounting på Dynamics 365 Finance

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Projektstyring og regnskab | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Formularnoter** og **Formularkonfiguration** er ikke synlige under **Projektstyringskonfiguration** i juridiske objekter i Finance, som er integreret med Project Operations. |
| Projektstyring og regnskab | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Standardbeskrivelsen for moms er tom, når **Bogføringstypen** = **Moms** for projektfakturabilag. |
| Projektstyring og regnskab | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Dobbelte transaktioner bogføres, når opgavebaseret fakturering bruges i Dataverse sammen med Project Operations-integration. |
| Projektstyring og regnskab | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Procentdel for fuldført arbejde i omsætningsgenkendelse er forkert, mens du bruger Project Operations-integration. |
| Projektstyring og regnskab | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Periodisering af omsætning fordobles på en afventende leverandørfaktura i et integreret scenario i Project Operations. |
| Projektstyring og regnskab | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Kan ikke bogføre integrationskladden, når reglen for omsætningsprofilen er angivet til konfiguration af **Gruppe**. |
| Projektstyring og regnskab | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | En købsfaktura kan ikke bogføres for projektkøbsordrer, der har linjer med flere måleenheder. |
| Projektstyring og regnskab | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Den økonomiske standarddimension på et projekt kan ikke opdateres ved hjælp af projektets dataobjektet **Projekter V2**. |
| Projektstyring og regnskab | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Batchprocessen for at oprette projektestimater tager for lang tid om at blive fuldført. |
| Projektstyring og regnskab | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Sletning af en kontrakt sletter også den adresse, der er knyttet til kunden. |
| Rejser og udgifter | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Arbejdsprocesbetingelse for godkendelse af udgiftsrapporter evalueres ikke korrekt. |
| Rejser og udgifter | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Politikken for udgiftsrapporter evaluerer ikke projekt-id'et korrekt. |
| Rejser og udgifter | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Handlingen **Opdeling til personlig for interne udgiftstransaktioner** fungerer ikke korrekt. |
| Rejser og udgifter | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Begrundelser for udgiftsrapportlinjer slettes utilsigtet, når visse rejserekvisitioner slettes. Dette sker, når rec-id for udgiftsrapporten og rejserekvisitionen er ens. |
| Rejser og udgifter | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Der er et problem i mobilappen Udgift, når feltet **Projekt-id** er påkrævet i politikker for udgiftsrapporter. |
| Rejser og udgifter | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Interne udgifter, der er knyttet til et projekt, kan ikke redigeres. I stedet vises følgende fejlmeddelelse "Objektreference ikke angivet til en forekomst af et objekt". |
| Rejser og udgifter | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Når en udgiftsrapport er bogført, vises den forkerte valuta og det forkerte beløb vises i bankens hovedbog. |
| Rejser og udgifter | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Der er sket forbedringer af funktionen *Slet kreditkorttransaktioner*.  |
| Rejser og udgifter | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Den moms, der inkluderes i en udgiftsrapport, beregnes ikke konsekvent, når der angives en anden rapporteringsvaluta i en juridisk enhed. |
| Rejser og udgifter | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Ydeevnen påvirkes, når der tilføjes en ny kontant rejseudgift. |
| Rejser og udgifter | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Regler for udgiftspolitikken udløses ikke på en udgiftsrapport. |
| Rejser og udgifter | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Hvis du overfører en ny delt kategori ved hjælp af strukturen Data Management, fjernes alle underkategorier for alle delte kategorier. |
| Rejser og udgifter | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Når du opretter en udgiftslinje og dernæst vælger en kategori, vises følgende fejlmeddelelse: "Kombinationen af momsgruppe DOM og varemomsgruppe STD er ikke gyldig". |
| Rejser og udgifter | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Der er synkroniseringsproblemer i mobilprogrammet Udgift. |
