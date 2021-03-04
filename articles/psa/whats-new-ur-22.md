---
title: Nyheder eller ændringer i opdateringsudgivelse 22, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150976"
---
# <a name="project-service-automation-update-release-22-v3"></a>Opdateringsudgivelse 22 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 22. opdateringsudgivelse. Denne version har buildnummer V 3.10.33.48 og er generelt tilgængelig via en opdatering, du selv har udført i juni 2020.

## <a name="update-release-22"></a>22. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser



**Tid og udgift**

Følgende problemer er blevet løst:

- **Tidsregistreringer** tilføjes ikke automatisk i planen for Tidsregistreringer efter importen.
- Datovælgergitteret for **Tidsregistrering** genkender ikke en brugers internationale indstillinger.

**Ressourcestyring**

Følgende problemer er blevet løst:

- I manuel tilstand kan ændringer af konturerne **Ressourcetildelingen** ikke genkendes under generering af **Ressourcebehov**.
- **Ressourceanmodninger** understøtter ikke brugerdefinerede anmodningsstatusser.

**Projektstyring**

Følgende problemer er blevet løst:

- Hvis dobbeltklikker på EstimateGridControl, fortolkes opdelte hollandske formatnumre ikke korrekt.
- Tildelte timer opdateres ikke korrekt, når tildelinger ændres ved hjælp af Microsoft Project-klienttilføjelsesprogrammet for stationære computere.
- Gitrene for Projektsporing og Estimater viser ukorrekte salgsvalutakode, når en kontraktvaluta er forskellig fra kundevaluta, og organisation er konfigureret til at vise valutakoder i stedet for valutasymboler.
- Et gruppemedlems slutdato vil tilføje én dag, hvis arbejdstidsplanen er 24 timer pr. dag.
- Hvis du føjer en Transaktionskategori til en Projektplan, udløser den ikke automatisk lagring.
- Følgende fejl vises, når du føjer et gruppemedlem til Projektskabelonen: "Ressourcekrav kan ikke knyttes til projektskabeloner". 
- Scriptet med regel for bånd "msdyn.Approval.CanApproveOrReject" viser en timeoutfejl.

**Sales**

Følgende problemer er blevet løst:

- Meddelelsen om valideringsfejl vises ikke, når der vælges en Kostprisliste i Prislisteopslaget på "Formular/objekt for prisliste for nyt tilbudsprojekt".
- Når du lukker tilbuddet som vundet, navigeres der ikke til den oprettede kontrakt, hvis et BPF, der er knyttet til tilbuddet, er i det sidste stadie.
- Hvis du tilbagefører **Ikke-faktureret salg**, knyttes de til den oprindelige omkostning, når en tidsregistrering tilbagekaldes.
- Når du har valgt knappen **Bekræft**, ændres fakturaens status ikke til **Bekræftet**, medmindre fakturaen opdateres.


[!INCLUDE[footer-include](../includes/footer-banner.md)]