---
title: Projektplanlægningslogfiler
description: Denne artikel indeholder oplysninger og eksempler, som kan hjælpe dig med at bruge projektplanlægningslogfilerne til at spore fejl, der er relateret til API'erne for projektplanlægningstjenesten og projektplanlægning.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923688"
---
# <a name="project-scheduling-logs"></a>Projektplanlægningslogfiler

_**Gælder for:** Project Operations til ressource/ikke-lagerbaserede scenarier, Lille udrulning – aftale om proformafakturaren_, _Project for the Web_

Microsoft Dynamics 365 Project Operations bruger [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) som det primære planlægningsprogram. I stedet for at bruge Microsoft Dataverse standard-API'er (Standard Web Application Programming Interfaces) bruger Project Operations de nye API'er for projektplanlægning til at oprette, opdatere og slette projektopgaver, ressourcetildelinger, opgaveafhængigheder, projektgrupper og medlemmer af projektteams. Når oprettelses-, opdaterings- eller slettehandlinger programmeringsmæssigt køres på arbejdsopgavehierarki (WBS), kan der dog opstå fejl. Der er implementeret to nye administrative logfiler til sporing af disse fejl og handlingshistorikken: **Handlingssæt** og **Projektplanlægningstjeneste (PSS)**. Du kan få adgang til disse logfiler ved at gå til **Indstillinger** \> **Planlæg integration**.

I følgende illustration vises datamodellen for logfilerne for projektplanlægning.

![Datamodel for projektplanlægningslogfilerne.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Logfil for handlingssæt

I logfilen for handlingssæt spores udførelsen af et handlingssæt, der bruges til at køre en eller mange oprettelses-, opdaterings- eller slettehandlinger i en batch på projekter, projektopgaver, ressourcetildelinger, opgaveafhængigheder, projektgrupper eller medlemmer af projektteams. Feltet **Handling i status** viser den overordnede status for handlingssættet. Detaljerne om nyttedataene for handlingssættet registreres i relaterede poster med detaljer om handlingssæt.

### <a name="operation-set"></a>Handlingssæt

I tabellen nedenfor vises de felter, der er relateret til objektet **Handlingssæt**.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Den dato/det klokkeslæt, hvor handlingssættet blev fuldført eller mislykkedes.                                                | CompletedOn            |
| msdyn_correlationid   | Værdien af **correlationId** for anmodningen.                                                                  | CorrelationId          |
| msdyn_description     | Beskrivelsen af handlingssættet.                                                                        | Description            |
| msdyn_executedon      | Datoen/det klokkeslæt, hvor posten blev kørt.                                                                       | Udført den            |
| msdyn_operationsetId  | Det entydige id for objektforekomster.                                                                   | OperationSet           |
| msdyn_Project         | Det projekt, der er relateret til handlingssættet.                                                            | Project                |
| msdyn_projectid       | Værdien af **projectid** for anmodningen.                                                                      | ProjectId (udfaset) |
| msdyn_projectName     | Ikke anvendelig.                                                                                              | Ikke tilgængelig         |
| msdyn_PSSErrorLog     | Det entydige id for den fejllog for projektplanlægningstjenesten, der er knyttet til handlingssættet. | PSS-fejllog          |
| msdyn_PSSErrorLogName | Ikke anvendelig.                                                                                              | Ikke tilgængelig         |
| msdyn_status          | Statussen for handlingssættet.                                                                             | Status                 |
| msdyn_statusName      | Ikke anvendelig.                                                                                              | Ikke tilgængelig         |
| msdyn_useraadid       | Azure Active Directory (Azure AD)-objekt-id'et for den bruger, som denne anmodning tilhører.                     | UserAADID              |

### <a name="operation-set-detail"></a>Oplysninger om handlingssæt

I tabellen nedenfor vises de felter, der er relateret til objektet **Detaljer om handlingssæt**.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | De serienummererede Dataverse-felter til anmodningen.                                            | CdsPayload            |
| msdyn_entityname           | Navnet på objektet til anmodningen.                                                     | EntityName            |
| msdyn_httpverb             | Anmodningsmetoden.                                                                         | HTTPVerb (frarådet) |
| msdyn_httpverbName         | Ikke anvendelig.                                                                             | Ikke tilgængelig        |
| msdyn_operationset         | Det entydige id for det handlingssæt, som denne post tilhører.                      | OperationSet          |
| msdyn_operationsetdetailId | Det entydige id for objektforekomster.                                                  | OperationSet-detalje   |
| msdyn_operationsetName     | Ikke anvendelig.                                                                             | Ikke tilgængelig        |
| msdyn_operationtype        | Handlingstypen af handlingssættets detaljer.                                             | Handlingstype         |
| msdyn_operationtypeName    | Ikke anvendelig.                                                                             | Ikke tilgængelig        |
| msdyn_psspayload           | De serienummererede felter i projektplanlægningsservicen for anmodningen.                           | PssPayload            |
| msdyn_recordid             | Identifikatoren for anmodningsposten.                                                       | Post-id             |
| msdyn_requestnumber        | Et automatisk genereret nummer, der identificerer den ordre, som forespørgslerne blev modtaget i. | Anmodningsnummer        |

## <a name="project-scheduling-service-error-logs"></a>Fejllogfiler for projektplanlægningstjenesten

Fejllogfilerne for projektplanlægningstjenesten registrerer de fejl, der opstår, når projektplanlægningstjenesten forsøger at **gemme** eller **åbne** en handling. Der findes tre understøttede scenarier, hvor disse logfiler oprettes:

- Kritiske fejl i forbindelse med brugerindledte handlinger (f.eks. kan der ikke oprettes en tildeling på grund af manglende rettigheder).
- Projektplanlægningstjenesten kan ikke programmeringsmæssigt oprette, opdatere, slette eller udføre andre overlappende handlinger på et objekt.
- Brugeren oplever fejl, når en post ikke åbnes (f.eks. når et projekt åbnes, eller et teammedlems oplysninger opdateres).

### <a name="project-scheduling-service-log"></a>Logfil for projektplanlægningstjeneste

I tabellen nedenfor vises de felter, der er inkluderet i logfilen for projektplanlægningstjenesten.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Kaldstakken for undtagelsen.                                               | Kaldstak     |
| msdyn_correlationid | Korrelations-id'et for fejlen.                                               | CorrelationId  |
| msdyn_errorcode     | Et felt, der bruges til at gemme Dataverse-fejlkoden eller HTTP-fejlkoden. | Fejlkode     |
| msdyn_HelpLink      | Et link til den offentlige tilgængelige hjælpedokumentation.                                       | Link til hjælp      |
| msdyn_log           | Logfilen fra projektplanlægningstjenesten.                                   | Log            |
| msdyn_project       | Det projekt, der er knyttet til fejllogfilen.                             | Project        |
| msdyn_projectName   | Navnet på projektet, hvis nyttelasten for handlingssættet fortsætter. | Ikke tilgængelig |
| msdyn_psserrorlogId | Det entydige id for objektforekomster.                                     | PSS-fejllog  |
| msdyn_SessionId     | Projektsessions-id'er.                                                        | Sessions-id     |

## <a name="error-log-cleanup"></a>Oprydning i fejllogfiler

Både fejllogfiler til projektplanlægningstjenesten og logfilen for operationssættet kan som standard ryddes op hver 90. dag. Alle poster, der er ældre end 90 dage, slettes. Ved at ændre værdien i feltet **msdyn_StateOperationSetAge** på siden **Projektparametre**, kan administratorer dog justere oprydningsintervallet til mellem 1 og 120 dage. Der findes flere metoder til at ændre denne værdi:

- Tilpas objektet **Projektparameter** ved at oprette en brugerdefineret side og tilføje feltet **Angiv alder for gamle handlinger**.
- Brug den klientkode, der bruger [softwarepakken til udvikling af WebApi](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Brug tjeneste-SDK-koden, der bruger Xrm-SDK-metoden **updateRecord** (klient-API-reference) i modelbaserede apps. Power Apps indeholder en beskrivelse og understøttede parametre for metoden **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
