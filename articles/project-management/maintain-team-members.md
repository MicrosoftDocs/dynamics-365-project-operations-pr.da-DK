---
title: Bevar projektteamets medlemmer
description: Denne emne indeholder oplysninger om reservation af navngivne ressourcer til projektteam og deres tildeling af opgaver.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961841"
---
# <a name="maintain-team-members"></a>Bevar projektteamets medlemmer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan tilføje en navngivet ressource til projektteamet ved at reservere den direkte til teamet.

1. Gå til **Projekter** i Dynamics 365 Project Operations, og vælg det åbne projekt, du skal reservere for.
2. På siden **Projekt** skal du på fanen **Team** vælge **Nyt**. 
3. Vælg den reserverbare ressource i dialogboksen **Hurtig oprettelse af projektteammedlem**. Feltet **Rolle** udfyldes med ressourcens standardrolle, hvis der er tildelt en sådan. Du kan ændre rollen. 
4. Vælg den fra- og til-dato, som ressourcen skal bruge, og vælg derefter fordelingsmetoden for ressourcens kapacitet. 
5. I feltet **Projektgodkender** skal du vælge **Ja**, hvis teammedlemmet skal være projektgodkender. Teammedlemmet kan godkende indsendte tids- og udgiftsregistreringer for dette projekt. 
6. Vælg **Gem**.

Du kan nu tildele den reserverede ressource opgaver på projektet. På siden **Projekt** skal du på fanen **Planlæg** tildele opgaver til den nye ressource. Den ressourcevælger, der åbnes i feltet **Ressourcer** i opgavegitteret, viser de teammedlemmer, du kan vælge.


I Project Operations er ressourcereservationer og opgavetildelinger ikke tæt sammenkoblet. Når du bruger ressourcevælgeren i tidsplanen, kan du tildele teammedlemmer opgaver for flere timer, end deres reservationer dækker på projektet.

Forskellene mellem teammedlemmers reservationer og tildelinger vises under fanerne **Team** og **Ressourceafstemning**. Du kan også afstemme forskellene mellem reservationer og tildelinger for ressourcer på et mere detaljeret niveau.

Anvend ressourcevælgeren under fanen **Planlæg** til at søge efter og vælge de reserverbare ressourcer, der ikke allerede er en del af projektteamet. Disse ressourcer vises i ressourcevælgeren som **Andre ressourcer**.

Når du foretager et valg, tilføjes ressourcen til projektteamet og tildeles opgaven, men der oprettes ikke nogen reservationer.

Du kan bruge fanen **Afstemning** til at udvide reservationsfunktionen eller **Planlægningsområde** til at reservere ressourcens kapacitet til projektet.

Når et teammedlem er reserveret på projektet, kan du bruge **Bevar reservationer** eller **Planlægningsområdet** til direkte at administrere deres reservationer.
