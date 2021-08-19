---
title: Nyheder eller ændringer i opdateringsudgivelse 34, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 1c8ef43b953ad282a1f5fed6eeeb1e1a991e715100b66938be03b5b5f3da575e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009749"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 34, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 34. opdateringsudgivelse. Denne version har buildnummer V3.10.55.38 og er generelt tilgængelig via en egenopdatering i juli 2021.

## <a name="update-release-34"></a>34. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser
Følgende problemer er blevet løst.

**Generelt**

- Udgiverbaserede opdateringer aktiverer ikke den nye moderne godkendelsesarbejdsproces.
- Attributterne **Målstatus** og **Handlingstype** mangler på hovedsiden for **godkendelsessæt**.

**Tid og udgift**

- Anmodning om godkendelse kan ikke godkendes ved hjælp af det moderne godkendelsesproces.
- Kopiering af en uges poster fungerer ikke, når der kopieres poster, der ikke er relateret til den bruger, der er logget på.

**Projektplanlægning**

- Ressourcetildelingsprofiler bliver beskadiget, når de importeres fra Microsoft Project-tilføjelsesprogrammet til stationære computere.

**Ressourcestyring**

- Når du udgiver et projekt fra Microsoft Project-tilføjelsesprogrammet til klienter på stationære computere, ændres slutdatoen for eksisterende krav.
- Decimalpræcisionen overstiger to decimaler i bekræftelsesdialogboksen for udvidelse af reservationer.

**Salg**

- Når du tilføjer en produktbaseret linje med et eksisterende produkt til en projektkontrakt, vises undtagelsen af typen **Nøgle blev ikke fundet i ordbog**.
- Kundeemner kan ikke kvalificeres, når en ordretype knyttes fra et kundeemne til en salgsmulighed.
