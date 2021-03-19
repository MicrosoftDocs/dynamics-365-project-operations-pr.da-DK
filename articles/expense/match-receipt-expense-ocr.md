---
title: Hent en kvittering ved hjælp af optisk tegngenkendelse
description: Dette emne indeholder oplysninger om behandling af kvitteringer ved hjælp af optisk tegngenkendelse (OCR).
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499844"
---
# <a name="capture-a-receipt-using-ocr"></a>Hent en kvittering ved hjælp af optisk tegngenkendelse

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Udgiftsposten er blevet forbedret via introduktionen af behandling af kvitteringer ved hjælp af optisk tegngenkendelse (OCR). Denne funktionalitet er udviklet til at forbedre brugeroplevelsen ved oprettelse af udgiftsrapporter.

## <a name="key-features"></a>Nøglefunktioner

- I systemet udtrækkes forhandlernavnet, datoen og det samlede beløb fra kvitteringer.
- Systemet forsøger at sammenligne ikke-tilknyttede kvitteringer med ikke-tilknyttede udgiftstransaktioner.
- Du kan oprette manuelt indtastede udgiftstransaktioner på grundlag af kvitteringer.

## <a name="attach-receipts-to-an-expense-report"></a>Vedhæft kvitteringer til en udgiftsrapport

Hvis du automatisk vil vedhæfte kvitteringer, der omfatter kreditkorttransaktioner, når en udgiftsrapport oprettes, skal du benytte følgende fremgangsmåde.

  1. Åbn arbejdsområdet **Udgiftsstyring**.
  2. På fanen **Kvitteringer** skal du kontrollere, at der findes ikke-tilknyttede kvitteringer. Du kan også overføre kvitteringer under fanen **Kvitteringer**.
  3. På fanen **Udgifter** skal du kontrollere, at der findes ikke-tilknyttede udgifter. Udgiftsadministratoren importerer typisk disse udgifter fra kreditkortudbyderen.
  4. Vælg **Ny udgiftsrapport**. Bemærk, at du nu også kan inkludere udgifter og kvitteringer, når du opretter en udgiftsrapport. Hvis du tilføjer både udgifter og kvitteringer, udløses automatisk afstemning af kvitteringer i forhold til udgifterne.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Opret eller afstem kvitteringer til en udgiftsrapport
Hvis du vil oprette en udgift eller afstemme en udgift fra en kvittering, skal du udføre følgende trin.

  1. På en udgiftsrapport skal du på fanen **Kvitteringer** tilknytte en kvittering ved at vælge **Tilføj kvitteringer**.
  2. Læg mærke til indstillingerne **Opret** og **Afstem** under det overførte billede af kvitteringen.

      - Vælg **Opret** for at oprette en manuelt angivet udgiftstransaktioner, og angiv de værdier, der er udtrukket fra kvitteringen.
      - Hvis du vælger **Afstem**, vil systemet forsøge at afstemme en eksisterende udgift med kvitteringen.

## <a name="installation"></a>Installation

Hvis du vil bruge disse avancerede udgiftsfunktioner, skal du installere tilføjelsesprogrammet til tjenesten for udgiftsstyring i Microsoft Dynamics 365 Finance og aktivere funktionerne i din forekomst. Du kan få adgang til tilføjelsesprogrammet fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).

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

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

**Bruger Microsoft mine data til sine modeller?**

Nej, Microsoft har udviklet en generel maskinel indlæringsmodel til sin tjeneste for behandling af kvitteringer. Denne model er ikke baseret på de kvitteringer, du overfører.

**Hvor er denne funktion tilgængelig og behandlet?**

USA understøttes i øjeblikket.

**Hvor forsvinder mine kvitteringer hen?**

Finance kontakter Cognitive Services for at udtrække feltdataene. Cognitive Services opbevarer en kopi af din kvittering i op til 24 timer, mens behandlingen pågår. Når behandlingen er fuldført, fjerner Cognitive Services kvitteringen. Kvitteringer gemmes stadig i Finance.

Du kan finde flere oplysninger under [Aktiver forståelse af kvitteringer med Form Recognizers nye funktion](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
