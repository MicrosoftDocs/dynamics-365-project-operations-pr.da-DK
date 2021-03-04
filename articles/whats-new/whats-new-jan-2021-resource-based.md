---
title: Nyheder januar 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Dette emne indeholder oplysninger om de kvalitetsopdateringer, der er tilgængelige i udgivelsen i januar 2021 af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24a6f3b49b9c67b7c2d97461ab0f23a9a704dbc7
ms.sourcegitcommit: ef7d498bf80b0bcc1245dc42f30c410c31f891bb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/13/2021
ms.locfileid: "4958899"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder januar 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_


Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

  - Project Operations på Dataverse-miljø version 4.6.0.154
  - Projektstyring og regnskab i Dynamics 365 Finance-miljø version 10.0.16

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| **Udrulning og konfiguration** | 2106818 | Løste omdøbningen af webkilden, der forårsagede problemer i forbindelse med tilpasningen af en side. |
| **Fakturering og prisfastsættelse** | 2091908 | Løste synligheden af indstillingerne **Lås prissætningen** og **Brug gældende prisfastsættelse** på siden **Faktura**, når Project Operations installeres sammen med Dynamics 365 Field Service. |
| **Fakturering og prisfastsættelse** | 2103058 | Opdaterede **Projekttotaler** for at håndtere null-værdier for de faktiske omkostninger for en opgave. |
| **Fakturering og prisfastsættelse** | 2116100 | Forbedrede fejlmeddelelser, der bruges sammen med funktionaliteten **Ret registreringer på faktiske**. |
| **Fakturering og prisfastsættelse** | 2116129 | Forbedret synlighed for udgiftsestimimater på fanen **Estimater** på siden **Projekter**. |
| **Fakturering og prisfastsættelse** | 2119112 | Løste sammenlægning af faktiske salgsværdier og faktiske omkostninger, når der bruges forskellige valutakurser. |
| **Fakturering og prisfastsættelse** | 2134705 | Rettet fejlen "Kan ikke læse egenskaben **getResourceString** af udefinerede", når siden **Fakturaen** åbnes, og Field Service er installeret. |
| **Styring af salgsmuligheder** | 2022195 | Det opgavebaserede faktureringsgitter på siden **Projekt** indeholder et ikon, der angiver, at der er knyttet en kontrakt eller tilbudslinje til den pågældende opgave. |
| **Styring af salgsmuligheder** | 2029135 | Løste den forretningsprocesfejl, der opstår, når en bruger forsøger at åbne en fakturalinje på en bekræftet faktura, hvor der er faktureret et forskud. |
| **Styring af salgsmuligheder** | 2040713 | Løste den scriptfejl, der opstår under oprettelse af en faktura ud fra en kontrakt, og Field Service er installeret. |
| **Projektplanlægning og -sporing** | 2090202 | Markerede forretningsregler, der ikke længere bruges, som **Frarådet**. |
| **Tid og udgift** | 2091249 | Strammede op på kontroller, som brugerne ikke kan ændre opgaven på en indsendt eller godkendt tidsregistrering. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Oversigt over projektstyring og regnskab i Dynamics 365 Finance

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| **Projektstyring og regnskab** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Der findes et forkert kontraktbeløb på siden **Aconto** for et fastprisprojekt med flere finansieringskilder. |
| **Projektstyring og regnskab** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Pladsholderen **Invoiceproposal.PSAnfRefProjId** viser ikke projekt-ID'et for arbejdsprocessen **Gennemse forslag til projektfaktura**. |
| **Projektstyring og regnskab** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Den forkerte kontaktrabatdato bruges, når projektfakturaforslag bogføres. |
| **Projektstyring og regnskab** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Fjernelse og læsning af ressourcetildelinger i Project Operations fordobler projektprognoseposterne i Finance. |
| **Projektstyring og regnskab** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | I Project Operations kan du ikke oprette projektestimater i Dataverse uden at have en kontraktlinje i projektet. |
| **Projektstyring og regnskab** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Den økonomiske dimension i en projektomkostningstransaktion synkroniseres ikke med det relaterede bilag og regnskabsfordelingen i udgiftsrapporten, når omkostningerne bogføres på balancen. |
| **Projektstyring og regnskab** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filteret **Fakturastatus** for bogførte projekttransaktioner for fastprisprojekter virker ikke. |
| **Projektstyring og regnskab** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Omvendt estimateudelukkelse fungerer ikke i afsnittet **Periodisk**. |
| **Projektstyring og regnskab** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Fakturaforslagslinjer kan slettes i Project Operations, når det integreres med Dataverse. |
| **Projektstyring og regnskab** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Forebyg aktivering af funktionen for flere kontraktlinjer uden integration af Dataverse. |
| **Projektstyring og regnskab** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Når acontofakturering er lig med fortjeneste og tab, vises den fakturerede omsætning som nul på overslagssiden. |
| **Projektstyring og regnskab** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Fakturarettelser fungerer ikke i integrerede miljøer. |
| **Projektstyring og regnskab** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Når salgsværdien af igangværende arbejde bogføres i intern projektfakturering, vælges den forkerte konto. |
| **Projektstyring og regnskab** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | I Project Operations kan afhængigheder af estimatopgaver i Dataverse ikke opdateres. |
| **Projektstyring og regnskab** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Hvis du sletter integrationskladder i Project Operations flere gange i Finance, medfører dette tab af data. |
| **Projektstyring og regnskab** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Der opstår følgende fejl i forbindelse med bogføring af et forslag til projektfaktura: "Transaktion stemmer ikke overens med rapporteringsvalutaen, når den fratrukne forskudsfaktura tilføjes". |
| **Projektstyring og regnskab** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Det forkerte projekt-ID inkluderes i fratrukkede beløb, når standardprojektkontrakten er blevet opdateret i Project Operations. |
| **Projektstyring og regnskab** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Anslået omsætning og omsætningsgenkendelse kan ikke fuldføres, når Project Operations er aktiveret. |
| **Projektstyring og regnskab** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Når du fjerner et projekt fra en kontrakt i Project Operations, nulstilles standardprojektet ikke i kontrakten. |
| **Projektstyring og regnskab** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | I Project Operations vises de forkerte udgiftslinjer på en intern faktura i listen **Tilføj linje**. |
| **Rejser og udgifter** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Udgiftslinjer kan ikke bogføres, fordi tidsopsætningen mangler på kontraktlinjen. |
| **Rejser og udgifter** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Når validering af et projekt/en kategori er obligatorisk, er de udgiftskategorier, der er knyttet til projektet, ikke synlige i udgiftsrapporten. |
| **Rejser og udgifter** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Kontantforskuddet opdateres ikke, når en udgiftsrapport bogføres efter linje. |
| **Rejser og udgifter** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Jobbet **Opdater betalingsoplysninger** mislykkes, når afstemninger tilbageføres, hvis en faktura blev afstemt med to eller flere betalingstransaktioner. |
| **Rejser og udgifter** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Der er et problem med beregningen af måltidsreduktion i diæter for udgiftskategori for diæter. |
| **Rejser og udgifter** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Rapporten **Udgiftstype pr. medarbejder** viser ikke udgifter pr. varer, hvis en brugers første forbindelse var på sproget es-MX. |
| **Rejser og udgifter** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Leverandørens betaling for en faktura i en udgiftsrapport bruger den forkerte oversigtskonto til at bogføre afstemning. |
| **Rejser og udgifter** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Når en udgiftsrapport bogføres med **Tillad gruppering af transaktioner baseret på modkonto til betaling** og **Korrigering af regnskabsdato ved bogføring** aktiveret, er regnskabsdatoerne ikke grupperet i tabellen **Regnskabsfordeling**, hvilket har indflydelse på momsposterne. |
| **Rejser og udgifter** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Tilknytning af udgiftsunderkategori fjernes, når afkrydsningsfeltet "Brug i udgifter" fjernes og derefter markeres igen. |
| **Rejser og udgifter** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Der kan ikke oprettes en intern udgiftsrapport, hvis projekt-id'et er tilføjet på overskriftsniveau. |
| **Rejser og udgifter** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Der er et problem med udgiftsbetalinger, når udgiftsbeløbet er større end beløbet for kontantforskud. |
| **Rejser og udgifter** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Feltet **Projekt-ID** i en intern udgiftsrapport er tom, hvis brugerrollen er knyttet til en bestemt organisation. |
| **Rejser og udgifter** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Udgiftskategorien er låst, når der tilføjes en ny udgiftslinje. |
| **Rejser og udgifter** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Hvis du specificerer udgiftsrapportlinjer efter varer, der allerede er opdelt, resulterer det i et ufuldstændigt bogføringsbilag for kreditor\hovedbog. På grund af duplikeringen af **TRVEXPTRANS.SOURCEDOCUMENTLINE**, er søgningen af regnskabskilden også forkert. |
| **Rejser og udgifter** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Det indeks, der tilføjes i tabellen **TRVREQUISITIONLINE**, som kunden har dupletter for, resulterer i en fejl under opgraderingen. |
| **Rejser og udgifter** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | I Project Operations kan tid med interne opgaver i Dataverse ikke oprettes eller godkendes. |

## <a name="regulatory-updates"></a>Lovgivningsmæssige opdateringer

Du kan finde oplysninger om lovgivningsmæssige opdateringer til Finance and Operations-apps under [Lovgivningsmæssige opdateringer](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på LCS og få vist de planlagte lovgivningsmæssige opdateringer ved hjælp af værktøjet til fejlsøgning. Fejlsøgning giver dig mulighed for at søge efter land, funktionstype og udgivelse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]