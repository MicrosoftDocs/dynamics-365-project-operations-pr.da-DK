---
title: Reservere navngivne ressourcer fra ressourcekrav
description: Denne emne indeholder oplysninger om at reservere navngivne ressourcer til et generisk ressourcekrav.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074377"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="c73d6-103">Reservere navngivne ressourcer fra ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="c73d6-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c73d6-104">Du kan reservere en navngivet ressource til at erstatte en generisk ressource, der har et ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="c73d6-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="c73d6-105">I Project Service Automation (PSA) skal du klikke på fanen **Team** på siden **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="c73d6-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="c73d6-106">Vælg den generiske ressource, der har et ressourcekrav, på listen, og klik derefter på **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="c73d6-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="c73d6-107">Du kan også åbne ressourcekravet og derefter klikke på **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="c73d6-107">Or, open the resource requirement and then click **Book**.</span></span>


![Reservation af et generisk teammedlem](media/RM-how-to-14.png)


3. <span data-ttu-id="c73d6-109">Vælg en navngivet ressource, der skal reserveres for projektteamet, på siden **Planlægningsassistent** , og klik derefter på **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="c73d6-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Reservation af et generisk teammedlem ved hjælp af planlægningsassistent](media/RM-how-to-15.png)

<span data-ttu-id="c73d6-111">Når reservationen er fuldført og opfyldt af en navngivet ressource, erstattes den generiske ressource med den navngivne ressource.</span><span class="sxs-lookup"><span data-stu-id="c73d6-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Navngivet teammedlem, der erstatter et generisk teammedlem](media/RM-how-to-16.png)

<span data-ttu-id="c73d6-113">Tildelingerne i tidsplanen opdateres også med den navngivne ressource.</span><span class="sxs-lookup"><span data-stu-id="c73d6-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Navngivet teammedlem, der er tildelt projektopgaver](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="c73d6-115">Indfri en generisk ressource med flere navngivne ressourcer</span><span class="sxs-lookup"><span data-stu-id="c73d6-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="c73d6-116">Indfrielse af et krav til en generisk ressource med flere navngivne ressourcer svarer til at tildele en enkelt navngivet ressource.</span><span class="sxs-lookup"><span data-stu-id="c73d6-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="c73d6-117">Der er f.eks. en opgave med en varighed på fem dage og 120 timer.</span><span class="sxs-lookup"><span data-stu-id="c73d6-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="c73d6-118">Denne opgave kan ikke udføres af én ressource, der fungerer som en normal ottetimers dag i en uge på fem dage.</span><span class="sxs-lookup"><span data-stu-id="c73d6-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![En opgave, der skal bruge 120 timers arbejde over fem dage](media/RM-how-to-21.png)

<span data-ttu-id="c73d6-120">Kravet er på 120 timers robotteknik over fem dage, hvilket er 24 timer om dagen.</span><span class="sxs-lookup"><span data-stu-id="c73d6-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Krav pr. dag](media/RM-how-to-22.png)

<span data-ttu-id="c73d6-122">Dette er et eksempel på, hvornår der skal bruges flere navngivne ressourcer til at indfri en generisk ressourceanmodning.</span><span class="sxs-lookup"><span data-stu-id="c73d6-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="c73d6-123">Du skal reservere flere ressourcer for at indfri kravet.</span><span class="sxs-lookup"><span data-stu-id="c73d6-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Reservation af flere ressourcer for at indfri kravet](media/RM-how-to-23.png)

<span data-ttu-id="c73d6-125">Den væsentligste forskel i dette scenarie er, at den generiske ressource forbliver i det team, der er tildelt opgaven, og teammedlemmer af den reserverede navngivne ressource er ikke tildelt som en del af stillingen.</span><span class="sxs-lookup"><span data-stu-id="c73d6-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="c73d6-126">Projektlederen kan tildele det arbejde, der er relevant for de navngivne ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c73d6-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="c73d6-127">**Afstemning** -visningen kan hjælpe en projektleder med at fordele reservationer på tværs af flere ressourcer til opgavetildelinger.</span><span class="sxs-lookup"><span data-stu-id="c73d6-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="c73d6-128">Dette sker ikke automatisk, da det i et hvilket som helst scenarie, der er mere kompliceret end det enkle eksempel overfor, f.eks. hvor du har et bundt opgaver, der udgør kravet, er projektlederens hensigt med tildelingen, der skal optages i systemet.</span><span class="sxs-lookup"><span data-stu-id="c73d6-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="c73d6-129">Da systemet ikke kan forstå hensigten, er det sandsynligt, at antagelserne vil være anderledes end forventet, og der opstår et forkert eller uforudsigeligt resultat.</span><span class="sxs-lookup"><span data-stu-id="c73d6-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="c73d6-130">Det forudsigelige resultat er, at den generiske ressource forbliver tildelt, indtil projektlederen bevidst opretter tildelinger med hjælp fra visningen **Afstemning**.</span><span class="sxs-lookup"><span data-stu-id="c73d6-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


