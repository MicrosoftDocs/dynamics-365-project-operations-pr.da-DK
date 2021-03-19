---
title: Reserveringer vs. tildelinger
description: Dette emne indeholder oplysninger om forskellene mellem ressourcereservationer og ressourcetildelinger.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279896"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="67f2f-103">Reserveringer vs. tildelinger</span><span class="sxs-lookup"><span data-stu-id="67f2f-103">Bookings vs assignments</span></span>

<span data-ttu-id="67f2f-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="67f2f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="67f2f-105">Reservationer er definitiv eller foreløbig allokering af ressourcerne til et projekt.</span><span class="sxs-lookup"><span data-stu-id="67f2f-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="67f2f-106">Definitive reservationer forbruger en ressources kapacitet.</span><span class="sxs-lookup"><span data-stu-id="67f2f-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="67f2f-107">Reservationer repræsenterer organisationskoncepter for teams, så de kan forstå, hvordan ressourcer anvendes på tværs af forskellige projekter.</span><span class="sxs-lookup"><span data-stu-id="67f2f-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="67f2f-108">Dynamics 365 Project Operations anser reservationer for at være et projektniveaukoncept.</span><span class="sxs-lookup"><span data-stu-id="67f2f-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="67f2f-109">I modsætning til reservationer er tildelinger ressourcers forpligtelse til projektopgaver i projektplanen.</span><span class="sxs-lookup"><span data-stu-id="67f2f-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="67f2f-110">Ressourcerne kan navngives eller være generiske.</span><span class="sxs-lookup"><span data-stu-id="67f2f-110">The resources can be named or generic.</span></span>  <span data-ttu-id="67f2f-111">Når et ressourcekrav udledes af projektopgavetildelingerne, bruger Project Operations ressourcetildelingens indsatsprofiler til at opbygge profilerne i detaljerne for ressourcekravet.</span><span class="sxs-lookup"><span data-stu-id="67f2f-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="67f2f-112">En henvisning til ressourcetildelingerne bibeholdes dog ikke.</span><span class="sxs-lookup"><span data-stu-id="67f2f-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="67f2f-113">Opdateringer af de reservationer, der stammer fra ressourcekravet, opdaterer ikke ressourcetildelinger.</span><span class="sxs-lookup"><span data-stu-id="67f2f-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="67f2f-114">Summen af en ressources reservationer svarer typisk til summen af ressourcens tildelinger på tværs af en eller flere opgaver.</span><span class="sxs-lookup"><span data-stu-id="67f2f-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="67f2f-115">Project Operations gennemtvinger dog ikke denne aftale.</span><span class="sxs-lookup"><span data-stu-id="67f2f-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="67f2f-116">I visningen **Afstemning** kan projektlederen se de steder, hvor en ressources reservationer og tildelinger ikke stemmer overens med hinanden.</span><span class="sxs-lookup"><span data-stu-id="67f2f-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]