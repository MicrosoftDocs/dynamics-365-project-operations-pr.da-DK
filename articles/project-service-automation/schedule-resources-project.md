---
title: Planlægge ressourcer til et projekt
description: Sådan planlægger du ressourcer til et projekt i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750618"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Planlægge ressourcer til et projekt (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Du kan kontrollere ressourcetilgængelighed for at få et generelt overblik over reservationer af dine ressourcer, eller du kan filtrere visningen efter færdigheder, team, placering og andre indstillinger.  
  
Planlægningsområdet viser en liste over ressourcer og deres tilgængelighed. Vælg en visningstilstand for at få vist tilgængelighed efter **timer**, **dag**, **uge** eller **måned**.  
  
Før du bruger planlægningsområdet, er det vigtigt at konfigurere det. Du kan finde flere oplysninger under [Konfigurering af planlægningsområdet (Field Service eller Project Service Automation)](../field-service/configure-schedule-board.md).
  
Hvis du bruger en ældre version, kan du finde oplysninger om ressourcetilgængelighed under [Få vist ressourcetilgængelighed](../project-service/view-resource-availability.md).  

> [!IMPORTANT]
>  For at bruge reservationsfunktionerne for planlægningsområde, geokodnings- og placeringstjenester skal du aktivere kort.  
> 
> 1. I hovedmenuen skal du vælge **Ressourceplanlægning** > **Administration**.  
> 2. Klik på **Planlægningsparametre**.  
> 3. Åbn posten, og rul ned til afsnittet **Resource Scheduling Optimization**.  
> 4. I feltet **Opret forbindelse til kort** skal du vælge **Ja**.  
> 5. Acceptér vilkårene, og gem posten.  
> 6. I hovedmenuen skal du vælge **Project Service** > **Planlægningsområde**. Herfra er der flere måder at planlægge et reservationskrav på manuelt. Vælg den metode, der fungerer for dig.
  
## <a name="find-available-resources"></a>Find tilgængelige ressourcer

1.  På listen **Krav til reservationer** skal du højreklikke på en ikke-planlagt reservation og vælge en af følgende fremgangsmåder:  
  
- Vælg **Søg efter Tilgængelighed – Aktuelle ressourcer** for at finde en tilgængelig ressource på listen i planlægningsområdet.  
- Vælg **Søg efter Tilgængelighed – Alle ressourcer** for at finde en tilgængelig ressource blandt ressourcerne i systemet.  
   > [!NOTE]
   >  Når du gør dette, viser filtrene indstillinger for det valgte reservationskrav.  
  
2. Når du ser en tilgængelige rubrik, skal du højreklikke på tidsrubrikken i planlægningsområdet og vælge **Reservér her**. Eller træk og slip reservationskravet til den ledige tidsrubrik.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Reservere en ressource ved hjælp af visningen daglig og finde ud af, hvem der er underreserveret
  
1.  I planlægningsområdet skal du vælge **Visningstilstand**, og derefter vælge **Dage**.  
  
    Der åbnes en gittervisning over, hvor mange timer en ressource er reserveret pr. dag, og hvilke dage ressourcen er ledig.  
  
2.  Klik på navnet på den ressource, du vil reservere, og vælg derefter **Reservér**.  
  
3.  I dialogboksen **Ressourcereservation (opret)** skal du vælge det projekt, du vil reservere ressourcen til, sammen med en reservationsmetode og start- og sluttidspunkter.  
  
4.  Når du er færdig, skal du vælge **Reservér**.  
  
## <a name="view-to-the-schedule-board"></a>Visning til planlægningsområdet
  
1.  Vælg et ikke-planlagt reservationskrav på listen nederst.  
  
2.  Træk reservationskravet til en tilgængelig ressource eller tidsrubrik i planlægningsområdet.  
  
3.  Når du er færdig, skal du vælge **Reservér**.  
  
### <a name="additional-resources"></a>Flere ressourcer  
 [Ressourcestyringsvejledning](../project-service/resource-manager-guide.md)
