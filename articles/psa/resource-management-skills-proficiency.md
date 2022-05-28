---
title: Færdigheds- og kompetencemodeller
description: Dette emne indeholder oplysninger om, hvordan du bruger færdigheds- og kompetencemodeller.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d46382939e22c1ee1d9f5517798aabb3520ae3bd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599861"
---
# <a name="skills-and-proficiency-models"></a>Færdigheds- og kompetencemodeller

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Færdigheder er ressourceegenskaber, der deles mellem Dynamics 365 Project Service Automation og Dynamics 365 Field Service hvis programmet er installeret. 

Hvis du vil bevare lageret af færdigheder i Project Service Automation, skal du gå til **Ressourcer** \> **Resourcefærdigheder**. 

> ![Ressourcefærdigheder.](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Brug af kompetencemodeller til klassificering af ressourcer

Færdigheder til ressourcer klassificeres af kompetencemodeller. De enkelte klassifikationer findes i en kompetencemodel. 

1. Hvis du vil oprette en kompetencemodel, skal du gå til **Ressourcer** \> **Kompetencemodeller** og derefter vælge **Ny**.
2. I den nye klassificeringsmodel skal du angive den mindste klassificeringsværdi, den højeste klassificeringsværdi og det objekt, der klassificeres.
3. I undergitteret **Klassificeringsværdier** kan du definere de forskellige klassificeringsværdier fra minimum til maksimum.

> ![Definerede minimum- og maksimumklassificeringer.](media/Resource-Management-image85.png)

Disse klassificeringsværdier vises i filtrene **Resourcekrav**, **Planlægningsområde** og **Planlægningsassistent**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
