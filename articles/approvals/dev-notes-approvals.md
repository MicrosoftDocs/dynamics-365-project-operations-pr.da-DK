---
title: Udviklers bemærkninger til godkendelser
description: Dette emne indeholder yderligere oplysninger til udviklere om, hvordan man arbejder med godkendelser.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996784"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="0bb67-103">Udviklers bemærkninger til godkendelser</span><span class="sxs-lookup"><span data-stu-id="0bb67-103">Developer notes for Approvals</span></span>

<span data-ttu-id="0bb67-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0bb67-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0bb67-105">Dynamics 365 Project Operations omfatter valideringslogik, som sikrer korrekt postomstilling via godkendelsesfaserne.</span><span class="sxs-lookup"><span data-stu-id="0bb67-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="0bb67-106">Korrekte postoverførsler sikrer:</span><span class="sxs-lookup"><span data-stu-id="0bb67-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="0bb67-107">At alle understøttende rækker oprettes i relaterede tabeller, som f.eks. kladder og faktiske værdier.</span><span class="sxs-lookup"><span data-stu-id="0bb67-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="0bb67-108">Godkenderen er markeret som en **Projektgodkender** i projektet, før der fortsættes.</span><span class="sxs-lookup"><span data-stu-id="0bb67-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]