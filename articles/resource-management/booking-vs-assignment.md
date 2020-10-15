---
title: Reserveringer vs. tildelinger
description: Dette emne indeholder oplysninger om forskellene mellem ressourcereservationer og ressourcetildelinger.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896004"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="1168b-103">Reserveringer vs. tildelinger</span><span class="sxs-lookup"><span data-stu-id="1168b-103">Bookings vs assignments</span></span>

<span data-ttu-id="1168b-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="1168b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1168b-105">Reservationer er definitiv eller foreløbig allokering af ressourcerne til et projekt.</span><span class="sxs-lookup"><span data-stu-id="1168b-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="1168b-106">Definitive reservationer forbruger en ressources kapacitet.</span><span class="sxs-lookup"><span data-stu-id="1168b-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="1168b-107">Tildelinger er tildelingen af ressourcer til projektopgaver i projektplanen.</span><span class="sxs-lookup"><span data-stu-id="1168b-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="1168b-108">Ressourcerne kan være faktiske eller generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="1168b-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="1168b-109">Ideelt set skulle faktiske ressourcer, reservationer og tildelinger være i overensstemmelse med hinanden, eftersom de ikke er forskellige.</span><span class="sxs-lookup"><span data-stu-id="1168b-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="1168b-110">Microsoft Dynamics Project Operations gennemtvinger dog ikke denne aftale.</span><span class="sxs-lookup"><span data-stu-id="1168b-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="1168b-111">I visningen **Afstemning** vises en projektledersituation, hvor en ressources reservationer og tildelinger ikke er i overensstemmelse med hinanden.</span><span class="sxs-lookup"><span data-stu-id="1168b-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
