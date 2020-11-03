---
title: Nyheder eller ændringer i Project Service Automation version 3.x, bølge 1 2020
description: Dette emne indeholder oplysninger om nyheder og ændringer i Project Service Automation version 3, bølge 1 2020.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074118"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Nyheder eller ændringer i Project Service Automation version 3, bølge 1 2020
Dette emne fremhæver centrale overvejelser i forbindelse med opgraderinger, når du flytter over til den nyeste version af Project Service Automation (PSA) version 3.x, bølge 1 2020.

## <a name="time-entry"></a>Tidsregistrering
Tidsregistreringsoplevelsen er blevet udvidet med henblik på at levere funktioner til udvidelse af tidsregistrering i flere kundescenarier. Dette omfatter muligheden for at tilføje posttyper, som nu er drivkraften bag en specifik adfærd, som er baseret på skemanavnsfeltet **Indstillinger for tidsregistrering** , der vises som **Tidskilde**. Der er tilføjet en ny løsning kaldet Tid, Udgift, Statusangivelse og Godkendelser (TESA) for at understøtte denne funktion.

### <a name="upgrade-consideration"></a>Overvejelse i forbindelse med opgradering
Med henblik på at yde support for denne funktion er rollerne i PSA blevet opdateret, så de indeholder nye rettigheder. Disse rettigheder giver læseadgang til det nye objekt **Indstillinger for tidsregistrering**.

Brugere, der har behov for at kunne logge tid, bør tildeles brugerrollen **Tidsregistreringsbruger** som supplement til eksisterende roller. Denne rolle inkluderer den nye funktionalitet og sikrer, at tidsregistreringerne fortsat fungerer.

Hvis du har brugerdefinerede app-moduler, der omfatter alle formularer for objektet tidsangivelse, skal du også fjerne **Formularen til hurtig oprettelse af TESA-tidsangivelse** fra modulet.

### <a name="currently-extended-time-entry-changes"></a>Aktuelle ændringer i udvidet tidsregistrering
Hvis du vil minimere virkningen for aktuelle brugere af tidsregistreringen, er denne rolleændring det eneste kernekrav, der er nødvendigt for at fortsætte med at bruge tidsregistrering. Hvis du har oprettet brugerdefinerede visninger eller separate tidsregistreringsoplevelser, skal du i felterne **Indstillinger for tidsregistrering** angive de korrekte PSA-værdier.
