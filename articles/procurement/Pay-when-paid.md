---
title: Betal ved betaling for betalinger til leverandører
description: I dette emne forklares, hvordan du kan bruge scenariet for betal når betalt (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525331"
---
# <a name="pay-when-paid-vendor-payments"></a>Betal ved betaling for betalinger til leverandører

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

I dette emne forklares, hvordan du kan bruge scenariet for betal når betalt (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Oprette en købsordre, der har PWP-vilkår

Når du bogfører en faktura fra en leverandør, og leverandøren er underlagt PWP-vilkår, vises disse vilkår på linjerne i PO'en for indkøbsordren. Benyt følgende fremgangsmåde for at oprette en PO med PWP-vilkår.

1. I Microsoft Dynamics 365 Finance skal du udføre disse trin:

    - Gå til **Indkøb og forsyning** \> **Indkøbsordrer** \> **Alle indkøbsordrer**. Vælg **Ny** i handlingsruden. Vælg den leverandør, som PWP-vilkårene er konfigureret for i projektet, i dialogboksen **Opret købsordre**, angiv andre nødvendige oplysninger, og vælg derefter **OK**.
    - Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**. Vælg fanen **Administrer** i handlingsruden, og vælg derefter **Vareopgave**. Vælg indkøbsordren. Vælg den leverandør, som PWP-vilkår er konfigureret for i projektet, og vælg derefter **OK**.

2. Vælg **Tilføj linje** i oversigtspanelet **Indkøbsordrelinjer** på siden **Indkøbsordre** for at oprette en indkøbsordrelinje.
3. Vælg varenummeret eller indkøbskategorien, og angiv de øvrige nødvendige oplysninger. Gennemse detaljerne på indkøbsordrelinjen for leverandøren.

    Indstillingen **Betal ved betaling** vælges automatisk, og værdien i feltet **Tærskelprocent for PWP** kopieres automatisk fra feltet **Tærskelprocent for PWP** på siden **Projekter**.

4. Hvis du ikke vil anvende Betal ved betaling-betingelser for leverandøren for en indkøbsordrelinje, skal du fjerne markeringen i indstillingen **Betal ved betaling**. I dette tilfælde nulstilles feltet **Tærskelprocent for PWP** for indkøbsordrelinjen til **0** (nul).
5. Gå til handlingsruden på siden **Indkøbsordre**, og vælg **Bekræft** under fanen **Køb** for at bekræfte indkøbsordren.
6. I handlingsruden under fanen **Faktura** skal du vælge **Faktura** for at oprette fakturaen for indkøbsordren.

## <a name="create-a-project-invoice-proposal"></a>Oprette et projektfakturaforslag

Projektfakturaforslag bruges til at oprette projektfakturaer for kunden. I PWP-scenariet afhænger leverandørbetalinger af kundebetalinger i henhold til indstillingerne for PWP. Der er dog indstillinger, som du kan bruge til at frigive betalingerne uden kundebetalinger efter behov. Hvis du vil oprette en projektfaktura for kunden, skal du følge disse trin.

1. I apps for kundeengagement skal du gå til **Projekt** \> **Projekter** og vælge projektet.
2. Under fanen **Faktiske** skal du vælge den faktiske linje, der er genereret af den indkøbsordre, som har transaktionstypen **Ikke-faktureret salg**. Vælg derefter **Klar til fakturering**.
3. Gå til **Salg** \> **Salg** \> **Projektkontrakt**, og vælg projektkontrakten.
4. I handlingsruden skal du vælge **Faktura** for at oprette kundefakturaen.
5. I Finance skal du gå til **Projektstyring og regnskab** \> **Periodisk** \> **Importér fra den midlertidige tabel** og vælge **OK** for at oprette Project Operations-integrationskladden.
6. Gå til **Projektstyring og regnskab** \> **Projektfaktura** \> **Projektfakturaforslag**, og vælg **Bogfør** for at bogføre det fakturaforslag, der blev genereret for projektet.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Opdater en kundebetaling og betal leverandøren

Når en leverandør er færdig med at arbejde på et projekt og sender dig en faktura, skal du gennemgå projektstatus og kundefakturaer for at afgøre, om PWP-vilkårene er opfyldt for projektet. Hvis PWP-vilkårene for leverandøren er opfyldt, kan du bestemme, hvilke linjer på leverandørfakturaen du vil betale, baseret på kundens betalinger for projektet. Hvis du beslutter dig for at betale leverandøren, selvom PWP-vilkårene ikke er opfyldt, kan du tilsidesætte disse på siden **Leverandørfaktura med betal ved betaling**.

1. I Finance skal du gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter** og vælge projektet.
2. Vælg **Kontrol** i handlingsruden, og vælg derefter **Leverandørfakturaer** for at få vist alle de leverandørfakturaer, der er oprettet for projektet.
3. På siden **Leverandørfakturaer med betal ved betaling** skal du i søgefeltet angive værdier for at finde den leverandørfaktura, som du vil gennemse, og derefter vælge **Søg**.
4. Vælg indstillingen **Betal ved betaling** for kun at få vist PWP-fakturaer.
5. I oversigtspanelet **Leverandørfakturalinjer** skal du markere de linjer, som du vil frigøre til betaling.
6. Vælg **Frigiv leverandørbetaling**. Markeringen i **Betal ved betaling** fjernes, og værdien i feltet **Klar til betaling** ændres til **Ja**.
