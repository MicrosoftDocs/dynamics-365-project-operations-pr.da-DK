---
title: Nyheder eller ændringer i opdateringsudgivelse 35, V3, til Project Service Automation
description: Dette emne angiver en liste over de funktioner og løsninger, der er tilgængelige i Microsoft Dynamics 365 Project Service Automation opdateringsversion 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574021"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 35, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 35. opdateringsudgivelse, V3. Denne version har buildnummer V3.10.56.110 og er generelt tilgængelig via en egenopdatering i september 2021.

## <a name="update-release-35"></a>35. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Tid og udgift**

- Projektgodkenderen modtager en læserettighedsfejl, når de godkender udgiftsregistreringer med en rolle som **Projektgodkender**.
- Projektgodkenderen modtager en skriverettighedsfejl på **msdyn_projectapproval**, når de annullerer en godkendt tidsregistrering med en rolle som **Projektgodkender**.
- Når du vælger **Kopiér uge** i en tidsregistreringspost i Dynamics 365 til telefon - appmodulet Project Resource Hub, opstår følgende fejl: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- Politikken **Prøv igen** godkender automatisk poster, der tidligere er blevet afvist.
- I undergitteret **Godkendelsessæt** vises ikke-gældende handlinger på båndet.
- Der mangler ikoner for **Projektopgave** og **Ressourcerolle** i objektet **Tidsregistrering**.
- Når du importerer ressourcetildelinger, har de importerede tidsregistreringer ikke den korrekte varighed for tildelinger, der er oprettet via manuelle opgaver.
- **Sletning** mangler på siden **Avanceret søgning efter tidsregistreringsposter**.
- **Gem** mangler på siden **Oplysninger om tidsregistrering**. Dette problem hindrer, at ændringer gemmes, når siden lukkes.

**Projektplanlægning**

- Gitrene **Ressourcetildeling** og **Ressourceafstemning** sorterer ikke alfabetisk i grupperede attributter.
- Opgaver kan ikke oprettes, hvis datofunktionsmåden er angivet som **Kun dato**.

**Ressourcestyring**

- Hvis både Dynamics 365 Field Service og Project Service Automation er installeret, opstår der problemer med overforbrug, når **Oversigt over tilknyttet ressourcekrav** er knyttet sammen med en hovedside.
- Når du dobbeltklikker på **Gem** i dialogboksen **Hurtig oprettelse af teammedlem**, kan ressourcekravet ikke oprettes.

**Salg**

- Der oprettes en undtagelse, hvis du sletter en opgave, der er knyttet til et tilbud med statussen **Vundet**.
