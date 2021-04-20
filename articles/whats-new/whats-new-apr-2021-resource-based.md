---
title: Nyheder april 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Dette emne giver oplysninger om kvaliteten af de opdateringer, der er tilgængelige i april 2021-udgivelsen af Project Operations for ressource-/ikke-lagerbaserede scenarier.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867986"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder april 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

- Project Operations på Dataverse-miljø version 4.9.0.221
- Projektstyring og regnskab i Dynamics 365 Finance-miljø version 10.0.17

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Følgende funktioner er omfattet af denne udgivelse:

- Ikke-lagerbaserede materialer til projekter. Nøglefunktionerne omfatter:
  - Estimering og prisfastsættelse af ikke-lagerførte materialer under et projekts salgscyklus. Du kan finde flere oplysninger i [Konfiguration af omkostnings- og salgspriser for katalogprodukter – lille](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sporing af brugen af ikke-lagerførte materialer under projektlevering. Du kan finde flere oplysninger i [Registrér materialeforbrug på projekter og projektopgaver](../material/material-usage-log.md).
  - Fakturering af anvendte ikke-lagerførte materialeomkostninger. Du kan finde flere oplysninger under [Administrer faktureringsefterslæb](../proforma-invoicing/manage-billing-backlog.md).
- Opgavebaseret fakturering: Tilføjet muligheden for at knytte projektopgaver til projektkontraktlinjer og dermed underlægge dem samme faktureringsmetode, fakturahyppighed og kunder som dem på kontraktlinjen. Denne tilknytning sikrer, at nøjagtig fakturering, regnskab, estimeret omsætning og genkendelse fungerer i overensstemmelse med denne opsætning på projektopgaver.
- Nye API'er i Dynamics 365 Dataverse gør det muligt at oprette, opdatere og slette handlinger med **Planlægningsobjekter**. Du kan finde flere oplysninger under [Brug planlægnings-API'er til at udføre handlinger med planlægningsobjekter](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations i Dynamics 365 Dataverse

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2124532 | Knappen **Ret faktura** vises på en proformafaktura, når forskudsbeløbet eller det anvendte forskudsbeløb findes på den oprindelige faktura. Knappen vises kun i miljøer med Finance version 10.0.19 eller nyere. |
| Fakturering og prisfastsættelse | 2224568 | Logik tilføjet for at aktivere tilpasninger, der indebærer aktivering af plug-in'et til bekræftelse af faktura. |
| Fakturering og prisfastsættelse | 2101098 | Logikken i standardfelterne på en proformafaktura er blevet forbedret: **Faktureringsadresse**, **Fakturamodtagers navn** og **Betalingsbetingelser** bruges nu som standard fra den tilsvarende kundepost i projektkontrakten. |
| Fakturering og prisfastsættelse | 2021413 | Du kan opdatere felterne **Faktiske omkostninger** og **Salg** i objektet **Opgave**, så de inkluderer salgsværdier fra ikke-fakturerede og fakturerede udgifter på opgaver. |
| Fakturering og prisfastsættelse | 2182110 | Når du kopierer en projektkontrakt, gendannes kontraktlinje-id'et i destinationsprojektkontrakten for at sikre, at det er entydigt. |
| Styring af salgsmuligheder | 2186741 | Valideringer tilføjet for at sikre, at feltet **Oprindelse** og **Transaktionstype** ikke opdateres på eksisterende tilbudslinjedetaljer. |
| Styring af salgsmuligheder | 2191353 | Der må ikke oprettes milepæle på en tids- og materialekontraktlinje. |
| Styring af salgsmuligheder | 2216956 | Løst problemer med **Opdatér priser**. |
| Planlægning og sporing | 2182979 | Funktionen projektkopiering er forbedret for at sikre, at omkostningsestimatlinjer kopieres fra det oprindelige projekt. |
| Planlægning og sporing | 2184144 | Funktionen projektkopiering er forbedret for at sikre, at ressourcepositionsnavnet kopieres fra det oprindelige projekt. |
| Planlægning og sporing | 2184799 | Projektkopi: Strengere kontrol for at sikre, at den anslåede startdato ikke ændres, mens kopieringen er i gang. |
| Planlægning og sporing | 2185134 | Projektkopi: Den anslåede startdato for destinationsprojektet angives til dags dato. |
| Planlægning og sporing | 2196373 | Projektkopi: Sikrer, at projektleder- og teammedlemsposter ikke duplikeres i projektteamet. |
| Planlægning og sporing | 2211833 | Projektkopi: Ressourcetildelinger kopieres fra kildeprojektopgaven til destinationsprojektet. |
| Planlægning og sporing | 2186541 | Løste problemer i gitteret **Estimater**, når der grupperes efter ressource. |
| Planlægning og sporing | 2166906 | Transaktionskategorien fra en opgave skal kopieres til objektet **Ressourcetildeling**. |
| Ressourcestyring | 2125362 | Løste problemer med oprettelse af et generisk teammedlem ved hjælp af en timebaseret allokeringsmetode. |
| Tid og udgift | 2113603 | Løste det tilpasningsrelaterede problem med at fjerne attributter fra siden **Tidsregistrering**. Systemet kontrollerer nu, om attributten findes på siden, inden disse tilgås ved hjælp af et script. |
| Tid og udgift | 2204377 | Kopierede timesedler skal vises automatisk, når du vælger **Kopiér uge** i forbindelse med tidsregistrering. |
| Tid og udgift | 2209059 | Feltet **Status** kan redigeres med henblik på tidsregistrering i Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Oversigt over projektstyring og regnskab i Dynamics 365 Finance

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Projektstyring og regnskab | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminering af tilbageført estimat fungerer ikke i **Periodisk**.  |
| Projektstyring og regnskab | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Funktionen **Regnskabsmæssig justering** skaber et problem med konti i hovedbogen, hvor **Tillad ikke manuel registrering** er valgt. |
| Projektstyring og regnskab | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Tilføjede forretningslogik til behandling af rettelsesfakturaer, herunder forskudsbeløb eller anvendte forskudsbeløb. |
| Projektstyring og regnskab | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Bogføring af salgsværdien af igangværende arbejde i intern projektfakturering vælge en uventet konto. |
| Projektstyring og regnskab | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Når du arbejder med forskud i Project Operations, medfører ændringer af standardprojektet på en kontrakt, efter at forudbetalingerne er blevet faktureret, problemer på et senere tidspunkt med indgående fradrag. |
| Projektstyring og regnskab | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Hvis et projekt fjernes fra en kontrakt i Project Operations, bør standardprojektet i kontrakten nulstilles, hvis det er nødvendigt. |
| Projektstyring og regnskab | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | I Project Operations vises de forkerte udgiftslinjer i listen **Tilføj linje** på den interne faktura. |
| Projektstyring og regnskab | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | I Project Operations er siden **Købsaftale** ikke synlig i juridiske enheder i Finance, der er integreret med Project Operations. |
| Projektstyring og regnskab | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | På grund af en integrationsfejl i Dataverse kan du ikke konvertere et tilbud til vundet i Project Operations. |
| Projektstyring og regnskab | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** kan angive finansieringskildens fakturaadresse fra en anden kunde.  |
| Projektstyring og regnskab | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | I Project Operations vælges der ingen dimensioner, når du opretter en bogføringsfaktura for en transaktion. |
| Rejser og udgifter | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Saldoen for kontantforskud opdateres ikke for en udgiftsrapport, hvis den godkendes og bogføres linje for linje. |
| Rejser og udgifter | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Moms for udregnede interne udgiftsrapporter beregnes ikke korrekt. |
| Rejser og udgifter | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Der vises yderligere felter for projekter på den gendannede side **Interne udgiftsrapporter**. |
| Rejser og udgifter | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Der vises en forkert fejlmeddelelse i overskriftskvitteringerne for udgiftsrapporter. |
| Rejser og udgifter | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | En udgiftsrapport bogføres forkert i et internt scenario, hvis momsen er bogført på den juridiske destinationsenhed. |
| Rejser og udgifter | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Datoerne for indsendelse af rapporter udskrives ikke på godkendte udgiftsrapporter. |
| Rejser og udgifter | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Felterne **Godkendelsesdato** og **Afvisningsdato** udfyldes ikke, når en omkostning er godkendt. |
| Rejser og udgifter | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | En rejserekvisition, der er oprettet for én arbejder, kan bruges til en anden arbejders udgiftsrapport. |
| Rejser og udgifter | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Udgiftskategorier er låst, når du tilføjer en ny udgiftslinje. |
| Rejser og udgifter | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Hvis du opdeler en allerede opdelt udgiftsrapportlinje, resulterer det i en ufuldstændig bogføring af bilagene Kreditor\Finansposter og ødelægger regnskabskildeoversigten, da **TRVEXPTRANS.SOURCEDOCUMENTLINE** duplikeres. |
| Rejser og udgifter | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Politikken for rejserekvisition fungerer ikke som forventet. |
| Rejser og udgifter | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Navnet på leverandørkontoen vises ikke på bogførte projekttransaktioner for udgiftsrapporter. |
| Rejser og udgifter | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | I Project Operations kan du ikke godkende tid med en opgave for et internt projekt. |
| Rejser og udgifter | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Tilbageførelseskategorien for kontantforskud opdaterer ikke saldi for kontantforskud, når den bogføres. |
| Rejser og udgifter | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Salgsprisen beregnes forkert på udgiftsrapporter, der er oprettet i en udenlandsk valuta ved hjælp af importerede kreditkorttransaktioner, og som er knyttet til et projekt. |
| Rejser og udgifter | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Dataobjektet **TrvRequisitionLine** og det tilknyttede entydige indeks er blevet rullet tilbage. |
| Rejser og udgifter | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Instrumentering til generation af **SOURCEDOCUMENTLINE** er blevet tilføjet. |
| Rejser og udgifter | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Den forkerte underkontokladde vises i et internt scenario, hvis momsen er bogført på den juridiske destinationsenhed. |
| Rejser og udgifter | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | I Project Operations slettes udgiftsestimater ikke fra Finance, når de slettes i Dataverse. |
| Rejser og udgifter | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Når en udgiftskategori er en ikke-projektkategori, kopieres de økonomiske dimensioner, der er valgt på siden **Udgifter**, ikke til udgiftsrapporten. |
