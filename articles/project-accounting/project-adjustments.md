---
title: Projektjusteringer
description: Denne artikel indeholder oplysninger om projektjusteringer.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788294"
---
# <a name="project-adjustments"></a>Projektjusteringer

_**Gælder for:** Project Operations for lagerbaserede/produktionsbaserede scenarier_

## <a name="adjustments-overview"></a>Oversigt over justeringer

Du kan konfigurere Microsoft Dynamics 365 Project Operations, så brugere kan foretage ændringer af bogførte transaktioner. Du kan justere projekttransaktioner enkeltvist, eller du kan vælge flere transaktioner på én gang på en liste over alle projekttransaktioner. Projektjusteringer bruges f.eks. til masseopdatering af faktureringsstatus, genberegning af omkostninger efter en konfigurationsændring eller til opdatering af finansieringskilder.

Brugere kan få adgang til funktionaliteten for projektjusteringer på flere måder:

- Ved hjælp af siden **Juster transaktioner**, der kan åbnes fra **Projektstyring og regnskab** \> **Konfiguration**.
- Ved hjælp af knappen **Justering** på siden **Bogførte projekttransaktioner**, som du kan få adgang til fra **Projektstyring og regnskab** \> **Transaktioner**.
- Ved hjælp af knappen **Justering** på siden **Bogførte projekttransaktioner** i forbindelse med et projekt. Du kan få adgang til denne side fra **Projektstyring og regnskab** \> **Alle projekter**.

Hvis du vil gøre det muligt at foretage justeringer, skal du aktivere en eller flere transaktionsstatusser fra **Projektstyring og regnskab** \> **Parametre for Projektstyring og regnskab** under fanen **Generelt** i sektionen **Tillad justering af transaktionsstatus**. Af eksempler på transaktionsstatusser kan nævnes bogførte transaktioner, fakturerede transaktioner eller fjernede transaktioner. Alle transaktionsstatusser, der angives til **Nej**, har transaktioner i den pågældende status, der ikke vises i justeringsprocessen som transaktioner, der kan vælges til justering.

En konfigurationsindstilling med navnet **Opret altid justeringstransaktion**, findes i øjeblikket i parametrene for Projektstyring og regnskab. Du kan deaktivere denne indstilling for at opdatere den oprindelige transaktion i stedet for at oprette nye transaktioner, når du skal justere et undersæt af scenarier. Det er blevet meddelt, at denne parameter udfases den 1. marts 2023. Efter 1. marts 2023 fungerer systemet altid, som om indstillingen er aktiveret.

## <a name="adjustments-process-flow"></a>Justeringsprocesflow

I nedenstående trin vises det typiske flow til behandling af justeringer.

1. Åbn siden **Projektjusteringer** .
2. Vælg **Vælg** for at søge efter transaktioner, der opfylder de forventede kriterier for justering.
3. Vælg alle transaktioner eller et delsæt af transaktionerne, som skal justeres, på listen over transaktioner.
4. Vælg **Juster**, og rediger attributterne på linjen. Hvis værdierne blev angivet manuelt under indtastning af transaktionen, kan du også vælge at angive standardsystemværdier.
5. Listen over transaktioner returneres, og der vises en markering i kolonnen **Ventende justering** for at angive, hvor ændringerne blev foretaget. Justeringer, der har ventende ændringer, vises i nederste halvdel af siden. Der kan du foretage flere detaljerede ændringer, ud over hvad der blev vist på den forrige side.
6. Vælg **Bogfør** for at bogføre justeringstransaktionerne.

Afhængigt af konfigurationen oprettes nye transaktioner typisk med henblik på justering.

- Feltet **Fakturastatus** for den oprindelige transaktion angives til **Justeret**.
- Der oprettes en tilbageførselstransaktion for at tilbageføre den oprindelige transaktion om, og feltet **Status** angives til **Justeret**.
- Der oprettes en ny transaktion, som indeholder de ændringer, der blev foretaget under justeringsprocessen.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Vælge flere bogførte projekttransaktioner ad gangen til justeringer og kreditnotaer

En ny funktion, der blev introduceret i 10.0.30-versionen, gør det muligt at vælge flere transaktioner, der justeres på én gang, på siden **Bogførte projekttransaktioner**.

Før du kan bruge denne funktion, skal den aktiveres i dit system. Administratorer kan bruge arbejdsområdet **Funktionsstyring** til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet til **Funktionsstyring** skal du søge efter og **Vælg flere bogførte projekttransaktioner til justeringer og kreditnoter** og derefter vælge **Aktivér nu**.

Denne funktion aktiverer følgende vigtige funktioner:

- Du kan få adgang til den fra siden med bogførte transaktioner i et projekt ved hjælp af knappen **Justering**.
- Derved aktiveres et kontrolelement til valg af flere rækker på siden **Bogførte projekttransaktioner**. Du kan anvende filtre på listesiden og vælge posterne, før du begynder at justere dem.
- Knappen **Justering** deaktiveres, hvis en enkelt transaktion ikke kan justeres, eller hvis du vælger en kombination af kreditnoter og kladder samlet i stedet for enkeltvis.
- På grund af tilføjelsen af kontrolelementet til valg af flere rækker er linket **Bundne omkostninger** på båndet ikke længere deaktiveret, hvis der er valgt flere rækker.
- Der tilføjes følgende advarsel: "Du har valgt flere poster end (det valgte antal) til justering. Det kan tage et stykke tid at udføre denne handling. Er du sikker på, at du vil fortsætte med denne handling?"

Denne funktion fjerner også trin 2 fra det procesflow, der blev beskrevet tidligere i denne artikel. Alle de transaktioner, der blev valgt, før siden **Juster transaktioner** blev åbnet, medtages derfor på listen over transaktioner, der kan justeres. Du behøver ikke at bruge knappen **Vælg** til at søge efter dem.

> [!NOTE] 
> Selvom denne funktion er deaktiveret, kan du stadig vælge flere poster, så de kan justeres. Men der er kun én post, der *forbliver markeret*, og dialogboksen **Vælg transaktioner** vises umiddelbart efter, du har valgt at åbne justeringer.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Statusser for justeringstransaktioner, der kan aktiveres eller deaktiveres for justeringer

Følgende statusser kan aktiveres eller deaktiveres under fanen **Generelt** på siden **Parametre for Projektstyring og regnskab**:

- Sendt
- Fakturaforslag
- Faktureret
- Estimeret
- Fjernet
- Startsaldo (time)

## <a name="adjustment-parameters"></a>Justeringsparametre

Disse parametre er angivet på siden **Parametre for Projektstyring og regnskab** under fanen **Generelt** i gruppen **Justering** og ændrer funktionsmåden for, hvordan justeringer behandles. 

| Parameternavn | Description |
|----------------|-------------
| Opret altid en justeringstransaktion | Hvis denne parameter er aktiveret, vil justeringsprocessen altid oprette en ny tilbageførselstransaktion og en ny justeret transaktion, når det har indflydelse på økonomi eller rapportering. Hvis parameteren er deaktiveret, opdaterer justeringsprocessen den oprindelige transaktion i stedet for at oprette en tilbageførselstransaktion for et scenarie, f.eks. en opdatering af transaktionsteksten. |
| Opdater felt automatisk | Hvis denne parameter er aktiveret, genberegnes kostpris og salgspris i systemet. |
| Brug justeringsdatoen som et nyt projekt | Denne parameter bruges til at flytte transaktioner til en fremtidig regnskabsperiode, før systemet understøttede denne funktion. Det anbefales ikke, at du bruger den, da den ændrer forretningsdatoen for transaktionen, og den udfases derfor i en fremtidig version. |
| Tillad lukkede aktiviteter | Normalt kan der ikke oprettes transaktioner for lukkede aktiviteter. Hvis denne parameter er aktiveret, tilsidesættes den pågældende funktionsmåde. Der kan derfor oprettes justeringer for lukkede aktiviteter. |
