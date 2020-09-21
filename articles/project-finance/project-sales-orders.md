---
title: Projektsalgsordrer for tids- og materialeprojekter
description: I dette emne gives en beskrivelse af, hvordan du kan oprette projektbaserede salgsordrer for tids- og materialeprojekter.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750499"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektsalgsordrer for tids- og materialeprojekter

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan oprette en salgsordre for et projekt. Der kan kun oprettes salgsordrer for projekter af typen **tid og materiale**.

Hvis et tids- og materialeprojekt har flere finansieringskilder i projektkontrakten, skal du aktivere parameteren **Tillad salgsordrer for projekter med flere finansieringskilder** på siden **Projektstyring og regnskabsparametre**. 

> [!NOTE]
> - Understøttelse af projektsalgsordrer med flere finansieringskilder er tilgængelig fra og med programfrigivelse 10.0.2 og nyere.
> - Den parameter, der bruges til at aktivere understøttelsen af projektsalgsordrer med flere finansieringskilder, fjernes i frigivelsesbølgende i april 2020, hvorefter funktionaliteten altid vil være aktiveret.

Du kan oprette projektbaserede salgsordrer på to måder:

- Gå til selve projektet. Vælg **Administrer > Vareopgaver > Salgsordre**i handlingsruden. Projektoplysningerne anvendes som standard for salgsordren fra projektet. Hvis projektkontrakten har mere end én finansieringskilde, skal du vælge den finansieringskilde, der skal bruges til at angive kunden til salgsordren. Hvis der kun er én finansieringskilde for projektet, angives kunden automatisk.
- Gå til listesiden **Alle salgsordre**, og opret en ny salgsordre. Du skal vælge projektet for salgsordren. Når projektet er valgt, angives kunden fra finansieringskilden, ellers skal du vælge finansieringskilden, hvis projektkontrakten har flere finansieringskilder.

