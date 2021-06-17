---
title: Oprette en projektskabelon
description: Sådan opretter du en projektskabelon i Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997234"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="c5143-103">Oprette en projektskabelon (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c5143-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c5143-104">Projektskabeloner sparer dig tid, hvis virksomheden regelmæssigt afgiver bud på lignende typer projekter.</span><span class="sxs-lookup"><span data-stu-id="c5143-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="c5143-105">De indeholder er standardsæt af roller og estimerede timer for en type projekt.</span><span class="sxs-lookup"><span data-stu-id="c5143-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="c5143-106">Kontoadministratorer og projektledere kan oprette projekter, der er baseret på en skabelon, eller de kan kopiere skabelonen og foretager en af deres egne.</span><span class="sxs-lookup"><span data-stu-id="c5143-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="c5143-107">Komponenter af projektskabelon</span><span class="sxs-lookup"><span data-stu-id="c5143-107">Components of project template</span></span>
 <span data-ttu-id="c5143-108">En projektskabelon består af tre komponenter:</span><span class="sxs-lookup"><span data-stu-id="c5143-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="c5143-109">**Arbejdsopgavehierarki**: Et arbejdsopgavehierarki i en projektskabelon har det samme sæt af elementer som i projektet.</span><span class="sxs-lookup"><span data-stu-id="c5143-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="c5143-110">Du kan oprette et opgavehierarki, knytte roller til opgaven, definere planlægningsattributter, angive afhængigheder og få vist alle data i Gantt.</span><span class="sxs-lookup"><span data-stu-id="c5143-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="c5143-111">Arbejdsopgavehierarkier i projektskabeloner understøtter også opgavetilstande for alle opgaver.</span><span class="sxs-lookup"><span data-stu-id="c5143-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="c5143-112">Der er ingen forskel mellem en projektskabelon og et projekt, når du opretter arbejdsplan.</span><span class="sxs-lookup"><span data-stu-id="c5143-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="c5143-113">**Projektestimater**: Projektestimater i skabeloner fungerer på samme måde som de gør i projekter, bortset fra prislister for standardomkostninger og salgspriser altid er standardomkostninger og salgsprislister, der er defineret i parametrene for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="c5143-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="c5143-114">Resten af funktionaliteten er den samme som i et projekt.</span><span class="sxs-lookup"><span data-stu-id="c5143-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="c5143-115">**Projektteamdannelse**: Når du danner en projektgruppe for en projektskabelon, kan du ikke reservere en navngivet ressource i en skabelon.</span><span class="sxs-lookup"><span data-stu-id="c5143-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="c5143-116">Du kan bruge **Opret projektteam** i arbejdsopgavehierarkier til at generere en række standardressourcer.</span><span class="sxs-lookup"><span data-stu-id="c5143-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="c5143-117">Du kan også angive de nødvendige færdigheder og kompetencer for standardressourcer.</span><span class="sxs-lookup"><span data-stu-id="c5143-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="c5143-118">Du kan ikke erstatte en standardressource med en reserverbar ressource i projektskabeloner.</span><span class="sxs-lookup"><span data-stu-id="c5143-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="c5143-119">Oprette et projekt på grundlag af skabelon</span><span class="sxs-lookup"><span data-stu-id="c5143-119">Create a project from a template</span></span>  
 <span data-ttu-id="c5143-120">Du kan oprette et projekt fra en skabelon på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="c5143-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="c5143-121">Når du opretter et projekt fra tilbuddet, kan du vælge en projektskabelon i projektets formular til hurtig oprettelse.</span><span class="sxs-lookup"><span data-stu-id="c5143-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="c5143-122">Når du opretter et projekt ved at klikke på **Nyt projekt**, vises projektformularen, før du gemmer posten.</span><span class="sxs-lookup"><span data-stu-id="c5143-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="c5143-123">Herfra kan du klikke på feltet **Vælg en skabelon** og vælge fra listen over foruddefinerede projektskabeloner i organisationen.</span><span class="sxs-lookup"><span data-stu-id="c5143-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="c5143-124">Klik på **Opret projekt fra en skabelon** på siden **Projektskabelon** for at oprette et projekt fra skabelonen.</span><span class="sxs-lookup"><span data-stu-id="c5143-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="c5143-125">Kopiere komponenter fra en skabelon til et projekt</span><span class="sxs-lookup"><span data-stu-id="c5143-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="c5143-126">Når du kopierer komponenter i en skabelon til et projekt, er der et par ting, du bør vide.</span><span class="sxs-lookup"><span data-stu-id="c5143-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="c5143-127">**Kopiere et arbejdsopgavehierarki**: Når du kopierer arbejdsopgavehierarkiet fra en projektskabelon, anvendes arbejdstimer fra projektets kalender til planlægning af opgaver, hvis projektet har en anden projektkalender end skabelonen.</span><span class="sxs-lookup"><span data-stu-id="c5143-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="c5143-128">Dette justerer planen for sikkerhedskopiering af projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="c5143-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="c5143-129">Den første opgave på arbejdsopgavehierarkiet tager ligeledes projektets startdato, så resten af opgavehierarkiplanlægningen opdateres baseret på varigheden og afhængigheder, der er angivet i skabelonens arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="c5143-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="c5143-130">**Kopiere projektestimater**: Når du kopierer på tværs af projektestimatlinjer, opdateres prislister baseret på den objekt, der er ejer af projektet, for kostprisliste og kunden for salgsprislisten.</span><span class="sxs-lookup"><span data-stu-id="c5143-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="c5143-131">Kostprisen og salgspriserne bestemmes fra disse prislister på projekter, der er knyttet til et salgsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c5143-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="c5143-132">**Kopiere en projektgruppe**: Når du kopierer projektgruppen fra skabelonen til et projekt, kopieres standardressourcerne på tværs af, sammen med de færdigheder og kompetencer, der er defineret i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="c5143-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="c5143-133">Standardressourcetildelinger bevares også i projektskabelonen.</span><span class="sxs-lookup"><span data-stu-id="c5143-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c5143-134">Se også</span><span class="sxs-lookup"><span data-stu-id="c5143-134">See Also</span></span>  
 [<span data-ttu-id="c5143-135">Vejledning til projektledere</span><span class="sxs-lookup"><span data-stu-id="c5143-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]