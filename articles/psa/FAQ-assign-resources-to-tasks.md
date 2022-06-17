---
title: Tildel en ressource til en opgave
description: Denne artikel indeholder oplysninger om, hvordan du tildeler ressourcer til opgaver.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: dae5a81c51f34b9115ac8c267452b167a6d7bef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913475"
---
# <a name="assign-a-resource-to-a-task"></a>Tildel en ressource til en opgave

[!include [banner](../includes/psa-now-project-operations.md)]

Der findes tre metoder at tildele en ressource til en opgave på i Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservere en ressource som et teammedlem og derefter tildele ressourcen til en opgave

Du kan føje en ressource til projektteamet og derefter tildele ressourcen til opgaver i projektplanen.

1. I fanen **Teammedlem** kan du tilføje et nyt teammedlem ved at vælge **Ny**. 

2. Panelet **Hurtig oprettelse af teammedlem** åbnes, hvor du kan vælge det reserverbare ressourcenavn og angive en rolle. 

    Vælg en af følgende allokeringsmetoder til reservation af ressourcen:

    - **Fuld kapacitet** reserverer ressourcens fulde kapacitet for de angivne fra- og til-datoer.
    - **Kapacitet som procentdel** reserverer ressourcen med en procentdel af ressourcens kapacitet på de angivne fra- og til-datoer.
    - **Efter timer - jævn fordeling** reserverer ressourcen i et angivet antal timer og distribuerer dem jævnt pr. dag over de angivne fra- og til-datoer.
    - **Efter timer - flest timer først i perioden** reserverer ressourcen i et angivet antal timer og distribuerer timerne pr. dag med de største udgifter først i perioden hen over de angivne fra- og til-datoer.
    - **Ingen** tilføjer ressourcen til teamet, men opretter ikke eventuelle reservationer, der kan absorbere deres kapacitet.

3. I gitteret **Tidsplan** for en opgave skal du vælge ikonet **Resource** i ressourcecellen og derefter vælge det teammedlem, du lige har tilføjet, under **Teammedlemmer** . 

> [!NOTE]
> I fanerne **Teammedlem** og **Afstemning** viser ressourcen reserverede timer og tildelte timer. Timerne bør være ens, men det er ikke noget krav, fordi reservationer og tildelinger ikke er tæt sammenknyttede. Fanen **Afstemning** giver dig oplysninger om, hvornår de er forskellige, f.eks. når du tildeler en ressource flere timer, end du har reserveret. Hvis du har brug for det, kan du korrigere oplysningerne ved at udvide ressourcens reservationer eller ændre tildelingen.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Oprette et generisk teammedlem via opgavetildeling

Når du opretter et generisk teammedlem via opgavetildeling, opretter du en pladsholder eller en generisk ressource, der beskriver egenskaberne for den navngivne ressource, som du i sidste ende vil have til at arbejde med opgaverne. Du kan derefter oprette et krav (eller sende en anmodning ved hjælp af kravet), der bruges til at søge efter, og reservere den navngivne ressource.

1. Vælg **Resource**-ikonet i ressourcecellen i gitteret **Planlægning** for en opgave.

2. Skriv et navn, der skal fungere som pladsholderressourcens navn. F.eks. programadministrator.

3. Vælg **Opret**, og angiv rollen for den generiske ressource i feltet **Hurtig oprettelse af projektteammedlem**.

4. Du kan fortsætte med at tildele opgaver til denne pladsholderressource ved at vælge ressourcen i **Resourcevælgeren** for opgaven. De er angivet under **Teammedlemmer**.

5. Når du har tildelt den generiske ressource, skal du vælge den generiske ressource under fanen **Team** og derefter vælge **Generer krav** for at oprette et ressourcekrav for den generiske ressource.

6. Vælg **Reservér** for den generiske ressource. Du kan derefter bruge planlægningsområdet til at finde og reservere en faktisk ressource. Du kan også sende kravet til en ressourceansvarlig til indfrielse.

7. Når den generiske ressource er indfriet med en navngivet ressource, fjernes den generiske ressource fra teamet, og opgavetildelingerne for den generiske ressource tildeles til den navngivne ressource, der opfyldte ressourcekravet til den generiske ressource.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tildele en navngivet ressource fra listen over alle reserverbare ressourcer

Du kan bruge søgefeltet i **Resourcevælgeren** til at søge i alle de reserverbare ressourcer i Project Service og tildele dem til en opgave.

Ressourcer, der er tildelt på denne måde, føjes til teamet uden reservationer. Dette svarer til at tilføje et gruppemedlem og vælge Ingen som fordelingsmetode. Ressourcen vises under fanen **Team** og fanen **Afstemning** som ressourcer med tildelinger og et reservationsunderskud. Reservér dem, hvis du vil bruge deres tilgængelighed.

1. Vælg **Resource**-ikonet i ressourcecellen i gitteret **Planlægning** for en opgave.

2. Begynd at skrive et navn. Søgeresultaterne for navnet vises i **Resourcevælgeren** under **Andre ressourcer**.

3. Vælg den ressource, som du vil tildele til opgaven.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
