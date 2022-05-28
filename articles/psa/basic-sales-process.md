---
title: Salgsprocesser
description: Denne emne indeholder oplysninger om de grundlæggende salgsprocesser.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bec8718e287500a7cbc778dc32758e793be8dc3b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580311"
---
# <a name="sales-processes"></a>Salgsprocesser

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

De salgsprocesser, der bruges i en projektbaseret organisation, adskiller sig fra de salgsprocesser, der bruges i en produktbaseret organisation. Forskellen opstår, fordi salgscyklusserne for projektbaserede organisationer er længere og kræver, at der er tilpasset estimatteknikker for at analysere og udarbejde tilbud for hver enkelt aftale. Dynamics 365 Project Service Automation bruger nogle af de samme funktioner, der bruges i salgsprocessen for Dynamics 365 Sales. Her er nogle eksempler:

- Et objekt af typen Kundeemne bruges til at spore salgsprocessen.
- Kvalificering af kundeemner spores som salgsmuligheder. Salgsprocessen kan også begynde med en salgsmulighed.
- Du har adgang til alle relaterede artefakter for en salgsmulighed. Disse artefakter omfatter salgsteamet, interessenter, sandsynlighed, klassificering, salgsfaser og forretningsprocesser.
- Der oprettes flere tilbud for en salgsmulighed.
- Et tilbud er markeret **Lukket som vundet** for at oprette en salgsordre. I PSA er salgsordren tilpasset, og den kaldes en projektkontrakt.

I følgende illustration vises en typisk salgsproces i en projektbaseret organisation.

> ![Salgsproces i en projektbaseret organisation.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimering af et salg
Værdien af et salg kan estimeres på basis af de projekter, der tidligere er leveret, og kompleksiteten af projekter. I forbindelse med projekter, der omfatter udvidelser til tidligere projekter, eller projekter, hvor leverandørens ekspertise er stor, og velkendte arbejdsskabeloner bruges, kan du bruge en enklere estimeringsproces. Mere komplekse projekter har som regel en længere købsproces. Der er derfor flere faser i salgsestimeringsprocessen. I starten af processen bruger salgsteamet input fra kundechefer og små og fageksperter til at oprette et estimat på højt niveau for hver enkelt komponent af det arbejde, der er angivet i tilbuddet. Disse komponenter i arbejdet repræsenteres af tilbudslinjer. 

Du kan oprette et estimat af tilbuddet på højt niveau. Til sidst erstattes dette overordnede estimat med et mere detaljeret estimat, der er baseret på en projektplan, som du opretter ved hjælp af de standardiserede projektskabeloner. Disse skabeloner hjælper dig med at udarbejde en plan og fastlægge pengeværdier for tilbuddet og dets komponenter (tilbudslinjer). 

Du kan oprette flere tilbud til et projekt og gruppere dem under en enkelt objekttype af salgsmulighed. Til sidst bliver et af disse tilbud markeret **Lukket som vundet**, og der oprettes en projektkontrakt eller en arbejdserklæring. En projektkontrakt indeholder kontraktværdien for hver komponent (kontraktlinje), der accepteres af kunden til levering. En arbejdserklæring oprettes normalt som et Microsoft Word-dokument. Alle de fakturaer, der sendes til kunden i løbet af projektet, refererer til projektkontrakten eller arbejdserklæringen.

Du kan også oprette alternative tilbud under én salgsmulighedsobjekttype eller konfigurere systemet, så der oprettes en projektkontrakt, når et tilbud er vundet. I dette tilfælde kan du vedhæfte et Word-dokument, der repræsenterer arbejdserklæringen i projektkontraktposten.

![Lukning af et tilbud for at oprette en projektkontrakt.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfiguration af salgsprocessen
Du kan bruge forretningsprocesforløb i Microsoft Dynamics 365 til at konfigurere salgsprocessen. Disse forløb giver salgsmedarbejderen en vejledning i en visuel grænseflade, som de kan bruge til at flytte tilbud fremad gennem de faser, der er typiske for din virksomhed.

Din virksomhed kan f.eks. indeholde følgende seks faser i salgsprocessen:

1. Kvalificer
2. Vurdering
3. Intern evaluering
4. Kontrakt
5. Levér
6. Luk

Disse seks faser repræsenteres af vinkeltegn (\>), som du vælger at udvide i hver salgsmulighedsobjekttype, du opretter.

![Konfiguration af forretningsproces i Dynamics 365.](media/basic-guide-3.png)
 
Din organisation bruger måske forskellige objekter til at repræsentere samme handel, mens den udvikles. Tidligt i salgsprocessen repræsenteres en handel af objektet Salgsmulighed. Efterhånden som tiden går, og flere detaljer opstår, kan du bruge estimaterne på øverste niveau til at oprette et eller flere tilbud. Hvis et af disse tilbud gennemses af interne interessenter og kundeinteressenter, repræsenterer tilbudsobjektet handlen. Når kunden har accepteret tilbuddet, repræsenterer en projektkontrakt eller en arbejdserklæring handlen. For at understøtte denne funktion er forretningsprocesforløb struktureret, så hver fase i processen er knyttet til en særskilt databasetabel.

Fasen **forretningsprocesforløb** i salgsprocessen kan understøttes af et salgsmulighedsobjekt. Faserne **Estimat** og **Intern evaluering** kan være understøttet af et tilbudsobjekt. Faserne **Kontrakt**, **Levering** og **Luk** kan være understøttet af et projektkontraktobjekt.

Når du flytter handler gennem faserne, bliver du bedt om at oprette den rette objektpost, så du lettere kan komme gennem processen. Faserne kan være betingede. Hvis du f.eks. kun har brug for en intern evaluering af et tilbud, hvis tilbuddet har en brugerdefineret prisliste, kan du konfigurere denne betingelse i den relevante fase i forretningsprocessen. Fasen **Intern evaluering** vises derefter kun for tilbud, hvor der anvendes en brugerdefineret prisliste. I forbindelse med alle andre handler og tilbud bliver fasen **Estimat** efterfulgt af fasen **Kontrakt**.

> [!NOTE]
> PSA indeholder specifikke sider til salgsmuligheds-, tilbuds-, ordre- og fakturaobjekter. Du skal oprette salgsmuligheder, tilbud, ordrer og fakturaer til projektstyring ved hjælp af projektoplysningssiderne for disse objekter. Hvis du bruger en anden side til at oprette en post, kan du ikke åbne posten fra siden **Projektoplysninger**. Hvis du vil åbne en post på siden **Projektoplysninger**, skal du slette posten og genoprette den ved hjælp af siden **Projektoplysninger**. På siden **Projektoplysninger** sikrer forretningslogikken for hver af disse objekttyper, at feltet **Type** for posten er angivet korrekt, og at alle de obligatoriske koncepter er initialiseret korrekt.

> ![Projektoplysninger for en ny ordre.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Forskelle mellem Project Service Automation og Sales
Selvom salgsprocessen i PSA bruger de grundlæggende funktioner i salgsprocessen i Sales, er der nogle vigtige forskelle på grund af variationer i forretningspraksis for projektbaserede organisationer. Her er nogle eksempler:

- **Projekttilbud** – I Project Service Automation lukkes et tilbud, efter at der er oprettet en projektkontrakt ud fra et tilbud. I Sales kan du holde et tilbud åbent, efter at du har vundet det. Årsagen til denne forskel er, at et sammenfald mellem et tilbud og en projektkontrakt er bedre for projektbaserede organisationer. 
- **Aktivering og revisioner** – I PSA understøttes aktivering og revisioner ikke for projekttilbud. I Sales kan et tilbud låses for at forhindre yderligere ændringer.
- **Lukning af et tilbud som tabt eller vundet** – I PSA forbliver salgsmuligheden åben, når et projekttilbud lukkes som vundet eller tabt. Alle andre tilbud på salgsmuligheden lukkes som tabt. Når et tilbud lukkes som vundet eller tabt i Sales, bliver brugeren bedt om at udføre en handling på salgsmuligheden. Afhængigt af brugerens input kan den underliggende salgsmulighed blive lukket eller forblive åben.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Sporing af ændringer til tilbud og projektplaner i salgscyklussen
I PSA kan du ikke spore ændringer, der er foretaget i et tilbud. Du skal i stedet markere det eksisterende tilbud **Lukket som tabt** og derefter oprette et nyt tilbud. Du kan kopiere et tilbud eller klone et projektbaseret tilbud ved hjælp af PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Sporing af kommentarer og godkendelser af tilbud og projektkontrakter
Du kan administrere gennemgang og godkendelse af tilbud og projektkontrakter ved hjælp af postvæggen og indlæg. Din organisation kan oprette tilpassede arbejdsprocesser og plug-ins for at tildele, omdirigere, eskalere og administrere meddelelser om gennemsyn og godkendelse af arbejdselementer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
