---
title: Nyheder eller ændringer i opdateringsudgivelse 23, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der er tilgængelige i forbindelse med opdateringsudgivelse nr. 23 til Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 968626c7b2097a9b85178cb000b3633a766f54c9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913022"
---
# <a name="project-service-automation-update-release-23-v3"></a>Opdateringsudgivelse 23 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse 23 til Project Service Automation, V3. Denne version har build-nummer V 3.10.34.30 og er generelt tilgængelig via en opdatering, som du selv skal foretage, i august 2020.

## <a name="update-release-23"></a>23. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Tid og udgift**

Følgende problemer er blevet løst:
- Håndtering af en sag på kanten i **Slet projektteammedlem** for at angive en meningsfuld undtagelse.
- Import af tildelinger medfører et tomt fjernelsesskærmbillede.

**Ressourcestyring**

Følgende problemer er blevet løst:

- **Ressourcekortet til ressourceudnyttelsesgitteret** viser forkerte data, når tidsskalaen er længere end fem dage.
- Når kunderne opretter en reserverbar ressource, kan-plug-in'et til tider ikke automatisk tilføje ressourcen til en Microsoft Office 365-gruppe.
- Visningen **Afstemning** viser manuelle konturer forkert i visningen **Uge** eller **Måned**.

**Projektstyring**

Følgende problemer er blevet løst:

- Et stort antal objekter af typen **RetrieveMultiple for brugerindstillinger** medfører forringet ydeevne i forbindelse med projektgodkendelse og andre operationer.
- Gitteret for opslag i ressourcers **Opgaveplanlægning** er begrænset, så der kun vises op til fem teammedlemmer fra projektteamet. 
- Gitteret for opslag i ressourcers **Opgaveplanlægning** filtrerer ikke inaktive ressourcer.
- Den manuelle tilstand fungerer ikke som forventet i projektplanlægningens arbejdsopgavehierarki.
- Gitteret for **Opgaveplanlægning** viser **Inaktive transaktionskategorier**.
- Gitteret for **Ressourcetildeling** afrunder forkert, når der er flere tildelinger i en opgave.
- Der er afvigelser i afrundingsværdierne for det planlagte kostbeløb og de faktiske omkostninger for en enkelt opgave.

**Sales**

Følgende problemer er blevet løst:

- Dobbeltklik på **Hent alle transaktionskategorier** opretter flere linjer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
