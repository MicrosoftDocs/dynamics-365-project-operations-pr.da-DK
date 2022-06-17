---
title: Sporing af projektsalg
description: Denne artikel indeholder oplysninger om, hvordan Project Operations sporer fremgang i forhold til arbejdsomsætning på et projekt.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce61acf95ee5e9ac10047406c9d4a5c9b1f92aad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911267"
---
# <a name="project-sales-tracking"></a>Sporing af projektsalg

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations sporer arbejdsestimater og -omsætning på den laveste krævede granularitet i en projektplan. Estimatet for arbejdsomsætning er baseret på den planlagte indsats og de generiske eller navngivne ressourcer, der er tildelt de enkelte bladnodeopgaver i projektplanen. Når projektet starter, og folk begynder at indberette tid på forskellige projektopgaver, opsummeres den faktiske arbejdsomsætning, hvilket starter en beregning af projektionerne.

## <a name="labor-revenue-tracking-view"></a>Visning af sporing af arbejdsomsætning

På siden **Projekter** kan du under fanen **Sporing** vælge **Sporing** > **Omkostning** for at åbne visningen **Omkostningssporing**. Du kan også vælge **Brug** > **Fakturasats** for at åbne visningen **Omsætningssporing**, der viser status for arbejdsomsætningen for de enkelte opgaver i projektplanen. I denne visning sammenlignes også den faktiske arbejdsomsætning, der er brugt på en opgave, med opgavens planlagte arbejdsomsætning. Project Operations bruger følgende formler til at beregne målepunkterne for arbejdsomsætning:

- **Planlagt omsætning**: Estimerede salgsværdier for alle ressourcetildelinger på de enkelte bladnodeopgaver
- **Faktisk omsætning**: Summen af alle ikke-fakturerede faktisk salg for den tid, der er registreret på opgaven
- **Fakturerbar omsætning %**: Faktisk omsætning - estimeret omsætning ved fuldførelse
- **Resterende omsætning**: Estimeret omsætning ved fuldførelse - faktisk omsætning
- **Estimeret omsætning ved fuldførelse**: Resterende omsætning + faktisk omsætning
- **Omsætningsafvigelse**: Planlagt omsætning - estimeret omsætning ved fuldførelse


> [!NOTE]
> I Project Operations vises arbejdsomsætninger kun på siden **Projekt** under fanen **Sporing**. Selv om materialer og udgifter kan estimeres og spores til forbrug, medtages disse omsætninger ikke i de omsætninger, der vises under fanen **Sporing**. Denne fane er designet til kun at fungere for nye projekteringer af arbejdsomsætning ved at foretage en ny projektering for indsatsen.  
> Alle viste omsætningsbeløb konverteres til projektets omkostningsvaluta. Projektets omkostningsvaluta er valutaen for den kontraktenhed, der indgår i projektet. I fastprisprojekter er omsætningstal i visningen **Sporing af arbejdsomsætning** ikke relevante, da ikke-fakturerede faktiske salg ikke registreres, når tiden er godkendt.
> De anslåede salgsværdier for tid, der vises under fanen **Estimat** for projektet, beløber sig muligvis ikke til den planlagte omsætningsværdi under fanen **Sporing**. Der kan være to mulige årsager til denne uoverensstemmelse:
><ol>
   ><li> Fanen <b>Estimater</b> viser den anslåede omsætning i salgsvalutaen, mens fanen <b>Sporing</b> viser den planlagte omsætning omregnet til omkostningsvalutaen. </li>
   ><li> Når anslåede salg konverteres til kontraktvalutaen, som vises under fanen <b>Estimater</b>, til projektvalutaen, indebærer konverteringen trin, der kan resultere i et vist præcisionstab: </li>
><ol>
><li> De anslåede salgsbeløb i kontraktvalutaen konverteres først til grundvalutaen (konvertering 1).</li>
><li> De anslåede salgsbeløb i grundvalutaen konverteres til projektets omkostningsvaluta (konvertering 2). </li>
></ol>
></ol>
> Valutapræcision anvendes i begge trin, hvilket resulterer i, at den planlagte omsætning i projektvalutaen afviger fra det planlagte salg i kontraktvalutaen.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Omprojektering af omsætninger på bladnodeopgaver

Arbejdsomsætning på en bladnodeopgave kan ikke omprojekteres direkte under fanen **Sporing** på siden **Projekt**. Du kan dog bruge visningen **Indsatssporing** til at omprojektere den resterende indsats på en opgave. Derved genberegnes den resterende omsætning på opgaven. Nedenfor følger en beskrivelse af, hvordan dette fungerer.

1. En projektleder kan omprojektere indsatsen på opgaver ved at opdatere standardværdien i feltet **Resterende indsats** med et nyt estimat af den resterende indsats på opgaven. Omprojektering medfører, at opgavens anslåede indsats ved fuldførelse (EAC), færdiggørelsesprocenten og den forventede omkostningsafvigelse for en opgave genberegnes. EAC, estimatet ved fuldførelse (ETC) og færdiggørelsesprocenten for hovedopgaverne genberegnes også og giver en ny projektion af indsatsafvigelsen.
2. På grundlag af den nye værdi for den resterende indsats på opgaven beregner systemet den resterende omsætning i visningen **Omsætningssporing**. Hvis du vil beregne den resterende omsætning på baggrund af den resterende indsats, beregner systemet først den gennemsnitlige omsætning for en times indsats på hovedopgaven som planlagt omsætning eller en planlagt indsats. Den planlagte omsætning er summen af omsætningen for alle ressourcetildelinger på opgaven. Den gennemsnitlige omsætning pr. time bruges til at beregne den resterende omsætning for den nyligt anslåede resterende indsats på opgaven.
3. Den estimerede omsætning ved fuldførelse og procenten for omsætningsforbruget på bladnodeopgaven beregnes igen.
4. Værdien af omsætningen ved fuldførelse for hovedopgaverne genberegnes helt ned til rodnoden.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Omprojektering af omsætninger på hovedopgaver

Du kan omprojektere arbejdsomsætning på hovedopgaver eller beholderopgaver. Arbejdsomsætning på en hovedprojektopgave kan dog ikke omprojekteres direkte under fanen **Sporing** på siden **Projekt**. På samme måde som ved bladnodeopgaver kan omprojektering af hoved- og beholderopgaver udføres ved hjælp af visningen **Indsatssporing**. I denne visning kan du omprojektere den resterende indsats på en hovedopgave, hvilket medfører en genberegning af den resterende omsætning på hovedopgaven. Nedenfor følger en beskrivelse af, hvordan dette fungerer.

1. En projektleder kan omprojektere indsatsen på opgaver ved at opdatere standardværdien i feltet **Resterende indsats** med et nyt estimat af den **Resterende indsats** på opgaven. Omprojektering medfører, at opgavens estimat ved fuldførelse (EAC), færdiggørelsesprocenten og den forventede omkostningsafvigelse for en opgave genberegnes. EAC, ETC og fremgangen i procenten for hovedopgaver genberegnes også og giver en ny projektion af afvigelsen i tidsforbruget.
2. På grundlag af den nye værdi i feltet **Resterende indsats** på opgaven beregner systemet den resterende omsætning i visningen **Omsætningssporing**. Hvis du vil beregne den resterende omsætning på baggrund af resterende indsats, beregner systemet først den gennemsnitlige omsætning for en times indsats på hovedopgaven som planlagt omsætning eller en planlagt indsats. Den planlagte omsætning er summen af omsætningen for alle ressourcetildelinger på opgaven. Denne gennemsnitlige omsætning pr. time bruges derefter til at beregne omsætningen for den nyligt anslåede resterende indsats på opgaven.
3. Den estimerede omsætning ved fuldførelse og procenterne for omsætningsforbruget på hovedopgaven beregnes igen.
4. Den nye værdi for den estimerede omsætning ved fuldførelse fordeles nedad til de underordnede opgaver i samme forhold, som den oprindelige planlagte omsætning på opgaven blev fordelt.
5. Den nye estimerede omsætning ved fuldførelse for hver af de enkelte opgaver nedad til bladnodeopgaver beregnes. På grundlag af denne værdi genberegnes den resterende omsætning og procenten for omsætningsforbruget for de berørte underopgaver helt ned til bladnoderne på baggrund af værdien for omsætning ved fuldførelse. Dette medfører, at der laves en ny projektion for afvigelsen i omsætningen for opgaven. 
6. Værdien af omsætningen ved fuldførelse for hovedopgaverne genberegnes helt ned til rodnoden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

