---
title: Definer færdigheder og kvalifikationer
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer kompetencemodeller til vurdering af ressourcer.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124766"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="26ad0-103">Definer færdigheder og kvalifikationer</span><span class="sxs-lookup"><span data-stu-id="26ad0-103">Define skills and proficiencies</span></span>

<span data-ttu-id="26ad0-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="26ad0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26ad0-105">Færdigheder er ressourceegenskaber, der deles mellem Dynamics 365 Project Operations og Dynamics 365 Field Service, hvis programmet er installeret.</span><span class="sxs-lookup"><span data-stu-id="26ad0-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="26ad0-106">Hvis du vil bevare lageret af færdigheder i Project Operations, skal du gå til **Ressourcer** \> **Ressourcefærdigheder**.</span><span class="sxs-lookup"><span data-stu-id="26ad0-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="26ad0-107">Brug af kompetencemodeller til klassificering af ressourcer</span><span class="sxs-lookup"><span data-stu-id="26ad0-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="26ad0-108">Færdigheder til ressourcer klassificeres af kompetencemodeller.</span><span class="sxs-lookup"><span data-stu-id="26ad0-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="26ad0-109">De enkelte klassifikationer findes i en kompetencemodel.</span><span class="sxs-lookup"><span data-stu-id="26ad0-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="26ad0-110">Hvis du vil oprette en kompetencemodel, skal du gå til **Ressourcer** \> **Kompetencemodeller** og derefter vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="26ad0-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="26ad0-111">I den nye klassificeringsmodel skal du angive den mindste klassificeringsværdi, den højeste klassificeringsværdi og det objekt, der klassificeres.</span><span class="sxs-lookup"><span data-stu-id="26ad0-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="26ad0-112">I undergitteret **Klassificeringsværdier** kan du definere de forskellige klassificeringsværdier fra minimum til maksimum.</span><span class="sxs-lookup"><span data-stu-id="26ad0-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="26ad0-113">Disse klassificeringsværdier vises i filtrene **Resourcekrav**, **Planlægningsområde** og **Planlægningsassistent**.</span><span class="sxs-lookup"><span data-stu-id="26ad0-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
