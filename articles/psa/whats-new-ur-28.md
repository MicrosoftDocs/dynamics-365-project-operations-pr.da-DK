---
title: Nyheder eller ændringer i opdateringsudgivelse 28, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der er tilgængelige i forbindelse med opdateringsudgivelse nr. 28 til Project Service Automation, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930587"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 28, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse nr. 28 til Project Service Automation V3. Denne version har buildnummer V3.10.46.32 og er generelt tilgængelig via en selvopdatering i januar 2021.

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
