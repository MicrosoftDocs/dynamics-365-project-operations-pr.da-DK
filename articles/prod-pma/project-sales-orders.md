---
title: Projektsalgsordrer for tids- og materialeprojekter
description: I dette emne gives en beskrivelse af, hvordan du kan oprette projektbaserede salgsordrer for tids- og materialeprojekter.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074157"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="378f3-103">Projektsalgsordrer for tids- og materialeprojekter</span><span class="sxs-lookup"><span data-stu-id="378f3-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="378f3-104">Dette emne indeholder en beskrivelse af, hvordan du kan oprette en salgsordre for et projekt.</span><span class="sxs-lookup"><span data-stu-id="378f3-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="378f3-105">Der kan kun oprettes salgsordrer for projekter af typen **tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="378f3-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="378f3-106">Hvis et tids- og materialeprojekt har flere finansieringskilder i projektkontrakten, skal du aktivere parameteren **Tillad salgsordrer for projekter med flere finansieringskilder** på siden **Projektstyring og regnskabsparametre**.</span><span class="sxs-lookup"><span data-stu-id="378f3-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="378f3-107">Understøttelse af projektsalgsordrer med flere finansieringskilder er tilgængelig fra og med programfrigivelse 10.0.2 og nyere.</span><span class="sxs-lookup"><span data-stu-id="378f3-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="378f3-108">Den parameter, der bruges til at aktivere understøttelsen af projektsalgsordrer med flere finansieringskilder, fjernes i frigivelsesbølgende i april 2020, hvorefter funktionaliteten altid vil være aktiveret.</span><span class="sxs-lookup"><span data-stu-id="378f3-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="378f3-109">Du kan oprette projektbaserede salgsordrer på to måder:</span><span class="sxs-lookup"><span data-stu-id="378f3-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="378f3-110">Gå til selve projektet.</span><span class="sxs-lookup"><span data-stu-id="378f3-110">Go to the project itself.</span></span> <span data-ttu-id="378f3-111">Vælg **Administrer > Vareopgaver > Salgsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="378f3-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="378f3-112">Projektoplysningerne anvendes som standard for salgsordren fra projektet.</span><span class="sxs-lookup"><span data-stu-id="378f3-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="378f3-113">Hvis projektkontrakten har mere end én finansieringskilde, skal du vælge den finansieringskilde, der skal bruges til at angive kunden til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="378f3-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="378f3-114">Hvis der kun er én finansieringskilde for projektet, angives kunden automatisk.</span><span class="sxs-lookup"><span data-stu-id="378f3-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="378f3-115">Gå til listesiden **Alle salgsordre** , og opret en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="378f3-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="378f3-116">Du skal vælge projektet for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="378f3-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="378f3-117">Når projektet er valgt, angives kunden fra finansieringskilden, ellers skal du vælge finansieringskilden, hvis projektkontrakten har flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="378f3-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>
