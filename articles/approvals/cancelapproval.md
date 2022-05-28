---
title: Annuller godkendelsen af tidligere godkendte poster
description: I dette emne forklares det, hvordan en projektleder kan annullere godkendelsen af tidligere godkendte tids-, udgifts- eller materialeforbrugsposter.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584773"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Annuller godkendelsen af tidligere godkendte poster

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

En projektleder eller godkender, som tidligere har godkendt tids-, udgifts- eller materialeforbrugsposter, kan annullere deres godkendelse af sådanne poster. 

Følg disse trin for at annullere godkendelsen af en tids-, udgifts- eller materialeforbrugspost, som du tidligere har godkendt.

1. Gå til **Projekter** \> **Mit arbejde** \> **Godkendelser**.
2. På listesiden **Godkendelser** vises alle de poster, der venter på at blive godkendt. Skift visningen til **Mine tidligere godkendelser**.
3. Vælg den tid, de udgifter eller de materialegodkendelser, der skal annulleres. Vælg derefter **Annuller godkendelse** i handlingsruden.
4. Vælg **OK** i bekræftelsesfeltet, der vises, for at bekræfte handlingen.

> [!IMPORTANT]
> Du kan ikke annullere godkendelsen af en tidligere godkendt tids-, udgifts- og materialeforbrugspost, der allerede er faktureret til kunden. Hvis du forsøger, modtager du en meddelelse, som fastslår, at godkendelsen ikke kan annulleres, fordi den allerede er faktureret. I dette tilfælde kan du kun annullere godkendelsen, hvis en korrektionsfaktura anvendes til at udstede en fuld kredit eller refundering til kunden på den oprindelige faktura.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Konsekvens af at annullere godkendelsen af en tidligere godkendt post

Når en godkendelse annulleres, har det både driftsmæssige og økonomiske konsekvenser.

### <a name="operational-impact"></a>Driftsmæssig konsekvens

Hvis godkendelsen af en post annulleres, markeres godkendelsesposten som **Indsendt**. Postens status ændres til **Indsendt**. I denne fase kan et medlem af et projektteam tilbagekalde posten uden at sende en anmodning om tilbagekaldelse.

Godkenderen kan ændre værdierne for **Fakturerbart antal** og **Faktureringstype** og derefter godkende posten én gang mere.

### <a name="financial-impact"></a>Økonomisk konsekvens

Hvis godkendelsen af en post annulleres, opdateres de tilsvarende faktiske værdier for omkostninger og salg på følgende måde:

- Feltet **Justeringsstatus** opdateres til **Justeret**.
- Feltet **Faktureringsstatus** opdateres til **Annulleret**.

Dernæst oprettes der tilbageførselsposter i tabellen med faktiske oplysninger. For at oprette tilbageførselsposter kopieres feltværdierne fra de oprindelige faktiske oplysninger i systemet. De eneste værdier, der ikke kopieres over, er antalsværdier. Disse værdier omgøres i stedet. Tilbageførte faktiske værdier oprettes for både faktiske **Omkostninger** og **Ikke-faktureret salg**. Feltet **Justeringsstatus** for de tilbageførte faktiske oplysninger angives til **Ikke-justerbar**, og feltet **Faktureringsstatus** angives til **Annulleret**. Pga. disse ændringer vil det registrerede beløb og omsætningens ordrebeholdning på projektet ikke længere medtage de beløb, som disse faktiske værdier repræsenterer.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
