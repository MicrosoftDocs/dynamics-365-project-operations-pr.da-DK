---
title: Konfigurer kilometertal ved hjælp af niveauer for kilometertal
description: Denne artikel indeholder oplysninger om kilometertal og niveauer for kilometertal.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9689bbaf4c4f88ad9f746c3f98676f97e634ab6c
ms.sourcegitcommit: 5e1f549a2e55a87351b2979e3aff402ed35487e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9064271"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Konfigurer kilometertal ved hjælp af niveauer for kilometertal

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når en omkostning rapporteres, og den valgte udgiftskategori er **Kilometertal**, beregnes beløbet for den pågældende udgiftslinje i henhold til beløbet *sats pr. kilometer*. Dette beløb bestemmes ved hjælp af definerede kilometerniveauer eller ved at følge en standardsats for kilometertal, hvis der ikke er konfigureret kilometerniveauer. 

Kilometerniveauer kan konfigureres ved at gå til **Udgiftsstyring** > **Konfiguration** > **Generelt** > **Udgiftskategorier** > **Kilometertal** > **Opsætning af kategori**.

Når du har opgraderet til 10.0.18, kan du overveje at aktivere kilometertalsfunktionen, når du har gennemset designændringerne nedenfor, hvis din organisation bruger udgiftskategorien for kilometertal. 

Det nye design af kilometertalsniveauer påvirker, hvordan værdien i feltet **Antal** behandles. Før udgivelsen af 10.0.18 blev værdien i feltet **Mængde** anset for at være den nederste grænse. Når værdien blev overgået, blev den tilsvarende sats anvendt.  Fra og med 10.0.18 betragtes værdien i feltet **Antal** som den øverste grænse. Den tilsvarende sats bruges, når kilometertallet er mindre end værdien i feltet **Antal**.  Den nye model for kilometertal er med til at gøre kilometertalsniveauer mere ensartede og mere anvendelige.   

Alle godkendte udgiftsrapporter genberegnes i forbindelse med bogføring i henhold til det nye design.

## <a name="example"></a>Eksempel
 
### <a name="before-version-10018"></a>Før version 10.0.18
Med to kilometertalsniveauer repræsenterer feltet **Antal** på de enkelte niveauer den lavere kilometertalsgrænse. I øjeblikket har niveau et en værdi på nul (0) og en sats på 0,45, og niveau to har en værdi på 1.000 og en sats på 0,25. Hvis de akkumulerede kilometer overstiger værdien i feltet, anvendes den relaterede sats. Hvis der ikke findes en linje med et nulantal, bruger systemet den sats for kilometertal, der er defineret i Udgiftsstyring. 
 
Hvis en medarbejder indsender en udgiftsrapport med 1.500 kilometer, er de to kilometerlinjer i den bogførte udgiftsrapport: 1.000 (sats 0,45) + 500 (sats 0,25) = 575,00.

### <a name="after-version-10018"></a>Efter version 10.0.18
I 10.0.18 repræsenterer feltet **Antal** på de enkelte niveauer den øverste grænse for niveauet. I øjeblikket har niveau et en værdi på 999 og en sats på 0,45, og niveau to har en værdi på 999.999.999,00 og en sats på 0,25. Hvis de akkumulerede kilometer overstiger værdien i feltet **Antal**, anvendes den relaterede sats. Hvis alle øvre grænser overskrides, bruger systemet den sats for kilometertal, der er defineret i Udgiftsstyring. 
 
Hvis det samme scenario skal beregnes korrekt, skal det niveau, der er konfigureret, ændres. Feltet **Antal** på niveau et har en værdi på 999,00 og en værdi 999.999.999,00 i niveau to. Hvis en medarbejder overskrider den samlede mængde af ressourcer eller kilometer på niveau et, bruges den sats for kilometertal, der er defineret i Udgiftsstyring. 
  
Hvis en medarbejder indsender en udgiftsrapport med 1.500 kilometer, er de to kilometerlinjer i den bogførte udgiftsrapport: 1.000 (sats 0,45) + 500 (sats 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Aktivér beregningen af kilometertal for funktionen med flere kilometerniveauer med samme sats

**Beregningen af kilometertal for funktionen med flere kilometerniveauer med samme sats** forbedrer beregningen af kilometersats. Fuldfør følgende trin for at aktivere denne funktion.

1. Gå til **Arbejdspladser** > **Funktionsstyring**. 
2. Find og vælg **Beregning af antal kilometertal for flere kilometer med samme sats** på listen, og vælg derefter **Aktivér nu**.

Når du har aktiveret funktionen, skal du nulstille kilometerniveauer, så de korrekt afspejler værdien i feltet **Antal**. 

## <a name="enable-the-mileage-totals-calculation-by-fiscal-year-feature"></a>Aktivér funktionen Beregning af totaler for antal kilometer i henhold til regnskabsår

Funktionen **Beregning af totaler for antal kilometer i henhold til regnskabsår** gør det muligt at angive en ny indstilling i Parametre for administration af udgifter, der udfører beregninger af samlede antal kilometer i henhold til regnskabsår i stedet for kalenderåret. Fuldfør følgende trin for at aktivere denne funktion.

1. Gå til **Arbejdspladser** > **Funktionsstyring**.
1. Find og vælg **Beregning af totaler for antal kilometer i henhold til regnskabsår** på listen, og vælg derefter **Aktivér nu**.
1. Gå til **Udgiftsstyring** > **Opsætning** > **Generelt** > **Parametre for udgiftsstyring**.
1. På siden **Parametre for administration af udgifter** skal du finde og aktivere **Brug regnskabsår til samlede antal kilometer**.

Når du har aktiveret **Brug regnskabsår for samlede antal kilometer**, beregnes de samlede antal kilometer efter regnskabsår.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
