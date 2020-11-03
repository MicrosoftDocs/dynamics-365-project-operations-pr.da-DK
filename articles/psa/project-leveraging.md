---
title: Salgsestimater og projekter
description: Dette emne indeholder oplysninger om, hvordan du kan udnytte planlægning og estimater i salgsprocessen.
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
ms.openlocfilehash: eafe60362003198a223026526f56261de414bb4a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074190"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="10ec3-103">Salgsestimater og projekter</span><span class="sxs-lookup"><span data-stu-id="10ec3-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="10ec3-104">Under salgsprocessen kan du oprette salgsestimater ved at knytte et projekt til et salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="10ec3-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="10ec3-105">På denne måde kan der opstå deterministisk estimering under salgsprocessen for at drage nytte af funktionerne projektplanlægning og estimater.</span><span class="sxs-lookup"><span data-stu-id="10ec3-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="10ec3-106">Hvis salget går igennem, kan den planlægning, der blev brugt til salgsestimater, bruges som udgangspunkt for yderligere forbedringer i projektplanen.</span><span class="sxs-lookup"><span data-stu-id="10ec3-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="10ec3-107">Sammenkædning af et projekt med en tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="10ec3-107">Linking a project to a quote line</span></span>

<span data-ttu-id="10ec3-108">Når du opretter en projektbaseret tilbudslinje, kan du oprette et nyt projekt eller tilknytte et eksisterende projekt på siden **Tilbudslinje**.</span><span class="sxs-lookup"><span data-stu-id="10ec3-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Tilbudslinjeformular](media/project-8.png)
 
<span data-ttu-id="10ec3-110">Når du opretter et nyt projekt ud fra oplysningerne i tilbudslinjen, kan du drage fordel af projektskabeloner.</span><span class="sxs-lookup"><span data-stu-id="10ec3-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="10ec3-111">Projektskabeloner er modelprojekter, der repræsenterer standardprojektplaner og økonomiske estimater, som er typiske i en organisation.</span><span class="sxs-lookup"><span data-stu-id="10ec3-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="10ec3-112">De kan også repræsentere kopier af projektplaner og estimater fra tidligere projekter.</span><span class="sxs-lookup"><span data-stu-id="10ec3-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Tilbudslinjedetaljer](media/project-9.png)
  
<span data-ttu-id="10ec3-114">Når du opretter projektet fra tilbuddet, knyttes det automatisk til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="10ec3-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="10ec3-115">Komponenter i estimater i et projekt</span><span class="sxs-lookup"><span data-stu-id="10ec3-115">Components of estimates in a project</span></span>

<span data-ttu-id="10ec3-116">En tidsplan giver dig mulighed for at opdele arbejdet i opgaver, vedligeholde et opgavehierarki, finde ud af, hvilke ressourcer der kræves for at udføre en opgave, og lave et skøn over den indsats, der kræves for at udføre en opgave.</span><span class="sxs-lookup"><span data-stu-id="10ec3-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="10ec3-117">Du kan definere en arbejdsindsats og planlægge estimater ved hjælp af felterne på fanen **Tidsplan** på siden **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="10ec3-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="10ec3-118">Da der er knyttet en prisliste til projektet, beregnes de økonomiske estimater ved hjælp af kost- og salgspriser, der er defineret i prislisten.</span><span class="sxs-lookup"><span data-stu-id="10ec3-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="10ec3-119">Import af estimater fra et projekt til et tilbud</span><span class="sxs-lookup"><span data-stu-id="10ec3-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="10ec3-120">Når du har defineret projektestimater, kan du importere dem til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="10ec3-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="10ec3-121">På siden **Tilbudslinjedetaljer** skal du vælge **Import fra estimater** på båndet for at opsummere projektestimater efter transaktionstype, rolle eller opgaveniveau.</span><span class="sxs-lookup"><span data-stu-id="10ec3-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
