---
title: Oversigt over planlægningsassistent
description: Dette emne indeholder oplysninger om, hvordan du kan arbejde med planlægningsassistenten for at reservere ressourcer.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125621"
---
# <a name="schedule-assistant-overview"></a>Oversigt over planlægningsassistent

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Planlægningsassistent bruges til at reservere ressourcer på baggrund af de krav, der er defineret af projektlederen. Planlægningsassistenten er afhængig af de parametre, der er angivet i ressourcekravet, for at finde ressourcen. Planlægningsassistenten anbefaler ressourcer, der stemmer overens med de relevante krav, f.eks. tidsfrister eller færdigheder.

Når den identificerer passende ressourcer, kan Resource Manager eller projektlederen reservere ressourcen til arbejdet.

## <a name="prerequisites"></a>Forudsætninger

Planlægningsassistenten er en del af Universal Resource Scheduling-løsningen. Denne løsning er inkluderet og installeret sammen med Dynamics 365 Project Operations, Dynamics 365 Field Service og Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Matche krav og ressourcer

Et genereret ressourcekrav er baseret på detaljer som f.eks.:

-   Egenskaber
-   Roller
-   Afdelinger
-   Ressourcepræferencer
-   Indsatsprofiler
-   Tidszone

I planlægningsassistenten bruges disse detaljer til at filtrere ressourcer.

## <a name="launch-the-schedule-assistant"></a>Start planlægningsassistenten

Planlægningsassistent kan startes på to måder. Hvis du bruger hybridtilstanden, kan du vælge et teammedlem med et ikke-opfyldt ressourcekrav i teammedlemsgitteret og derefter vælge **Reserver**. Hvis du bruger den centrale tilstand, finder og vælger Resource Manageren ressourcen.

## <a name="schedule-assistant-filters"></a>Planlægningsassistentfiltre

Når planlægningsassistenten kører, vises detaljerne fra ressourcekravet som filtrerede værdier i venstre rude. Resource Manageren eller projektlederen kan finjustere resultaterne ved at justere filtrene, så de opfylder planlægningsbehovene.

I filtreringsruden vises de arbejdsrelaterede indstillinger, herunder:

-   Arbejdets start og afslutning
-   Egenskaber
-   Roller
-   Afdelinger
-   Ressourcevirksomhed
-   Ressourcetyper
-   Foretrukne ressourcer
