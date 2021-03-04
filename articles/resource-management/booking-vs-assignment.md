---
title: Reserveringer vs. tildelinger
description: Dette emne indeholder oplysninger om forskellene mellem ressourcereservationer og ressourcetildelinger.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841165"
---
# <a name="bookings-vs-assignments"></a>Reserveringer vs. tildelinger

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Reservationer er definitiv eller foreløbig allokering af ressourcerne til et projekt. Definitive reservationer forbruger en ressources kapacitet. Reservationer repræsenterer organisationskoncepter for teams, så de kan forstå, hvordan ressourcer anvendes på tværs af forskellige projekter. Dynamics 365 Project Operations anser reservationer for at være et projektniveaukoncept. 

I modsætning til reservationer er tildelinger ressourcers forpligtelse til projektopgaver i projektplanen. Ressourcerne kan navngives eller være generiske.  Når et ressourcekrav udledes af projektopgavetildelingerne, bruger Project Operations ressourcetildelingens indsatsprofiler til at opbygge profilerne i detaljerne for ressourcekravet. En henvisning til ressourcetildelingerne bibeholdes dog ikke. Opdateringer af de reservationer, der stammer fra ressourcekravet, opdaterer ikke ressourcetildelinger.

Summen af en ressources reservationer svarer typisk til summen af ressourcens tildelinger på tværs af en eller flere opgaver. Project Operations gennemtvinger dog ikke denne aftale. I visningen **Afstemning** kan projektlederen se de steder, hvor en ressources reservationer og tildelinger ikke stemmer overens med hinanden.


