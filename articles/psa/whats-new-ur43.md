---
title: Nyheder eller ændringer i opdateringsudgivelse 43, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der findes i opdateringsudgivelse nr. 43 til Microsoft Dynamics 365 Project Service Automation, V3.
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915303"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 43, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Det er kompatibelt med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse nr. 43 til Project Service Automation, V3. Denne version har buildnummer V3.10.74.200 og er generelt tilgængelig via en opdatering, du selv har udført i maj 2022.

## <a name="update-release-43"></a>43. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.


**Tid og udgift**

- Når du importerer tidsposter fra reservationer eller ressourcetildelinger, bevares referencen til den relaterede reserverbare ressource ikke.
- Når gitteret for tidsregistrering udvides til fuld skærm, fungerer navigation i gitteret med tabulatortasten ikke.
- Når der indsendes en tidspost, der er oprettet af en anden bruger, udfyldes feltet **Indsendt af** ikke korrekt med den bruger, der oprettede timeseddelen.
