---
title: Opdater estimat ved fuldførelse
description: Dette emne indeholder oplysninger om opdatering af den projekterede indsats for et projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897759"
---
# <a name="update-estimate-at-completion"></a>Opdater estimat ved fuldførelse

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Det er almindeligt, at en projektleder reviderer de oprindelige estimater for en opgave. Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning. Vi anbefaler dog ikke, at projektledere ændrer de oprindelige tal, fordi den oprindelige projektplan repræsenterer den etablerede sande kilde for projektets tidsplan og omkostningsestimat, og alle projektets interessenter er blevet enige herom.

En projektleder kan ændre arbejdsindsatsen på opgaver på to måder:

- Tilsidesæt standardestimeringen for fuldførelse med et nyt estimat for den faktiske resterende indsats på opgaven. 
- Tilsidesætte standardstatussen i procent med et nyt estimat for den faktiske indsats på opgaven.

Hver af disse fremgangsmåder medfører en genberegning af opgavens procentvise ETC, estimering ved fuldførelse (EAC) og status samt den forventede afvigelse i tidsforbrug på en opgave. EAC, ETC og status i procenten for hovedopgaver genberegnes og giver en ny projektion af afvigelsen i tidsforbruget.