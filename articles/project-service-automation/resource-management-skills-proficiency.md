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
# <a name="skills-and-proficiency-models"></a>Færdigheds- og kompetencemodeller

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Færdigheder er ressourceegenskaber, der deles mellem Dynamics 365 Project Service Automation og Dynamics 365 Field Service hvis programmet er installeret. 

Hvis du vil bevare lageret af færdigheder i Project Service Automation, skal du gå til **Ressourcer** \> **Resourcefærdigheder**. 

> ![Ressourcefærdigheder](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Brug af kompetencemodeller til klassificering af ressourcer

Færdigheder til ressourcer klassificeres af kompetencemodeller. De enkelte klassifikationer findes i en kompetencemodel. 

1. Hvis du vil oprette en kompetencemodel, skal du gå til **Ressourcer** \> **Kompetencemodeller** og derefter vælge **Ny**.
2. I den nye klassificeringsmodel skal du angive den mindste klassificeringsværdi, den højeste klassificeringsværdi og det objekt, der klassificeres.
3. I undergitteret **Klassificeringsværdier** kan du definere de forskellige klassificeringsværdier fra minimum til maksimum.

> ![Minimum- og maksimumklassificeringer defineret](media/Resource-Management-image85.png)

Disse klassificeringsværdier vises i filtrene **Resourcekrav**, **Planlægningsområde** og **Planlægningsassistent**.
