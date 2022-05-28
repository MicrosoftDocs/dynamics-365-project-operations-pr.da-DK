---
title: Nyheder eller ændringer i opdateringsudgivelse 40, V3, til Project Service Automation
description: Dette emne angiver en liste over de funktioner og løsninger, der er tilgængelige i Microsoft Dynamics 365 Project Service Automation opdateringsversion 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588637"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 40, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 40. opdateringsudgivelse, V3. Denne version har et build-nummer V3.10.61.61 og er generelt tilgængelig via egen opdatering i februar 2022.

## <a name="update-release-40"></a>40. opdateringsudgivelse

### <a name="features"></a>Funktioner
Fase 1 af opgraderingen fra Project Service Automation til Project Operations – lille udgives i februar 2022 til alle kunder. Se [Opgrader fra Project Service Automation til Project Operations](upgrade-project-operations-non-stocked.md) for at kontrollere egnethed. Hvis programmet ikke vises i din forekomst i Power Platform Administration, skal du kontakte support og bede om, at funktionen aktiveres for dine miljøer. Din anmodning skal indeholde en liste over miljø-id'er, hvor funktionen skal aktiveres.

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Tid og udgift**
- Der mangler en notepost, når en tidspost afvises eller annulleres. 

**Salg**

- Når du opdaterer omkostnings- eller salgsestimater ved hjælp af standard-plug-ins, får du fejlagtigt tilladelse til at sende JSON-nyttedata, der ikke er gyldige uden for brugergrænsefladen.
- Når du opdaterer tilbudslinjer ved hjælp af den hurtige visning, kan du aktivere tilbud.
