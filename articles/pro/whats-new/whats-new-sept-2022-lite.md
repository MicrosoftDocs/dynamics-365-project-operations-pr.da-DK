---
title: Nyheder i september 2022 – Project Operations lille udrulning
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i september 2022-udgivelsen af Microsoft Dynamics 365 Project Operations lille udrulning.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634845"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Nyheder i september 2022 – Project Operations lille udrulning

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.46.0.60

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

| Funktionsområde | Funktionsnavn | Mere information |
| --- | --- | --- |
| Styring af salgsmuligheder | **Revision og aktivering af tilbud**<br>Project Operations understøtter salgsprocessen fuldt ud. Projekttilbud kan aktiveres til at repræsentere en tilstand, hvor tilbuddet er skrivebeskyttet og under gennemsyn. Aktiverede tilbud kan revideres for at oprette nye tilbud med et trinvist stigende revisionsnummer. Aktiverede projekttilbud eller tilbudsrevisioner kan lukkes som vundne eller tabte. | [Aktivere og revidere et projekttilbud](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturering og prisfastsættelse | **Standardpris for tidszoneagnostik**<br>Project Operations har introduceret begrebet "tidszoneagnostik" på alle faktiske projektdatoer. Et nyt felt, **Transaktionsdato**, er nu tilgængeligt på kladdelinjer og faktiske poster og bruges til at gemme den dato, hvor transaktionen fandt sted, men uden at konvertere denne dato til Coordinated Universal Time. Denne dato bruges til downstreamprocesser, f.eks. standardpriser og oprettelse af fakturaer. | <p>[Fastsætte omkostningssatser for projektbaserede estimater og faktiske værdier](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Fastsætte salgspriser for projektbaserede estimater og faktiske værdier](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Fakturering og prisfastsættelse | **Gældende pristilsidesættelser for dato i Project Operations**<br>Gældende pristilsidesættelser for dato giver mulighed for at tilsidesætte eller ændre bestemte priser på prislisten. | [Gældende pristilsidesættelser for dato](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tid og udgift | **Global godkender**<br>Denne funktion aktiverer uafhængig softwareleverandør og central godkendelse, uanset projekt- eller teammedlemmets status i projektet. | [Sikkerhed og godkendelser](/dynamics365/project-operations/approvals/approvals-security) |
|Projektplanlægning og -sporing|**Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter** </br> </br>API'en til konturredigering af ressourcetildelinger gør det muligt for udviklere at angive en opgavetildelingsindsats via programmering på tværs af alle understøttede datointervaller for planlægning af en mere detaljeret tidsfasedelt indsats.|[Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kvalitetsopdateringer

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2754422 | Materiale- og udgiftsestimater overføres ikke til Dynamics 365 Finance, når projekter kopieres til Dataverse. |
| Tid og udgift | 2787409 | En ikke-gyldig godkender kan godkende en tidspost, der ikke er fra et projekt. |
| Styring af salgsmuligheder | 2788907 | Opdateret fejlmeddelelse om entydig validering af ordrelinjer, der indeholder flag. |
| Tid og udgift | 2842253 | Håndtering af null-undtagelse i forbindelse med tidsgodkendelse. |
| Fakturering og prisfastsættelse | 2844181 | Hvis korrelations-id'et ikke hentes, blokeres der for oprettelse af fakturaen. |
| Fakturering og prisfastsættelse | 2876628 | QLD, CLD – Estimeret prislisteløsning skal bruge ældre datointervalfelter for prislisten. |
| Underentrepriser | 2893222 | Hvis der ikke er angivet en rolle for en linje i underentrepriseaftalen, bør det være muligt at vælge den pågældende linje på et gruppemedlem for en hvilken som helst rolle. |
