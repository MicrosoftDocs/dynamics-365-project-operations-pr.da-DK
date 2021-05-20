---
title: Nyheder eller ændringer i opdateringsudgivelse 31, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945528"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 31, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 31. opdateringsudgivelse. Denne version har buildnummer V3.10.52.77 og er generelt tilgængelig via en opdatering, du selv har udført i maj 2021.

## <a name="update-release-31"></a>31. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:

- Kommandoknapperne for tidsregistrering på siden **Reserverbar ressource** var forvirrende.
- Der blev genereret en nulreferenceundtagelse **i Project.SetTrackingFields**, når en tidsregistrering godkendes.

**Ressourcestyring**

Følgende problemer er blevet løst:

- **Opret teammedlem** viser ikke korrekt indstillingen for metadata for reservationskonfiguration for **Standardstatus for bunden reservation**.
- Når der opgraderes fra PSA 1.X til 3.X, mislykkes opgraderingsprocessen ved **UpgradeResourceRequirements**.


**Salg**

Følgende problemer er blevet løst:

- Faktisk omsætning konverterer beløbene til projektvalutaen i sporingsgitteret.
- Valutastandarden er uklar, når der oprettes kladdelinjer, tilbudslinjer og kontraktlinjer i scenarier, hvor en organisations grundvaluta er forskellig fra projektvalutaen.
- Forespørgslen **Afventende validering af rettelseskladde** filtrerer ikke efter projekt.
- Resterende salg beregnes forkert i et projekt.
- Tilbud, der er baseret på en kontakt, kan ikke oprettes, når de oprettes uden en prisliste.
- Der vises ingen behandlingsspinner, når du vælger **Bekræft faktura**.
- Der vises ingen behandlingsspinner, når du vælger **Opret faktura**.
- Hvis du lukker et tilbud som tabt, annulleres reservationerne ikke.






