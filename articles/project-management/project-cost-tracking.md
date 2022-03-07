---
title: Sporing af omkostninger på projekt
description: Denne emne oplysninger om, hvordan Project Operations sporer status i forhold til arbejdsomkostninger og bruger på et projekt.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d37df64db1808722b7851c952c20be731aa2d670fe066c02ef90386712487407
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987789"
---
# <a name="labor-cost-tracking-on-projects"></a>Sporing af arbejdsomkostninger på projekter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations sporer arbejdsestimater og -forbrug på den laveste krævede granularitet i projektplanen. Det økonomiske estimat for arbejdsomkostninger er baseret på den planlagte indsats og de generiske eller navngivne ressourcer, der er tildelt de enkelte bladnodeopgaver i projektplanen. Når projektet starter, og folk begynder at indberette tid på forskellige projektopgaver, opsummeres de faktiske arbejdsomkostninger, hvilket starter en beregning af projektionerne.

## <a name="labor-cost-tracking-view"></a>Visning af arbejdsomkostningssporing

På siden **Projekter** under fanen **Sporing** kan du vælge **Sporing** > **Omkostninger** for at åbne visningen **Omkostningssporing** og se statussen for arbejdsforbrug på de enkelte opgaver i projektplanen. I denne visning sammenlignes også de faktiske arbejdsomkostninger, der er brugt på en opgave, med opgavens planlagte arbejdsomkostninger. Project Operations bruger følgende formler til at beregne målepunkterne for arbejdsomkostninger:

- **Planlagte omkostninger**: Estimerede omkostninger for alle ressourcetildelinger på de enkelte bladnodeopgaver
- **Faktiske omkostninger**: Summen af alle faktiske omkostninger for den tid, der er registreret på opgaven
- **Omkostningsforbrugsprocentprocent**: Faktiske omkostninger - omkostningsestimat ved fuldførelse
- **Resterende omkostninger**: Estimerede omkostninger ved fuldførelse - faktiske omkostninger
- **Omkostninger ved fuldførelse**: Resterende omkostninger + faktiske omkostninger
- **Omkostningsafvigelse**: Planlagte omkostninger - omkostningsestimat ved fuldførelse

Hver opgave viser en projektion af afvigelsen i omkostningerne for opgaven. Hvis omkostningsestimatet ved fuldførelse er større end de planlagte omkostninger, forventes opgaven at overskride budgettet. Hvis omkostningsestimatet ved fuldførelse er lavere end de planlagte omkostninger, forventes opgaven at koste mindre end det budgetterede.

>[!NOTE]
> I Project Operations vises arbejdstidsomkostninger kun på siden **Projekt** under fanen **Sporing**. Selv om materialer og udgifter kan estimeres og spores til forbrug, medtages disse omkostninger ikke i de omkostninger, der vises under fanen **Sporing**. Denne fane er designet til kun at fungere for nye projekteringer af arbejdsomkostninger ved at foretage en ny projektering for indsatsen.
Alle viste omkostningsbeløb konverteres til projektets omkostningsvaluta fra projektets kostprisvaluta, der bruges til at bestemme omkostningskursen. Projektets omkostningsvaluta er valutaen for den kontraktenhed, der indgår i projektet. De anslåede omkostningsværdier for tid, der vises under fanen **Estimater** på siden **Projekt**, beløber sig muligvis ikke til de planlagte omkostninger under fanen **Sporing**. Årsagen til denne uoverensstemmelse skyldes forskellene i, hvordan anslåede omkostninger opsummeres i gitteret **Estimater**, og hvordan de planlagte omkostninger beregnes i gitteret **Sporing**. 
>
> - **Fanen Estimater** beregner de anslåede omkostninger ved hjælp af samme valuta som omkostningskursen på prislisten. Derefter konverteres de anslåede omkostninger i prislistevalutaen til de anslåede omkostninger i projektets omkostningsvaluta. De anslåede omkostninger i projektvalutaen vises med to decimaler. Valutapræcision anvendes på intet tidspunkt under denne konvertering. 
> - Under fanen **Sporing** følger beregningen af de planlagte omkostninger en lidt anden beregningsrækkefølge, som indebærer, at valutapræcision anvendes i to faser: 
   ><ol>
   ><li>Det anslåede omkostningsbeløb i prislistevalutaen konverteres til grundvalutaen (konvertering 1).</li>
   ><li>Det anslåede omkostningsbeløb i grundvalutaen konverteres til projektets omkostningsvaluta (konvertering 2). </li>
   ></ol>
   >Valutapræcision anvendes i begge trin for at få en planlagt omkostning (under fanen **Sporing**), der afviger en smule fra den anslåede omkostning (i visningen **Tidsfase** på fanen **Estimater**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Omprojektering af omkostninger på bladnodeopgaver

Arbejdsomkostninger på en bladnodeopgave kan ikke omprojekteres direkte under fanen **Sporing** på siden **Projekt**. Du kan dog bruge visningen **Indsatssporing** til at omprojektere den resterende indsats på en opgave. Derved genberegnes de resterende omkostninger for opgaven. Nedenfor følger en beskrivelse af, hvordan dette fungerer.

1. En projektleder kan omprojektere indsatsen på opgaver ved at opdatere standardværdien i feltet **Resterende indsats** med et nyt estimat af den resterende indsats på opgaven. Omprojektering medfører, at opgavens anslåede indsats ved fuldførelse (EAC), færdiggørelsesprocenten og den forventede omkostningsafvigelse for en opgave genberegnes. EAC, estimatet ved fuldførelse (ETC) og færdiggørelsesprocenten for hovedopgaverne genberegnes også og giver en ny projektion af indsatsafvigelsen.
2. På grundlag af den nye værdi for den resterende indsats på opgaven beregner systemet de resterende omkostninger i visningen **Omkostningssporing**. Hvis du vil beregne de resterende omkostninger på baggrund af den resterende indsats, beregner systemet først de gennemsnitlige omkostninger for en times indsats på opgaven som planlagte omkostninger eller en planlagt indsats. De planlagte omkostninger er summen af omkostningerne for alle ressourcetildelinger på opgaven. De gennemsnitlige omkostninger pr. time bruges til at beregne de resterende omkostninger for den nyligt anslåede resterende indsats på opgaven.
3. Omkostningen ved fuldførelse og procenten for omkostningsforbruget på bladnodeopgaven beregnes igen.
4. Værdien af omkostninger ved fuldførelse for hovedopgaverne genberegnes helt ned til rodnoden.

## <a name="reprojecting-costs-on-summary-tasks"></a>Omprojektering af omkostninger på hovedopgaver

Du kan omprojektere arbejdsomkostningerne på hovedopgaver eller beholderopgaver. Arbejdsomkostninger på en hovedprojektopgave kan dog ikke omprojekteres direkte under fanen **Sporing** på siden **Projekt**. På samme måde som ved bladnodeopgaver kan omprojektering af hoved- og beholderopgaver udføres ved hjælp af visningen **Indsatssporing**. I denne visning kan du omprojektere den resterende indsats på en hovedopgave, hvilket medfører en genberegning af de resterende omkostninger på hovedopgaven. Nedenfor følger en beskrivelse af, hvordan dette fungerer.

1. En projektleder kan omprojektere indsatsen på hovedopgaver ved at opdatere standardværdien for den resterende indsats med et nyt estimat på opgaven. Denne opdatering medfører, at hovedopgavens estimat ved fuldførelse (EAC), færdiggørelsesprocenten og den forventede omkostningsafvigelse for en opgave genberegnes. EAC, ETC og fremgangen i procenten for hovedopgaver genberegnes også og giver en ny projektion af afvigelsen i tidsforbruget.
2. På grundlag af den nye værdi for resterende indsats på hovedopgaven beregner systemet de resterende omkostninger i visningen **Omkostningssporing**. Hvis du vil beregne de resterende omkostninger på baggrund af den resterende indsats, beregner systemet først de gennemsnitlige omkostninger for en times indsats på hovedopgaven som planlagte omkostninger eller en planlagt indsats. De gennemsnitlige omkostninger pr. time bruges til at beregne omkostningerne for den nyligt anslåede resterende indsats på hovedopgaven.
3. Omkostningen ved fuldførelse og procenten for omkostningsforbruget på hovedopgaven beregnes igen.
4. Den nye omkostning ved fuldførelse fordeles nedad til de underordnede opgaver i samme forhold, som den oprindelige planlagte omkostning på opgaven blev fordelt.
5. Den nye værdi for omkostninger ved fuldførelse for hver af de enkelte opgaver nedad til bladnodeopgaver beregnes. På grundlag af denne værdi genberegnes de resterende omkostninger og procenten for omkostningsforbruget for de berørte underopgaver helt ned til bladnoderne på baggrund af værdien for omkostninger ved fuldførelse. Denne værdi medfører, at der laves en ny projektion for afvigelsen i omkostninger for opgaven. 


Feltet **Omkostningsydeevne** kan angives ud fra sporingsdataene. Når omkostningsafvigelsen for rodnoden i visningen **Omkostningssporing** er negativ, kan du angive dette felt til **Under budget**. Når omkostningsafvigelsen for rodnoden er positiv, kan du angive værdien til **Over budget**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
