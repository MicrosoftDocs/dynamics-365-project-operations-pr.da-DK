---
title: Ydeevne af forslag til projektfaktura
description: Dette emne indeholder oplysninger om forslag til forbedring af ydeevne for forslag til projektfakturaer.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e707b0d9b379df59726271b5a0441ac04e269b9a
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683439"
---
# <a name="project-invoice-proposal-performance"></a>Ydeevne af forslag til projektfaktura

[!include [banner](../includes/banner.md)]

Når du opretter et nyt fakturaforslag, kan du støde på problemer med ydeevnen, efterhånden som antallet af projekter og underprojekter øges. Hvis ydeevnen skal forbedres, er der en funktion, der reducerer den tid, det tager at oprette et nyt fakturaforslag for bogførte projekttransaktioner.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Aktivér forbedret ydeevne i forbindelse med projektfakturaforslag
Hvis du vil aktivere funktionen til forbedring af ydeevnen for forslag til projektfaktura, skal du fuldføre følgende trin.

1.  Gå til **Funktionsstyring** > **Alle**. I funktionslisten skal du finde **Forbedring af ydeevne for projektfakturaforslag**.
2.  Vælg **Aktivér nu**.
3.  Opdater din browser, og opret derefter et nyt fakturaforslag.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Deaktivér forbedret ydeevne i forbindelse med projektfakturaforslag
Fuldfør følgende trin for at deaktivere funktionen til forbedring af ydeevnen for forslag til projektfaktura.

1.  Gå til **Funktionsstyring** > **Alle**. I funktionslisten skal du finde **Forbedring af ydeevne for projektfakturaforslag**.
2.  Vælg **Deaktiver**.
3.  Opdater browseren.

> [!NOTE]
> Ydeevnen for fakturaforslag kan ikke anvendes, når faktureringsregler er aktiveret.
> 
> Under batchprocessen for at oprette fakturaforslag opdeler antallet af underopgaver opgaverne til et maksimumantal baseret på af antallet af kontrakter med fakturerbare transaktioner, uanset hvad du har angivet. Hvis du f.eks. angiver **3** for antallet af underopgaver for oprettelse af fakturaforslag i batchjob, og der kun findes to kontrakter med fakturerbare transaktioner, oprettes der kun to underopgaver.
