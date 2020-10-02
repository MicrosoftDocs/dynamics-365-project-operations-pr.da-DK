---
title: Opdater estimat ved fuldførelse
description: Dette emne indeholder oplysninger om opdatering af den projekterede indsats for et projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897759"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="6cfb6-103">Opdater estimat ved fuldførelse</span><span class="sxs-lookup"><span data-stu-id="6cfb6-103">Update estimate at completion</span></span>

<span data-ttu-id="6cfb6-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6cfb6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6cfb6-105">Det er almindeligt, at en projektleder reviderer de oprindelige estimater for en opgave.</span><span class="sxs-lookup"><span data-stu-id="6cfb6-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="6cfb6-106">Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning.</span><span class="sxs-lookup"><span data-stu-id="6cfb6-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="6cfb6-107">Vi anbefaler dog ikke, at projektledere ændrer de oprindelige tal, fordi den oprindelige projektplan repræsenterer den etablerede sande kilde for projektets tidsplan og omkostningsestimat, og alle projektets interessenter er blevet enige herom.</span><span class="sxs-lookup"><span data-stu-id="6cfb6-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="6cfb6-108">En projektleder kan ændre arbejdsindsatsen på opgaver på to måder:</span><span class="sxs-lookup"><span data-stu-id="6cfb6-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="6cfb6-109">Tilsidesæt standardestimeringen for fuldførelse med et nyt estimat for den faktiske resterende indsats på opgaven.</span><span class="sxs-lookup"><span data-stu-id="6cfb6-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="6cfb6-110">Tilsidesætte standardstatussen i procent med et nyt estimat for den faktiske indsats på opgaven.</span><span class="sxs-lookup"><span data-stu-id="6cfb6-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="6cfb6-111">Hver af disse fremgangsmåder medfører en genberegning af opgavens procentvise ETC, estimering ved fuldførelse (EAC) og status samt den forventede afvigelse i tidsforbrug på en opgave.</span><span class="sxs-lookup"><span data-stu-id="6cfb6-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="6cfb6-112">EAC, ETC og status i procenten for hovedopgaver genberegnes og giver en ny projektion af afvigelsen i tidsforbruget.</span><span class="sxs-lookup"><span data-stu-id="6cfb6-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
