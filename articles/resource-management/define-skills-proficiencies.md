---
title: Definer færdigheder og kvalifikationer
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer kompetencemodeller til vurdering af ressourcer.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e825d80bb8ac342b269783747a9a0c0f540d349f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585969"
---
# <a name="define-skills-and-proficiencies"></a>Definer færdigheder og kvalifikationer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Færdigheder er ressourceegenskaber, der deles mellem Dynamics 365 Project Operations og Dynamics 365 Field Service hvis programmet er installeret. 

- Hvis du vil bevare lageret af færdigheder i Project Operations, skal du gå til **Ressourcer** \> **Ressourcefærdigheder**. 

## <a name="use-proficiency-models-to-rate-resources"></a>Brug af kompetencemodeller til klassificering af ressourcer

Færdigheder til ressourcer klassificeres af kompetencemodeller. De enkelte klassifikationer findes i en kompetencemodel. 

1. Hvis du vil oprette en kompetencemodel, skal du gå til **Ressourcer** \> **Kompetencemodeller** og derefter vælge **Ny**.
2. I den nye klassificeringsmodel skal du angive den mindste klassificeringsværdi, den højeste klassificeringsværdi og det objekt, der klassificeres.
3. I undergitteret **Klassificeringsværdier** kan du definere de forskellige klassificeringsværdier fra minimum til maksimum.


Disse klassificeringsværdier vises i filtrene **Resourcekrav**, **Planlægningsområde** og **Planlægningsassistent**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]