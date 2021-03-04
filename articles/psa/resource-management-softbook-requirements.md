---
title: Foreløbig reservation af krav
description: Dette emne indeholder oplysninger om, hvordan du reserverer krav foreløbigt.
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
ms.openlocfilehash: 09f7acb95be014034cc03d7eed9d37363d430601
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147376"
---
# <a name="soft-book-requirements"></a>Foreløbig reservation af krav

[!include [banner](../includes/psa-now-project-operations.md)]

Et ressourcekrav kan reserveres definitivt. En definitiv reservation opretter et forslag, der forbruger en ressources kapacitet. Derefter sendes forslaget tilbage til anmoderen til godkendelse. En foreløbig reservation føjer foreløbigt en ressource til et projektteam og har en anden status i planlægningsområdet, men den forbruger ikke ressourcens kapacitet. Hvis du reserverer en ressource foreløbigt i planlægningsområdet, skal du angive feltet **Reservationsstatus** til **Foreløbig**.

![Reservationsstatus indstillet til Foreløbig](media/Resource-Management-image77.png)

Når fanen **Team** er i visningen **Navngivne teammedlemmer**, vises ressourcen her. Timer der er foreløbigt reserveret i kolonnen **Foreløbigt reserverede timer**.

![Foreløbigt reserverede timer i visningen Navngivne teammedlemmer](media/Resource-Management-image78.png)

Foreløbigt reserverede teammedlemmer kan tildeles til opgaver.

![Foreløbigt reserveret teammedlem tildelt til en opgave](media/Resource-Management-image79.png)

På fanen **Afstemning** vises der ingen reservationer for en foreløbigt reserveret ressource, da fanen **Afstemning** kun medtager definitive reservationer.

![Foreløbigt reserveret ressource uden reservationer på fanen Afstemning](media/Resource-Management-image80.png)

> [!NOTE]
> Du kan ikke reservere en ressource foreløbigt i et krav, der blev genereret i et generisk teammedlem.

I planlægningsområdet bruges der en anden farve til foreløbige reservationer af en ressource.

![Foreløbige reservationer i planlægningsområdet](media/Resource-Management-image81.png)

Hvis du vil konvertere en foreløbig reservation til en definitiv reservation, skal du højreklikke på den foreløbige reservation i planlægningsområdet og derefter vælge **Skift status** \> **Definitiv reservation** \> **Definitiv**.

![Ændring af reservationsstatus til Definitiv](media/Resource-Management-image82.png)

Reservationen ændres, og statussen ændres i planlægningsområdet. Da reservationsstatussen nu er **Definitiv**, vises ressourcen som reserveret, og dens kapacitet og tilgængelighed justeres.

Du kan bruge samme metode til at annullere en definitiv reservation eller en midlertidig reservation i planlægningsssområdet.

Hvis du vil konvertere en ressource, der er foreløbigt reserveret til definitivt reserveret på projektets fane **Team,** skal du vælge ressourcen og derefter **Bekræft**.

![Bekræft kommando](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]