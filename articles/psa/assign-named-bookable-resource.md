---
title: Reservere navngivne reserverbare ressourcer til et projektteam og tildele opgaver
description: Dette emne indeholder oplysninger om, hvordan du reserverer navngivne ressourcer til projektteams og tildeler dem til opgaver.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: cdbcd84d2277ba1c8e68270d5b1f8ca45c17f05e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575343"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Reservere navngivne reserverbare ressourcer til et projektteam og tildele opgaver 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan føje en navngivet ressource til projektteamet ved at reservere den direkte for teamet. Det kan du gøre ved at benytte følgende fremgangsmåde.

1. Gå til **Projekter** i Project Service Automation, og vælg det åbne projekt, du skal reservere for.
2. Klik på **Ny** under fanen **Team** på siden **Projekt**. 

![Tilføjelse af et teammedlem fra fanen Team.](media/RM-how-to-1.png)

3. Vælg den reserverbare ressource i dialogboksen **Hurtig oprettelse af projektteammedlem**. Feltet **Rolle** udfyldes med ressourcens standardrolle, hvis der er tildelt en sådan. Du kan ændre rollen, hvis det er nødvendigt. 
4. Vælg den fra- og til-dato, som ressourcen skal bruge, og vælg derefter fordelingsmetoden for ressourcens kapacitet. 
5. Hvis teammedlemmet skal være projektgodkender, skal du vælge **Ja** i feltet **Projektgodkender**. Det betyder, at teammedlemmet kan godkende indsendte tids- og udgiftsposter for dette projekt. 
6. Klik på **Gem**.

![Tilføjelse af et teammedlem i formularen Hurtig oprettelse.](media/RM-how-to-2.png)


Du kan nu tildele den reserverede ressource opgaver på projektet. Klik på fanen **Planlæg** på siden **Projekt** for at tildele den nye ressource opgaver. Den ressourcevælger, der åbnes i feltet **Ressourcer** i opgavegitteret, viser de teammedlemmer, du kan vælge.

![Tildeling af et teammedlem til en opgave på fanen Planlæg.](media/RM-how-to-3.png)

I version 3 til Project Service Automation (PSA) er ressourcereservationer og opgavetildelinger ikke tæt sammenkoblet. Det betyder, at når du bruger ressourcevælgeren i tidsplanen, kan du tildele teammedlemmer opgaver for flere timer, end deres reservationer dækker på projektet.
Du kan se forskellene mellem teammedlemmernes reservationer og tildelinger under fanen **Team** eller under fanen **Ressourceafstemning**. Du kan også afstemme forskellene mellem reservationer og tildelinger for ressourcer på et mere detaljeret niveau.

![Fanen Ressourceafstemning.](media/RM-how-to-4.png)

Du kan også bruge ressource vælgeren under fanen **Planlæg** til at søge efter og vælge de reserverbare ressourcer, der ikke allerede er en del af projektteamet. Disse vises i ressourcevælgeren som **Andre ressourcer**.

![Tildeling af en arbejder, der ikke er medlem af et team, til en opgave.](media/RM-how-to-5.png)

Når du gør dette, føjes ressourcen til projektteamet og tildeles opgaven, men der oprettes ikke nogen reservationer.

![Teammedlemmer med tildelinger uden reservationer.](media/RM-how-to-6.png)

Du kan bruge fanen **Afstemning** til at udvide reservationsfunktionen eller **Planlægningsområde** til at reservere ressourcens kapacitet til projektet.

![Udvidelse af reservationer for et teammedlem på fanen Ressourceafstemning.](media/RM-how-to-7.png)

Når et teammedlem er reserveret på projektet, kan du bruge vedligeholdelse af reservationer eller planlægningsområdet til direkte at administrere deres reservationer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
