---
title: Udarbejd projektskabeloner med Kopier projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter projektskabeloner ved hjælp af den brugerdefinerede handling Kopier projekt.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045002"
---
# <a name="develop-project-templates-with-copy-project"></a>Udarbejd projektskabeloner med Kopier projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations understøtter muligheden for at kopiere et projekt og tilbageføre eventuelle tildelinger til de standardressourcer, der repræsenterer rollen. Kunder kan bruge denne funktion til at oprette grundlæggende projektskabeloner.

Når du vælger **Kopier projekt**, opdateres statussen for destinationsprojektet. Brug **Statusårsag** til at bestemme, hvornår kopieringen er fuldført. Hvis du vælge **Kopier projekt**, opdateres startdatoen for projektet også til den aktuelle startdato, hvis der ikke er registreret nogen destinationsdato i destinationsprojektobjektet.

## <a name="copy-project-custom-action"></a>Den brugerdefinerede handling for Kopier projekt 

### <a name="name"></a>Navn 

**msdyn_KopierProjektV2**

### <a name="input-parameters"></a>Inputparametre
Der er tre inputparametre:

| Parameter          | Skriv   | Værdier                                                   | 
|--------------------|--------|----------------------------------------------------------|
| IndstillingKopierProjekt  | String | **{"fjernNavngivneRessourcer":sand}** eller **{"RydTeamsOgTildelinger": sand}** |
| KildeProjekt      | Objektreference | Kildeprojekt |
| Destination             | Objektreference | Destinationsprojekt |


- **{"RydTeamsOgTildelinger":sand}**: Tre standardfunktionsmåder for Project til internettet og fjerner alle tildelinger og teammedlemmer.
- **{"fjernNavngivneRessourcer": sand}** Standardfunktionsmåden for Project Operations og vil gendanne tildelinger til generiske ressourcer.

Du kan finde flere oplysninger om handlinger under [Anvend WEB-API-handlinger](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Angiv de felter, der skal kopieres 
Når handlingen kaldes, kigger **Kopier projekt** på projektvisningen **Kopier projektkolonner** for at afgøre, hvilke felter der skal kopieres, når projektet kopieres.


### <a name="example"></a>Eksempel
I følgende eksempel vises det, hvordan du kan kalde den brugerdefinerede handling **Kopier projekt** med angivelsen af parameteren **fjernNavngivneRessourcer**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]