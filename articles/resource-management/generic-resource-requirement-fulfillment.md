---
title: Opfyldelse af generiske ressourcekrav
description: Dette emne indeholder oplysninger om, hvordan du reserverer navngivne ressourcer til et generisk ressourcekrav.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130300"
---
# <a name="generic-resource-requirement-fulfillment"></a>Opfyldelse af generiske ressourcekrav

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan reservere en navngivet ressource til at erstatte en generisk ressource, der har et ressourcekrav.

1. På siden **Projekter** skal du vælge fanen **Team**.
2. Vælg den generiske ressource, der har et ressourcekrav, på listen, og vælg derefter **Reservér**. Du kan også åbne ressourcekravet og derefter vælge **Reservér**.
3. Vælg en navngivet ressource, der skal reserveres for projektteamet, på siden **Planlægningsassistent**, og vælg derefter **Reservér**.

Når reservationen er fuldført og opfyldt af en navngivet ressource, erstattes den generiske ressource med den navngivne ressource.

Tildelingerne i tidsplanen opdateres også med den navngivne ressource.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Indfri en generisk ressource med flere navngivne ressourcer
Indfrielse af et krav til en generisk ressource med flere navngivne ressourcer svarer til at tildele en enkelt navngivet ressource. Der er f.eks. en opgave med en varighed på fem dage og 120 timer. Denne opgave kan ikke udføres af én ressource, der fungerer som en normal ottetimers dag i en uge på fem dage. 

Kravet er på 120 timers robotteknik over fem dage, hvilket er 24 timer om dagen.

Dette er et eksempel på, hvornår der skal bruges flere navngivne ressourcer til at indfri en generisk ressourceanmodning. Du skal reservere flere ressourcer for at indfri kravet.

Den væsentligste forskel i dette scenarie er, at den generiske ressource forbliver i det team, der er tildelt opgaven, og teammedlemmer af den reserverede navngivne ressource er ikke tildelt som en del af stillingen. Projektlederen kan tildele det arbejde, der er relevant for de navngivne ressourcer. **Afstemning**-visningen kan hjælpe en projektleder med at fordele reservationer på tværs af flere ressourcer til opgavetildelinger. Dette sker ikke automatisk, da det i et hvilket som helst scenarie, der er mere kompliceret end det enkle eksempel overfor, f.eks. hvor du har et bundt opgaver, der udgør kravet eller er projektlederens hensigt med tildelingen, der skal optages i systemet. Da systemet ikke kan forstå hensigten, vil antagelserne sandsynligvis være anderledes end hensigten, og der opstår et forkert eller uforudsigeligt resultat. Det forudsigelige resultat er, at den generiske ressource forbliver tildelt, indtil projektlederen bevidst opretter tildelinger med hjælp fra visningen **Afstemning**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]