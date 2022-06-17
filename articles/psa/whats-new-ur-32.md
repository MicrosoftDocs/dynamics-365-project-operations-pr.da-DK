---
title: Nyheder eller ændringer i opdateringsudgivelse 32, V3, til Project Service Automation
description: Denne artikel indeholder de funktioner og løsninger, der er tilgængelige i forbindelse med opdateringsudgivelse nr. 32 til Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 5124137c24da9b579ee1365524d66d9135b2d420
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912877"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 32, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikel indeholder de funktioner og løsninger, der er nye eller ændrede i forbindelse med opdateringsudgivelse nr. 32 til Project Service Automation, V3. Denne version har buildnummer V3.10.53.108 og er generelt tilgængelig via en selvopdatering i juni 2021.

## <a name="update-release-32"></a>32. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

#### <a name="general"></a>Generelt

- Når en større opgradering mislykkes, bør kun indgangspunkterne i hovedprogrammet blive blokeret for at sikre, at delte objekter stadig er tilgængelige.

#### <a name="time-and-expense"></a>Tid og udgift

Følgende problemer er blevet løst:

- **TimeEntriesImportFromResourceAssignment** vedligeholder ikke start- og sluttiderne for ressourcetildelingsudsnit.
- Når du vælger **Åben post** i gitteret **Tidsregistrering**, kan du muligvis ikke vælge andre formularer.
- Mens du importerer tildelinger til tidsregistreringen, kan klientkodeforespørgslen oprette en lang URL-adresse, som ikke lykkes med at udføre forespørgslen.
- Når en værdi er slettet fra en celle i gitteret **Tidsregistrering**, forbliver fokus ikke på gitteret.
- Knappen **Afvis** er blevet fjernet fra visningen **Behandling af godkendelser** for moderne godkendelser.
- Stabiliteten og ydeevnen af massegodkendelse af tidsregistreringer påvirkes af fastlåsninger og en fejl i den passende håndtering af tilpasninger, der er relateret til objektet **Tidsregistrering**.

#### <a name="project-planning"></a>Projektplanlægning

- Der oprettes en nulreferenceundtagelse, når du opdaterer et projekt, der har en null-værdi i feltet **Kontraktenhed**.
- **Opdater projekttotaler** beregner de resterende omkostninger og salg i et projekt forkert.
- Overflødige prisfastsættelsesberegninger påvirker den ydeevne, der er relateret til opdateringer af ressourcetildelinger.

#### <a name="resource-management"></a>Ressourcestyring

Følgende fejl er blevet løst:

- Når en reserverbar ressources kalenderkapacitet er større end 1, genkender Project Service Automation ikke kapaciteten korrekt som 0 (nul). Der indtræffer derfor en uendelig løkke i planlægningsvisningen.

#### <a name="sales"></a>Salg

Følgende problemer er blevet løst:

- Når der oprettes en gitterlinje, som har en brugerdefineret transaktionstype, indtræffer følgende null-referenceundtagelse: *Microsoft.Dynamics.ProjectService.Plugins.StilstandLinePlugins.ValidateUnitScheduleAndUnitActionTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodePlaugin)*.
- Der bør ikke tilføjes roller og kategorier, der er deaktiveret, før et tilbud kopieres til fakturerbare roller og kategorier i det nyligt kopierede tilbud.
- Dokumentdatoen og regnskabsdatoen stemmer ikke overens med den startdato, der findes på en fakturalinjedetalje, som oprettes direkte på en kladdefaktura.
- Der oprettes null-referenceundtagelser i scenarier, der er relateret til deaktiveringen af roller og kategorier, før et tilbud kopieres.
- Handlingen **Opdater priser** på siden **Projekter** opdaterer ikke udgiftsestimater og materialeestimater.
