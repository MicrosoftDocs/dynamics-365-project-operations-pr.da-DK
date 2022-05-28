---
title: Nyheder eller ændringer i opdateringsudgivelse 33, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601471"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 33, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 33. opdateringsudgivelse. Denne version har buildnummer V3.10.54.98 og er generelt tilgængelig via en egenopdatering i juli 2021.

## <a name="update-release-33"></a>33. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:

- To låste felter, **msdyn_description** og **msdyn_externaldescription** kan redigeres efter indsendelse.
- Der vises en fejlmeddelelse, hvis der oprettes en udgiftspost, som ikke er relateret til et projekt.
- Når der oprettes en tidsregistrering, angives ressourcerollen som standard til en inaktiv rolle.
- Kladdelinjer, der er knyttet en tilbagekaldt eller slettet udgift, slettes ikke.
- På **Formular til hurtig oprettelse af tidsregistrering** skal du opdatere visningen **Projektopgaveliste** for at ændre den som standard viste dato til opgavens startdato.
- Når du opretter en tidsregistrering under fanen **Relateret** i den reserverbare ressource, oprettes tidsregistreringen forkert for den bruger, der er logget på, i stedet for den overordnede ressource, der kan reserveres.
- Nye felter tilføjes til dialogboksen **MDD-massegodkendelse**.

**Projektplanlægning**

Følgende problemer er blevet løst:
- Dårlig ydeevne i forbindelse med oprettelse af projekter, når projektskabeloner med arbejdstid anvendes med komplekse kalendere.
- Når startdatoen er større end slutdatoen, vises der en fejl i kopiprojektskabelonen på grund af forskelle i tidskomponenten i hvert felt.

**Ressourcestyring**

Følgende problemer er blevet løst:
- Der bruges en forkert parameter i ressourceforbrugsforespørgslen, og XML fører til forkerte filterresultater i gitteret **Ressourceforbrug**.
- Bekræftelse af **Udvidelse af reservation** viser en forkert slutdato for reservationer.

**Salg**

Følgende problemer er blevet løst:
- Der opstår en fejlmeddelelse, hvis der oprettes en kategoripris med manglende værdier.
- Der opstår en fejlmeddelelse, hvis der oprettes en kontraktlinjemilepæl uden en ordrelinje.
