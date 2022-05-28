---
title: Nyheder eller ændringer i opdateringsudgivelse 19, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 19, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 96229a6c656cd88b7314b4692ae5d53897b4e6c5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596104"
---
# <a name="project-service-automation-update-release-19-v3"></a>Opdateringsudgivelse 19 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 19. opdateringsudgivelse. Denne version har buildnummer V3.10.30.41 og er generelt tilgængelig via en opdatering, du selv har udført i maj 2020.

## <a name="update-release-19"></a>19. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst: 

- Fejl, der er afledt af import af tidsangivelser, er ikke bragt op til overfladen korrekt.
- Gitteret for tidsangivelse understøtter ikke adfærden for feltet **Kun dato**.
- Projektressourcer kan ikke oprette udgifter til et projekt.

**Projektstyring**

Følgende problemer er blevet løst: 

-  En underordnet opgave resulterer i et forkert indsatsestimat i forbindelse med beregningen af fuldførelse (EAC).

**Sales**

Følgende problemer er blevet løst: 

- Funktionen **Genberegning** fungerer ikke sammen med detaljer om kontraktlinjer for udgifter eller detaljer om tilbudslinjer.
- Der mangler **Opdater priser** for udgiftsestimater.
-  Kunderne kan ikke vælge brugerdefinerede kontraktstatusårsager på siden **Projektkontrakt**.
- Kunder oplever forringet ydeevne, når der oprettes en brugerdefineret prisliste ud fra et tilbud.
- Kunder oplever uoverensstemmelse med standarderne **enhed** på siderne **Detaljer om tilbudslinje** og **Detaljer om kontraktlinje**.
- Tilføjelse af elementer for ikke-fakturerbare transaktionskategorier til en debiterbar kontraktlinje respekterer ikke transaktionskategoriens faktureringstype **Ikke-fakturerbar**.
- Kunderne kan ikke bruge de netop tilføjede roller og kategorier i tidligere oprettede kontrakter.
- Kunder oplever forringet ydeevne ved unødvendig hentning i PreValidateProjectTeamMemberUpdate.cs
- Roller, der er konfigureret som ikke-fakturerbare på listen **Ressourcekategorier**, skal føjes til fanen **Fakturerbare roller** som **Ikke-fakturerbare** på kontraktlinjen for et projekt.
- Kunderne kan opleve forringet ydeevne, når de opretter et projekt, da **GetBookableResourceIdFromUser** henter alle kolonner med reserv rbare ressourcer i stedet for kun det primære id.
- Objektet **TransactionType** mangler plug-in'en til opdatering før validering for at forhindre brugere i at angive **Enheder** og **UnitGroups**, der ikke er gyldige for transaktionstyper.
- Trinnet **Fjern** virker ikke for import af tidsangivelse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
