---
title: Projektsalgsordrer for tids- og materialeprojekter
description: I dette emne gives en beskrivelse af, hvordan du kan oprette projektbaserede salgsordrer for tids- og materialeprojekter.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3e88235b08ca2b8a5ccaab3dfdd7bcff4ab64f5f
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684497"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektsalgsordrer for tids- og materialeprojekter

[!include[banner](../includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan oprette en salgsordre for et projekt. Der kan kun oprettes salgsordrer for projekter af typen **tid og materiale**.

Hvis et tids- og materialeprojekt har flere finansieringskilder i projektkontrakten, skal du aktivere parameteren **Tillad salgsordrer for projekter med flere finansieringskilder** på siden **Projektstyring og regnskabsparametre**. 

> [!NOTE]
> - Understøttelse af projektsalgsordrer med flere finansieringskilder er tilgængelig fra og med programfrigivelse 10.0.2 og nyere.
> - Den parameter, der bruges til at aktivere understøttelsen af projektsalgsordrer med flere finansieringskilder, fjernes i frigivelsesbølgende i april 2020, hvorefter funktionaliteten altid vil være aktiveret.

Du kan oprette projektbaserede salgsordrer på to måder:

- Gå til selve projektet. Vælg **Administrer > Vareopgaver > Salgsordre** i handlingsruden. Projektoplysningerne anvendes som standard for salgsordren fra projektet. Hvis projektkontrakten har mere end én finansieringskilde, skal du vælge den finansieringskilde, der skal bruges til at angive kunden til salgsordren. Hvis der kun er én finansieringskilde for projektet, angives kunden automatisk.
- Gå til listesiden **Alle salgsordre**, og opret en ny salgsordre. Du skal vælge projektet for salgsordren. Når projektet er valgt, angives kunden fra finansieringskilden, ellers skal du vælge finansieringskilden, hvis projektkontrakten har flere finansieringskilder.



[!INCLUDE[footer-include](../includes/footer-banner.md)]