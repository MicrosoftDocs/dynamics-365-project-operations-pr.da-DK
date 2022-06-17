---
title: Nyheder eller ændringer i opdateringsudgivelse 17, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der er tilgængelige i forbindelse med opdateringsudgivelse nr. 17 til Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915683"
---
# <a name="project-service-automation-update-release-17-v3"></a>Opdateringsudgivelse 17 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.  Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse nr. 17 til PSA, V3. Denne version har build-nummer V3.10.6.34 og er generelt tilgængelig via en opdatering, du selv skal foretage, i marts 2020.


## <a name="update-release-17"></a>17. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Generelt**

- Løst: Opdater Project service Automation for at gennemtvinge licenser til gruppemedlemmer (Projektressourcehub inkluderer metadata for serviceplanen for gruppemedlemmerne 3.x)
 
**Tid og udgift**

- Løst: Det er ikke muligt at ændre et udgiftsestimat fra en pris, der ikke er nul, til nul (0). Ændringen ignoreres.

**Projektstyring**

- Løst: Der er blevet tilføjet en kontrol af, om der er null-værdier i et gruppemedlems stillingsbetegnelse.
- Løst: Feltet **msdyn_userresourceid** i objektet **msdyn_resourceassignment** er blevet frarådet.
- Løst: Ved at opgradere fra 2.x til 3.x kan du nu håndtere de tomme indsatsprofiler på opgavetildelinger.

**Sales**

- Løst: **Faktura.ForhåndsgodkendelseAfOpdateringAfFaktura** håndterer nu scenariet for gentildeling af postejere korrekt.
- Løst: Når transaktionsklassen er **Tid**, er **UnitGroup** ikke redigerbar for alle objekter, herunder **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** og **ContractLineDetails**. Men **Enhed** kan ikke alene redigeres for **JournalLine** og **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
