---
title: Navigation i brugergrænsefladen
description: Dette emne indeholder oplysninger om projektstyring i Dynamics 365 Project-operationer.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127511"
---
# <a name="navigating-the-user-interface"></a>Navigation i brugergrænsefladen

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

## <a name="overview"></a>Oversigt

Den primære projektformular er opdelt i flere faner. De enkelte faner repræsenterer et andet detaljeringsniveau i projektet.

- **Oversigt**: Angiver en beskrivelse af projektet og sammenfatter både projektets planlagte og faktiske præstation.

    ![Oversigtsfane og felter](media/navigation7.png)

- **Opgaver**: Indeholder detaljer om arbejdsopgavehierarkiet, der repræsenteres af en gittervisning, en kortvisning og et Gantt-diagram.

    ![Opgavefane og felter](media/navigation8.png)

- **Team**: Indeholder oplysninger om projektdeltagere. De enkelte teammedlemmers tildelte indsats opsummeres også i denne visning.

    ![Teamfane og felter](media/navigation9.png)

- **Ressourcetildelinger**: Indeholder en tidsfaseinddelt visning af indsatsen for hver ressource på et projekt.

    ![Fanen ressourcetildelinger og felter](media/navigation10.png)

- **Ressourceafstemning**: Angiver en tidsfaseinddelt visning af forskellene mellem tildelingerne af hver navngivet ressource og deres reservationer.

    ![Fanen ressourceafstemning og felter](media/navigation11.png)

- **Estimater**: Angiver en tidsfaseinddelt visning af omkostnings- og salgsestimater for et projekt.

    ![Fane for estimater og felter](media/navigation12.png)

- **Sporing**: Indeholder en visning, der viser opgavers fremgang i arbejdsopgavehierarkiet i forbindelse med indsats, omkostninger og salg.

    ![Sporingsfane og felter](media/navigation13.png)

- **Salg**: Indeholder dybdegående links til tilbud og kontrakter, der er knyttet til projektet.

- **Udgiftsestimater**: Indeholder et gitter, der definerer projektudgifter baseret på organisationens omkostningskategorier.

    ![Fane for udgiftsestimater og felter](media/navigation14.png)

## <a name="grid-controls"></a>Gitterkontrolelementer

Nedenstående er en kort oversigt over de typiske kontrolelementer, der findes under de forskellige projektplanlægningsfaner.

### <a name="refresh"></a>Opdater

**Opdatering**: Henter de nyeste data fra serveren, hvis der er foretaget ændringer, efter at gitteret blev indlæst.

![Knappen Opdater](media/navigation7.png)

### <a name="group-by"></a>Gruppér efter

**Grupper efter**: Opdaterer grupperingen af rækkerne i gitteret for at afspejle enten ressourcer, roller eller kategorier, afhængigt af brugerens behov.

![Grupper ved hjælp af knap](media/navigation6.png)

### <a name="previousnext"></a>Forrige/næste

**Forrige**/**næste**: Opdater de synlige tidsperioder på tidsfaseinddelte gitre.

![Knapperne forrige og næste](media/navigation2.png)

### <a name="timescale"></a>Tidsskala

**Tidsskala**: Rediger sammenlægningen af tidsfaseinddelte data mellem dage, uger, måneder og år.

![Tidsskalaknap](media/navigation3.png)

### <a name="expand"></a>Udvid

**Udvid**: Gengiv det synlige gitter til fuldskærmsvisning for at kunne se flere roller.

![knappen Udvid](media/navigation4.png)

### <a name="time-phase-by"></a>Tidsfase efter

**Tidsfase efter**: Opdater grupperingen af rækkerne i gitteret for at afspejle omkostningsestimater for salgsestimater. Dette kontrolelement finder også anvendelse på det estimerede script og sporingsgitteret.

![Knap til tidsfase efter](media/navigation0.png)

### <a name="add-column"></a>Tilføj kolonne

**Tilføj kolonne**: Giver brugeren mulighed for at definere de synlige kolonner i gitteret. Det er kun de foruddefinerede kolonner, der kan tilføjes til gitrene i formularen **Projektplanlægning**.

![Tilføj kolonneknap](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]