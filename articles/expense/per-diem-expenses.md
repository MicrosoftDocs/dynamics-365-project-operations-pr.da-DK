---
title: Diætudgifter
description: Dette emne indeholder oplysninger om, hvordan du arbejder med diætudgifter.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596043"
---
# <a name="per-diem-expenses"></a>Diætudgifter

> [!IMPORTANT] 
> Funktioner, der beskrives i dette emne, er tilgængelige for målrettede brugere, der er en del af målgruppen for en eksempelversion.

En diætbetaling er en fast, forudbestemt dagspris, som en virksomhed betaler til sine medarbejdere for ophold (hoteller), måltider og uforudsete omkostninger, som de pågældende medarbejdere betaler, mens de rejser i embedsmedfør. Virksomheden udbetaler dette beløb til medarbejderne i stedet for at betale de faktiske rejseomkostninger. Medarbejdere kan bruge deres **Uforudsete/andet** diætbetaling til drikkepenge, roomservice, vask eller rens i forbindelse med vigtige forretningsmøder. Diæten pr. medarbejder kan variere, afhængigt af om arbejdsgiver vælger at godtgøre de samlede omkostninger for ophold og måltider eller kun omkostningerne til måltider og diverse.

Diætsatser kan være baseret på tidspunktet for året, rejselokationen eller begge. Når du opretter en diætregel, kan du angive, at du vil tilbageholde en procentdel af en diætsats, hvis en medarbejder modtager ekstra måltider eller tjenester. Du kan også angive et minimumantal timer og et maksimumantal timer, som kan anvendes som diæt for en medarbejders rejse.

Diæten som det samlede beløb, der tilbydes pr. dag, minus reduktion for måltider (omkostningen ved ekstra måltider), som ydes til medarbejderen.

## <a name="configure-per-diems"></a>Konfigurer diæter

Gør følgende for at konfigurere udgifter til diæter.

1. Gå til **Udgiftsstyring** \> **Opsætning** \> **Generelt** \> **Parametre for udgiftsstyring**.
2. På fanen **Diæt** skal du i feltet **Beregning af måltidsreduktion via** vælge, hvordan diæterne bør beregnes:

    - **Måltidstype pr. rejse** – Beregn diæten ud fra den type måltidstype, der angives (morgenmad, frokost eller aftensmad), og ud fra den måltidsreduktion, der er angivet for hver måltidstype i henhold til diættilskuddet for rejsens varighed.
    - **Måltidstype pr. dag** – Beregn diæten ud fra den type måltidstype, der angives, og ud fra den måltidsreduktion, der er angivet for hver måltidstype i henhold til diættilskuddet pr. dag.
    - **Antal måltider pr. dag** – Beregn diæten ud fra antallet af måltider, der angives pr. dag, og måltidsreduktionen for antallet af måltider, der betales pr. dag.

3. Gå til **Udgiftsstyring** \> **Opsætning** \> **Beregning og koder** \> **Diætlokationer**.
4. Tilføj lokationer, hvor diæter kan bruges.
5. For hver lokation, du tilføjer, skal du på fanen **Diæter** vælge den diætsats og valuta, der gælder mellem bestemte start- og slutdatoer, og som skal anvendes på ophold, måltider og andre udgifter. Hvis du vil konfigurere diætsatser og valutaer, skal du gå til **Udgiftsstyring** \> **Opsætning** \> **Beregning og koder** \> **Diæter**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Diæter i den moderniserede udgiftsbrugergrænseflade

Funktionen diæt understøttes i det moderniserede arbejdsområde **Udgiftsstyring** i Microsoft Dynamics 365 Finance version 10.0.25 og nyere.

Du kan aktivere diæter ved at følge disse trin.

1. I arbejdsområdet **Funktionsstyring** skal du finde og vælge funktionen **Moderniserede udgiftsrapporter** på listen derefter vælge **Aktivér nu**.
2. Find og vælg funktionen **Moderniseret brugergrænseflade for diætudgiftsrapport** på listen derefter vælge **Aktivér nu**.

## <a name="how-the-feature-works"></a>Sådan fungerer funktionen

Dette afsnit indeholder eksempler på tre konfigurationsscenarier. For hvert eksempel angives feltet **Beregn måltidsreduktion** til en anden værdi. I alle tre eksempler er det samlede beløb, der skal betales, det samme, indtil måltidsreduktionen anvendes. Derefter adskiller det samlede beløb, der skal betales, sig for de enkelte eksempler.

Hvis du vil oprette de diætudgifter, der bruges til alle tre eksempler, skal du følge disse trin.

1. Gå til **Arbejdsområder** \> **Udgiftsstyring**.
2. Vælg **Ny udgiftsrapport**, eller vælg en eksisterende udgiftsrapport.
3. Tilføj en ny udgift. I feltet **Kategori** skal du vælge **Diæt**. Vælg lokationen og rejsens start- og slutdatoer. Diæten for ophold, måltider og diverse (andre udgifter) beregnes på baggrund af det daglige beløb, der er angivet for den valgte placering.

    Du vælger f.eks. **Redmond (USA)** som lokation. Det daglige beløb for den pågældende lokation er 150 USD (150 USD) til ophold, 75 USD til måltider og 5 USD til diverse. Startdatoen er 10. januar, og slutdatoen er 14. januar. Den valgte varighed er derfor fem dage, når den valgte konfiguration er kalenderdage med tid, og den valgte tid starter og slutter kl. 12:00 på start- og slutdatoer. Her er beregningerne:

    - Samlet beløb, der skal betales = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
    - Andelen af beløbet til måltider og diverse = 5 × (75 + 5) = 400 USD

Hvis der blev serveret morgenmad, frokost og aftensmad under rejsen, skal de angives som en måltidsreduktion.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Eksempel 1:Diæt, hvor måltidsreduktioner er baseret på måltidstype pr. rejse

I dette eksempel er måltidsreduktionen 30 procent for morgenmad, 30 procent for frokost og 40 procent for aftensmad. På siden **Parametre for udgiftsstyring** feltet **Beregn måltidsreduktion på grundlag af** til **Måltidstype pr. rejse**. Her er de beregninger, der skal udføres, hvis medarbejderen får stillet tre morgenmad, to frokoster og ingen aftensmad til rådighed:

- Måltidsreduktion = (3 × \[75 × 30 %\]) + (2 × \[75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Måltider og diverse = 400 – 112,50 = 287,50 USD
- Samlet beløb, der skal betales = Samlet beløb, der ydes – måltidsreduktion= 1.150 – 112,50 = 1.037,50 USD

![Diætudgift, hvor måltidsreduktionen er baseret på måltidstype pr. rejse.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Eksempel 2: Diæt, hvor måltidsreduktioner er baseret på måltidstype pr. dag

I dette eksempel er måltidsreduktionen 30 procent for morgenmad, 30 procent for frokost og 40 procent for aftensmad. På siden **Parametre for udgiftsstyring** feltet **Beregn måltidsreduktion på grundlag af** til **Måltidstype pr. dag**. I dette tilfælde skal du i gitteret **Måltider** i dialogboksen **Rediger udgift** fjerne markeringen i afkrydsningsfelterne for at angive, hvilke måltider du fik stillet til rådighed under rejsen.

Her kan du f.eks. se beregningerne, hvis de første tre dage af turen var med morgenmad:

- Daglig måltidsreduktion for hver af de første tre dage = 75 × 30 % = 22,50 USD
- Samlet måltidsreduktion = 3 × 22,50 = 67,50 USD
- Måltider og diverse for dag 1-3 = 75 - 22,50 = 57,50 USD
- Samlet måltider og diverse = Sum af måltider og diverse for fem dage = 400 til 67,50 = 332,50 USD
- Samlet beløb, der skal betales = Samlet beløb – måltidsreduktion= 1.150 – 67,50 = 1.082,50 USD

![Diætudgift, hvor måltidsreduktionen er baseret på måltidstype pr. dag.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Eksempel 3: Diæt, hvor måltidsreduktioner er baseret på antal måltider pr. dag

I dette eksempel beregnes måltidsreduktionen på baggrund af det antal måltider, der blev stillet til rådighed pr. dag (dvs. at feltet **Beregning af måltidsreduktion på baggrund af** på siden **Parametre for udgiftsstyring** er angivet til **Antal måltider pr. dag**). I gitteret **Måltider** i dialogboksen **Rediger udgift** fjerne markeringen i afkrydsningsfelterne for at angive, hvilke måltider du fik stillet til rådighed.
I dette tilfælde er måltidsreduktionen kun baseret på antallet af måltider, der blev stillet til rådighed, og ikke på den angivne type måltider (morgenmad/frokost/aftensmad).

Her er beregningerne for diæter, når den daglige godtgørelse er 150 USD til ophold, 75 USD til måltider og 5 USD til diverse:

- **Samlet beløb, der skal betales** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **Ét måltid:** Måltidsreduktion = 20 % = 15 USD
- **To måltider:** Måltidsreduktion = 50 % = 37,50 USD
- **Tre måltider:** Måltidsreduktion = 100 % = 75 USD

Her er beregningerne for **tilskud til måltider og diverse**, som omfatter 5 USD til diverse:

- Dag 1 - To måltider stilles til rådighed = (75- 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dag 2 - To måltider stilles til rådighed = (75- 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dag 3 – Et måltid stilles til rådighed = (75- 15) + 5 = 60 + 5 = 65 USD
- Dag 4 - Ingen måltider stilles til rådighed = (75- 0) + 5 = 75 + 5 = 80 USD
- Dag 5 - Tre måltider stilles til rådighed = (75- 75) + 5 = 0 + 5 = 5 USD

- Samlede måltider og diverse = Måltider og diverse for dag 1+ dag 2+ dag 3+ dag 4 + dag 5 = 235 USD
- Samlet måltidsreduktion = Måltidsreduktion for dag 1+ dag 2 + dag 3 + dag 4 + dag 5 = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Samlet beløb, der skal betales = Samlet beløb, der ydes – samlet måltidsreduktion= 1.150 USD – USD 165 = 985 USD

![Diætudgift, hvor måltidsreduktionen er baseret på antal måltider pr. dag.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Hvis du bruger den nye brugergrænseflade i Finance version 10.0.23, kan du ikke oprette diæt udgifter, der har overlappende datoer. Hvis du forsøger, får du vist en fejlmeddelelse.
