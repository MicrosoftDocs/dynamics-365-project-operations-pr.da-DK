---
title: Nyheder eller ændringer i Project Service Automation version 3.x, bølge 1 2020
description: Dette emne indeholder oplysninger om nyheder og ændringer i Project Service Automation version 3, bølge 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750540"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Nyheder eller ændringer i Project Service Automation version 3, bølge 1 2020
Dette emne fremhæver centrale overvejelser i forbindelse med opgraderinger, når du flytter over til den nyeste version af Project Service Automation (PSA) version 3.x, bølge 1 2020.

## <a name="time-entry"></a>Tidsregistrering
Tidsregistreringsoplevelsen er blevet udvidet med henblik på at levere funktioner til udvidelse af tidsregistrering i flere kundescenarier. Dette omfatter muligheden for at tilføje posttyper, som nu er drivkraften bag en specifik adfærd, som er baseret på skemanavnsfeltet **Indstillinger for tidsregistrering**, der vises som **Tidskilde**.

### <a name="upgrade-consideration"></a>Overvejelse i forbindelse med opgradering
Med henblik på at yde support for denne funktion er rollerne i PSA blevet opdateret, så de indeholder nye rettigheder. Disse rettigheder giver læseadgang til det nye objekt **Indstillinger for tidsregistrering**.

Brugere, der har behov for at kunne logge tid, bør tildeles brugerrollen **Tidsregistreringsbruger** som supplement til eksisterende roller. Denne rolle inkluderer den nye funktionalitet og sikrer, at tidsregistreringerne fortsat fungerer.

### <a name="currently-extended-time-entry-changes"></a>Aktuelle ændringer i udvidet tidsregistrering
Hvis du vil minimere virkningen for aktuelle brugere af tidsregistreringen, er denne rolleændring det eneste kernekrav, der er nødvendigt for at fortsætte med at bruge tidsregistrering. Hvis du har oprettet brugerdefinerede visninger eller separate tidsregistreringsoplevelser, skal du i felterne **Indstillinger for tidsregistrering** angive de korrekte PSA-værdier.
