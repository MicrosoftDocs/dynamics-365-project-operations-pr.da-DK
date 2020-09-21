---
title: Færdigheds- og kompetencemodeller
description: Dette emne indeholder oplysninger om, hvordan du bruger færdigheds- og kompetencemodeller.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750621"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="45fdc-103">Færdigheds- og kompetencemodeller</span><span class="sxs-lookup"><span data-stu-id="45fdc-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="45fdc-104">Færdigheder er ressourceegenskaber, der deles mellem Dynamics 365 Project Service Automation og Dynamics 365 Field Service hvis programmet er installeret.</span><span class="sxs-lookup"><span data-stu-id="45fdc-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="45fdc-105">Hvis du vil bevare lageret af færdigheder i Project Service Automation, skal du gå til **Ressourcer** \> **Resourcefærdigheder**.</span><span class="sxs-lookup"><span data-stu-id="45fdc-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Ressourcefærdigheder](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="45fdc-107">Brug af kompetencemodeller til klassificering af ressourcer</span><span class="sxs-lookup"><span data-stu-id="45fdc-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="45fdc-108">Færdigheder til ressourcer klassificeres af kompetencemodeller.</span><span class="sxs-lookup"><span data-stu-id="45fdc-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="45fdc-109">De enkelte klassifikationer findes i en kompetencemodel.</span><span class="sxs-lookup"><span data-stu-id="45fdc-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="45fdc-110">Hvis du vil oprette en kompetencemodel, skal du gå til **Ressourcer** \> **Kompetencemodeller** og derefter vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="45fdc-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="45fdc-111">I den nye klassificeringsmodel skal du angive den mindste klassificeringsværdi, den højeste klassificeringsværdi og det objekt, der klassificeres.</span><span class="sxs-lookup"><span data-stu-id="45fdc-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="45fdc-112">I undergitteret **Klassificeringsværdier** kan du definere de forskellige klassificeringsværdier fra minimum til maksimum.</span><span class="sxs-lookup"><span data-stu-id="45fdc-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Minimum- og maksimumklassificeringer defineret](media/Resource-Management-image85.png)

<span data-ttu-id="45fdc-114">Disse klassificeringsværdier vises i filtrene **Resourcekrav**, **Planlægningsområde** og **Planlægningsassistent**.</span><span class="sxs-lookup"><span data-stu-id="45fdc-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
