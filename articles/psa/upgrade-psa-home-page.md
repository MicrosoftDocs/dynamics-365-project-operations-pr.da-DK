---
title: Startside for opgradering
description: Dette emne viser, hvor du kan finde vigtige oplysninger om de nye og ændrede funktioner i Dynamics 365 Project Service Automation og processen for opgradering til den nyeste version.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a2e17fbdfb71eb62053236bf6c8a3d1aedf332df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012354"
---
# <a name="upgrade-home-page"></a>Startside for opgradering

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Opgradere fra PSA version 2.x eller 1.x til version 3.x

### <a name="new-instances"></a>Nye forekomster

Fra og med 17. maj 2019 installeres version 3.x som standard, når Project Service Automation er valgt under klargøring af en ny forekomst.

### <a name="existing-instances"></a>Eksisterende forekomster

Før var kunder, der havde en forekomst af PSA version 2.x og skulle opgradere til version 3.x, som er den UCI-baserede (Unified Client Interface) version af PSA, nødt til at kontakte Microsoft Support for at få oplysninger om deres forekomst, så supportafdelingen kunne aktivere forekomsten, som du vil opgradere til version 3.x. Fra 1. marts 2020 vil kunder, der har en forekomst af PSA version 2.x og har brug for at opgradere til version 3.x, kunne opgradere deres forekomster direkte fra administrationsportalen uden at skulle kontakte Microsoft Support.  

> [!NOTE]
> PSA-version 3.x indeholder betydelige ændringer. Den er baseret på Unified Interface-rammen med det formål at give en bedre brugeroplevelse. Den nydesignede app har en ensartet, effektiv brugergrænseflade (UI) med dynamisk design og optimal visning på en hvilken som helst skærmstørrelse eller enhed. Der er sket andre ændringer i hele programmet. Nogle af de områder, der er blevet ændret, omfatter prisfastsættelse, reservation og tildeling af ressourcer, tid, udgifter og godkendelser.

Det anbefales, at du udfører følgende opgaver, før du påbegynder opgraderingsprocessen:

- Kontrollér, om både Dynamics 365 Field Service og Project Service Automation er installeret på den identificerede forekomst. Hvis begge løsninger er installeret, bør du planlægge at opgradere dem begge, før du genoptager den almindelige brug af forekomsten.
- Gennemse følgende emner grundigt. Kendskab til og forståelse af forskellene mellem versionerne kan hjælpe dig med opgraderingsprocessen. Disse emner indeholder oplysninger om de største ændringer i PSA samt overvejelser og anbefalinger i forbindelse med planlægning af opgraderingen til version 3.x.

    - [Nyheder eller ændringer i Project Service Automation version 3](whats-new-changed-v3.md)
    - [Overvejelser i forbindelse med opgradering – Project Service Automation version 2.x eller 1.x til version 3](upgrade-v3.md)

- Opgrader sandkasseforekomsten for at evaluere ændringerne i implementeringen, før du opgraderer din produktionsforekomst.

Når du har gennemgået de emner, der er nævnt tidligere, og du er klar til at opgradere til PSA version 3.x eller den UCI-baserede version, skal du indsende en forespørgsel til Microsoft Support for at gøre opgraderingen tilgængelig fra Administration. Angiv oplysningerne om din forekomst i din anmodning.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Ældre versioner af PSA (PSA version 2.x) i en nyoprettet forekomst

Fra og med 17. maj 2019 har alle nye forekomster også UCI som standardklient. For at kunne tilpasse sig denne ændring vil PSA version 3.x og Field Service version 8.x blive leveret som standard, da disse versioner er udviklet til at fungere sammen med UCI-klienten.

Fra 1. marts 2020 vil kunder med Dynamics PSA ikke længere kunne oprette et nyt miljø med ældre versioner af PSA, f.eks. PSA version 2.x eller lavere. Alle nye miljøer kan kun hentes til version 3.x af PSA.

> [!NOTE]
> For at få den bedste oplevelse, når du bruger ældre versioner af Field Service- og PSA-programmer, skal du gå til siden **Systemindstillinger** og for feltet **Brug kun den nye Unified Interface (anbefales)** skal du klikke på **Nej**, da disse versioner ikke er designet til at blive indlæst korrekt i UCI. Når du har slået UCI fra, kan du åbne og køre disse versioner af Field Service og PSA ved hjælp af den gamle webklient. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]