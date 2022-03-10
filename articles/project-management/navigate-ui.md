---
title: Navigation i brugergrænsefladen
description: Dette emne indeholder oplysninger om projektstyring i Dynamics 365 Project-operationer.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 97483a53163edbbe6dfe383d6a6a60183a17e6e9df9ec3c47c9f33aef88aea3e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989139"
---
# <a name="navigating-the-user-interface"></a>Navigation i brugergrænsefladen

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

## <a name="overview"></a>Oversigt

Den primære projektformular er opdelt i flere faner. De enkelte faner repræsenterer et andet detaljeringsniveau i projektet.

- **Oversigt**: Angiver en beskrivelse af projektet og sammenfatter både projektets planlagte og faktiske præstation.

    ![Fanen Oversigt og felter.](media/navigation7.png)

- **Opgaver**: Indeholder detaljer om arbejdsopgavehierarkiet, der repræsenteres af en gittervisning, en kortvisning og et Gantt-diagram.

    ![Fanen Opgave og felter.](media/navigation8.png)

- **Team**: Indeholder oplysninger om projektdeltagere. De enkelte teammedlemmers tildelte indsats opsummeres også i denne visning.

    ![Fanen Team og felter.](media/navigation9.png)

- **Ressourcetildelinger**: Indeholder en tidsfaseinddelt visning af indsatsen for hver ressource på et projekt.

    ![Fanen Ressourcetildelinger og felter.](media/navigation10.png)

- **Ressourceafstemning**: Angiver en tidsfaseinddelt visning af forskellene mellem tildelingerne af hver navngivet ressource og deres reservationer.

    ![Fanen Ressourceafstemning og felter.](media/navigation11.png)

- **Estimater**: Angiver en tidsfaseinddelt visning af omkostnings- og salgsestimater for et projekt.

    ![Fanen Estimater og felter.](media/navigation12.png)

- **Sporing**: Indeholder en visning, der viser opgavers fremgang i arbejdsopgavehierarkiet i forbindelse med indsats, omkostninger og salg.

    ![Fanen Sporing og felter.](media/navigation13.png)

- **Salg**: Indeholder dybdegående links til tilbud og kontrakter, der er knyttet til projektet.

- **Udgiftsestimater**: Indeholder et gitter, der definerer projektudgifter baseret på organisationens omkostningskategorier.

    ![Fanen Udgiftsestimater og felter.](media/navigation14.png)

## <a name="grid-controls"></a>Gitterkontrolelementer

Nedenstående er en kort oversigt over de typiske kontrolelementer, der findes under de forskellige projektplanlægningsfaner.

### <a name="refresh"></a>Opdater

**Opdatering**: Henter de nyeste data fra serveren, hvis der er foretaget ændringer, efter at gitteret blev indlæst.

![Knappen Opdater.](media/navigation7.png)

### <a name="group-by"></a>Gruppér efter

**Grupper efter**: Opdaterer grupperingen af rækkerne i gitteret for at afspejle enten ressourcer, roller eller kategorier, afhængigt af brugerens behov.

![Gruppér ved hjælp af knap.](media/navigation6.png)

### <a name="previousnext"></a>Forrige/næste

**Forrige**/**næste**: Opdater de synlige tidsperioder på tidsfaseinddelte gitre.

![Knapperne Forrige og Næste.](media/navigation2.png)

### <a name="timescale"></a>Tidsskala

**Tidsskala**: Rediger sammenlægningen af tidsfaseinddelte data mellem dage, uger, måneder og år.

![Knappen Tidsskala.](media/navigation3.png)

### <a name="expand"></a>Udvid

**Udvid**: Gengiv det synlige gitter til fuldskærmsvisning for at kunne se flere roller.

![Knappen Udvid.](media/navigation4.png)

### <a name="time-phase-by"></a>Tidsfase efter

**Tidsfase efter**: Opdater grupperingen af rækkerne i gitteret for at afspejle omkostningsestimater for salgsestimater. Dette kontrolelement finder også anvendelse på det estimerede script og sporingsgitteret.

![Tidsfase ved hjælp af knap.](media/navigation0.png)

### <a name="add-column"></a>Tilføj kolonne

**Tilføj kolonne**: Giver brugeren mulighed for at definere de synlige kolonner i gitteret. Det er kun de foruddefinerede kolonner, der kan tilføjes til gitrene i formularen **Projektplanlægning**.

![Knappen Tilføj kolonne.](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]