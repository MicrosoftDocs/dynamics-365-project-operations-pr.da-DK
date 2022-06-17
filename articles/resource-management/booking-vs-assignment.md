---
title: Reserveringer vs. tildelinger
description: Denne artikel indeholder oplysninger om forskellene mellem ressourcebooking og ressourcetildelinger.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918581"
---
# <a name="bookings-vs-assignments"></a>Reserveringer vs. tildelinger

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Reservationer er definitiv eller foreløbig allokering af ressourcerne til et projekt. Definitive reservationer forbruger en ressources kapacitet. Reservationer repræsenterer organisationskoncepter for teams, så de kan forstå, hvordan ressourcer anvendes på tværs af forskellige projekter. Dynamics 365 Project Operations anser reservationer for at være et projektniveaukoncept. 

I modsætning til reservationer er tildelinger ressourcers forpligtelse til projektopgaver i projektplanen. Ressourcerne kan navngives eller være generiske.  Når et ressourcekrav udledes af projektopgavetildelingerne, bruger Project Operations ressourcetildelingens indsatsprofiler til at opbygge profilerne i detaljerne for ressourcekravet. En henvisning til ressourcetildelingerne bibeholdes dog ikke. Opdateringer af de reservationer, der stammer fra ressourcekravet, opdaterer ikke ressourcetildelinger.

Summen af en ressources reservationer svarer typisk til summen af ressourcens tildelinger på tværs af en eller flere opgaver. Project Operations gennemtvinger dog ikke denne aftale. I visningen **Afstemning** kan projektlederen se de steder, hvor en ressources reservationer og tildelinger ikke stemmer overens med hinanden.




[!INCLUDE[footer-include](../includes/footer-banner.md)]