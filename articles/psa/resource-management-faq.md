---
title: Ofte stillede spørgsmål om ressourcestyring
description: Dette emne indeholder svar på ofte stillede spørgsmål om ressourcestyring.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144361"
---
# <a name="resource-management-faq"></a>Ofte stillede spørgsmål om ressourcestyring

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Hvad er forskellen mellem et teammedlem og et ressourcebehov?

Et projektteammedlem kan tildeles til opgaver, der er reserveret eller overreserveret, og kan angives som godkender. Et ressourcekrav kan eksistere uden et projektteammedlem, som et kladdenotat om behov. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Hvad er forskellen mellem foreslåede og foreløbigt reserverede timer?

Foreslåede timer og foreløbigt reserverede timer adskiller sig fra hinanden, hvad angår synlighed. Foreslåede timer er kun synlige for personalechefer og den projektleder, der startede efterspørgslen ved hjælp af en ressourceanmodning. Foreløbigt reserverede timer er synlige for alle, der har adgang til planlægningsområdet.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Hvordan kan jeg se de foreløbigt reserverede timer for ressourcer i et team?

Foreløbige reservationer kan foretages, når du reserverer et ressourcekrav. Ressourcer, der er foreløbigt reserveret til et projektteam, vises som teammedlemmer, der har foreløbigt reserverede timer. De vises også i planlægningsområdet.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Hvordan ændrer jeg de påkrævede timer samt start- og slutdatoerne for en ressource (generisk eller navngivet), som jeg har reserveret?

Når der er reserveret ressourcer, skal du vælge **Vedligehold reservationer** for at foretage eventuelle nødvendige ændringer.

## <a name="what-resources-types-does-project-service-automation-support"></a>Hvilke ressourcetyper understøtter Project Service Automation?

**Bruger** og **Kontakt** er de eneste ressourcetyper, der understøttes i Dynamics 365 Project Service Automation. Selvom du kan oprette andre typer ressourcer, (f.eks. **Udstyr** og **Gruppe**), understøttes ingen situationer med end-to-end-brug for dem.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Hvad er forskellen på en tildeling og en reservation?

Tildelinger er tildelingen af ressourcer til projektopgaver i projektplanen. Ressourcerne kan være enten faktiske ressourcer eller generiske ressourcer. Reservationer er definitiv eller foreløbig allokering af ressourcerne til et projekt. Definitive reservationer forbruger en ressources kapacitet. Ideelt set skulle faktiske ressourcer, reservationer og tildelinger være i overensstemmelse med hinanden, eftersom de ikke er forskellige. PSA gennemtvinger dog ikke denne aftale. I visningen Afstemning vises en projektledersituation, hvor en ressources reservationer og tildelinger ikke er i overensstemmelse med hinanden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]