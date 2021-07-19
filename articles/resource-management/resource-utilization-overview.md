---
title: Oversigt over tidsforbrug for ressource
description: Dette emne indeholder oplysninger om ressourceforbrug i Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367929"
---
# <a name="resource-utilization-overview"></a>Oversigt over tidsforbrug for ressource

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Ressourcer kan have et fakturerbart tidsforbrug for et mål. Dette mål-tidsforbrug er defineret som en attribut i en ressources standardrolle eller angivet på posten for den individuelle, reserverbare ressource. Beregningerne af tidsforbrug er baseret på det faktiske antal timer, som ressourcer har rapporteret ved hjælp af godkendte tidsregistreringer.

Følgende formler bruges til at beregne forbrug:

  - Fakturerbart tidsforbrug = fakturerbare faktiske timer ÷ ressourcekapacitet
  - Ikke-fakturerbar tidsforbrug = faktisk tid med faktureringstype-ID = ikke-fakturerbar, komplementær eller ikke tilgængelig ÷ ressourcekapacitet
  - Intern = faktisk tid uden salgskontrakt ÷ ressourcekapacitet
  - Ressourcekapacitet = ressourcens arbejdstimer – ikke til stede – fridage

Du kan finde visningen **Ressourceforbrug** i ruden **Ressourcer.**

Hver celle i gitteret repræsenterer den fakturerbare udnyttelsesprocent for ressourcen i en periode, f.eks. en dag, uge eller måned. Følgende formler bruges til farvning af cellerne:

  - **Grøn**: Fakturerbart tidsforbrug > = ressourcens måltidsforbrug
  - **Gul**: Måltidsforbrug – 20 < = fakturerbart tidsforbrug < måltidsforbrug
  - **Rød**: Fakturerbart tidsforbrug < måltidsforbrug – 20

Da visningen **Ressourceforbrug** er baseret på planlægningsområdet, kan du bruge filtreringsfunktionerne i planlægningsområdet til at filtrere resultaterne.

Gitteret kræver, at du angiver et mål-tidsforbrug for enten rolle eller den enkelte ressource. Du konfigurerer dette ved at gå til **Ressourcer** > **Ressourceroller**.

Derudover skal der tildeles en standardrolle til hver af de pågældende reserverbare ressourcer. Gå til **Ressourcer** > **Ressourcer**. På fanen **Project Service** skal du kontrollere, at der er defineret en ressourcerolle, og at feltet **Er standard** er angivet til **Ja**. Du kan tilføje flere roller, hvor **Er standard** = **Nej**. Den rolle, hvor **Er standard** = **Ja**, bruges til at evaluere ressourcens tidsforbrug i forhold til destinationen for den pågældende rolle.

På fanen **Project Service** kan du også angive en individuel mål-tidsforbrug for ressourcen. I beregningen af tidsforbruget bruger derefter denne mål-tidsforbrug til at evaluere ressourcens mål i stedet for målet for ressourcens standardrolle.

Tidsforbrug vises kun for en ressource, hvis den pågældende ressource har godkendt fakturerbar tid i løbet af den periode, der vises i gitteret.


[!INCLUDE[footer-include](../includes/footer-banner.md)]