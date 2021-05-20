---
title: Definer projektkalendere
description: Dette emne giver oplysninger om, hvordan du anvender en kalenderskabelon på et projekt til at spore projektplanen.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981293"
---
# <a name="define-project-calendars"></a><span data-ttu-id="d62eb-103">Definer projektkalendere</span><span class="sxs-lookup"><span data-stu-id="d62eb-103">Define project calendars</span></span>

<span data-ttu-id="d62eb-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="d62eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d62eb-105">Hvis du vil oprette og administrere et projekt, skal du anvende en kalenderskabelon på projektet.</span><span class="sxs-lookup"><span data-stu-id="d62eb-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="d62eb-106">I kalenderskabelonen defineres følgende projektattributter:</span><span class="sxs-lookup"><span data-stu-id="d62eb-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="d62eb-107">Arbejdstider, herunder start- og sluttid</span><span class="sxs-lookup"><span data-stu-id="d62eb-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="d62eb-108">Arbejdsdage</span><span class="sxs-lookup"><span data-stu-id="d62eb-108">Working days</span></span>
- <span data-ttu-id="d62eb-109">Kalenderundtagelser, f.eks. ikke-arbejdsdage</span><span class="sxs-lookup"><span data-stu-id="d62eb-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="d62eb-110">Den kalenderskabelon, der anvendes på et projekt, er en kopi af den kalenderskabelon, der er defineret i organisationens indstillinger.</span><span class="sxs-lookup"><span data-stu-id="d62eb-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="d62eb-111">Hvis du ændrer kalenderskabelonen, overføres disse ændringer ikke til projektets arbejdstider.</span><span class="sxs-lookup"><span data-stu-id="d62eb-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="d62eb-112">Hvis du vil ændre projektets arbejdstimer, skal der anvendes en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="d62eb-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="d62eb-113">Hvis du vil oprette en kalenderskabelon for din organisation, er der to nøglekrav:</span><span class="sxs-lookup"><span data-stu-id="d62eb-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="d62eb-114">Definér skabelonens ønskede arbejdstimer ved hjælp af en ny eller eksisterende ressource, der kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="d62eb-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="d62eb-115">Opret en ny kalenderskabelon, og knyt skabelonen til den ressource, der kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="d62eb-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="d62eb-116">**Definér arbejdstimerne for skabelonen**</span><span class="sxs-lookup"><span data-stu-id="d62eb-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="d62eb-117">Gå til **Ressourcer** \> **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="d62eb-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="d62eb-118">Opret en ny ressource, der skal refereres til i kalenderskabelonen, eller vælg en eksisterende ressource.</span><span class="sxs-lookup"><span data-stu-id="d62eb-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="d62eb-119">Vælg fanen **Arbejdstimer** for ressourcen, og fuldfør instruktionerne i [Angiv arbejdstimer for en ressource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) for at konfigurere kalenderreglerne.</span><span class="sxs-lookup"><span data-stu-id="d62eb-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="d62eb-120">**Opret en ny kalenderskabelon**</span><span class="sxs-lookup"><span data-stu-id="d62eb-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="d62eb-121">Gå til **Indstillinger** \> **Kalenderskabelon**.</span><span class="sxs-lookup"><span data-stu-id="d62eb-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="d62eb-122">Vælg **Ny**, og angiv et navn, en beskrivelse og en skabelonressource.</span><span class="sxs-lookup"><span data-stu-id="d62eb-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="d62eb-123">Når der refereres til en ressource i en kalenderskabelon, knyttes der en kopi af ressourcens kalender til kalenderskabelonen.</span><span class="sxs-lookup"><span data-stu-id="d62eb-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="d62eb-124">Hvis arbejdstimerne i den kopierede skabelon ændres, vil disse ændringer ikke blive overført til kalenderskabelonen.</span><span class="sxs-lookup"><span data-stu-id="d62eb-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="d62eb-125">Du kan nu knytte arbejdsskabelonen til en skabelon for projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="d62eb-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

