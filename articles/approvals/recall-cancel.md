---
title: Tilbagekaldelse af tidligere godkendte registreringer
description: I denne artikel forklares det, hvordan et medlem af et projektteam kan anmode om at få vist tilbagekaldt tidligere indsendte og godkendte tids-, udgifts- og materialeforbrugsposter, og hvordan en projektleder kan godkende eller afvise forespørgsler om tilbagekaldelse.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930357"
---
# <a name="recall-previously-approved-entries"></a>Tilbagekaldelse af tidligere godkendte registreringer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Et medlem af et projektteam, der indsender en tids-, udgifts- eller materialeforbrugspost, kan tilbagekalde denne post, efter at den er godkendt. Processen for tilbagekaldelse består af to primære trin:

1. En afsender anmoder om en tilbagekaldelse.
2. En godkender skal godkende tilbagekaldelsesanmodningen.

## <a name="request-a-recall"></a>Anmodning om tilbagekaldelse

Følg disse trin for at anmode om tilbagekaldelse af en godkendt tids-, udgifts- eller materialeforbrugspost.

1. Afhængigt af den posttype, du vil tilbagekalde, skal du følge et af disse trin:

    - Ved tidsposter skal du gå til **Projekter** \> **Mit arbejde** \> **Tidsregistrering** og vælge alle tidsposterne for en bestemt kombination af et projekt og en opgave. Du kan også vælge de enkelte celler for tid på en bestemt dato i forbindelse med et bestemt projekt i gitteret.
    - I forbindelse med udgiftsposter skal du gå til **Projekter** \> **Mit arbejde** \> **Udgifter** og vælge rækken for udgiftsposten, som du vil tilbagekalde.
    - I forbindelse med materialeforbrug skal du gå til **Projekter** \> **Mit arbejde** \> **Logfil for materialeforbrug** og vælge rækken for materialeforbrug, som du vil tilbagekalde.

2. Vælg **Tilbagekalde**. En bekræftelsesdialogboks åbnes. Hvis de valgte tids-, udgifts eller materialeforbrugsposter allerede er godkendt, bliver du bedt om at angive en årsag til tilbagekaldelsen.
3. Angiv en årsag til tilbagekaldelsen, og vælg derefter **OK** for at bekræfte handlingen. Systemet sender den person, som godkendte posterne, en anmodning om at godkende tilbagekaldelsen.

> [!IMPORTANT]
> Du kan ikke oprette en anmodning om tilbagekaldelse af en godkendt tids-, udgifts- eller materialeforbrugspost, der allerede er faktureret til kunden. Hvis du forsøger, modtager du en meddelelse, som fastslår, at tids-, udgifts- eller materialeforbrugsposten ikke kan tilbagekaldes, fordi den allerede er faktureret. I dette tilfælde kan du kun anmode om at tilbagekalde posten, hvis en korrektionsfaktura anvendes til at udstede en fuld kredit eller refundering til kunden på den oprindelige faktura.

## <a name="approve-or-reject-a-recall-request"></a>Godkende eller afvise en anmodning om tilbagekaldelse

Følg disse trin for at godkende eller afvise en anmodning om tilbagekaldelse.

1. Gå til **Projekter** \> **Mit arbejde** \> **Godkendelser**.
2. Skift visningen til **Tilbagekald anmodninger om godkendelse** på listesiden **Godkendelser**. Der vises en liste over sendte anmodninger om tilbagekaldelser.
3. Vælg en eller flere poster, og vælg derefter enten **Godkend** eller **Afvis**.
4. Hvis du har valgt **Godkend**, modtager du en advarsel, der forklarer, hvordan godkendelsen virker. Vælg **OK** for at bekræfte handlingen. Anmodningen om tilbagekaldelse er godkendt

    eller

    Hvis du har valgt **Afvis**, afvises anmodningen om tilbagekaldelse.

> [!IMPORTANT]
> Når en tilbagekaldelse er godkendt, lige som tilfældet er med anmodningen, kontrollere systemet eventuelle faktureringsaktiviteter for tids-, udgifts- og materialeforbrugsposter. Hvis en post allerede er faktureret, eller hvis den er på en kladdefaktura, modtager godkenderen en fejlmeddelelse, der angiver, at tiden eller udgiften ikke kan godkendes til tilbagekaldelse, da den allerede er blevet faktureret. I dette tilfælde kan godkenderen kun godkende tilbagekaldelsen, hvis en korrektionsfaktura anvendes til at udstede en fuld kredit eller refundering til kunden på den oprindelige faktura.

## <a name="impact-of-a-recall-request"></a>Virkning af en anmodning om tilbagekaldelse

Når en godkendelse tilbagekaldes, har det både driftsmæssige og økonomiske konsekvenser.

### <a name="operational-impact"></a>Driftsmæssig konsekvens

Hvis en anmodning om tilbagekaldelse godkendes, markeres godkendelsesposten som **Afvist**. Postens status ændres til enten **Returneret** eller **Afvist**, afhængigt af om det er en tidsregistrering eller en udgift- eller materialeforbrugspost.

Projektteammedlemmet kan få vist poster, redigere og derefter sende poster igen eller fuldstændigt slette posterne.

Hvis en anmodning om tilbagekaldelse afvises, forbliver statussen for posten **Godkendt**, og posten kan ikke redigeres af projektteammedlemmet eller godkenderen for projektet.

### <a name="financial-impact"></a>Økonomisk konsekvens

Hvis en tilbagekaldelse godkendes, opdateres de tilsvarende faktiske værdier for omkostninger og salg på følgende måde:

- Feltet **Justeringsstatus** opdateres til **Justeret**.
- Feltet **Faktureringsstatus** opdateres til **Annulleret**.

Dernæst oprettes der tilbageførselsposter i tabellen med faktiske oplysninger. For at oprette tilbageførselsposter kopieres feltværdierne fra de oprindelige faktiske oplysninger i systemet. De eneste værdier, der ikke kopieres over, er antalsværdier. Disse værdier omgøres i stedet. Tilbageførte faktiske værdier oprettes for både faktiske **Omkostninger** og **Ikke-faktureret salg**. Feltet **Justeringsstatus** for de tilbageførte faktiske oplysninger angives til **Ikke-justerbar**, og feltet **Faktureringsstatus** angives til **Annulleret**. Pga. disse ændringer vil det registrerede beløb og omsætningens ordrebeholdning på projektet ikke længere medtage de beløb, som disse faktiske værdier repræsenterer.

Hvis en anmodning om tilbagekaldelse afvises, har det ingen økonomisk indvirkning på projektet.

## <a name="changes-to-time-entry-records"></a>Ændringer af tidsregistreringsposter

I den følgende illustration vises de ændringer, der sker for godkendte tidsregistreringer og de tilsvarende godkendelsesposter, når de tilbagekaldes.

![Tilstandsovergange for tidsregistreringer.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Ændringer af posterne for udgifter og materialeforbrug

I den følgende illustration vises de ændringer, der sker for godkendte udgifts- og materialeforbrugsposter og de tilsvarende godkendelsesposter, når de tilbagekaldes.

![Tilstandsovergange for udgiftsposter.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
