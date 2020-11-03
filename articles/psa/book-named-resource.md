---
title: Reservere navngivne ressourcer fra ressourcekrav
description: Denne emne indeholder oplysninger om at reservere navngivne ressourcer til et generisk ressourcekrav.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074377"
---
# <a name="book-named-resources-from-resource-requirements"></a>Reservere navngivne ressourcer fra ressourcekrav

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan reservere en navngivet ressource til at erstatte en generisk ressource, der har et ressourcekrav.

1. I Project Service Automation (PSA) skal du klikke på fanen **Team** på siden **Projekter**.
2. Vælg den generiske ressource, der har et ressourcekrav, på listen, og klik derefter på **Reservér**. Du kan også åbne ressourcekravet og derefter klikke på **Reservér**.


![Reservation af et generisk teammedlem](media/RM-how-to-14.png)


3. Vælg en navngivet ressource, der skal reserveres for projektteamet, på siden **Planlægningsassistent** , og klik derefter på **Reservér**.

![Reservation af et generisk teammedlem ved hjælp af planlægningsassistent](media/RM-how-to-15.png)

Når reservationen er fuldført og opfyldt af en navngivet ressource, erstattes den generiske ressource med den navngivne ressource.

![Navngivet teammedlem, der erstatter et generisk teammedlem](media/RM-how-to-16.png)

Tildelingerne i tidsplanen opdateres også med den navngivne ressource.

![Navngivet teammedlem, der er tildelt projektopgaver](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Indfri en generisk ressource med flere navngivne ressourcer
Indfrielse af et krav til en generisk ressource med flere navngivne ressourcer svarer til at tildele en enkelt navngivet ressource. Der er f.eks. en opgave med en varighed på fem dage og 120 timer. Denne opgave kan ikke udføres af én ressource, der fungerer som en normal ottetimers dag i en uge på fem dage. 

![En opgave, der skal bruge 120 timers arbejde over fem dage](media/RM-how-to-21.png)

Kravet er på 120 timers robotteknik over fem dage, hvilket er 24 timer om dagen.

![Krav pr. dag](media/RM-how-to-22.png)

Dette er et eksempel på, hvornår der skal bruges flere navngivne ressourcer til at indfri en generisk ressourceanmodning. Du skal reservere flere ressourcer for at indfri kravet.

![Reservation af flere ressourcer for at indfri kravet](media/RM-how-to-23.png)

Den væsentligste forskel i dette scenarie er, at den generiske ressource forbliver i det team, der er tildelt opgaven, og teammedlemmer af den reserverede navngivne ressource er ikke tildelt som en del af stillingen. Projektlederen kan tildele det arbejde, der er relevant for de navngivne ressourcer. **Afstemning** -visningen kan hjælpe en projektleder med at fordele reservationer på tværs af flere ressourcer til opgavetildelinger. Dette sker ikke automatisk, da det i et hvilket som helst scenarie, der er mere kompliceret end det enkle eksempel overfor, f.eks. hvor du har et bundt opgaver, der udgør kravet, er projektlederens hensigt med tildelingen, der skal optages i systemet. Da systemet ikke kan forstå hensigten, er det sandsynligt, at antagelserne vil være anderledes end forventet, og der opstår et forkert eller uforudsigeligt resultat. Det forudsigelige resultat er, at den generiske ressource forbliver tildelt, indtil projektlederen bevidst opretter tildelinger med hjælp fra visningen **Afstemning**.


