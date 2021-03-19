---
title: Opret et arbejdsopgavehierarki
description: I dette emne forklares det, hvordan du kan oprette et arbejdsopgavehierarki (WBS), inklusive basiskontrolelementerne i den nye planlægningsgrænseflade.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 695bbc2ae1ba1e762472b5f5fa853c89017d2f52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287006"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Opret et arbejdsopgavehierarki (WBS)

En projektplan kommunikerer, hvad der skal udføres, hvilke ressourcer der skal udføre arbejdet, og tidsrammen, inden for hvilken arbejdet skal være afsluttet. Planen afspejler det arbejde, der er knyttet til levering af projektet til tiden. I Dynamics 365 Project Operations opretter du en projektplan ved at:

  - Opdeling af arbejdet i overskuelige opgaver.
  - Estimering af den tid, der kræves til at udføre de enkelte opgaver.
  - Angivelse af opgaveafhængigheder.
  - Angivelse af opgavers varighed.
  - Estimering af de generiske ressourcer, der skal udføre opgaverne. 

Projektplanen oprettes under fanen **Tidsplan** på siden **Projekt**.

## <a name="tasks"></a>Opgaver

Det første trin i oprettelsen af en projektplan er at bryde arbejdet op i dele, der kan administreres. Planen i Project Operations understøtter følgende funktioner:

- Oversigts- eller beholderopgaver
- Bladnodeopgaver

### <a name="summary-tasks"></a>Hovedopgaver

Hovedopgaver kan bruges til at gemme andre hovedopgaver eller bladnodeopgaver. De har ikke deres egen arbejdsindsats eller egne omkostninger. Deres arbejdsindsats og omkostninger er i stedet en akkumulering af arbejdsindsats og omkostninger i forbindelse med deres beholderopgaver. Hovedopgavens startdato er startdatoen for beholderopgaver, og slutdatoen er slutdatoen for beholderopgaver. Navnet på en hovedopgave kan redigeres, men planlægningens egenskaber, herunder indsats, datoer og varighed, kan ikke redigeres. Hvis du sletter en hovedopgave, sletter du også alle dens beholderopgaver.

### <a name="leaf-node-tasks"></a>Bladnodeopgaver

Bladnodeopgaver repræsenterer det mest detaljerede arbejde på projektet. De har en anslået indsats, anslåede ressourcer, planlagt start- og slutdato samt en varighed.

## <a name="create-a-task-hierarchy"></a>Opret et opgavehierarki

### <a name="add-a-task"></a>Tilføje en opgave

For at tilføje en eller flere opgaver skal du fuldføre følgende fremgangsmåde.

1. Gå til **Projekter**, og vælg og åbn den projektpost, som du vil oprette en tidsplan for. 
2. Vælg fanen **Opgaver**. 
3. Vælg **Tilføj ny opgave**, angiv et navn til opgaven, og tryk derefter på Enter.
2. Angiv et andet opgavenavn, og tryk på Enter igen, indtil du har en komplet liste over opgaver.

### <a name="manage-hierarchy-of-a-task"></a>Administrer en opgaves hierarki

Når en opgave rykkes ind, bliver den et underordnet element i den opgave, der er direkte over den. Opgavens tidsplans-id genberegnes derefter, så det er baseret på tidsplans-id'et for den nye overordnede opgave og følger skemaet til dispositionsnummerering. Den overordnede opgave er nu en hovedopgave. Den er derfor en akkumulering af dens underopgaver. Når en opgave forfremmes, er den ikke længere underordnet den opgave, der var dens overordnede opgave. Tidsplans-id'et genberegnes derefter, så det afspejler opgavens opdaterede dybde og placering i hierarkiet. Indsatsen, omkostningerne og datoerne for den forrige overordnede opgave genberegnes, så de ikke inkluderer denne opgave.

For at tilføje en indrykket opgave eller forfremme en opgave skal du fuldføre følgende fremgangsmåde.

1. På siden **Projekt** skal du på fanen **Opgaver** under **Hovedopgaver** vælge de tre lodrette punkter ud for opgavenavnet og derefter vælge **Opret underopgave**. 
2. Markér den opgave, der skal indrykkes eller forfremmes. Hvis du vil markere mere end én opgave, skal du vælge en opgave, trykke på og holde CTRL nede og derefter vælge yderligere opgaver.
2. Vælg **Indryk** eller **Forfrem underopgave** for at flytte opgaver under eller væk fra hovedopgaver.

### <a name="move-tasks-up-and-down"></a>Flyt opgaver op og ned

Opgaver kan flyttes til et hvilket som helst niveau i arbejdsopgavehierarki på to måder:

- Markér endnu en opgave, og træk den til den ønskede placering.
- Markér en eller flere opgaver, højreklik, og vælg **Klip**, vælg destinationscelle i planen, og højreklik derefter, og vælg **Sæt ind**.

## <a name="task-attributes"></a>Opgaveattributter

En opgaves navn beskriver det arbejde, der skal udføres. I Project Operations beskriver de attributter, der er knyttet til en opgave, opgaveplanen og kravene til medarbejderne.

## <a name="schedule-attributes"></a>Planlæg attributter

Attributterne **Indsats**, **Startdato**, **Slutdato** og **Varighed** definerer opgavens tidsplan.

I tabellen nedenfor vises yderligere planlægningsattributter.

| **Endeligt vist navn** | **Endelig beskrivelse** |
| --- | --- |
| Fuldført indsats (timer) | Udført arbejde på opgaven i timer. |
| Varighed | Viser opgavens varighed i dage. |
| Samlet indsats | Opgavens samlede arbejde i timer. |
| Afslut | Slutdato og -klokkeslæt. |
| % fuldført | Procentdelen af opgaven, der er fuldført. |
| Projektbucket | Opgaveområdet kan grupperes efter bucket, så hver bucket har sin egen kolonne. |
| Resterende indsats (timer) | Det resterende arbejde på opgaven i timer. |
| Start | Startdato og -klokkeslæt. |
| Navn | Navnet på opgaven. |
| Id | Opgavens ID i arbejdsopgavehierarkiet. |

Som en administrator kan du definere brugerdefinerede felter i opgaveobjektet. Felterne kan dog ikke vises i planlægningsgitteret. Hvis du vil se de brugerdefinerede felter, skal du tilføje dem til siden med detaljer for **Projektopgaven**.

## <a name="staffing-attributes"></a>Bemandingsattributter

Der kan opnås adgang til medarbejderattributter via feltet **Ressourcer** i tidsplanen. Du kan enten søge efter en eksisterende ressource eller vælge **Opret** og i ruden **Hurtig oprettelse** tilføje et medlem af projektteamet som en ny ressource.

Felterne **Rolle**, **Ressourceenhed** og **Navn på stilling** bruges til at beskrive personalekravene for opgaven. Disse medarbejderattributter sammen med opgaveplanlægning bruges til at finde tilgængelige ressourcer til udførelse af denne opgave.

   - **Rolle**: Angiv den type ressource, der kræves til udførelse af opgaven.
   - **Ressourceenhed**: Angiv den enhed, som ressourcer til opgaven skal tildeles fra. Denne attribut påvirker omkostnings- og salgsestimatet for opgaven, hvis kostprisen og fakturasatsen for ressourcen er angivet på baggrund af reressourceenhederne.
   - **Stillingsnavn**: Angiv et navn til den generiske ressource, der fungerer som pladsholder for den ressource, der til sidst udfører arbejdet.

Feltet **Ressourcer** indeholder stillingsnavnet på den generiske ressource eller den navngivne ressource, når der findes en ressource.

Feltet **Kategori** indeholder de værdier, der angiver en bredere arbejdstype, som opgaven kan grupperes i. Dette felt påvirker ikke planlægning eller bemanding. Feltet bruges i stedet kun til rapportering.

## <a name="task-dependencies"></a>Opgaveafhængigheder

Du kan bruge planlægningen i Project Operations til at oprette foregående relationer mellem opgaver. Feltet **Foregående aktivitet** bruger en eller flere værdier til at angive, hvilke opgaver en opgave afhænger af. Når du tildeler en foregående værdi til en opgave, kan opgaven kun starte, når du har fuldført de foregående opgaver. På grund af afhængigheden nulstilles opgavens planlagte startdato til den dato, hvor de foregående opgaver fuldføres.

Opgavetilstanden påvirker ikke de opdateringer, der er foretaget af start- og slutdatoerne for foregående/afhængige opgaver.

## <a name="accessibility-and-keyboard-shortcuts"></a>Hjælp til handicappede og tastaturgenveje

Gitteret **Planlægning** er fuldt tilgængeligt og kan bruges sammen med skærmlæsere, f.eks. Oplæser, JAWS eller NVDA. Du kan flytte gennem gitterområdet ved hjælp af piletasterne (som i Microsoft Excel), du kan bruge tabulatortasten til at gennemblade de interaktive brugergrænsefladeelementer, og du kan bruge pil ned-tasten, tasten ENTER eller mellemrumstasten til at åbne og aktivere rullemenuerne.


[!INCLUDE[footer-include](../includes/footer-banner.md)]