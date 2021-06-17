---
title: Definer projektkalendere
description: Dette emne giver oplysninger om, hvordan du anvender en kalenderskabelon på et projekt til at spore projektplanen.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998989"
---
# <a name="define-project-calendars"></a>Definer projektkalendere

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Hvis du vil oprette og administrere et projekt, skal du anvende en kalenderskabelon på projektet. I kalenderskabelonen defineres følgende projektattributter:

- Arbejdstider, herunder start- og sluttid
- Arbejdsdage
- Kalenderundtagelser, f.eks. ikke-arbejdsdage

Den kalenderskabelon, der anvendes på et projekt, er en kopi af den kalenderskabelon, der er defineret i organisationens indstillinger.

> [!NOTE]
> Hvis du ændrer kalenderskabelonen, overføres disse ændringer ikke til projektets arbejdstider. Hvis du vil ændre projektets arbejdstimer, skal der anvendes en ny skabelon.

Hvis du vil oprette en kalenderskabelon for din organisation, er der to nøglekrav:

- Definér skabelonens ønskede arbejdstimer ved hjælp af en ny eller eksisterende ressource, der kan reserveres.
- Opret en ny kalenderskabelon, og knyt skabelonen til den ressource, der kan reserveres.

**Definér arbejdstimerne for skabelonen**

1. Gå til **Ressourcer** \> **Ressourcer**.
2. Opret en ny ressource, der skal refereres til i kalenderskabelonen, eller vælg en eksisterende ressource.
3. Vælg fanen **Arbejdstimer** for ressourcen, og fuldfør instruktionerne i [Angiv arbejdstimer for en ressource](/dynamics365/field-service/set-work-hours-resource.md) for at konfigurere kalenderreglerne.

**Opret en ny kalenderskabelon**

1. Gå til **Indstillinger** \> **Kalenderskabelon**.
2. Vælg **Ny**, og angiv et navn, en beskrivelse og en skabelonressource.

> [!NOTE]
> Når der refereres til en ressource i en kalenderskabelon, knyttes der en kopi af ressourcens kalender til kalenderskabelonen. Hvis arbejdstimerne i den kopierede skabelon ændres, vil disse ændringer ikke blive overført til kalenderskabelonen.

Du kan nu knytte arbejdsskabelonen til en skabelon for projektkalenderen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

