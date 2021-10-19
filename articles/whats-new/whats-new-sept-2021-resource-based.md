---
title: Nyheder september 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Dette emne giver oplysninger om de kvalitative opdateringer, der er tilgængelige i september 2021-udgivelsen af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547147"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder september 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

*Finder anvendelse for: Project Operations for ressource-/ikke-lagerbaserede scenarier*

Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

   - Project Operations i Microsoft Dataverse-miljø version 4.14.0.99.
   - Projektstyring og regnskab i Dynamics 365 Finance-miljø version 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Der er ingen opdateringer til Project Operations-tilknytninger med dobbelt skrivning i denne udgivelse. Du kan få vist en aktuel liste og aktuelle versioner af Project Operations-tilknytninger med dobbelt skrivning i [Project Operations-versioner med tilknytning af dobbelt skrivning](../environment/resource-dual-write-maps.md).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Visse funktioner fungerer muligvis ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan se den aktive version af tilknytningen på siden **Dobbelt skrivning** i kolonnen **Version**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har brugertilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer med at starte tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner for tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Tid og udgift | 1811407 | Tilpassede sikkerhedsrollen for projektgodkender af godkendelser af udgiftsregistreringer. |
| Tid og udgift | 1811438 | Tilpassede sikkerhedsrollen for projektgodkender for annullering af godkendelse af tidsregistrering. |
| Tid og udgift | 2370126 | Ikonerne for **Projektopgave** og **Rolle** er blevet opdaterede i objektet **Tidsregistrering**. |
| Tid og udgift | 2379879 | Korrigerede funktionen **Kopiér uge** i tidsregistreringen, når Dynamics 365 til telefon anvendes. |
| Fakturering og prisfastsættelse | 2371906 | Det samlede beløb på proformafakturaer må ikke kunne ændres i Project Operations for ressourcebaserede udrulninger. |
| Fakturering og prisfastsættelse | 2385802 | Løste den fejl, der opstår med negative faktiske timer, når projekttotaler opdateres. |
| Fakturering og prisfastsættelse | 2389675 | Forbedret funktionsmåde for bekræftelse af proformafaktura. Hvis et job skal køre længe, skal der tages højde for den aktivitet, der kræves for at skrive bekræftelsesresultater for regnskabet. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Oversigt over projektstyring og regnskab i Dynamics 365 Finance

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Rejser og udgifter | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | De beløb i leverandør- og momstransaktioner, der er bogført fra en omkostning, som blev oprettet på grundlag af en kreditkorttransaktion, er forkerte. |
| Rejser og udgifter | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Der oprettes de forkerte afstemningslinjer, når betalingskladden dannes. |
| Rejser og udgifter | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | De beløb i momstransaktioner, der er bogført fra en omkostning, som blev oprettet på grundlag af en kreditkorttransaktion, er forkerte. |
| Rejser og udgifter | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Det kan tage lang tid at slette en udgiftslinje. |
| Projektregnskab | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Når du anvender vidensbase 4619395, understøttes ændring af nummersekvensen til **Kontinuerlig** ikke, og når du bogfører et estimat, opstår følgende fejl: "Konfiguration af "kontinuerlig" nummerserie Proj_X understøttes ikke i systemet". |
| Projektregnskab | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Du kan muligvis ikke bogføre en leverandørfaktura ved hjælp af følgende fejlmeddelelse: "Transaktionerne på bilaget stemmer ikke pr. 5/17/2021. (regnskabsvaluta: 0,00 – rapporteringsvaluta: 0,01)." |
