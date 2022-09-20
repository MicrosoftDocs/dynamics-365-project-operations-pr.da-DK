---
title: Funktionsændringer fra Project Service Automation til Project Operations
description: Denne artikel indeholder en oversigt over funktionsændringerne fra Project Service Automation til Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459919"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Funktionsændringer fra Project Service Automation til Project Operations

Opgraderingen fra Dynamics 365 Project Service Automation til Dynamics 365 Project Operations lille leveres i tre faser. Denne artikel indeholder oplysninger om de store ændringer, som du kan forvente at se, når opgraderingen er fuldført.

| Levering af opgradering | Fase 1 <br>(Januar 2022) | Fase 2 <br>(November 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Ingen afhængighed af arbejdsopgavehierarkiet (WBS) til projekter. | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| WBS er inkluderet i de grænser for Project Operations, der understøttes i øjeblikket. | &nbsp; | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| WBS'en uden for de grænser for Project Operations, der understøttes i øjeblikket, herunder understøttelse af Project Desktop Client. | &nbsp; | &nbsp; | :heavy_kontrol_mærke: |

## <a name="project-management"></a>Projektstyring

De vigtigste ændringer i brugeroplevelsen vil være inden for projektplanlægning. Project Operations vedtager en ny og moderne oplevelse med at administrere et arbejdsopgavehierarki (WBS) ved at udnytte de planlægningsfunktioner, der findes i [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Forskelle i planlægningsoplevelsen

I følgende tabel opsummeres forskellene i planlægning mellem Project Service Automation og Project Operations.

|  Planlægning     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektskabeloner – Mulighed for at definere og anvende projektskabeloner, når et projekt oprettes  |  &nbsp;    | :heavy_kontrol_mærke: |
| Integration af arbejdsopgavehierarki (WBS) for projekter med klient til stationære computere   |    &nbsp;  | :heavy_kontrol_mærke: |
| Begrænsninger – Start tidligst, og afslut senest  | :heavy_kontrol_mærke: |   &nbsp;  |
| Milepæle – Opgaver uden varighed   | :heavy_kontrol_mærke:  |  &nbsp;  |
| Ressourcebaserede opgaver respekterer tilgængeligheden af tildelte ressourcer   | :heavy_kontrol_mærke: |  &nbsp;    |
| Tidsfasebaseret redigering – Redigér planer, og arbejd på daglig basis   |   &nbsp;  | :heavy_kontrol_mærke: |
| Automatisk/manuel planlægning – Brug projektplanlægningsprogrammet til automatisk eller manuel planlægning af opgaver |  &nbsp; | :heavy_kontrol_mærke:  |
| Redigér store projekter direkte i brugergrænsefladen: Der er ingen grænser for størrelsen på de planer, der kan redigeres  | Grænse på 500 opgaver  | :heavy_kontrol_mærke:       |
| Procentdel fuldført – Markér status for opgave   | :heavy_kontrol_mærke:  |  &nbsp;  |
| [Projektplantilstande](../project-management/scheduling-modes.md) – Definér projektet som faste enheder, fast indsats eller fast varighed | :heavy_kontrol_mærke: | &nbsp; |
| Tidslinje - Opbyg og tilpas tidslinjevisningen for at visualisere planlægningsdetaljer og kommunikere med interessenter. | :heavy_kontrol_mærke:  | &nbsp; |
| Indsatsbaserede opgaver – Planlægning af programsupport til planlægning af en opgave som indsatsbaseret  | :heavy_kontrol_mærke:  | &nbsp; |
| Dialogboksen **Opgaveoplysninger** – Gemme opgavedetaljer ved hjælp af en dialogboks | :heavy_kontrol_mærke:  |  &nbsp;  |
| Træk og slip – Vælg flere opgaver ad gangen, og redigér deres placering i WBS | :heavy_kontrol_mærke: | &nbsp;  |
| Fleksible faste visninger – Definér mere detaljerede visninger af opgaveattributter   | :heavy_kontrol_mærke:  | &nbsp; |
| Sortér og filtrér WBS  | :heavy_kontrol_mærke:  | &nbsp; |
| Visning af tavle for projektlevering, der ikke er et vandfald  | :heavy_kontrol_mærke:   | &nbsp; |
| Tidslinjevisning – Interaktivt Gantt-diagram, som anvendes til at illustrere og redigere WBS   | :heavy_kontrol_mærke:  | &nbsp; |
| Tastaturgenveje – Brug tastaturgenveje til almindelige handlinger, som f.eks. indrykning eller indsættelse  | :heavy_kontrol_mærke:  |  &nbsp; |
| Fortryd på flere niveauer – Udfør what if-analyser for at få en fuld forståelse af ændringernes indvirkning ved at omvende og genanvende et helt sæt handlinger | :heavy_kontrol_mærke: | &nbsp; |
| Klip/kopiér/sæt ind – Samarbejd om planlægningsudvikling ved at kopiere og indsætte detaljer om planlægning mellem programmer  | :heavy_kontrol_mærke: | &nbsp; |
| Kontrollister til opgaver – Tilføj op til 20 kontrollisteelementer til en opgave   | :heavy_kontrol_mærke: | &nbsp; |

## <a name="project-planning"></a>Projektplanlægning

Siden **Projekt** i Project Operations indeholder et betydeligt antal forskelle i forhold til siden **Projekt** i Project Service Automation.

Følgende handlinger er blevet fjernet fra siden **Projekter** som en del af fase 1-opgraderingen:

  - **Åbn i MS Project**
  - **Opret skabelon**
  - **Fjern link til MS Project**

Siden **Projekt** i Project Operations indeholder følgende nye faner.

- **Materialeestimater**
- **Konfiguration af opgavefakturering**

Fanen **Status** er blevet fjernet, og feltet **Status** findes nu under fanen **Oversigt** med projektplanlægningstilstanden.

   ![Opdateringer til projektsiden.](media/projectform.png)

Fanen **Planlægning** er omdøbt til fanen **Opgave** og indeholder den nye projektplanlægningsoplevelse med Project for the Web.

   ![Fanen Nye projektopgaver.](media/tasktab.png)

## <a name="scheduling-modes"></a>Planlægningstilstande

Project Operations har introduceret en ny funktion, [Planlægningstilstande](../project-management/scheduling-modes.md). Alle eksisterende projekter i Project Service Automation er som standard **Fast varighed** i Project Operations. Standarden for nye projekter kan dog administreres ved at gå til **Indstillinger** > **Parametre** > **Parametre** > **Planlægningstilstand**.

   ![Projektparameterindstillinger for planlægningstilstand.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Grænser for projektplanlægning

Project Operations er afhængig af Project for the Web i forbindelse med alle projektplanlægningshandlinger. Project for the Web administrerer arbejdsopgavehierakiet ved hjælp af grænseværdierne i følgende tabel.

| **Felt**                                          | **Grænse**             |
|----------------------------------------------------|-----------------------|
| Det maksimale samlede antal opgaver for et projekt                  | 500                   |
| Den maksimale samlede varighed af et projekt               | 3.650 dage (10 år)  |
| Det maksimale samlede antal ressourcer for et projekt              | 300                   |
| Det maksimale samlede antal links (kun efterfølger) for et projekt | 600                   |
| Det maksimale samlede antal brugertilpassede felter for et projekt          | 10                    |
| Det maksimale hierarkiniveau                            | 10 niveauer             |
| Det maksimale antal links (efterfølger + forgænger)            | 20                    |
| Den maksimale varighed af bladopgaver                      | 1250 dage             |
| Den maksimale varighed af en opsummeringsopgave                 | 3.650 dage (10 år)  |
| Det maksimale antal ressourcer, der kan tildeles en opgave               | 20 ressourcer          |
| Understøttet datointerval for en opgave                    | 1/1/2000 - 31/12/2149 |
| Kontrollistepunkter                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Mulighed for udvidelse og udvikling af projektplanlægning

Når du har opgraderet til Project Operations, skal du bruge API'er for projektplanlægning til at udføre oprettelses-, opdaterings- og sletningshandlinger for følgende objekter:

|   Enhedsnavn           |   Objektets logiske navn       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektopgave            | msdyn_projecttask           |
| Projektopgaveafhængighed | msdyn_projecttaskdependency |
| Ressourcetildeling     | msdyn_resourceassignment    |
| Projektbucket          | msdyn_projectbucket         |
| Medlem af projektteam     | msdyn_projectteam           |

Hvis du i øjeblikket har tilpasninger, der omfatter disse objekter, skal du se [Brug API'er til projektplanlægning til at udføre handlinger med planlægningsobjekter](../project-management/schedule-api-preview.md) for vejledning til gennemførelse.

## <a name="data-model-changes"></a>Ændringer i datamodel

Som en del af opgraderingens fase 1 er der ændringer af datamodellen. Disse ændringer er primært feltændringer af eksisterende objekter. I fase 1 er objekterne **msydn_project** og **msdyn_projectteam** en refaktorering af tilpasningerne. 

> [!IMPORTANT]
> Dette afsnit opdateres med flere objekter, efterhånden som fremtidige opgraderingsfaser fuldføres.

Følgende felter er blevet erstattet med nye felter.

|   Enhed          |   Gammelt logisk navn   |   Nyt logisk navn    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_varighed        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Følgende felter er blevet tilføjet.

|   Enhed          |   Logisk navn                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Viser den samlede værdi af det faktiske vederlagssalg for projektet. Kun til anvendelse i Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Viser aggregatet af de faktiske materialeomkostninger for projektet. Kun til anvendelse i Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Viser den samlede værdi af de faktiske materialesalg for projektet. Kun til anvendelse i Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Kontraktlinjen, der er tilknyttet dette projekt. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Dette er et internt systemfelt, der bruges til at **Kopiere projektet**, som er relateret til korrelations-id'et. Kun til anvendelse i Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Dette er et internt systemfelt, der bruges til at **Kopiere projektet**, som er relateret til sessions-id'et. Kun til anvendelse i Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Seneste synkronisering af xRM Global Revision Token fra projektplanlægningstjenesten. |
| msdyn_project     | msdyn_msprojectdocument                      | Det Microsoft Project-dokument, der hører sammen med projektet. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Aggregatet af de planlagte materialeomkostninger for projektet. Kun til anvendelse i Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Aggregatet af de planlagte materialesalg for projektet. Kun til anvendelse i Project Service Automation. |
| msdyn_project     | msdyn_program                                | Det program, som dette projekt er relateret til. |
| msdyn_project     | msdyn_quotelineproject                       | Tilbudslinjen, der er tilknyttet dette projekt. |
| msdyn_project     | msdyn_replaylogheader                        | Overskriften til afspilningslogfiler. |
| msdyn_project     | msdyn_schedulemode                           | Standardplanlægningstilstanden, der bruges til alle opgaver i projektet.  |
| msdyn_project     | msdyn_taskearlieststart                      | Den tidligste startdato for en hvilken som helst opgave i projektet.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Det projektteammedlem, som dette projektteammedlem blev kopieret fra. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indikerer, om ressourcekravet skal oprettes for et nyligt oprettet generisk teammedlem.  |
| msdyn_projectteam | msdyn_deletestatus                           | Slettestatussen for teammedlemmet for at spore, om der er sendt en anmodning om sletning til projektplanlægningstjenesten, og om den sender et svar inden for det forventede tidsrum. |
| msdyn_projectteam | msdyn_effortcompleted                        | Sporer den indsats, som teammedlemmerne har ydet på deres tildelinger. |
| msdyn_projectteam | msdyn_effortremaining                        | Sporer den indsats, som teammedlemmet endnu ikke har ydet på deres tildelinger. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Ventetiden fra det tidspunkt, hvor teammedlemmet sender en sletteanmodning til projektplanlægningstjenesten, og til teammedlemmet rent faktisk slettes i Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Det tidsstempel, der skal registreres, når anmodningen om sletning af teammedlemmet sendes til projektplanlægningstjenesten. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Viser det projektteammedlem, som dette projektteammedlem er kopieret fra.  |

## <a name="project-templates"></a>Projektskabeloner

Project Operations understøtter ikke projektskabeloner. Men du kan gengive meget af kernefunktionaliteten ved hjælp af [API'en Kopiér projekt](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Understøttelse af tilføjelsesprogrammet til stationære computere

Support til Microsoft Project-tilføjelsesprogrammet til stationære computere er ikke tilgængelig i de første to faser af opgraderingen. I fase 3 kan kunder, der har projekter, som er større end de aktuelt understøttede grænser for Project for the Web, bruge tilføjelsesprogrammet til stationære computere.

## <a name="editing-resource-assignment-contours"></a>Redigering af ressourcetildelingsprofiler

Muligheden for at redigere ressourcetildelinger er tilgængelig, når fase 2 i opgraderingen er tilgængelig.

## <a name="billing-and-pricing"></a>Fakturering og prisfastsættelse

Følgende nye funktioner er blevet tilføjet i Project Operations. Disse funktioner har karakter af tilføjelser og har ingen indvirkning på datamodellen for Project Service Automation.

- [Registrering af materialeforbrug på projekter og projektopgaver](../material/material-usage-log.md)
- [Administration af underentrepriser](../pro/subcontracting/managing-subcontracts-overview.md)
- [Forskudskontrakter og kontrakter baseret på forskudshonorar](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontraktstatus, som ikke må overskrides, og valideringer](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Opgavebaseret fakturering](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Udfasede komponenter

I følgende tabeller dokumenteres alle udfasede felter, som flyttes til løsningen for udfasede komponenter efter opgraderingen. Du kan finde flere oplysninger og et link til løsninger i [Dynamics 365 Project Service Automation 3x til udfasede komponenter i Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>fakturadetalje

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Felter                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

