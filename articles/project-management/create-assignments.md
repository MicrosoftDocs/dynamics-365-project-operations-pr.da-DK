---
title: Opret ressourcetildelinger
description: Dette emne indeholder oplysninger om oprettelse af generiske og navngivne ressourcetildelinger.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906117"
---
# <a name="create-resource-assignments"></a>Opret ressourcetildelinger

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


En ressourcetildeling er den direkte tilknytning af et medlem af et projektteam til en bladnodeopgave. Dette emne indeholder oplysninger om de forskellige måder, hvorpå du tildeler ressourcer.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Oprette et generisk teammedlem via opgavetildeling


Når du opretter et generisk teammedlem via opgavetildeling, kan du oprette en pladsholder eller en generisk ressource. Denne generiske ressource beskriver egenskaberne for den navngivne ressource, som du i sidste ende vil have til at arbejde med opgaverne. Du kan derefter oprette et krav, eller indsende en anmodning ved hjælp af kravet, der bruges til at søge efter, og reservere den navngivne ressource.

1. Vælg ressource-ikonet i cellen **Ressource** i planlægningsgitteret for en opgave.
2. Skriv et navn, der skal fungere som pladsholderressourcens navn. F.eks. programadministrator.
3. Vælg **Opret**, og angiv rollen for den generiske ressource i feltet **Hurtig oprettelse af projektteammedlem**.
4. Tildel opgaver efter behov til denne pladsholderressource ved at vælge ressourcen i **Resourcevælgeren** for opgaven. De angivne ressourcer under **Teammedlemmer**.
5. Når du er færdig med at tildele den generiske ressource, skal du under fanen **Team** vælge den generiske ressource og derefter vælge **Generer krav** for at oprette et ressourcekrav for den generiske ressource.
6. Vælg **Reservér** for den generiske ressource, og brug derefter planlægningsområdet til at finde og reservere en faktisk ressource. Du kan også sende kravet til en ressourceansvarlig til indfrielse.
7. Når den generiske ressource er fuldstændig opfyldt (en delvis opfyldelse af et ressourcekrav resulterer ikke i en ressourcetildeling) med en navngivet ressource, fjernes den generiske ressource fra teamet. Opgavetildelingerne for den generiske ressource tildeles den navngivne ressource, som opfyldt ressourcekravet for den generiske ressource.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tildele en navngivet ressource fra listen over alle reserverbare ressourcer

Du kan bruge søgefeltet i **Ressourcevælger** til at søge i alle de aktive reserverbare ressourcer og tildele dem til en hvilken som helst bladnodeopgave. Ressourcer, der er tildelt på denne måde, føjes til teamet uden reservationer. Dette svarer til at tilføje et teammedlem og vælge **Ingen** som fordelingsmetode. Ressourcen vises på fanerne **Team**, **Ressourcetildeling** og **Afstemning** som ressourcer, der kun har tildelinger og et reservationsunderskud. Reservér dem, hvis du vil bruge deres tilgængelighed.

1. Fra opgavegitteret, området eller tidslinjen skal du navigere til cellen **Tildelt til**.
2. Begynd at skrive et navn i søgefeltet. Søgeresultaterne for navnet vises i **Resourcevælgeren** under **Andre ressourcer**.
3. Vælg den ressource, som du vil tildele til opgaven, eller vælg navnet på ressourcen under **Andre teamressourcer**.
