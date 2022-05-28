---
title: Nyheder eller ændringer i opdateringsudgivelse 38, V3, til Project Service Automation
description: Dette emne angiver en liste over de funktioner og løsninger, der er tilgængelige i Microsoft Dynamics 365 Project Service Automation opdateringsversion 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598711"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 38, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 38. opdateringsudgivelse, V3. Denne version har et build-nummer V3.10.59.117 og er generelt tilgængelig via egen opdatering i december 2021.

## <a name="update-release-38"></a>38. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Tid og udgift**

- Der opstår en undtagelse, når længden af logfilerne for godkendelsessættet overstiger 100.000 poster.
- Brugere kan ikke få adgang til gitteret **Tidsregistrering** fra hovedsiden for **Tidsregistrering**.
- Der vises ikke tekst i dialogboksen **Import af tidsregistrering**, når der ikke er nogen elementer, som er berettiget til import.
- Brugere kan oprette godkendelsessæt, hvor feltet **Målstatus** er angivet til **Ukendt**.

**Projektstyring**

- Forskellige værdier vises ikke korrekt i ressourcetildelinger for UTC(+09:30) og UTC(+10:00), når sommertid starter.
- Feltet **Ekstra kolonne** til arbejdsopgavehierarkistrukturer er skjult i visse lokaliteter.
- Datovælgeren for kalenderkontrolelementet i gitteret **Projektopgave** er ikke korrekt oversat til kinesisk.

**Salg**

- Værdierne for **Kontraktresultater** og **Faktiske projektomkostninger** stemmer ikke overens, når ressourcer, der kan reserveres, og som har forskellige kontraktenheder og valutaer, indsender tidsregistreringer.
- En brugerdefineret arbejdsproces, der automatisk bekræfter fakturaer, lykkes ikke, når fakturaerne importeres som en administreret løsning. Følgende meddelelse vises: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException-besked: Ugyldig fakturastatus".
- Når **Root** vælges som opsummeringsindstillingen, og projektet har estimeringer fra alle transaktionsklasser (f.eks. en kombination af tid, udgifter og materialeestimater), opsummerer systemet på tværs af transaktionsklasser som en enkelt gebyrlinje.
- I scenarier, hvor der tilføjes en udgiftslinje, før en kontraktlinje knyttes til et projekt, angives den korrekte prisfastsættelse ikke som en standardværdi i feltet **Opdater pris**.
- Negative salgsbeløb er ikke tilladt i objekterne **Projekt** og **Opgave**.
