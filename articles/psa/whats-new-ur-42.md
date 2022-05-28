---
title: Nyheder eller ændringer i opdateringsudgivelse 42, V3, til Project Service Automation
description: Dette emne angiver en liste over de funktioner og løsninger, der er tilgængelige i Microsoft Dynamics 365 Project Service Automation opdateringsversion 42, V3.
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589189"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 42, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 42. opdateringsudgivelse, V3. Denne version har buildnummer V3.10.73.61 og er generelt tilgængelig via en opdatering, du selv har udført i april 2022.

## <a name="update-release-42"></a>42. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Tid og udgift**

- Når en timeseddel afvises, identificeres den bruger, der har afvist den, forkert som **System**.
- Når der importeres tidsposter, mangler værdien **Ressourcekategori**.
- Projektgodkendere kan godkende indsendte projekter, når deres tilladelser ikke er specifikt angivet til **Kan godkende**.

**Salg**

- Når de faktiske værdier logføres på opgaver, der ikke er på rodniveauet, aggregeres de faktiske omkostninger forkert.
