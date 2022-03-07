---
title: Konfigurer udgiftskategorier
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere udgiftskategorier og delte kategorier for udgiftsrapporter.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8f5b1a5d069b8d73051406369ecba2c4547eaa38e0d5bde2e34f52c5b7b724bd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993099"
---
# <a name="set-up-expense-categories"></a>Konfigurer udgiftskategorier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når medarbejdere opretter udgiftsrapporter, skal hver enkelt udgift, de registrerer, være knyttet til en udgiftskategori. Udgiftskategorier afledes af delte kategorier, der kan deles på tværs af de juridiske enheder i organisationen. Afhængigt af, hvordan organisationen er defineret, kan disse udgiftskategorier også deles i andre områder. Afhængigt af definitionen af din organisation og vejledning fra implementeringsteamet skal du afgøre, om de kategorier, der bruges i udgiftsstyring, kun skal bruges i udgiftsstyring eller skal deles i andre områder.

> [!NOTE]
> Disse kategorier kan deles mellem projektstyring og regnskab samt udgiftsstyring eller mellem projektstyring og regnskab og produktion. De kan dog ikke deles mellem udgiftsstyring og produktion.

Før du kan gå i gang med konfigurationsprocessen, skal der træffes følgende beslutninger for de enkelte udgiftskategorier:

- Hvad er udgiftskategorien? Som eksempel kan nævnes kategorier for fly, hotel eller kørsel.
- Kan udgiftskategorien også bruges i projektstyring og regnskab? Det kan den, hvis du også træffer følgende beslutninger:

    - Hvilke omkostningskonti skal bruges til følgende udgifter?

        - Omkostning
        - Lønfordeling
        - Værdi af omkostningerne ved IGVA
        - Omkostningselement
        - Værdielement for omkostning ved IGVA
        - Periodiseret tab
        - Periodiseret tab for IGVA

    - Hvilke omsætningskonti skal der bruges til følgende omsætningskilder?

        - Faktureret omsætning
        - Periodiseret omsætning - salgsværdi
        - IGVA - salgsværdi
        - Periodiseret omsætning - produktion
        - IGVA - produktion
        - Periodiseret omsætning - overskud
        - IGVA - overskud
        - Periodiseret omsætning - abonnement
        - IGVA - abonnement

- Hvad er udgiftstypen?
- Hvad er standardbetalingsmetoden for udgiftskategorien?
- Skal udgifter i udgiftskategorien specificeres?
- Hvad er den primære standardkonto for udgiftskategorien?
- Hvad er standardvaremomsgruppen for udgiftskategorien?
- Er yderligere betalingsmetoder for udgiftskategorien tilladt? Hvis det er tilfældet, hvilke?
- Er der underkategorier i denne udgiftskategori? I så fald skal du også træffer følgende beslutninger:

    - Er nogen af underkategorierne undtaget fra momsopkrævning?
    - Hvad er varemomsgruppen for underkategorierne?


[!INCLUDE[footer-include](../includes/footer-banner.md)]