---
title: Udarbejd projektskabeloner med Kopier projekt
description: Denne artikel indeholder oplysninger om, hvordan du opretter projektskabeloner ved hjælp af den brugerdefinerede handling Kopiér projekt.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923825"
---
# <a name="develop-project-templates-with-copy-project"></a>Udarbejd projektskabeloner med Kopier projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations understøtter muligheden for at kopiere et projekt og tilbageføre eventuelle tildelinger til de standardressourcer, der repræsenterer rollen. Kunder kan bruge denne funktion til at oprette grundlæggende projektskabeloner.

Når du vælger **Kopier projekt**, opdateres statussen for destinationsprojektet. Brug **Statusårsag** til at bestemme, hvornår kopieringen er fuldført. Hvis du vælge **Kopier projekt**, opdateres startdatoen for projektet også til den aktuelle startdato, hvis der ikke er registreret nogen destinationsdato i destinationsprojektobjektet.

## <a name="copy-project-custom-action"></a>Den brugerdefinerede handling for Kopier projekt

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Inputparametre

Der er tre inputparametre:

- **ReplaceNamedResources** eller **ClearTeamsAndAssignments** – Angiv kun én af indstillingerne. Du skal ikke angive begge.

    - **\{"ReplaceNamedResources":true\}** – Standardfunktionsmåden for Project Operations. Alle navngivne ressourcer erstattes med generiske ressourcer.
    - **\{"ClearTeamsAndAssignments":true\}** – Standardfunktionsmåden for Project for the Web. Alle tildelinger og teammedlemmer fjernes.

- **SourceProject** – Objektreferencen for det kildeprojekt, der skal kopieres fra. Dette parameter kan ikke være null.
- **Destination** – Objektreferencen for det destinationsprojekt, der skal kopieres til. Dette parameter kan ikke være null.

I følgende tabel vises en oversigt over de tre parametre.

| Parameter                | Skriv             | Værdi                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Sandt** eller **Falsk** |
| ClearTeamsAndAssignments | Boolean          | **Sandt** eller **Falsk** |
| KildeProjekt            | Objektreference | Kildeprojektet    |
| Target                   | Objektreference | Destinationsprojektet    |

Du kan finde flere oplysninger om handlinger under [Anvend WEB-API-handlinger](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Valideringer

Følgende valideringer udføres.

1. Null-kontrollerer og henter kilde- og destinationsprojektet for at bekræfte, at begge projekter findes i organisationen.
2. Systemet validerer, at destinationsprojektet er gyldigt til kopiering, ved at kontrollere følgende betingelser:

    - Der er ingen tidligere aktiviteter i projektet (herunder valg af fanen **Opgaver**), og projektet er nyoprettede.
    - Der er ingen tidligere kopi, der er ikke anmodet om import til dette projekt, og projektet har ikke statussen **Mislykkedes**.

3. Handlingen kaldes ikke ved hjælp af HTTP.

## <a name="specify-fields-to-copy"></a>Angiv de felter, der skal kopieres

Når handlingen kaldes, kigger **Kopier projekt** på projektvisningen **Kopier projektkolonner** for at afgøre, hvilke felter der skal kopieres, når projektet kopieres.

### <a name="example"></a>Eksempel

I følgende eksempel vises, hvordan du kan kalde den brugerdefinerede handling **CopyProjectV3**, hvor parameteren **removeNamedResources** er angivet.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
