---
title: Opret et projektteam
description: Dette emne indeholder oplysninger om, hvordan du opretter og administrerer projektteams.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074337"
---
# <a name="create-a-project-team"></a>Opret et projektteam

[!include [banner](../includes/banner.md)]

Hvis du vil bruge de roller, der tidligere blev konfigureret i et projekt, skal en projektleder knytte rollerne sammen med projektet. Der kan tildeles flere roller til et projekt. For at forhindre forvirring navngives disse roller automatisk i forbindelse med reservationen. Hvis projektlederen f.eks. har behov for tre softwareteknikere, oprettes der automatisk tre roller for softwareteknikere, der automatisk navngives **softwareingeniør1**, **softwareingeniør 2** og **softwareingeniør 3**. Hvis der tidligere er konfigureret rolleegenskaber for rollen, anvendes de som et filter under søgninger efter en ressource. Du kan tilføje yderligere egenskaber, hvis du vil begrænse søgningen yderligere.

Visningsindstillinger kan også tilpasses for at give en bedre visning af ressourcetilgængelighed. Der er mulighed for at få vist tilgængelighed baseret på tid, dag, uge, måned, kvartal og år. Der findes også en indstilling, der viser tilgængelighed og resterende kapacitet for ressourcer. Denne indstilling er nyttig i forbindelse med tidsstyring, når du beregner ledig tid for aktiviteter eller tilgængelighed af ressourcer.

Projektlederen kan vælge en rolle på siden og derefter vælge at reservere en ressource til at udfylde rollen, hvis der findes en tilgængelig ressource, der opfylder behovet. Bemærk, at der ikke skal reserveres ressourcer på dette tidspunkt i planlægningsstadiet. Når du opretter en WBS, kan du erstatte roller med personaleressourcer i projektet. Hvis roller erstattes med personaleressourcer i WBS, opdaterer ressourceopsætningen automatisk projektteamets liste og planlægning.

[![Projektteamets liste, som indeholder både roller og faktiske ressourcer](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektlederen har forskellige muligheder for at reservere en ressource til et bestemt projekt, f.eks. **Resterende kapacitet**, **Fuld kapacitet**, **Kapacitetsprocent** og **Angiv timer**. Disse indstillinger for reservation kan når som helst annulleres, hvis ressourcetildelingerne ændres. Der understøttes to typer af reservation:

- **Reserver definitivt** – Ressourcereservationen blev godkendt og bekræftet til at arbejde på aftalen i den angivne periode.
- **Reserver foreløbig** – Ressourcereservationer blev midlertidigt angivet til at arbejde på aftalen i den angivne periode.

Følgende procedure forklarer, hvordan du opretter et projektteam.

## <a name="create-a-project-team"></a>Opret et projektteam

1. På listesiden **Alle projekter** skal du vælge et projekt og derefter vælge **Rediger**.
2. På fanen **Projektteam og planlægning** skal du i feltet **Planlæg slutdato** angive den planlagte startdato plus en måned. Hvis planens startdato f.eks. er den 24. juni 2017 (24/06/2017), skal du angive **24/07/2017**.
3. Vælg **Tilføj**.
4. I ruden **Tilføj roller til projektet** skal du i feltet **Rolle** vælge **Overordnet projektleder**.
5. Vælg **Krævede kompetencer**.
6. På siden **Vælg egenskaber** vælges de egenskaber, som du tidligere har angivet for rollen overordnet projektleder, som standard. Vælg **OK**.
7. På siden **Tilføj roller til projekt** skal du i feltet **Antal ressourcer** angive **1**.
8. I feltet **Ressource** vises opslaget for alle de ressourcer, der har de krævede kompetencer. Vælg **Daniel Goldschmidt**, og vælg derefter **Opret**.
9. På siden **Projekt** skal du vælge **Tilføj**.
10. I ruden **Tilføj roller til projektet** skal du i feltet **Rolle** vælge **Teammedlem**. Angiv **5** i feltet **Antal ressourcer**.
11. Vælg **Opret**.
12. På siden **Projekter** skal du vælge **Opfyld ressource**.

## <a name="monitor-project-teams"></a>Overvåg projektteams
1. På siden **Alle projekter** skal du vælge linket **Projekt-id** for projektet **XYZ-opgraderingsfase 2**.
2. På hurtigfanen **Projektteam og planlægning** skal du kontrollere, at de viste projektressourcer er korrekt angivet.
