---
title: Udarbejd projektskabeloner med Kopier projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter projektskabeloner ved hjælp af den brugerdefinerede handling Kopier projekt.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005649"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="4f82e-103">Udarbejd projektskabeloner med Kopier projekt</span><span class="sxs-lookup"><span data-stu-id="4f82e-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="4f82e-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="4f82e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4f82e-105">Dynamics 365 Project Operations understøtter muligheden for at kopiere et projekt og tilbageføre eventuelle tildelinger til de standardressourcer, der repræsenterer rollen.</span><span class="sxs-lookup"><span data-stu-id="4f82e-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="4f82e-106">Kunder kan bruge denne funktion til at oprette grundlæggende projektskabeloner.</span><span class="sxs-lookup"><span data-stu-id="4f82e-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="4f82e-107">Når du vælger **Kopier projekt**, opdateres statussen for destinationsprojektet.</span><span class="sxs-lookup"><span data-stu-id="4f82e-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="4f82e-108">Brug **Statusårsag** til at bestemme, hvornår kopieringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="4f82e-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="4f82e-109">Hvis du vælge **Kopier projekt**, opdateres startdatoen for projektet også til den aktuelle startdato, hvis der ikke er registreret nogen destinationsdato i destinationsprojektobjektet.</span><span class="sxs-lookup"><span data-stu-id="4f82e-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="4f82e-110">Den brugerdefinerede handling for Kopier projekt</span><span class="sxs-lookup"><span data-stu-id="4f82e-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="4f82e-111">Navn</span><span class="sxs-lookup"><span data-stu-id="4f82e-111">Name</span></span> 

<span data-ttu-id="4f82e-112">**msdyn_KopierProjektV2**</span><span class="sxs-lookup"><span data-stu-id="4f82e-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="4f82e-113">Inputparametre</span><span class="sxs-lookup"><span data-stu-id="4f82e-113">Input parameters</span></span>
<span data-ttu-id="4f82e-114">Der er tre inputparametre:</span><span class="sxs-lookup"><span data-stu-id="4f82e-114">There are three input parameters:</span></span>

| <span data-ttu-id="4f82e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f82e-115">Parameter</span></span>          | <span data-ttu-id="4f82e-116">Skriv</span><span class="sxs-lookup"><span data-stu-id="4f82e-116">Type</span></span>   | <span data-ttu-id="4f82e-117">Værdier</span><span class="sxs-lookup"><span data-stu-id="4f82e-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="4f82e-118">IndstillingKopierProjekt</span><span class="sxs-lookup"><span data-stu-id="4f82e-118">ProjectCopyOption</span></span>  | <span data-ttu-id="4f82e-119">String</span><span class="sxs-lookup"><span data-stu-id="4f82e-119">String</span></span> | <span data-ttu-id="4f82e-120">**{"fjernNavngivneRessourcer":sand}** eller **{"RydTeamsOgTildelinger": sand}**</span><span class="sxs-lookup"><span data-stu-id="4f82e-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="4f82e-121">KildeProjekt</span><span class="sxs-lookup"><span data-stu-id="4f82e-121">SourceProject</span></span>      | <span data-ttu-id="4f82e-122">Objektreference</span><span class="sxs-lookup"><span data-stu-id="4f82e-122">Entity Reference</span></span> | <span data-ttu-id="4f82e-123">Kildeprojekt</span><span class="sxs-lookup"><span data-stu-id="4f82e-123">Source Project</span></span> |
| <span data-ttu-id="4f82e-124">Destination</span><span class="sxs-lookup"><span data-stu-id="4f82e-124">Target</span></span>             | <span data-ttu-id="4f82e-125">Objektreference</span><span class="sxs-lookup"><span data-stu-id="4f82e-125">Entity Reference</span></span> | <span data-ttu-id="4f82e-126">Destinationsprojekt</span><span class="sxs-lookup"><span data-stu-id="4f82e-126">Target Project</span></span> |


- <span data-ttu-id="4f82e-127">**{"RydTeamsOgTildelinger":sand}**: Tre standardfunktionsmåder for Project til internettet og fjerner alle tildelinger og teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="4f82e-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="4f82e-128">**{"fjernNavngivneRessourcer": sand}** Standardfunktionsmåden for Project Operations og vil gendanne tildelinger til generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="4f82e-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="4f82e-129">Du kan finde flere oplysninger om handlinger under [Anvend WEB-API-handlinger](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="4f82e-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="4f82e-130">Angiv de felter, der skal kopieres</span><span class="sxs-lookup"><span data-stu-id="4f82e-130">Specify fields to copy</span></span> 
<span data-ttu-id="4f82e-131">Når handlingen kaldes, kigger **Kopier projekt** på projektvisningen **Kopier projektkolonner** for at afgøre, hvilke felter der skal kopieres, når projektet kopieres.</span><span class="sxs-lookup"><span data-stu-id="4f82e-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="4f82e-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4f82e-132">Example</span></span>
<span data-ttu-id="4f82e-133">I følgende eksempel vises det, hvordan du kan kalde den brugerdefinerede handling **Kopier projekt** med angivelsen af parameteren **fjernNavngivneRessourcer**.</span><span class="sxs-lookup"><span data-stu-id="4f82e-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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