---
title: Projektskabeloner
description: Dette emne indeholder oplysninger om, hvordan du kan bruge projektskabeloner til hurtig opsætning af projekter.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074334"
---
# <a name="project-templates"></a><span data-ttu-id="01515-103">Projektskabeloner</span><span class="sxs-lookup"><span data-stu-id="01515-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="01515-104">En projektskabelon er en foruddefineret struktur, der gør det nemt og hurtigt at starte et projekt.</span><span class="sxs-lookup"><span data-stu-id="01515-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="01515-105">Du kan bruge en foruddefineret skabelon til at oprette et nyt projekt med et enkelt klik.</span><span class="sxs-lookup"><span data-stu-id="01515-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="01515-106">Som i forbindelse med projekter skal du definere forudsætningerne for projektskabeloner.</span><span class="sxs-lookup"><span data-stu-id="01515-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="01515-107">Du skal definere en projektkalender for de enkelte projektskabeloner, og roller og prislister skal være foruddefineret i organisationen, så der findes brugbare data til skabelonens komponenter.</span><span class="sxs-lookup"><span data-stu-id="01515-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="01515-108">En projektskabelon består af tre komponenter: en plan, projektestimater og medlemmer af projektteamet.</span><span class="sxs-lookup"><span data-stu-id="01515-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="01515-109">Planlæg</span><span class="sxs-lookup"><span data-stu-id="01515-109">Schedule</span></span>

<span data-ttu-id="01515-110">En tidsplan i en projektskabelon har samme sæt elementer som en tidsplan i et projekt.</span><span class="sxs-lookup"><span data-stu-id="01515-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="01515-111">Du kan oprette et opgavehierarki, knytte roller til opgaver, definere planlægningsattributter og angive afhængigheder.</span><span class="sxs-lookup"><span data-stu-id="01515-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="01515-112">En tidsplan i en projektskabelon understøtter også opgavetilstande for de enkelte opgaver.</span><span class="sxs-lookup"><span data-stu-id="01515-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="01515-113">Den understøtter derfor planlægningsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="01515-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="01515-114">Du skal knytte en projektkalender til projektet.</span><span class="sxs-lookup"><span data-stu-id="01515-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="01515-115">Når du opretter en arbejdsplan, er der ingen forskel mellem en projektskabelon og et projekt.</span><span class="sxs-lookup"><span data-stu-id="01515-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="01515-116">Projektestimater</span><span class="sxs-lookup"><span data-stu-id="01515-116">Project estimates</span></span>

<span data-ttu-id="01515-117">Projektestimater i en projektskabelon fungerer på samme måde som projektestimater i et projekt.</span><span class="sxs-lookup"><span data-stu-id="01515-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="01515-118">Kost- og salgspriserne trækkes dog fra de standardomkostnings- og prislister, der er defineret i parametrene.</span><span class="sxs-lookup"><span data-stu-id="01515-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="01515-119">Oprettelse af et projekt på baggrund af en skabelon</span><span class="sxs-lookup"><span data-stu-id="01515-119">Creating a project from a template</span></span>
 
<span data-ttu-id="01515-120">Du kan oprette et projekt på baggrund af en projektskabelon på flere måder:</span><span class="sxs-lookup"><span data-stu-id="01515-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="01515-121">Når du opretter et projekt fra tilbuddet, kan du vælge en projektskabelon i dialogboksen **Hurtig oprettelse: Projekt**</span><span class="sxs-lookup"><span data-stu-id="01515-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Dialogboksen Hurtig oprettelse: Projekt](media/project-11.png)

- <span data-ttu-id="01515-123">Når du opretter et projekt ved at vælge **Nyt projekt** vises siden **Projekt** , før posten gemmes.</span><span class="sxs-lookup"><span data-stu-id="01515-123">When you create a project by selecting **New Project** , the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="01515-124">I feltet **Vælg en skabelon** skal du vælge en af de foruddefinerede projektskabeloner i organisationen.</span><span class="sxs-lookup"><span data-stu-id="01515-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="01515-125">Brug **Opret projekt fra en skabelon** på siden **Skabelonobjekt**.</span><span class="sxs-lookup"><span data-stu-id="01515-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="01515-126">Kopiere komponenter fra en skabelon til et projekt</span><span class="sxs-lookup"><span data-stu-id="01515-126">Copying components of template to project</span></span>

<span data-ttu-id="01515-127">Når du kopierer komponenterne i en projektskabelon til et projekt, kan der opstå nogle få tilsidesættelser, afhængigt af indstillingerne i projektet.</span><span class="sxs-lookup"><span data-stu-id="01515-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="01515-128">Kopiere planen</span><span class="sxs-lookup"><span data-stu-id="01515-128">Copying the schedule</span></span>

<span data-ttu-id="01515-129">Når du kopierer planen fra en projektskabelon, anvendes arbejdstimer fra projektets kalender til opgaveplanlægningen, hvis projektet har en anden projektkalender end skabelonen.</span><span class="sxs-lookup"><span data-stu-id="01515-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="01515-130">Derved justeres planen, så den svarer til sikkerhedskopieringen af projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="01515-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="01515-131">Den første opgave på planen tager projektets startdato, og planen for resten af hierarkiet opdateres baseret på den varighed og de afhængigheder, der er angivet i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="01515-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="01515-132">Kopiere projektestimater</span><span class="sxs-lookup"><span data-stu-id="01515-132">Copying project estimates</span></span> 

<span data-ttu-id="01515-133">Når du kopierer på tværs af projektestimatlinjer, opdateres prislisterne.</span><span class="sxs-lookup"><span data-stu-id="01515-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="01515-134">Hvad angår listen over kostpriser, er disse opdateringer baseret på ejerskabsenheden for projektet.</span><span class="sxs-lookup"><span data-stu-id="01515-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="01515-135">For salgsprislisten er de baseret på kunden.</span><span class="sxs-lookup"><span data-stu-id="01515-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="01515-136">For projekter, der er knyttet til et salgsobjekt, bestemmes kost- og salgspriserne ud fra disse prislister.</span><span class="sxs-lookup"><span data-stu-id="01515-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="01515-137">Kopiere et projektteam</span><span class="sxs-lookup"><span data-stu-id="01515-137">Copying a project team</span></span>

<span data-ttu-id="01515-138">Når et projektteam kopieres fra en projektskabelon til et projekt, kopieres standardressourcerne sammen med de færdigheder og kompetencer, der er defineret i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="01515-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="01515-139">Standardressourcetildelinger bevares også, som de var, i projektskabelonen.</span><span class="sxs-lookup"><span data-stu-id="01515-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="01515-140">Navngivne ressourcer understøttes ikke i projektskabeloner.</span><span class="sxs-lookup"><span data-stu-id="01515-140">Named resources aren't supported in project templates.</span></span>