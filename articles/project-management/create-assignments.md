---
title: Opret ressourcetildelinger
description: Denne artikel indeholder oplysninger om oprettelse af generiske og navngivne ressourcetildelinger.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811986"
---
# <a name="create-resource-assignments"></a>Opret ressourcetildelinger

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


En ressourcetildeling er den direkte tilknytning af et medlem af et projektteam til en bladnodeopgave. Denne artikel indeholder oplysninger om, hvordan du kan tildele ressourcer på forskellige måder.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Oprette et generisk teammedlem via opgavetildeling


Når du opretter et generisk teammedlem via opgavetildeling, kan du oprette en pladsholder eller en generisk ressource. Denne generiske ressource beskriver egenskaberne for den navngivne ressource, som du i sidste ende vil have til at arbejde med opgaverne. Du kan derefter oprette et krav, eller du kan indsende en anmodning ved hjælp af kravet, der bruges til at søge efter, og reservere den navngivne ressource.

1. Vælg ressource-ikonet i cellen **Ressource** i planlægningsgitteret for en opgave.
2. Skriv et navn, der skal fungere som pladsholderressourcens navn. F.eks. programadministrator.
3. Vælg **Opret**, og angiv rollen for den generiske ressource i feltet **Hurtig oprettelse af projektteammedlem**.
4. Tildel opgaver efter behov til denne pladsholderressource ved at vælge ressourcen i **Resourcevælgeren** for opgaven. De angivne ressourcer under **Teammedlemmer**.
5. Når du er færdig med at tildele den generiske ressource, skal du under fanen **Team** vælge den generiske ressource og derefter vælge **Generér krav** for at oprette et ressourcekrav for den generiske ressource.
6. Vælg **Reservér** for den generiske ressource, og brug derefter planlægningsområdet til at finde og reservere en faktisk ressource. Du kan også sende kravet til en ressourceansvarlig til indfrielse.
7. Når den generiske ressource er helt udfyldt med en navngivet ressource, fjernes den generiske ressource fra teamet. (En delvis opfyldelse af et ressourcekrav resulterer ikke i en ressourcetildeling). Opgavetildelingerne for den generiske ressource tildeles den navngivne ressource, som opfyldt ressourcekravet for den generiske ressource.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tildele en navngivet ressource fra listen over alle reserverbare ressourcer

Du kan bruge søgefeltet i **Ressourcevælger** til at søge i alle de aktive reserverbare ressourcer og tildele dem til en hvilken som helst bladnodeopgave. Ressourcer, der er tildelt på denne måde, føjes til teamet uden reservationer. Dette svarer til at tilføje et teammedlem og vælge **Ingen** som fordelingsmetode. Ressourcen vises på fanerne **Team**, **Ressourcetildeling** og **Afstemning** som ressourcer, der kun har tildelinger og et reservationsunderskud. Reservér dem, hvis du vil bruge deres tilgængelighed.

1. Fra opgavegitteret, området eller tidslinjen skal du navigere til cellen **Tildelt til**.
2. Begynd at skrive et navn i søgefeltet. Søgeresultaterne for navnet vises i **Resourcevælgeren** under **Andre ressourcer**.
3. Vælg den ressource, som du vil tildele til opgaven, eller vælg navnet på ressourcen under **Andre teamressourcer**.

## <a name="editing-resource-assignment-contours"></a>Redigering af ressourcetildelingsprofiler

Når ressourcer tildeles til en opgave i tidsplanen, fordeles deres indsats som standard lineært til de enkelte ressourcer baseret på ressourcens arbejdstimer og tilstanden for projektets tidsplan. En projektleder kan bruge ressourcetildelingsgitteret til at finjustere indsatsestimaterne for de enkelte ressourcer, der er tildelt til en eller flere opgaver på tværs af de forskellige tidsskalaer. Denne funktion hjælper projektledere med at udarbejde mere nøjagtige omkostnings- og salgsestimater, som er baseret på ressourcetildelingsprofiler, som genereres, når en ressource tildeles til en opgave. Derudover kan projektledere nemmere afspejle det ressourcebehov, der kræves for at opbygge behovet i et ressourcekrav.

### <a name="navigation"></a>Navigation

For at få adgang til gitteret til redigering af profiler vælger projektlederen først fanen **Opgaver** på projektets hovedside og vælger derefter fanen **Tildelinger**.

![Fanen Tildelinger under fanen Opgaver på projektets hovedside.](media/AssignmentGrid.png)

Gitteret understøtter to metoder til gruppering: **gruppér efter ressource** og **gruppér efter opgave**. I modsætning til i gittervisningen kan kolonner ikke konfigureres. De eneste synlige kolonner er **Tildelt til**, **Opgavenavn**, **Tildelingsstart**, **Tildelingsslut** og **Tildelingsindsats**.

Når gitteret gengives første gang, starter det med den tidligste tildelingsprofil. Hvis tidsplanen ikke indeholder tildelinger med indsatser, er gitteret tomt og gengiver ikke noget.

![Tomt tildelingsgitter.](media/emptyassignmentgrid.png)

Hvis du vil have vist dine profiler og forskellige tidsskalaer, er det skrivebeskyttede ressourcetildelingsgitter og ressourceafstemningsgitteret også tilgængelige.

### <a name="resource-calendars"></a>Ressourcekalendere

Muligheden for at redigere en profil for en bestemt dag bestemmes af ressourcens arbejdsdage, som det afspejles i kalenderen. Hvis en celle er deaktiveret for en bestemt ressource, har den pågældende ressource ikke arbejdsdage i den pågældende periode.

En ressources profiler kan strække sig ud over den tildelte opgaves aktuelle start- og slutdatoer. Hvis en profil opdateres, så den ligger efter den seneste slutdato for en opgave eller den tidligste startdato for en opgave, ændres opgavens slutdato eller startdato efter behov. Men hvis en profil opdateres, så den ligger før startdatoen for en opgave, der er knyttet til en tidligere opgave, mislykkes opdateringen, fordi tildelingen udløser opgaven til at starte, før den tidligere opgave afsluttes, og denne funktionsmåde understøttes ikke i øjeblikket.

### <a name="co-authoring"></a>Samtidig redigering

Ændringer af ressourcetildelingsgitteret afspejles automatisk i tilknyttede visninger, herunder diagrammet, tidslinjen, området og gittervisningerne. Hvis flere brugere gennemgår projektet samtidig, afspejles eventuelle ændringer, som én bruger foretager, i gitteret. Derimod vises eventuelle ændringer, der foretages i ressourcetildelingsgitteret, for alle andre brugere, der ser projektet i samme session.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
