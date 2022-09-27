---
title: Nyheder eller ændringer i opdateringsudgivelse 47, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der findes i opdateringsudgivelse nr. 47 til Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477228"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 47, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse nr. 45 til Project Service Automation, V3. Denne version har buildnummer V3.10.78.8 og er generelt tilgængelig via en egenopdatering i juli 2022.

## <a name="update-release-47"></a>47. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Ressourcestyring**
- En validering blev opdateret for at sikre, at brugere ikke kan udløse en nulreferenceundtagelse, når de forsøger at oprette et projektteammedlem uden en **ressource, der kan reserveres**.
