---
title: Projektkontrakter
description: Dette emne giver eksempler på de projektkontrakter, som du kan oprette til forskellige typer projekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere projektkunder.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b92668c38071e8b1afdee9a79fd4a25190248ada30380bfb79054a6dc587f95
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001019"
---
# <a name="project-contracts"></a>Projektkontrakter

[!include [banner](../includes/banner.md)]

Denne artikel giver eksempler på de projektkontrakter, som du kan oprette til forskellige typer projekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere projektkunder.

Projekttypen, som du har oprettet for en projektkontrakt, bestemmer den metode, der bruges til at fakturere projektkunder. Du kan ændre en projektkontrakt og det relaterede projekt, men du kan ikke ændre projekttypen. 

Ved hjælp af en projektkontrakt kan du fakturere et eller flere projekter på samme tid. Projektkontrakten er også med til at sikre en ensartet faktureringsprocedure for alle underprojekter i en projektstruktur. 

Alle de projekter, der skal faktureres, skal knyttes til en projektkontrakt. Indstillingerne for en projektkontrakt gælder for alle projekter og underprojekter, der er knyttet til den pågældende projektkontrakt. 

En projektkontrakt kan angive en eller flere finansieringskilder. Du kan derfor opdele faktureringen mellem flere finansieringskilder, konfigurere finansieringsgrænser, så finansieringskilder ikke faktureres mere end et bestemt beløb, og konfigurere finansieringsregler for opkrævning af udgifter.

## <a name="funding-for-project-contracts"></a>Finansiering til projektkontrakter
Nogle projektkontrakter angiver, at flere parter deler ansvaret for finansieringen af projektomkostningerne. Her er nogle eksempler:

-   En stor kunde, der har flere inddelinger, anmoder om, at finansieringen af et projekt opdeles efter division.
-   Din virksomhed deler omkostningerne ved et stort projekt med en ekstern organisation.
-   Et vejprojekt samfinansieres af to kommuner.
-   Et bro-projekt finansieres af statsstøtte og en privat virksomhed.

I Dynamics 365 Finance kan du dele faktureringen for en enkelt transaktion eller et helt projekt op mellem flere kunder, tilskud eller organisationer. 

I projekter, der har flere finansieringskilder, kaldes alle de parter, der bidrager til finansieringen af et avanceret finansieringsprojekt, også for finansieringskilder. Når en kunde, en organisation eller et tilskud er defineret som en finansieringskilde, kan den tildeles en eller flere finansieringsregler. Finansieringsregler indeholder de kriterier, der bestemmer, hvordan opkrævninger tildeles de forskellige finansieringskilder i et projekt. 

Da lagervarer, såsom dem, der vises på indkøbsrekvisitioner og indkøbsordrer, ikke kan opdeles, kan omkostningsbeløbet ikke deles op mellem flere finansieringskilder på distributionstidspunktet. Finansieringskildens værdi forbliver derfor 0 (nul), indtil lagerfejlen er bogført. Når lagerfejlen bogføres, fordeles omkostningsbeløbet i henhold til projektets distributionsregler for kontoen.

Her er nogle trin, du kan udføre for at gøre det nemmere at dele faktureringen op mellem flere finansieringskilder:

-   Specificer, at alle de transaktioner, der angives for et projekt, skal bruge samme salgsvaluta som projektkontrakten.
-   Opret finansieringslofter, så en finansieringskilde ikke faktureres mere end et bestemt beløb i et projekt.
-   Konfigurer finansieringsregler og finansieringslofter for hver arbejder, vare, kategori, kategorigruppe og transaktionstype (eller for alle transaktionstyper).
-   Vælg valgfrie start- og slutdatoer for at definere den periode, hvor de enkelte finansieringsregler er gyldige.
-   Angiv den procentdel, som hver finansieringskilde er ansvarlig for.
-   Angiv, hvilken finansieringskilde der er ansvarlig for afrundingsdifferencer, som forårsages af beregninger af finansieringsallokering.
-   Konfigurer regler, der bestemmer, hvordan eksterne kunder faktureres for projektomkostninger, og disse opkræves ved interne organisationer.
-   Registrer transaktioner på en afventende finansieringskonto, indtil der kan opnås yderligere finansiering, eller indtil du beslutter dig for at bære omkostningerne internt.

Der søges efter en momsgruppetildeling i projektet for at afgøre, hvilken momsgruppe der skal knyttes til en transaktion. Hvis der ikke er foretaget nogen momsgruppetildeling på projektniveau, søges der i projektkontrakten.

### <a name="example-multiple-funding-sources-simple"></a>Eksempel: flere finansieringskilder (simpel)

Følgende tabel indeholder scenarier til administration af finansieringsallokering mellem flere finansieringskilder. Disse scenarier er baseret på følgende forudsætninger:

-   Prioritetsindstillingerne indregnes i allokeringen af midler, før andre finansieringsregelkriterier anvendes.
-   Der er ikke angivet noget datointerval for at definere perioden d, når finansieringsreglen er gyldig.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenarie</strong></td>
<td><strong>Finansieringskilde</strong></td>
<td><strong>Fordelingsprocent</strong></td>
<td><strong>Fordelingsprioritet</strong></td>
</tr>
<tr class="even">
<td>Hvis du vil tildele omkostninger til én finansieringskilde, indtil midlerne er opbrugt, skal du fordele omkostningerne til en anden finansieringskilde, indtil dennes midler er opbrugt, og endelig tildele de resterende omkostninger til en tredje finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du vil tildele 75 procent af omkostningerne til én finansieringskilde og 25 procent til en anden finansieringskilde. Når en af disse finansieringskilder er opbrugt, vil du betale de resterende omkostninger fra en tredje finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Du vil tildele 75 procent af omkostningerne til én finansieringskilde og 25 procent til en anden finansieringskilde. Når en af disse finansieringskilder er opbrugt, vil du dele de resterende omkostninger op mellem en tredje og en fjerde finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
<li>Finansieringskilde 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du vil tildele de første 25 procent af omkostningerne til én finansieringskilde og de resterende til en anden finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde 1</li>
<li>Finansieringskilde 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Eksempel: flere finansieringskilder (kompleks)

Du har tre finansieringskilder, som du vil bruge i følgende rækkefølge:

1.  Brug finansieringskilde 2 og finansieringskilde 3 ligeligt, indtil finansieringskilde 2 er udtømt.
2.  Fortsæt med at bruge finansieringskilde 3, indtil den er tømt.
3.  Brug finansieringskilde 1, når finansieringskilde 3 er udtømt.

For at opnå dette skal du gøre følgende:

-   Opret finansieringslofter for finansieringskilde 2 og finansieringskilde 3 i henhold til deres respektive beløb.
-   Opret følgende finansieringsregler:
    -   Regel 1 (prioritet 1): tildel 50 procent af transaktioner til finansieringskilde 2 og 50 procent til finansieringskilde 3.
    -   Regel 2 (prioritet 2): tildel 100 procent af transaktioner til finansieringskilde 3.
    -   Regel 3 (prioritet 3): tildel 100 procent af transaktioner til finansieringskilde 1.

Denne opsætning virker, fordi transaktionerne holdes op imod regler og begrænsninger for at afgøre, om nogen af dem gælder for transaktionen. Hvis der ikke gælder nogen specifikke regler eller grænser for transaktionen, gælder reglen for alle transaktioner. Reglen for alle transaktioner passer til alle transaktioner. 

Hvis der findes en regel, der passer til en transaktion, anvendes den procentdel, der er allokeret i reglen, først, men først efter at de pågældende matches er blevet holdt op imod eventuelle grænser, der er konfigureret. Hvis en grænse er overskredet, og en finansieringskildes midler er opbrugt, ignoreres finansieringsreglen, der er knyttet til finansieringsloftet, og programmet søger efter den næste regel, der gælder. 

I visse tilfælde kan kun en del af en transaktion allokeres i henhold til en regel. Dette kan ske, hvis en grænse nås, når transaktionen allokeres. I dette tilfælde er det kun et bestemt beløb, der allokeres i henhold til den pågældende regel, f.eks. 50 procent, til hver enkelt finansieringskilde. Dette er tilfældet i regel 1, der er beskrevet ovenfor i dette sektion. Resten allokeres efter den næste regel i sekvensen. 

Den følgende tabel undersøger dette scenarie mere detaljeret.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Detaljer</strong></td>
</tr>
<tr class="even">
<td>Finansieringsregler</td>
<td><ul>
<li>Regel 1 (prioritet 1): alle transaktioner. Tildel finansieringskilde 2 ved 50 % og finansieringskilde 3 ved 50 %.</li>
<li>Regel 2 (prioritet 2): alle transaktioner. Tildel finansieringskilde 3 ved 100 %.</li>
<li>Regel 3 (prioritet 2): alle transaktioner. Tildel finansieringskilde 1 ved 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansieringslofter</td>
<td><ul>
<li>Grænse for finansieringskilde 1 = 10.000,00</li>
<li>Grænse for finansieringskilde 2 = 500,00</li>
<li>Grænse for finansieringskilde 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaktion 1</td>
<td><strong>Transaktionsbeløb:</strong> 100,00<strong>Finansiering:</strong> Transaktionen betales kun i henhold til regel 1, da transaktionen er fuldt betalt, efter at regel 1 anvendes. Transaktionen finansieres ligeligt mellem finansieringskilde 2 og finansieringskilde 3.
<ul>
<li>Finansieringskilde 2: 50,00</li>
<li>Finansieringskilde 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transaktion 2</td>
<td><strong>Transaktionsbeløb:</strong> 5.000,00<strong>Finansiering:</strong> Transaktionen betales i henhold til alle tre regler. <strong>Regel 1</strong>
<ul>
<li>Finansieringskilde 2: 450,00</li>
<li>Finansieringskilde 3: 450,00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Finansieringskilde 3: 250,00 (=750,00 - 50,00 - 450,00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Finansieringskilde 1: 3.850,00 (=5.000,00 - 450,00 - 450,00 - 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>De samlede midler, der distribueres til hver finansieringskilde</td>
<td><ul>
<li>Finansieringskilde 1: 3.850,00</li>
<li>Finansieringskilde 2: 500,00</li>
<li>Finansieringskilde 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Faktureringsregler
Når du forhandler en projektkontrakt med en kunde, definerer du, hvordan og hvornår du kan fakturere kunden for det udførte arbejde på et projekt. Når du har konfigureret projektkontrakten og projektet, kan du konfigurere faktureringsregler for projektet. Faktureringsregler er baseret på de projektbetingelser, der er angivet i projektkontrakten. De faktureringsregler, du kan oprette, afhænger af vilkårene i projektkontrakten og projekttypen, f.eks. tid og materialer eller fast pris, som du knytter til faktureringsreglen. Du kan oprette mere end én faktureringsregel for en projektkontrakt. Du kan også tildele en faktureringsregel til flere projekter, der er knyttet til den samme projektkontrakt og har lignende faktureringsbetingelser. 

Du kan oprette følgende typer faktureringsregler:

-   **Leveringsenhed** – Fakturer en kunde, når du har fuldført en leveringsenhed. Du kan definere de enheder, der skal leveres, i kontrakten.
-   **Fremgang** – Fakturer kunden, når du har fuldført en bestemt procentdel af projektet. Du kan konfigurere en faktureringsregel for automatisk at beregne procentdelen af det fuldførte arbejde, eller du kan beregne procentdelen af fuldført arbejde manuelt og det beløb, som kunden skal faktureres.
-   **Milepæl** – Fakturer kunden for det fulde beløb for en projektmilepæl, når milepælen er nået.
-   **Gebyr** – Fakturer kunden for dine tjenester plus et administrationsgebyr, som normalt er en procentdel af omkostningerne forbundet hermed.
-   **Tid og materiale** – Fakturer en kunde for værdien af den tid og de materialer, der bruges på et projekt.

I forbindelse med alle typer faktureringsregler kan du angive en tilbageholdelsesprocent, som trækkes fra på kundefakturaer, indtil et projekt når et aftalte stadie. Der er angivet en procentdel for tilbageholdelse af betaling i projektkontrakten. Beløbet beregnes på baggrund af, og trækkes fra, den samlede værdi af linjerne i en kundes faktura. 

For så vidt angår faktureringsregler for **Tid og materiale** samt **Fremgang** kan du tildele fakturerbare kategorier. Fakturerbare kategorier angiver de transaktioner, der skal inkluderes i kundefakturaer. 

Når du er klar til at fakturere kunden, beregnes det beløb, der skal faktureres for projektet, på grundlag af faktureringsreglerne, og der genereres et projektfakturaforslag. 

Følgende sektioner indeholder eksempler, der viser, hvordan du kan konfigurere og administrere faktureringsregler for et projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Eksempel: Opret en faktureringsregel, der er baseret på antallet af leverede enheder

Din organisation indgår en aftale om at give i alt fem oplæringssessioner til en kundes medarbejdere til en pris på 10.000 pr. oplæringssession. Du fakturerer kunden efter hver enkelt oplæringssession. 

Når du konfigurerer faktureringsreglerne for kontrakten, skal du bruge følgende værdier:

-   Leveringsenheden er én oplæringssession.
-   Enhedsprisen er 10.000 pr. oplæringssession.
-   Det samlede antal enheder er fem oplæringssessioner.

Når du har fuldført én oplæringssession, kan du oprette en faktura på 10.000 for den første enhed, der blev leveret, og sende fakturaen til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Eksempel: Opret en faktureringsregel, der er baseret på en angivet procent for projektets fuldførelse (manuel beregning)

Din organisation, som yder softwarerådgivning, indgår i en aftale med en kunde om at udvikle en del af et produkt, som kunden udvikler. Din organisation indvilliger i at levere softwarekoden over en periode på seks måneder. Kunden indvilliger i at betale din organisation i alt 100.000 for arbejdet. Du opretter en faktureringsregel for at fakturere kunden på grundlag af den procentdel af arbejdet, der er fuldført på projektet, som angivet i kontrakten.

-   I slutningen af den første måned mødes du med kunden for at finde ud af, hvor mange procent af arbejdet der er fuldført. Når du og kunden gennemgår projektet, beslutter du, at projektet er 15 procent fuldført.
-   Du opretter en faktura på 15.000 (15 procent af 100.000) og sender den til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Eksempel: Opret en faktureringsregel, der er baseret på en angivet procent for projektets fuldførelse (automatisk beregning)

Din organisation, som er et softwareudviklingsfirma, indgår en aftale om at udvikle en lønafregningspakke til en kunde for 30.000. Kunden indvilliger i at betale din organisation på grundlag af procentdelen af fuldført arbejde. Du skønner, at projektomkostningerne beløber sig til 20.000. Projektkontrakten angiver de arbejdskategorier, der bruges i faktureringsprocessen. Du konfigurerer faktureringsregler, der automatisk beregner fakturabeløbene for den procentdel af arbejdet, der er fuldført for de enkelte kategorier. Du konfigurerer et budget for hver kategori:

-   **Udvikling** – Udgifter på 15.000 og omsætning på 20.000
-   **Udrulning** – Udgifter på 5.000 og omsætning på 10.000

Første gang du opretter en kundefaktura, beregnes fakturabeløbet automatisk på baggrund af følgende oplysninger:

-   Efter en måned sender arbejderen på projektet en timeseddel for projektet. Omkostningerne til arbejderens timer er 5.000 for udvikling og 1.000 til installation. Udviklingsarbejdet er 33 procent fuldført (5.000 i faktiske omkostninger/15.000 i budgetomkostninger), og installationsarbejdet er 20 procent fuldført (1.000 i faktiske omkostninger/5.000 i budgetomkostninger).
-   Fakturabeløbet på 8.667 beregnes automatisk (33 procent af 20.000 + 20 procent af 10.000).
-   Du opretter en faktura på 8.667 og sender den til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Eksempel: Opret en faktureringsregel, der er baseret på aftalte milepæle

Din organisation er et ledelsesrådgivningsfirma, der er med til at udføre markedsundersøgelser for et forbrugerprodukt, som kunden har til hensigt at sælge. Kunden indvilliger i at bruge dine tjenester i en periode på tre måneder fra og med marts og accepterer at betale din organisation 50.000. Der er tre milepæle i projektet:

-   Milepæl 1: indsamling af forbrugerdata – 31. marts
-   Milepæl 2: analyse af forbrugerdata – 30. april
-   Milepæl 3: fremlæggelse af et forslag til produktets levedygtighed – 31. maj

Kunden indvilliger i at betale din organisation 10.000 for den første milepæl, 20.000 for den anden milepæl og 20.000 for den tredje milepæl. 

Når du konfigurerer projektkontrakten, accepterer du at fakturere kunden på baggrund af den milepæl, der er fuldført. Opsætningen af faktureringsreglen omfatter følgende trin:

-   Definer projektets milepæle.
-   Definer det beløb, kunden skal faktureres, når de enkelte milepæle er fuldført.

Når den første milepæl er fuldført den 31. marts, markerer du milepælen som fuldført og opretter derefter en faktura lydende på 10.000 og sender den til kunden. Du kan ikke oprette en faktura for en milepæl, før du har markeret milepælen som fuldført.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Eksempel: Opret en faktureringsregel, der er baseret på tjenester plus et administrationsgebyr

Din organisation, et ledelsesrådgivningsfirma, indgår en aftale om at udføre markedsundersøgelser for at vurdere levedygtigheden for et produkt, som kunden, et detailfirma, udvikler. Vilkårene for aftalen angiver, at du vil stille dine tre bedste ledelseskonsulenter til rådighed, som udfører undersøgelsen på tids- og materialebasis. Kunden indvilliger i at betale 100 pr. time plus et administrationsgebyr på 10 procent for de konsulenttimer, der tilskrives projektet. 

Når du konfigurerer projektkontrakten, skal du oprette en faktureringsregel for at tilføje et administrationsgebyr på 10 procent til de konsulenttimer, der tilskrives projektet. 

Når du opretter en faktura for kunden, faktureres kunden et administrationsgebyr på 10 procent plus prisen for konsulenttimerne. Hvis de tre konsulenter f.eks. har arbejdet i alt 200 timer på projektet, oprettes der en faktura på 22.000, der er baseret på følgende beregning:

-   200 timer ved 100 pr. time = 20.000
-   10 procent administrationsgebyr = 2.000
-   Samlet fakturabeløb = 22.000

Hvis gebyrer er momspligtige for en kunde, og du vælger en momsgruppe i projektkontrakten, angives momsgruppen automatisk som en faktureringsregel for gebyrer.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Eksempel: Opret en faktureringsregel for værdien af tid og materialer

Din organisation, som er en softwarekonsulentvirksomhed, indgår aftale om at stille fem tekniske konsulenter til rådighed til at arbejde på et softwareudviklingsprojekt for en kunde i de næste seks måneder. Kunden indvilliger i at betale 150 for hver konsulenttime samt udgifterne til kontorartikler. Din organisation sender en faktura til kunden i slutningen af hver måned. 

Når du konfigurerer projektkontrakten, indvilliger du i at fakturere kunden hver måned for tid og materialer anvendt på projektet. Du opretter en faktureringsregel, der indeholder følgende oplysninger:

-   Kontraktperioden er på seks måneder.
-   Konsulenttid beregnes med en sats på 150 pr. time.
-   Kontorartikler faktureres til kostpris, og de samlede omkostninger for projektet må ikke overstige 10.000.
-   Du opretter en faktura til kunden i slutningen af hver kalendermåned, så længe projektet er i gang.

I løbet af den første måned registreres der i alt 800 konsulenttimer på projektet. Kostprisen for de kontorartikler, der tilskrives projektet, er 2.000. I slutningen af måneden opretter du derfor en faktura på 122.000, som beregnes som 800 timer af 150 pr. time, plus 2.000 til kontorartikler.





[!INCLUDE[footer-include](../includes/footer-banner.md)]