---
title: Ressourcestyringsvejledning
description: En vejledning til ressourcestyring i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750620"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="accc5-103">Vejledning til ressourcestyring (Project Service)</span><span class="sxs-lookup"><span data-stu-id="accc5-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="accc5-104">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funktionerne i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] hjælper dig med at finde de rette ressourcer på det rigtige tidspunkt til projektet og med at sikre, at alle ressourcer udnyttes effektivt.</span><span class="sxs-lookup"><span data-stu-id="accc5-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="accc5-105">Udnyt virksomhedens konsulenter effektivt med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="accc5-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="accc5-106">Disse giver dig de værktøjer, du skal bruge til at planlægge ressourcer baseret på kravene og tidsplanerne i forbindelse med konsulentprojekter og dine konsulenters færdigheder og tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="accc5-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="accc5-107">Du kan hurtigt finde de mest kvalificerede konsulenter, der er tilgængelige til at arbejde på projekter, og du kan nemt se, hvordan du bedre lægger tidsplaner for dem i løbet af hvert projekt.</span><span class="sxs-lookup"><span data-stu-id="accc5-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="accc5-108">Ressourceplanlægning hjælper dig med at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="accc5-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="accc5-109">Afstemme ressourcer med projekter baseret på, hvor godt ressourcernes færdigheder og kompetenceniveauer svarer til projektets ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="accc5-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="accc5-110">Afstemme en ressources tidsplan med en projektkalender baseret på ressourcens tilgængelighed og planlagte fridage.</span><span class="sxs-lookup"><span data-stu-id="accc5-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="accc5-111">Den farvekodede kalender giver dig visuelle stikord om tilgængeligheden af ressourcer.</span><span class="sxs-lookup"><span data-stu-id="accc5-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="accc5-112">Gennemse hver konsulents kapacitet og find ud af, hvordan denne kapacitet bruges i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="accc5-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="accc5-113">Dette kan hjælpe dig med at finde ud af, hvor en konsulent kan være over- eller underudnyttet, eller om de arbejder på fuld kapacitet.</span><span class="sxs-lookup"><span data-stu-id="accc5-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="accc5-114">Tildele en procentdel eller et bestemt antal timer for en arbejders kapacitet til et projekt.</span><span class="sxs-lookup"><span data-stu-id="accc5-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="accc5-115">Foretage grupperessourcereservationer.</span><span class="sxs-lookup"><span data-stu-id="accc5-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="accc5-116">Reservere ressourcer foreløbigt eller definitivt og konvertere foreløbige timer til definitive timer i ét trin.</span><span class="sxs-lookup"><span data-stu-id="accc5-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="accc5-117">Automatisk danne en projektgruppe baseret på ressourcer, der er defineret i et arbejdsopgavehierarki til et projekt.</span><span class="sxs-lookup"><span data-stu-id="accc5-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="accc5-118">Udføre ressourceanmodninger (reservér, foreslå, finde erstatningsressourcer).</span><span class="sxs-lookup"><span data-stu-id="accc5-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="accc5-119">Tildele ressourcer ud fra en central (ressourcestyring tildeler) eller hybrid model (bl.a. ressourcestyring kan tildele).</span><span class="sxs-lookup"><span data-stu-id="accc5-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="accc5-120">Du kan finde flere oplysninger om konfiguration af en central kontra hybrid ressourcestyringsmodel i [Konfigurere indstillinger for yderligere parametre (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="accc5-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="accc5-121">Du kan administrere ressourcer effektivt på tværs af projekter og sikre, at projekter bemandes hensigtsmæssigt.</span><span class="sxs-lookup"><span data-stu-id="accc5-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="accc5-122">Du skal udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="accc5-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="accc5-123">[Administrere anmodninger om ressourcer](../project-service/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="accc5-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="accc5-124">Afstemme dine konsulenters færdigheder og kompetencer med de rigtige projekter.</span><span class="sxs-lookup"><span data-stu-id="accc5-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="accc5-125">[Vise ressourcetilgængelighed](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="accc5-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="accc5-126">Se konsulenternes tilgængelighed i en kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="accc5-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="accc5-127">[Vise tidsforbrug for ressource](../project-service/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="accc5-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="accc5-128">Se procentdelen af tiden, din konsulenter er optaget i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="accc5-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="accc5-129">[Planlægge ressourcer til et projekt](../project-service/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="accc5-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="accc5-130">Planlægge konsulenter for et projekt.</span><span class="sxs-lookup"><span data-stu-id="accc5-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="accc5-131">Du kan finde flere oplysninger om at sende anmodninger om ressourcer for individuelle projekter under [Sende anmodninger om ressourcer](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="accc5-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="accc5-132">Se også</span><span class="sxs-lookup"><span data-stu-id="accc5-132">See Also</span></span>  
 <span data-ttu-id="accc5-133">[Oversigt over Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="accc5-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="accc5-134">[Administratorvejledning](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="accc5-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="accc5-135">[Vejledning til kundechefer](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="accc5-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="accc5-136">[Vejledning til projektledere](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="accc5-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="accc5-137">Tids-, udgifts- og samarbejdsvejledning</span><span class="sxs-lookup"><span data-stu-id="accc5-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
