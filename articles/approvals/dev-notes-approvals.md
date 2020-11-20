---
title: Udviklers bemærkninger til godkendelser
description: Dette emne indeholder yderligere oplysninger til udviklere om, hvordan man arbejder med godkendelser.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483941"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="cb170-103">Udviklers bemærkninger til godkendelser</span><span class="sxs-lookup"><span data-stu-id="cb170-103">Developer notes for Approvals</span></span>

<span data-ttu-id="cb170-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="cb170-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb170-105">Dynamics 365 Project Operations inkluderer valideringslogik, der sikrer korrekt postoverførsel gennem godkendelsesfaserne.</span><span class="sxs-lookup"><span data-stu-id="cb170-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="cb170-106">Korrekte postoverførsler sikrer:</span><span class="sxs-lookup"><span data-stu-id="cb170-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="cb170-107">At alle understøttende rækker oprettes i relaterede tabeller, som f.eks. kladder og faktiske værdier.</span><span class="sxs-lookup"><span data-stu-id="cb170-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="cb170-108">Godkenderen er markeret som en **Projektgodkender** i projektet, før der fortsættes.</span><span class="sxs-lookup"><span data-stu-id="cb170-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
