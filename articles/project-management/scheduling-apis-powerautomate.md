---
title: Brug API'er til projektplanlægning med Power Automate
description: Denne artikel indeholder et eksempelflow, der bruger API'erne for projektplanlægning (programmeringsgrænseflader).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2527375ff3f3d631f3bb3de1458abb3b8838db54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916327"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Brug API'er til projektplanlægning med Power Automate

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Denne artikel beskriver et eksempelflow, som viser, hvordan du opretter en komplet projektplan ved hjælp af Microsoft Power Automate, hvordan du opretter et operationssæt, og hvordan du kan opdatere et objekt. I eksemplet vises, hvordan du opretter et projekt, et projektteammedlem, operationssæt, projektopgaver og ressourcetildelinger. Denne artikel forklarer også, hvordan du kan opdatere et objekt og udføre et handlingssæt.

Her følger en fuldstændig liste over de trin, der dokumenteres i eksempelflowet i denne artikel:

1. [Opret en PowerApps-udløser](#1)
2. [Opret et projekt](#2)
3. [Initialiser en variabel for teammedlemmerne](#3)
4. [Opret et generisk teammedlem](#4)
5. [Opret et handlingssæt](#5)
6. [Opret en projekt-bucket](#6)
7. [Initialiser en variabel for linkstatussen](#7)
8. [Initialiser en variabel for antallet af opgaver](#8)
9. [Initialiser en variabel for projektopgave-id'et](#9)
10. [Gør dette, indtil](#10)
11. [Angiv en projektopgave](#11)
12. [Opret en projektopgave](#12)
13. [Opret en ressourcetildeling](#13)
14. [Reducér en variabel](#14)
15. [Omdøb en projektopgave](#15)
16. [Kør et handlingssæt](#16)

## <a name="assumptions"></a>Forudsætninger

I denne artikel antages det, at du har en grundlæggende viden om Dataverse-platformen, cloudflow og API'en (programmeringsgrænseflader) til projektplanlægning. Du kan finde flere oplysninger i afsnittet [Referencer](#references) senere i denne artikel.

## <a name="create-a-flow"></a>Opret et flow

### <a name="select-an-environment"></a>Vælg et miljø

Du kan oprette flowet Power Automate i dit miljø.

1. Gå til <https://flow.microsoft.com>, og brug dine administratorlegitimationsoplysninger til at logge ind.
2. Vælg **Miljøer** i øverste højre hjørne.
3. Vælg det miljø på listen, hvor Dynamics 365 Project Operations er installeret.

### <a name="create-a-solution"></a>Opret en løsning

Følg disse trin for at oprette et [løsningsorienteret flow](/power-automate/overview-solution-flows). Ved at oprette et løsningsafhængigt flow kan du nemmere eksportere flowet, så du kan bruge det senere.

1. Vælg **Løsninger** i navigationsruden.
2. På siden **Løsninger** skal du vælge **Nu løsning**.
3. I dialogboksen **Ny løsning** skal du angive de krævede felter og dernæst vælge **Opret**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Trin 1: Opret en PowerApps-udløser

1. På siden **Løsninger** skal du vælge den løsning, som du har oprettet, og derefter vælge **Ny**.
2. I venstre rude skal du vælge **Cloudflows** \> **Automation** \> **Cloudflow** \> **Omgående**
3. I feltet **Flownavn** skal du angive **Planlægnings-API Demoflow**.
4. På listen **Vælg, hvordan denne proces skal udløses** skal du vælge **Power Apps**. Når du opretter en Power Apps-udløser, er logikken op til dig som forfatter. I denne artikel skal du lade inputparametrene stå tomme med henblik på test.
5. Vælg **Opret**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Trin 2: Oprette et projekt

Følg disse trin for at oprette et prøveprojekt.

1. Vælg **Nyt trin** i det flow, du har oprettet.

    ![Tilføj et nyt trin.](media/newstep.png)

2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **udfør ubundet handling**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.

    ![Valg en handling.](media/chooseactiontab.png)

3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.

![Omdøb et trin.](media/renamestep.png)

4. Omdøb trinnet **Opret projekt**.
5. I feltet **Handlingsnavn** skal du vælge **msdyn\_CreateProjectV1**.
6. I feltet **msdyn\_emne** skal du vælge **Tilføj dynamisk indhold**.
7. På fanen **Udtryk** skal du i funktionsfeltet angive **Projektnavn – utcNow()**.
8. Vælg **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Trin 3: Initialiser en variabel for teammedlemmet

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **initialiser variabel**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet til **Init-teammedlem**.
5. I feltet **Navn** skal du angive **TeamMemberAction**.
6. I feltet **Type** skal du vælge **Streng**.
7. I feltet **Værdi** skal du angive **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Trin 4: Opret et generisk projektteammedlem

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **udfør ubundet handling**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet til **Opret teammedlem**.
5. I feltet **Handlingsnavn** skal du vælge **TeamMemberAction** i dialogboksen **Dynamisk indhold**.
6. Angiv følgende parameteroplysninger i feltet **Handlingsparametre**.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Her er en forklaring på parametrene:

    - **\@\@odata.type** – Objektets navn. Skriv f.eks. **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – Den primære nøgle til projektteam-id'et. Værdien er et Globally Unique Identifier-udtryk (GUID).   Id'et oprettes under fanen Udtryk.

    - **msdyn\_project\@odata.bind** – Projekt-id'et for det ejende projekt. Værdien er dynamisk indhold, som kommer fra responsen på trinnet "Opret projekt". Sørg for at angive hele stien, og tilføj dynamisk indhold mellem parenteserne. Der skal bruges anførselstegn. Skriv f.eks. **"/msdyn\_projects(TILFØJ DYNAMISK INDHOLD)"**.
    - **msdyn\_name** – Navnet på teammedlemmet. Skriv f.eks. **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Trin 5: Opret et handlingssæt

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **udfør ubundet handling**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet **Opret handlingssæt**.
5. I feltet **Handlingsnavn** skal du vælge den brugerdefinerede handling **msdyn\_CreateOperationSetV1** i Dataverse.
6. I feltet **Beskrivelse** skal du indtaste **ScheduleAPIDemoOperationSet**.
7. I feltet **Projekt** skal du angive **/msdyn\_projects(**.
8. I dialogboksen **Dynamisk indhold** skal du vælge **msdyn\_CreateProjectV1Response ProjectId**.
9. I feltet **Projekt** skal du angive **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Trin 6: Opret en projekt-bucket

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **tilføj ny række**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet **Opret bucket**.
5. I feltet **Tabelnavn** skal du vælge **Projekt-buckets**.
6. I feltet **Navn** skal du angive **ScheduleAPIDemoBucket1**.
7. Til feltet **Projekt** skal du vælge **msdyn\_CreateProjectV1Response ProjectId** i dialogboksen **Dynamisk indhold**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Trin 7: Initialiser en variabel for linkstatussen

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **initialiser variabel**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet **Init linkstatus**.
5. I feltet **Navn** skal du angive **linkstatus**.
6. I feltet **Type** skal du vælge **Heltal**.
7. I feltet **Værdi** skal du angive **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Trin 8: Initialiser en variabel for antallet af opgaver

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **initialiser variabel**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet **Init Antal opgaver**.
5. I feltet **Navn** skal du angive **antal opgaver**.
6. I feltet **Type** skal du vælge **Heltal**.
7. I feltet **Værdi** skal du angive **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Trin 9: Initialiser en variabel for projektopgave-id'et

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **initialiser variabel**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet til **Init-ProjectTaskID**.
5. I feltet **Navn** skal du angive **antal opgaver**.
6. I feltet **Type** skal du vælge **Streng**.
7. I feltet **Værdi** skal du angive **guid()** i udtryksbyggeren.

## <a name="step-10-do-until"></a><a id="10"></a>Trin 10: Gør dette, indtil

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **gør, indtil**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. Angiv den første værdi i den betingede sætning til **antallet af opgavevariabler** i dialogboksen **Dynamisk indhold**.
4. Angiv betingelsen til **mindre end lig med**.
5. Angiv den anden værdi i den betingede sætning til **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Trin 11: Angiv en projektopgave

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **angiv variabel**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I det nye trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet til **Angiv projektopgave**.
5. I feltet **Navn** skal du vælge **msdyn\_projecttaskid**.
6. I feltet **Værdi** skal du angive **guid()** i udtryksbyggeren.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Trin 12: Opret en projektopgave

Følg disse trin for at oprette en projektopgave, der har et entydigt id, som tilhører det aktuelle projekt, og det projekt, du har oprettet.

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **udfør ubundet handling**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I dette trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet til **Opret projektopgave**.
5. I feltet **Handlingsnavn** skal du vælge **msdyn\_PssCreateV1**.
6. Angiv følgende parameteroplysninger i feltet **Objekt**.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Her er en forklaring på parametrene:

    - **\@\@odata.type** – Objektets navn. Skriv f.eks. **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – Opgavens entydige id. Værdien skal angives til en dynamisk variabel fra **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – Projekt-id'et for det ejende projekt. Værdien er dynamisk indhold, som kommer fra responsen på trinnet "Opret projekt". Sørg for at angive hele stien, og tilføj dynamisk indhold mellem parenteserne. Der skal bruges anførselstegn. Skriv f.eks. **"/msdyn\_projects(TILFØJ DYNAMISK INDHOLD)"**.
    - **msdyn\_subject** – Et hvilket som helst opgavenavn
    - **msdyn\_projectbucket\@odata.bind** – Den projekt-bucket, der indeholder opgaverne. Værdien er dynamisk indhold, som kommer fra responsen på trinnet "Opret bucket". Sørg for at angive hele stien, og tilføj dynamisk indhold mellem parenteserne. Der skal bruges anførselstegn. Skriv f.eks. **"/msdyn\_projectbuckets(TILFØJ DYNAMISK INDHOLD)"**.
    - **msdyn\_start** – Dynamisk indhold til startdatoen. I morgen vises f.eks. som **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Den planlagte startdato. I morgen vises f.eks. som **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Den planlagte slutdato. Vælg en dato i fremtiden. Angiv f.eks. **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Linkstatussen. Angiv f.eks. **"192350000"**.

7. Til feltet **OperationSetId** skal du vælge **msdyn\_CreateOperationSetV1Response** i dialogboksen **Dynamisk indhold**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Trin 13: Opret en ressourcetildeling

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **udfør ubundet handling**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I dette trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet **Opret tildeling**.
5. I feltet **Handlingsnavn** skal du vælge **msdyn\_PssCreateV1**.
6. Angiv følgende parameteroplysninger i feltet **Objekt**.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Til feltet **OperationSetId** skal du vælge **msdyn\_CreateOperationSetV1Response** i dialogboksen **Dynamisk indhold**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Trin 14: Reducér en variabel

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **reducér variabel**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I feltet **Navn** skal du vælge **antal opgaver**.
4. I feltet **Værdi** skal du angive **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Trin 15: Omdøb en projektopgave

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **udfør ubundet handling**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I dette trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet til **Omdøb projektopgave**.
5. I feltet **Handlingsnavn** skal du vælge **msdyn\_PssUpdateV1**.
6. Angiv følgende parameteroplysninger i feltet **Objekt**.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Til feltet **OperationSetId** skal du vælge **msdyn\_CreateOperationSetV1Response** i dialogboksen **Dynamisk indhold**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Trin 16: Kør et handlingssæt

1. Vælg **Nyt trin** i flowet.
2. I dialogboksen **Vælg en handling** skal du i søgefeltet angive **udfør ubundet handling**. Vælg derefter handlingen i listen over resultater på fanen **Handlinger**.
3. I dette trin skal du vælge ellipsen (**...**) og derefter vælge **Omdøb**.
4. Omdøb trinnet **Udfør handlingssæt**.
5. I feltet **Handlingsnavn** skal du vælge **msdyn\_ExecuteOperationSetV1**.
6. Til feltet **OperationSetId** skal du vælge **msdyn\_CreateOperationSetV1Response OperationSetId** i dialogboksen **Dynamisk indhold**.

## <a name="references"></a>Referencer

- [Oversigt over, hvordan du integrerer flows med Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Brug projektplanlægnings-API'er til at udføre handlinger med planlægningsobjekter](schedule-api-preview.md)
- [Oversigt over cloudflows - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Oversigt over løsningsbaserede flows - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
