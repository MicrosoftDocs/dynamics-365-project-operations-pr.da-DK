---
title: Nyheder eller ændringer i opdateringsudgivelse 13, V3, til Project Service Automation
description: Dette emne indeholder oplysninger om nyhederne i 13. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074132"
---
# <a name="project-service-automation-update-release-13-v3"></a>Opdateringsudgivelse 13 til Project Service Automation, V3
Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA). Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 13. opdateringsudgivelse. Denne version har build-nummer V3.10.3.18 og er tilgængelig for følgende plan:

- **Almindelig tilgængelighed (egen opdatering):** november 2019
- **Automatisk opdatering:** december 2019


## <a name="update-release-13"></a>13. opdateringsudgivelse 

### <a name="bug-fixes"></a>Fejlrettelser

- Tid og udgift

     - Løst: Søgefunktionaliteten på siden **Udgiftsgodkendelse** fungerer ikke, når der søges efter udgiftsformål.

- Ressourcestyring

     - Løst: Tallene i afstemningen er blevet opdateret, så de er begrundet korrekt.
     - Løst: De navngivne ressourcer kan ikke tildeles opgaver via fanen **Planlægning**.

- Projektstyring

     - Løst: Undtagelsen null-reference i forbindelse med tildeling af et teammedlem, når **TransactionType** mangler oplysninger om konfiguration af **Enhed** og **DefaultGroup**.

- Sales

     - Løst: Dubletter med poster af typen transaktion returnerer en fejl, når der oprettes rolleprisposter.
     - Løst: Ekstra knapper til **Ny salgsmulighed** , **Tilbud** , **Ordrelinje** og **Tilføj produkt** er synlige i kommandoer for salgsmuligheder, tilbud, ordreprodukter og undergittret for projektbaserede linjer.


