---
title: Nyheder maj 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i maj 2021-udgivelsen af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930403"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder maj 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Dynamics 365 Project Operations:

- Project Operations på Dynamics 365 Dataverse-miljø version 4.10.0.186
- Projektstyring og regnskab i programmiljøer til programmer til finans og drift version 10.0.18

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Følgende funktioner er omfattet af denne udgivelse:

- [Planlægningstilstande](../project-management/scheduling-modes.md): Projektledere kan definere, om et projekt skal administreres ved hjælp af planlægningstilstanden fast varighed, fast arbejde eller faste enheder.
- [Konfigurer kilometertal ved hjælp af niveauer for kilometertal](../expense/set-up-mileage.md): Opdater niveauerne for kilometertal for medarbejderens udgiftsrapporter.

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

På følgende liste vises de dobbeltskrivning-tilknytninger, der er blevet ændret eller tilføjet i frigivelsen til Project Operations fra maj 2021.

| Objekttilknytning | Opdateret version | Kommentarer |
| --- | --- | --- |
| Projektfinansieringskilde (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Synkronisering af betalingsvilkår for projektkontraktkunder. |
| Projektfakturaforslag V2 (fakturaer) | 1.0.0.3 | Synkronisering af betalingsvilkår for proformafakturaer. |
| Integrationsobjekt for eksport af projektleverandørfakturalinje i Project Operations (msdyn\_projektleverandørlinjer) | 1.0.0.1 | Kvalitetsopdateringer |
| Projekter V2 (msdyn\_projekter) | 1.0.0.2 | Kvalitetsopdateringer |

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og løsningen til programmer til finans og drift. Visse funktioner fungerer muligvis ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan se den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbelt skrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har brugertilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på et problem, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner på tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2227635 | Værdierne i felterne **Enhedsgruppe** og **Enhed** anvendes som standard fra produktet i gitteret **Materialeestimater**. |
| Fakturering og prisfastsættelse | 2234127 | Feltet **Opgave-id** integreres nu korrekt med faktiske værdier i Dataverse-projekter, når en leverandørfaktura bogføres. |
| Fakturering og prisfastsættelse | 2235564 | Hvis du gemmer kladdelinjen, sikrer du, at den valuta, der vises i kladdelinjeposten, tilpasser standardvalutaen til linjen efter lagringen. |
| Fakturering og prisfastsættelse | 2246671 | Hvis du gør en transaktion ikke-fakturerbar under fakturering, tilbageføres den oprindelige ikke-fakturerede salgspost, og der oprettes en ny ikke-faktureret salgspost som ikke-faktureret. |
| Fakturering og prisfastsættelse | 2264042 | Gyldig fakturarettelse må ikke blokeres, hvis der eksisterer en detalje om fakturarettelser, som ikke er gyldig i miljøet. |
| Fakturering og prisfastsættelse | 2146367 | Tilknytning af projektfakturaoverskrift med dobbelt skrivning udvides til at omfatte betalingsvilkår. |
| Styring af salgsmuligheder | 2086888 | Tilføj ikke roller og kategorier, der er deaktiveret, før du kopierer et tilbud til fakturerbare roller og kategorier i et nyligt kopieret tilbud. |
| Styring af salgsmuligheder | 2234376 | Skrivebeskyttede felter er nedtonet i gitteret **Materialeestimater**. |
| Styring af salgsmuligheder | 2238337 | Et tilbud, der er baseret på en kontakt, kan gemmes, selvom det ikke er knyttet til en projektprisliste. |
| Styring af salgsmuligheder | 2239810 | Hvis du lukker et tilbud som tabt, lukkes det tilknyttede projekt også, og eventuelle reservationer annulleres. |
| Projektplanlægning og -sporing | 2099559 | Tilføjede yderligere valideringer for systemets tilstand, før gitteret **Projektopgaver** åbnes. |
| Projektplanlægning og -sporing | 2178987 | Løst en midlertidig fejl, der opstår, når du vælger **Næste fase** på siden **Projekt**. |
| Ressourcestyring | 2224817 | Funktionaliteten til at udvide reservationer angives som standard til den korrekte reservationsstatus. |
| Tidsregistrering | 2202476 | På siden **Tidsregistrering** bruges nu reaktiv gitterkontrol og løser problemer såsom fejljustering af gitre. |
| Tidsregistrering | 2223377 | Tidsregistrering er skjult i sektionen **Relateret** på siden **Reserverbar ressource** for at undgå forvirring om anvendelighed. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Project Management and Accounting i Dynamics 365 Finance

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Projektstyring og regnskab | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations til ressourcebaserede scenarier: Kan ikke konvertere tilbud til vundet på grund af en integrationsfejl. |
| Projektstyring og regnskab | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Der opstår en fejl, når du forsøger at knytte en kontraktlinje til et projekt-id på grund af kontrollen af overlappende kontraktlinjer og transaktionstyper. |
| Projektstyring og regnskab | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** angiver finansieringskildens fakturaadresse fra en anden kunde. |
| Rejser og udgifter | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Der kan opstå en bogføringsfejl, som relaterer sig til konfigurationen af kilometertal. |
| Rejser og udgifter | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funktionaliteten **Opdeling til personlig** virker ikke for transaktioner med udenlandske valutaomkostninger. |
| Rejser og udgifter | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Værdierne i rullemenuen for udgiftskategorier viser forkerte kategorier for stedfortrædere, uanset om de er konfigureret som en ressource. |
| Rejser og udgifter | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Du kan ikke gemme en intern udgiftsrapport på grund af en fejl i **Ressource/kategorivalidering**. |
| Rejser og udgifter | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Den forkerte beregning af kilometertal i omkostningsrapportbogføring har opdelt linjer. |
| Rejser og udgifter | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Du kan ikke bogføre en intern udgiftsrapport, når moms inkluderes, og mellemregningskontotypen i betalingsmetoden er **Arbejder**. |
| Rejser og udgifter | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Opdatering af dataobjektet **TrvRequisitionLine** og det tilknyttede entydige indeks er blevet annulleret. |
| Rejser og udgifter | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Udgiftsrapport understøtter oprettelse og opdatering af kildedokumentlinjer. |
| Rejser og udgifter | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Der vises en forkert underkontokladde i et internt scenario, hvis momsen er bogført på den juridiske destinationsenhed. |
| Rejser og udgifter | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Udgiftsestimatet slettes ikke fra Finance, når det slettes fra Dataverse. |
| Rejser og udgifter | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Når udgiftskategorien er en ikke-projektkategori, kopieres de økonomiske dimensioner, der er valgt på siden **Udgifter**, ikke til udgiftsrapporten. |
