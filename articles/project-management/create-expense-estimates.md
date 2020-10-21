---
title: Udgiftsestimater
description: Dette emne indeholder oplysninger om, hvordan du definerer eller estimerer projektbaserede udgifter.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908010"
---
# <a name="expense-estimates"></a>Udgiftsestimater
_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Når der defineres ressourcebaserede estimater, giver Dynamics 365 Project Operations projektledere mulighed for at definere projektbaserede udgifter for hvert enkelt projekt. De enkelte udgiftsenheder kan knyttes til en bestemt projektopgave eller udgiftskategori. Udgiftskategorier defineres typisk på organisationsniveau. Prisfastsættelse for de enkelte udgiftskategorier defineres typisk i følgende hierarki:

- Organisation
- Kunde
- Tilbud/kontrakt

Fuldfør følgende fremgangsmåde for at få vist, tilføje eller slette en projektudgift.

1. Gå til **Projekter**, og vælg det projekt, som du vil arbejde på.
2. Vælg fanen **Projektestimater**, og få vist listen over projektudgifter.
3. Vælg **Ny udgift** for at tilføje en udgift. Du kan også vælge en udgift, du vil slette, og derefter vælge **Slet udgift**.

Følgende attributter defineres for de enkelte udgiftslinjeelementer:

- **Kategori**: De almindelige grupperinger, der bruges til at beskrive alle de udgifter, der påløber et projekt.
- **Startdato**: Den dato, hvor udgiften estimeres at skulle afholdes.
- **Antal**: Det estimerede antal udgiftsenheder for en bestemt kategori.
- **Enhedskostpris**: Den enhedspris, der bruges til at beregne omkostningerne for udgiften.
- **Enhedssalgspris**: Den enhedspris, der bruges til at beregne salgspriserne for udgiften.

