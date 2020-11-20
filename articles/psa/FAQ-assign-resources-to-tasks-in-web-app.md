---
title: Hvordan tildeler jeg en reserverbar ressource til en opgave i webappen?
description: En oversigt over, hvordan du kan tildele reserverbare ressourcer.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cc1859540ede064c4ab3e2ac128573972912a207
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125171"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Hvordan tildeler jeg en reserverbar ressource til en opgave i webappen (Project Service-app v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Der findes to metoder til at tildele en ressource til en opgave i Project Service. Du kan reservere en ressource som et teammedlem og derefter tildele den til en opgave. Eller du kan oprette et generisk teammedlem via rolletildeling på opgaver, oprette et team og derefter indfri kravene til sikkerhedskopiering med en navngivet ressource.

Bemærk, at hvis du vil tildele en reserverbar ressource til en opgave, skal det reserverbare ressourceteammedlem have nok tilgængelige reservationer. Status for reservationen skal være Bekræftelsestype for Reservér definitivt og status Bekræftet. Hvis der ikke er tilstrækkeligt mange reservationer for ressourcen, fjerner Project Service tildelingen og viser følgende fejlmeddelelse:

*Det er ikke muligt at tildele ressourcen til opgaven – Følgende ressource(r) har ikke tilstrækkeligt mange timer reservereret til projekt*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservere en ressource som et teammedlem og derefter tildele ressourcen til en opgave

Med denne metode kan du føje en ressource til projektteamet og derefter tildele opgaver til ressourcen i projektplanen. Her kan du se, hvordan du gør dette:
1.  I teammedlemsgitteret kan du tilføje et nyt teammedlem ved at vælge **Ny**.
2.  På skærmbilledet Hurtig oprettelse for teammedlemmer kan du vælge det reserverbare ressourcenavn og angive en rolle.
3.  Vælg **Fra** og **Til** datoerne.

    > [!div class="mx-imgBorder"] 
    > ![Skærmbillede af tilføjelse af gruppemedlem](media/FAQ-Resources-to-Tasks2-1.png "Skærmbillede af tilføjelse af gruppemedlem")
 
4.  Vælg en af følgende allokeringsmetoder til reservation af ressourcen:
    - **Fuld kapacitet** reserverer ressourcens fulde kapacitet for de angivne fra- og til-datoer.
    - **Kapacitet som procentdel** reserverer ressourcen med en procentdel af ressourcens kapacitet på de angivne fra- og til-datoer.
    - **Efter timer - jævn fordeling** reserverer ressourcen i et angivet antal timer og distribuerer dem jævnt pr. dag over de angivne fra- og til-datoer.
    - **Efter timer - flest timer først i perioden** reserverer ressourcen i et angivet antal timer og distribuerer timerne pr. dag med de største udgifter først i perioden hen over de angivne fra- og til-datoer.

    Du skal ikke vælge **Ingen**, fordi det føjer ressourcen til teamet, men opretter ikke nogen reservationer, der forbruger ressourcens kapacitet.
5.  Vælg **Gem**.

    Bemærk, at reservationstimerne skal kunne dække indsatstimer og datointervaller for de opgaver, som du tildeler denne ressource til. Hvis de ikke er justerede, kan du ikke tildele ressourcen til opgaven.

6.  Klik på ressourcecellens rulleliste i arbejdsopgavehierarkiet (WBS) for opgaven. Derefter: 

    1. Vælg **Tilføj**.
    2. Vælg rullelisten under **Ressourcer**, og vælg det teammedlem, du har tilføjet ovenfor.
    3. Vælg **OK**. Teammedlemmet tildeles nu til opgaven.

    > [!div class="mx-imgBorder"] 
    > ![Skærmbillede af tilføjelse af ressourcer med WBS](media/FAQ-Resources-to-Tasks2-2.png "Skærmbillede af tilføjelse af ressourcer med WBS")
 
Du kan se den samlede mængde af ressourcens tildelte timer under Tildelte timer i teammedlemsgitteret. Den vil være mindre end eller lig med de reserverede timer for ressourcen. 

> [!div class="mx-imgBorder"] 
> ![Skærmbillede af tildelte timer for en ressource](media/FAQ-Resources-to-Tasks2-3.png "Skærmbillede af tildelte timer for en ressource")
 
Hvis den opgave, du forsøger at tildele til ressourcen, starter efter slutdatoen for ressourcereservationer, vises ressourcen ikke på rullelisten.

Bemærk, at du kan tildele en ressource til flere timer end deres reserverede timer, hvis ressourcen har en vis mængde ikke-tildelt kapacitet. I dette tilfælde tildeles ressourcen kun delvist op til deres reservationer. Du kan se disse resterende ikke-tildelte opgavetimer ved at føje kolonnen Ubemandede timer til arbejdsopgavehierarkiet.

Hvis der er tildelt ressourcer til ressourcens reserverede timer (reserverede timer er lig med tildelte timer), vises følgende fejlmeddelelse, når du forsøger at tildele yderligere opgaver til ressourcen:

*Det er ikke muligt at tildele ressourcen til opgaven – Følgende ressource(r) har ikke tilstrækkeligt mange timer reservereret til projekt.*

Derudover tilføjes det teammedlem, der er standardprojektleder, og som føjes til teamet, når du opretter projektet, uden eventuelle reservationer og kan ikke tildeles til en opgave. De vises ikke på rullelisten med ressourcer for opgaver.

Hvis du vil tildele denne ressource, skal du fjerne vedkommende fra teamet og derefter tilføje ham eller hende igen med en anden allokeringsmetode end Ingen. Grunden til, at de føjes til teamet, når projektet oprettes, er, at et projekt har mindst én projektgodkender som standard.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Oprette et generisk teammedlem via rolletildeling på opgaver

Denne metode sikrer, at ressourcer har tilstrækkelige reservationer for opgaver. Først skal du oprette en pladsholder eller en generisk ressource, der beskriver egenskaberne for den navngivne ressource, som du i sidste ende vil have til at arbejde med opgaverne, ved at oprette et team, når du har tildelt roller til opgaverne. Her kan du se, hvordan du gør dette:

1. Vælg en opgave i arbejdsopgavehierarkiet.
2. Vælg ikonet **Tildelt rolle** på rullelisten i ressourcecellen.
3. Vælg rullelisten **Rolle**, og vælg rollen for den generiske ressource.
4. Vælg **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Skærmbillede af anvendelse af WBS til at tilføje ressourcer](media/FAQ-Resources-to-Tasks2-4.png "Skærmbillede af anvendelse af WBS til at tilføje ressourcer")
 
Når du har tildelt roller til opgaver i WBS, kan du vælge **Opret projektteam**. Project Service opretter det mindste antal generiske teammedlemmer baseret på roller, ressourceorganisationsenheder og projektkalender ved at sammenlægge de tildelte opgaver.

> [!div class="mx-imgBorder"] 
> ![Skærmbillede af oprettelse af projektteam](media/FAQ-Resources-to-Tasks2-5.png "Skærmbillede af oprettelse af projektteam")
 
I gitteret Teammedlem kan se du ressourcer af typen Generisk ressource med navnet på rollen og stillingen. Hvis der kræves to ressourcer til en rolle for at fuldføre arbejdet, opretter funktionen Opret team to teammedlemmer og bruger stillingsnavnet til at adskille dem.

> [!div class="mx-imgBorder"] 
> ![Skærmbillede af tilføjelse af to generiske ressourcer](media/FAQ-Resources-to-Tasks2-6.png "Skærmbillede af tilføjelse af to generiske ressourcer")
 
Du kan åbne sikkerhedskopiering af ressourcekrav for det generiske teammedlem ved at vælge linket under Ressourcekrav.

> [!div class="mx-imgBorder"] 
> ![Skærmbillede af åbning af det bagvedliggende ressourcekrav](media/FAQ-Resources-to-Tasks2-7.png "Skærmbillede af åbning af det bagvedliggende ressourcekrav")

Vælg **Reservér** for den generiske ressource, så du kan bruge planlægningsområdet til at finde og reservere en faktisk ressource. Du kan også sende kravet til en ressourceansvarlig til indfrielse ved at vælge **Send anmodning**.

Når den generiske ressource er indfriet med en navngivet ressource, fjernes den generiske ressource fra teamet, og opgavetildelingerne for den generiske ressource tildeles til den navngivne ressource, der opfyldte ressourcekravet til den generiske ressource.
 

