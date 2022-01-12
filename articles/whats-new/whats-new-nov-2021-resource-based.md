---
title: Nyheder november 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Dette emne giver oplysninger om de kvalitative opdateringer, der er tilgængelige i november 2021-udgivelsen af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fb9dad5b04ef2933ed8a8d8211f888f13df5ba40
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942878"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder november 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

*Finder anvendelse for: Project Operations for ressource-/ikke-lagerbaserede scenarier*

Dette emne gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.26.0.145, 4.26.0.148, 4.26.0.150 og 4.26.0.155
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.22

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Følgende funktioner er omfattet af denne udgivelse:

- Grænseflader for programmering af projektplanlægningsprogrammer (API'er) understøtter nu muligheden for at oprette og slette projektgrupper.

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Der er ingen opdateringer til Project Operations-tilknytninger med dobbelt skrivning i denne udgivelse. Du kan få vist en aktuel liste og aktuelle versioner af Project Operations-tilknytninger med dobbelt skrivning i [Project Operations-versioner med tilknytning af dobbelt skrivning](/dynamics365/project-operations/environment/resource-dual-write-maps).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-in-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2240080 | Feltet **Betalingsbetingelser** må ikke duplikeres på proformafakturaen. |
| Fakturering og prisfastsættelse | 2358236 | Fakturakorrektion skal tillade rettelser, der har nulprislinjer. |
| Ressourcestyring | 2410072 | Tillad konfiguration af en ressource, der er tildelt opgaven, som projektleder. |
| Fakturering og prisfastsættelse | 2430234 | Løs et problem med beregning af omkostningseffektivitet. |
| Tid og udgift | 2436978 | Tillad, at klokkeslæt angives i formatet tt:mm. |
| Fakturering og prisfastsættelse | 2448623 | Tillad, at prislister opdateres, når de er tilknyttet en afdeling. |
| Tid og udgift | 2460396 | Tillad, at en tidsregistrering slettes ved at rydde cellen. |
| Fakturering og prisfastsættelse | 2467386 | Tillad, at et projekt, der har en opgave, slettes, også selvom opgaven er knyttet til et vundet tilbud. |
| Tid og udgift | 2461744 | Visningen **Min mislykkede godkendelse** viser kun projektgodkendelser i fasen **Indsendt**. |
| Tid og udgift | 2464082 | Fjern linket fra projektgodkendelser til den godkendelse, der blev angivet, når status for et mål sammenkædes. |
| Tid og udgift | 2468108 | I planlægningsjobbet skal der ikke angives status for **Behandling** af godkendelsessættet. |
| Tid og udgift | 2471503 | Slet godkendelsessæt, der er syv dage gamle. |
| Fakturering og prisfastsættelse | 2480687 | Tilbudslinjereferencen må ikke fjernes, når der oprettes en tilbudslinjemilepæl. |

### <a name="project-management-and-accounting-in-finance"></a>Oversigt over projektstyring og regnskab i Finance

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Projektstyring og regnskab | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Overførte leverandørbeløb i projektomkostningstransaktioner vises ikke på transaktionslisten. |
| Projektstyring og regnskab | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Den interne leverandørfaktura brydes, når integration af leverandørfakturaer slås til. |
| Projektstyring og regnskab | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Betalingsbetingelserne på projektfakturaer fungerer ikke som forventet. |
| Projektstyring og regnskab | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Når der frigives leverandørtilbageholdelse, indeholder bilagsbogføringen flere linjer, som ikke er korrekte. |
| Projektstyring og regnskab | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Når integrationskladden for Project Operations bogføres, lykkes det ikke på grund af manglende dimensioner for en konto, der ikke bogføres til. |
| Projektstyring og regnskab | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Fanen **Projekt** kan ikke redigeres på en afventende leverandørfaktura, når indkøbskategorien tildeles til varen. |
| Projektstyring og regnskab | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigationsruden mangler, hvis du ikke er logget på Project Operations Dataverse. |
| Projektstyring og regnskab | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Når du bogfører omsætning fra en projektfaktura i en anvendt tilbageholdelsessag, opstår der et problem, fordi transaktioner på bilaget ikke er afstemt. |
| Projektstyring og regnskab | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Oprettelse af et estimat, efter du har bogført et forslag til en faktura, blokerer korrektionslinjer fra importen. |
| Projektstyring og regnskab | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Det bør ikke være muligt at ændre en fuldt faktureret milepælspost. |
| Rejser og udgifter | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alle udgiftsrapporter er synlige, når du søger efter en kategori i mobilappen Udgift. |
| Rejser og udgifter | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Forkerte beløb i leverandørtransaktioner og momstransaktioner, der er bogført fra en udgift, som er oprettet på grundlag af en kreditkorttransaktion. |
| Rejser og udgifter | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Der vises en irrelevant advarsel, når du opdaterer siden **Udgiftsrapport**. |
| Rejser og udgifter | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Den forkerte midlertidige godkender bruges, når du sletter en midlertidig godkender og derefter indsender en udgiftsrapport igen via arbejdsprocessen. |
| Rejser og udgifter | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Der opstår en bogføringsfejl, der er relateret til konfigurationen af kilometertal. |
