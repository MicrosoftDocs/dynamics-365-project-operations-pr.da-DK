---
title: Nyheder eller ændringer i opdateringsudgivelse 30, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der er tilgængelige i forbindelse med opdateringsudgivelse nr. 30 til Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: ad00b126a13e18a5de47df335aea06b9690efa13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925067"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 30, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse 30 til Project Service Automation, V3. Denne version har buildnummer V3.10.51.61 og er generelt tilgængelig via en opdatering, du selv har udført i april 2021.

## <a name="update-release-30"></a>30. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:

- Der opstår en fejl, når du opretter og gemmer en tidsregistrering på siden **Hurtig oprettelse**, hvis feltet **Rolle** fjernes.
- Filteret for tidsregistrering anvender den forkerte filteroperator.
- Kopierede timesedler vises ikke automatisk, når du vælger **Kopiér uge** i tidsregistreringskontrollen.

**Ressourcestyring**

Følgende problemer er blevet løst:

- Når du udvider en reservation, er den reservationsstatus, der er tildelt den faste reservation, forkert. Hvis en reservation udvides, respekteres den reservationsstatus, der er defineret som **Bindende** i metadataene for reservationen.
- Når der ikke er angivet en gyldig reservationsstatus, er fejlmeddelelsen ikke korrekt oversatte.

**Projektstyring**

Følgende problemer er blevet løst:

- Projekter kan ikke oprettes i én valuta og medtage relaterede opgaver i en anden valuta.

**Salg**

Følgende problemer er blevet løst:

- Når en prisliste kopieres, opdateres priser ikke.
- Det lykkes ikke at lukke et tilbud som vundet, når omkostningsdetaljerne har en værdi for oprindelse.
- I objektet **Projektopgave** er **Estimerede omkostninger** blevet omdøbt til **Planlagte omkostninger (basis)**.
- Der oprettes en nulreferenceundtagelse, når fakturaer oprettes eller slettes.
