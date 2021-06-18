---
title: Nyheder eller ændringer i opdateringsudgivelse 28, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 28, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010509"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 28, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede i forbindelse med Project Service Automation V3, opdateringsudgivelse 28. Denne version har build-nummer V3.10.46.32 og er generelt tilgængelig via selvopdatering i januar 2021.

## <a name="update-release-28"></a>28. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:

- Brugerne kan bruge **Masseredigering** til at opdatere tidsregistreringer, der er godkendt og indsendt.

**Projektstyring**

Følgende problemer er blevet løst:

- I de tilfælde, hvor opgave-GUID'et fortolkes som et tal, kan opgaver ikke åbnes til redigering ved hjælp af **Rediger opgave** på båndet på siden **Arbejdsopgavehierarki**.

**Sales**

Følgende problemer er blevet løst:

- Der genereres en null-referenceundtagelse, når tilføjelsesprogrammet **GetEstimatesForProject** aktiveres.
- **Markering af klar til at blive faktureret** i milepælsgitteret, opdaterer kun attributter delvist, bortset fra attributten **Fakturastatus**, som opdateres.



[!INCLUDE[footer-include](../includes/footer-banner.md)]