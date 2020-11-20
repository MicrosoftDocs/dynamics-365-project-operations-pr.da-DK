---
title: Reserveringer vs. tildelinger
description: Dette emne indeholder oplysninger om forskellene mellem ressourcereservationer og ressourcetildelinger.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130211"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="c48b2-103">Reserveringer vs. tildelinger</span><span class="sxs-lookup"><span data-stu-id="c48b2-103">Bookings vs assignments</span></span>

<span data-ttu-id="c48b2-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c48b2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c48b2-105">Reservationer er definitiv eller foreløbig allokering af ressourcerne til et projekt.</span><span class="sxs-lookup"><span data-stu-id="c48b2-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="c48b2-106">Definitive reservationer forbruger en ressources kapacitet.</span><span class="sxs-lookup"><span data-stu-id="c48b2-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="c48b2-107">Reservationer repræsenterer organisationskoncepter for teams, så de kan forstå, hvordan ressourcer anvendes på tværs af forskellige projekter.</span><span class="sxs-lookup"><span data-stu-id="c48b2-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="c48b2-108">Dynamics 365 Project Operations anser reservationer for at være et koncept på projektniveau.</span><span class="sxs-lookup"><span data-stu-id="c48b2-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="c48b2-109">I modsætning til reservationer er tildelinger ressourcers forpligtelse til projektopgaver i projektplanen.</span><span class="sxs-lookup"><span data-stu-id="c48b2-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="c48b2-110">Ressourcerne kan navngives eller være generiske.</span><span class="sxs-lookup"><span data-stu-id="c48b2-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="c48b2-111">Summen af en ressources reservationer svarer typisk til summen af ressourcens tildelinger på tværs af en eller flere opgaver.</span><span class="sxs-lookup"><span data-stu-id="c48b2-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="c48b2-112">Project Operations gennemtvinger dog ikke denne aftale.</span><span class="sxs-lookup"><span data-stu-id="c48b2-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="c48b2-113">I visningen **Afstemning** kan projektlederen se de steder, hvor en ressources reservationer og tildelinger ikke stemmer overens med hinanden.</span><span class="sxs-lookup"><span data-stu-id="c48b2-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
