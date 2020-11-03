---
title: Konfigurer udgiftsstyring
description: I denne artikel beskrives de overvejelser og beslutninger, du skal foretage under planlægningsprocessen, før du konfigurerer udgiftsstyring i Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074320"
---
# <a name="configure-expense-management"></a>Konfigurer udgiftsstyring

[!include [banner](../includes/banner.md)]

Dette emne beskriver de overvejelser og beslutninger, du skal foretage under planlægningsprocessen, før du konfigurerer udgiftsstyring. I udgiftsstyring kan du gemme oplysninger om betalingsmetoder, rejserekvisitioner, udgiftsrapporter, politikker osv.

Da mange af de beslutninger, du foretager, når du planlægger din konfiguration af udgiftsstyring, er baseret på organisationens hierarki og økonomiske struktur, skal du referere til planlægningsdokumenterne for de pågældende områder.

## <a name="intercompany-expenses"></a>Interne udgifter

Når du aktiverer interne udgifter, giver du juridiske enheder og medarbejdere mulighed for at betale udgifter på vegne af en anden juridisk enhed og opkræve betaling fra den juridiske enhed i organisationen, hvor de er ansat. En medarbejder i den juridiske enhed A fuldfører f.eks. et projekt for den juridiske enhed B, og projektet har resulteret i rejserelaterede udgifter. Hvis interne udgifter er aktiveret, kan medarbejderen derefter arkivere en udgiftsrapport, der skal bogføre udgiften i den juridiske enhed B, og udgiften skal derefter betales af den juridiske enhed A. Hvis organisationen ikke har flere juridiske enheder, behøver du ikke at aktivere interne udgifter.

**Beslutning:** Vil du aktivere interne udgifter?

## <a name="financial-management"></a>Økonomistyring

Udgiftsstyring er tæt integreret med organisationens økonomiske styring. Mange af dine konfigurationer i udgiftsstyring er baseret på de beslutninger, du har træffet i relation til organisationens økonomi. I følgende afsnit beskrives de forskellige områder, der kræver planlægning og beslutninger, baseret på organisationens økonomiske beslutninger og vejledninger fra dit lederteam.

### <a name="per-diems"></a>Pr. dag

Du skal definere medarbejderens diæter, som organisationen kan tilbyde. Da diæter typisk bruges til at dække udgifter såsom måltider, logi og andre uforudsete udgifter, kan du oprette regler for de diætgodtgørelser, som organisationen tilbyder. diætsatser kan være baseret på tidspunktet for året, rejselokationen eller begge. Når du definerer en diætregel, kan du angive, at en procentdel af diætsatsen skal tilbageholdes, hvis en arbejder modtager gratis måltider eller servicer. Du kan også definere diætsatser med en nedre og øvre grænse for antallet af timer, hvor diætsatsen kan finde anvendelse på en arbejders rejse.

**Beslutninger:**

- Standarddiætregler for første og sidste dag:

    - Hvad er det mindste antal timer, en medarbejder har krav på på en dag og stadig modtage en diæt?
    - Sker der reduktion i det beløb, der tilbydes til måltider for den første dag og den sidste dag? Hvis der er en reduktion, hvad er procentdelen af reduktionen?
    - Sker der reduktion i det beløb, der tilbydes til hotelophold for den første dag og den sidste dag? Hvis der er en reduktion, hvad er procentdelen af reduktionen?
    - Sker der reduktion i det beløb, der tilbydes til andre udgifter, som er afholdt den første dag og den sidste dag? Hvis der er en reduktion, hvad er procentdelen af reduktionen?

- Standarddiætregler:

    - Er der en procentvis reduktion i diætgodtgørelsen for de enkelte måltider, hvis der f.eks. er et gratis måltid? Hvis der er en reduktion, hvad er procentdelen af reduktionen for hvert måltid?
    - Er reduktionen af måltid beregnet pr. dag, pr. rejse eller efter antallet af måltider pr. dag?
    - Skal diætbeløb afrundes på normal måde eller rundes op?
    - Beregnes diæter for en periode på 24 timer eller for en kalenderdag?

- Regler for diæter, der er baseret på placering:

    - Skal diætsatser variere afhængigt af lokationen? Hvilke lokationer inkluderes?
    - Hvis diæter varierer i forhold til lokation, skal du for hver lokation finde ud af, hvilket procentvist beløb der er angivet for følgende typer udgifter:

        - Måltider
        - Hotel
        - Andre udgifter

### <a name="expense-management-journals-and-accounts"></a>Kladder og konti til udgiftsstyring

Udgiftsstyring kræver, at du bruger flere kladder og konti. Du skal f.eks. beslutte, om den samme konto skal bruges til kontantforskud og uoverensstemmelser vedrørende kreditkort.

**Beslutninger:**

- Hvilken finanskladde er godkendte udgiftsrapporter bogført i?
- Hvilken konto bruges til kontantforskud?
- Skal kontantforskud bogføres omgående?

### <a name="payment-methods"></a>Betalingsmetoder

Når du giver medarbejdere mulighed for at afholde udgifter på vegne af din virksomhed, skal du definere de betalingsmetoder, som medarbejderne har lov til at bruge. Du kan f.eks. give medarbejdere mulighed for at bruge kontanter eller en virksomheds kreditkort. Du kan også give medarbejderne mulighed for at bruge personlige kreditkort og derefter refundere medarbejderne. Du skal træffe følgende beslutninger for hver betalingsmetode, du tillader.

**Beslutninger:**

- Hvilke betalingsmetoder er tilladt?
- Hvem ejer betalingsmetodeudgifterne?
- Er der en modkontotype? Hvis der er angivet en modkontotype, hvad er det så?
- Hvis der er angivet en modkonto, hvad er kontoen?
- Hvis betalingsmetoden er et kreditkort, skal betalingsmetoden kun bruges til importerede transaktioner?

### <a name="expense-categories-and-shared-categories"></a>Udgiftskategorier og delte kategorier

Når medarbejdere opretter en udgiftsrapport, skal hver enkelt udgift, de registrerer, være knyttet til en udgiftskategori. Udgiftskategorier afledes af delte kategorier, der kan deles på tværs af de juridiske enheder i organisationen. Disse kategorier kan også deles i Projektstyring og regnskab, afhængigt af den måde, som organisationen er defineret på. Afhængigt af definitionen af din organisation og vejledning fra implementeringsteamet skal du afgøre, om de kategorier, der bruges i udgiftsstyring, kun skal bruges i udgiftsstyring, eller om de skal deles mellem Projektstyring og regnskab og Udgiftsstyring. Bemærk, at disse kategorier kan deles mellem projekt og udgift eller projekt og produktion, men ikke mellem udgift og produktion. Du skal træffe følgende beslutninger for hver udgiftskategori.

**Beslutninger:**

- Hvad er udgiftskategorien? Som eksempel kan nævnes kategorier for fly, hotel eller kørsel.
- Kan udgiftskategorien også bruges i projektstyring og regnskab?
- Hvad er udgiftstypen?
- Hvad er standardbetalingsmetoden for udgiftskategorien?
- Skal udgifter i udgiftskategorien specificeres?
- Hvad er den primære standardkonto for udgiftskategorien?
- Hvad er standardvaremomsgruppen for udgiftskategorien?
- Er yderligere betalingsmetoder for udgiftskategorien tilladt? Hvis der er flere betalingsmetoder tilladt, hvad er de så?
- Er der underkategorier i denne udgiftskategori? I så fald skal du også træffer følgende beslutninger:

    - Er nogen af underkategorierne undtaget fra momsopkrævning?
    - Hvad er varemomsgruppen for underkategorierne?

Hvis udgiftsarten også bruges i Projektstyring og regnskab, skal du besvare de resterende spørgsmål. I modsat fald skal du gå til næste sektion.

- Hvilke omkostningskonti skal bruges til følgende udgifter?

    - Omkostning
    - Lønfordeling
    - Værdi af omkostningerne ved IGVA
    - Omkostningselement
    - Værdielement for omkostning ved IGVA
    - Periodiseret tab
    - Periodiseret tab for IGVA

- Hvilke omsætningskonti skal bruges til følgende?

    - Faktureret omsætning
    - Periodiseret omsætning - salgsværdi
    - IGVA - salgsværdi
    - Periodiseret omsætning - produktion
    - IGVA - produktion
    - Periodiseret omsætning - overskud
    - IGVA - overskud
    - Periodiseret omsætning - abonnement
    - IGVA - abonnement

### <a name="taxes"></a>Skatter

I forbindelse med udgiftsrelateret moms skal du angive, hvad der er medtaget eller aktiveret i udgiftsrapporter.

**Beslutninger:**

- Er moms inkluderet i udgiftsbeløbene?
- Skal momsopkrævning aktiveres for udgifter?

    > [!NOTE]
    > Når du planlægger finanskontoen, og såfremt du besluttede dig for at anvende de amerikanske regler for moms og importmoms, kan du ikke aktivere momsopkrævning for udgifter. (Hvis du vil anvende de amerikanske regler for moms og importmoms, skal du angive indstillingen **Anvend regler for momsbeskatning** til **Ja**.)

## <a name="policies"></a>Politikker

Ved at oprette politikker for udgiftsrapporter kan du hjælpe din organisation med at spare tid og penge, når medarbejderne afholder udgifter på dennes vegne. Politikker er med til at sikre, at medarbejdere holder sig indenfor budgettet, stiller alle påkrævede oplysninger til rådighed og kun bruger penge, når de har brug for det. Du skal træffe følgende beslutninger for hver udgiftsrapportpolitik og de enkelte politikker for godkendelse af udgiftsrapporter, som du opretter.

**Beslutninger:**

- Hvad er navnet på politikken?
- Hvad er udgiftspolitikken for?
- Hvis du tidligere har besluttet dig for at aktivere interne udgifter, hvilke virksomheder i organisationen, gælder denne politik så for?
- Hvornår træder politikken i kraft?
- Hvornår udløber politikken?
- Hvad er politikreglen?
- Hvad er udfaldet af politikreglen?
