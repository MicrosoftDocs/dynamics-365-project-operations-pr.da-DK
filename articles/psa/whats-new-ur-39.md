---
title: Nyheder eller ændringer i opdateringsudgivelse 39, V3, til Project Service Automation
description: Dette emne angiver en liste over de funktioner og løsninger, der er tilgængelige i Microsoft Dynamics 365 Project Service Automation opdateringsversion 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588729"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 39, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 39. opdateringsudgivelse, V3. Denne version har build-nummer V3.10.60.170 og er generelt tilgængelig via en opdatering, du selv skal foretage, i januar 2022.

## <a name="update-release-39"></a>39. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Generelt**

- Der er foretaget adskillige forbedringer af oversigten over webstedet til arabisk oversættelse.

**Projektstyring**

- Der opstår en fejl, når du ændrer projektlederen i et projekt til en bruger, der allerede er et teammedlem i projektet.

**Salg**

- Ejeren af **Projektkontraktprislisten** er forkert, når prislisten oprettes automatisk. 
- Prislistens ikrafttrædelsesdato overholdes ikke, når prislisten anvendes på projektparameteren.
- Kontraktparten har muligvis ikke den rette standardværdi, når to separate tilbud redigeres.
