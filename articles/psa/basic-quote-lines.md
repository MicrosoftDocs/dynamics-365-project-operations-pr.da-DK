---
title: Tilbud og tilbudslinjer
description: Dette emne indeholder oplysninger om tilbud og tilbudslinjer.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 024a7cdb81340a077e839d92c4321c8b0051404b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145108"
---
# <a name="quotes-and-quote-lines"></a>Tilbud og tilbudslinjer

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Dynamics 365 Project Service Automation findes der to typer tilbud: projekttilbud og salgstilbud. De to typer er forskellige på følgende måder:

- I et salgstilbud er der kun ét gitter til linjeelementer. I et projekttilbud er der to gitre til linjeelementer: ét til projektlinjer og ét til produktlinjer.
- Et salgstilbud understøtter aktivering og revisioner. Et projekttilbud understøtter ikke disse processer.
- Du kan knytte flere ordrer til et salgstilbud. Du kan kun tilknytte én projektkontrakt til et projekttilbud.
- Du kan vinde et salgstilbud og holde den relaterede salgsmulighed åben. Når et projekttilbud er vundet, lukkes den tilknyttede salgsmulighed.
- Et salgstilbud inkluderer ikke visse felter og begreber, der findes i et projekttilbud, som indeholder felter. Felterne omfatter **Kontraktenhed**, **Account Manager** og **Kontaktnavn for fakturering**.  
- Salgstilbud og projekttilbud identificeres også af et felt baseret på grupperet indstilling med navnet **Type.** I forbindelse med et salgstilbud indeholder dette felt værdien **Elementbaseret**. I forbindelse med et projekttilbud har det værdien **Arbejdsbaseret**.

I dette emne fokuseres der på detaljerne i projekttilbud.

Et projekttilbud i PSA kan have flere linjeelementer eller tilbudslinjer. Faktisk indeholder et projekttilbud to gitre for linjeelementer. Et gitter er til projektbaserede linjer, der gør det muligt at foretage detaljerede estimater. Det andet gitter er til produktbaserede linjer, der bruger en simpel enhedspris og en mængdebaseret tilgang.

- **Projektbaseret** – mængden (værdi i tilbud) bestemmes, efter at du har anslået, hvor meget arbejde der er nødvendigt. Du kan estimere arbejde på et højt niveau, eller du kan estimere det direkte som linjedetaljer under hver tilbudslinje. Endelig kan du vurdere arbejde baseret på estimater fra bunden ved hjælp af et projekt og en projektplan. Projektbaserede tilbudslinjer findes kun i projektbaserede tilbud, der er oprettet ved hjælp af Project Service Automation. Denne type tilbudslinje er en brugerdefineret formular for de tilbudslinjer, der skal rekvireres, og som er tilgængelige i Microsoft Dynamics 365 Sales.
- **Produktbaseret** – mængden (værdi i tilbud) bestemmes på baggrund af det antal enheder, der er solgt, og produktets enhedssalgspris. Produktet på en produktbaseret linje kan komme fra et produktkatalog i Salg, eller det kan være et produkt, som du definerer. Denne type tilbudslinje er også tilgængelig for projektbaserede tilbud, der oprettes ved hjælp af PSA.

Beløbet i et tilbud er det samlede beløb på tværs af de produktbaserede linjer og de projektbaserede linjer.

> [!NOTE]
> Tilbud og tilbudslinjer er ikke nødvendige i PSA. Du kan starte projektprocessen med en projektkontrakt (solgt projekt). Der kræves dog altid en salgsmulighed, uanset om du starter med et tilbud eller en projektkontrakt.

## <a name="project-based-quote-lines"></a>Projektbaserede tilbudslinjer.

En projektbaseret tilbudslinje i PSA har følgende faktureringsmetoder:

- Tid og materiale
- Fast pris

### <a name="time-and-material"></a>Tid og materiale

Metoden til fakturering af tid og materiale er baseret på forbrug. Når du vælger denne faktureringsmetode, faktureres kunden, efterhånden som der påløber omkostninger for projektet. Fakturaer oprettes ud fra en datobaseret periodisk hyppighed. I salgsprocessen giver værdien i tilbuddet for en tids- og materialekomponent kun et estimat over de endelige omkostninger til kunden. Leverandøren forpligter sig ikke til at fuldføre projektet med præcist værdien i tilbuddet. Tids- og materialekomponenter øger kundens risiko. Kunderne ønsker måske at forhandle yderligere klausuler, der ikke må overskrides, for at minimere risikoen. PSA understøtter ikke angivelse af klausuler, der ikke må overskrides.

### <a name="fixed-price"></a>Fast pris

Ved hjælp af faktureringsmetoden Fast pris forpligter en leverandør sig til at levere projektet til kunden til en fast pris. Kunden faktureres værdien i tilbuddet for fastpristilbudslinjen, uanset hvilke omkostninger leverandøren pådrager sig for at levere den pågældende tilbudslinje. Værdien i tilbudslinjen med fast pris faktureres på en af følgende måder: 

- Som et engangsbeløb i starten eller slutningen af projektet, eller når en milepæl i projektet nås. 
- Med en datobaseret frekvens af ens afdrag af den faste værdi på tilbudslinjen. Disse afdrag kaldes periodiske milepæle.
- I afdrag, der har en pengeværdi, som er justeret efter statussen for arbejde eller bestemte milepæle, der er nået i projektet. I dette tilfælde kan værdien af de enkelte afdrag være forskellige, men de skal til sammen være lig med den faste værdi på tilbudslinjen.

PSA understøtter alle tre typer fakturatidsplaner for tilbudslinjer med fast pris.

## <a name="transaction-classification"></a>Transaktionsklassificering

Professionelle serviceorganisationer udarbejder typisk et tilbud og fakturerer deres kunder efter klassificering af omkostninger. I PSA repræsenteres omkostningerne af følgende transaktionsklassificeringer:

- **Tid** – denne klassificering repræsenterer omkostningerne ved arbejdskraft eller personalets tid, der er brugt på et projekt.
- **Udgift**: – denne klassificering repræsenterer alle andre typer udgifter i et projekt. Udgifter kan klassificeres bredt, men de fleste organisationer opretter underkategorier, f.eks. ferie, billeje, hotel eller kontorforsyninger.
- **Gebyr** – denne klassificering repræsenterer diverse omkostninger, ekstragebyrer og andet, som en kunde debiteres. 
- **Moms** – denne klassificering repræsenterer momsbeløb, som brugerne tilføjer, mens de angiver udgifter.
- **Materialetransaktion** – denne klassificering repræsenterer faktiske værdier fra produktlinjer på en bekræftet projektfaktura.
- **Milepæl** – denne klassificering bruges af faktureringslogikken med fast pris i PSA.

En eller flere af disse transaktionsklassificeringer kan tilknyttes den enkelte tilbudslinje. Når et tilbud er vundet, overføres tilknytningen mellem transaktions klassificering og tilbudslinje til kontraktlinjen.
 
> ![Skærmbillede af tilknytning af transaktionstyper til tilbuds- og kontraktlinjer](media/basic-guide-5.png)
  
Et tilbud kan f.eks. indeholde følgende to tilbudslinjer: 
- Konsulentarbejde, der benytter en metode til fakturering af tid og materiale, hvor klassificeringer af tids- og vederlagstransaktioner er gældende. For eksempel faktureres alle tids- og vederlagstransaktioner for eksempelprojektet **Dynamics AX Implementering** til kunden baseret på den tid og de materialer, der er brugt. 
- Relaterede rejseudgifter, der bruger en faktureringsmetode med fast pris. For eksempel faktureres alle rejseudgifter for eksempelprojektet **Dynamics AX Implementering** med en fast pengeværdi.

> [!NOTE]
> Kombinationen af projekt- og transaktionsklassificeringerne af **Tid**, **Udgift** og **Vederlag**, der er tilknyttet en tilbuds- eller kontraktlinje, skal være entydig. Hvis den samme kombination af projekt- og transaktionsklasse er knyttet til mere end én kontraktlinje eller tilbudslinje, vil PSA ikke fungere korrekt.

## <a name="billing-types"></a>Faktureringstyper

Feltet **Faktureringstype** definerer begrebet fakturerbarhed i PSA. Det er en grupperet indstilling, der har følgende mulige værdier:

- **Fakturerbar** – den omkostning, der er periodiseret af denne rolle/kategori, er en direkte omkostning, der styrer udførelsen af projektet, og kunden betaler for dette arbejde. Betalingen kan administreres som et tids-og materialearrangement eller et fastprisarrangement. Den medarbejder, der bruger denne tid, modtager dog den tilsvarende kredit for vedkommendes fakturerbare tidsforbrug.
- **Ikke-fakturerbar** – den omkostning, der er periodiseret af denne rolle/kategori, anses for at være en direkte omkostning, der styrer udførelsen af projektet, også selvom dette faktum ikke anerkendes af kunden, og denne ikke vil betale for dette arbejde. Den medarbejder, der bruger tiden, krediteres ikke med det fakturerbare tidsforbrug for det.
- **Gratis** – den omkostning, der er periodiseret af denne rolle/kategori, anses for at være en direkte omkostning, der styrer udførelsen af projektet, og kunden anerkender dette faktum. Den medarbejder, der bruger tiden, krediteres det fakturerbare tidsforbrug for det. Denne omkostning debiteres dog ikke kunden.
- **Ikke tilgængelig** – de omkostninger, der påløber i interne projekter, som ikke kræver sporing af omsætning, spores ved hjælp af denne indstilling.

## <a name="invoice-schedule"></a>Fakturatidsplan

En fakturatidsplan er en række datoer for, hvornår fakturering for et projekt finder sted. Du kan vælge at oprette en fakturatidsplan på en tilbudslinje i PSA. Hver tilbudslinje kan have sin egen fakturatidsplan. Hvis du vil oprette en fakturatidsplan, skal du angive følgende attributværdier:

- En startdato for fakturering 
- En leveringsdato, der repræsenterer faktureringens slutdato i projektet
- En fakturahyppighed

PSA bruger disse tre attributværdier til at oprette et foreløbigt sæt datoer, der skal oprettes fakturering for.

## <a name="invoice-frequency"></a>Fakturahyppighed

Fakturahyppighed er et objekt, der lagrer attributværdier, som kan bruges til at angive hyppigheden af fakturaoprettelse. Følgende attributter udtrykker eller definerer objektet Fakturahyppighed:

- **Periode** – hver måned, hver anden uge og ugentlige perioder understøttes. 
- **Kørsler pr. periode** – hvis perioderne er ugentlige eller hver anden uge, kan du kun definere én kørsel pr. periode. For månedlige perioder kan du definere mellem én og fire kørsler pr. periode. 
- **Kørselsdage** – de dage, hvor faktureringen skal køres. Du kan konfigurere denne attribut på to måder:
  - **Hverdage** – du kan f.eks. angive, at faktureringen skal køres hver mandag eller hver anden mandag. Kunder, der skal angive fakturering til at køre på en arbejdsdag, foretrækker muligvis denne form for konfiguration. 
  - **Kalenderdage** – du kan f.eks. angive, at faktureringen skal køres den 7. og 21. i hver måned. Nogle organisationer foretrækker muligvis denne form for konfiguration, da den er med til at sikre, at fakturering køres efter en fast tidsplan hver måned.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Fakturatidsplan for en tilbudslinje med fast pris

I forbindelse med en tilbudslinje med fast pris kan du bruge gitteret **Fakturatidsplan** til at oprette faktureringsmilepæle, der er lig med værdien af tilbudslinjen.

- Hvis du vil oprette faktureringsmilepæle, der er fordelt ligeligt, skal du vælge en fakturahyppighed, angive faktureringsstartdatoen på tilbudslinjen og vælge **Ønsket fuldførelse** for tilbuddet i sektionen **Oversigt** i overskriften til tilbuddet. Vælg **Generer periodiske milepæle** for at oprette ligeligt opdelte milepæle baseret på den valgte fakturahyppighed. 
- Hvis du vil oprette en faktureringsmilepæl med en engangssum, skal du oprette en milepæl og derefter angive værdien for tilbudslinjen som beløbet for milepælen.
- Hvis du vil oprette faktureringsmilepæle, der er baseret på bestemte opgaver i projektplanen, skal du oprette en milepæl og knytte den til projektets tidsplanelement i brugergrænsefladen til faktureringsmilepælen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]