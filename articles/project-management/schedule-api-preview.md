---
title: Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter
description: Dette emne indeholder oplysninger og eksempler på brug af projektplanlægnings-API'er.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293220"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

> [!IMPORTANT] 
> Visse eller alle de funktioner, der er omtalt i dette emne, er tilgængelige som en del af en forhåndsversion. Indholdet og funktionerne kan ændres. 

## <a name="scheduling-entities"></a>Planlægningsobjekter

Projektplanlægnings-API'er gør det muligt at oprette, opdatere og slette handlinger med **Planlægningsobjekter**. Disse objekter administreres via planlægningsprogrammet i Projekt til internettet. Handlinger til oprettelse, opdatering og sletning med **Planlægningsobjekter** var i tidligere udgivelser til Dynamics 365 Project Operations begrænset.

Følgende tabel indeholder en fuldstændig liste over projektplanlægningsobjekterne.

| Enhedsnavn  | Objektets logiske navn |
| --- | --- |
| Project | msdyn_project |
| Projektopgave  | msdyn_projecttask  |
| Projektopgaveafhængighed  | msdyn_projecttaskdependency  |
| Ressourcetildeling | msdyn_resourceassignment |
| Projektbucket  | msdyn_projectbucket |
| Medlem af projektteam | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet er et arbejdsenhedsmønster, der kan bruges, når flere forespørgsler, der påvirker tidsplanen, skal behandles i en transaktion.

## <a name="project-schedule-apis"></a>Projektplanlægnings-API'er

Følgende er en liste over aktuelle projektplanlægnings-API'er.

- **msdyn_CreateProjectV1**: Denne API kan bruges til at oprette et projekt. Projekt- og standardprojektbucket oprettes med det samme.
- **msdyn_CreateTeamMemberV1**: Denne API kan bruges til at oprette et projektteammedlem. Teammedlemsposten oprettes med det samme.
- **msdyn_CreateOperationSetV1**: Denne API kan bruges til at planlægge flere forespørgsler, der skal udføres i en transaktion.
- **msdyn_PSSCreateV1**: Denne API kan bruges til at oprette et objekt. Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter oprettelseshandlingen.
- **msdyn_PSSUpdateV1**: Denne API kan bruges til at opdatere et objekt. Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter opdateringshandlingen.
- **msdyn_PSSDeleteV1**: Denne API kan bruges til at slette et objekt. Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter slettehandlingen.
- **msdyn_ExecuteOperationSetV1**: Denne API bruges til at udføre alle handlinger i det givne operationssæt.

## <a name="using-project-schedule-apis-with-operationset"></a>Brug af projektplanlægnings-API'er med handlingssæt

Da poster med både **CreateProjectV1** og **CreateTeamMemberV1** oprettes med det samme, kan disse API'er ikke bruges direkte i **OperationSet**. Du kan dog bruge API'en til at oprette de krævede poster, et **OperationSet** og derefter bruge disse forudoprettede poster i **OperationSet**.

## <a name="supported-operations"></a>Understøttede handlinger

| Planlægningsobjekt | Opret | Opdatering | Delete | Vigtige overvejelser |
| --- | --- | --- | --- | --- |
Projektopgave | Ja | Ja | Ja | Intet |
| Projektopgaveafhængighed | Ja | Ja | | Projektopgaveafhængighedsposter opdateres ikke. I stedet kan en gammel post slettes, og der kan oprettes en ny post. |
| Ressourcetildeling | Ja | Ja | | Handlinger med følgende felter understøttes ikke: **BookableResourceID**, **Indsats**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**. Ressourcetildelingsposter opdateres ikke. I stedet kan den gamle post slettes, og der kan oprettes en ny post. |
| Projektbucket | I/R | I/R | I/R | Standardbucket oprettes ved hjælp af API'en **CreateProjectV1**. |
| Projektteammedlem | Ja | Ja | Ja | Brug API'en **CreateTeamMemberV1** til oprettelseshandlingen. |
| Project | Ja | Ja | I/R | Handlinger med følgende felter understøttes ikke: **StateCode**, **BulkStatus**, **GlobalRevisionToken**, **CalendarID**, **Indsats**, **EffortCompleted**, **EffortRemaining**, **Status**, **Afsluttet**, **TaskEarliestStart** og **Varighed**. |

Disse API'er kan kaldes sammen med enhedsobjekter, der indeholder brugerdefinerede felter.

Id-egenskaben er valgfri. Hvis den oplyses, forsøger systemet at bruge den, og der udløses en undtagelse, hvis den ikke kan bruges. Hvis den ikke er angivet, oprettes den af systemet.

## <a name="restricted-fields"></a>Begrænsede felter

I følgende tabeller defineres de felter, der er begrænset fra **Opret** og **Rediger**.

### <a name="project-task"></a>Projektopgave

| **Logisk navn**                       | **Kan oprette** | **Kan redigere**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | nej             | nej               |
| msdyn_actualcost_base                  | nej             | nej               |
| msdyn_actualend                        | nej             | nej               |
| msdyn_actualsales                      | nej             | nej               |
| msdyn_actualsales_base                 | nej             | nej               |
| msdyn_actualstart                      | nej             | nej               |
| msdyn_costatcompleteestimate           | nej             | nej               |
| msdyn_costatcompleteestimate_base      | nej             | nej               |
| msdyn_costconsumptionpercentage        | nej             | nej               |
| msdyn_effortcompleted                  | nej             | nej               |
| msdyn_effortestimateatcomplete         | nej             | nej               |
| msdyn_iscritical                       | nej             | nej               |
| msdyn_iscriticalname                   | nej             | nej               |
| msdyn_ismanual                         | nej             | nej               |
| msdyn_ismanualname                     | nej             | nej               |
| msdyn_ismilestone                      | nej             | nej               |
| msdyn_ismilestonename                  | nej             | nej               |
| msdyn_LinkStatus                       | nej             | nej               |
| msdyn_linkstatusname                   | nej             | nej               |
| msdyn_msprojectclientid                | nej             | nej               |
| msdyn_plannedcost                      | nej             | nej               |
| msdyn_plannedcost_base                 | nej             | nej               |
| msdyn_plannedsales                     | nej             | nej               |
| msdyn_plannedsales_base                | nej             | nej               |
| msdyn_pluginprocessingdata             | nej             | nej               |
| msdyn_progress                         | nej             | nej (ja for P4W) |
| msdyn_remainingcost                    | nej             | nej               |
| msdyn_remainingcost_base               | nej             | nej               |
| msdyn_remainingsales                   | nej             | nej               |
| msdyn_remainingsales_base              | nej             | nej               |
| msdyn_requestedhours                   | nej             | nej               |
| msdyn_resourcecategory                 | nej             | nej               |
| msdyn_resourcecategoryname             | nej             | nej               |
| msdyn_resourceorganizationalunitid     | nej             | nej               |
| msdyn_resourceorganizationalunitidname | nej             | nej               |
| msdyn_salesconsumptionpercentage       | nej             | nej               |
| msdyn_salesestimateatcomplete          | nej             | nej               |
| msdyn_salesestimateatcomplete_base     | nej             | nej               |
| msdyn_salesvariance                    | nej             | nej               |
| msdyn_salesvariance_base               | nej             | nej               |
| msdyn_scheduleddurationminutes         | nej             | nej               |
| msdyn_scheduledend                     | nej             | nej               |
| msdyn_scheduledstart                   | nej             | nej               |
| msdyn_schedulevariance                 | nej             | nej               |
| msdyn_skipupdateestimateline           | nej             | nej               |
| msdyn_skipupdateestimatelinename       | nej             | nej               |
| msdyn_summary                          | nej             | nej               |
| msdyn_varianceofcost                   | nej             | nej               |
| msdyn_varianceofcost_base              | nej             | nej               |

### <a name="project-task-dependency"></a>Projektopgaveafhængighed

| **Logisk navn**              | **Kan oprette** | **Kan redigere** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | nej             | nej           |
| msdyn_linktypename            | nej             | nej           |
| msdyn_predecessortask         | ja            | nej           |
| msdyn_predecessortaskname     | ja            | nej           |
| msdyn_project                 | ja            | nej           |
| msdyn_projectname             | ja            | nej           |
| msdyn_projecttaskdependencyid | ja            | nej           |
| msdyn_successortask           | ja            | nej           |
| msdyn_successortaskname       | ja            | nej           |

### <a name="resource-assignment"></a>Ressourcetildeling

| **Logisk navn**             | **Kan oprette** | **Kan redigere** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | ja            | nej           |
| msdyn_bookableresourceidname | ja            | nej           |
| msdyn_bookingstatusid        | nej             | nej           |
| msdyn_bookingstatusidname    | nej             | nej           |
| msdyn_committype             | nej             | nej           |
| msdyn_committypename         | nej             | nej           |
| msdyn_effort                 | nej             | nej           |
| msdyn_effortcompleted        | nej             | nej           |
| msdyn_effortremaining        | nej             | nej           |
| msdyn_finish                 | nej             | nej           |
| msdyn_plannedcost            | nej             | nej           |
| msdyn_plannedcost_base       | nej             | nej           |
| msdyn_plannedcostcontour     | nej             | nej           |
| msdyn_plannedsales           | nej             | nej           |
| msdyn_plannedsales_base      | nej             | nej           |
| msdyn_plannedsalescontour    | nej             | nej           |
| msdyn_plannedwork            | nej             | nej           |
| msdyn_projectid              | ja            | nej           |
| msdyn_projectidname          | nej             | nej           |
| msdyn_projectteamid          | nej             | nej           |
| msdyn_projectteamidname      | nej             | nej           |
| msdyn_start                  | nej             | nej           |
| msdyn_taskid                 | nej             | nej           |
| msdyn_taskidname             | nej             | nej           |
| msdyn_userresourceid         | nej             | nej           |

### <a name="project-team-member"></a>Projektteammedlem

| **Logisk navn**                                 | **Kan oprette** | **Kan redigere** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | nej             | nej           |
| msdyn_creategenericteammemberwithrequirementname | nej             | nej           |
| msdyn_deletestatus                               | nej             | nej           |
| msdyn_deletestatusname                           | nej             | nej           |
| msdyn_effort                                     | nej             | nej           |
| msdyn_effortcompleted                            | nej             | nej           |
| msdyn_effortremaining                            | nej             | nej           |
| msdyn_finish                                     | nej             | nej           |
| msdyn_hardbookedhours                            | nej             | nej           |
| msdyn_hours                                      | nej             | nej           |
| msdyn_markedfordeletiontimer                     | nej             | nej           |
| msdyn_markedfordeletiontimestamp                 | nej             | nej           |
| msdyn_msprojectclientid                          | nej             | nej           |
| msdyn_percentage                                 | nej             | nej           |
| msdyn_requiredhours                              | nej             | nej           |
| msdyn_softbookedhours                            | nej             | nej           |
| msdyn_start                                      | nej             | nej           |

### <a name="project"></a>Project

| **Logisk navn**                       | **Kan oprette** | **Kan redigere** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | nej             | nej           |
| msdyn_actualexpensecost_base           | nej             | nej           |
| msdyn_actuallaborcost                  | nej             | nej           |
| msdyn_actuallaborcost_base             | nej             | nej           |
| msdyn_actualsales                      | nej             | nej           |
| msdyn_actualsales_base                 | nej             | nej           |
| msdyn_contractlineproject              | ja            | nej           |
| msdyn_contractorganizationalunitid     | ja            | nej           |
| msdyn_contractorganizationalunitidname | ja            | nej           |
| msdyn_costconsumption                  | nej             | nej           |
| msdyn_costestimateatcomplete           | nej             | nej           |
| msdyn_costestimateatcomplete_base      | nej             | nej           |
| msdyn_costvariance                     | nej             | nej           |
| msdyn_costvariance_base                | nej             | nej           |
| msdyn_varighed                         | nej             | nej           |
| msdyn_effort                           | nej             | nej           |
| msdyn_effortcompleted                  | nej             | nej           |
| msdyn_effortestimateatcompleteeac      | nej             | nej           |
| msdyn_effortremaining                  | nej             | nej           |
| msdyn_finish                           | ja            | ja          |
| msdyn_globalrevisiontoken              | nej             | nej           |
| msdyn_islinkedtomsprojectclient        | nej             | nej           |
| msdyn_islinkedtomsprojectclientname    | nej             | nej           |
| msdyn_linkeddocumenturl                | nej             | nej           |
| msdyn_msprojectdocument                | nej             | nej           |
| msdyn_msprojectdocumentname            | nej             | nej           |
| msdyn_plannedexpensecost               | nej             | nej           |
| msdyn_plannedexpensecost_base          | nej             | nej           |
| msdyn_plannedlaborcost                 | nej             | nej           |
| msdyn_plannedlaborcost_base            | nej             | nej           |
| msdyn_plannedsales                     | nej             | nej           |
| msdyn_plannedsales_base                | nej             | nej           |
| msdyn_progress                         | nej             | nej           |
| msdyn_remainingcost                    | nej             | nej           |
| msdyn_remainingcost_base               | nej             | nej           |
| msdyn_remainingsales                   | nej             | nej           |
| msdyn_remainingsales_base              | nej             | nej           |
| msdyn_replaylogheader                  | nej             | nej           |
| msdyn_salesconsumption                 | nej             | nej           |
| msdyn_salesestimateatcompleteeac       | nej             | nej           |
| msdyn_salesestimateatcompleteeac_base  | nej             | nej           |
| msdyn_salesvariance                    | nej             | nej           |
| msdyn_salesvariance_base               | nej             | nej           |
| msdyn_scheduleperformance              | nej             | nej           |
| msdyn_scheduleperformancename          | nej             | nej           |
| msdyn_schedulevariance                 | nej             | nej           |
| msdyn_taskearlieststart                | nej             | nej           |
| msdyn_teamsize                         | nej             | nej           |
| msdyn_teamsize_date                    | nej             | nej           |
| msdyn_teamsize_state                   | nej             | nej           |
| msdyn_totalactualcost                  | nej             | nej           |
| msdyn_totalactualcost_base             | nej             | nej           |
| msdyn_totalplannedcost                 | nej             | nej           |
| msdyn_totalplannedcost_base            | nej             | nej           |


## <a name="limitations-and-known-issues"></a>Begrænsninger og kendte problemer
Her følger en liste over begrænsninger og kendte problemer:

- Projektplanlægnings-Api'er kan kun bruges af **Brugere med Microsoft Project-licens**. De kan ikke bruges af:
    - Programbrugere
    - Systembrugere
    - Integrationsbrugere
    - Andre brugere, der ikke har den påkrævede licens
- Hvert **OperationSet** kan kun have op til 100 handlinger.
- Hver bruger kan kun have op til 10 åbne **OperationSet**.
- Project Operations understøtter i øjeblikket maksimalt 500 opgaver i alt på et projekt.
- Status for fejl i **OperationSet** og fejllogfiler er ikke tilgængelige i øjeblikket.
- [Begrænsninger og grænser for projekter og opgaver](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Fejlhåndtering

   - Hvis du vil gennemse de fejl, der er genereret i operationssæt, skal du gå til **Indstillinger** \> **Integration af planlægning** \> **Operationssæt**.
   - Hvis du vil gennemse de fejl, der er genereret fra projektplanlægningstjenesten, skal du gå til **Indstillinger** \> **Planlægning af integration** \> **PSS-fejllogfiler**.

## <a name="sample-scenario"></a>Eksempelscenarie

I dette scenario skal du oprette et projekt, et teammedlem, fire opgaver og to ressourcetildelinger. Derefter skal du opdatere én opgave, opdatere projektet, slette én opgave, slette én ressourcetildeling og oprette en opgaveafhængighed.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Yderligere eksempler

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
