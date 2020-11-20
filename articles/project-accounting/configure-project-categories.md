---
title: Konfigurer projektkategorier
description: Dette emne indeholder oplysninger om opsætning af projektkategorier.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131921"
---
# <a name="configure-project-categories"></a>Konfigurer projektkategorier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Project Operations tilbyder effektive funktioner til kategorisering af indtægter og udgifter på projekter. Kategorier giver mulighed for at rapportere og analysere projekttransaktioner og oprette en rapport, der skal bogføres i finanskladden.

I følgende diagram illustreres korrelationen mellem transaktionskategorier, delte kategorier og projektkategorier. 

Transaktionskategorier er den grundlæggende gruppering for projekttransaktioner. I denne gruppering findes der et sæt delte kategorier, som kan deles på tværs af programmer og moduler. Mere dybdegående er projektkategorier det mest detaljerede niveau for kategorier. Projektkategorier er specifikke for en juridisk enhed, et modul og program.

![Korrelationen mellem transaktionskategorier, delte kategorier og projektkategorier](media/project-categories.png)

## <a name="transaction-categories"></a>Transaktionskategorier

Transaktionskategorier repræsenterer den grundlæggende gruppering for projekttransaktioner og er ikke virksomheds- eller transaktionstypespecifikke. Contoso Robotics bruger f.eks. design-, rejse-, installations- og servicetransaktionskategorier til at gruppere projekttransaktioner.

Transaktionskategorier defineres i Project Operations-modulet. 
1. Gå til **Indstillinger** \> **Transaktionskategorier** for at åbne formularen. 
2. Opret en ny transaktionskategori ved enten at vælge **Ny** eller ved at vælge **Importér fra Excel**.

## <a name="shared-categories"></a>Delte kategorier

I Dynamics 365 bruges begrebet Delte kategorier til at kategorisere udgifter i forskellige programmer, f.eks Dynamics 365 Finance, Dynamics 365 Supply Chain og Dynamics 365 Project Operations. For hver oprettet transaktionskategori opretter Project Operations automatisk fire relaterede delte kategorier: timer, udgifter, gebyrer og varer. Du kan gennemse og justere de delte kategorier ved at gå til **Projektstyring og regnskab** \> **Opsætning** \> **Kategorier** \> **Delte kategorier**.

## <a name="project-categories"></a>Projektkategorier

Projektkategorier repræsenterer det mest detaljerede niveau for kategorikonfiguration og skal konfigureres separat og for hvert enkelt firma af en projektbogholder.

1. Gå til **Projektstyring og regnskab** \> **Opsætning** \> **Kategorier** \> **Projektkategorier**.
2. Vælg **Ny**.
3. Vælg **Kategori-id** for den delte kategori, du har oprettet i forrige afsnit. Project Operations gør det kun muligt at bruge de delte kategorier, der er knyttet til transaktionskategorier.
4. Vælg en kategorigruppe.

## <a name="category-groups"></a>Kategorigrupper

Kategorigrupper bruges til at dele egenskaber, primært posteringsprofiler, mellem relaterede projektkategorier. Der skal være mindst én kategorigruppe for hver enkelt transaktionstype, og hver enkelt projektkategori tildeles en gruppe.

Bogføringsspecifikationerne i Project Operations er defineret i reglerne for projektomkostnings- og indtægtsprofil, projektkategorier og kategorigrupper. Du kan oprette kategorigrupper ved at gå til **Projektstyring og regnskab** \> **Opsætning** \> **Kategorier** \> **Kategorigrupper**.
