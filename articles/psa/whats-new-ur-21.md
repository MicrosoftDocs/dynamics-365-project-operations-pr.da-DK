---
title: Nyheder eller ændringer i opdateringsudgivelse 21, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der er tilgængelige i forbindelse med opdateringsudgivelse nr. 21 til Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 7d7c098a4572aa4f5730ffdbdab77b2897cdfeff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918811"
---
# <a name="project-service-automation-update-release-21-v3"></a>Opdateringsudgivelse 21 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse 21 til Project Service Automation, V3. Denne version har buildnummer V 3.10.32.50 og er generelt tilgængelig via en opdatering, du selv har udført i juni 2020.

## <a name="update-release-21"></a>21. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:

- Når du hoster **Kontrolelementet for tidsregistreringsgitteret** i Dashboards, anvender gitteret ikke hele bredden på objektbeholderen for Dashboardgitteret.
- I forbindelse med bestemte tidszoner viser gitterkontrolelementet for **Tidsregistrering** ikke poster.
- Tidsregistreringer, der ligger efter kl. 21:00, vises på den forkerte dag.
- Brugere kan ikke sende udgifter, hvis udgiftskategorien **Kvittering for udgift påkrævet** ikke ar en værdi.

**Ressourcestyring**

Følgende problemer er blevet løst:

- Inaktive bookinger vises i oversigten **Afstemning**.
- Generisk ressourceopfyldelse manglede validering for at sikre, at der findes en gyldig bookingstatus.

**Projektstyring**

Følgende problemer er blevet løst:

- Formulargitterne for **Projekt** (**Ressourcetildeling**, **Opgave**, **Afstemning**, **Udgiftsestimater**) er fortsat redigerbare, også selvom et projekt ikke er aktivt.
- Duplikerede kunder kan ikke flettes med kunder, der er knyttet til bekræftede projektkontrakter.
- Når en ressource, der ikke har en gyldig kalender, er tilføjet, returnerer systemet ikke en brugervenlig fejlmeddelelse.
- Knappen **Tilføj opgave** i opgavegitteret aktiveres, når projektet sammenkædes med et **Microsoft Project-tilføjelsesprogram**.
- Indsatsen stiger ukontrollerbart, når en opgave med en kategori tildeles en ressource, som har en angivet kostpris.

**Sales**

Der er blevet foretaget følgende forbedringer:

- **Fakturafrekvens** og **Faktureringsstart** er blevet flyttet til fanen **Fakturaplanlægning**.

Følgende problemer er blevet løst:

- **Den samlede salgspris** er nul (0) for **Kategorien**, også selvom **Rollen** har en samlet salgspris, der ikke er nul.
- Kunderne kan ikke ændre værdien i feltet **Fakturastatus** til **Klar til fakturering**, når en anden tilpasset proces opdaterer et ekstra felt.
- Knappen **Opdater fakturalinjer** kan oprette flere duplikerede linjer, hvis den er valgt flere gange.
- Knappen **Opdater priser** virker ikke i undergitteret **Rollepriser** i formularen til **Hurtig visning**.
- Logikken **Løsningen til salgsprislisten**, håndterer ikke tidszoner korrekt, hvilket medfører et forkert udvalg af prislister.
- Beløbet for et projekts **Samlede faktiske omkostninger** kan fravige med en brøkdel, når en enkelt post er godkendt.
- Logikken **Prisløsning** indeholder ikke en brugervenlig fejlmeddelelse, hvis den **Hentede Rollepris** ikke indeholder værdier i felterne **"Primær enhed"** og **"Pris i primær enhed"**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
