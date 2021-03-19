---
title: Opdater estimat ved fuldførelse
description: Dette emne indeholder oplysninger om opdatering af den projekterede indsats for et projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286421"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="cf09b-103">Opdater estimat ved fuldførelse</span><span class="sxs-lookup"><span data-stu-id="cf09b-103">Update estimate at completion</span></span>

<span data-ttu-id="cf09b-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="cf09b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cf09b-105">Det er almindeligt, at en projektleder reviderer de oprindelige estimater for en opgave.</span><span class="sxs-lookup"><span data-stu-id="cf09b-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="cf09b-106">Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning.</span><span class="sxs-lookup"><span data-stu-id="cf09b-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="cf09b-107">Vi anbefaler dog ikke, at projektledere ændrer de oprindelige tal, fordi den oprindelige projektplan repræsenterer den etablerede sande kilde for projektets tidsplan og omkostningsestimat, og alle projektets interessenter er blevet enige herom.</span><span class="sxs-lookup"><span data-stu-id="cf09b-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="cf09b-108">En projektleder kan ændre arbejdsindsatsen på opgaver på to måder:</span><span class="sxs-lookup"><span data-stu-id="cf09b-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="cf09b-109">Tilsidesæt standardestimeringen for fuldførelse med et nyt estimat for den faktiske resterende indsats på opgaven.</span><span class="sxs-lookup"><span data-stu-id="cf09b-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="cf09b-110">Tilsidesætte standardstatussen i procent med et nyt estimat for den faktiske indsats på opgaven.</span><span class="sxs-lookup"><span data-stu-id="cf09b-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="cf09b-111">Hver af disse fremgangsmåder medfører en genberegning af opgavens procentvise ETC, estimering ved fuldførelse (EAC) og status samt den forventede afvigelse i tidsforbrug på en opgave.</span><span class="sxs-lookup"><span data-stu-id="cf09b-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="cf09b-112">EAC, ETC og status i procenten for hovedopgaver genberegnes og giver en ny projektion af afvigelsen i tidsforbruget.</span><span class="sxs-lookup"><span data-stu-id="cf09b-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]