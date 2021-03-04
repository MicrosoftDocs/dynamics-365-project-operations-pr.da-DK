---
title: Nyheder eller ændringer i opdateringsudgivelse 14, V3, til Project Service Automation
description: Dette emne indeholder oplysninger om nyhederne i 14. opdateringsudgivelse til Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147151"
---
# <a name="project-service-automation-update-release-14-v3"></a>Opdateringsudgivelse 14 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA). Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 14. opdateringsudgivelse. Denne version har build-nummer V3.10.4.21 og er tilgængelig for følgende plan:

- **Almindelig tilgængelighed (egen opdatering):** januar 2020
- **Automatisk opdatering:** februar 2020

## <a name="update-release-14"></a>14. opdateringsudgivelse

### <a name="enhancements"></a>Forbedringer

- Sales

     - Brugerdefinerede feltværdier fra **Detaljer for tilbudslinjer** kopieres til **Detaljer om projektkontraktlinjer**, når et tilbud opdateres til **Lukkes som vundet**.
     - Bekræftede projekter kan **Lukkes som tabt**.

- Ressourcestyring

     - Når du udvider reservationer, får brugerne vist en bekræftelsesdialogboks, hvor det er muligt at opsummere reservationsresultaterne og oprette et link til at vedligeholde reservationer.


### <a name="bug-fixes"></a>Fejlrettelser

- Tid og udgift

     - Løst: Forbedret brugeroplevelse, når brugeren ikke har valgt, hvilke poster der skal rettes.

- Ressourcestyring

     - Løst: Reservation af en ressource flere gange skaber overløb for navnet på den reserverbare ressource.

- Sales

     - Løst: Den samlede salgspris beregnes ikke, før brugeren også opretter en kostpris for udgiftsestimater på et projekt.
     - Løst: Lukning af et tilbud som **Vundet** mislykkes, hvis den tilknyttede projektkontrakt ikke er i tilstanden **Kladde**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]