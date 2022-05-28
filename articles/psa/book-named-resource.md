---
title: Reservere navngivne ressourcer fra ressourcekrav
description: Denne emne indeholder oplysninger om at reservere navngivne ressourcer til et generisk ressourcekrav.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 92a61012beb9aa200f4ea65b777acb0fae04e7e6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590063"
---
# <a name="book-named-resources-from-resource-requirements"></a>Reservere navngivne ressourcer fra ressourcekrav

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan reservere en navngivet ressource til at erstatte en generisk ressource, der har et ressourcekrav.

1. I Project Service Automation (PSA) skal du klikke på fanen **Team** på siden **Projekter**.
2. Vælg den generiske ressource, der har et ressourcekrav, på listen, og klik derefter på **Reservér**. Du kan også åbne ressourcekravet og derefter klikke på **Reservér**.


![Reservation af et generisk teammedlem.](media/RM-how-to-14.png)


3. Vælg en navngivet ressource, der skal reserveres for projektteamet, på siden **Planlægningsassistent**, og klik derefter på **Reservér**.

![Reservation af et generisk teammedlem ved hjælp af planlægningsassistent.](media/RM-how-to-15.png)

Når reservationen er fuldført og opfyldt af en navngivet ressource, erstattes den generiske ressource med den navngivne ressource.

![Navngivet teammedlem, der erstatter et generisk teammedlem.](media/RM-how-to-16.png)

Tildelingerne i tidsplanen opdateres også med den navngivne ressource.

![Navngivet teammedlem, der er tildelt projektopgaver.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Indfri en generisk ressource med flere navngivne ressourcer
Indfrielse af et krav til en generisk ressource med flere navngivne ressourcer svarer til at tildele en enkelt navngivet ressource. Der er f.eks. en opgave med en varighed på fem dage og 120 timer. Denne opgave kan ikke udføres af én ressource, der fungerer som en normal ottetimers dag i en uge på fem dage. 

![En opgave, der skal bruge 120 timers arbejde over fem dage.](media/RM-how-to-21.png)

Kravet er på 120 timers robotteknik over fem dage, hvilket er 24 timer om dagen.

![Krav pr. dag.](media/RM-how-to-22.png)

Dette er et eksempel på, hvornår der skal bruges flere navngivne ressourcer til at indfri en generisk ressourceanmodning. Du skal reservere flere ressourcer for at indfri kravet.

![Reservation af flere ressourcer for at indfri kravet.](media/RM-how-to-23.png)

Den væsentligste forskel i dette scenarie er, at den generiske ressource forbliver i det team, der er tildelt opgaven, og teammedlemmer af den reserverede navngivne ressource er ikke tildelt som en del af stillingen. Projektlederen kan tildele det arbejde, der er relevant for de navngivne ressourcer. **Afstemning**-visningen kan hjælpe en projektleder med at fordele reservationer på tværs af flere ressourcer til opgavetildelinger. Dette sker ikke automatisk, da det i et hvilket som helst scenarie, der er mere kompliceret end det enkle eksempel overfor, f.eks. hvor du har et bundt opgaver, der udgør kravet, er projektlederens hensigt med tildelingen, der skal optages i systemet. Da systemet ikke kan forstå hensigten, er det sandsynligt, at antagelserne vil være anderledes end forventet, og der opstår et forkert eller uforudsigeligt resultat. Det forudsigelige resultat er, at den generiske ressource forbliver tildelt, indtil projektlederen bevidst opretter tildelinger med hjælp fra visningen **Afstemning**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
