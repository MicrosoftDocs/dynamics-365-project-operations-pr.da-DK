---
title: Foreløbig reservation af krav
description: Dette emne indeholder oplysninger om, hvordan du reserverer krav foreløbigt.
author: ruhercul
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
ms.openlocfilehash: 95f064e0f83d2052ac4ae9673b4fcdcd16a2574246d3320e1ed3798cd6ff062b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007004"
---
# <a name="soft-book-requirements"></a>Foreløbig reservation af krav

[!include [banner](../includes/psa-now-project-operations.md)]

Et ressourcekrav kan reserveres definitivt. En definitiv reservation opretter et forslag, der forbruger en ressources kapacitet. Derefter sendes forslaget tilbage til anmoderen til godkendelse. En foreløbig reservation føjer foreløbigt en ressource til et projektteam og har en anden status i planlægningsområdet, men den forbruger ikke ressourcens kapacitet. Hvis du reserverer en ressource foreløbigt i planlægningsområdet, skal du angive feltet **Reservationsstatus** til **Foreløbig**.

![Reservationsstatus indstillet til Foreløbig.](media/Resource-Management-image77.png)

Når fanen **Team** er i visningen **Navngivne teammedlemmer**, vises ressourcen her. Timer der er foreløbigt reserveret i kolonnen **Foreløbigt reserverede timer**.

![Foreløbigt reserverede timer i visningen Navngivne teammedlemmer.](media/Resource-Management-image78.png)

Foreløbigt reserverede teammedlemmer kan tildeles til opgaver.

![Foreløbigt reserveret teammedlem tildelt til en opgave.](media/Resource-Management-image79.png)

På fanen **Afstemning** vises der ingen reservationer for en foreløbigt reserveret ressource, da fanen **Afstemning** kun medtager definitive reservationer.

![Foreløbigt reserveret ressource uden reservationer på fanen Afstemning.](media/Resource-Management-image80.png)

> [!NOTE]
> Du kan ikke reservere en ressource foreløbigt i et krav, der blev genereret i et generisk teammedlem.

I planlægningsområdet bruges der en anden farve til foreløbige reservationer af en ressource.

![Foreløbige reservationer i planlægningsområdet.](media/Resource-Management-image81.png)

Hvis du vil konvertere en foreløbig reservation til en definitiv reservation, skal du højreklikke på den foreløbige reservation i planlægningsområdet og derefter vælge **Skift status** \> **Definitiv reservation** \> **Definitiv**.

![Ændring af reservationsstatus til Definitiv.](media/Resource-Management-image82.png)

Reservationen ændres, og statussen ændres i planlægningsområdet. Da reservationsstatussen nu er **Definitiv**, vises ressourcen som reserveret, og dens kapacitet og tilgængelighed justeres.

Du kan bruge samme metode til at annullere en definitiv reservation eller en midlertidig reservation i planlægningsssområdet.

Hvis du vil konvertere en ressource, der er foreløbigt reserveret til definitivt reserveret på projektets fane **Team,** skal du vælge ressourcen og derefter **Bekræft**.

![Bekræft kommando.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]