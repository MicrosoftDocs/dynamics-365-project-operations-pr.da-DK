---
title: Nyheder eller ændringer i opdateringsudgivelse 29, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948615"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 29, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 29. opdateringsudgivelse. Denne version har et build-nummer V3.10.47.7 og er generelt tilgængelig via egen opdatering i februar 2021.

## <a name="update-release-29"></a>29. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:

- Brugere kan ikke se, at arbejdstimer er logget på fridage i gitteret for tidsregistrering.
- Godkendte udgiftsposter kan redigeres i gitteret.

**Projektstyring**

Følgende problemer er blevet løst:

- Manglende valideringslogik, der sikrer, at ressourcetildelingens indsatstimer ikke kan være negative.
- Ved hjælp af den brugerdefinerede handling **AssignResourcesForTask** opdateres alle felter i stedet for kun ændrede felter.
- Når du kopierer et projekt i et miljø med tilføjelsesprogrammer eller arbejdsprocesser, der er registreret i hændelsen **Opretprojekt**, så opdateres attributten **msdyn_bulkgenerationstatus** ikke, hvis **CopyWBSToProject** mislykkes.
- Når du udvider projektkalenderen, sorteres arbejdsdagene ikke i stigende rækkefølge, hvilket medfører, at visse opdateringer af projektopgaven ikke lykkes.
- Hvis du ændrer projektlederen i et eksisterende projekt, udløses organisationsenhedens standardlogik.

**Salg**

Følgende problemer er blevet løst:

- Fanen **Kontraktens ydeevne** på siden **Kontrakt** forbliver stille under initialisering, når der ikke findes nogen kontraktlinjer.