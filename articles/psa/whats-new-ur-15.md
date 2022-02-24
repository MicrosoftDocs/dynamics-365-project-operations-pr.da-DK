---
title: Nyheder eller ændringer i opdateringsudgivelse 15, V3, til Project Service Automation
description: Dette emne indeholder oplysninger om nyhederne i 15. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 0ec6746c0d3a1a03ee56440c73d044df844046f8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143956"
---
# <a name="project-service-automation-update-release-15-v3"></a>Opdateringsudgivelse 15 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA). Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 15. opdateringsudgivelse. Denne version har build-nummer V3.10.5.28 og er generelt tilgængelig via en opdatering, du selv skal foretage, i januar 2020.

## <a name="update-release-15"></a>15. opdateringsudgivelse 

### <a name="enhancements"></a>Forbedringer

- Projektstyring

### <a name="bug-fixes"></a>Fejlrettelser

- Tid og udgift

  - Løst: Du kan tilføje fejlbehandling ved indlæsning i afstemningsvisningen.
  - Løst: Projektressourcehub: Omdøb **Beløb** for mindre flertydighed.
  - Løst: Juster visningen af **Kopier kolonnerne for tidsregistrering** for at medtage typen.
  - Løst: Redigering af varighed af tidsregistrering i gittervisning ved hjælp af decimaltal resulterer i en ukendt fejl for visse tal.

- Projektstyring

  - Løst: Rullemenuen til **Brug i sporingsvisning** udvides nu på baggrund af bredden af indstillingerne.
  - Løst: I forbindelse med styringen af projekter i tidszonen +13, kan der blive vist unøjagtige resultater i opgaveberegninger.
  - Løst: **Sluttidspunktet for teammedlem** er blevet rettet, når der bruges en 24-timerskalender.
  - Løst: **BPF** i hovedformularen **msdyn_project** er atter aktiveret.
  - Løst: Beregning af tildelinger ignorerer ikke længere en dag.
  - Løst: Der er føjet et nyt meddelelsesbanner til projektformularen, når der er afvigelser mellem tidszonen for bruger og projekt.

- Sales

  - Løst: Opslag i kategorien for estimerede udgifter kan anvendes til at filtrere dubletter.
  - Løst: Koden i **PluginDomain.ExecuteInTryCatchBlock(..)** skjuler ikke længere undtagelsens oprindelse.
  - Løst: Du får ikke længere en fejlmeddelelse i **Projektopslag** i formularen **Tilbudslinje**, når der er mere end 1.000 projekter.
  - Løst: Gitteret **Anslået** for arbejdsestimater og udgiftsestimater viser nu det korrekte valutasymbol.
  - Løst: Når en organisation opdaterer PSA fra 14. opdateringsudgivelse til 15. opdateringsudgivelse, vises fanen **Planlægning** ikke længere som tom i formularen **Projekt**.
