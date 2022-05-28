---
title: Nyheder eller ændringer i opdateringsudgivelse 43, V3, til Project Service Automation
description: Dette emne angiver en liste over de funktioner og løsninger, der er tilgængelige i Microsoft Dynamics 365 Project Service Automation opdateringsversion 43, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709975"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 43, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Det er kompatibelt med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 43. opdateringsudgivelse, V3. Denne version har buildnummer V3.10.74.200 og er generelt tilgængelig via en opdatering, du selv har udført i maj 2022.

## <a name="update-release-43"></a>43. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.


**Tid og udgift**

- Når du importerer tidsposter fra reservationer eller ressourcetildelinger, bevares referencen til den relaterede reserverbare ressource ikke.
- Når gitteret for tidsregistrering udvides til fuld skærm, fungerer navigation i gitteret med tabulatortasten ikke.
- Når der indsendes en tidspost, der er oprettet af en anden bruger, udfyldes feltet **Indsendt af** ikke korrekt med den bruger, der oprettede timeseddelen.
