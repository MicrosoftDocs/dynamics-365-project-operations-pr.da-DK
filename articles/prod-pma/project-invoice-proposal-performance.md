---
title: Ydeevne af forslag til projektfaktura
description: Denne artikel indeholder oplysninger om forbedringer af ydeevnen i forslag til projektfakturaer.
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
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927183"
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
