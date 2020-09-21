---
title: Projektindstillinger
description: Dette emne indeholder oplysninger om indstillinger for projektstyring.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750520"
---
# <a name="project-settings"></a><span data-ttu-id="c4de2-103">Projektindstillinger</span><span class="sxs-lookup"><span data-stu-id="c4de2-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c4de2-104">Brug følgende indstillinger for at få adgang til funktionerne til projektplanlægning.</span><span class="sxs-lookup"><span data-stu-id="c4de2-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="c4de2-105">Arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="c4de2-105">Work template</span></span>

<span data-ttu-id="c4de2-106">Du opretter en projektplan ved at oprette en projektkalenderskabelon, der definerer antallet af arbejdstimer pr. dag og eventuelle lukketider.</span><span class="sxs-lookup"><span data-stu-id="c4de2-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="c4de2-107">Du opretter en projektkalenderskabelon ved at knytte en arbejdsskabelon til feltet **Kalenderskabelon** for projektet.</span><span class="sxs-lookup"><span data-stu-id="c4de2-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="c4de2-108">Følg disse trin for at oprette en arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="c4de2-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="c4de2-109">I venstre navigationsrude i PSA skal du klikke på **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="c4de2-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="c4de2-110">På listesiden **Ressourcer** skal du åbne en brugerpost og derefter vælge **Vis arbejdstimer**.</span><span class="sxs-lookup"><span data-stu-id="c4de2-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c4de2-111">Sørg for at tillade pop op-vinduer på browsersiden.</span><span class="sxs-lookup"><span data-stu-id="c4de2-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="c4de2-112">Her kan du se de arbejdstimer, der er angivet for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c4de2-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="c4de2-113">På fanen **Månedsvisning** skal du klikke på **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="c4de2-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="c4de2-114">Der vises en liste med tre valgmuligheder:</span><span class="sxs-lookup"><span data-stu-id="c4de2-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="c4de2-115">Ny ugeplan</span><span class="sxs-lookup"><span data-stu-id="c4de2-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="c4de2-116">Arbejdsplan for én dag</span><span class="sxs-lookup"><span data-stu-id="c4de2-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="c4de2-117">Fri</span><span class="sxs-lookup"><span data-stu-id="c4de2-117">Time Off</span></span>

> ![Konfigurer indstillinger](media/project-13.png)

4. <span data-ttu-id="c4de2-119">Vælg **Ny ugeplan**, og angiv derefter indstillingerne for denne ressourceplanlægning.</span><span class="sxs-lookup"><span data-stu-id="c4de2-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="c4de2-120">Du kan angive en tilbagevendende ugentlig tidsplan, parametre for daglige timer, lukketider og meget mere.</span><span class="sxs-lookup"><span data-stu-id="c4de2-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="c4de2-121">Angiv datointervallet, vælg **Gem**, og klik derefter på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="c4de2-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="c4de2-122">Gå tilbage til listesiden **Ressourcer**, og vælg den ressource, du vil angive arbejdstimer for.</span><span class="sxs-lookup"><span data-stu-id="c4de2-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="c4de2-123">Vælg **Angiv kalender som** for at angive arbejdsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="c4de2-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="c4de2-124">I dialogboksen **Arbejdsskabelon** skal du angive et navn for arbejdsskabelonen og derefter vælge **Anvend.**</span><span class="sxs-lookup"><span data-stu-id="c4de2-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="c4de2-125">Du kan nu knytte arbejdsskabelonen til en skabelon for projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="c4de2-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="c4de2-126">Ressourceroller</span><span class="sxs-lookup"><span data-stu-id="c4de2-126">Resource roles</span></span>

<span data-ttu-id="c4de2-127">Udtrykket *Ressourcerolle* refererer til det sæt færdigheder, kompetencer og certificeringer, som en person skal have for at kunne udføre et bestemt sæt opgaver på et projekt.</span><span class="sxs-lookup"><span data-stu-id="c4de2-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="c4de2-128">PSA giver dig mulighed for at omkostningsbestemme og fakturere en ressources tid baseret på den rolle, ressourcen er knyttet til.</span><span class="sxs-lookup"><span data-stu-id="c4de2-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="c4de2-129">De enkelte organisationer skal konfigurere disse roller ved hjælp af den venstre navigationsrude i menuen **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="c4de2-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="c4de2-130">De enkelte organisationer skal konfigurere disse roller på siden **Aktive ressourcekategorier**.</span><span class="sxs-lookup"><span data-stu-id="c4de2-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="c4de2-131">Hvis du vil åbne denne side, skal du vælge **Ressourceroller** i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="c4de2-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="c4de2-132">Prislister</span><span class="sxs-lookup"><span data-stu-id="c4de2-132">Price lists</span></span>

<span data-ttu-id="c4de2-133">Prislisterne giver dig mulighed for at indstille kost- og salgspriser for ressourceroller, udgiftskategorier, produkter og andre elementer i en organisation.</span><span class="sxs-lookup"><span data-stu-id="c4de2-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="c4de2-134">Inden du angiver økonomiske estimater for det arbejde, der skal leveres til et projekt, skal du oprette en sikkerhedskopi af omkostnings- og prisliste.</span><span class="sxs-lookup"><span data-stu-id="c4de2-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="c4de2-135">I sektionen parametre skal du også konfigurere en standard omkostnings- og prisliste, der gælder for alle de projekter, der oprettes i organisationen.</span><span class="sxs-lookup"><span data-stu-id="c4de2-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="c4de2-136">På siden **Aktive projektparametre** skal du sørge for at konfigurere en omkostnings- og prisliste.</span><span class="sxs-lookup"><span data-stu-id="c4de2-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
