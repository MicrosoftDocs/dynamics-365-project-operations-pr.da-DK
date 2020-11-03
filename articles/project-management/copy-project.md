---
title: Kopiér et projekt
description: Dette emne indeholder oplysninger om kopiering af projekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074113"
---
# <a name="copy-a-project"></a>Kopiér et projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Med Dynamics 365 Project Operations kan du hurtigt bygge nye projekter ved at vælge **Kopiér projekt** på formularen **Projekter**. Hvis du vil kopiere et projekt, skal du åbne det projekt, du vil kopiere, og derefter vælge **Kopiér projekt**. Handlingen kopierer:

- Projektegenskaber
- Arbejdsopgavehierarkiet
- Projektteamets medlemmer
- Projektestimater
- Projektets udgiftsestimater

## <a name="project-properties"></a>Projektegenskaber

Når projektet kopieres, kopieres værdierne i følgende felter:

- Navn
- Beskrivelse
- Kunde
- Kalenderskabelon
- Valuta
- Kontraktenhed
- Projektleder
- Status
- Overordnet projektstatus
- Kommentarer
- Estimater
- Anslået startdato
- Slutdato
- Indsats (timer)
- Anslåede arbejdsomkostninger
- Anslåede udgiftsomkostninger

## <a name="work-breakdown-structure"></a>Arbejdsopgavehierarki

Når projektet kopieres, kopieres hele det ressourceindlæste arbejdsopgavehierarki. Navngivne ressourcer erstattes med generiske ressourcer. Hvis de navngivne ressourcer ikke har samme arbejdstid som den generiske ressource, vil tidsplanen blive genberegnet, og opgavevarighederne kan blive ændret.

## <a name="project-team-members"></a>Projektteamets medlemmer

Når et projektteam kopieres fra kildeprojektet, kopieres de generiske ressourcer. Standardressourcetildelinger bevares også, som de var, i kildeprojektet. Navngivne ressourcer konverteres til generiske teammedlemmer.

## <a name="estimates"></a>Estimater

Når projektet kopieres, kopieres både ressource- og udgiftsestimatlinjer fra kildeprojektet. 

Oplysninger om, hvordan du får adgang til Kopier projekt via programmering, finder du under [Udvikling af projektskabeloner med Kopier projekt](dev-copy-project.md).
