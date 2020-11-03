---
title: Projektplaner
description: Dette emne indeholder oplysninger om, hvordan du opretter en tidsplan.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074207"
---
# <a name="project-schedules"></a>Projektplaner 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En projektplan kommunikerer, hvad der skal udføres, hvilke ressourcer der skal udføre arbejdet, og tidsrammen, som arbejdet skal udføres i. Projektplanen afspejler det arbejde, der er knyttet til levering af projektet til tiden. I Dynamics 365 Project Service Automation kan du oprette en projektplan ved at opdele arbejdet i opgaver, der kan administreres, vurdere den tid, det tager at udføre de enkelte opgaver, og angive opgaveafhængigheder og opgavevarigheder samt vurdere de standardressourcer, der skal udføre opgaverne. Projektplanen oprettes under fanen **Tidsplan** på projektsiden.
 
## <a name="tasks"></a>Opgaver

Det første trin i oprettelsen af en projektplan er at bryde arbejdet op i dele, der kan administreres. Planen i PSA understøtter følgende funktioner:

- Rodnoden til projekt
- Oversigts- eller beholderopgaver
- Bladnodeopgaver

### <a name="project-root-node"></a>Rodnoden til projekt

Projektets rodnode er hovedopgaven på øverste niveau for projektet. Alle andre projektopgaver oprettes under den. Navnet på rodnoden angives altid til navnet på projektet. Indsats, datoer og varighed af rodnoden opsummeres på grundlag af værdierne i hierarkiet under den. Du kan ikke redigere egenskaberne for rodnoden. Du kan heller ikke slette rodnoden.

### <a name="summary-or-container-tasks"></a>Oversigts- eller beholderopgaver 

Hovedopgaver har underopgaver eller beholderopgaver under sig. De har ikke deres egen arbejdsindsats eller egne omkostninger. Deres arbejdsindsats og omkostninger er i stedet en akkumulering af arbejdsindsats og omkostninger i forbindelse med deres beholderopgaver. Hovedopgavens startdato er startdatoen for beholderopgaver, og slutdatoen er slutdatoen for beholderopgaver. Navnet på en hovedopgave kan redigeres, men planlægningens egenskaber (tidsforbrug, datoer og varighed) kan ikke redigeres. Hvis du sletter en hovedopgave, sletter du også alle dens beholderopgaver.

### <a name="leaf-node-tasks"></a>Bladnodeopgaver

Bladnodeopgaver repræsenterer det mest detaljerede arbejde på projektet. De har en anslået indsats, anslåede ressourcer, planlagt start- og slutdato samt en varighed.
 
## <a name="creating-a-task-hierarchy"></a>Oprettelse af et opgavehierarki

Du kan oprette et arbejdshierarki ved brug af følgende valgmuligheder:

- Knappen **Tilføj opgave**
- Knappen **Ryk opgave ind**
- Knappen **Ryk opgave ud**
- Knapperne **Flyt op** og **Flyt ned**
- Hjælp til handicappede og tastaturgenveje

### <a name="add-task"></a>Tilføj opgave

Knappen **Tilføj opgave** giver dig mulighed for at oprette en ny opgave i hierarkiet. Hvis du ikke vælger en placering, indsættes opgave til sidst. 

Der tildeles et tidsplans-id til alle opgaver. Tidsplans-id'et repræsenterer opgavens dybde og placering i hierarkiet. Det bruger dispositionsnummerering. I forbindelse med opgaver på det første niveau under projektets rodnode bruges et nummereringsskema med 1, 2, 3 osv. I forbindelse med opgaver under det første niveau bruges et nummereringsskema med 1.1, 1.2, 1.3 osv.

### <a name="indent-task"></a>Ryk opgave ind.

Når en opgave rykkes ind, bliver den et underordnet element i den opgave, der er direkte over den. Opgavens tidsplans-id genberegnes derefter, så det er baseret på tidsplans-id'et for den nye overordnede opgave og følger skemaet til dispositionsnummerering. Den overordnede opgave er nu en hovedopgave eller en beholderopgave. Den er derfor en akkumulering af dens underopgaver.

### <a name="outdent-task"></a>Ryk opgave ud. 

Når en opgave rykkes ud, er den ikke længere underordnet i forbindelse med den opgave, der var dens overordnede opgave. Tidsplans-id'et genberegnes derefter, så det afspejler opgavens opdaterede dybde og placering i hierarkiet. Indsatsen, omkostningerne og datoerne for den forrige overordnede opgave genberegnes, så de ikke inkluderer denne opgave.

### <a name="move-up-and-move-down"></a>Flyt op og Flyt ned. 

Knapperne **Flyt op** og **Flyt ned** ændrer placeringen af en opgave i dens overordnede hierarki. Ændringer af denne type påvirker ikke opgavens indsats, omkostninger, datoer eller varighed. Det er kun opgavens tidsplans-id, der påvirkes. Tidsplans-id'et genberegnes, så det afspejler opgavens nye placering i den overordnede opgaves liste over underordnede opgaver.

### <a name="accessibility-and-keyboard-shortcuts"></a>Hjælp til handicappede og tastaturgenveje

Gitteret **Planlægning** er fuldt tilgængeligt og kan bruges sammen med skærmlæsere, f.eks. Oplæser, JAWS eller NVDA. Du kan flytte gennem gitterområdet ved hjælp af piletasterne (som i Microsoft Excel), du kan bruge tabulatortasten til at gennemblade de interaktive brugergrænsefladeelementer, og du kan bruge pil ned-tasten, tasten ENTER eller mellemrumstasten til at vælge og aktivere rullemenuerne. Kolonneoverskrifterne er også interaktive. Du kan skjule og få vist kolonner, bruge tabulatortasten og piletasterne til at bevæge dig gennem kolonneoverskrifterne og bruge handlingsknapperne på værktøjslinjen. Du kan desuden bruge følgende tastaturgenveje:

- **Opdater** : ALT + SKIFT + F5
- **Tilføj** : Alt + SHIFT + Insert
- **Slet** : ALT + SHIFT + Delete
- **Flyt op/ned** : ALT + SHIFT + pil op/ned
- **Indrykning/udrykning** : ALT_SHIFT + venstre/højre pil
- **Udvid/skjul hierarkier** : ALT + SHIFT + plus/minus-taster

## <a name="task-attributes"></a>Opgaveattributter

En opgaves navn beskriver det arbejde, der skal udføres. I PSA er de attributter, der er knyttet til en opgave, en beskrivelse af opgaveplanen og kravene til personaleansættelse.

> ![Opgaveattributter](media/project-2.png)
 
### <a name="schedule-attributes"></a>Planlæg attributter

Attributterne **Indsats** , **Startdato** , **Slutdato** og **Varighed** definerer opgavens tidsplan.

Yderligere planlægningsattributter omfatter:

- **Tidsforbrug** : Angiv et estimat for de timer, der kræves for at fuldføre opgaven. 
- **Varighed** : Angiv det antal arbejdsdage, der skal bruges for at fuldføre opgaven.
- **Tidsplans-id** : Dette automatisk genererede id bruges til at sortere opgaver i hierarkiet. Afhængigheder mellem opgaverne styrer den faktiske rækkefølge, hvori opgaverne udføres.
 
### <a name="staffing-attributes"></a>Bemandingsattributter

Der kan opnås adgang til medarbejderattributter via feltet **Ressourcer** i tidsplanen. Du kan enten søge efter en eksisterende ressource eller klikke på **Opret** og i ruden **Hurtig oprettelse** tilføje et medlem af projektteamet som en ny ressource.

Felterne **Rolle** , **Ressourceenhed** og **Navn på stilling** bruges til at beskrive personalekravene for opgaven. Disse medarbejderattributter sammen med opgaveplanlægning bruges til at finde tilgængelige ressourcer til udførelse af denne opgave.

**Rolle** – Angiv den type ressource, der kræves til udførelse af opgaven.

**Ressourceenhed** – Angiv den enhed, som ressourcer til opgaven skal tildeles fra. Denne attribut påvirker omkostnings- og salgsestimatet for opgaven, hvis kostprisen og fakturasatsen for ressourcen er angivet på baggrund af reressourceenhederne.

**Stillingsnavn** – Angiv et fuldt navn til den generiske ressource, der fungerer som pladsholder for den ressource, der til sidst udfører arbejdet.

Feltet **Ressourcer** indeholder stillingsnavnet på den generiske ressource eller den navngivne ressource, når der findes en ressource.

Feltet **Kategori** indeholder de værdier, der angiver en bredere arbejdstype, som opgaven kan grupperes i. Dette felt påvirker ikke planlægning eller bemanding. Det bruges kun til rapportering.

### <a name="task-dependencies"></a>Opgaveafhængigheder 

Du kan bruge planlægningen i PSA til at oprette foregående relationer mellem opgaver. Feltet **Foregående aktivitet** under **Opgaver** bruger en eller flere værdier til at angive, hvilke opgaver en opgave afhænger af. Når du tildeler en foregående værdi til en opgave, kan opgaven kun starte, når du har fuldført de foregående opgaver. På grund af afhængigheden nulstilles opgavens planlagte startdato til den dato, hvor de foregående opgaver fuldføres.

Opgavetilstanden påvirker ikke de opdateringer, der er foretaget af start- og slutdatoerne for foregående/afhængige opgaver.

## <a name="task-mode"></a>Opgavetilstand 

Opgavetilstanden bestemmer planlægningen af bladnodeopgaver. PSA understøtter to tilstande for opgaver for hver opgave: automatisk planlægning og manuel planlægning.

### <a name="auto-scheduling"></a>Automatisk planlægning 
 
Når du vælger opgavetilstanden **Planlagt automatisk** for en opgave, bruger planlægningsprogrammet planlægningsreglerne på opgaveattributterne for at bestemme planlægningen for opgaven:

#### <a name="scheduling-rules"></a>Planlægningsregler

Der gælder som standard, at hvis en bladnodeopgave ikke har foregående opgaver, er dens startdato angivet til projektets planlagte startdato. Varigheden af en bladnodeopgave beregnes altid som antallet af arbejdsdage mellem dets start- og slutdatoer. Når en opgave er planlagt automatisk, vil planlægningsprogrammet følge disse regler:

- Start- og slutdatoen for opgaven skal være arbejdsdage i henhold til projektets planlægningskalender. 
- Startdatoen for en opgave, der har foregående opgaver, er automatisk angivet til den seneste slutdato for sine forgængere.
- Indsatsen beregnes ved hjælp af denne formel: antal personer × varighed × timer på en normal arbejdsdag i projektkalenderen.

### <a name="manual-scheduling"></a>Manuel planlægning

Hvis reglerne for automatisk planlægning ikke opfylder dine krav, kan du indstille opgavetilstanden for opgaven til **Manuelt planlagt**. Denne indstilling stopper planlægningsprogrammet i at beregne værdierne for andre planlægningsattributter. Uanset opgavetilstand kan du altid påvirke den afhængige opgaves startdato, hvis du angiver de foregående opgaver for opgaverne.
