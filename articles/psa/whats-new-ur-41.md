---
title: Nyheder eller ændringer i opdateringsudgivelse 41, V3, til Project Service Automation
description: Dette emne angiver en liste over de funktioner og løsninger, der er tilgængelige i Microsoft Dynamics 365 Project Service Automation opdateringsversion 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580909"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 41, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 41. opdateringsudgivelse, V3. Denne version har build-nummer V3.10.62.162 og er generelt tilgængelig via en opdatering, du selv skal foretage, i marts 2022.

## <a name="update-release-41"></a>41. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Projektstyring**
- Når du forsøger at oprette et projekt ud fra en skabelon, der er baseret på et projekt, som er oprettet fra tilføjelsesprogrammet til skrivebordet, vises følgende fejl: "Valideringen af ressourcetildelingens planlagte arbejdsfelt: Hver ressourcetildelingstidssnit må ikke være tidligere end startdatoen".

**Tid og udgift**
- Når du forsøger at slette en tidspost, vises fejlmeddelelsen "Der opstår en uventet fejl fra ISV-kode".

**Salg**
- Når du opretter en faktura for en fast pris-milepæl, udfyldes felterne **Beskrivelse** og **Ekstern beskrivelse** ikke. 
