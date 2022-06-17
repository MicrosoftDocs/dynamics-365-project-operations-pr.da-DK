---
title: Synkroniser ressourcekapacitet
description: Denne artikel indeholder oplysninger om, hvordan du kan synkronisere en ressources kapacitet på tværs af kalendere og projekter.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b684833ffae83b7cedfc73ee96a8aa8ddd4ec57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920697"
---
# <a name="synchronize-resource-capacity"></a>Synkroniser ressourcekapacitet

[!include [banner](../includes/banner.md)]

Processerne for ressourcesynkronisering er med til at sikre, at oplysninger til kalenderen og basiskalenderen når frem til projektets ressourceplanlægningen. Hvis kalenderen ændres, foretager processerne de påkrævede opdateringer i planlægningen af projektressourcer. Processerne er også med til at forbedre ydeevnen, da kalenderens ressourceoplysninger er blevet synkroniseret på forhånd. Opdateringer af oplysninger om ressourceplanlægning sker derfor hurtigere. Det anbefales, at du planlægger processerne som et batch i stedet for en ad gangen. I modsat fald er der risiko for, at en bruger glemmer de inkluderede datoer, da oplysningerne sidst blev synkroniseret. Hvis der ikke bruges inkluderede datoer, kan der opstå huller under datosynkroniseringen.

![Synkronisering af kalendere.](./media/projectresourcing04-1024x471.jpg)

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

[![Synkroniseringsproces.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]