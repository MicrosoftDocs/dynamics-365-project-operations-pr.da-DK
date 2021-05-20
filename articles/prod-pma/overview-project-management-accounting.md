---
title: Oversigt over projektstyring og regnskab
description: Funktionerne til projektstyring og regnskab kan bruges i flere brancher til at levere en tjeneste, fremstille et produkt eller opnå et resultat.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f6ceabe1809cc94357a31f1d57c445593f0f788
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950437"
---
# <a name="project-management-and-accounting-overview"></a>Oversigt over projektstyring og regnskab

[!include [banner](../includes/banner.md)]

Funktionerne til projektstyring og regnskab kan bruges i flere brancher til at levere en tjeneste, fremstille et produkt eller opnå et resultat.  

Et projekt er en gruppe aktiviteter, der er udviklet til at levere en tjeneste, fremstille et produkt eller opnå et resultat. Projekterne forbruger ressourcer og genererer økonomiske resultater i form af indtægter eller aktiver.

## <a name="projects-across-industries"></a>Projekter på tværs af brancher
Funktionaliteten for projektstyring og regnskab kan bruges i flere brancher, som vist i følgende illustration.

[![Projekter på tværs af brancher](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

I et callcenter kan en billet bruges til at beskrive det sæt handlinger, der kræves for at løse et kald. Konsulentfirmaer, f.eks. administrative organisationer eller tekniske rådgivningsorganisationer, anser deres aktiviteter for at være projekter. Inden for marketing repræsenterer en kampagne en række arbejde, som skal leveres. I projektbaseret produktion relaterer en produktionsordre sig til de forskellige arbejdsopgaver, der skal udføres for at fremstille nogle færdigvarer. Uanset hvad de kaldes, omfatter disse projekter ressourcer, planer og omkostninger, og funktionaliteten for projektstyring og regnskab kan hjælpe med at planlægge, udføre og analysere disse projekter.

## <a name="project-phases"></a>Projektfaser
Selvom følgende procesforløb er rettet mod eksterne projekter eller projekter, der er fuldført for en eller flere kunder, gælder funktionaliteten også for interne projekter, der udelukkende er omkostningsbaserede. 

![3 projektfaser](./media/3-stages-of-a-project.png) 

Som vist i den foregående illustration, kan projektstyring og regnskab inddeles i tre faser:

1.  Opstart
2.  Udfør
3.  Analyser

## <a name="initiate-the-project"></a>Opstart af projektet
I forbindelse med opstarten af projektet indtræder der flere nøgleprocesser. Du kan bruge et projekttilbud til at kommunikere den anslåede arbejdstid, udgifterne og materialerne til kunden. Du kan registrere faktureringsvilkårene, begrænsningerne og aftalerne i en projektkontrakt. Du kan bruge et arbejdsopgavehierarki til at planlægge og vurdere arbejdet. Du kan konfigurere prognoser og budgetter for at styre projektafviklingen. I følgende illustration vises strukturen for et projekt.[![projektstruktur](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Opret projekttilbud

I et projekts første salgsfase vil et projekttilbud gøre det muligt for dig at give kunden et ikke-bindende tilbud. Et tilbud kan indeholde elementer såsom de varer og tjenester, der er indeholdt i tilbuddet, grundlæggende kontaktoplysninger, særlige handelsaftaler og rabatter samt eventuelle skatter og tillægsafgifter.

Du kan også udstede en garanti for en projekttilbudstransaktion mellem din organisation og kunden. Når projekttilbuddet er oprettet, kan du oprette garantianmodningen for kunden og sende den til banken. Når banken har godkendt anmodningen, udstedes garantien til kunden. 

Du kan finde flere oplysninger i [Projekttilbud](project-quotations.md).

### <a name="create-project-contracts"></a>Opret projektkontrakter

Når du indgår en aftale med en kunde eller en anden finansieringskilde om at fuldføre et projekt, skal du først oprette en projektkontrakt. Når du derefter opretter projektet, skal du tildele det til den tilknyttede kontrakt. Projekttypen, som du har oprettet for en projektkontrakt, bestemmer den metode, der bruges til at fakturere projektkunderne. Du kan ændre en projektkontrakt og det relaterede projekt, men du kan ikke ændre projekttypen. Du kan finde flere oplysninger om projekttyper i sektionen "Oprettelse af projekter".

Du kan finde flere oplysninger om projektkontrakter i [Projektkontrakter](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Opret arbejdsopgavehierarkier

Detaljeringsgraden i et WBS afhænger af det præcisionsniveau, der kræves i estimater, og det sporingsniveau, der kræves mod disse estimater. Projekter med meget lav tolerance for overskridelser i relation til planlægning eller omkostninger kræver som regel et mere detaljeret WBS, og det kræver også behørig sporing af arbejdets fremgang og omkostningerne i forhold til WBS. 

Du kan finde flere oplysninger i [Oversigt over arbejdsopgavehierakier](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Opret projektprognoser og budgetter

Du kan bruge prognoser, hvis din organisation har et operationelt perspektiv og fokuserer på indtægter og omkostninger, der er afledt af bestemte transaktioner. Men hvis organisationen fokuserer mere på økonomiske beløb, kan du bruge budgettering. Hver metode har sine fordele. Du kan finde flere oplysninger i [Projektprognoser og budgetter](project-forecasts-budgets.md).

### <a name="create-projects"></a>Opret projekter

Du kan oprette seks projekttyper i Finance. De enkelte projekttyper konfigureres anderledes i forbindelse med omkostninger og indtægtsføring. Den projekttype, du vælger, afhænger af formålet med projektet. I tabellen nedenfor finder du en beskrivelse af den mest almindelige brug af de enkelte projekttyper.
                                                                                                            
<table>
  <tr>
    <td>Projekttype</th>
    <td>Beskrivelse</th>
  </tr>
  <tr>
    <td>Tid og materiale</td>
    <td>I tids- og materialeprojekter faktureres kunden for alle omkostninger, der påløber et projekt. Disse omkostninger inkluderer omkostninger for timer, udgifter, varer og gebyrer.</td>
  </tr>
  <tr>
    <td>Fast pris</td>
    <td>I fastprisprojekter består fakturaerne af aconto-transaktioner. Et fastprisprojekt faktureres i henhold til en faktureringsplan, der er baseret på en projektkontrakt. Omsætning for et fastprisprojekt kan beregnes og bogføres i hele projektets forløb ved hjælp af fuldførelsesprocentmetoden. Du kan også beregne og bogføre en omsætning, når projektet er fuldført, ved hjælp af fuldført kontrakt-metoden. Det er ofte gavnligt for virksomhederne at bruge værdien for igangværende arbejde (IGVA) til at beregne graden af et projekts eller en gruppe af projekters fuldførelse.</td>
  </tr>
  <tr>
    <td>Investering</td>
    <td>Investeringsprojekter er projekter, der ikke giver øjeblikkelig indtjening. De bruges typisk til langfristede interne projekter, hvor omkostningerne skal kapitaliseres. Der kan kun registreres omkostninger for varer, timer og udgifter for et investeringsprojekt. Omkostningerne i et investeringsprojekt spores og kontrolleres ved hjælp af estimatfunktionen. Investeringsprojekter kan konfigureres med en valgfri maksimal kapitalisering. Efterhånden som investeringsprojektet skrider frem, registrerer du dets omkostninger i IGVA-konti, hvor omkostningerne opbevares, indtil projektet er fuldført. Når projektet elimineres, kan du overføre værdien for IGVA til et anlægsaktiv, en finanskonto eller et nyt projekt. <br></br> <strong>BEMÆRK:</strong> Transaktioner på investeringsprojekter vises ikke på siden <strong>Bogfør omkostninger<strong>, <strong>Akkumuler omsætning</strong> eller <strong>Opret fakturaforslag</strong>.</td>
  </tr>
  <tr>
    <td>Omkostningsprojekt</td>
    <td>På samme måde som investeringsprojekter bruges omkostningsprojekter typisk til at spore interne projekter, og der kan kun registreres timer, udgifter og varer for dem. Omkostningsprojekter er dog som regel af kortere varighed end investeringsprojekter. I modsætning til investeringsprojekter kan omkostningsprojekter heller ikke kapitaliseres i statuskonti. I stedet bogføres projekttransaktionerne kun på driftskonti. <br></br> <strong>BEMÆRK:</strong> Transaktioner på omkostningsprojekter afspejles ikke på siden <strong>Bogfør omkostninger</strong>, <strong>Akkumuler omsætning</strong> eller <strong>Opret fakturaforslag</strong>. Da omkostningsprojekter typisk bruges til at spore interne projekter, skal de normalt ikke knyttes til en kundekonto. Men hvis opsætningen kræver, at der oprettes varebehov for indkøbsordrer, skal du knytte omkostningsprojektet til en kunde. Denne tilknytning er obligatorisk, da varebehov administreres som salgsordrelinjer, og systemet kræver, at der skal angives en kunde. Men denne opsætning vil ikke medføre, at der automatisk oprettes varebehov ud fra en indkøbsordre. I forbindelse med omkostningsprojekter ignoreres indstillingen <strong>Opret varebehov</strong>. Hvis du har brug for et varebehov i et omkostningsprojekt, kan du oprette det manuelt, forudsat at der er knyttet en kunde til projektet.</td>
  </tr>
  <tr>
    <td>Intern</td>
    <td>Interne projekter bruges til at spore omkostninger for et projekt, der er internt i organisationen. Interne projekter kan tilvejebringe et planlægningsværktøj til administration af ressourceforbrug. <br></br><strong>BEMÆRK:<strong> Transaktioner på interne projekter afspejles ikke på siden <strong>Bogfør omkostninger</strong> eller <strong>Opret fakturaforslag</strong>.</td>
  </tr>
  <tr>
    <td>Time</td>
    <td>Tidsprojekter bruges til at spore tid, der er knyttet til ikke-fakturerbare og ikke-produktive aktiviteter, som f.eks. et projekt, der sporer sygefravær for arbejdere. Transaktioner i tidsprojekter bogføres ikke i finanskladden. De indgår i stedet i rapporter over arbejderens tidsforbrug. Der kan kun registreres timetransaktioner i tidsprojekter. Du bruger en timekladde eller timeseddel til at registrere disse timer i projektet. Når timerne er registreret, vises de som projekttransaktioner, men de har ikke tilsvarende bilagstransaktioner. <br></br><strong>BEMÆRK:</strong> Transaktioner på tidsprojekter afspejles ikke på siden <strong>Bogfør omkostninger</strong>, <strong>Akkumuler omsætning</strong> eller <strong>Opret fakturaforslag</strong>.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Tildel arbejdere, kategorier og ressourcer

Du kan planlægge arbejderressourcer på grundlag af enten kravene til og tidsplanen for et projekt eller arbejdernes færdigheder og tilgængelighed. Ved hjælp af funktionerne til ressourceplanlægning kan du anvende organisationens arbejdere mere effektivt. Du kan hurtigt finde de mest kvalificerede arbejdere, der er tilgængelige til at arbejde på dit projekt. Du kan også nemt se, hvordan disse arbejdere kan bruges mere effektivt i løbet af projektet. 

Her er nogle af de måder, du kan bruge ressourceplanlægningsfunktionen på:

-   Brug oplysninger om en arbejders attributter, som f.eks. uddannelse, færdigheder, certificeringer og projekterfaring, til at knytte arbejderen til kravene i et projekt.
-   Brug oplysninger om en arbejders kalender og tilgængelighed, så den stemmer overens med arbejderens tidsplan i projektkalenderen.
-   Gennemse hver arbejders kapacitet og find ud af, hvordan denne kapacitet bruges. Hvis en arbejder f.eks. ikke bruges nok, kan arbejderen tildeles til et projekt, der passer til vedkommendes tilgængelighed og attributter.
-   Gennemse en arbejders tilgængelighed for at sikre, at der ikke er konflikter mellem arbejderens tildelinger i kalenderen.
-   Gennemse oplysninger om arbejderens tidsforbrug i enten en oversigtsvisning (f.eks. efter afdeling eller pr. arbejder) eller i en detaljeret visning (f.eks. efter arbejdere i en afdeling eller efter ugentlige detaljer for hver arbejder).
-   Tilpas ressourcetildelinger for forskellige tidsenheder, som f.eks. dag, uge eller måned, for at optimere den måde, arbejderne anvendes på.

## <a name="execute-the-project"></a>Udfør projektet
I forbindelse med projektets udførelse registrerer teammedlemmer eller ledere det arbejde og de udgifter, der er afholdt, ved hjælp af timesedler, udgiftsrapporter og andre forretningsdokumenter. Projektledere har værktøjer, der giver dem mulighed for at overvåge forbruget af budgetterede beløb for projektet. Projektledere kan også bestille, plukke eller fremskaffe materiale til projekter ved hjælp af indkøbsordrer og andre forretningsdokumenter. Fakturaer udarbejdes og godkendes, så kunderne kan faktureres for igangværende arbejde. Endelig registreres omsætningen under denne proces, hvilket betyder, at organisationens finansiering er blevet påvirket.

### <a name="manage-work-breakdown-structures"></a>Administrer arbejdsopgavehierarkier

En WBS er en beskrivelse af det arbejde, der skal fuldføres for et projekt. En WBS er et hierarki af opgaver. Den repræsenterer ikke kun arbejdet for de enkelte opgaver, men også størrelsen, omkostningerne og varigheden af en opgave. 

Du kan finde flere oplysninger i [Oversigt over arbejdsopgavehierakier](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Administrer projektprognoser og budgetter

Du kan administrere og styre dine projekter på to måder: projektprognoser og projektbudgetter. Du kan bruge prognoser, hvis din organisation har et operationelt perspektiv og fokuserer på indtægter og omkostninger, der er afledt af bestemte transaktioner. Men hvis organisationen fokuserer mere på økonomiske beløb, kan du bruge budgettering.

Du kan finde flere oplysninger i [Projektprognoser og budgetter](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Opret produktionsordrer

En projektrelateret produktionsordre kan knyttes til en salgsordre eller et varebehov enten ved hjælp af metoden for en færdig vare eller metoden for en forbrugt vare. Hvis produktionsordren er oprettet manuelt, er der desuden ingen tilknytning mellem produktionsordren og salgsordren eller varebehovet (ingen tilknytning til ordre). Men hvis produktionsordren blev oprettet automatisk for at opfylde en salgsordre eller et varebehov, er der en forbindelse mellem produktionsordren og salgsordren eller varebehovet (tilknytning til ordre). 

Afhængigt af kombinationerne af disse faktorer kan du benytte en af følgende fremgangsmåder:

- **Færdig vare/tilknytning til ordre** – Sammenkæd projektet med en salgsordre eller et varebehov. Når du bruger denne metode, bogføres de faktiske projektomkostninger, når salgsordren faktureres, eller når følgesedlen opdateres for varebehovet. Omkostningen bogføres som en færdig vare.
- **Færdig vare/ingen tilknytning til ordre** – Det er ikke muligt at bogføre faktiske omkostninger, før produktionscyklussen for en vare har statussen **Afsluttet**. Omkostningen for færdigvaren bogføres som en enkelt transaktion.
- **Forbrugt vare/tilknytning til ordre** – Sammenkæd projektet med et varebehov. Ved hjælp af denne metode kan du få vist de faktiske projektomkostninger, når produktionen har statussen **Igangsat** eller er blevet rapporteret som færdig. Omkostningerne bogføres som flere transaktioner for vareposteringer for projekter i relation til råmaterialer og timer, der er brugt på produktionen. Når følgesedlen opdateres for varebehovet, bogføres der ingen projektomkostninger. Du kan også definere det niveau i styklistehierarkiet, hvor projekterne i produktionen spores.
- *<strong><em>Forbrugt vare/ingen tilknytning til ordre</em></strong>* – Sammenkæd projektet med et varebehov. Ved hjælp af denne metode kan du få vist de faktiske projektomkostninger, når produktionen har statussen <strong>Igangsat</strong> eller er blevet rapporteret som færdig. Omkostningerne bogføres som flere transaktioner for vareposteringer for projekter i relation til råmaterialer og timer, der er brugt på produktionen. Du kan også definere det niveau i styklistehierarkiet, hvor projekterne i produktionen spores.

### <a name="procure-products-and-services"></a>Fremskaf produkter og tjenester

Køb og salg af varer er f.eks. almindeligt forevisende aktiviteter i mange projektorienterede virksomheder.

#### <a name="purchase-orders-for-projects"></a>Indkøbsordrer for projekter

Formålet med indkøbsordren bestemmer, hvornår indkøbsordren forbruges, og derfor hvornår varerne debiteres på et projekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Formål</th>
<th>Forbrug af varer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Opret en indkøbsordre direkte.</td>
<td>Køb varer fra en ekstern leverandør, som skal forbruges i et projekt. Du kan oprette indkøbsordren på følgende måder:
<ul>
<li>Fra selve projektet. I dette tilfælde er projektet allerede defineret for indkøbsordren.</li>
<li>Ved at gå til projektets indkøbsordre. Du skal både vælge den leverandør og det projekt, som du vil oprette indkøbsordren for.</li>
</ul></td>
<td>Varer forbruges, når leverandørfakturaen opdateres.</td>
</tr>
<tr class="even">
<td>Opret en indkøbsordre fra en salgsordre.</td>
<td>Køb varer, når du opretter en salgsordre fra et projekt.</td>
<td>Varerne forbruges, når salgsordren faktureres til kunden.</td>
</tr>
<tr class="odd">
<td>Opret en indkøbsordre ud fra et varebehov.</td>
<td>Køb varer, når du opretter et varebehov fra et projekt.</td>
<td>Varer forbruges, når følgesedlen til varebehovet opdateres.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Salgsordrer for projekter

I Projektstyring og regnskab kan du registrere forbruget af varer på forskellige måder. Du kan sælge varer eller købe varer fra et projekt eller reservere varer til et projekt. 

Du kan bestille varer fra firmaets lager med henblik på at forbruge dem i et projekt. Du kan også købe varer fra en ekstern leverandør. Der kan forbruges varer på alle typer projekter undtagen tidsprojekter. 

Den måde, du bestiller varer på, afhænger af, hvor du bestiller dem fra:

-   Hvis du vil bestille varer fra firmaets lager, skal du angive ordren som et varebehov. Hvis du bruger siden **Varebehov**, kan du konfigurere behovet, så du modtager varerne som delleverancer. Du kan derfor udskyde forbruget af et antal varer, indtil der er brug for varerne.
-   Hvis du vil bestille varer fra en ekstern leverandør, skal du oprette ordren som en indkøbsordre på siden **Indkøbsordre**.

> [!NOTE] 
> Følgesedlen for en projektrelateret salgsordre kan ikke annulleres, hvis varerne allerede er markeret til emballering. 

I følgende tabel vises de metoder, der bruges til at bestille varer, og det beskrives, hvordan varerne forbruges.

| Metode            | Formål                                                                                                                                                        | Forbrug af varetransaktioner                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Salgsordre       | Angiv en transaktion direkte i et tids- og materialeprojekt.                                                                                                   | Varetransaktioner forbruges, når kundefakturaen bogføres.                                                                               |
| Lagerkladde | Angiv og vedligehold hurtigt vareposter. Hvis du f.eks. vil angive et varebehov, der er baseret på en udskrevet oversigt, kan du anvende lagerkladden. | Varetransaktioner forbruges, når kladden bogføres.                                                                                        |
| Varebehov  | Angiv de varer, der ikke skal forbruges med det samme. Med denne metode kan du spore antallet af varer, der er forbrugt i en enkelt varebehovspost.    | Varetransaktioner forbruges, når følgesedlen opdateres. Det vil sige, at varebehovet oprettes, når følgesedlen bogføres. |
| Indkøbsordrer   | Angiv transaktionerne på en af tre lokationer, afhængigt af indkøbsmetoden.                                                                              | Varetransaktioner forbruges, når følgesedlen opdateres, eller når kunden eller leverandøren faktureres.                                      |

### <a name="process-project-invoices"></a>Behandl projektfakturaer

Projekttypen bestemmer, hvilken faktureringsprocedure der skal anvendes. Der er kun de to eksterne projekttyper (tids- og materialeprojekter samt fastprisprojekter), som kan faktureres. Tids- og materialeprojekter samt fastprisprojekter er altid knyttet til en projektkontrakt. 

Før du opretter en kundefaktura for et projekt, kan du oprette en foreløbig faktura eller et fakturaforslag. I et fakturaforslag kan du vælge projekttransaktioner, der skal inkluderes i en projektfaktura. Du kan derefter gennemse fakturaoplysningerne, inden du bogfører projektfakturaen og sender den til kunden eller en anden finansieringskilde. 


Du finder flere oplysninger om, hvordan du behandler projektfakturaer i [Projektfakturering](/dynamics365/finance/accounts-payable/project-invoicing).


### <a name="calculate-the-cost-to-complete-a-project"></a>Beregn omkostningerne for at fuldføre et projekt

Når du opretter et estimat, kan du vælge den metode, der skal bruges til at beregne færdiggørelsesomkostningerne for projektet. Du kan vælge en metode i feltet **Færdiggørelsesomkostningsmetode** på siden **Opret estimat**. Den metode, du vælger, anvendes separat på de enkelte omkostningslinjer i omkostningsestimatet. Mens en linje har statussen **Oprettet**, kan du ændre den metode, der anvendes på den, på siden **Omkostningsestimat**. 

I tabellen nedenfor finder du en beskrivelse af de metoder, du kan anvende til at beregne omkostningerne for at fuldføre et projekt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Samlede omkostninger - faktiske</td>
<td>De estimerede omkostninger skal angives manuelt. Når kolonnen <strong>Samlede omkostninger</strong> eller <strong>Samlet antal</strong> på siden <strong>Omkostningsestimat</strong> er fuldført, trækkes de faktiske omkostninger fra de brugerindtastede totaler. Resultatet er omkostningerne ved at fuldføre projektet. Normalt spores statussen ikke på basis af f.eks. det antal hotelophold og måltider, der er registreret i hver periode. I stedet. Sporing er normalt baseret på en sammenligning af det samlede antal forventede timer. Denne fremgangsmåde kræver ikke en prognosemodel, og de samlede omkostninger eller det samlede antal kan ændres manuelt. Når der angives en værdi i kolonnen <strong>Samlede omkostninger</strong> eller <strong>Samlet antal</strong>, sammenligner Finance værdien med de faktiske transaktioner, der er bogført i perioden, og derefter reduceres værdien i kolonnen <strong>Antal, der skal fuldføres</strong> eller <strong>Fuldførelsesomkostninger</strong>.</td>
</tr>
<tr class="even">
<td>Samlet budget – faktisk</td>
<td>De faktiske omkostninger sammenlignes med den budgetmodel, du vælger, for at bestemme omkostningerne. I denne metode bruges en samlet budgetmodel, der inkluderer planlagte transaktioner. Hvis du vil opnå en mere nøjagtig visning af projektet, kan du justere budgetmodellen, når projektet er igangværende. Hvis du vil justere prognosen, skal du følge denne generelle proces:
<ol>
<li>Kopier prognosetransaktionerne til en anden prognosemodel.</li>
<li>Sammenlign prognosetransaktionerne med de faktiske transaktioner.</li>
<li>Fasthold, reducer eller forøg estimaterne for den næste periode.</li>
</ol>
Finance reducerer ikke estimeringerne automatisk. Det er derfor en god ide at bevare en oprindelig prognosemodel for fastprisprojektet for at fastlægge en basislinje for sammenligning, når projektet er fuldført. 
<br></br> <strong>BEMÆRK:</strong> Når du vælger denne metode, skal du bruge mindst to prognosemodeller. En model bør indeholde det oprindelige budget. I forbindelse med den anden model skal du kopiere prognosetransaktionerne fra en anden model. Denne metode er kun gyldig i forbindelse med fastpris- og investeringsprojekter.</td>
</tr>
<tr class="odd">
<td>Resterende budget</td>
<td>I denne metode bruges en resterende budgetmodel til at beregne færdiggørelsesomkostningerne for projektet. Når du bruger denne metode, lægges de faktiske omkostninger og de estimerede beløb i den resterende budgetmodel sammen. Resultatet er en samlet omkostning. Før du bruger denne metode, skal der være konfigureret en resterende budgetmodel til at fratrække transaktioner, der er baseret på faktiske transaktioner, som er registreret i systemet. På siden <strong>Prognosemodeller</strong> skal du sikre dig, at felterne er markeret i gruppen <strong>Automatisk prognosereduktion</strong>. Et resterende budget kopieres typisk fra et oprindeligt budget. Transaktionerne i det resterende budget reduceres, efterhånden som der indtastes transaktioner. Efterhånden som projektet skrider frem, kan du tilskrive de estimerede transaktioner på det resterende budget, hvis du finder ud af, at det resterende budget skal reguleres. <br></br> <strong>BEMÆRK:</strong> Denne metode kan kun anvendes, hvis der er knyttet en prognosemodel til estimatet.</td>
</tr>
<tr class="even">
<td>Som forrige estimat</td>
<td>Den samme estimatmetode, der blev brugt i den foregående periode, anvendes. Denne metode kræver en prognosemodel, hvis den forrige periode krævede en prognosemodel.</td>
</tr>
<tr class="odd">
<td>Angiv færdiggørelsesomkostninger til nul</td>
<td>Denne metode bruges typisk, før det estimerede projekt elimineres. Denne metode sammenholder de samlede estimeringer med de faktiske transaktioner, der er blevet bogført, og kolonnen <strong>Færdiggørelsesomkostninger</strong>. Den deraf følgende færdiggørelsesgrad er altid 100 procent. Feltet <strong>Prognose</strong> er ikke markeret for de enkelte omkostningslinjer, du opretter, og det samlede estimat kopieres fra det forrige omkostningsestimat. Det faktiske forbrug i estimatperioden trækkes fra færdiggørelsesomkostningerne for projektet. Denne metode kræver ikke en prognosemodel.</td>
</tr>
<tr class="even">
<td>Fra omkostningsskabelon</td>
<td>Den metode for færdiggørelsesomkostninger, der er konfigureret i den omkostningsskabelon, der er knyttet til det valgte forkalkulerede projekt, anvendes.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analysér projektet
På det mest grundlæggende niveau bruges et projekt til at gruppere transaktioner, der registrerer omkostninger, og derefter bogføre disse omkostninger i den finanskladden. 

Disse transaktioner er generelt set resultatet af forretningsdokumenter, som f.eks. timesedler, udgiftsrapporter, leverandørfakturaer eller lagertransaktioner. Et projekts livscyklus starter som regel med estimater, prognoser og budgetter, der hjælper med at planlægge og forudse projektets arbejde og økonomiske konsekvenser. Når du analyserer et projekt, kan du ikke kun evaluere de transaktioner, der er opstået i løbet af projektet, men også nøjagtigheden af dine estimater og prognoser, tidsforbrugsgraden for medlemmer af projektteamet samt det overordnede projekts succes.

### <a name="analyze-cash-flow"></a>Analysér pengestrøm

Brug overvågning af pengestrømme til at gennemgå både de anslåede pengestrømme og de faktiske pengestrømme for et projekt. Du kan gennemse pengestrømme, mens et projekt er igangværende, eller du kan få vist pengestrømme for et afsluttet projekt. 

Ved at overvåge pengestrømme kan du evaluere et enkelt projekt, bruge rapporterne til at få vist flere projekter og overføre projektpengestrømer til likviditetsprognoser i finanskladden.

#### <a name="cash-inflow-forecasting"></a>Prognose over likviditetstilgang

Afhængigt af din konfiguration kan du udarbejde en prognose for likviditetstilgangen for et valgt projekt. Hvis projektdatoen f.eks. er den 5. marts 2012, og du fakturerer den 31. marts 2012, kan du her se, hvordan du kan forudsige forfaldsdatoen og den forventede salgsbetalingsdato:

-   **Projektdato:** 5. marts 2012.
-   **Fakturadato:** 31. marts 2012. Denne dato bestemmes ud fra fakturafrekvensen. I dette eksempel skal du angive fakturafrekvensen til den aktuelle måned. Alle transaktioner, der bogføres i marts måned, faktureres derfor den sidste dag i måneden.
-   **Forfaldsdato:** 14. april 2012. Denne dato bestemmes ud fra de betalingsbetingelser, der blev angivet for projektet. I dette eksempel har du valgt betalingsbetingelser på 14 dage. Der føjes derfor 14 dage til fakturadatoen, som skal forfalde den 14. april 2012.
-   **Forventet salgsbetalingsdato:** 27. april 2012. Denne dato beregnes ved at tilføje antallet af dage i feltet **Generelle bufferdage** på siden **Projektstyring og regnskabsparametre** til antallet af dage i feltet **Individuelle bufferdage** på siden **Projektkontrakter** og derefter tilføje totalen til antallet af dage i feltet **Forfaldsdato**. I dette eksempel har du angivet **3** i feltet **Generelle bufferdage** og **10** i feltet **Individuelle bufferdage**. Der føjes derfor 13 dage til forfaldsdatoen, som er sammenfaldende med en forventet salgsbetalingsdato, der er angivet som den 27. april 2012.

De generelle bufferdage kan enten erstatte de enkelte bufferdage eller blive tilføjet til de enkelte bufferdage:

-   Hvis du vil bruge de generelle bufferdage i stedet for de enkelte bufferdage, skal du angive det gennemsnitlige antal dage mellem forfaldsdato og den faktiske betalingsdato for kunder.
-   Hvis du vil tilføje de generelle bufferdage til de enkelte bufferdage, skal du i feltet **Generelle bufferdage** angive dit estimat for antallet af dage mellem den dag, hvor kunden sender betalingen, og den dag, hvor din organisation modtager betalingen.

Konfigurer individuelle bufferdage i projektets kontrakt. Dagene beregnes på baggrund af både forfaldsdato for salgsfaktura og din organisations erfaring med en kundes betalingsmønster.

#### <a name="actual-cash-inflow"></a>Faktisk likviditetstilgang

Den faktiske likviditetstilgang ligner prognoser, men du kan begynde at foretage beregninger fra den første fakturadato. Her er et eksempel:

-   **Fakturadato:** 2. marts 2012.
-   **Forfaldsdato:** 16. marts 2012. Betalingsbetingelserne er angivet til 14 dage.
-   **Forventet salgsbetalingsdato:** 29. marts 2012. Beregningen inkluderer tre almindelige bufferdage og 10 individuelle bufferdage.

#### <a name="cost-forecasting"></a>Omkostningsprognose

På baggrund af de dage, der er defineret, kan omkostningsbetalingsdatoen være forskellig fra projektdatoen. I dette tilfælde beregnes omkostningsbetalingsdatoen ved at tilføje antallet af dage fra projektdatoen til antallet af dage i betalingsbetingelserne. 

Projektdatoen for transaktionen er f.eks. den 5. marts 2012, og følgende betalingsbetingelser angives:

-   **Tidspunkt:** Indeværende måned (**M**)
-   **Udgifter:** 14 dage (**D14**)
-   **Varer:** 30 dage (**D30**)

Afhængigt af disse indstillinger er omkostningsbetalingsdatoen for de enkelte posteringstyper i dette tilfælde:

-   **Tidspunkt:** 31. marts 2012, som er den sidste dag i den valgte måned.
-   **Udgifter:** 19. marts 2012, som er 14 dage efter transaktionsdatoen.
-   **Varer:** 4. april 2012, som er 30 dage efter transaktionsdatoen.

> [!NOTE] 
> Forfaldsdatoen for indkøbsordren er baseret på leverandørtransaktionen, når projektindkøbsordren oprettes. Forfaldsdatoen bestemmes ikke af standardindstillingerne. 

Omkostningsbetalingsdatoen beregnes ikke for bufferdage. Når et projekt er fuldført, og alle omkostningsberegninger og fakturering er fuldført, bogføres både omkostningerne og salget til driftskonti. 

Når alle salgs- og leverandørfakturaer er fuldført, kan du få vist relationen mellem felter på siden **Likviditet** og felter på siden **Projektopgørelser**.

:::row:::
    :::column:::
        #### <a name="cash-flow-page"></a>Likviditetsside
        - Likviditetstilgange 
        - Likviditetsafgange
        - Nettolikviditet
    :::column-end:::
    :::column:::
        #### <a name="project-statements-page"></a>Projektopgørelsessiden
        - Omsætning
        - Samlet omkostning
        - Bruttoavance
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Gennemse omkostninger

Du kan overvåge de omkostninger, der opstår i organisationen i forbindelse med et projekt, på siden **Omkostningsstyring**. Ved at sammenligne de oprindelige budgetterede omkostninger for projektet med de aktuelle faktiske omkostninger og de bindende omkostninger kan du afgøre, om projektet er på rette spor, har overskredet budgettet eller er under budgettet. 

> [!NOTE] 
> Når du bruger siden **Omkostningsstyring** til at få vist den aktuelle status for projektomkostninger, skal du bruge de prognosemodeller, der blev valgt til det oprindelige og det resterende budget. Hvis du vælger andre prognosemodeller, når du beregner omkostninger, er beregningerne ikke nøjagtige.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Få vist de resterende budgetterede beløb

Hvis **Resterende budget** er valgt som metode for omkostningsstyring på siden **Projektstyring og regnskabsparametre**, beregner siden **Omkostningsstyring** de omkostninger, der ikke er blevet bogført som faktiske eller markeret som bindende. Beløbene under fanen **Generelt** i den nederste rude på siden **Omkostningsstyring** beregnes mere specifikt på følgende måder:

-   **Faktisk omkostning** – Det samlede beløb, der er brugt på projektet for den valgte omkostningslinje. Det faktiske omkostningsbeløb beregnes på siden **Finansopdateringer**.
-   **Bindende omkostning** – Det ekstra udgiftsbeløb, som den juridiske enhed har givet tilsagn om at betale. De specifikke bindende omkostninger beregnes på siden **Bindende omkostninger**.
-   **Resterende budget** – Den del af det oprindelige budgetterede beløb, der stadig er tilgængeligt for den valgte omkostningslinje. Det resterende budgetbeløb beregnes på siden **Forhåndsvisning af finanskladden**.
-   **Samlede omkostninger** – Summen af de faktiske omkostninger, bindende omkostninger og resterende budgetbeløb.

På siden **Omkostningsstyring** under fanen **Afvigelse** kan du se en sammenligning af de samlede forventede omkostninger med det oprindelige budget. Denne sammenligning viser eventuelle forskelle mellem disse beløb. Du kan derfor se, hvor dataene ikke stemmer overens. Afvigelsesbeløbene beregnes på følgende måder:

-   **Oprindeligt budget** – Det beløb, der oprindeligt blev budgetteret med for den valgte omkostningslinje. Det oprindelige budgetbeløb beregnes på siden **Forhåndsvisning af finanskladden**.
-   **Samlede omkostninger** – Summen af de faktiske omkostninger, bindende omkostninger og det resterende budget som rapporteret på fanen **Generelt**.
-   **Afvigelse** – Forskellen mellem de samlede omkostninger og det oprindelige budget.
-   **Afvigelse baseret på antal** – Den samlede difference mellem den oprindelige prognose og den samlede prognose. Forskellen kan udtrykkes matematisk som (samlet estimeret antal) × (oprindeligt gennemsnitspris – samlet gennemsnitspris). Denne beregning gælder kun for projekttimer.
-   **Forskel baseret på pris** – Den samlede difference mellem den oprindelige prognose og den samlede prognose. Forskellen kan udtrykkes matematisk som (oprindeligt estimeret pris) × (oprindeligt estimeret antal – samlet estimeret antal). Denne beregning gælder kun for projekttimer.

#### <a name="viewing-the-total-budgeted-amounts"></a>Få vist de samlede budgetterede beløb

Hvis **Det samlede budget** er valgt som metode for omkostningsstyring på siden **Projektstyring og regnskabsparametre**, beregner siden **Omkostningsstyring** de faktiske omkostninger og projektets samlede omkostninger for at hjælpe dig med at identificere eventuelle forskelle mellem de to. På siden **Omkostningsstyring** kan du i kolonnerne i den nederste rude på fanen **Generelt** specifikt se beløbene, som beregnes på følgende måder:

-   **Samlede budgetterede omkostninger** – Det samlede budgetterede beløb for den valgte omkostningslinje.
-   **Faktisk omkostning** – De samlede omkostninger, der er påløbet for projektet dags dato for de valgte omkostningslinjer.
-   **Bindende omkostning** – Det samlede beløb, der er givet tilsagn om for den valgte omkostningslinje.
-   **Afvigelse** – Forskellen mellem summen af faktiske og bindende omkostninger og de samlede omkostninger. Afvigelsen viser, om der skal angives yderligere omkostninger for det samlede budget.

På siden **Omkostningsstyring** under fanen **Afvigelse** kan du få vist forskellen mellem det samlede budget og det oprindelige budget ved at kigge på følgende felter:

-   **Oprindeligt budget** – Det beløb, der oprindeligt blev budgetteret med for omkostningslinjen. Det oprindelige budget beregnes på siden **Forhåndsvisning af finanskladden**.
-   **Samlede budgetterede omkostninger** – De samlede omkostninger, der oprindeligt blev budgetteret med for omkostningslinjen. De samlede budgetterede omkostninger beregnes på siden **Forhåndsvisning af finanskladden**.
-   **Afvigelse** – Afvigelsen for omkostningslinjen. Dette beløb beregnes ved at fratrække de samlede omkostninger fra det oprindelige budget.
-   **Afvigelse baseret på antal** – Den samlede difference mellem det oprindelige budget og det samlede budget. Dette beløb beregnes ved at trække de samlede budgetterede timer fra de oprindeligt budgetterede timer og derefter gange forskellen med den oprindelige budgetterede kostpris. Denne forskel kan udtrykkes matematisk som (oprindeligt budgetteret kostpris) × (oprindeligt budgetterede timer – samlet antal budgettimer). Denne beregning gælder kun for projekttimer.
-   **Afvigelse baseret på pris** – Dette beløb beregnes ved at trække de samlede budgetterede timer fra de oprindeligt budgetterede timer og derefter gange forskellen med det samlede antal forbrugte timer. Denne forskel kan udtrykkes matematisk som (samlet antal forbrugte timer) × (oprindeligt budgetterede timer – samlet antal budgettimer). Denne beregning gælder kun for projekttimer.

### <a name="analyze-utilization"></a>Analysér tidsforbrug

Tidsforbrugsgraden er den procentdel af tid, som en arbejder udfører fakturerbart eller produktivt arbejde i en bestemt arbejdsperiode. Fakturerbare timer er de antal timer, som en arbejder anvender, og som kan opkræves ved en bestemt kunde. 

En arbejders tidsforbrugsgrad beregnes ved at dividere antallet af fakturerbare timer med antallet af arbejdstimer i en bestemt periode. Hvis en arbejder f.eks. har 30 fakturerbare timer i en periode, og antallet af arbejdstimer i samme periode er 40, er procentandelen for arbejderens tidsforbrug 75. 

Når du beregner tidsforbrugsgraden for en arbejder, kan du enten beregne faktureringsgraden eller effektivitetsgraden:

-   **Faktureringsgrad** – Forskellen mellem fakturerbare timer og ikke-fakturerbare timer eller normtimer.
-   **Effektivitetsgrad** – Forskellen mellem produktive timer og ikke-produktive timer eller normtimer. Produktive timer er de timer, som arbejderen bruger til at bidrage til et bestemt projekt. Produktive timer faktureres typisk til kunder, undtagen i forbindelse med interne projekter. Ikke-produktive timer faktureres aldrig til en kunde.

Du beregner tidsforbrugsgrader på siden **Tidsforbrug i timer**. Beregningerne er baseret på standardindstillinger. Disse indstillinger angiver også, hvordan timer beregnes ved at tildele **Tidsforbrug** eller **Byrde** til hver enkelt projekttype. Dette gælder for beregninger af fakturerbare satser og beregninger af effektivitetsgrad.

-   **Tidsforbrug** – Antal timer, der rapporteres for den valgte projekttype, og som altid betragtes som fakturerbart eller effektivt tidsforbrug.
-   **Byrde** – Antal timer, der rapporteres for den valgte projekttype, og som altid betragtes som ikke-fakturerbart eller ineffektivt tidsforbrug.
-   **I henhold til linjeegenskab** – De enkelte linjeegenskaber for en bestemt timetransaktion bestemmer, om timerne anses for at være fakturerbart eller effektivt tidsforbrug.
-   **Ikke medtaget** – Timer medtages ikke i beregningen af fakturerbart eller effektivt tidsforbrug.

På siden **Tidsforbrug i timer** kan du, udover den samlede procent af tidsforbrugsgraden for en arbejders eller et projekts tidsforbrug, få vist det antal timer, der blev brugt til beregning af tidsforbrug for hver af følgende timetyper:

-   **Ikke-inkluderede timer** – Disse timer indgår ikke i tidsforbrugssatsen angivet i timer.
-   **Inkluderede timer** – Disse timer beregnes ved at tilføje tidsforbruget i timer og direkte tid. Disse timer inkluderes i tidsforbrugsgraden.
-   **Belastet tid** – Hvis du beregner en faktureringsgrad, er disse timer de samme som ikke-fakturerbare timer. Hvis du beregner en effektivitetsgrad, er disse timer de samme som ikke-produktive timer.
-   **Tidsforbrug i timer** – Hvis du beregner en faktureringsgrad, er disse timer de samme som fakturerbare timer. Hvis du beregner en effektivitetsgrad, er disse timer de samme som produktive timer.

Når du beregner tidsforbrugsgraden for en arbejder, kan du bruge normtimer eller inkluderede timer. Hvis du bruger inkluderede timer, skal du sikre dig, at arbejdere registrerer al arbejdstid i timeseddelperioderne, da beregningen udtrykkes som en procentdel af de timer, der er angivet. Når du beregner den timelige tidsforbrugssats for et projekt, en projektkontrakt, en kundepost eller en kategori, skal du bruge inkluderede timer i beregningen.

### <a name="review-project-statements"></a>Gennemse projektopgørelser

Du kan oprette en projektopgørelse for at få vist et hurtigt snapshot af et projekts fremgang. Når du kører en projektopgørelse, kan du specificere de kriterier, der bruges til at beregne opgørelsen, ved at foretage valg under fanen **Generelt** på siden **Projektopgørelser**. Du kan vælge at medtage eller udelade følgende oplysninger:

-   Projekttyper
-   Transaktionstyper
-   Projektdato/finanskladdedato
-   Data

Når opgørelsen er beregnet, kan du se følgende oplysninger under de forskellige faner på siden **Projektopgørelser**:

-   **Generelt** – Generelle oplysninger om projektets grundlæggende driftsstruktur.
-   **Drift** – Oplysninger om akkumuleret omsætning.
-   **IGVA** – Oplysninger om saldi for IGVA-konti.
-   **Forbrug** – Oplysninger om forbrug af timer, varer, udgifter og løntransaktioner.
-   **Faktura** – Oplysninger om fakturaer og acontofakturering.
-   **Timesats** – Timesatserne for timer, der bogføres på indtægts- og omkostningskonti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]