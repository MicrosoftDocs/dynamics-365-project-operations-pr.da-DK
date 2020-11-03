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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074378"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Planlægge ressourcer til et projekt (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Du kan kontrollere ressourcetilgængelighed for at få et generelt overblik over reservationer af dine ressourcer, eller du kan filtrere visningen efter færdigheder, team, placering og andre indstillinger.  
  
Planlægningsområdet viser en liste over ressourcer og deres tilgængelighed. Vælg en visningstilstand for at få vist tilgængelighed efter **timer** , **dag** , **uge** eller **måned**.  
  
Før du bruger planlægningsområdet, er det vigtigt at konfigurere det. Du kan finde flere oplysninger under [Konfigurering af planlægningsområdet (Field Service eller Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Hvis du bruger en ældre version, kan du finde oplysninger om ressourcetilgængelighed under [Få vist ressourcetilgængelighed](../psa/view-resource-availability.md).  

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
  
1.  I planlægningsområdet skal du vælge **Visningstilstand** , og derefter vælge **Dage**.  
  
    Der åbnes en gittervisning over, hvor mange timer en ressource er reserveret pr. dag, og hvilke dage ressourcen er ledig.  
  
2.  Klik på navnet på den ressource, du vil reservere, og vælg derefter **Reservér**.  
  
3.  I dialogboksen **Ressourcereservation (opret)** skal du vælge det projekt, du vil reservere ressourcen til, sammen med en reservationsmetode og start- og sluttidspunkter.  
  
4.  Når du er færdig, skal du vælge **Reservér**.  
  
## <a name="view-to-the-schedule-board"></a>Visning til planlægningsområdet
  
1.  Vælg et ikke-planlagt reservationskrav på listen nederst.  
  
2.  Træk reservationskravet til en tilgængelig ressource eller tidsrubrik i planlægningsområdet.  
  
3.  Når du er færdig, skal du vælge **Reservér**.  
  
### <a name="additional-resources"></a>Flere ressourcer  
 [Ressourcestyringsvejledning](../psa/resource-manager-guide.md)
