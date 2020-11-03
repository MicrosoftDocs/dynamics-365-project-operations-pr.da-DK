---
title: Administrer tidszoner
description: Når et projekt oprettes, er tidszonen baseret på den tidszone, der er angivet i den anvendte arbejdstidsskabelon.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074110"
---
# <a name="manage-time-zones"></a>Administrer tidszoner

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


## <a name="projects"></a>Projekter

Når et projekt oprettes, er tidszonen baseret på den tidszone, der er angivet i den anvendte arbejdstidsskabelon. På **Projektet** for er datoerne altid relative i forhold til den brugers tidszone, der er logget på de enkelte faner, undtagen fanen **Opgave**. Når du får vist arbejdsopgavehierarkiet, vises datoerne altid i projektets tidszone.

## <a name="tasks"></a>Opgaver

Når en opgave er oprettet, styres starttidspunktet, sluttidspunktet og tider/dag af projektets arbejdstid. Hvis en opgave f.eks. er oprettet ved hjælp af et projekt, hvor tidszonen er -8 PST, og hvor de efterfølgende arbejdstider er: 9:00 til 17:00 mandag til fredag, vil alle opgaver, der er oprettet uden en tildeling, respektere starttidspunktet og sluttidspunktet for projektkalenderen.

## <a name="manage-resources-with-time-zones"></a>Administrer ressourcer med tidszoner

Hvis du vil have præcise og forudsigelige resultater, når du bruger **Forlæng reservation** , er der to nøgleforudsætninger, der skal overholdes:  

- Brugeren skal konfigurere enhedens tidszone, så den stemmer overens med den tidszone, der er angivet i systemets **Indstillinger for personlig tilpasning**.
 
  ![Tidszoneindstillinger i Windows 10](media/reconcile-assignments-03.png)

  ![Tidszoneindstillinger i tilpasningsindstillinger](media/reconcile-assignments-04.png)
 
- Den reserverbare ressource skal have mindst ét minuts arbejdstid, som overlapper med de profiler, der bruges til at definere den ønskede udvidelse. Følgende ressourcer kan f.eks. have arbejdstid mellem kl. 9:00 og 19:00. 

  ![Sammenligning af ressourceprofiler](media/reconcile-assignments-05.png)

Følgende tabel viser:

- En projektkalenderskabelon
- Ressource A: Denne ressource har samme kalender og er i den samme tidszone som projektet. Starttidspunktet for reservationerne er kl. 9:00.
- Ressource B: Denne ressource er placeret i en anden tidszone end projektet og starter kl. 7:00 i deres tidszone. Reservationerne starter dog kl. 9:00, som er det tidligste starttidspunkt for tildelingsprofilen.
- Ressourcer C og D: Ressourcerne er placeret i forskellige tidszoner, som både varierer i forhold til hinanden og projektet, og deres reservationer starter tidligst de respektive ledige starttider.

|Objekt  |Kalender  |
|-|-|
|Projektkalenderskabelon   | ![projektkalender](media/reconcile-assignments-06.png) |
|Ressource A  | ![Kalender for ressource A](media/reconcile-assignments-06.png) |
|Ressource B  |  ![Kalender for ressource B](media/reconcile-assignments-07.png) |
|Ressource C  |  ![Kalender for ressource C](media/reconcile-assignments-08.png) |
|Ressource D  | ![Kalender for ressource D](media/reconcile-assignments-09.png)  |
 
Når du navigerer til visningen **Afstemning** , vises ressourcetildelingerne og de manglende tilknyttede reservationer.

![Afstemningsvisning før udvidelse](media/reconcile-assignments-10.png)

Når funktionen til forlængelse af reservation er blevet brugt for de enkelte ressourcer, forlænges reservationerne for hver ressource, da hver ressources arbejdstid overlappede med underskudsprofilerne.

![Afstemningsvisning efter reservationsudvidelse](media/reconcile-assignments-11.png) 

Bemærk, hvis du kigger nærmere på detaljerne for reservationerne, kan du se forskelle på starttidspunkterne for reservationerne. Reservationernes startdato er ikke tidligere end starttidspunktet for tildelingsprofilen og kan ikke være før ressourcens tilgængelige starttidspunkt.

![Nye reservationer af ressourcerne i planlægningsområdet](media/reconcile-assignments-12.png)
