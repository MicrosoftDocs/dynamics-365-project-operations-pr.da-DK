---
title: Projektskabeloner
description: Dette emne indeholder oplysninger om, hvordan du kan bruge projektskabeloner til hurtig opsætning af projekter.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148051"
---
# <a name="project-templates"></a>Projektskabeloner 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En projektskabelon er en foruddefineret struktur, der gør det nemt og hurtigt at starte et projekt. Du kan bruge en foruddefineret skabelon til at oprette et nyt projekt med et enkelt klik. Som i forbindelse med projekter skal du definere forudsætningerne for projektskabeloner. Du skal definere en projektkalender for de enkelte projektskabeloner, og roller og prislister skal være foruddefineret i organisationen, så der findes brugbare data til skabelonens komponenter.

En projektskabelon består af tre komponenter: en plan, projektestimater og medlemmer af projektteamet.

## <a name="schedule"></a>Planlæg

En tidsplan i en projektskabelon har samme sæt elementer som en tidsplan i et projekt. Du kan oprette et opgavehierarki, knytte roller til opgaver, definere planlægningsattributter og angive afhængigheder. En tidsplan i en projektskabelon understøtter også opgavetilstande for de enkelte opgaver. Den understøtter derfor planlægningsprogrammet. Du skal knytte en projektkalender til projektet. Når du opretter en arbejdsplan, er der ingen forskel mellem en projektskabelon og et projekt.

## <a name="project-estimates"></a>Projektestimater

Projektestimater i en projektskabelon fungerer på samme måde som projektestimater i et projekt. Kost- og salgspriserne trækkes dog fra de standardomkostnings- og prislister, der er defineret i parametrene.

## <a name="creating-a-project-from-a-template"></a>Oprettelse af et projekt på baggrund af en skabelon
 
Du kan oprette et projekt på baggrund af en projektskabelon på flere måder:

- Når du opretter et projekt fra tilbuddet, kan du vælge en projektskabelon i dialogboksen **Hurtig oprettelse: Projekt**

> ![Dialogboksen Hurtig oprettelse: Projekt](media/project-11.png)

- Når du opretter et projekt ved at vælge **Nyt projekt** vises siden **Projekt**, før posten gemmes. I feltet **Vælg en skabelon** skal du vælge en af de foruddefinerede projektskabeloner i organisationen.
- Brug **Opret projekt fra en skabelon** på siden **Skabelonobjekt**.

## <a name="copying-components-of-template-to-project"></a>Kopiere komponenter fra en skabelon til et projekt

Når du kopierer komponenterne i en projektskabelon til et projekt, kan der opstå nogle få tilsidesættelser, afhængigt af indstillingerne i projektet.

### <a name="copying-the-schedule"></a>Kopiere planen

Når du kopierer planen fra en projektskabelon, anvendes arbejdstimer fra projektets kalender til opgaveplanlægningen, hvis projektet har en anden projektkalender end skabelonen. Derved justeres planen, så den svarer til sikkerhedskopieringen af projektkalenderen. Den første opgave på planen tager projektets startdato, og planen for resten af hierarkiet opdateres baseret på den varighed og de afhængigheder, der er angivet i skabelonen. 

### <a name="copying-project-estimates"></a>Kopiere projektestimater 

Når du kopierer på tværs af projektestimatlinjer, opdateres prislisterne. Hvad angår listen over kostpriser, er disse opdateringer baseret på ejerskabsenheden for projektet. For salgsprislisten er de baseret på kunden. For projekter, der er knyttet til et salgsobjekt, bestemmes kost- og salgspriserne ud fra disse prislister.

### <a name="copying-a-project-team"></a>Kopiere et projektteam

Når et projektteam kopieres fra en projektskabelon til et projekt, kopieres standardressourcerne sammen med de færdigheder og kompetencer, der er defineret i skabelonen. Standardressourcetildelinger bevares også, som de var, i projektskabelonen. Navngivne ressourcer understøttes ikke i projektskabeloner.


[!INCLUDE[footer-include](../includes/footer-banner.md)]