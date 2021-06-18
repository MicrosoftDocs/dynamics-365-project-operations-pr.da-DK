---
title: Ofte stillede spørgsmål om ressourcestyring
description: Dette emne indeholder svar på ofte stillede spørgsmål om ressourcestyring.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008754"
---
# <a name="resource-management-faq"></a><span data-ttu-id="ed1b9-103">Ofte stillede spørgsmål om ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="ed1b9-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="ed1b9-104">Hvad er forskellen mellem et teammedlem og et ressourcebehov?</span><span class="sxs-lookup"><span data-stu-id="ed1b9-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="ed1b9-105">Et projektteammedlem kan tildeles til opgaver, der er reserveret eller overreserveret, og kan angives som godkender.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="ed1b9-106">Et ressourcekrav kan eksistere uden et projektteammedlem, som et kladdenotat om behov.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="ed1b9-107">Hvad er forskellen mellem foreslåede og foreløbigt reserverede timer?</span><span class="sxs-lookup"><span data-stu-id="ed1b9-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="ed1b9-108">Foreslåede timer og foreløbigt reserverede timer adskiller sig fra hinanden, hvad angår synlighed.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="ed1b9-109">Foreslåede timer er kun synlige for personalechefer og den projektleder, der startede efterspørgslen ved hjælp af en ressourceanmodning.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="ed1b9-110">Foreløbigt reserverede timer er synlige for alle, der har adgang til planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="ed1b9-111">Hvordan kan jeg se de foreløbigt reserverede timer for ressourcer i et team?</span><span class="sxs-lookup"><span data-stu-id="ed1b9-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="ed1b9-112">Foreløbige reservationer kan foretages, når du reserverer et ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="ed1b9-113">Ressourcer, der er foreløbigt reserveret til et projektteam, vises som teammedlemmer, der har foreløbigt reserverede timer.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="ed1b9-114">De vises også i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="ed1b9-115">Hvordan ændrer jeg de påkrævede timer samt start- og slutdatoerne for en ressource (generisk eller navngivet), som jeg har reserveret?</span><span class="sxs-lookup"><span data-stu-id="ed1b9-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="ed1b9-116">Når der er reserveret ressourcer, skal du vælge **Vedligehold reservationer** for at foretage eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="ed1b9-117">Hvilke ressourcetyper understøtter Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="ed1b9-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="ed1b9-118">**Bruger** og **Kontakt** er de eneste ressourcetyper, der understøttes i Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="ed1b9-119">Selvom du kan oprette andre typer ressourcer, (f.eks. **Udstyr** og **Gruppe**), understøttes ingen situationer med end-to-end-brug for dem.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="ed1b9-120">Hvad er forskellen på en tildeling og en reservation?</span><span class="sxs-lookup"><span data-stu-id="ed1b9-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="ed1b9-121">Tildelinger er tildelingen af ressourcer til projektopgaver i projektplanen.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="ed1b9-122">Ressourcerne kan være enten faktiske ressourcer eller generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="ed1b9-123">Reservationer er definitiv eller foreløbig allokering af ressourcerne til et projekt.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="ed1b9-124">Definitive reservationer forbruger en ressources kapacitet.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="ed1b9-125">Ideelt set skulle faktiske ressourcer, reservationer og tildelinger være i overensstemmelse med hinanden, eftersom de ikke er forskellige.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="ed1b9-126">PSA gennemtvinger dog ikke denne aftale.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="ed1b9-127">I visningen Afstemning vises en projektledersituation, hvor en ressources reservationer og tildelinger ikke er i overensstemmelse med hinanden.</span><span class="sxs-lookup"><span data-stu-id="ed1b9-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]