---
title: Udgiftsspecifikation
description: I denne artikel forklares det, hvordan du kan specificere udgifter ved hjælp af det nye arbejdsområde Udgifter.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920927"
---
# <a name="expense-itemization"></a>Udgiftsspecifikation

[!include [banner](../includes/banner.md)]

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Organisationer kræver ofte, at medarbejderne angiver detaljerede oplysninger om de udgifter, der opstår under rejser. Ethotelophold kan f.eks. indeholde flere specificerede linjer for værelsespris, moms, parkering og andre diverse udgifter, der opstår hver dag under et ophold. Eller en måltidsudgift kan kræve, at du angiver en mere detaljeret pris for mad, frokost eller aftensmad. Uanset organisationens behov kan de enkelte udgiftskategorier konfigureres til at afspejle de underkategorier eller linjeelementer, der udgør en udgift. Mens specificering altid har været understøttet i **Udgiftsstyring**, giver det **Nydesignede arbejdsområde for udgifter** mulighed for en mere effektiv specificering, når funktionen **Mulighed for hurtigt at specificere tilbagevendende udgifter** er aktiveret.  

## <a name="enable-quick-itemization"></a>Aktiver hurtig specificering 

Du kan bruge funktionen **Mulighed for hurtigt at specificere tilbagevendende udgifter** til at angive tilbagevendende udgifter hurtigt, samtidig med at du undgår at skulle angive de daglige udgifter, der er forbundet med dit ophold, hver gang. Fuldfør følgende trin for at aktivere hurtig specificering.

1. Gå til arbejdsområdet **Funktionsstyring**, og find og vælg **Nydesignede udgiftsrapporter** på listen over funktioner . 
2. Vælg **Aktivér nu**. 
3. På funktionslisten skal du finde og vælge **Mulighed for hurtigt at specificere tilbagevendende udgifter**.
4. Vælg **Aktivér nu**. 

## <a name="itemization-grid"></a>Specificeringsgitter 

Hvis en udgiftskategori indeholder underkategorier eller forskellige komponenter, der udgør denne udgift, kan den specificeres. Hvis du vil specificere en udgift, skal du vælge udgiftslinjen i udgiftsrapporten og i ruden **Udgiftsdetaljer** væge **Handlinger** > **Specificer**. Skyderen **Specificering** viser et gitter med felter. Følgende tabel indeholder et eksempel på hvert enkelt felt i gitteret, og hvordan feltet gengives i udgiftsrapporten. 

|     Felt          |     Description                                                                                  |     Eksempel              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Underkategori    |     Listen over underkategorier, der er konfigureret under kategoritypen **Hotel**.             |     Daglig værelsespris      |
|     Startdato     |     Den dato, hvor udgiftselementet første gang opstod.                                           |     13/09/2021           |
|     Dagspris     |     Det beløb, der er afholdt for udgiftselementet.                                                    |     200                  |
|     Antal       |     Det antal gange, som beløbet gentages over en løbende periode.                       |     3                    |

![Specificer udgifter.](media/Itemization%20screen%201.png)

Når du gemmer en specificering, kan du se en individuelt angivet linje for det antal, der er angivet i specificeringsgitteret. Hver linje starter på den dato, der er angivet i gitteret.

![Specificeret rapport.](media/Itemization%20screen%202.png)

