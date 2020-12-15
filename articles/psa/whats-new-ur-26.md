---
title: Nyheder eller ændringer i opdateringsudgivelse 26, V3, til Project Service Automation
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643256"
---
<a name="project-service-automation-update-release-26-v3"></a>Opdateringsudgivelse 26 til Project Service Automation, V3
================================================

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 26. opdateringsudgivelse, V3. Denne version har et build-nummer V3.10.44.59 og er generelt tilgængelig via egen opdatering i december 2020.

<a name="update-release-26"></a>26. opdateringsudgivelse
-----------------

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:

-   Brugerne kan ændre opgaven på en tidspost, der er godkendt/sendt.

-   Fejlmeddelelsen "objektreference ikke angivet" vises under lagring af klokkeslæt.

-   Import af tidsregistrering fra ressourcetildelinger opretter tidsposter med forkerte værdier for dato og klokkeslæt.

-   Når både Project Service Automation- og Field Service-appen er installeret, vises knappen **Ny** to gange på kommandolinjen for tidsregistreringer i Field Service-appen.

-   Cellerne **Tillad enhed** og **Enhedsgruppe** samarbejder nu i gitteret **Udgiftsestimater**.

-   Formularen **Opdater redigering af tidsregistrering** indeholder **Tidslinje**.

-   Tidsgodkendelse i forbindelse med tidsregistreringer, som ikke er projektrelaterede, blokerer systemet, når der søges efter en rolle som projektgodkender.

**Ressourcestyring**

Følgende problemer er blevet løst:

-   Der er tilføjet en validering i plug-in **PostProjectCreate** for at kontrollere, om der er et primært krav, før der kan oprettes et.

-   Formularen til hurtig oprettelse af **Medlem af projektteam** viser en null-reference-undtagelse, hvis der fjernes felter fra formularen.

-   Der kan ikke oprettes krav til 12 timer fordelt over et år.

-   Forbedret fejlmeddelelse med null-reference-undtagelse under oprettelse af ressourcekrav.

**Projektstyring**

Følgende problemer er blevet løst:

-   Forbedret validering til håndtering af null-reference-undtagelse i plug-in **PreProjectUpdate**.

-   Projekter, der er udgivet af desktop-tilføjelsesprogrammet Microsoft Project sletter ikke-tildelte tildelinger.

-   En ny validering er tilføjet, når en opgaves projektreference er ugyldig pga. null-reference-undtagelse i plug-in **PreValidateProjectTaskUpdate**.

-   Teammedlemsgitteret viser ikke særskilte tildelinger i teammedlemsposten.

-   Der er tilføjet ny validering og fejlmeddelelser på grund af null-reference-undtagelsen i plug-in **PreProjectTaskDelete**.

**Sales**

Følgende problemer er blevet løst:

-   Når du vælger en projektbaseret linje i tilbud eller kontrakt, bør knappen **Forslag** kun vises, når du vælger en produktbaseret linje, der er knyttet til et eksisterende produkt.

-   Opdel rettigeheden **Opret produkt** fra rettigheden **Opret_Projektkontrakt**.

-   Sletning af fakturalinjen medfører fejl i null-referencer på **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
