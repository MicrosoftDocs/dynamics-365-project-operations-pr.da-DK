---
title: Nyheder eller ændringer i opdateringsudgivelse 27, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der er tilgængelige i forbindelse med opdateringsudgivelse nr. 27 til Project Service Automation, V3.
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
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912923"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 27, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse 27 til Project Service Automation, V3. Denne version har build-nummer V3.10.45.98 og er generelt tilgængelig via en opdatering, du selv skal foretage, i januar 2021.

## <a name="update-release-27"></a>27. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Generelt**

Følgende problemer er blevet løst:

- Logfiler, der er genereret af tilføjelsesprogrammer i Project Service Automation, er ikke angivet til at blive slettet automatisk.
- Den automatiske opgradering mislykkes, fordi løsningen Project Service Automation indeholder et ældre null-NavBarArea- og titelelement.

**Tid og udgift**

Følgende problemer er blevet løst:

- Gitteret **Tidsregistrering** viser forkerte data for datofunktionen **Uafhængig af tidszone**.
- Gitteret **Tidsregistrering** opretter forkert tid for datofunktionen **Uafhængig af tidszone**.
- Opgaveopslag er ikke begrænset til det valgte projekt på siden **Rediger tidsregistrering**.
- Tidsgodkendelse i forbindelse med tidsregistreringer er blokerede, da systemet søger efter en projektgodkender.
- Der vises en forkert fejlmeddelelse i de korrekte registreringer på faktiske værdier.
- Når en opgave indeholder en null-værdi for faktiske omkostninger, og projekttotalerne opdateres, opstår følgende fejl: "Den oplyste nøgle findes ikke i ordbogen".
- I bestemte tilfælde viser filtrene **Grupper efter** på fanen **Projektestimat** ikke udgiftsestimater.
- Intervallet **Sommertid** er ikke korrekt for tidsregistreringer.

**Projektstyring**

Følgende problemer er blevet løst:

- Cachelagringsforbedringer, der forbedrer ydeevnen i forbindelse med indlæsning af siden **Projekt**.
- Forældet forretningsregel, der forhindrer, at projektopgaver fuldføres.
- Tilføjelsesprogrammet Microsoft Project overholder ikke tilføjelsesprogrammets kalender, hvilket resulterer i forkerte ressourcekrav.
- Når du opretter projekter ud fra skabeloner, angives tildelingsdatoerne forkert, og muligheden for at oprette ressourcekrav forhindres.
- Brugeren kan ikke få adgang til indstillingerne **Kategori**, **Beskrivelse** og **Status** ved hjælp af tastaturet.
- De faktiske salgsværdier i projektet inkluderer ikke salgsværdier for gebyrer og materiale.
- Sammenlægning af faktiske salgsværdier og faktiske omkostninger foretages forkert, når der bruges forskellige valutakurser.
- Beskrivelsen i **Standardskabelonen for arbejdstid** er vildledende.
- Når du indrykker en opgave, fjernes **Kategori** i brugergrænsefladen først, når den opdateres.
- Manglende validering for at sikre, at det ikke er tilladt for et projekt at strække sig ud over slutdatoen.

**Sales**

Følgende problemer er blevet løst:

- Der oprettes en nulreferenceundtagelse på en projekttilbudslinje, da **Import fra projektestimering** er synlig, når et projekt ikke er valgt.
- Følgende fejl: "Objektreference er ikke angivet til en forekomst på et objekt" opstår, når du lukker et tilbud som **Vundet**.
- Tilpasningsstatus angives ikke i forbindelse med en faktisk tilbageførsel, når der fjernes en tilknytning til et projekt fra en kontraktlinje.
- Når Dynamics 365 Field Service og Project Service Automation begge er installeret, vises indstillingerne **Lås prisfastsættelse** og **Brug aktuel prisfastsættelse** ikke samtidig på siden **Faktura**.
- På japansk mangler der overensstemmelse mellem oversættelsen af andre kalenderbaserede sider.
- **Aktivér** og **Deaktiver** er blevet fjernet fra objekterne **Prislistetilknytning** i Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
