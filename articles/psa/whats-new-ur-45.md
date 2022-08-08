---
title: Nyheder eller ændringer i opdateringsudgivelse 45, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der findes i opdateringsudgivelse nr. 45 til Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169151"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 45, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse nr. 45 til Project Service Automation, V3. Denne version har buildnummer V3.10.76.168 og er generelt tilgængelig via en egenopdatering i juli 2022.

## <a name="update-release-45"></a>45. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Salg**

- Brugerne kan ikke oprette fakturaer, når de har forsøgt at oprette en faktura uden ikke-faktureret salg, hvis de også får vist den samme forekomst af siden og ikke opdaterer den.

**Tid og udgift**

- Når moderne godkendelser er aktiveret, og en genkaldt projektgodkendelse godkendes, opdateres postens fase ikke korrekt til **Tilbagekaldsanmodning godkendt**.
- Når moderne godkendelser er aktiveret, og cloudflow er inaktiv, kan godkendelsesprocessen ikke gennemføres, og de indsendende eller godkendende bruger bliver ikke underrettet.
