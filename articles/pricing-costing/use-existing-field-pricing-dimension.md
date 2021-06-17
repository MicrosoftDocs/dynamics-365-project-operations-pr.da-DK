---
title: Anvendelse af felter i Project Operations som prisfastsættelsesdimensioner
description: Dette emne indeholder oplysninger om at bruge felterne som prisfastsættelsesdimensioner i Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004479"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="d43ad-103">Felter i Project Operations som prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="d43ad-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="d43ad-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="d43ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d43ad-105">Objektet **Faktiske** har mange felter, der kan bruges som prisfastsættelsesdimensioner for ressourcebaseret prisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="d43ad-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="d43ad-106">Et almindeligt felt er f.eks. **Reserverbar ressource**.</span><span class="sxs-lookup"><span data-stu-id="d43ad-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="d43ad-107">Mindre virksomheder, der har færre end 20-30 fakturerbare ressourcer, kan mene, at det er enklere at have faktura- og omkostningssatser, der er specifikke for hver enkelt ressource.</span><span class="sxs-lookup"><span data-stu-id="d43ad-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="d43ad-108">Men da den fakturerbare arbejdsstyrke vokser, kan ressourcespecifikke satser blive urealistiske at opretholde.</span><span class="sxs-lookup"><span data-stu-id="d43ad-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="d43ad-109">Ressourceomkostninger og faktureringssatser begynder at variere, efterhånden som ressourcer bliver forfremmet, får flere oplevelser, eller kræver et andet sæt færdigheder.</span><span class="sxs-lookup"><span data-stu-id="d43ad-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="d43ad-110">Et andet eksempel er transaktionskategorien.</span><span class="sxs-lookup"><span data-stu-id="d43ad-110">Another example is that of transaction category.</span></span> <span data-ttu-id="d43ad-111">Kunder og installatører har brugt transaktionskategorien til at klassificere arbejde og bruge feltet til at angive priser og omkostninger baseret på arbejdskategorien.</span><span class="sxs-lookup"><span data-stu-id="d43ad-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]