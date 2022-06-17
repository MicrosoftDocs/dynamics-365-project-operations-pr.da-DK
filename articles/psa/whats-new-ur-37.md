---
title: Nyheder eller ændringer i opdateringsudgivelse 37, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der findes i opdateringsudgivelse nr. 37 til Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922491"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 37, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse nr. 37 til Project Service Automation, V3. Denne version har buildnummer V3.10.58.120 og er generelt tilgængelig via en selv-opdatering i november 2021.

## <a name="update-release-37"></a>37. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Tid og udgift**
- Brugere kan ikke slette en tidsregistrering ved at rydde cellen.
- Visningen **Min mislykkede godkendelse** indeholder kun projektgodkendelser med statussen **Indsendt**.

**Projektstyring**
- Brugere modtager en nulreferenceundtagelsesfejl, når de åbner et projekt i Microsoft-tilføjelsesprogrammet til skrivebordet, hvis projektteammedlemmets stillingsbetegnelse er tom.
- Knappen **Gem** findes ikke på siden **Projektopgave**, så brugere ikke kan gemme ændringer af opgaveposter.
- Brugere kan ikke slette et projekt, hvor der er knyttet en opgave til et tilbud med statussen **Vundet**.

**Salg**
- Feltet **Valuta** på siden **Projekt** opdateres, så det stemmer overens med den anvendte skabelons valuta.
- Omkostningen beregnes forkert på opgaver, der har flere valutaer.
