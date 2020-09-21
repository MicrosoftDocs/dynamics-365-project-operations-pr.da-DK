---
title: Nyheder i 13. opdateringsudgivelse til Project Service Automation, V3
description: Dette emne indeholder oplysninger om nyhederne i 13. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750544"
---
# <a name="project-service-automation-v3-update-release-13"></a>13. opdateringsudgivelse til Project Service Automation V3
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
     - Løst: Ekstra knapper til **Ny salgsmulighed**, **Tilbud**, **Ordrelinje** og **Tilføj produkt** er synlige i kommandoer for salgsmuligheder, tilbud, ordreprodukter og undergittret for projektbaserede linjer.


