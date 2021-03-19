---
title: Afstemme reservationer og tildelinger
description: Dette emne indeholder oplysninger om faktiske værdier.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 30af3cca9b4c3dc3f1a9412de7380c963bde88f0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283406"
---
# <a name="reconcile-bookings-and-assignments"></a>Afstemme reservationer og tildelinger

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Et projektteammedlems projektreservationer og projektopgavetildelinger er løst sammenkoblet. En ressource kan derfor have opgavetildelinger, der ikke stemmer overens med reservationer, og reservationer, der ikke stemmer overens med opgavetildelinger. Ideelt set skal projektreservationer og -tildelinger justeres, så ressourcer har bindende kapacitet til at udføre deres opgavetildelingerne. Virkeligheden er, at reservationer kan ske på baggrund af tilgængelighed, og at opgavetidspunkter kan ændres, efterhånden som projektet gennemføres i sin livscyklus. Derfor giver den løse sammenkobling større fleksibilitet.

På grund af den løse sammenkobling af projektreservationer og opgavetildelinger findes der en fane **Afstemning** på projektobjektet. Denne fane hjælper projektledere med at afstemme teammedlemmernes reservationer og tildelinger for deres projektteam.

For hvert navngivet teammedlem viser fanen **Afstemning** reservationer og tildelinger helt ned til niveauet for de enkelte opgavetildelinger. Den viser timer i celler, der kan repræsentere tidsperioder fra måneder ned til dage.

I feltet **Tidsskala** kan du vælge **Måned**, **Uge** eller **Dag**. **Uge** er valgt som standard. Men du kan dog ændre standardværdien ved at vælge knappen **Indstillinger.** Når fanen **Afstemning** åbnes, vises dags dato, men du kan bruge kalenderkontrolelementet til at gå frem eller tilbage i tiden. Når et projekt har en startdato, der ligger ud i fremtiden, vises datoen under fanen, når den åbnes. Kalenderkontrolelementet indeholder også indstillinger, du kan bruge til at gå til projektets start- og slutdatoer.

Du kan bruge kontrolelementerne for udvidelser på de enkelte ressourcer til at få vist detaljer om den pågældende ressources reservationer. Du kan også udvide hver ressources tildelinger til niveauet for den enkelte opgave.

Nederst under fanen **Afstemning** vises et samlet nettototal for projektet, og fanen indeholder også kolonnen total. For hver ressource beregner fanen forskellen mellem et teammedlems reservationer i forbindelse med projektet og dette teammedlems akkumulering af opgavetildelinger. Ideelt skal forskellen være 0 (nul). Det vil sige, at der ikke bør være nogen forskel mellem ressourcens reservationer og opgavetildelinger. Eventuelle forskelle er angivet ved farve og skygge for at gøre opmærksom på to forhold:

- **Manglende reservation** – Der opstår manglende reservation, når en ressource har flere tildelinger end reservationer. Da denne kapacitet ikke er reserveret, kan en projektleder rette dette forhold ved at forlænge reservationer af ressourcen for at dække underskuddet.
- **Overskydende reservationer** – Der forekommer overskydende reservationer, når en ressource er blevet reserveret til projektet, men ikke er tildelt opgaver. Dette forhold kan være acceptabelt, hvis ressourcen f.eks. er blevet reserveret, før opgavetildelingen finder sted. I andre tilfælde er ressourcen måske ikke planlagt til at blive tildelt. I disse tilfælde skal projektlederen overveje at annullere reservationerne af ressourcen, så kapaciteten kan bruges til et andet projekt.

> [!NOTE]
> Forklaringen på disse forhold kan være skjult for at give mere plads til gitteret. I så fald kan du gøre forklaringen synlig ved at klikke på knappen **Indstillinger**.

Når feltet **Tidsskala** er angivet til et niveau, der er højere end **Dag**, kan forskelle i visse tilfælde blive beregnet til 0 (nul). På niveauet **Måned** kan nettoforskellen for en ressource f.eks. være 0 (nul) for at angive, at reservationer stemmer overens med tildelinger. Men hvis du kigger på niveauet **Uge**, kan du muligvis se, at der er tildelinger på 0 (nul) timer og reservationer på 40 timer i den første uge af måneden, og tildelinger på 40 timer og reservationer på 0 (nul) timer i løbet af den anden uge af måneden. Selvom det samlede antal reservationer og tildelinger for måneden er ens, er de forskellige fra uge til uge.

Når du får vist tiden på højere niveauer, har fanen **Afstemning** en celleindikator, der giver dig besked om, at der er forskelle på lavere tidsniveauer. I den følgende illustration vises der f.eks. en celleindikator i cellen for oktober 2018 for den ressource, der hedder Elisabeth Larsen. Du kan derfor se, at selvom ressourcens reservationer og tildelinger er ens, når de samles på niveauet **Måned**, matcher de ikke på lavere niveauer.

![Uoverensstemmende reservationer og tildelinger på månedsniveau](media/reconcile-assignments-01.JPG)

Dobbeltklik på en celle for at zoome ind på det næste lavere niveau og få vist forskellen. Hvis du f.eks. dobbeltklikker på forskellen for oktober 2018 for Elisabeth Larsen, kan du gå ned på niveauet **Uge**. Du kan derefter se, at ressourcen har reservationer på 16 timer, men ingen tildelinger, i de første to uger af oktober og 16 timers tildelinger, men ikke reservationer, i 3. uge af oktober.

![Uoverensstemmende reservationer og tildelinger på ugeniveau](media/reconcile-assignments-02.JPG)

Du kan højreklikke på en celle for at zoome ud på det næste højere niveau. Du kan også slå celleindikatoren fra ved at klikke på knappen **Indstillinger**. 

Du kan også bruge knapperne **Forrige** og **Næste** over gitteret til at bevæge dig igennem eventuelle forskelle i projektet. Hvis du vil bruge disse knapper, skal du først vælge en ressource. Vælg **Næste** for at gå til den næste forskel mellem reservationer og tildelinger for den pågældende ressource. Vælg **Forrige** for at gå til den forrige forskel.

I situationer, hvor du har opgavetildelinger for en ressource men ingen reservationer, kan du vælge den manglende reservation og derefter vælge **Udvid reservation**. Du kan derefter se den reservation, der kræves for at løse manglen på ressourcen. Du kan også få vist ressourcens reservationer i det aktuelle projekt og i andre projekter. Vælg **OK** for at oprette reservationen for ressourcen uden hensyn til aktuel tilgængelighed. Projektlederen eller den ressourceansvarlige kan derefter bruge planlægningsområdet til at administrere de situationer, hvor en ressource overreserveres i forhold til dens kapacitet, fordi reservationerne heraf blev udvidet.

## <a name="managing-with-time-zones"></a>Administration af tidszoner
For at sikre præcise og forudsigelige resultater i forbindelse med anvendelsen af udvidet reservation er der to nøgleforudsætninger, som skal være opfyldte:  

- Brugeren skal konfigurere enhedens tidszone, så den stemmer overens med den tidszone, der er angivet i systemets tilpasningsindstillinger.
 
  ![Tidszoneindstillinger i Windows 10](media/reconcile-assignments-03.png)

  ![Tidszoneindstillinger i tilpasningsindstillinger](media/reconcile-assignments-04.png)
 
- Den reserverbare ressource skal have mindst ét minuts arbejdstid, som overlapper med de profiler, der bruges til at definere den ønskede udvidelse. F.eks. viser følgende eksempel, hvordan du gennemser ressourcer med arbejdstimer, der ligger mellem kl. 9:00 og 19:00. 

  ![Sammenligning af ressourceprofiler](media/reconcile-assignments-05.png)

Følgende tabel viser:

- En projektkalenderskabelon.
- Ressource A: Denne ressource har samme kalender og er i den samme tidszone som projektet. Starttidspunktet for reservationerne er kl. 9:00.
- Ressourcer B: Denne ressource er placeret i en anden tidszone end projektet og starter derfor kl. 19:00 i deres tidszone. Reservationerne starter dog kl. 9:00, som er det tidligste starttidspunkt for tildelingsprofilen.
- Ressourcer C og D: Disse ressourcer er ligeledes placeret i forskellige tidszoner, som både adskiller sig fra hinanden og projektet, og deres reservationer starter tidligst på deres respektive ledige starttider.

|Objekt  |Kalender  |
|-|-|
|Projektkalenderskabelon   | ![projektkalender](media/reconcile-assignments-06.png) |
|Ressource A  | ![Kalender for ressource A](media/reconcile-assignments-06.png) |
|Ressource B  |  ![Kalender for ressource B](media/reconcile-assignments-07.png) |
|Ressource C  |  ![Kalender for ressource C](media/reconcile-assignments-08.png) |
|Ressource D  | ![Kalender for ressource D](media/reconcile-assignments-09.png)  |
 
Når du navigerer til afstemningsvisningen, vises ressourcetildelingerne og de tilknyttede reservationsunderskud.
 ![Afstemningsvisning før udvidelse](media/reconcile-assignments-10.png)

Når funktionen til udvidelse af reservationer er blevet udført for de enkelte ressourcer, udvides reservationerne for hver ressource. Dette skyldes, at de enkelte ressourcers arbejdstimer overlapper med profilerne for underskuddet.
 ![Afstemningsvisning efter reservationsudvidelse](media/reconcile-assignments-11.png) 

Du kan dog få vist de nærmere detaljer for reservationen, hvoraf forskellene i starttidspunkterne for reservationerne fremgår. Reservationerne starter tidligst på starttidspunktet for tildelingsprofilen og ikke førend ressourcens tilgængelige starttidspunkt.
 ![Nye reservationer af ressourcerne i planlægningsområdet](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]