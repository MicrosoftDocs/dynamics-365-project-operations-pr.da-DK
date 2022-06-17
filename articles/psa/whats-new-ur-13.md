---
title: Nyheder eller ændringer i opdateringsudgivelse 13, V3, til Project Service Automation
description: Denne artikel indeholder oplysninger om nyheder i opdateringsudgivelse nr. 13 til Project Service Automation, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930679"
---
# <a name="project-service-automation-update-release-13-v3"></a>Opdateringsudgivelse 13 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA). Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse 13 til Project Service Automation, V3. Denne version har build-nummer V3.10.3.18 og er tilgængelig for følgende plan:

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
     - Løst: Ekstra knapper til **Ny salgsmulighed**, **Tilbud**, **Ordrelinje** og **Tilføj produkt** er synlige i kommandoer for salgsmuligheder, tilbud, bestil produkter og undergitteret for de projektbaserede linjer.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
