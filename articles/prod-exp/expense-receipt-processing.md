---
title: Behandling af udgiftskvittering
description: Dette emne indeholder oplysninger om behandling af kvitteringer ved hjælp af optisk tegngenkendelse (OCR). Denne funktion er beregnet til at forbedre brugeroplevelsen, når der oprettes udgiftsrapporter i Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 067432106742447d2b8fa215ec05bf05f4b41e70
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684313"
---
# <a name="expense-receipt-processing"></a>Behandling af udgiftskvittering

Udgiftsposten er blevet forbedret via introduktionen af behandling af kvitteringer ved hjælp af optisk tegngenkendelse (OCR). Denne funktion er udviklet til at forbedre brugeroplevelsen ved oprettelse af udgiftsrapporter.

## <a name="key-features"></a>Nøglefunktioner

- Forhandlernavnet, datoen og det samlede beløb udtrækkes fra kvitteringer.
- Denne funktion forsøger at sammenholde ikke-tilknyttede kvitteringer med ikke-tilknyttede udgiftstransaktioner.
- Brugere kan oprette manuelt indtastede udgiftstransaktioner på grundlag af kvitteringer.

## <a name="usage-examples"></a>Eksempler på brug

Hvis du automatisk vil vedhæfte kvitteringer, der omfatter kreditkorttransaktioner, når en udgiftsrapport oprettes, skal du gøre følgende:

  1. Åbn arbejdsområdet **Udgiftsstyring**.
  2. På fanen **Kvitteringer** skal du kontrollere, at der findes ikke-tilknyttede kvitteringer. Du kan også overføre kvitteringer under fanen **Kvitteringer**.
  3. På fanen **Udgifter** skal du kontrollere, at der findes ikke-tilknyttede udgifter. Udgiftsadministratoren importerer typisk disse udgifter fra kreditkortudbyderen.
  4. Vælg **Ny udgiftsrapport**. Bemærk, at du nu også kan inkludere udgifter og kvitteringer, når du opretter en udgiftsrapport. Hvis du tilføjer både udgifter og kvitteringer, udløses automatisk afstemning af kvitteringer i forhold til udgifterne.

Hvis du vil oprette en udgift eller afstemme en udgift fra en kvittering, skal du gøre følgende:

  1. På en udgiftsrapport skal du på fanen **Kvitteringer** tilknytte en kvittering ved at vælge **Tilføj kvitteringer**.
  2. Læg mærke til indstillingerne **Opret** og **Afstem** under det overførte billede af kvitteringen.

      - Vælg **Opret** for at oprette en manuelt angivet udgiftstransaktioner, og angiv de værdier, der er udtrukket fra kvitteringen.
      - Hvis du vælger **Afstem**, vil systemet forsøge at afstemme en eksisterende udgift med kvitteringen.

## <a name="installation"></a>Installation

Denne funktion fungerer sammen med funktionen for **Nye udgiftsrapporter**, som hjælper med at forenkle udgiftsoplevelsen. Denne funktion er kun tilgængelig for miljøer over niveau 2, hvilke er sandkasse- og produktionsmiljøer.

Hvis du vil bruge disse avancerede udgiftsfunktioner, skal du installere tilføjelsesprogrammet til Udgiftsstyring-tjeneste til Microsoft Dynamics 365 Finance, og aktivere funktionerne i din forekomst. Du kan få adgang til tilføjelsesprogrammet fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).

1. Log på LCS, og åbn det ønskede miljø.
2. Gå til **Komplette detaljer**.
3. Vælg **Bevar** eller rul ned til oversigtspanelet **Tilføjelsesprogrammer i miljøet**.
4. Vælg **Installer et nyt tilføjelsesprogram**.
5. Vælg **Tjeneste til udgiftsstyring**.
6. Følg installationsvejledningen, og accepter vilkårene og betingelserne.
7. Vælg **Installer**.

I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktioner:

- Nye udgiftsrapporter
- Automatisk afstemning og opret udgift fra kvittering

Når du aktiverer disse funktioner, udføres følgende handlinger:

- Det eksisterende arbejdsområde for **Udgiftsstyring** erstattes med det nye arbejdsområde.
- Der tilføjes et nyt menupunkt for synligheden af udgiftsfeltet.
- Du kan stadig åbne den tidligere side med **Udgiftsrapport** ved at gå til **Udgiftsstyring > Mine udgifter > Udgiftsrapporter**.
- Arbejdsprocesser og eventuelle godkendelser fører dig stadig til siden med den eksisterende udgiftsrapport.
- Kvitteringer vil blive behandlet via Microsoft Azure Cognitive Services, og metadata udtrækkes og tilføjes.
- Der tilføjes en indstilling, som giver dig mulighed for at oprette en udgiftsrapport, der indeholder afstemte ikke-tilknyttede kvitteringer.
- En indstilling, der tilføjes til udgiftsrapporter, giver dig mulighed for at oprette en udgiftslinje på grundlag af en kvittering eller forsøger at afstemme en eksisterende kvittering med en eksisterende udgiftslinje.

Du kan finde flere oplysninger om funktionen for nye udgiftsrapporter under [Nye udgiftsrapporter](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

**Bruger Microsoft mine data til sine modeller?**

Nej, Microsoft har udviklet en generel maskinel indlæringsmodel til sin tjeneste for behandling af kvitteringer. Denne model er ikke baseret på de kvitteringer, du overfører.

**Hvor er denne funktion tilgængelig og behandlet?**

USA understøttes i øjeblikket.

**Hvor forsvinder mine kvitteringer hen?**

Finance kontakter Cognitive Services for at udtrække feltdataene. Cognitive Services opbevarer en kopi af din kvittering i op til 24 timer, mens behandlingen pågår. Når behandlingen er fuldført, fjerner Cognitive Services kvitteringen. Kvitteringer gemmes stadig i Finance.

Du kan finde flere oplysninger under [Aktiver forståelse af kvitteringer med Form Recognizers nye funktion](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]