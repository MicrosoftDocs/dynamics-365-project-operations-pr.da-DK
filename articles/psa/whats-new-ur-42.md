---
title: Nyheder eller ændringer i opdateringsudgivelse 42, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der findes i opdateringsudgivelse nr. 42 til Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912708"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 42, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse nr. 42 til Project Service Automation, V3. Denne version har buildnummer V3.10.73.61 og er generelt tilgængelig via en opdatering, du selv har udført i april 2022.

## <a name="update-release-42"></a>42. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Tid og udgift**

- Når en timeseddel afvises, identificeres den bruger, der har afvist den, forkert som **System**.
- Når der importeres tidsposter, mangler værdien **Ressourcekategori**.
- Projektgodkendere kan godkende indsendte projekter, når deres tilladelser ikke er specifikt angivet til **Kan godkende**.

**Salg**

- Når de faktiske værdier logføres på opgaver, der ikke er på rodniveauet, aggregeres de faktiske omkostninger forkert.
