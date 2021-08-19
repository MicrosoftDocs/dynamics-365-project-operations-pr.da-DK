---
title: Kopiér et projekt
description: Dette emne indeholder oplysninger om kopiering af projekter i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007184"
---
# <a name="copy-a-project"></a>Kopiér et projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Ved hjælp af Dynamics 365 Project Operations kan du hurtigt oprette nye projekter ved at vælge **Kopiér projekt** i formularen **Projekter**. Hvis du vil kopiere et projekt, skal du åbne det projekt, du vil kopiere, og derefter vælge **Kopiér projekt**. Handlingen kopierer følgende:

- Projektegenskaber 
- Arbejdsopgavehierarki
- Projektteamets medlemmer
- Projektestimater
- Projektets udgiftsestimater
- Projektmaterialeestimater

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
- Anslået startdato: Datoen, hvor projektet oprettes ud fra kopien.
- Anslået slutdato: Denne dato justeres på baggrund af startdatoen for det nye projekt, der blev oprettet på baggrund af kopien.
- Indsats (timer)
- Anslåede arbejdsomkostninger
- Anslåede udgiftsomkostninger
- Anslåede materialeomkostninger

> [!NOTE]
> Kopiér projekt er en langvarig handling. Projektposter, deres relevante attributter og mange relaterede objekter kopieres også. På grund af handlingens langvarige karakteristika er destinationsprojektsiden låst til redigering, når kopien er startet, og indtil kopieringen er fuldført.

## <a name="work-breakdown-structure"></a>Arbejdsopgavehierarki

Når projektet kopieres, kopieres hele det ressourceindlæste arbejdsopgavehierarki. Navngivne ressourcer erstattes med generiske ressourcer. Hvis de navngivne ressourcer ikke har samme arbejdstid som den generiske ressource, vil tidsplanen blive genberegnet, og opgavevarighederne kan blive ændret.

## <a name="project-team-members"></a>Projektteamets medlemmer

Når et projektteam kopieres fra kildeprojektet, kopieres de generiske ressourcer. Standardressourcetildelinger bevares også, som de var, i kildeprojektet. Navngivne ressourcer konverteres til generiske teammedlemmer.

## <a name="estimates"></a>Estimater

Når projektet kopieres, kopieres ressource-, udgifts- og materialeestimatlinjer fra kildeprojektet. 

Oplysninger om, hvordan du får adgang til Kopier projekt via programmering, finder du under [Udvikling af projektskabeloner med Kopier projekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
