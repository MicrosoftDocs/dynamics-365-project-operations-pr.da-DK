---
title: Opfyldelse af generiske ressourcekrav
description: Denne emne indeholder oplysninger om at reservere navngivne ressourcer til et generisk ressourcekrav.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897579"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="7a85d-103">Opfyldelse af generiske ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="7a85d-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="7a85d-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="7a85d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7a85d-105">Du kan reservere en navngivet ressource til at erstatte en generisk ressource, der har et ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="7a85d-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="7a85d-106">På siden **Projekter** skal du vælge fanen **Team**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="7a85d-107">Vælg den generiske ressource, der har et ressourcekrav, på listen, og vælg derefter **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="7a85d-108">Du kan også åbne ressourcekravet og derefter vælge **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="7a85d-109">Vælg en navngivet ressource, der skal reserveres for projektteamet, på siden **Planlægningsassistent**, og vælg derefter **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="7a85d-110">Når reservationen er fuldført og opfyldt af en navngivet ressource, erstattes den generiske ressource med den navngivne ressource.</span><span class="sxs-lookup"><span data-stu-id="7a85d-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="7a85d-111">Tildelingerne i tidsplanen opdateres også med den navngivne ressource.</span><span class="sxs-lookup"><span data-stu-id="7a85d-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="7a85d-112">Indfri en generisk ressource med flere navngivne ressourcer</span><span class="sxs-lookup"><span data-stu-id="7a85d-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="7a85d-113">Indfrielse af et krav til en generisk ressource med flere navngivne ressourcer svarer til at tildele en enkelt navngivet ressource.</span><span class="sxs-lookup"><span data-stu-id="7a85d-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="7a85d-114">Der er f.eks. en opgave med en varighed på fem dage og 120 timer.</span><span class="sxs-lookup"><span data-stu-id="7a85d-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="7a85d-115">Denne opgave kan ikke udføres af én ressource, der fungerer som en normal ottetimers dag i en uge på fem dage.</span><span class="sxs-lookup"><span data-stu-id="7a85d-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="7a85d-116">Kravet er på 120 timers robotteknik over fem dage, hvilket er 24 timer om dagen.</span><span class="sxs-lookup"><span data-stu-id="7a85d-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="7a85d-117">Dette er et eksempel på, hvornår der skal bruges flere navngivne ressourcer til at indfri en generisk ressourceanmodning.</span><span class="sxs-lookup"><span data-stu-id="7a85d-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="7a85d-118">Du skal reservere flere ressourcer for at indfri kravet.</span><span class="sxs-lookup"><span data-stu-id="7a85d-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="7a85d-119">Den væsentligste forskel i dette scenarie er, at den generiske ressource forbliver i det team, der er tildelt opgaven, og teammedlemmer af den reserverede navngivne ressource er ikke tildelt som en del af stillingen.</span><span class="sxs-lookup"><span data-stu-id="7a85d-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="7a85d-120">Projektlederen kan tildele det arbejde, der er relevant for de navngivne ressourcer.</span><span class="sxs-lookup"><span data-stu-id="7a85d-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="7a85d-121">**Afstemning**-visningen kan hjælpe en projektleder med at fordele reservationer på tværs af flere ressourcer til opgavetildelinger.</span><span class="sxs-lookup"><span data-stu-id="7a85d-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="7a85d-122">Dette sker ikke automatisk, da det i et hvilket som helst scenarie, der er mere kompliceret end det enkle eksempel overfor, f.eks. hvor du har et bundt opgaver, der udgør kravet eller er projektlederens hensigt med tildelingen, der skal optages i systemet.</span><span class="sxs-lookup"><span data-stu-id="7a85d-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="7a85d-123">Da systemet ikke kan forstå hensigten, vil antagelserne sandsynligvis være anderledes end hensigten, og der opstår et forkert eller uforudsigeligt resultat.</span><span class="sxs-lookup"><span data-stu-id="7a85d-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="7a85d-124">Det forudsigelige resultat er, at den generiske ressource forbliver tildelt, indtil projektlederen bevidst opretter tildelinger med hjælp fra visningen **Afstemning**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>

