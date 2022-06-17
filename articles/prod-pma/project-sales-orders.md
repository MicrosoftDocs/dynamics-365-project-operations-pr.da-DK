---
title: Projektsalgsordrer for tids- og materialeprojekter
description: Denne artikel beskriver, hvordan du opretter projektbaserede salgsordre for tids- og materialeprojekter.
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
ms.openlocfilehash: 3a040de6d22b626b9e3d462272f43c5763b5b90f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933807"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektsalgsordrer for tids- og materialeprojekter

[!include[banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du opretter en ny salgsordre for et projekt. Der kan kun oprettes salgsordrer for projekter af typen **tid og materiale**.

Hvis et tids- og materialeprojekt har flere finansieringskilder i projektkontrakten, skal du aktivere parameteren **Tillad salgsordrer for projekter med flere finansieringskilder** på siden **Projektstyring og regnskabsparametre**. 

> [!NOTE]
> - Understøttelse af projektsalgsordrer med flere finansieringskilder er tilgængelig fra og med programfrigivelse 10.0.2 og nyere.
> - Den parameter, der bruges til at aktivere understøttelsen af projektsalgsordrer med flere finansieringskilder, fjernes i frigivelsesbølgende i april 2020, hvorefter funktionaliteten altid vil være aktiveret.

Du kan oprette projektbaserede salgsordrer på to måder:

- Gå til selve projektet. Vælg **Administrer > Vareopgaver > Salgsordre** i handlingsruden. Projektoplysningerne anvendes som standard for salgsordren fra projektet. Hvis projektkontrakten har mere end én finansieringskilde, skal du vælge den finansieringskilde, der skal bruges til at angive kunden til salgsordren. Hvis der kun er én finansieringskilde for projektet, angives kunden automatisk.
- Gå til listesiden **Alle salgsordre**, og opret en ny salgsordre. Du skal vælge projektet for salgsordren. Når projektet er valgt, angives kunden fra finansieringskilden, ellers skal du vælge finansieringskilden, hvis projektkontrakten har flere finansieringskilder.



[!INCLUDE[footer-include](../includes/footer-banner.md)]