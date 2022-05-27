---
title: Tilbagekalde godkendte tids- eller udgiftsposter
description: Dette emne indeholder oplysninger om, hvordan du kan tilbagekalde en tidligere godkendt tids- eller udgiftstransaktion.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
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
ms.openlocfilehash: 457aebb00851a1db3e4aa1068f6a825759b8f2e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578793"
---
# <a name="recall-approved-time-or-expense-entries"></a>Tilbagekalde godkendte tids- eller udgiftsposter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Et medlem af et projektteam eller en anden person, der sender en tids- eller udgiftspost, kan tilbagekalde denne tids- eller udgiftspost, efter at den er godkendt. Fremgangsmåden for at tilbagekalde en godkendt tids- eller udgiftspost består af to trin:

1. En afsender anmoder om en tilbagekaldelse.
2. En godkender godkender tilbagekaldelsen.

## <a name="request-a-recall"></a>Anmodning om tilbagekaldelse

Følg disse trin for at anmode om tilbagekaldelse af en godkendt tids- eller udgiftspost.

1. I forbindelse med tidsposter skal du gå til **Projekter** \> **Mit arbejde** \> **Tidsregistrering**.

    eller

    I forbindelse med tidsposter skal du gå til **Projekter** \> **Mit arbejde** \> **Udgifter**.

2. Ved tidsposter skal du vælge alle tidsposterne for en bestemt kombination af et projekt og en opgave. Du kan også vælge de enkelte celler for tid på en bestemt dato i forbindelse med et bestemt projekt i gitteret.

    eller

    I forbindelse med udgiftsposter skal du markere rækken for den udgiftspost, der skal tilbagekaldes.

3. Vælg **Tilbagekalde**. En bekræftelsesdialogboks åbnes. Hvis de valgte tids- og udgiftsposter allerede er godkendt, bliver du bedt om at angive en årsag til tilbagekaldelsen.
4. Angiv en årsag til tilbagekaldelsen, og vælg derefter **OK** for at bekræfte handlingen. Systemet sender den person, som godkendte posterne, en anmodning om at godkende tilbagekaldelsen.

> [!NOTE]
> Selvom det er muligt at tilbagekalde godkendte tids- og udgiftsposter, så kan der ikke oprettes en anmodning om tilbagekaldelse, hvis en godkendt tid eller udgift allerede er faktureret til kunden. En bruger, der forsøger at oprette en anmodning om tilbagekaldelse, modtager en meddelelse om, at tiden eller udgiften ikke kan tilbagekaldes, fordi den allerede er faktureret.

## <a name="approve-or-reject-a-recall-request"></a>Godkende eller afvise en anmodning om tilbagekaldelse

Følg disse trin for at godkende eller afvise en anmodning om tilbagekaldelse.

1. Gå til **Projekter** \> **Mit arbejde** \> **Godkendelser**.
2. Skift visningen til **Tilbagekald anmodninger om godkendelse** på listesiden **Godkendelser**. Der vises en liste over sendte anmodninger om tilbagekaldelser.
3. Vælg en eller flere poster, og vælg derefter enten **Godkend** eller **Afvis**.
4. Hvis du har valgt **Godkend**, modtager du en advarsel, der forklarer, hvordan godkendelsen virker. Vælg **OK** for at bekræfte handlingen. Anmodningen om tilbagekaldelse er godkendt

    eller

    Hvis du har valgt **Afvis**, afvises anmodningen om tilbagekaldelse.

> [!NOTE]
> Som når der anmodes om tilbagekaldelse, kontrolleres det i systemet, om faktureringsaktiviteten for tids- og udgiftsposterne registreres, når en tilbagekaldelse godkendes. Hvis en post allerede er faktureret, eller hvis den er på en kladdefaktura, modtager godkenderen en fejlmeddelelse, der angiver, at tiden eller udgiften ikke kan godkendes til tilbagekaldelse, da den allerede er blevet faktureret.

## <a name="impact-of-a-recall-request"></a>Virkning af en anmodning om tilbagekaldelse

Når en godkendelse tilbagekaldes, har det både driftsmæssige og økonomiske konsekvenser.

### <a name="operational-impact"></a>Driftsmæssig konsekvens

Hvis en anmodning om tilbagekaldelse godkendes, markeres godkendelsesposten som **Afvist**. Postens status ændres til enten **Returneret** eller **Afvist**, afhængigt af om det er en tidsregistrering eller en udgiftspost.

Projektteammedlemmet kan få vist poster, redigere og derefter sende poster igen eller slette posterne fuldstændigt.

Hvis en anmodning om tilbagekaldelse afvises, forbliver statussen for posten **Godkendt**, og posten kan ikke redigeres af projektteammedlemmet eller godkenderen for projektet.

### <a name="financial-impact"></a>Økonomisk konsekvens

Hvis en tilbagekaldelse godkendes, opdateres de tilsvarende faktiske værdier for omkostninger og salg på følgende måde:

- Feltet **Justeringsstatus** opdateres til **Justeret**.
- Feltet **Faktureringsstatus** opdateres til **Annulleret**.

Dernæst oprettes der tilbageførselsposter i tabellen med faktiske oplysninger. For at oprette tilbageførselsposter kopieres feltværdierne fra de oprindelige faktiske oplysninger i systemet. De eneste værdier, der ikke kopieres over, er antalsværdier. Disse værdier omgøres i stedet. Tilbageførte faktiske værdier oprettes for både faktiske **Omkostninger** og **Ikke-faktureret salg**. Feltet **Justeringsstatus** for de tilbageførte faktiske oplysninger angives til **Ikke-justerbar**, og feltet **Faktureringsstatus** angives til **Annulleret**. Pga. disse ændringer vil det registrerede beløb og omsætningens ordrebeholdning på projektet ikke længere medtage de beløb, som disse faktiske værdier repræsenterer.

Hvis en anmodning om tilbagekaldelse afvises, har det ingen økonomisk indvirkning på projektet.

## <a name="changes-to-time-entry-records"></a>Ændringer af tidsregistreringsposter

I den følgende illustration vises de ændringer, der sker for godkendte tidsregistreringer, når de tilbagekaldes.

![Tilstandsovergange for tidsregistreringer.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Ændringer af udgiftsregistreringsposter

I den følgende illustration vises de ændringer, der sker for godkendte udgiftsposter, når de tilbagekaldes.

![Tilstandsovergange for udgiftsposter.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
