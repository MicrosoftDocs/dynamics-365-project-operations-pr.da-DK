---
title: Bruge et eksisterende felt i Project Service som en prisdimension
description: Dette emne indeholder oplysninger om brug af eksisterende felter i Project Service som prisdimensioner.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008079"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="f951d-103">Bruge et eksisterende felt i Project Service som en prisdimension</span><span class="sxs-lookup"><span data-stu-id="f951d-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f951d-104">I Project Service Automation (PSA) findes mange felter på objektet **Faktiske**, der kan bruges som prisdimensioner til ressourcebaseret prisfastsættelse i projektorganisationer.</span><span class="sxs-lookup"><span data-stu-id="f951d-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="f951d-105">Et almindeligt felt er f.eks. **Reserverbar ressource**.</span><span class="sxs-lookup"><span data-stu-id="f951d-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="f951d-106">Mindre virksomheder, der har færre end 20-30 fakturerbare ressourcer, kan mene, at det er enklere at have faktura- og omkostningssatser, der er specifikke for hver enkelt ressource.</span><span class="sxs-lookup"><span data-stu-id="f951d-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="f951d-107">Men efterhånden som den fakturerbare arbejdsstyrke vokser, kan det være urealistisk at opretholde specifikke satser, når ressourceomkostnings- og fakturasatser begynder at variere, efterhånden som der kommer flere ressourcer, fås mere erfaring, eller opnås nye færdigheder.</span><span class="sxs-lookup"><span data-stu-id="f951d-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="f951d-108">Da denne fremgangsmåde stadig fungerer for virksomheder af en vis størrelse, henvises til [Brug en reserverbar ressource som en prisfastsættelsesdimension](bookable-resource-pricing-dimension.md) for at forstå, hvordan et eksisterende felt i Project Service kan bruges som en prisfastsættelsesdimension.</span><span class="sxs-lookup"><span data-stu-id="f951d-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="f951d-109">Et andet eksempel er transaktionskategorien.</span><span class="sxs-lookup"><span data-stu-id="f951d-109">Another example is that of transaction category.</span></span> <span data-ttu-id="f951d-110">Kunder og installatører har brugt transaktionskategorien i PSA til at klassificere arbejde og bruge feltet til at angive priser og omkostninger baseret på arbejdskategorien.</span><span class="sxs-lookup"><span data-stu-id="f951d-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="f951d-111">Du kan finde flere oplysninger i [Bruge en transaktionskategori som en prisdimension](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="f951d-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]