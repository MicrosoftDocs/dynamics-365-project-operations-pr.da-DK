---
title: Foreløbig reservation af en ressource
description: Denne artikel indeholder oplysninger om, hvordan du foreløbigt planlægger eller foreløbigt reserverer projektteammedlemmer.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c666e5c0a83a3d1b440144a62cbd58a58c5db81
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929115"
---
# <a name="soft-book-a-resource"></a>Foreløbig reservation af en ressource

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan planlægge midlertidigt eller "foreløbigt reservere" en ressource til et projektteam for at vise, at du har planer om at tildele ressourcen til projektet. Foreløbige reservationer forbruger ikke en ressources ledige kapacitet, og du kan tildele foreløbigt reserverede teammedlemmer til projektopgaver. Men fordi foreløbige reservation ikke forbruger en ressources kapacitet, kan du fortsat foretage en "definitiv reservation" af ressourcen til andre opgaver i samme periode. Generiske ressourcer må ikke være foreløbige, og en foreløbig reservation kan heller ikke efterkomme en anmodning om en generisk ressource.

Foreløbigt reserverede medlemmer af projektteamet vises under fanen **Team** på siden **Projekt** med deres foreløbigt reserverede timer vist i kolonnen **Foreløbigt reserverede timer** i visningen **Navngivne teammedlemmer**. Foreløbigt reserverede teammedlemmer vises også i planlægningsområdet. Da de er reserveret foreløbigt, viser planlægningsområdet ikke noget forbrug af kapacitet for disse ressourcer. Foreløbigt reserveret tid vises ikke under fanen **Afstemning** og heller ikke i feltet **Udvid reservationer** under fanen **Afstemning** i planlægningsområdet. 

Der er to måder til at foretage foreløbig reservation af et teammedlem til et projekt: direkte fra planlægningsområdet eller ved at tilføje teammedlemmet under fanen **Team**. 

## <a name="soft-book-from-the-schedule-board"></a>Reservér foreløbigt fra planlægningsområdet
Benyt følgende fremgangsmåde for midlertidigt at reservere en ressource fra planlægningsområdet. 

1. Åbn planlægningsområdet, og vælg derefter fanen **Projekt** i panelet **Reservationskrav**.
2. Find det projekt, du vil foretage en foreløbig reservation af en ressource til. Hvis der er et stort antal projekter på listen, skal du vælge kolonneoverskriften **Projekt** og derefter bruge filteret til at søge efter et eller flere projekter.
3. Vælg projektet, træk det og slip det derefter på ressourcens tidsgitter.
5. I panelet **Opret ressourcereservation** skal du justere start- og slutdatoen, angive **Reservationsstatus** til **Foreløbig** og derefter angive timerne. 
6. Klik på **Reservér**. Ressourcen vises nu under fanen **Team** som en ressource for projektet. I visningen **Navngivne teammedlemmer** kan du se de foreløbigt reserverede timer i kolonnen **Foreløbigt reserverede timer**.

> [!NOTE]
> Du kan nu tildele den foreløbigt reserverede ressource til opgaver under fanen **Tidplan**. Under fanen **Afstemning** viser ressourcen et reservationsunderskud i forhold til opgavetildelingen, fordi fanen **Afstemning** kun medtager definitive reservationer. Du kan bruge funktionen **Udvid reservationer** til at reservere ressourcen definitivt for at eliminere underskuddet af definitive reservationer i forhold til ressourcetildelingerne. Du skal manuelt annullere den foreløbige reservation for ressourcen ved hjælp af **Vedligehold reservationer**.

## <a name="soft-book-on-the-team-tab"></a>Reservere foreløbigt under fanen Team

Du kan tilføje teammedlemmer direkte under fanen **Team** og derefter redigere deres reservationsstatus fra **definitiv** til **foreløbig** med **Vedligehold reservationer**. Når du tilføjer et teammedlem på denne måde, medfører det altid en definitiv reservation, medmindre du vælger allokeringsmetoden **Ingen**.

Du kan bruge denne metode ved at udføre følgende trin.

1. Klik på **Ny** under fanen **Team** på siden **Projekt**.
2. Vælg den reserverbare ressource, rollen, og fra- og til-datoer.
3. Vælg en anden allokeringsmetode end **Ingen**.
4. Vælg **Gem**. Du kan se ressourcen i gitteret og vedkommendes timer i kolonnen **Definitivt reserverede timer**.
5. Du kan vedligeholde ressourcens reservationer ved at vælge **Vedligehold reservationer**.
6. Når planlægningsområdet åbnes, skal du udvide ressourcen for at få vist hans eller hendes reservationer. Du kan se reservationen vist som **Definitiv**.
7. Højreklik på reservationen, og vælg **Reservér foreløbigt** \> **Foreløbig** under **Skift status**. Status for reservation er nu **Foreløbig**.
8. Når du har lukket planlægningsområdet, kan du se, at timerne for ressourcen er flyttet fra kolonnen **Definitivt reserverede timer** til **Foreløbigt reserverede timer** i gitteret under fanen **Team**, når du ser på visningen **Navngivne teammedlemmer**.

> [!NOTE]
> Hvis du reserverer en ressource definitivt til teamet og derefter tildeler ressourcen opgaver i tidsplanen, når du bruger **Vedligehold reservationer** til at ændre status fra **Definitiv** til **Foreløbig**, bevares opgavetildelingerne for ressourcen. Men under fanen **Afstemning** har ressourcen et reservationsunderskud, fordi kun definitive reservationer tages i betragtning ved afstemning af reservationer vs. tildelinger. Du kan bruge funktionen **Udvid reservationer** under fanen **Afstemning** til at reservere ressourcen definitivt for at eliminere underskuddet af definitive reservationer i forhold til ressourcetildelingerne. Du skal annullere den foreløbige reservation for ressourcen ved hjælp af **Vedligehold reservationer**.

Når du er klar til at ændre en foreløbigt reserveret teammedlemsressource til et definitivt reserveret teammedlem, skal du gøre følgende:

1. I planlægningsområdet skal du udvide ressourcen for at få vist hans eller hendes reservationer. Du kan se reservationen vist som **Foreløbig**.
2. Højreklik på reservationen, og vælg **Reservér definitivt** \> **Definitivt** under **Skift status**. Status for reservation er nu **Definitiv**.
3. Når du lukker planlægningsområdet, går tilbage til projektet og åbner fanen **Team**, kan du se, at timerne for ressourcen er flyttet fra kolonnen **Foreløbigt reserverede timer** til kolonnen **Definitivt reserverede timer** under fanen **Team**, når du har åbnet visningen **Navngivne teammedlemmer**. Hvis ressourcen blev tildelt til opgaver, viser de ikke længere et reservationsunderskud under fanen **Afstemning**, fordi deres reservationer nu er definitive.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
