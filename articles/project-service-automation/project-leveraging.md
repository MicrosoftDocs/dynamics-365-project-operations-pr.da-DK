---
title: Salgsestimater og projekter
description: Dette emne indeholder oplysninger om, hvordan du kan udnytte planlægning og estimater i salgsprocessen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750523"
---
# <a name="sales-estimates-and-projects"></a>Salgsestimater og projekter

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Under salgsprocessen kan du oprette salgsestimater ved at knytte et projekt til et salgstilbud. På denne måde kan der opstå deterministisk estimering under salgsprocessen for at drage nytte af funktionerne projektplanlægning og estimater. Hvis salget går igennem, kan den planlægning, der blev brugt til salgsestimater, bruges som udgangspunkt for yderligere forbedringer i projektplanen.

## <a name="linking-a-project-to-a-quote-line"></a>Sammenkædning af et projekt med en tilbudslinje

Når du opretter en projektbaseret tilbudslinje, kan du oprette et nyt projekt eller tilknytte et eksisterende projekt på siden **Tilbudslinje**. 

> ![Tilbudslinjeformular](media/project-8.png)
 
Når du opretter et nyt projekt ud fra oplysningerne i tilbudslinjen, kan du drage fordel af projektskabeloner. Projektskabeloner er modelprojekter, der repræsenterer standardprojektplaner og økonomiske estimater, som er typiske i en organisation. De kan også repræsentere kopier af projektplaner og estimater fra tidligere projekter.

> ![Tilbudslinjedetaljer](media/project-9.png)
  
Når du opretter projektet fra tilbuddet, knyttes det automatisk til tilbudslinjen.

## <a name="components-of-estimates-in-a-project"></a>Komponenter i estimater i et projekt

En tidsplan giver dig mulighed for at opdele arbejdet i opgaver, vedligeholde et opgavehierarki, finde ud af, hvilke ressourcer der kræves for at udføre en opgave, og lave et skøn over den indsats, der kræves for at udføre en opgave.

Du kan definere en arbejdsindsats og planlægge estimater ved hjælp af felterne på fanen **Tidsplan** på siden **Projekt**. Da der er knyttet en prisliste til projektet, beregnes de økonomiske estimater ved hjælp af kost- og salgspriser, der er defineret i prislisten.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Import af estimater fra et projekt til et tilbud

Når du har defineret projektestimater, kan du importere dem til tilbudslinjen. På siden **Tilbudslinjedetaljer** skal du vælge **Import fra estimater** på båndet for at opsummere projektestimater efter transaktionstype, rolle eller opgaveniveau.
