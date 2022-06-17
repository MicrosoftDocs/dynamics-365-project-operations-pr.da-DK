---
title: Kopiér et projekt
description: Denne artikel indeholder oplysninger om kopiering af projekter i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925757"
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
- Projekttjeklister
- Projektbuckets

## <a name="project-properties"></a>Projektegenskaber

Når projektet kopieres, kopieres værdierne i følgende felter.

| Felt | Project Operations for ikke-lagerførte materialer | Project Operations lille | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| Description | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Kunde | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Kalenderskabelon | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| Valuta | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Kontraktenhed | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Ejende virksomhed | :heavy_kontrol_mærke: | | |
| Projektleder | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| Status | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Overordnet projektstatus | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Kommentarer | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Estimater | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| <p>Anslået startdato</p><p><strong>Bemærk:</strong> I dette felt angives den dato, hvor projektet oprettes ud fra kopien. | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| <p>Anslået fuldførelsesdato</p><p><strong>Bemærk:</strong> Datoen i dette felt justeres på baggrund af startdatoen for det nye projekt, der blev skabt på baggrund af kopien.</p> | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Indsats (timer) | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Anslåede arbejdsomkostninger | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Anslåede udgiftsomkostninger | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | |
| Anslåede materialeomkostninger | | :heavy_kontrol_mærke: | |

> [!NOTE]
> Kopiér projekt er en langvarig handling. Projektposter, deres relevante attributter og mange relaterede objekter kopieres også. På grund af handlingens langvarige karakteristika er destinationsprojektsiden låst til redigering, når kopien er startet, og indtil kopieringen er fuldført.

## <a name="work-breakdown-structure"></a>Arbejdsopgavehierarki

Når projektet kopieres, kopieres hele det ressourceindlæste arbejdsopgavehierarki. Navngivne ressourcer erstattes med generiske ressourcer. Hvis de navngivne ressourcer ikke har samme arbejdstimer som den generiske ressource, genberegnes planen, og opgavernes varigheder ændres måske.

## <a name="project-team-members"></a>Projektteamets medlemmer

Når et projektteam kopieres fra kildeprojektet, kopieres de generiske ressourcer. Standardressourcetildelinger bevares også, som de var, i kildeprojektet. Navngivne ressourcer konverteres til generiske teammedlemmer.

> [!NOTE]
> Teammedlemmer og tildelinger kopieres ikke i Project for the Web.

## <a name="estimates"></a>Estimater

Når projektet kopieres, kopieres ressource-, udgifts- og materialeestimatlinjer fra kildeprojektet. 

Oplysninger om, hvordan du får adgang til Kopier projekt via programmering, finder du under [Udvikling af projektskabeloner med Kopier projekt](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Tilbud og kontrakter

Tilbud og kontrakter er ikke knyttet til destinationsprojektet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
