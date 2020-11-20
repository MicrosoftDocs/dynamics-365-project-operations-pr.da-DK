---
title: Udarbejd projektskabeloner med Kopier projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter projektskabeloner ved hjælp af den brugerdefinerede handling Kopier projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131606"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="5e154-103">Udarbejd projektskabeloner med Kopier projekt</span><span class="sxs-lookup"><span data-stu-id="5e154-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="5e154-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5e154-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5e154-105">Dynamics 365 Project Operations understøtter muligheden for at kopiere et projekt og tilbageføre eventuelle tildelinger til de standardressourcer, der repræsenterer rollen.</span><span class="sxs-lookup"><span data-stu-id="5e154-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="5e154-106">Kunder kan bruge denne funktion til at oprette grundlæggende projektskabeloner.</span><span class="sxs-lookup"><span data-stu-id="5e154-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="5e154-107">Når du vælger **Kopier projekt**, opdateres statussen for destinationsprojektet.</span><span class="sxs-lookup"><span data-stu-id="5e154-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="5e154-108">Brug **Statusårsag** til at bestemme, hvornår kopieringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="5e154-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="5e154-109">Hvis du vælge **Kopier projekt**, opdateres startdatoen for projektet også til den aktuelle startdato, hvis der ikke er registreret nogen destinationsdato i destinationsprojektobjektet.</span><span class="sxs-lookup"><span data-stu-id="5e154-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="5e154-110">Den brugerdefinerede handling for Kopier projekt</span><span class="sxs-lookup"><span data-stu-id="5e154-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="5e154-111">Navn</span><span class="sxs-lookup"><span data-stu-id="5e154-111">Name</span></span> 

<span data-ttu-id="5e154-112">**msdyn_KopierProjektV2**</span><span class="sxs-lookup"><span data-stu-id="5e154-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="5e154-113">Inputparametre</span><span class="sxs-lookup"><span data-stu-id="5e154-113">Input parameters</span></span>
<span data-ttu-id="5e154-114">Der er tre inputparametre:</span><span class="sxs-lookup"><span data-stu-id="5e154-114">There are three input parameters:</span></span>

| <span data-ttu-id="5e154-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e154-115">Parameter</span></span>          | <span data-ttu-id="5e154-116">Skriv</span><span class="sxs-lookup"><span data-stu-id="5e154-116">Type</span></span>   | <span data-ttu-id="5e154-117">Værdier</span><span class="sxs-lookup"><span data-stu-id="5e154-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="5e154-118">IndstillingKopierProjekt</span><span class="sxs-lookup"><span data-stu-id="5e154-118">ProjectCopyOption</span></span>  | <span data-ttu-id="5e154-119">String</span><span class="sxs-lookup"><span data-stu-id="5e154-119">String</span></span> | <span data-ttu-id="5e154-120">**{"fjernNavngivneRessourcer":sand}** eller **{"RydTeamsOgTildelinger": sand}**</span><span class="sxs-lookup"><span data-stu-id="5e154-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="5e154-121">KildeProjekt</span><span class="sxs-lookup"><span data-stu-id="5e154-121">SourceProject</span></span>      | <span data-ttu-id="5e154-122">Objektreference</span><span class="sxs-lookup"><span data-stu-id="5e154-122">Entity Reference</span></span> | <span data-ttu-id="5e154-123">Kildeprojekt</span><span class="sxs-lookup"><span data-stu-id="5e154-123">Source Project</span></span> |
| <span data-ttu-id="5e154-124">Destination</span><span class="sxs-lookup"><span data-stu-id="5e154-124">Target</span></span>             | <span data-ttu-id="5e154-125">Objektreference</span><span class="sxs-lookup"><span data-stu-id="5e154-125">Entity Reference</span></span> | <span data-ttu-id="5e154-126">Destinationsprojekt</span><span class="sxs-lookup"><span data-stu-id="5e154-126">Target Project</span></span> |


- <span data-ttu-id="5e154-127">**{"RydTeamsOgTildelinger":sand}**: Tre standardfunktionsmåder for Project til internettet og fjerner alle tildelinger og teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="5e154-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="5e154-128">**{"fjernNavngivneRessourcer": sand}** Standardfunktionsmåden for Project Operations og vil gendanne tildelinger til generiske ressourcer.</span><span class="sxs-lookup"><span data-stu-id="5e154-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="5e154-129">Du kan finde flere oplysninger om handlinger under [Anvend WEB-API-handlinger](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="5e154-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="5e154-130">Angiv de felter, der skal kopieres</span><span class="sxs-lookup"><span data-stu-id="5e154-130">Specify fields to copy</span></span> 
<span data-ttu-id="5e154-131">Når handlingen kaldes, kigger **Kopier projekt** på projektvisningen **Kopier projektkolonner** for at afgøre, hvilke felter der skal kopieres, når projektet kopieres.</span><span class="sxs-lookup"><span data-stu-id="5e154-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
