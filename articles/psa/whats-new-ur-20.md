---
title: Nyheder eller ændringer i opdateringsudgivelse 20, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige i opdateringsudgivelse 20 til Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: db416343ac9ac2591007e83be80493a48f9ae904
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280661"
---
# <a name="project-service-automation-update-release-20-v3"></a>Opdateringsudgivelse 20 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 20. opdateringsudgivelse. Denne version har buildnummer V 3.10.31.37 og er generelt tilgængelig via en opdatering, du selv har udført i juni 2020.

## <a name="update-release-20"></a>20. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Projektstyring**

Følgende problemer er blevet løst:

- Import af projektgruppemedlemmer med en fordelingsmetode, der kræver timer, resulterer i en utydelig fejlmeddelelse, når de angivne timer er nul.
- Brugerne får vist en fejlmeddelelse om, at der er indsat et maksimum antal tegn i feltet **Beskrivelse** for en projektopgave.
- Siden **Overfør tilføjelsesprogram til Microsoft Dynamics 365 Project Service Automation** omdirigerer til den engelske overførselsside, når brugerens sprogindstillinger er angivet til japansk.
- Når der opstår en serverfejl, beholdes synkroniseringsnavnet på fanen **Planlægning** i formularen **Projekter** til tider.
- Overflødige opgaveopdateringer sendes til serveren, når en opgave ændres.

**Sales**

Følgende problemer er blevet løst:

- På formularen **Kontrakt** bliver der ved at dobbeltklikke på **Opret faktura** oprettet to fakturaer for værdierne af en enkelt post.
- I Internet Explorer 11 kan brugere ikke oprette udgiftsposter.
- Tilbageførsel af omkostning og tilbageførsel af faktiske værdier for ikke-fakturerede salg er ikke koblet sammen.
- Knappen **Opdater de faktiske værdier** i formularen **Projekter** opdaterer ikke **Projektets faktiske timer**.
- Plug-in'et **PreValidateProjectTeamMemberCreate** kan oprette duplikerede, generiske reserverbare ressourcer, når attributten **msdyn_isgenericresourceprojectscoped** er angivet til **Falsk**.
- **Genberegn** rydder de fakturerbare omkostninger i detaljerne for produktbaserede tilbudslinjer og kontraktlinjer.
- I specifikke scenarier viser plug-in-et **PostEstimateLineUpdate** en undtagelsesfejl i null-reference.
- Varighed af tidsfasen i **Rentabilitetsanalysediagrammet** stemmer ikke overens med varigheden for omkostningerne i detaljerne for tilbudslinjerne for fastpris i tilbuddet.
- Enheds- og enhedsgruppeværdier nulstilles ikke korrekt for udgiftskategorier i formularerne **Detaljer om kontraktlinje** og **Detaljer om tilbudslinje**.
- Listerne **Org enhedskostpris** tillader overlapninger i datoeffektiviteten.
- Brugere har ikke tilladelse til at ændre **OrgUnit**, når ordretypen ikke er arbejdsbaseret, fordi den vil resultere i en undtagelsesfejl i null-referencen.
- Når du forsøger at navigere fra formularen **Detaljer om tilbudslinjen** tilbage til fanen **Tilbud**, opdateres formularen, og fanen **Oversigt** vises.


[!INCLUDE[footer-include](../includes/footer-banner.md)]