---
title: Planlægge et projekt med et arbejdsopgavehierarki
description: Sådan planlægger du et projekt med et arbejdsopgavehierarki i Project Service
author: ruhercul
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
ms.openlocfilehash: 896f19746bde1ba6cf2acd6d558137f4271a5cd99424043053eefe128d3b4250
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996789"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Planlægge et projekt med et arbejdsopgavehierarki (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

En projektplan kommunikerer, hvad der skal udføres, hvilke ressourcer der skal udføre arbejdet og tidsrammen, som arbejdet skal udføres i. Projektplanen afspejler det arbejde, der er knyttet til levering af projektet til tiden. En af de første trin i den indledende fase af projektet er at komme med en projektplan. Hvis du vil oprette en projektplan, skal du oprette et arbejdsopgavehierarki.  
  
 Opret en projektstruktur med et arbejdsopgavehierarki, som hjælper dig med at:  
  
- Opdele arbejdet i overskuelige opgaver  
  
- Anslå den tid, det tager at fuldføre en opgave  
  
- Oprette opgaveafhængigheder og opgavevarighed  
  
- Bestemme de roller, der er nødvendige for at udføre hver opgave  
  
  Projektplanen i arbejdsopgavehierarkiet har et velkendt udseende, komplet med et interaktivt Gantt-diagram.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Oprette et arbejdsopgavehierarki til et projekt  
 Opret et arbejdsopgavehierarki for at repræsentere sekvensen af opgaver i et projekt. Arbejdsopgavehierarkiet indeholder opgaver, krav til hver enkelt opgave og oplysninger om indtægter og omkostninger. I din arbejdsopgavehierarki kan du tilføje::  
  
-   Rækkefølgen af opgaverne i et hierarki  
  
-   Andre opgaver, som eventuelt skal udføres, før en opgave kan startes.  
  
-   Startdato, sidste dato og varighed for en opgave  
  
-   Antallet timer, der kræves for en opgave  
  
-   Eventuelle påkrævede færdigheder og uddannelse hos arbejderne  
  
-   De arbejdere, der er tildelt til en opgave  
  
-   Anslået omsætning og omkostninger  
  
## <a name="task-types"></a>Opgavetyper  
Du skal bruge følgende typer opgaver, når du opretter dit arbejdsopgavehierarki:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Rodnoden til projekt** | Den øverste oversigtsopgave for projektet. Alle andre projektopgaver oprettes under den. Navnet på rodopgaven er navnet på projektet. Indsats, datoer og varighed af rodnoden er baseret på værdierne i hierarkiet under den. Du kan ikke redigere egenskaber for rodnode eller slette rodnoden. | 
| **Oversigts- eller beholderopgaver** | En oversigtsopgave er en opgave, som har underordnede opgaver. En hovedopgave indeholder ingen arbejdsindsats eller egne omkostninger. Dens arbejdsindsats og omkostninger er en pakke bestående af dens underopgaver. Du kan ændre navnet på en oversigtsopgave, men du kan ikke ændre indsats, datoer eller varighed, fordi de beregnes automatisk. Hvis du sletter en oversigtsopgave, slettes opgaven og alle dens underopgaver.|  
| **Bladnodeopgaver** | En bladnodeopgave repræsenterer det mest detaljerede arbejde på projektet. Den har en anslået indsats, en planlagt antal ressourcer, planlagte start- og slutdatoer og en varighed.|

  
## <a name="task-hierarchy"></a>Opgavehierarki  
 Du har følgende valgmuligheder, når du opretter et opgavehierarki:  
  
- **Tilføj opgave**.   Du kan tilføje en opgave på en placering, du vælger i opgavehierarkiet. Hvis du ikke vælger en placering, vises den nye opgave i slutningen.  
  
- **Indryk opgave**.   Indryk en opgave for at gøre den til en underordnet til opgaven direkte over den.  
  
- **Ryk opgave ud**.   Ryk en opgave ud, så den ikke længere er en underopgave til dens oprindelige overordnede opgave.  
  
- **Flyt op og Flyt**.   Flyt opgaver op eller ned i hierarkiet med dens overordnede opgave. Hvis du flytter en opgave op eller ned, har det ingen indflydelse på indsats, omkostninger, datoer eller varighed.  
  
## <a name="task-attributes"></a>Opgaveattributter  
 En opgaves navn beskriver det arbejde, der skal udføres. Du kan bruge forskellige opgaveattributter til at beskrive tidsplan og krav til arbejdskraft til opgaven.  
  
### <a name="schedule-attributes"></a>Planlæg attributter

 - Tildel værdier til **Indsatstimer**, **Antal ressourcer**, **Startdato**, **Slutdato** og **Varighed** til at bestemme tidspunktet for opgaven. 
 - **Indsats** er et skøn over de timer, det tager at udføre opgaven.
 - **Antal ressourcer** er et skøn, der giver projektlederen til opgave til at komme med den bedste mulige tidsplan. 
 - **Varighed** (i dage) angiver antallet af arbejdsdage, det tager at fuldføre opgaven.  
  
### <a name="staffing-attributes"></a>Bemandingsattributter

 - **Rolle**, **ressourceafdeling**, **antal ressourcer,** og **ressourcer** beskriver behov for personale til opgaven. 
 - **Rolle** beskriver den type ressource, der er nødvendige for at udføre opgaven. 
 - **Ressourceafdeling** angiver den afdeling, der skal bemandes ressourcer til denne opgave. Dette påvirker også omkostninger og salgsvurdering af opgaven, da dette er taget i betragtning ved fastsættelsen af enhedssalgsprisen for ressourcen. 
 - **Ressourcer** indeholder en generisk ressource eller en navngivet ressource, når der findes en.  
  
## <a name="task-dependencies"></a>Opgaveafhængigheder  
 Du kan oprette relationer mellem foregående opgaver mellem en eller flere opgaver i arbejdsopgavehierarkiet. Du kan angive en eller flere værdier for feltet foregående opgaver for at angive de opgaver, som det vil være afhængige af. Når du tildeler en foregående værdi til en opgave, kan opgaven kun starte, når du har fuldført de foregående opgaver. Angivelse af denne afhængighed på en opgave medfører genberegning af den planlagte startdato for opgaven som seneste slutningen af alle de foregående opgaver. Indvirkningen af relateret til foregående på en tidsplan er ikke begrænset af opgavetilstanden, der er defineret på opgaven.  
  
## <a name="task-mode"></a>Opgavetilstand  
 Opgavetilstand er en af de vigtige faktorer, der bestemmerplanlægning af bladnodeopgaver. Der er to tilstande for opgave for hver opgave: automatisk planlægning og manuel planlægning.  
  
-   **Automatisk planlægning**.   Når du vælger opgavetilstanden Planlagt automatisk, bruger planlægningsprogrammet planlægningsreglerne på følgende opgaveattributter til at bestemme planlægningen for opgaven:  
  
    -   Foregående  
  
    -   Indsats  
  
    -   Antal ressourcer  
  
    -   Start- og slutdatoer  
  
-   **Planlægningsregler**.   Startdatoen for en bladnodeopgave, der ikke har foregående er som standard projektets planlagte startdato. Varigheden af en bladnodeopgave beregnes altid som antallet af arbejdsdage mellem dets start- og slutdatoer. Når en opgave er planlagt automatisk, vil planlægningsprogrammet følge nedenstående regler:  
  
    -   Start- og slutdatoer for en opgave skal altid være arbejdsdage i projektets planlægningskalender  
  
    -   Startdatoen for en opgave, der har foregående opgaver, er som standard den seneste slutdato af sine forgængere  
  
    -   Indsats = antal personer * varighed * timer i en standardarbejdsdag i projektkalenderen  
  
-   **Manuel planlægning**.   I nogle tilfælde kan du afvige fra disse regler. I disse tilfælde kan du angive, at tilstanden for opgaven skal være manuelt planlagt. Dette stopper planlægningsprogrammet fra at beregne værdier for andre planlægningsattributter. Angivelse af foregående opgaver har altid indflydelse på startdatoen for den afhængige opgave.  
  
## <a name="create-a-work-breakdown-structure"></a>Oprette et arbejdsopgavehierarki  
  
1.  Gå til **Project Service > Projekter**.  
  
2.  Klik på det projekt, som du vil arbejde på.  
  
3.  Vælg pil ned ud for projektnavnet på linjen øverst på skærmen, og klik derefter på Arbejdsopgavehierarki.  
  
4.  Hvis du vil tilføje en opgave, skal du klikke på **Tilføj opgave**. Udfyld felterne for opgaven, og klik derefter på **Gem**.  
  
5.  Fortsæt med at tilføje opgaver, indtil arbejdsopgavehierarkiet er fuldført. Når du opretter dit arbejdsopgavehierarki, kan du gøre følgende for at organisere dine opgaver:  
  
    -   Marker en opgave, og klik på **Indryk** for at flytte den under en anden opgave, eller klik på Ryk ud for at flytte den ud af et niveau.  
  
    -   Marker en opgave, og klik på **Flyt op** eller **Flyt ned** for at flytte den op eller ned på listen.  
  
    -   Klik på **Skjul Gantt** for at skjule Gantt-diagrammet, og klik på **Vis Gantt** for at vise det igen.  
  
    -   Vælg en anden tidsperiode for Gantt-diagrammet i **Tidsskala**.  
  
6.  Klik for at tilføje de roller, du har angivet i dit arbejdsopgavehierarki til projektets teammedlemmer, klik på **Opret projektteam**.  
  
7.  Klik på **Gem** i nederste højre hjørne af skærmen, når du er færdig med at foretage ændringer.  
  
### <a name="see-also"></a>Se også  
 [Vejledning til projektledere](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]