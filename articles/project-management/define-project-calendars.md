---
title: Definer projektkalendere
description: Dette emne indeholder oplysninger om, hvordan du bruger en projektkalender til at spore projektplanlægningen.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131651"
---
# <a name="define-project-calendars"></a><span data-ttu-id="ecae1-103">Definer projektkalendere</span><span class="sxs-lookup"><span data-stu-id="ecae1-103">Define project calendars</span></span>

<span data-ttu-id="ecae1-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="ecae1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ecae1-105">Du opretter en projektplan ved at oprette en projektkalenderskabelon, der definerer antallet af arbejdstimer pr. dag og eventuelle lukketider.</span><span class="sxs-lookup"><span data-stu-id="ecae1-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="ecae1-106">Du opretter en projektkalenderskabelon ved at knytte en arbejdsskabelon til feltet **Kalenderskabelon** for projektet.</span><span class="sxs-lookup"><span data-stu-id="ecae1-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="ecae1-107">Følg disse trin for at oprette en arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="ecae1-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="ecae1-108">I venstre navigationsrude skal du vælge **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="ecae1-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="ecae1-109">På listesiden **Ressourcer** skal du åbne en brugerpost og derefter vælge **Vis arbejdstimer**.</span><span class="sxs-lookup"><span data-stu-id="ecae1-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ecae1-110">Sørg for at tillade pop op-vinduer på browsersiden.</span><span class="sxs-lookup"><span data-stu-id="ecae1-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="ecae1-111">Her kan du se de arbejdstimer, der er angivet for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ecae1-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="ecae1-112">På fanen **Månedsvisning** skal du vælge **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="ecae1-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="ecae1-113">Der vises en liste med tre valgmuligheder:</span><span class="sxs-lookup"><span data-stu-id="ecae1-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="ecae1-114">Ny ugeplan</span><span class="sxs-lookup"><span data-stu-id="ecae1-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="ecae1-115">Arbejdsplan for én dag</span><span class="sxs-lookup"><span data-stu-id="ecae1-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="ecae1-116">Fri</span><span class="sxs-lookup"><span data-stu-id="ecae1-116">Time Off</span></span>

4. <span data-ttu-id="ecae1-117">Vælg **Ny ugeplan**, og angiv derefter indstillingerne for denne ressourceplanlægning.</span><span class="sxs-lookup"><span data-stu-id="ecae1-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="ecae1-118">Du kan angive en tilbagevendende ugentlig tidsplan, parametre for daglige timer, lukketider og meget mere.</span><span class="sxs-lookup"><span data-stu-id="ecae1-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="ecae1-119">Angiv datointervallet, vælg **Gem**, og vælg derefter **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ecae1-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="ecae1-120">Gå tilbage til listesiden **Ressourcer**, og vælg den ressource, du vil angive arbejdstimer for.</span><span class="sxs-lookup"><span data-stu-id="ecae1-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="ecae1-121">Vælg **Angiv kalender som** for at angive arbejdsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="ecae1-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="ecae1-122">I dialogboksen **Arbejdsskabelon** skal du angive et navn for arbejdsskabelonen og derefter vælge **Anvend.**</span><span class="sxs-lookup"><span data-stu-id="ecae1-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="ecae1-123">Du kan nu knytte arbejdsskabelonen til en skabelon for projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="ecae1-123">You can now associate the work template with a project calendar template.</span></span>
