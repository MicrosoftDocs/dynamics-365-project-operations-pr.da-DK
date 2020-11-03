---
title: Bruge et eksisterende felt i Project Service som en prisdimension
description: Dette emne indeholder oplysninger om brug af eksisterende felter i Project Service som prisdimensioner.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074250"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="d6fc2-103">Bruge et eksisterende felt i Project Service som en prisdimension</span><span class="sxs-lookup"><span data-stu-id="d6fc2-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="d6fc2-104">I Project Service Automation (PSA) findes mange felter på objektet **Faktiske** , der kan bruges som prisdimensioner til ressourcebaseret prisfastsættelse i projektorganisationer.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="d6fc2-105">Et almindeligt felt er f.eks. **Reserverbar ressource**.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="d6fc2-106">Mindre virksomheder, der har færre end 20-30 fakturerbare ressourcer, kan mene, at det er enklere at have faktura- og omkostningssatser, der er specifikke for hver enkelt ressource.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="d6fc2-107">Men efterhånden som den fakturerbare arbejdsstyrke vokser, kan det være urealistisk at opretholde denne opfattelse, når ressourceomkostnings- og fakturasatser begynder at variere, efterhånden som der kommer flere ressourcer, fås mere erfaring, eller færdighederne får en anden karakter.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="d6fc2-108">Da denne fremgangsmåde stadig fungerer for virksomheder af en vis størrelse, henvises til emnet [Bruge reserverbar ressource som en prisdimension](bookable-resource-pricing-dimension.md) for at forstå, hvordan et eksisterende felt i Project Service kan bruges som en prisdimension.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="d6fc2-109">Et andet eksempel er transaktionskategorien.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-109">Another example is that of transaction category.</span></span> <span data-ttu-id="d6fc2-110">Kunder og installatører har brugt transaktionskategorien i PSA til at klassificere arbejde og bruge feltet til at angive priser og omkostninger baseret på arbejdskategorien.</span><span class="sxs-lookup"><span data-stu-id="d6fc2-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="d6fc2-111">Du kan finde flere oplysninger i [Bruge en transaktionskategori som en prisdimension](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="d6fc2-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>