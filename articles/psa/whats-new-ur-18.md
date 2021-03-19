---
title: Nyheder eller ændringer i opdateringsudgivelse 18, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: b35c2f8f67e1bb75493a8787f1c4d8c2baf74d51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280751"
---
# <a name="project-service-automation-update-release-18-v3"></a>Opdateringsudgivelse 18 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 18. opdateringsudgivelse. Denne version har buildnummer V3.10.8.12 og er generelt tilgængelig via en opdatering, du selv har udført i april 2020.

## <a name="update-release-18"></a>18. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

- Løst: Processerne **Tilbagekald**, **Anmodning** og **Annuller godkendelse** udløser undtagelser med fejlmeddelelser, der ikke er tydelige.
- Løst: Når det ikke er muligt at **Annullere godkendelse** af en udgift, udløses der ikke en relevant undtagelsesfejl.
- Løst: Tidsregistreringsgitteret håndterer fejlagtigt ikke-arbejdsdage i Australien efter parameteren for sommertid (sommertid) i oktober.
- Løst: Forkert standardlogik forhindrer indsendelse af udgifter.
- Løst: Når godkendelsen af tidsregistreringen mislykkes, forbliver godkendelsen i tilstanden **Afventende**.
- Løst: SQL-fejl for massegodkendelser (baglås/timeout).
- Løst: Væsentlige problemer med ydeevnen i brugeroplevelsen, som skyldes en opdatering af gruppemedlemmer under godkendelse af tidsregistreringer.

**Projektstyring**

- Løst: Tidszonemeddelelse, der flyttes fra visningen **Afstemning** til hovedformularen **Projekt**.
- Løst: Kalenderskabelonen bruges ikke korrekt, når der åbnes en ny projektformular.
- Løst: Det er i chrom-baserede browsere ikke muligt for brugere ubesværet at kunne vælge de foregående opgaver, der skal slettes.
- Løst: Oprettelse eller kopiering af et **Projekt fra en tom skabelon** henter ikke-relaterede tildelinger.
- Løst: I bestemte grænsesager resulterer oprettelsen af en ny tildeling fra opgavegitteret i dubletter af de poster, der oprettes.
- Løst: I manuel tilstand kan brugerne ikke opdatere opgavernes startdatoer, så de ligger efter den aktuelle gemte dato.

**Ressourcestyring**

- Løst: I subtotalrækken i visningen **Afstemning** beregnes reservationsvariansen ikke korrekt, når reservationen er blevet forlænget.
- Løst: Visningen **Afstemning** vises ikke ressourcetildelinger korrekt, når den reserverbare ressource har en kalender, der ikke stemmer overens med projektkalenderen.

**Sales**

- Løst: Når tidsangivelser godkendes igen (**Godkend > Annuller >** Godkend igen), oprettes der en dublet, der ikke kan faktureres.


[!INCLUDE[footer-include](../includes/footer-banner.md)]