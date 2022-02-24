---
title: Synkroniser ressourcekapacitet
description: Dette emne indeholder oplysninger om, hvordan du synkroniserer en ressources kapacitet på tværs af kalendere og projekter.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074150"
---
# <a name="synchronize-resource-capacity"></a>Synkroniser ressourcekapacitet

[!include [banner](../includes/banner.md)]

Processerne for ressourcesynkronisering er med til at sikre, at oplysninger til kalenderen og basiskalenderen når frem til projektets ressourceplanlægningen. Hvis kalenderen ændres, foretager processerne de påkrævede opdateringer i planlægningen af projektressourcer. Processerne er også med til at forbedre ydeevnen, da kalenderens ressourceoplysninger er blevet synkroniseret på forhånd. Opdateringer af oplysninger om ressourceplanlægning sker derfor hurtigere. Det anbefales, at du planlægger processerne som et batch i stedet for en ad gangen. I modsat fald er der risiko for, at en bruger glemmer de inkluderede datoer, da oplysningerne sidst blev synkroniseret. Hvis der ikke bruges inkluderede datoer, kan der opstå huller under datosynkroniseringen.

![Synkronisering af kalendere](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synkronisering af akkumulering af ressourcekapacitet

Synkroniseringsprocessen er tiltænkt at skulle synkronisere alle ressourcekalenderoplysninger. Disse oplysninger inkluderer basiskalenderoplysninger om eventuelle ændringer af tabellen for projektets ressourcekalenderkapacitet. Hvis der tilføjes nye ressourcer i projektet, kan synkroniseringen hjælpe dig med at sikre, at de opdaterede kalenderoplysninger er tilgængelige. Denne synkronisering kan udføres på et hvilket som helst tidspunkt.

Vi anbefaler, at du bruger en batch . Indstillingerne er tilgængelige under synkronisering af kapacitetsreservationer.

1. Vælg **Projektstyring og regnskab** &gt; **Periodisk** &gt; **Kapacitetssynkronisering** &gt; **Synkroniser ressourcekapacitetsakkumuleringer**.
2. Angiv mulighederne i den følgende tabel.

    | Indstilling      | Beskrivelse |
    |-------------|-------------|
    | Periodekode | Du kan evt. vælge intervalkoden for finanskladden for at angive start- og slutdatoer for synkroniseringsprocessen for akkumulering af ressourcekapacitet. |
    | Startdato  | Angiv startdatoen for synkroniseringsprocessen for akkumuleringer af ressourcekapacitet. |
    | Slutdato    | Angiv slutdatoen for synkroniseringsprocessen for akkumuleringer af ressourcekapacitet. |

[![Synkroniseringsproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
