---
title: Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter
description: Denne artikel indeholder oplysninger om og eksempler på, hvordan du bruger API'er til Projektplanlægning.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541117"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


**Planlægningsobjekter**

Projektplanlægnings-API'er gør det muligt at oprette, opdatere og slette handlinger med **Planlægningsobjekter**. Disse objekter administreres via planlægningsprogrammet i Projekt til internettet. Handlinger til oprettelse, opdatering og sletning med **Planlægningsobjekter** var i tidligere udgivelser til Dynamics 365 Project Operations begrænset.

Følgende tabel indeholder en fuldstændig liste over projektplanlægningsobjekterne.

| **Enhedsnavn**         | **Objektets logiske navn**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektopgave            | msdyn_projecttask           |
| Projektopgaveafhængighed | msdyn_projecttaskdependency |
| Ressourcetildeling     | msdyn_resourceassignment    |
| Projektbucket          | msdyn_projectbucket         |
| Medlem af projektteam     | msdyn_projectteam           |
| Projekttjeklister      | msdyn_projectchecklist      |
| Projektnavn           | msdyn_projectlabel          |
| Projektopgave til navn   | msdyn_projecttasktolabel    |
| Projektsprint          | msdyn_projectsprint         |

**OperationSet**

OperationSet er et arbejdsenhedsmønster, der kan bruges, når flere forespørgsler, der påvirker tidsplanen, skal behandles i en transaktion.

**Projektplanlægnings-API'er**

Følgende er en liste over aktuelle projektplanlægnings-API'er.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Denne API bruges til at oprette et projekt. Projekt- og standardprojektet-bucket oprettes med det samme.                         |
| **msdyn_CreateTeamMemberV1**            | Denne API bruges til at oprette et teammedlem. Teammedlemsposten oprettes med det samme.                                  |
| **msdyn_CreateOperationSetV1**          | Denne API kan bruges til at planlægge flere forespørgsler, der skal udføres i en transaktion.                                        |
| **msdyn_PssCreateV1**                   | Denne API bruges til at oprette et objekt. Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter oprettelseshandlingen. |
| **msdyn_PssUpdateV1**                   | Denne API bruges til at opdatere et objekt. Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter opdateringshandlingen  |
| **msdyn_PssDeleteV1**                   | Denne API bruges til at slette et objekt. Objektet kan være et hvilket som helst af de projektplanlægningsobjekter, der understøtter slettehandlingen. |
| **msdyn_ExecuteOperationSetV1**         | Denne API bruges til at udføre alle handlinger i det givne operationssæt.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Denne API bruges til at opdatere planlagt arbejdsprofil for ressourcetildeling.                                                        |



**Brug af projektplanlægnings-API'er med handlingssæt**

Da poster med både **CreateProjectV1** og **CreateTeamMemberV1** oprettes med det samme, kan disse API'er ikke bruges direkte i **OperationSet**. Du kan dog bruge API'en til at oprette de krævede poster, et **OperationSet** og derefter bruge disse forudoprettede poster i **OperationSet**.

**Understøttede handlinger**

| **Planlægningsobjekt**   | **Opret** | **Update** | **Delete** | **Vigtige overvejelser**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektopgave            | Ja        | Ja        | Ja        | Felterne **Fremgang**, **EffortCompleted** og **EffortRemaining** kan redigeres i Project for the Web, men de kan ikke redigeres i Project Operations.                                                                                                                                                                                             |
| Projektopgaveafhængighed | Ja        | Nr.         | Ja        | Projektopgaveafhængighedsposter opdateres ikke. I stedet kan en gammel post slettes, og der kan oprettes en ny post.                                                                                                                                                                                                                                 |
| Ressourcetildeling     | Ja        | Ja\*      | Ja        | Handlinger med følgende felter understøttes ikke: **BookableResourceID**, **Indsats**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**. Ressourcetildelingsposter opdateres ikke. I stedet kan den gamle post slettes, og der kan oprettes en ny post. Der er angivet en separat API til opdatering af profiler for ressourcetildelinger. |
| Projektbucket          | Ja        | Ja        | Ja        | Standardplaceringen oprettes ved hjælp af API'en **CreateProjectV1**. I frigivelsen af opdatering 16 blev der tilføjet support til oprettelse og sletning af projektbucket.                                                                                                                                                                                                   |
| Projektteammedlem     | Ja        | Ja        | Ja        | Brug API'en **CreateTeamMemberV1** til oprettelseshandlingen.                                                                                                                                                                                                                                                                                           |
| Project                 | Ja        | Ja        |            | Handlinger med følgende felter understøttes ikke: **StateCode**, **BulkStatus**, **GlobalRevisionToken**, **CalendarID**, **Indsats**, **EffortCompleted**, **EffortRemaining**, **Status**, **Afsluttet**, **TaskEarliestStart** og **Varighed**.                                                                                       |
| Projekttjeklister      | Ja        | Ja        | Ja        |                                                                                                                                                                                                                                                                                                                                                         |
| Projektnavn           | Nr.         | Ja        | Nr.         | Etiketnavne kan ændres. Denne funktion er kun tilgængelig for Project for the Web                                                                                                                                                                                                                                                                      |
| Projektopgave til navn   | Ja        | Nr.         | Ja        | Denne funktion er kun tilgængelig for Project for the Web                                                                                                                                                                                                                                                                                                  |
| Projektsprint          | Ja        | Ja        | Ja        | Feltet **Start** skal have en dato, der er tidligere end feltet **Afslut**. Sprints for det samme projekt kan ikke overlappe hinanden. Denne funktion er kun tilgængelig for Project for the Web                                                                                                                                                                    |




Id-egenskaben er valgfri. Hvis den oplyses, forsøger systemet at bruge den, og der udløses en undtagelse, hvis den ikke kan bruges. Hvis den ikke er angivet, oprettes den af systemet.

**Begrænsninger og kendte problemer**

Her følger en liste over begrænsninger og kendte problemer:

-   Projektplanlægnings-Api'er kan kun bruges af **Brugere med Microsoft Project-licens**. De kan ikke bruges af:
    -   Programbrugere
    -   Systembrugere
    -   Integrationsbrugere
    -   Andre brugere, der ikke har den påkrævede licens
-   Hvert **OperationSet** kan kun have op til 100 handlinger.
-   Hver bruger kan kun have op til 10 åbne **OperationSet**.
-   Project Operations understøtter i øjeblikket maksimalt 500 opgaver i alt på et projekt.
-   Hver opdateringshandling for profiler for ressourcetildelinger tæller som en enkelt handling.
-   Hver liste over opdaterede profiler kan indeholde op til 100 tidsudsnit.
-   Status for fejl i **OperationSet** og fejllogfiler er ikke tilgængelige i øjeblikket.
-   Der må højst være 400 sprints pr. projekt.
-   [Begrænsninger og grænser for projekter og opgaver](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Etiketter er i øjeblikket kun tilgængelige for Project for the Web.

**Fejlhåndtering**

-   Hvis du vil gennemse de fejl, der er genereret i operationssæt, skal du gå til **Indstillinger** \> **Integration af planlægning** \> **Operationssæt**.
-   Hvis du vil gennemse de fejl, der er genereret fra projektplanlægningstjenesten, skal du gå til **Indstillinger** \> **Planlægning af integration** \> **PSS-fejllogfiler**.

**Redigering af profiler for ressourcetildeling**

I modsætning til alle andre API'er for projektplanlægning, der opdaterer et objekt, er API'en for profiler for ressourcetildelinger eneansvarlig for opdateringer af et enkelt felt, msdyn_plannedwork, på et enkelt objekt, msydn_resourceassignment.

Den angivne planlægningstilstand er:

-   **faste enheder**
-   projektkalender er 9-5p er 9-5pst, man, tir, tor, fre (INGEN ARBEJDSONSDAGE),
-   og ressourcekalenderen er 9-1p PST- man-fre

Denne tildeling gælder i en uge, fire timer om dagen. Det skyldes, at ressourcekalenderen er fra 9-1 PST eller fire timer om dagen.

| &nbsp;     | Opgave | Startdato | Slutdato  | Quantity | 13-06-2022 | 14-06-2022 | 15-06-2022 | 16-06-2022 | 17-06-2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 arbejder |  T1  | 13-06-2022  | 17-06-2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Hvis arbejderen f.eks. kun skal arbejde tre timer hver dag i denne uge, og der skal frigives én time til andre opgaver.

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours-eksempelnyttedata:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Dette er tildelingen, når API'en til opdatering af profilplanlægning er kørt.

| &nbsp;     | Opgave | Startdato | Slutdato  | Quantity | 13-06-2022 | 14-06-2022 | 15-06-2022 | 16-06-2022 | 17-06-2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 arbejder | T1   | 13-06-2022  | 17-06-2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Eksempelscenarie**

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

**Yderligere eksempler

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
