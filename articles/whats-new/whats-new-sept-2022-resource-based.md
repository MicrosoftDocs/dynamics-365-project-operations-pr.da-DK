---
title: Nyheder september 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel giver oplysninger om de kvalitative opdateringer, der er tilgængelige i september 2022-udgivelsen af Microsoft Dynamics 365 Project Operations til ressource/ikke-lagerbaserede scenarier.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621220"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder september 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.46.0.60
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.29

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

| Funktionsområde | Funktionsnavn | Mere information |
| --- | --- | --- |
| Styring af salgsmuligheder | **Revision og aktivering af tilbud**<br>Project Operations understøtter salgsprocessen fuldt ud. Projekttilbud kan aktiveres til at repræsentere en tilstand, hvor tilbuddet er skrivebeskyttet og under gennemsyn. Aktiverede tilbud kan revideres for at oprette nye tilbud med et trinvist stigende revisionsnummer. Aktiverede projekttilbud eller tilbudsrevisioner kan lukkes som vundne eller tabte. | [Aktivere og revidere et projekttilbud](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturering og prisfastsættelse | **Standardpris for tidszoneagnostik**<br>Project Operations har introduceret begrebet "tidszoneagnostik" på alle faktiske projektdatoer. Et nyt felt, **Transaktionsdato**, er nu tilgængeligt på kladdelinjer og faktiske poster og bruges til at gemme den dato, hvor transaktionen fandt sted, men uden at konvertere denne dato til Coordinated Universal Time. Denne dato bruges til downstreamprocesser, f.eks. standardpriser og oprettelse af fakturaer. | <p>[Fastsætte omkostningssatser for projektbaserede estimater og faktiske værdier](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Fastsætte salgspriser for projektbaserede estimater og faktiske værdier](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Fakturering og prisfastsættelse | **Gældende pristilsidesættelser for dato i Project Operations**<br>Gældende pristilsidesættelser for dato giver mulighed for at tilsidesætte eller ændre bestemte priser på prislisten. | [Gældende pristilsidesættelser for dato](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Underentrepriser | **Afstemning af underentreprise- og leverandørfaktura**<br>Denne funktion gør det muligt for kunder at oprette underentrepriser for at købe ressourcetid, udgiftskategorier og materiale, der bruges til projektarbejde. Det gør det også muligt for kunder at registrere – i programmer til finans og drift – leverandørfakturaer, der vil være tilgængelige for projektledere i Dataverse i forbindelse med verificering. | <p>[Administration af underentrepriser](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Oprette leverandørfakturaer](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tid og udgift | **Global godkender**<br>Denne funktion aktiverer uafhængig softwareleverandør og central godkendelse, uanset projekt- eller teammedlemmets status i projektet. | [Sikkerhed og godkendelser](/dynamics365/project-operations/approvals/approvals-security) |
| Udgiftsstyring | **Mulighed for at bogføre udgifter i leverandørvaluta**<br>Denne funktion gør det muligt at bogføre udgiftsrapporter i leverandørens valuta for kontantbetalingsmetoden. | [Mulighed for at bogføre udgifter i leverandørvaluta](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektindkøb | **Betal ved betaling for betalinger til leverandører**<br>Ved hjælp af denne funktion kan funktionen Betal ved betaling (PWP) bruges sammen med ikke-lagerbaserede Project Operations-miljøer. Det gør det muligt at blokere/bevare kreditorbetalinger på basis af vilkår for tilbageholdelse, indtil betaling modtages fra kunden. | [Betal ved betaling for betalinger til leverandører](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektindkøb | **Indkøbsrekvisitioner for projekt**<br>Denne funktion giver brugere mulighed for at oprette projektrelaterede købsordrer i juridiske enheder, hvor integration af Project Operations i Dynamics 365 Customer Engagement er aktiveret. Projektindkøbsordrer kan bruges til at registrere indkøb af ikke-lagermateriale i forhold til projektet af indkøbsafdelingen. Projektindkøbsordrer synkroniseres ikke med Dataverse. Men du kan bruge et virtuelt objekt til at få vist projektindkøbsordrelinjer i Dataverse for at få oplysninger om projektlederen. Projektrelaterede omkostninger til leverandørfakturaer er integreret i objektet Projektets faktiske værdier i Dataverse. Projektomkostninger registreres i projektets hovedbog ved hjælp af integrationskladden til Project Operations. | |

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Følgende tabel viser de tilknytninger med dobbelt skrivning, der er ændret eller tilføjet i Project Operations-versionen fra september 2022.

| Objekttilknytning | Opdateret version | Kommentarer |
| -------------- | ------------------- | ------------|
| Integration af faktiske oplysninger i Project Operations (msdyn_actuals) | 1.0.0.15 | Denne tilknytning understøtter den faktiske behandling af underleverandører med Project Operations til ressourcebaserede scenarier. |
| Integrationsobjekt for eksport af projektleverandørfaktura i Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Denne tilknytning understøtter den faktiske behandling af underleverandører med Project Operations til ressourcebaserede scenarier. |
| Integrationsobjekt for eksport af projektleverandørfakturalinje i Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Denne tilknytning understøtter den faktiske behandling af underleverandører med Project Operations til ressourcebaserede scenarier. |

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2754422 | Materiale- og udgiftsestimater overføres ikke til Finance, når projekter kopieres til Dataverse. |
| Tid og udgift | 2787409 | En ikke-gyldig godkender kan godkende en tidspost, der ikke er fra et projekt. |
| Styring af salgsmuligheder | 2788907 | Opdateret fejlmeddelelse om entydig validering af ordrelinjer, der indeholder flag. |
| Tid og udgift | 2842253 | Håndtering af null-undtagelse i forbindelse med tidsgodkendelse. |
| Fakturering og prisfastsættelse | 2844181 | Hvis korrelations-id'et ikke hentes, blokeres der for oprettelse af fakturaen. |
| Fakturering og prisfastsættelse | 2876628 | QLD, CLD – Estimeret prislisteløsning skal bruge ældre datointervalfelter for prislisten. |
| Underentrepriser | 2893222 | Hvis der ikke er angivet en rolle for en linje i underentrepriseaftalen, bør det være muligt at vælge den pågældende linje på et gruppemedlem for en hvilken som helst rolle. |

### <a name="project-management-and-accounting-in-finance"></a>Oversigt over projektstyring og regnskab i Finance

Du kan få flere oplysninger om de fejlrettelser, der er inkluderet i denne opdatering, ved at logge på Microsoft Dynamics Lifecycle Services og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktioner, der som standard slået til i den kommende udgivelse

I følgende tabel vises de funktioner, der som standard er slået til i version 10.0.30. De fleste funktioner, der automatisk er slået til, kan slås fra i [Funktionsstyring](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). I fremtiden kan nogle funktioner, der er blevet slået til automatisk, blive fjernet fra Funktionsadministration og blive obligatoriske. Denne ændring sikrer, at kunderne bruger den aktuelle funktionalitet, så forbedringerne kan bygge på den aktuelle funktionalitet, efterhånden som de tilføjes. Funktioner aktiveres aldrig automatisk på under et år, medmindre de antages at være afgørende.

| Funktionsnavn | Dato for aktivering | Tilføjet funktion | Funktionstilstand | Modul |
| --- | --- | --- |--- |--- |
| Aktivér asynkron handling, når brugeren skal skifte mellem synkrone og asynkrone handlinger | 21. oktober 2022 | 9. april 2021 | Til som standard | Udgiftsstyring |
| Evaluering af udgiftspolitik for påkrævede kvitteringer | 21. oktober 2022 | 20. december 2021 | Til som standard | Udgiftsstyring |
| Listevisning af udgiftsrapporter, der er oprettet af delegerede medarbejdere | 21. oktober 2022 | 19. februar 2020 | Til som standard | Udgiftsstyring |
| Beregning af totaler for kilometertal efter regnskabsår | 21. oktober 2022 | 10. maj 2022 | Til som standard | Udgiftsstyring |
