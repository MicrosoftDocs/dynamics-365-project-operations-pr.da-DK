---
title: Reserveringer vs. tildelinger
description: Dette emne indeholder oplysninger om forskellene mellem ressourcereservationer og ressourcetildelinger.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130211"
---
# <a name="bookings-vs-assignments"></a>Reserveringer vs. tildelinger

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Reservationer er definitiv eller foreløbig allokering af ressourcerne til et projekt. Definitive reservationer forbruger en ressources kapacitet. Reservationer repræsenterer organisationskoncepter for teams, så de kan forstå, hvordan ressourcer anvendes på tværs af forskellige projekter. Dynamics 365 Project Operations anser reservationer for at være et koncept på projektniveau. 

I modsætning til reservationer er tildelinger ressourcers forpligtelse til projektopgaver i projektplanen. Ressourcerne kan navngives eller være generiske. 

Summen af en ressources reservationer svarer typisk til summen af ressourcens tildelinger på tværs af en eller flere opgaver. Project Operations gennemtvinger dog ikke denne aftale. I visningen **Afstemning** kan projektlederen se de steder, hvor en ressources reservationer og tildelinger ikke stemmer overens med hinanden.
