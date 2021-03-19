---
title: Konfigurer og anvend betal ved betaling for betalinger til leverandører
description: I dette emne forklares det, hvordan du kan oprette vilkår for betal ved betaling ("PWP"), så du kan frigive delvise leverandørbetalinger på grundlag af kundebetalinger.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f2469c8396eb4867b435f70b046aa421552d0fa1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288582"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Konfigurer og anvend betal ved betaling for betalinger til leverandører

[!include [banner](../includes/banner.md)]

Når du godkender, at en leverandør skal arbejde som underleverandør, kan det være en god ide at tilbageholde betaling til leverandøren, indtil kunden betaler dig for projektet. For at understøtte dette scenario kan du konfigurere vilkår for betal ved betaling (PWP), når du konfigurerer indkøbsordren (PO) med en leverandør.

Når en kunde f.eks. betaler et beløb på en projektfaktura, kan du frigive dele af eller hele beløbet på leverandørfakturaen. Du kan nøjes med at konfigurer vilkår for PWP, som angiver, at leverandøren skal betales, når du har modtaget en procentdel af den pågældende betaling fra kunden. Hvis du modtager en delbetaling fra en kunde, kan du manuelt frigive nogle af de relaterede leverandørfakturaer til betaling.

I følgende eksempel beskrives processen for anvendelse af PWP-vilkår.

## <a name="example"></a>Eksempel

Din organisation indgår en aftale om at levere 100 computere til kunden, hvor softwaren er installeret, til en pris på 150,00 amerikanske dollar (USD) pr. computer. Du skal derefter ansætte en leverandør til at levere de computere, hvor software er installeret på. Ifølge aftalen skal kunden godkende kvaliteten af computerne, før din organisation modtager betaling. Din organisations politik er at tilbageholde betaling til leverandører, indtil kunden har betalt dig. Du skal derfor konfigurere projektet, så det har en PWP-procent på 100 procent.

Leverandøren sender dig de 100 computere, hvor software er installeret på, sammen med en faktura på 10.000,00 USD. Da PWP-vilkårene for projektet er konfigureret, betaler du ikke leverandøren ved modtagelsen af computerne. Du sender i stedet computerne til kunden sammen med en faktura på 15.000,00. Kunden undersøger computerne og godkender det fulde beløb på projektfakturaen.

Når du har modtaget den fulde betaling fra kunden, skal du betale leverandøren 10.000,00, som er det fulde beløb på leverandørfakturaen.

## <a name="set-up-pwp-terms-for-a-project"></a>Konfigurer PWP-vilkår for et projekt

Når du konfigurerer PWP-vilkår for for et projekt, skal du i procent angive det minimumbeløb, som en kunde skal betale dig for projektet, inden du betaler leverandøren. Tærskelbeløbet beregnes automatisk på kundefakturaerne for projektet. Benyt følgende fremgangsmåde for at konfigurere tærskelprocenten for PWP-vilkår.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.
2. Find og åbn det projekt, som du vil konfigurere PWP-vilkår for.
3. I oversigtspanelet **Leverandøraftaler** skal du vælge **Tilføj linje**.
3. I feltet **Kontokode** skal du vælge en af følgende indstillinger:

    - **Tabel** – PWP-vilkårene gælder for en enkelt leverandør.
    - **Gruppe** – PWP-vilkårene gælder for alle leverandører i en leverandørgruppe.
    - **Alle** – PWP-vilkårene gælder for alle leverandører.

4. Hvis du har valgt **Tabel** eller **Gruppe** i forrige trin, skal du i feltet **Leverandør/leverandørgruppe** vælge den leverandør eller leverandørgruppe, som PWP-vilkårene gælder for. Hvis du har valgt **Alle** i det foregående trin, kan feltet **Leverandør/leverandørgruppe** ikke redigeres.
5. Hvis der er konfigureret betingelser for tilbageholdelse af leverandørbetaling i projektet, skal du i feltet **Betingelser for tilbageholdelse af leverandørbetaling** vælge regel-id'et for tilbageholdelsesbetingelserne.
6. I feltet **Tærskelprocent for PWP** skal du angive tærskelprocenten for projektet. Den procent, som du angiver for projektet, definerer det minimumbeløb, som kunden skal betale dig, inden du betaler leverandøren.

## <a name="create-a-po-that-has-pwp-terms"></a>Opret en PO, der indeholder vilkår for PWP

Når du bogfører en faktura fra en leverandør, og leverandøren er omfattet af PWP-vilkår, vises disse vilkår på linjerne i PO'en. Benyt følgende fremgangsmåde for at oprette en PO med PWP-vilkår.

1. Gå til **Indkøb og forsyning** \> **Indkøbsordrer** \> **Alle indkøbsordrer**.
2. Vælg **Ny** i handlingsruden. Angive derefter i dialogboksen **Opret indkøbsordre** de nødvendige oplysninger, og vælg **OK**.

    Du kan også åbne en eksisterende PO på listesiden **Alle indkøbsordrer**.

4. På siden **Indkøbsordre** skal du i oversigtspanelet **Indkøbsordrelinjer** gennemse oplysningerne om indkøbsordrelinjen for leverandøren. Indstillingen **Betal ved betaling** vælges automatisk, og værdien i feltet **Tærskelprocent for PWP** kopieres automatisk fra feltet **Tærskelprocent for PWP** på siden **Projekter**.
6. Hvis du ikke vil anvende Betal ved betaling-betingelser for leverandøren for en indkøbsordrelinje, skal du fjerne markeringen i indstillingen **Betal ved betaling**. I dette tilfælde nulstilles feltet **Tærskelprocent for PWP** for indkøbsordrelinjen til 0 (nul).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Opdater en kundebetaling og betal leverandøren

Når en leverandør er færdig med at arbejde på et projekt og sender dig en faktura, skal du gennemgå projektstatus og kundefakturaer for at afgøre, om PWP-vilkårene er opfyldt for projektet. Hvis PWP-vilkårene for leverandøren er opfyldt, kan du bestemme, hvilke linjer på leverandørfakturaen du vil betale, baseret på kundens betalinger for projektet. Hvis du beslutter dig for at betale leverandøren, selvom PWP-vilkårene ikke er opfyldt, kan du tilsidesætte disse på siden **Leverandørfaktura med betal ved betaling**.

1. Gå til **Projektstyring og regnskab** \> **Forespørgsler og rapporter** \> **Tilbageholdelsesforespørgsler** \> **Leverandørfaktura med betal ved betaling**.
2. På siden **Leverandørfakturaer med betal ved betaling** skal du i søgefeltet angive værdier for at finde den leverandørfaktura, som du vil gennemse, og derefter vælge **Søg**.
3. I oversigtspanelet **Leverandørfakturalinjer** skal du markere de linjer, som du vil ændre.
4. Hvis vilkårene for **Betal ved betaling** er opfyldt for fakturalinjen, skal du vælge **Frigiv leverandørbetaling**. Markeringen i **Betal ved betaling** fjernes, og værdien i feltet **Klar til betaling** ændres til **Ja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]