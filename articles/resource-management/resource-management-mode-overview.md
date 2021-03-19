---
title: Oversigt over tilstande for ressourcestyring
description: Dette emne indeholder oplysninger om funktionaliteten for ressourcestyring i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279446"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="c278b-103">Oversigt over tilstande for ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="c278b-103">Resource management modes overview</span></span>

<span data-ttu-id="c278b-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c278b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c278b-105">Dynamics 365 Project Operations understøtter to tilstande, således at du kan udføre den overordnede reservationsstrøm.</span><span class="sxs-lookup"><span data-stu-id="c278b-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="c278b-106">Administrationstilstanden defineres som en projekt parameter og kan ændres, hvis din virksomhed har behov for at skifte.</span><span class="sxs-lookup"><span data-stu-id="c278b-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="c278b-107">Central tilstand</span><span class="sxs-lookup"><span data-stu-id="c278b-107">Central mode</span></span>
<span data-ttu-id="c278b-108">For organisationer, der centraliserer fordelingen for ressourcer til projekter, er den centrale tilstand en måde, hvorpå det sikres, at projektledere kan definere ressourcekrav på projektniveau.</span><span class="sxs-lookup"><span data-stu-id="c278b-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="c278b-109">Opfyldelsen af ressourcekravene er uddelegeret til en Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="c278b-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="c278b-110">Projektledere kan acceptere eller afvise ressourcer, der er foreslået af Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="c278b-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Central tilstand](./media/resource-management-central.png)

<span data-ttu-id="c278b-112">Hvis du vil administrere ressourcer med den centrale tilstand, skal du se:</span><span class="sxs-lookup"><span data-stu-id="c278b-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="c278b-113">Tildel generiske reserverbare ressourcer til en opgave og generering af ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="c278b-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="c278b-114">Reserver navngivne ressourcer fra ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="c278b-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="c278b-115">Send en anmodning om ressource(r)</span><span class="sxs-lookup"><span data-stu-id="c278b-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="c278b-116">Opfyld en ressourceanmodning</span><span class="sxs-lookup"><span data-stu-id="c278b-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="c278b-117">Acceptere eller afvise en foreslået projektressource i en ressourceanmodning</span><span class="sxs-lookup"><span data-stu-id="c278b-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="c278b-118">Hybridtilstand</span><span class="sxs-lookup"><span data-stu-id="c278b-118">Hybrid mode</span></span>
<span data-ttu-id="c278b-119">For organisationer, der har behov for fleksibilitet i fordelingen af ressourcer, giver hybridtilstanden mulighed for, at både projektledere og Resource Manager kan reservere ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c278b-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybridtilstand](./media/resource-management-hybrid.png)

<span data-ttu-id="c278b-121">Ud over den understøttede centrale tilstand skal du se følgende emner for at administrere alle andre understøttede reservationsflows i hybridtilstanden:</span><span class="sxs-lookup"><span data-stu-id="c278b-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="c278b-122">Reserver en ressource direkte til et projekt:</span><span class="sxs-lookup"><span data-stu-id="c278b-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="c278b-123">Reservere navngivne reserverbare ressourcer til et projektteam og tildele opgaver</span><span class="sxs-lookup"><span data-stu-id="c278b-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="c278b-124">Reserver en ressource fra et ressourcekrav:</span><span class="sxs-lookup"><span data-stu-id="c278b-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="c278b-125">Tildel generiske reserverbare ressourcer til en opgave og generering af ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="c278b-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="c278b-126">Reserver navngivne ressourcer fra ressourcekrav</span><span class="sxs-lookup"><span data-stu-id="c278b-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]