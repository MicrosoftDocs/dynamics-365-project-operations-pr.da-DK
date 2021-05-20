---
title: Versioner af Project Operations med dobbeltskrivning
description: Dette emne indeholder den liste over dobbeltskrivning-tilknytninger, der kræves i Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938965"
---
# <a name="project-operations-dual-write-map-versions"></a>Versioner af Project Operations med dobbeltskrivning

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Brug af Dynamics 365 Project Operations til ressource/ikke-lagerførte scenarier kræver, at der kører et sæt dobbeltskrivning-tilknytninger i miljøet. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Forudsatte tilknytninger: løsning med dobbeltskrivningsorganisering

Følgende tilknytninger er nødvendige forudsætninger for løsningen Project Operations. Sørg for at køre de tilknytninger, der er anført i følgende tabel, og eventuelle relaterede tabelkort i dit miljø.

| Tabeltilknytning | Første synkronisering |
| --- | --- |
| Hovedbog (msdyn_ledgers) | Kræver oprindelig synkronisering for tabeltilknytningen og alle forudsætninger. Master for første synkronisering er Finance and Operations-apps. |
| Juridiske enheder (cdm_companies) | Ikke påkrævet. Systemet udfylder automatisk dette objekt, når der tilknyttes miljøer ved hjælp af dobbelteskrivningsmiljøer. |
| Kunder V3 (konti) | Kræves ikke til klargøring. |
| Leverandører V2 (msdyn_vendors) | Kræves ikke til klargøring. |

1. Markér listet med tilknytninger, vælg tilknytningen for hovedbog **(msdyn\_ledgers)** med alle forudsætninger, og markér afkrydsningsfeltet **Oprindelig synkronisering**. I feltet **Master for oprindelig synkronisering** skal du vælge **Finance and Operations-apps** til både hovedbogstilknytning og alle nødvendige tilknytninger. Vælg **Kør**.

![Synkronisering af tilknytning i hovedbog](media/DW6.png)

1. Benyt samme fremgangsmåde for alle de resterende tabeltilknytninger, der er angivet i ovenstående tabel. Markér ikke afkrydsningsfeltet **Oprindelig synkronisering**, når du kører disse tilknytninger.

## <a name="project-operations-dual-write-maps"></a>Project Operations med dobbeltskrivning-tilknytninger

Følgende tilknytninger er nødvendige for en løsning med Project Operations.

| **Objekttilknytning** | **Seneste version** | **Første synkronisering** |
| --- | --- | --- |
| Integrationsobjekt for projekttransaktionsrelationer (msdyn\_transaktionsforbindelser) | 1.0.0.0 | Kræves ikke til klargøring. |
| Projektkontraktoverskrifter (salgsordrer) | 1.0.0.1 | Kræves ikke til klargøring. |
| Projekkontraktlinjer (salgsordredetaljer) | 1.0.0.0 | Kræves ikke til klargøring. |
| Projektfinansieringskilde (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Kræves ikke til klargøring. |
| Integrationstabellen for materialeestimater i Project Operations (msdyn\_estimerlinjer) | 1.0.0.0 | Kræves ikke til klargøring. |
| Forslag til projektfakturaer V2 (fakturaer) | 1.0.0.2 | Kræves ikke til klargøring. |
| Integration af faktiske oplysninger i Project Operations (msdyn_actuals) | 1.0.0.14 | Kræves ikke til klargøring. |
| Integration af kontraktlinjemilepæle i Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Kræves ikke til klargøring. |
| Integrationsobjekt for udgiftsestimater i Project Operations (msdyn_estimateslines) | 1.0.0.2 | Kræves ikke til klargøring. |
| Integrationsobjekt for timeestimater i Project Operations (msdyn_resourceassignments) | 1.0.0.5 | Kræves ikke til klargøring. |
| Integrationsobjekt for eksport af projektudgiftskategorier i Project Operations (msdyn_expensecategories) | 1.0.0.2 | Kræves ikke til klargøring. |
| Integrationsobjekt for eksport af projektudgifter i Project Operations (msdyn_expenses) | 1.0.0.2 | Kræves ikke til klargøring. |
| Integrationsobjekt for eksport af projektleverandørfaktura i Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Kræves ikke til klargøring. |
| Integrationsobjekt for eksport af projektleverandørfakturalinje i Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Kræves ikke til klargøring. |
| Projektressourceroller for alle firmaer (reserverbareressourcekategorier) | 1.0.0.1 | Kræver en indledende synkronisering af tabeltilknytningen for at synkronisere de ressourceroller for projektledere og teammedlemmer, der udfyldes i Dynamics 365 Dataverse-miljøet under klargøring. Dataverse er hovedkilden til den første synkronisering. |
| Projektopgaver (msdyn_projecttasks) | 1.0.0.4 | Kræves ikke til klargøring. |
| Projekttransaktionskategorier (msdyn_transactioncategories) | 1.0.0.0 | Kræves ikke til klargøring. |
| Projekter V2 (msdyn_projects) | 1.0.0.1 | Kræves ikke til klargøring. |

Udfør følgende trin for at køre de viste tilknytninger.

1. Aktivér projektressourcerollerne for tabeltilknytningen **alle firmaer (bookableresourcecategories)**, da denne tilknytning kræver den første synkronisering. I feltet **Master for indledende synkronisering** skal du vælge **Common Data Service**. 

 ![Synkronisering af tilknytning af ressourcerolletabel](media/6ResourceInitialSync.jpg)

 Vent, indtil statussen på tilknytningen er **Kører**, før du går videre til næste trin.

2. Vælg alle de resterende obligatoriske tilknytninger. Du kan filtrere dem på listen over dobbeltetilknytninger ved hjælp af nøgleordet **Projekt** i søgning i øverste højre hjørne. Du kan vælge alle tilknytninger og derefter køre. Du kan finde flere oplysninger i [Administrer flere tilknytninger til tabeller](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Sørg for, at relaterede objekttilknytninger også aktiveres og køres.

### <a name="project-operations-dual-write-map-versions"></a>Versioner af Project Operations med dobbeltskrivning

Kør altid den nyeste version af tilknytningen i dit miljø. Visse funktioner og funktionaliteter fungerer muligvis ikke korrekt, hvis der findes en af følgende betingelser:

- En tilknytning er ikke aktiveret.
- Den nyeste version af tilknytningen er ikke aktiveret. 
- Relaterede tabeltilknytninger er ikke aktiveret.

Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. Du kan aktivere en ny version af tilknytningen ved at vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har brugertilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).