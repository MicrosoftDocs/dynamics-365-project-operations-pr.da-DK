---
title: Færdigheds- og kompetencemodeller
description: Denne artikel indeholder oplysninger om, hvordan du bruger færdigheds- og kompetencemodeller.
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
ms.openlocfilehash: 27a9668c3a0d6a2323fb4797a29f6c7d3d146c57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925297"
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
