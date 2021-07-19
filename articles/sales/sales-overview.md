---
title: Oversigt over salgsproces
description: Dette emne indeholder oplysninger om grundlæggende salgsprocesser.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: ed9731193e83eebd35e979adffcea529a289b9c5
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368334"
---
# <a name="sales-process-overview"></a>Oversigt over salgsproces

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

De salgsprocesser, der bruges i en projektbaseret organisation, adskiller sig fra de salgsprocesser, der bruges i en produktbaseret organisation. Dettes skyldes, at salgscyklusserne for projektbaserede organisationer er længere og kræver brugertilpassede estimatteknikker for at analysere og udarbejde et tilbud for hver enkelt aftale. Dynamics 365 Project Operations bruger visse af følgende funktioner, der bruges i en salgsproces:

- En kundeemnepost bruges til at spore salgsprocessen.
- Kvalificering af kundeemner spores som salgsmuligheder.
- Du har adgang til alle relaterede artefakter for en salgsmulighed. Disse artefakter omfatter salgsteamet, interessenter, sandsynlighed, klassificering, salgsfaser og forretningsprocesser.
- Der oprettes flere tilbud for en salgsmulighed.
- Et tilbud tildeles statussen **Lukket som vundet** for at oprette en salgsordre. I Project Operations er salgsordren tilpasset og kaldes en projektkontrakt.

## <a name="estimate-a-sale"></a>Estimer et salg
Værdien af et salg kan estimeres på basis af de projekter, der tidligere er leveret, og kompleksiteten af projekterne. I forbindelse med projekter, der omfatter udvidelser til tidligere projekter, eller projekter, hvor leverandørens ekspertise er stor, og velkendte arbejdsskabeloner bruges, kan du bruge en enklere estimeringsproces. Mere komplekse projekter har som regel en længere købsproces. Der er derfor flere faser i salgsestimeringsprocessen. I starten af processen bruger salgsteamet input fra kundechefer og fageksperter til at oprette et estimat på højt niveau for hver enkelt komponent af det arbejde, der er angivet i tilbuddet. Disse komponenter i arbejdet repræsenteres af tilbudslinjer. 

Du kan oprette et estimat af tilbuddet på højt niveau. Til sidst erstattes dette overordnede estimat med et mere detaljeret estimat, der er baseret på en projektplan, som du opretter ved hjælp af de standardiserede projektskabeloner. Disse skabeloner hjælper dig med at udarbejde en plan og fastlægge pengeværdier for tilbuddet og dets komponenter (tilbudslinjer). 

Du kan oprette flere tilbud til et projekt og gruppere dem under en enkelt salgsmulighedspost. Til sidst bliver et af tilbuddene markeret som **Lukket som vundet**, og der oprettes en projektkontrakt eller en arbejdserklæring. En projektkontrakt indeholder kontraktværdien for hver komponent (kontraktlinje), der accepteres af kunden til levering. En arbejdserklæring oprettes normalt som et Microsoft Word-dokument. Alle de fakturaer, der sendes til kunden i løbet af projektet, refererer til projektkontrakten eller arbejdserklæringen.

Du kan også oprette alternative tilbud under én salgsmulighedspost eller konfigurere systemet, så der oprettes en projektkontrakt, når et tilbud er vundet. I dette tilfælde kan du vedhæfte et Word-dokument, der repræsenterer arbejdserklæringen i projektkontraktposten.

## <a name="configure-the-sales-process"></a>Konfigurer salgsprocessen
Du kan bruge forretningsprocesforløb til at konfigurere salgsprocessen. Disse flow giver en styret visuel grænseflade til at flytte tilbud fremad gennem salgsprocessens faser.

Din virksomhed kan f.eks. indeholde følgende seks faser i salgsprocessen:

1. Kvalificer
2. Estimat
3. Intern evaluering
4. Kontrakt
5. Levér
6. Luk
 
Din organisation bruger måske forskellige objekter til at repræsentere samme handel, mens den udvikles. Tidligt i salgsprocessen repræsenteres en handel af objektet Salgsmulighed. Efterhånden som tiden går, og flere detaljer opstår, kan du bruge estimaterne på øverste niveau til at oprette et eller flere tilbud. Hvis et af disse tilbud gennemses af interne interessenter og kundeinteressenter, repræsenterer tilbudsobjektet handlen. Når kunden har accepteret tilbuddet, repræsenterer en projektkontrakt eller en arbejdserklæring handlen. For at understøtte denne funktion er forretningsprocesforløb struktureret, så hver fase i processen er knyttet til en særskilt databasetabel.

Fasen **forretningsprocesforløb** i salgsprocessen kan understøttes af et salgsmulighedsobjekt. Faserne **Estimat** og **Intern evaluering** kan være understøttet af et tilbudsobjekt. Faserne **Kontrakt**, **Levering** og **Luk** kan være understøttet af et projektkontraktobjekt.

Når du flytter handler gennem faserne, bliver du bedt om at oprette den rette objektpost, så du lettere kan komme gennem processen. Faserne kan være betingede. Hvis du f.eks. kun har brug for en intern evaluering af et tilbud, hvis tilbuddet har en brugerdefineret prisliste, kan du konfigurere denne betingelse i den relevante fase i forretningsprocessen. Fasen **Intern evaluering** vises derefter kun for tilbud, hvor der anvendes en brugerdefineret prisliste. I forbindelse med alle andre handler og tilbud bliver fasen **Estimat** efterfulgt af fasen **Kontrakt**.

> [!NOTE]
> Project Operations har specifikke sider for objektposter af typen salgsmulighed, tilbud, ordre og faktura. Du skal oprette disse poster ved hjælp af projektoplysningssiderne for disse objekter. Ellers kan du ikke åbne posterne fra siden **Projektoplysninger**. Hvis du vil åbne en post på siden **Projektoplysninger**, skal du slette posten og genoprette den ved hjælp af siden **Projektoplysninger**, hvor forretningslogikken for hver af disse objekttyper sikrer, at feltet **Type** for posten er angivet korrekt, og at alle de obligatoriske koncepter er initialiseret korrekt.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Spor revisioner til tilbud og projektplaner i salgscyklussen
I Project Operations kan du ikke spore de revisioner, der er foretaget i et tilbud. Du skal i stedet markere det eksisterende tilbud **Lukket som tabt** og derefter oprette et nyt tilbud. Du kan kopiere et tilbud eller klone et projektbaseret tilbud.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Spor kommentarer og godkendelser af tilbud og projektkontrakter
Du kan administrere gennemgang og godkendelse af tilbud og projektkontrakter ved hjælp af postvæggen og indlæg. Din organisation kan oprette tilpassede arbejdsprocesser og plug-ins for at tildele, omdirigere, eskalere og administrere meddelelser om gennemsyn og godkendelse af arbejdselementer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]