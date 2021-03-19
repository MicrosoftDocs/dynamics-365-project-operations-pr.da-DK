---
title: Opret en fakturaplan på en projektbaseret kontraktlinje
description: Dette emne indeholder oplysninger om, hvordan du opretter fakturaplaner og milepæle på kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0da3b3f8f14ecf9a4c4f057cd26c0ca9eb5ec2f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278231"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Opret en fakturaplan på en projektbaseret kontraktlinje 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Du kan oprette en fakturaplan på en projektbaseret kontraktlinje. Fakturering er kun tilladt, når kontrakten er vundet, og du opretter en projektkontrakt. Ved hjælp af en fakturatidsplan kan der automatisk oprettes kladdefakturaer for en projektbaseret kontraktlinje. Hvis du dog kun opretter fakturaer manuelt, kan du springe over oprettelse af fakturaplaner på kontraktlinjer.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Opret en plan for fakturering af tid og materialer for en kontraktlinje

Når en projektbaseret kontraktlinje har faktureringsmetoden tid og materialer, kan du oprette en datobaseret fakturaplan. Hvis du automatisk vil oprette en datobaseret fakturaplan, skal du udføre følgende trin.

1. Gå til **Indstillinger** > **Fakturafrekvenser**, og konfigurer en fakturafrekvens.
2. Gå til projektkontraktposten, og vælg en dato på fanen **Opsummering** i feltet **Ønsket leveringsdato**.
3. Åbn kontraktlinjen **Tid og materialer**, som du opretter en datobaseret fakturaplan for. 
4. På fanen **Fakturaplan** skal du vælge startdatoen og fakturafrekvensen for faktureringen.
5. Vælg **Generér fakturaplan** i undergitteret. Fakturaplanen genereres med felterne **Kørselsdato for faktura**, **Skæringsdato for transaktion** og **Status for kørsel** angivet på følgende måde:

    - **Kørselsdato for faktura**: Denne dato er dikteret af fakturafrekvensen.
    - **Skæringsdatoen for transaktionen**: Dagen før fakturaens kørselsdato.
    - **Status for kørsel**: Angives automatisk til **Ikke kørt**. Når jobbet for automatisk oprettelse af en faktura køres for en bestemt kørselsdato for faktura, opdateres feltet til **Kørsel gennemført** eller **Kørsel mislykket**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Opret en plan for fakturering af fast pris for en kontraktlinje

Når kontraktlinjen har en fast faktureringsmetode, kan du oprette en milepælsbaseret fakturaplan. 

> [!NOTE]
> Der kan ikke oprettes milepæle på en kontraktlinje, hvis der ikke er knyttet et projekt til kontraktlinjen.

Benyt følgende fremgangsmåde for at oprette en milepælsbaseret fakturaplan for et fast sæt ligeligt fordelte milepæle i kalenderperioden.

1. Gå til **Indstillinger** > **Fakturafrekvenser**, og konfigurer en fakturafrekvens.
2. Gå til projektkontraktposten, og vælg en dato på fanen **Opsummering** i feltet **Ønsket leveringsdato**.
3. Åbn kontraktlinjen **Fast pris**, som du opretter milepælsplanen for. På fanen **Faktureringsmilepæl** skal du vælge startdatoen og fakturafrekvensen for faktureringen. 
4. Vælg **Generér periodiske milepæle** i undergitteret. Der oprettes en fakturaplan med felter indeholdende **Navnet på milepælen**, **Datoen for milepælen** og **Milepælsbeløbene** på følgende måde:

    - **Milepælsnavn**: Dette navn er dikteret af fakturafrekvensen.
    - **Datoen for milepælen**: Denne dato er dikteret af fakturafrekvensen.
    - **Milepælsbeløbet**: Dette beløb beregnes ved at dividere kontraktbeløbet på kontraktlinjen med antallet af milepæle, som er dikteret af frekvensen, startdatoen for fakturering samt de ønskede leveringsdatoer.

    Hvis der er angivet en værdi i feltet **Estimeret momsbeløb** i kontraktlinjen, fordeles dette felt også til hver milepæl ligeligt, når der genereres periodiske milepæle.

Faktureringsmilepæle bør være lig med kontraktlinjens kontraktværdi. Hvis de ikke er det, får du vist en fejl på siden **Kontraktlinje**. Du kan rette fejlen ved at kontrollere, at faktureringsmilepælene samlet set beløber sig til den kontraktmæssige værdi af linjen ved at oprette, redigere eller slette milepæle. Opdater siden, når du har foretaget ændringerne, for at fjerne fejlen.

### <a name="manually-create-milestones"></a>Opret milepæle manuelt

Du kan generere milepæle for fast pris manuelt, når de ikke er periodisk opdelt. Benyt følgende fremgangsmåde for manuelt at oprette en ny milepæl.

1. Åbn kontraktlinjen med fast pris, som du er ved at oprette en milepæl for, og vælg i undergitteret på fanen **Fakturaplan** **+ Opret en ny kontraktlinjemilepæl**. 
2. På siden **Opret milepæl** skal du angive de påkrævede oplysninger, der er baseret på følgende tabel.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| Navn på milepæl | Hurtig oprettelse | Tekstfelt for navnet på milepælen. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |
| Projektopgave | Hurtig oprettelse | Hvis milepælen er knyttet til en projektopgave, kan denne reference anvendes til at tilføje en brugerdefineret logik ved at angive status for milepælen på baggrund af opgavestatus. | Programmet har ingen afledt virkning for denne reference til en opgave. |
| Milepælsdato | Hurtig oprettelse | Angiv den dato, hvor processen til automatisk oprettelse af fakturaer skal holde øje med statussen for denne milepæl for at tage den i betragtning til fakturering. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |
| Fakturastatus | Hurtig oprettelse | Når der oprettes en milepæl, angives denne status altid til **Ikke klar til fakturering** eller **Ikke påbegyndt**. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |
| Linjebeløb | Hurtig oprettelse | Beløb eller værdi for den milepæl, der vil blive faktureret kunden. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |
| Moms | Hurtig oprettelse | Det momsbeløb, der anvendes på milepælen. | Dette overføres til milepælen på projektkontraktlinjen og til fakturaen. |

3. Vælg **Gem og luk**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]