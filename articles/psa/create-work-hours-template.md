---
title: Opret en arbejdstidsskabelon
description: Dette emner beskriver, hvordan du opretter en arbejdstimeskabelon i Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981248"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="3e227-103">Oprette en arbejdstimeskabelon (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3e227-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3e227-104">Hvis du vil oprette og administrere et projekt, skal du anvende en kalenderskabelon på projektet.</span><span class="sxs-lookup"><span data-stu-id="3e227-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="3e227-105">I kalenderskabelonen defineres følgende projektattributter:</span><span class="sxs-lookup"><span data-stu-id="3e227-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="3e227-106">Arbejdstider, herunder start- og sluttid</span><span class="sxs-lookup"><span data-stu-id="3e227-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="3e227-107">Arbejdsdage</span><span class="sxs-lookup"><span data-stu-id="3e227-107">Working days</span></span>
- <span data-ttu-id="3e227-108">Kalenderundtagelser, f.eks. ikke-arbejdsdage</span><span class="sxs-lookup"><span data-stu-id="3e227-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="3e227-109">Den kalenderskabelon, der anvendes på et projekt, er en kopi af den kalenderskabelon, der er defineret i organisationens indstillinger.</span><span class="sxs-lookup"><span data-stu-id="3e227-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="3e227-110">Hvis du ændrer kalenderskabelonen, overføres disse ændringer ikke til projektets arbejdstider.</span><span class="sxs-lookup"><span data-stu-id="3e227-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="3e227-111">Hvis du vil ændre projektets arbejdstimer, skal der anvendes en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="3e227-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="3e227-112">Hvis du vil oprette en kalenderskabelon for din organisation, er der to nøglekrav:</span><span class="sxs-lookup"><span data-stu-id="3e227-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="3e227-113">Definér skabelonens ønskede arbejdstimer ved hjælp af en ny eller eksisterende ressource, der kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="3e227-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="3e227-114">Opret en ny kalenderskabelon, og knyt skabelonen til den ressource, der kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="3e227-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="3e227-115">**Definér arbejdstimerne for skabelonen**</span><span class="sxs-lookup"><span data-stu-id="3e227-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="3e227-116">Gå til **Ressourcer** \> **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="3e227-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="3e227-117">Opret en ny ressource, der skal refereres til i kalenderskabelonen, eller vælg en eksisterende ressource.</span><span class="sxs-lookup"><span data-stu-id="3e227-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="3e227-118">Vælg fanen **Arbejdstimer** for ressourcen, og fuldfør instruktionerne i [Angiv arbejdstimer for en ressource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) for at konfigurere kalenderreglerne.</span><span class="sxs-lookup"><span data-stu-id="3e227-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="3e227-119">**Opret en ny kalenderskabelon**</span><span class="sxs-lookup"><span data-stu-id="3e227-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="3e227-120">Gå til **Indstillinger** \> **Kalenderskabelon**.</span><span class="sxs-lookup"><span data-stu-id="3e227-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="3e227-121">Vælg **Ny**, og angiv et navn, en beskrivelse og en skabelonressource.</span><span class="sxs-lookup"><span data-stu-id="3e227-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="3e227-122">Når der refereres til en ressource i en kalenderskabelon, knyttes der en kopi af ressourcens kalender til kalenderskabelonen.</span><span class="sxs-lookup"><span data-stu-id="3e227-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="3e227-123">Hvis arbejdstimerne i den kopierede skabelon ændres, vil disse ændringer ikke blive overført til kalenderskabelonen.</span><span class="sxs-lookup"><span data-stu-id="3e227-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="3e227-124">Se også</span><span class="sxs-lookup"><span data-stu-id="3e227-124">See Also</span></span>  
 [<span data-ttu-id="3e227-125">Konfigurer ressourcer</span><span class="sxs-lookup"><span data-stu-id="3e227-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
