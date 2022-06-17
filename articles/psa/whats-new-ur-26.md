---
title: Nyheder eller ændringer i opdateringsudgivelse 26, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der er tilgængelige i forbindelse med opdateringsudgivelse nr. 26 til Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 11f722c1f31c0e8aa08192cc955aabbe97018225
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928793"
---
# <a name="project-service-automation-update-release-26-v3"></a>Opdateringsudgivelse 26 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse 26, V3 til Project Service Automation. Denne version har et build-nummer V3.10.44.59 og er generelt tilgængelig via egen opdatering i december 2020.

## <a name="update-release-26"></a>26. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:

- Brugerne kan ændre opgaven på en tidspost, der er godkendt/sendt.
- Fejlmeddelelsen "objektreference ikke angivet" vises under lagring af klokkeslæt.
- Import af tidsregistrering fra ressourcetildelinger opretter tidsposter med forkerte værdier for dato og klokkeslæt.
- Når både Project Service Automation- og Field Service-appen er installeret, vises knappen **Ny** to gange på kommandolinjen for tidsregistreringer i Field Service-appen.
- Cellerne **Tillad enhed** og **Enhedsgruppe** samarbejder nu i gitteret **Udgiftsestimater**.
- Formularen **Opdater redigering af tidsregistrering** indeholder **Tidslinje**.
- Tidsgodkendelse i forbindelse med tidsregistreringer, som ikke er projektrelaterede, blokerer systemet, når der søges efter en rolle som projektgodkender.

**Ressourcestyring**

Følgende problemer er blevet løst:

- Der er tilføjet en validering i plug-in **PostProjectCreate** for at kontrollere, om der er et primært krav, før der kan oprettes et.
- Formularen til hurtig oprettelse af **Medlem af projektteam** viser en null-reference-undtagelse, hvis der fjernes felter fra formularen.
- Der kan ikke oprettes krav til 12 timer fordelt over et år.
- Forbedret fejlmeddelelse med null-reference-undtagelse under oprettelse af ressourcekrav.

**Projektstyring**

Følgende problemer er blevet løst:

- Forbedret validering til håndtering af null-reference-undtagelse i plug-in **PreProjectUpdate**.
- Projekter, der er udgivet af desktop-tilføjelsesprogrammet Microsoft Project sletter ikke-tildelte tildelinger.
- En ny validering er tilføjet, når en opgaves projektreference er ugyldig pga. null-reference-undtagelse i plug-in **PreValidateProjectTaskUpdate**.
- Teammedlemsgitteret viser ikke særskilte tildelinger i teammedlemsposten.
- Der er tilføjet ny validering og fejlmeddelelser på grund af null-reference-undtagelsen i plug-in **PreProjectTaskDelete**.

**Sales**

Følgende problemer er blevet løst:

- Når du vælger en projektbaseret linje i tilbud eller kontrakt, bør knappen **Forslag** kun vises, når du vælger en produktbaseret linje, der er knyttet til et eksisterende produkt.
- Opdel rettigeheden **Opret produkt** fra rettigheden **Opret_Projektkontrakt**.
- Sletning af fakturalinjen medfører fejl i null-referencer på **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
