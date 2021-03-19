---
title: Kopiér et projekt
description: Dette emne indeholder oplysninger om kopiering af projekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479512"
---
# <a name="copy-a-project"></a>Kopiér et projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Ved hjælp af Dynamics 365 Project Operations kan du hurtigt oprette nye projekter ved at vælge **Kopiér projekt** i formularen **Projekter**. Hvis du vil kopiere et projekt, skal du åbne det projekt, du vil kopiere, og derefter vælge **Kopiér projekt**. Handlingen kopierer:

- Projektegenskaber (den anslåede startdato kopieres fra kildeprojektet)
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
