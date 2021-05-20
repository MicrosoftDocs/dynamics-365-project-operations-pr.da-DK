---
title: Integration af dobbeltskrivning i Project Operations
description: Dette emne indeholder en oversigt over Integration af dobbeltskrivning i Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955651"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="21861-103">Oversigt over integration af dobbeltskrivning i Project Operations</span><span class="sxs-lookup"><span data-stu-id="21861-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="21861-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="21861-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="21861-105">Project Operations bruger [funktioner til dobbeltskrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) til at synkronisere data på tværs af Microsoft Dataverse og Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="21861-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="21861-106">I følgende illustration vises, hvordan data synkroniseres som en del af denne integration mellem Dataverse og Finance.</span><span class="sxs-lookup"><span data-stu-id="21861-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Oversigt over dataflow i Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="21861-108">Project Operations på Dataverse indeholder en moderne brugergrænseflade (UI) og nem udvidelse uden kode/med lav kode ved hjælp af Power Platform-funktioner.</span><span class="sxs-lookup"><span data-stu-id="21861-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="21861-109">Projektledere, Resource Manager, medlemmer af projektteam og andre front office-personer udfører deres aktiviteter i Project Operations på Dataverse.</span><span class="sxs-lookup"><span data-stu-id="21861-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="21861-110">Project Operations i Finance understøtter projektregnskaber og indtægtsføring.</span><span class="sxs-lookup"><span data-stu-id="21861-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="21861-111">Project Operations-plugins til den økonomiske ramme i Finance til momsberegning, valutakurser, rapportering om økonomiske dimensioner og meget mere.</span><span class="sxs-lookup"><span data-stu-id="21861-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="21861-112">Projektrevisorens erfaringer findes primært i Finance.</span><span class="sxs-lookup"><span data-stu-id="21861-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="21861-113">Integration af Project Operations består af følgende komponentintegration:</span><span class="sxs-lookup"><span data-stu-id="21861-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="21861-114">Opsætning af Project Operations og konfiguration af dataintegration</span><span class="sxs-lookup"><span data-stu-id="21861-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="21861-115">Projektestimater og faktiske tal</span><span class="sxs-lookup"><span data-stu-id="21861-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="21861-116">Projektfakturaer</span><span class="sxs-lookup"><span data-stu-id="21861-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="21861-117">Udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="21861-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="21861-118">Leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="21861-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
