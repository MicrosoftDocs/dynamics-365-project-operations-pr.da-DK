---
title: Omkostningsestimering af ressourcetildelinger, som er omfattet af en underentreprise
description: Denne artikel forklarer, hvordan Microsoft Dynamics 365 Project Operations beregner omkostningsestimering af ressourcetildelinger, som er omfattet af en underentreprise.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262052"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Omkostningsestimering af ressourcetildelinger, som er omfattet af en underentreprise

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Omkostningerne for opgavetildelinger for projektteammedlemmer, der tilhører underleverandøren, beregnes hjælp af den **Indkøbsprisliste**, der er knyttet til underentreprisen på den relaterede teammedlemspost. Dette er forskelligt fra den måde, som omkostningerne til medarbejderressourcetildelinger beregnes på, hvor omkostningerne ved opgavetildelinger af medarbejderressourcer beregnes ved hjælp af den **Omkostningsprisliste**, der er knyttet til den kontraherende enhed i projektet. 

For generiske projektteammedlemmer, som er omfattet af en underentreprise, beregnes omkostningerne for tildelinger for ved hjælp af den indkøbsprisliste, der er knyttet til underentreprisen. Indkøbspriser kan også konfigureres specifikt for de enkelte ressourcer. Disse ressourcespecifikke priser får førsteprioritet, når opgavetildelinger for navngivne projektteammedlemmer er kontraktmedarbejdere. 

Prioriteten for at bruge rollespecifikke indkøbspriser i forhold til ressourcespecifikke er baseret på opsætningen af prioriteten for prisfastsættelsesdimension i **Parametre > Beløbsbaserede prisfastsættelsesdimensioner**.

Denne funktion med dynamisk afledte priser, som er baseret på dimensionskonfigurationen for indkøbspriser for underleverandører, svarer til den måde, som omkostnings- og faktureringssatser afledes for fuldtidsmedarbejdere. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Oprettelse af opgavetildelinger for at få omkostningsestimeringer for underleverandørressourcer

Opgavetildelinger for underleverandører kan oprettes på to måder: 
- Ved hjælp af fanen **Opgaver**.
- Ved hjælp af fanen **Team**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Oprettelse af ressourcetildelinger ved hjælp af fanen Opgaver
Ved hjælp af listen **Ressourcer** under fanen **Opgaver** for en bestemt opgave kan du oprette en opgavetildeling for en navngivet ressource eller en generisk ressource. Hvis du vælger en navngivet ressource på rullelisten **Tildelte ressourcer** på opgaven, og denne ressource er en kontraktmedarbejder, tildeles den navngivne ressource til opgaven, og der oprettes en tilsvarende projektteammedlemspost, hvor medarbejdertypen er angivet til **Kontraktmedarbejder** og **Gyldighed** angivet til **Ugyldig**. Som næste trin skal du åbne posten for projektteammedlemmerne og vælge en underleverandør- og underentrepriselinje. Derved opdateres opgavetildelingen, så den indeholder en reference til underleverandøren og underentrepriselinjen, og statussen for teammedlemmerne opdateres til **Gyldig**.

Hvis du vælger at oprette et generisk teammedlem fra rullelisten **Tildelte ressourcer** på opgaven, giver dialogboksen **Oprettelse af generiske teammedlem** dig mulighed for at vælge en underleverandør og underentrepriselinje. Når den generiske ressource tildeles til opgaven, og den tilknyttede projektteammedlemspost oprettes, vil du se, at projektteammedlemsposte er oprettet, og medarbejdertypen er angivet til **Kontraktmedarbejder** og **Gyldighed** er angivet til **Gyldig**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Oprettelse af projektteammedlemmer ved hjælp af fanen Team
Ved hjælp af fanen Team på projektet kan du oprette et generisk eller navngivet teammedlem. Når du opretter teammedlemmer, kan du vælge underleverandøren og underentrepriselinjen. Når teamedlemmet er oprettet, skal du tildele teammedlemmet til en opgave ved hjælp af rullelisten **Tildelte ressourcer** på opgaven. 

## <a name="updating-estimates"></a>Opdatering af estimater
Når du har tildelt projektteammedlemmer til opgaver, skal du navigere til fanen **Estimater** i projektet og vælge **Opdater priser** for at sikre, at omkostningssatserne for underleverandørressourcetildelinger opdateres på baggrund af den indkøbsprisliste, der er knyttet til underentreprisen. Der udregnes ikke estimater for ikke-tildelte opgaver i Microsoft Dynamics 365 Project Operations. Derfor skal du oprette opgavetildelinger til forskellige pris- og omkostningsopgaver i projektet. 

> [BEMÆRK!] Medlemmer af projektteam, der har **Medarbejdertypen** **Kontraktmedarbejder**, men ikke har en underleverandørreference, markeres som **Ugyldige** i gitteret **Projektteammedlemmer**. Hvis der findes et projektteammedlem med denne status, skal du åbne projektteammedlemsposten og manuelt opdatere felterne for underleverandøren og underentrepriselinjen, så det økonomiske omkostningsestimat korrekt afspejler underleverandøromkostningerne på fanen **Estimater**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
