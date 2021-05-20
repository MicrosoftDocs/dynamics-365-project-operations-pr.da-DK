---
title: Nyheder eller ændringer i opdateringsudgivelse 25, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948864"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 25, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede i forbindelse med Project Service Automation V3, opdateringsudgivelse 25. Denne version har build-nummer V 3.10.43.76 og er generelt tilgængelig via selvopdatering i oktober 2020.

## <a name="update-release-25"></a>25. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende fejl er blevet løst:

- Timeregistreringsdiagram viser yderligere data, som er baseret på et hentet for stort interval.

**Ressourcestyring**

Følgende fejl er blevet løst:

- Tilføjelse af kode itl Package Deployer for at springe over import af patch til Universal Resource Scheduling, hvis der allerede findes en nyere opdatering.

**Projektstyring**

Følgende problemer er blevet løst:

- Rettelser af uoverensstemmelser i afrunding og valutakurs, der medfører ukorrekte planlagte omkostninger i gitteret til projektsporing.
- Understøtter muligheden for at få vist to eller flere reaktionsgitre i formularen **Projekt**.
- Angivet validering for at imødegå muligheden for at tildele en opgave efter kalenderens slutdato, som resulterer i en mislykket ressourcetildeling.
- Forbedret fejlhåndtering til imødegåelse af null-referenceundtagelsen, som blev genereret fra følgende:

    - **PreValidateProjectTeamMemberCreate**-plug-in
    - **PreValidateProjectTaskCreate**, når en projektopgave oprettes uden et tilknyttet projekt
    - **PreProjectTeamMemberCreate**-plug-in
    - **PostProjectTeamMemberDelete**-plug-in
    - **PreValidateProjectTaskDelete**-plug-in

**Sales**

Følgende problemer er blevet løst:

- Forbedret fejlhåndtering til imødegåelse af null-referenceundtagelser, der er genereret fra **Kopier projekt: estimering af administration af hjælperessourcer**.
- **Ikke er klar til fakturering** på en **Faktureringsefterslæb for tid og materialer** rydder ikke faktureringsstatussen.
- Rettede, fejlmærkede knapper for **Priser** på fanen **Rollepris** og **Katalogelementer**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]