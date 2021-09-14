---
title: Nyheder august 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Dette emne indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i august 2021-udgivelsen af Project Operations for ressourcebaserede/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cd5a7e74fc90c6138cd672ff6109b59a8d2ae916
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323454"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder august 2021 - Project Operations for ressource-/ikke-lagerbaserede scenarier

*Finder anvendelse for: Project Operations for ressource-/ikke-lagerbaserede scenarier*

Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

   - Project Operations i Microsoft Dataverse-miljø version 4.13.0.152.
   - Projektstyring og regnskab i Dynamics 365 Finance-miljø version 10.0.20.

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Følgende funktioner er omfattet af denne udgivelse:

- **Godkendelsessæt**: Ved godkendelse angives gruppetids-, udgifts- eller materialebrugsgodkendelsesanmodninger samlet i mindre undersæt af handlinger. Denne gruppering gør det muligt at behandle godkendelser i en bestemt ordre efter projekt, og gør nye forsøg og sekvensering muligt. Når anmodningerne grupperes, forbedres pålideligheden og sporingen af godkendelsesbehandlingen for store mængder godkendelser. Du kan finde flere oplysninger under [Godkendelsessæt](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

Der er ingen opdateringer til Project Operations tilknytninger med dobbeltskrivning i denne udgivelse. 

Du kan få vist en aktuel liste og aktuelle versioner af Project Operations-tilknytninger med dobbelt skrivning i [Project Operations-versioner med tilknytning af dobbelt skrivning](../environment/resource-dual-write-maps.md).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Visse funktioner fungerer muligvis ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan se den aktive version af tilknytningen på siden **Dobbelt skrivning** i kolonnen **Version**. Aktivér en ny version af tilknytningen ved at vælge **Tabeltilknytningsversioner** og dernæst vælge den nyeste version samt gemme den valgte version. Hvis du har brugertilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du begynder at tilknytte, skal du følge instruktionerne i sektionen [Problemer med mangler tabelkolonner på tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i vejledningen til fejlfinding af dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2295625 | Milepælsnavnet skal kopieres fra fakturaplanen til fakturalinjedetaljer. |
| Fakturering og prisfastsættelse | 2316323 | Rabatten bør ikke kunne redigeres på en proformafaktura i Project Operations for ressourcebaserede scenarier. |
| Styring af salgsmuligheder | 2338619 | Forretningsregler for **Salgsmulighed** og **Tilbud** skal kun fremgå af sider. |
| Ressourcestyring | 2316523 | Brugen af **Send anmodning** fra et ressourcekrav, der har en tilknyttet rolle, bør ikke vise en fejl. |
| Ressourcestyring | 2326885 | Hvis du opretter et ressourcekrav via et projekt, må der ikke vises en fejl. |
| Tid og udgift | 2335584 | Frarådede opgaveprocesser i tidsregistreringen. |
| Tid og udgift | 2336884 | Knappen for tidsregistreringen **Kopiér uge** skal fungere for mere end kun den aktuelle bruger. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Oversigt over projektstyring og regnskab på Dynamics 365 Finance

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Rejser og udgifter | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Beløbene for forkerte leverandørtransaktioner og salgsmomstransaktioner bogføres, når der oprettes en udgift fra en kreditkorttransaktion. |
| Rejser og udgifter | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Når betalingskladden oprettes, oprettes der forkerte afstemningslinjer. |
| Rejser og udgifter | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Beløbene for salgsmomstransaktioner bogføres, når der oprettes en udgift fra en kreditkorttransaktion. |
| Rejser og udgifter | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Det kan tage lang tid at slette en udgiftslinje. |
| Projektregnskab | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Systemet understøtter ikke konfigurationen af løbende nummersekvenser, når du bogfører et estimat efter anvendelse af KB 4619395. |
| Projektregnskab | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Bogføring af leverandørfaktura lykkes muligvis ikke med fejlmeddelelsen "Der er ingen modpost til transaktionerne på bilaget pr. 17.05.2021. (regnskabsvaluta: 0,00 – rapporteringsvaluta: 0,01)" |
