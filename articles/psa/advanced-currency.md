---
title: Scenarier med flere valutaer (version 3.x)
description: Denne emne indeholder oplysninger om scenarier med flere valutaer.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 33e44297dc80801c3e4416cd9fc3bedae5f3c4ba
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291702"
---
# <a name="multiple-currency-scenarios"></a>Scenarier med flere valutaer

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 har to koncepter for valutaer:

- **Transaktionsvaluta** – Den valuta, som en transaktion foretages i. 
- **Grundvaluta** – Valutaen i Dynamics 365-forekomsten. Denne valuta konfigureres, når en Dynamics 365-forekomst klargøres. Den kan ikke ændres.

Contoso US solgte f.eks. 100 t-shirts til en kunde i Storbritannien for 15 pund sterling (GBP) hver. I følgende tabel vises, hvordan denne transaktion registreres i objektet Ordreprodukt.

| Produkt | Antal | Pris pr. enhed | Valuta | Beløb | Valutakurs | Pris pr. enhed (basis)| Beløb (basis)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T-shirt | 100      | 15             | GBP      | 1500   | 0.94          | kr. 17.25               | kr. 1,725       |

I kolonnen **Valuta** vises transaktionsvalutaen, som er den valuta, salget fandt sted i. I kolonnen **Valutakurs** vises valutakursen mellem transaktionsvalutaen og grundvalutaen. Grundvalutaen er amerikanske dollar (USD). Denne grundvaluta blev konfigureret, da Dynamics 365-forekomsten blev klargjort.
Som tabellen viser, registreres alle transaktioner både i transaktionsvalutaen og grundvalutaen. I Dynamics 365 bruges valutakursen til beregning af beløb i grundvalutaen.

## <a name="project-service-automation-extensions"></a>Project Service Automation-udvidelser

Dynamics 365 Project Service Automation har indflydelse på transaktionsvalutaen, da forretningstransaktioner som regel har to aspekter: omkostninger og salg.

Følgende objekter betragtes som forretningstransaktioner:

- Tilbudslinjedetaljer
- Projektkontraktlinjedetalje
- Estimatlinje
- Kladdelinje
- Fakturalinjedetalje
- Faktisk

I hvert af disse objekter findes der en post, der repræsenterer omkostningsbeløbet eller salgsbeløbet. Ligesom for alle Dynamics 365-objekter, der har et **beløbsfelt**, inkluderer hver post beløb i både transaktionsvalutaen og grundvalutaen. 

PSA udvider konceptet med transaktionsvalutaen for omkostninger og salg på følgende måder:

- Omkostningstransaktionsvalutaen for timetransaktioner hentes altid fra valutaen i den organisationsenhed, der ejer eller styrer projektet. Denne organisationsenhed kaldes kontraktenheden.
- Salgstransaktionsvalutaen for tids- og udgiftstransaktioner hentes altid fra den valuta, der bruges i projektkontrakten.
- Omkostningstransaktionsvalutaen for udgifter hentes fra den valuta, som udgiftsposten er oprettet i.

## <a name="multiple-currency-scenario"></a>Scenarie med flere valutaer

I dette afsnit beskrives et eksempel på et projekt, som Contoso UK leverer til en kunde, der hedder Fabrikam, Japan. Scenariet er konfigureret sådan:

1. GBP og japanske yen (JPY) er konfigureret under **Indstillinger** \> **Forretningsstyring** \> **Valutaer**. 
2. Der er konfigureret en kundekonto med navnet **Fabrikam -Japan**, og JPY er valgt som valuta for firmaet.
3. En organisationsenhed med navnet **Contoso UK** er konfigureret, og GBP er valgt som valuta.
4. Der oprettes en projektkontrakt, hvor **Contoso UK** angives som kontraktenheden, og **Fabrikam – Japan** er angivet som kunden.
5. Der oprettes projektkontraktlinjer på baggrund af faktureringsordningerne for de forskellige transaktionsklasser i projektet, f.eks. fakturering for tid i forhold til fakturering af udgifter.
6. Der oprettes et projekt, hvor **Contoso UK** angives som kontraktenheden. Projektet oprettes og knyttes til projektkontraktlinjerne.


Under estimering, der bruger tilbudslinjedetaljer, projektkontraktlinjedetaljer eller estimatlinjen i tidsplanen, oprettes der altid to poster i objektet. Den ene post er til omkostning, og den anden post er til salg.

- Som standard angives transaktionsvalutaen i omkostningsposten til valutaen for projektets kontraktenhed. I dette eksempel er valutaen GBP.
- Som standard angives transaktionsvalutaen i salgsposten til valutaen for projektets kontrakt. I dette eksempel er valutaen JPY.

Når faktiske oplysninger oprettes for tid ved brug af tidsregistrering eller kladdelinje, indtræffer følgende funktionsmåde:

- Som standard angives transaktionsvalutaen i omkostningsposten til valutaen for projektets kontraktenhed.
- Som standard angives transaktionsvalutaen i salgsposten til valutaen for projektets kontrakt.

Når faktiske oplysninger oprettes for udgifter ved brug af udgiftspost eller kladdelinje, indtræffer følgende funktionsmåde:

- Du kan registrere udgiftsbeløbet i en hvilken som helst valuta. Vælg valutaen ved hjælp af valutavælgeren på siden **Udgiftspost** eller siden **Kladdelinje**. Som standard angives transaktionsvalutaen for omkostningsposten til valutaen på udgiftsposten. 
- Som standard er transaktionsvalutaen for salgsposten lig med valutaen for projektets kontrakt. For at angive denne valuta konverterer systemet først transaktionsbeløbet i den valuta, som brugeren har indtastet, til grundvalutaen. Beløbet konverteres derefter til den valuta, der er angivet i projektkontrakten. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Beregning af akkumuleringer, når faktiske projektoplysninger registreres i flere transaktionsvalutaer

I Dynamics 365 håndteres akkumuleringer af beløb automatisk i forskellige valutaer. Her er et eksempel.

| Transaktionsklasse | Transaktionstype| Date   | Ressource | Transaktionskategori | Antal | Enhedspris | Beløb      | Valutakurs | Beløb i grundvaluta |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Tidspunkt              | Ikke-faktureret salg   | 14-jun | Adam  |                      | 8 timer    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Tidspunkt              | Ikke-faktureret salg   | 15-jun | Adam  |                      | 8 timer    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Udgift           | Ikke-faktureret salg   | 16-jun | Adam  | Hotel                | 1 EA     | 250 EUR      | 250 EUR     | 0,94          | 265,95 USD     |
| Udgift           | Ikke-faktureret salg   | 17-jun | Adam  | Biludlejning           | 1 EA     | 150 EUR      | 150 EUR     | 0,94          | 159,57 USD     |

Hvis du vil beregne den samlede ikke-fakturerede salgsværdi på projektet, kan du oprette et akkumuleringsfelt for **Beløb** i alle de relaterede ikke-fakturerede faktiske salg. Akkumuleringsfeltet er en struktur i Dynamics 365, der gør det muligt at have hurtige formler på relaterede poster.


[!INCLUDE[footer-include](../includes/footer-banner.md)]