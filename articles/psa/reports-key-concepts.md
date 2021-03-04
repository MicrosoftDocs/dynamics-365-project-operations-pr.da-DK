---
title: Nøglekoncepter
description: Dette emne indeholder oplysninger om nøglebegreberne for ressourcestyring i Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 75b2d2c520cc48eb59c266289ca2bdc1288f2920
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147736"
---
# <a name="key-concepts"></a>Nøglekoncepter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I den følgende tabel defineres nøglebegreber, der bruges i Dynamics 365 Project Service Automation-appen.

| Begreb                    | Definition |
|----------------------------|------------|
| Projektteammedlem        | Som en del af projektteamet kan et projektteammedlem være en navngivet ressource, der har reservationer, en navngivet ressource, der ikke har reservationer, eller en generisk ressource. Generiske ressourcer har ikke reservationer, er lokale for projektet, og har ikke kapacitetsbegrænsninger på tværs af projekter. |
| Projektgenerisk ressource   | En ressourcepladsholder, der giver dig mulighed for at oprette et team og besætte en projektplan med medarbejdere, uden at det er nødvendigt at kende den navngivne ressource. Projektkalenderen bruges som den generiske ressources kalender. Standardressourcer kan føjes til et projektteam og tildeles opgaver. |
| Reserverede timer               | Ressourcetidsforbrug er definitivt reserveret til et projekt for at sikre, at projektarbejdet fuldføres. Reserverede timer forbruges fra ressourcens overordnede kapacitet. Reservationer sker kun i forhold til navngivne ressourcer, ikke i forhold til generiske ressourcer. |
| Tildelte timer             | Ressourcetimer tildeles til opgaver i projektplanen. Tildelinger kan ske enten i forhold til navngivne ressourcer eller generiske ressourcer. Tildelinger kan være uafhængige af reservationer. |
| Krævede timer             | Den kapacitet, der kræves, men som endnu ikke er opfyldt af en navngivet ressource. Påkrævede timer er kun relevante for generiske teammedlemmer, der har genereret ressourcekrav. |
| Behov                     | Den aktuelle, indgående arbejdsbyrde. I Project Service Automation vises behovet som ressourcekrav eller ressourceanmodninger. |
| Ressourcekrav       | Et objekt, der bruges til at registrere påkrævede timer, start- og slutdatoer, færdigheder, geografi og andre prisdimensioner for de krævede ressourcer. Ressourcekrav genereres enten fra projektteammedlemmer eller oprettes individuelt. |
| Ressourceanmodning           | Et objekt, der bruges som en "kuvert", der indeholder det ressourcekrav, som skal opfyldes af en personalechef. |
| Ressourcestandardrolle      | Den rolle, en ressource grupperes under i forbindelse med beregning af forbrug. Ressourcen antages at have de nødvendige færdigheder til rollen og til at overholde mål-tidsforbruget for den pågældende rolle. |
| Ressourceafdeling | Den afdeling, som en ressource er tildelt til. |
| Omrids                    | Opgave, krav eller tildelingstimer, efterhånden som de opdeles i en daglig fordeling. En opgave på fem dage, 40 timer, kan f.eks. oprettes som otte timer om dagen i løbet af fem dage. |
| Visningen Afstemning        | En visning, der viser reservationer og tildelinger for hvert enkelt projektteammedlem. Denne visning giver projektlederne mulighed for at se, om der er uoverensstemmelse mellem reservationer og tildelinger, så de kan foretage korrigerende handlinger, hvis der forekommer uoverensstemmelser. |
| Arbejdstimer                 | Et objekt, der bruges til at identificere ressourcekapacitet, arbejdstimer og fritid. Dette objekt kaldes også ressourcekalenderen. |
