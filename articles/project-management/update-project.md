---
title: Opdater et projekt
description: Dette emne indeholder oplysninger om opdatering af projekter i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286376"
---
# <a name="update-a-project"></a><span data-ttu-id="65078-103">Opdater et projekt</span><span class="sxs-lookup"><span data-stu-id="65078-103">Update a project</span></span>

<span data-ttu-id="65078-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="65078-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="65078-105">Nedenfor vises en oversigt over de felter, der kan opdateres i et projekt, efter at det er blevet oprettet, og eventuelle relevante konsekvenser af opdateringerne.</span><span class="sxs-lookup"><span data-stu-id="65078-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="65078-106">Felter med projektdetaljer</span><span class="sxs-lookup"><span data-stu-id="65078-106">Project detail fields</span></span>

- <span data-ttu-id="65078-107">**Navn**: Projektets titel.</span><span class="sxs-lookup"><span data-stu-id="65078-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="65078-108">**Beskrivelse**: En oversigt over projektet.</span><span class="sxs-lookup"><span data-stu-id="65078-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="65078-109">**Kunde**: Den virksomhed, som projektet skal leveres til.</span><span class="sxs-lookup"><span data-stu-id="65078-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="65078-110">**Kalenderskabelon**: Projektets arbejdstid.</span><span class="sxs-lookup"><span data-stu-id="65078-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="65078-111">Når feltet ændres, genberegnes hele planen.</span><span class="sxs-lookup"><span data-stu-id="65078-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="65078-112">**Valuta**: Valutaen for projektet.</span><span class="sxs-lookup"><span data-stu-id="65078-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="65078-113">Dette felts standardindstillinger er baseret på den valuta, der er defineret i kontraktenheden.</span><span class="sxs-lookup"><span data-stu-id="65078-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="65078-114">Når kontraktenheden opdateres, opdateres feltet også.</span><span class="sxs-lookup"><span data-stu-id="65078-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="65078-115">**Kontraktenhed**: Den organisationsenhed, der repræsenterer den virksomhedsgruppe eller division, som primært er ansvarlig for at vinde salg og administrere levering af arbejde og servicer til kunden.</span><span class="sxs-lookup"><span data-stu-id="65078-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="65078-116">**Projektleder**: Det medlem af projektteamet, der har tilladelse til at gennemse og godkende tidsregistreringer og udgifter.</span><span class="sxs-lookup"><span data-stu-id="65078-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="65078-117">Estimatfelter</span><span class="sxs-lookup"><span data-stu-id="65078-117">Estimate fields</span></span>

- <span data-ttu-id="65078-118">**Estimeret startdato**: Den dato, hvor projektet starter.</span><span class="sxs-lookup"><span data-stu-id="65078-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="65078-119">Når dette felt opdateres, flyttes opgaver i projektet forholdsmæssigt sammen med den nye startdato.</span><span class="sxs-lookup"><span data-stu-id="65078-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="65078-120">**Slutdato**: Den dato, hvor projektet er planlagt til at skulle slutte.</span><span class="sxs-lookup"><span data-stu-id="65078-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="65078-121">**Indsats**: Projektets anslåede indsats.</span><span class="sxs-lookup"><span data-stu-id="65078-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="65078-122">Når der tilføjes opgaver til projektet, kan du ikke længere redigere dette felt.</span><span class="sxs-lookup"><span data-stu-id="65078-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="65078-123">**Estimeret arbejdskraftomkostninger**: De anslåede arbejdskraftomkostninger ved projektet.</span><span class="sxs-lookup"><span data-stu-id="65078-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="65078-124">Når der tilføjes arbejdskraftomkostninger til projektet, kan du ikke længere redigere dette felt.</span><span class="sxs-lookup"><span data-stu-id="65078-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="65078-125">**Estimerede udgifter**: De estimerede udgifter til projektet.</span><span class="sxs-lookup"><span data-stu-id="65078-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="65078-126">Når der tilføjes udgifter til projektet, kan du ikke længere redigere dette felt.</span><span class="sxs-lookup"><span data-stu-id="65078-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="65078-127">Felter for faktiske projektoplysninger</span><span class="sxs-lookup"><span data-stu-id="65078-127">Project actual fields</span></span>
- <span data-ttu-id="65078-128">**Faktisk starttidspunkt**: Den dato, hvor projektet blev startet.</span><span class="sxs-lookup"><span data-stu-id="65078-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="65078-129">**Faktisk sluttidspunkt**: Opdateres, når et projekt er fuldført.</span><span class="sxs-lookup"><span data-stu-id="65078-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="65078-130">Felter til projektstatus</span><span class="sxs-lookup"><span data-stu-id="65078-130">Project status fields</span></span>

- <span data-ttu-id="65078-131">**Overordnet projektstatus**: Den overordnede projekttilstand, der er angivet af projektlederen.</span><span class="sxs-lookup"><span data-stu-id="65078-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="65078-132">**Kommentarer**: En kommentar om den aktuelle tilstand for projektet, som angives af projektlederen.</span><span class="sxs-lookup"><span data-stu-id="65078-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]