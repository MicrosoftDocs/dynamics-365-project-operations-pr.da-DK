---
title: Planlægningstilstande
description: Dette emne indeholder oplysninger om planlægningstilstande.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cb507528c4815f5149c813bba0a354f7d840a4a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588407"
---
# <a name="scheduling-modes"></a>Planlægningstilstande

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Dynamics 365 Project Operations giver organisationer muligheden for at definere, hvordan de administrerer ændringer af nøglevariabler i arbejdsopgavehierarkiet. Projektledere kan på baggrund af organisationens specifikke behov foretage ændringer af planlægningstilstanden, når der oprettes et projekt.

Der findes tre planlægningstilstande i Project Operations:

  - Fast varighed (dette er standardtilstanden)
  - Fast indsats (*Arbejde*)
  - Faste enheder

De værdier, der påvirkes af definitionen af en bestemt planlægningstilstand, bestemmes af følgende formel:

  Indsats = Varighed x Enheder

Når du definerer et projekts planlægningstilstand, angiver du en af disse værdier, som derefter ikke kan ændres. Fastholdelse af værdi som en konstant medfører, at den værdi skal prioriteres, hvilket giver systemet besked om, at den ikke skal ændres, når de to andre værdier ændres. Følgende tabel indeholder oplysninger om, hvordan det påvirker valget af en bestemt tilstand.

| **I denne opgave**             | **Hvis du reviderer enheder**   | **Hvis du reviderer varigheden** | **Hvis du reviderer indsatsen**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Fast enhedsopgave     | Varigheden genberegnes. | Indsatsen genberegnes.    | Varigheden genberegnes. |
| Fast indsatsopgave    | Varigheden genberegnes. | Enheder genberegnes.    | Varigheden genberegnes. |
| Fast varighedsopgave  | Indsatsen genberegnes.   | Indsatsen genberegnes.    | Enheder genberegnes.   |

Du kan finde flere oplysninger om konsekvenserne af en bestemt tilstand under [Ændring af opgavetypen for at opnå en mere nøjagtig planlægning](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). I emnet bruges udtrykket **Arbejde** i stedet for **Indsats**.

## <a name="change-the-organizations-scheduling-mode"></a>Ændre organisationens planlægningstilstand

Udfør følgende trin for at definere planlægningstilstanden for en organisation.

1. Gå til **Indstillinger** \> **Generelt** \> **Parametre**, og vælg derefter projektparameteren. 
2. På siden **Projektparametre** skal du vælge standardplanlægningstilstanden for organisationen og derefter definere projektlederens mulighed for at tilsidesætte indstillingen under oprettelsen af et nyt projekt.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Ændr planlægningstilstandsindstillingen for et projekt

Hvis en organisation tillader projektlederen at tilsidesætte standardplanlægningstilstanden, kan projektlederen foretage denne ændring, når vedkommende opretter et nyt projekt. Men når projektet er gemt, kan planlægningstilstanden ikke ændres.

## <a name="copied-projects"></a>Kopierede projekter

Da der oprettes et projekt, når kopien af projekthandlingen foretages, kan projektlederen ikke angive planlægningstilstanden. Destinationsprojektet vil altid være standard for den tilstand, der er defineret på organisationsniveau.

## <a name="copied-tasks"></a>Kopierede opgaver

Når en opgave kopieres fra et projekt til et andet, arver opgaven planlægningstilstanden for destinationsprojektet.
