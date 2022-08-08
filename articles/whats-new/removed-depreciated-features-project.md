---
title: Fjernede eller udfasede funktioner i Dynamics 365 Project Operations
description: Denne artikel beskriver funktioner, der er blevet fjernet, eller som vil blive fjernet, fra Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028322"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Fjernede eller udfasede funktioner i Dynamics 365 Project Operations

_**Gælder for:** Project Operations for ressource/ikke-lagerbaserede scenarier, lille udrulning - aftale om proformafakturering og Project Operations for lagerbaserede/produktionsbaserede scenarier_

Denne artikel beskriver funktioner, der er blevet fjernet, eller som vil blive fjernet, fra Dynamics 365 Project Operations.

- En *fjernet* funktion er ikke længere tilgængelig i produktet.
- En *forældet* funktion er ikke i aktiv udvikling, og den kan blive fjernet i en senere opdatering.

Denne liste har til formål at hjælpe dig med overvejelser om fjernelse og forældelse i din egen planlægning.

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i programmer til finans og drift i [**Tekniske referencerapporter**](/dynamics/s-e/global/axtechrefrep_61). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af programmer til finans og drift.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Fjernede eller udfasede funktioner i udgivelsen til Project Operations fra marts 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parameteren Projektstyring og regnskab "Opret altid justeringstransaktion"

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsag til forældelse/fjernelse** | Justeringstransaktioner er påkrævet af hensyn til revision. Når denne parameter er udfaset, skjules den. Systemet opretter altid justeringstransaktioner, på samme måde som det gør på nuværende tidspunkt, når parameteren er angivet til **Ja**. |
| **Erstattet af en anden funktion?** | Nr. |
| **Berørte produktområder** | Applikation |
| **Installationsindstilling** | Project Operations for produktion/lagerførte scenarier |
| **Status** | Udfaset: Inden den 1. marts 2023 skjuler vi parameteren og ændrer systemfunktionsmåden, så justeringstransaktioner altid oprettes. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parameteren Projektstyring og regnskab "Brug startdato som ny projektdato"

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsag til forældelse/fjernelse** | Denne parameter blev oprindeligt brugt til at tillade justeringer, når en regnskabsperiode blev lukket. Det er dog ikke længere påkrævet, da regnskabsdatoen for transaktionen kan ændres til den første dato i den åbne periode, hvis den er konfigureret. Projektdatoen må ikke ændres, da den repræsenterer den dato, hvor transaktionen fandt sted. |
| **Erstattet af en anden funktion?** | Nr. |
| **Berørte produktområder** | Applikation |
| **Installationsindstilling** | Project Operations for produktion/lagerførte scenarier |
| **Status** | Udfaset: Inden den 1. marts 2023 skjuler vi parameteren og ændrer systemfunktionsmåden, så projektdatoen aldrig ændres i justeringer. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Arbejdsproces for ressourceanmodning i Project Operations i lager-/produktionsbaserede scenarier

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsag til forældelse/fjernelse** | Udfaset på grund af lavt brug og begrænsninger i transaktionsmængde. |
| **Erstattet af en anden funktion?** | Nr. |
| **Berørte produktområder** | Applikation |
| **Installationsindstilling** | Project Operations for produktion/lagerførte scenarier |
| **Status** | Udfaset: Inden den 1. marts 2023 deaktiverer vi muligheden for at anmode om ressourcer til projektet ved hjælp af arbejdsprocessen. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Siden Projektfakturaforslag uden visning af overskrift og linjer

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsag til forældelse/fjernelse** | Udfaset på grund af forbedringer af den side, der blev indført sammen med brug funktionsnøglen **Brug projektfakturaforslag og fakturakladdeformularer med visning af overskrift og linjer**. |
| **Erstattet af en anden funktion?** | Ja |
| **Berørte produktområder** | Applikation |
| **Installationsindstilling** | Project Operations til produktions-/lagerscenarier; Project Operations i ressourcescenarier/ikke-lagerbaserede scenarier |
| **Status** | Udfaset: Inden den 1. marts 2023 deaktiverer vi den tidligere (ældre) side og aktiverer funktionsnøglen **Brug projektfakturaforslag og fakturakladdeformularer med visning af overskrift og linjer** som standard. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Fjernede eller udfasede funktioner i udgivelsen fra december 2021 til Project Operations

### <a name="collaboration-workspaces"></a>Samarbejdende arbejdsområder

[Opret eller opret et link til et samarbejdende arbejdsområde (Projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsag til forældelse/fjernelse** | Udfasning på grund af lavt forbrug. Kunder, der bruger Project Operations i ressource/ikke-lagerbaserede scenarier, kan udnytte [Samarbejdet med Office Groups](../project-management/collaboration-groups.md). |
| **Erstattet af en anden funktion?** | Nr. |
| **Berørte produktområder** | Applikation  |
| **Installationsindstilling** | Project Operations for produktion/lagerførte scenarier |
| **Status** | Udfaset: Fra den 1. december 2022 vil vi ikke længere understøtte samarbejdende arbejdsområder. |
