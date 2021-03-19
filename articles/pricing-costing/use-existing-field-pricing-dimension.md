---
title: Anvendelse af felter i Project Operations som prisfastsættelsesdimensioner
description: Dette emne indeholder oplysninger om at bruge felterne som prisfastsættelsesdimensioner i Dynamics 365 Project Operations.
author: rumant
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274631"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="25f67-103">Felter i Project Operations som prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="25f67-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="25f67-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="25f67-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25f67-105">Objektet **Faktiske** har mange felter, der kan bruges som prisfastsættelsesdimensioner for ressourcebaseret prisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="25f67-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="25f67-106">Et almindeligt felt er f.eks. **Reserverbar ressource**.</span><span class="sxs-lookup"><span data-stu-id="25f67-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="25f67-107">Mindre virksomheder, der har færre end 20-30 fakturerbare ressourcer, kan mene, at det er enklere at have faktura- og omkostningssatser, der er specifikke for hver enkelt ressource.</span><span class="sxs-lookup"><span data-stu-id="25f67-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="25f67-108">Men da den fakturerbare arbejdsstyrke vokser, kan ressourcespecifikke satser blive urealistiske at opretholde.</span><span class="sxs-lookup"><span data-stu-id="25f67-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="25f67-109">Ressourceomkostninger og faktureringssatser begynder at variere, efterhånden som ressourcer bliver forfremmet, får flere oplevelser, eller kræver et andet sæt færdigheder.</span><span class="sxs-lookup"><span data-stu-id="25f67-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="25f67-110">Et andet eksempel er transaktionskategorien.</span><span class="sxs-lookup"><span data-stu-id="25f67-110">Another example is that of transaction category.</span></span> <span data-ttu-id="25f67-111">Kunder og installatører har brugt transaktionskategorien til at klassificere arbejde og bruge feltet til at angive priser og omkostninger baseret på arbejdskategorien.</span><span class="sxs-lookup"><span data-stu-id="25f67-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]