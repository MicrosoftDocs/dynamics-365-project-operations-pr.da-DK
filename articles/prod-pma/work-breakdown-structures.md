---
title: Oversigt over arbejdsopgavehierarkier
description: Et arbejdsopgavehierarki (WBS) er en beskrivelse af det arbejde, der skal udføres for et projekt. Det er et hierarki af opgaver, der repræsenterer projektteamets forståelse for arbejdskompositionen og størrelsen, omkostningerne samt varigheden af hver komponent eller opgave.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 093f9901aec0db1fa8f920533c0084f877f26445fd07159e8e1ae0cf53849641
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998814"
---
# <a name="work-breakdown-structures-overview"></a>Oversigt over arbejdsopgavehierarkier

[!include [banner](../includes/banner.md)]

Et arbejdsopgavehierarki (WBS) er en beskrivelse af det arbejde, der skal udføres for et projekt. Det er et hierarki af opgaver, der repræsenterer projektteamets forståelse for arbejdskompositionen og størrelsen, omkostningerne samt varigheden af hver komponent eller opgave. Et WBS har tre større formål:

-   Beskrive opdelingen eller kompositionen af opgaver.
-   Planlægge projektarbejdet.
-   Estimere omkostningerne for de enkelte opgaver.

Detaljeringsgraden i et WBS afhænger af det præcisionsniveau, der kræves i estimater, og det sporingsniveau, der kræves mod disse estimater. Projekter med meget lav tolerance for overskridelser i relation til planlægning eller omkostninger kræver som regel et mere detaljeret WBS og behørig sporing af arbejdets fremgang og omkostningerne i forhold til WBS. Denne form for projekt er almindelig i bygge- og anlægsbranchen. 

Projekter i brancher såsom medie- og reklamebranchen har til sammenligning som oftest enestående software- og IT-infrastruktur, og produktiviteten er relativ set i forhold til erfaringen og kompetencen for den person, der udfører opgaven. Disse brancher bruger derfor et WBS til at få en indbyrdes tilnærmelse af størrelsen på et projekt, og ikke til at spore projektets fremgang ned til mindste detalje. 

Opbygning af et WBS er en intensiv proces, der som regel udføres over en længere periode, og som kræver samarbejde og oplysninger fra en lang række personer. I dette emne beskrives, hvordan du kan bruge WBS-forbedringer til at overholde dine krav til estimater og sporing.

## <a name="prerequisites-for-creating-a-wbs"></a>Forudsætninger for oprettelse af et WBS
Hvis du vil oprette et WBS, skal du kunne oprette en arbejdsplan og vurdere omkostningerne til arbejdet.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Forudsætninger for at oprette en arbejdsplan

Hvis du vil bruge de fulde planlægningsfunktioner i WBS-funktionerne, skal du fuldføre følgende opsætning:

1.  Konfigurer en standardkalender og en projektkalender:
    1.  Klik på **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Projektstyring og regnskabsparametre** &gt; **Planlægning**. I feltet **Standardarbejdskalender** skal du angive en standardkalender. Denne arbejdskalender er standard for alle nye projekter, der oprettes.
    2.  Du kan ændre standardkalenderen for et bestemt projekt. Klik på projektets oplysningsside, og derefter skal i hurtigfanen **Projektteam og planlægning** opdatere feltet **Planlægningskalender** ved at vælge en anden kalender.

2.  Konfigurer standardarbejdsdage og arbejdstider. Den kalender, du har angivet som arbejdskalender for projektet, bruges i WBS til at bestemme følgende oplysninger:

-   Arbejdsdage og helligdage
-   Antallet af arbejdstimer på en dag

Hvis du vil angive arbejdsdage og arbejdstider for en kalender, eller hvis du vil oprette en ny kalender, skal du klikke på **Organisationens administration** &gt; **Almindelige** &gt; **Kalendere**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Forudsætninger for at vurdere arbejdsomkostningerne

Hvis du vil bruge de fulde kapaciteter for omkostningsestimering i WBS, skal du konfigurere omkostninger og salgspriser for arbejdere, kategorier af arbejde, udgifter og gebyrer samt varer.

-   Hvis du vil konfigurere kost- og salgspriser for kategorierne arbejde, udgifter og gebyr, skal du klikke på **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Priser**.
-   Hvis du vil konfigurere kost- og salgspriser for varer, skal du bruge siden **Handelsaftaler** for hver vare på listesiden **Frigivne produkter** i Administration af produktoplysninger.

## <a name="creating-a-wbs"></a>Oprettelse af WBS
Oprettelse af et WBS involverer tre aktiviteter:

1.  **Arbejdsfordeling** – Opret en opdeling af arbejde til håndterbare segmenter eller opgaver.
2.  **Arbejdsplan** – Estimer den tid, der kræves for at udføre en opgave, angive afhængigheder mellem opgaver og vælg start- og slutdatoer for opgaver.
3.  **Omkostningsestimering** – Estimer omkostninger for de enkelte opgaver.

I følgende sektioner drøftes det, hvordan du kan bruge WBS-funktionerne til hver af disse aktiviteter.

### <a name="work-decomposition"></a>Arbejdsopdeling

Oprettelse af en opdeling eller dekomposition af arbejde er som regel det første trin i processen til oprettelse af et WBS. WBS-funktionaliteten understøtter følgende grundlæggende konstruktioner for arbejdsfordeling eller dekomposition. 

**Rodopgave for projekt** Projektets rodopgave er den opsummerende opgave på øverste niveau for et projekt. Alle andre projektopgaver oprettes nedenunder den. Navnet på rodopgaven angives altid til navnet på projektet. Tidsforbruget, datoerne og varigheden af rodopgaven opsummerer værdierne for opgaverne under rodopgaven. Du kan ikke modificere egenskaberne for rodopgaven eller slette den.

**Opsummerings- eller containeropgaver** En opsummerende opgave er en opgave, der har underopgaver eller konstituentopgaver nedenunder. En hovedopgave indeholder ingen arbejdsindsats eller egne omkostninger. I stedet er arbejdsindsatsen og omkostningerne ved en opsummerende opgave summen af arbejdsindsatsen og omkostningerne for dens konstituentopgaver. Den tidligste startdato for konstituentopgaver anvendes som startdatoen for den opsummerende opgave, og den seneste slutdato for konstituentopgaver anvendes som slutdatoen. Du kan ændre navnet på en opsummerende opgave, men du kan ikke ændre planlægningsegenskaber for tidsforbrug, datoer og varighed. Hvis du sletter en opsummerende opgave, sletter du også alle dens konstituentopgaver. 

**Bladnodeopgaver** En bladnodeopgave repræsenterer den mest detaljerede arbejdspakke for projektet. En bladnode har et estimeret tidsforbrug, et planlagt antal ressourcer, en planlagt start- og slutdato samt en varighed. 

Du kan udføre følgende hierarkihandlinger for at gøre det muligt at oprette et arbejdshierarki eller en dekomposition for et projekt. 

**Ny opgave** En ny opgave, som du opretter, tilføjes automatisk under rodnoden, og der tildeles automatisk et WBS-nummer til opgaven. WBS-nummeret repræsenterer opgavens niveau i hierarkiet. I forbindelse med opgaver på det første niveau under projektets rodopgave bruges et nummereringsskema med 1, 2, 3 osv. I forbindelse med opgaver, der henhører under det første niveau bruges et nummereringsskema med 1.1, 1.2, 1.3 osv. For hvert niveau, der tilføjes under et tidligere niveau, tilføjes der en ny punktserie med tal. 

I øjeblikket kan du ikke tilpasse WBS-nummereringen. 

**Indrykket opgave** Når du indrykker en opgave, bliver den til et underordnet element til den opgave, der står før den. WBS-nummeret for den nye underordnede opgave genberegnes automatisk på grundlag af WBS-nummeret på den nye overordnede. Den overordnede opgave er nu en oversigt eller en containeropgave, og den bliver derfor en akkumulering af dens konstituentopgaver. 

> [!NOTE] 
> Når du indrykker opgaver under en opgave, der var en bladnode før indrykningshandlingen, mister den nyoprettede opsummerende opgave sine egne datoer, tidsforbrug og antal ressourcer. Den bruger nu en oversigt over værdierne for de nye konstituentopgaver. 

**Udrykket opgave** Når du rykker en opgave ud, er den ikke længere en konstituentopgave for dens overordnede. WBS-nummeret for denne opgave genberegnes automatisk for at afspejle opgavens nye niveau i hierarkiet. Tidsforbruget, omkostningerne og datoerne for opgavens tidligere overordnede opgave genberegnes, så den ekskluderer denne opgave. 

**Flyt op og flyt ned** Når du klikker på **Flyt op** og **Flyt ned**, kan du ændre placeringen af en opgave i dens overordnedes hierarki. En opgaves position påvirker ikke opgavens tidsforbrug, omkostninger, datoer eller varighed. WBS-nummeret for denne opgave genberegnes dog automatisk for at afspejle opgavens nye position.

### <a name="schedule-estimation"></a>Planlægningsestimering

Planlægningsestimering er som regel det andet trin i oprettelsen af et WBS. Den bedste fremgangsmåde er at fuldføre planlæsningsestimering, når du har oprettet opgaverne. Siden **Arbejdsopgavehierarki** i Finance indeholder to sektioner. Den øverste rude er beregnet til planlægningsestimeringer, og den nederste rude indeholder en fane med **Estimerede omkostninger og omsætning**, som du kan bruge til omkostningsestimering. 
**Opgaveafhængigheder** I et WBS kan du oprette en foregående relation mellem opgaver. Når du tildeler foregående opgaver til en opgave, kan opgaven kun starte, når du har fuldført alle de foregående opgaver. Opgavens planlagte startdato indstilles automatisk til den seneste dato for alle dens foregående opgaver. 

**Opgaveplanlægning** Følgende faktorer bestemmer planlægningen af bladnodeopgaver:

-   Foregående
-   Indsats
-   Antallet af ressourcer
-   Start- og slutdatoer

Startdatoen for en bladnodeopgave, der ikke har foregående opgaver, angives automatisk som projektets planlagte startdato. Varigheden af en bladnodeopgave beregnes altid som antallet af arbejdsdage mellem dets start- og slutdatoer. 

*<strong><em>Planlægningsregler</em></strong>* Når automatisk planlægningsassistance er slået til, gælder følgende regler for opgaveplanlægningen af bladnodeopgaver:

-   Start- og slutdatoen for en opgave skal være arbejdsdage i henhold til projektets planlægningskalender.
-   Startdatoen for en opgave, der har foregående opgaver, angives automatisk til den seneste slutdato af sine forgængere.
-   En opgaves tidsforbrug beregnes automatisk på følgende måde:

Antal personer x varighed x antal timer for en standardarbejdsdag i projektkalenderen. 

I nogle tilfælde kan du afvige fra disse regler. Du kan slå automatisk planlægning fra for at forhindre, at Finance automatisk indstiller eller retter egenskaber for bladnodeopgaver. Når du angiver oplysninger om en opgave, der medfører overtrædelse af eventuelle planlægningsregler, vises der et ikon for planlægningsfejl for opgaven. Hvis du ikke vil have vist planlægningsfejl, skal du klikke på **Planlægningsfejl vises** for at deaktivere funktionen. 

> [!NOTE] 
> Værdierne for en opsummerings- eller objektbeholderopgave beregnes fortsat som summen af værdierne for konstituentopgaver, uanset om den automatiske planlægningsassistance er slået til eller fra. 

**Rettelse af planlægningsfejl** Når automatisk planlægningsassistance er slået til, opstår der sandsynligvis ikke planlægningsfejl. Men hvis du deaktiverer automatisk planlægningsassistance og derefter aktiverer det igen på et senere tidspunkt, vises der muligvis ikoner for planlægningsfejl i WBS. 

**Rettelse af planlægningsfejl efter opgave** Når du dobbeltklikker på ikonet for planlægningsfejl for en bestemt opgave, vises der en dialogboks med alle planlægningsfejl for den pågældende opgave. Du kan beslutte, hvilke planlægningsfejl der skal rettes i forbindelse med opgaven. 

**Rettelse af alle planlægningsfejl** Hvis du vil have, at Finance skal rette alle planlægningsfejl i WBS, skal du klikke på **Ret alle planlægningsuoverensstemmelser**. 

> [!NOTE] 
> Denne funktion kan forårsage betydelige ændringer af WBS. Fejl rettes i følgende rækkefølge:

1.  Det anslåede tidsforbrug for alle opgaver ændres, så den er lig med den kapacitet, der er defineret i projektkalenderen.
2.  Startdatoen for de enkelte opgaver ændres, så opgaven starter, når alle dens foregående opgaver er fuldført.
3.  Startdatoen for de enkelte opgaver ændres for at fjerne huller i startdatoerne for foregående opgaver.

### <a name="cost-estimation"></a>Omkostningsestimat

Som det tidligere blev nævnt i dette dokument, skal du angive omkostningsestimeringen for de enkelte bladnodeopgaver ved hjælp af fanen **Estimerede omkostninger og omsætning** i den nederste rude på siden **Arbejdsopgavehierarki**. 

> [!NOTE] 
> Du kan ikke ændre omkostningsestimeringen for en oversigt eller en objektbeholderopgave. Omkostningsestimeringen for en opsummerende opgave er lig med summen af omkostningsestimeringen for opgaverne i bladnoden. De estimerede samlede omkostninger for de enkelte opgaver beregnes som summen af de estimerede omkostningsbeløb for følgende transaktionstyper:

-   Arbejdskraft
-   Vare eller materiale
-   Udgifter

En transaktionstype som **Gebyr** bruges til at estimere den gebyrbaserede omsætning. Denne transaktionstype har ikke en omkostningskomponent og tages derfor ikke i betragtning, når omkostningerne estimeres. 

En transaktionstype som **Aconto** bruges til at registrere den aftalte salgsværdi i en projekttype med faste værdier. Denne transaktionstype tages heller ikke med i betragtningen, når omkostninger estimeres. 

Når du estimerer omkostningerne for arbejde, materialer og udgifter for de enkelte opgaver, skal du tildele en projektkategori til den estimerede omkostning. 

**Estimering af arbejdsomkostninger** For de enkelte bladnodeopgaver, skal du tildele en arbejdsindsats i timer og en standardkategori. Når du opretter en tidsplan for en opgave, tilføjes estimatet for arbejdsomkostningerne for den pågældende opgave derfor automatisk i standardkategorien for arbejde. Dette omkostningsestimat vises under fanen **Estimerede omkostninger og omsætning** i gitteret **Linjedetalje** for den pågældende opgave. Hvis du har brug for flere estimater over arbejdsomkostninger, kan du tilføje dem under denne fane. Hvis du forhøjer eller reducerer timerne for estimeringen af arbejdsløn, genberegnes tidsplanen for opgaven automatisk. 

**Estimering af udgifts- og materialeomkostninger** Fanen **Estimerede omkostninger og omsætning** giver dig også mulighed for at estimere udgifts- og materialeomkostninger for en opgave, hvis du har brug for estimater. 

Omkostningerne og salgsprisen for hver arbejdskraft eller udgiftsestimatlinje er baseret på den opsætning, der er defineret for hver kategori i prisfastsættelsestabellerne i **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Prisfastsættelse**. I relation til varer tilføjes omkostninger og salgspriser som standard fra varen eller handelsaftalen på listesiden **Frigivne produkter** i Styring af projektoplysninger.

## <a name="tracking-progress-on-the-wbs"></a>Spor status for WBS
Nogle brancher sporer status for et projekt i forhold til et WBS på et meget detaljeret niveau, hvorimod andre sporer status på et højere niveau i WBS. I dette afsnit beskrives det, hvordan du kan bruge sporing af WBS til dine projektbehov. 

Finance har tre visninger for et projekts WBS: Planlægningsvisning, visning af tidsforbrugssporing og visning af sporing af omkostninger.

### <a name="planning-view"></a>Planlægningsvisning

I Planlægningsvisning vises det planlagte eller grundlæggende estimat for tidsplanen og omkostningsoplysningerne. Selvom der ikke er nogen funktioner til sporing af versionen og basislinjen for et projekt-WBS, er værdierne i denne visning beregnet til at repræsentere basisversionen. Sektionerne Planlægningsestimat og Omkostningsestimat i dette emne beskriver visningen, og hvordan den bruges til at oprette et WBS.

### <a name="effort-tracking-view"></a>Visning af indsatssporing

Visningen af tidsforbrugssporing viser sporingen af status for opgaver i WBS. Den sammenligner den akkumulerede faktiske tidsforbrug i timer for en opgave med det planlagte tidsforbrug. Følgende formularer angiver værdierne i visningen af tidsforbrugssporing:

-   Status i procent = faktisk tidsforbrug til dato ÷ planlagt tidsforbrug for opgaven
-   Resterende tidsforbrug (også kaldet estimat-til-fuldførelse \[ETC\]) = planlagt tidsforbrug – faktisk tidsforbrug til dato
-   Estimat ved fuldførelse (EAC) = resterende tidsforbrug + faktisk tidsforbrug indtil dato
-   Forventet afvigelse i tidsforbrug = planlagt indsats ÷ EAC

Visningen af tidsforbrugssporing viser en projektion af afvigelsen for opgavens tidsforbrug på grundlag af, om EAC er højere eller lavere end det planlagte tidsforbrug:

-   Hvis EAC er højere end det planlagte tidsforbrug, projekteres opgaven til at tage længere tid, end det oprindeligt var planlagt, og er bagud i forhold til planlægningen.
-   Hvis EAC er mindre end det planlagte tidsforbrug, projekteres opgaven til at tage kortere tid, end det oprindeligt var planlagt, og er forud i forhold til planlægningen.

**Projektleders nye projektion af tidsforbrug** Projektlederen eller en anden person, der sporer status for et projekt, skal til tider revidere de oprindelige estimater på en opgave. Opgaven kan måske have en hurtigere eller langsommere fremgang end forventet af forskellige årsager. Omfanget er f.eks. blevet reduceret, eller arbejdere har mindre erfaring end oprindeligt planlagt. Projektionerne er en projektleders opfattelse af estimater baseret på et projekts aktuelle status. Du bør generelt ikke ændre de grundliggende tal, da en basislinje for et projekt udgør et velkendt dokument for projektets planlægnings- og omkostningsestimat, som alle interessenter på projektet er blevet enige om. 

Projektledere kan tilpasse tidsforbruget på opgaver på to måder:

-   Tilpasse det resterende tidsforbrug, der automatisk angives til at opdatere det faktiske resterende tidsforbrug på opgaven.
-   Tilpasse fremgangsprocenten, der automatisk angives til at opdatere opgavens egentlige fremgang.

Begge disse fremgangsmåder medfører en genberegning af opgavens ETC, EAC og fremgangsprocent samt den forventede afvigelse i tidsforbrug på opgaven. EAC, ETC og fremgangsprocenten for opsummerende opgaver genberegnes også, og deres projekterede afvigelse i tidsforbruget opdateres. 

**Tilpasset tidsforbrug i forbindelse med opsummerende opgaver** Du kan tilpasse tidsforbruget for opsummerende opgaver eller objektbeholderopgaver. Uanset om du tilpasser disse værdier ved hjælp af det resterende tidsforbrug eller fremgangsprocenten for de opsummerende opgaver, foretages beregningerne automatisk i følgende rækkefølge:

1.  EAC, ETC og statussen i procent for opgaven beregnes.
2.  Den nye EAC fordeles til de underordnede opgaver i samme forhold, som det oprindelige EAC-beløb.
3.  Den nye EAC for de enkelte bladnodeopgaver beregnes.
4.  Det resterende tidsforbrug og fremgangsprocent beregnes på ny for alle de berørte underordnede opgaver på baggrund af den nye værdi for EAC. Tidsforbrugsafvigelsen for opgaver genberegnes også.
5.  EAC af de opsummerende opgaver genberegnes også fra bladnoderne.

Klik på **Udvid til niveau** i visningen for tidsforbrugssporing for at angive det niveau, hvor WBS skal spores, og vedligeholde din WBS. WBS udvides automatisk til det pågældende niveau i visningen for tidsforbrugssporing, hver gang du åbner det.

### <a name="cost-tracking-view"></a>Visning af omkostningssporing

I visningen for omkostningssporing kan du se sporingen af omkostningsforbruget for en opgave. I denne visning sammenlignes de faktiske omkostninger, der er brugt på opgaven til dato, med de planlagte omkostninger for opgaven. Følgende formularer angiver værdierne i visningen omkostningssporing:

-   Procent af forbrugte omkostninger = faktiske omkostninger til dato ÷ planlagte omkostninger for opgaven
-   Omkostninger indtil fuldførelse (CTC) = planlagte omkostninger ÷ faktiske omkostninger til dato
-   Vurdering ved fuldført (EAC) = CTC + faktiske omkostninger til dato
-   Forventet omkostningsafvigelse = Planlagte omkostninger ÷ EAC

Visningen af omkostningssporing viser en projektion af afvigelsen for opgavens omkostninger på grundlag af, om EAC er højere eller lavere end de planlagte omkostninger:

-   Hvis EAC er højere end de planlagte omkostninger, projekteres opgaven til at bruge flere penge, end det oprindeligt var planlagt, og er gået over budget.
-   Hvis EAC er lavere end de planlagte omkostninger, projekteres opgaven til at bruge færre penge, end det oprindeligt var planlagt, og er under budget.

**Projektlederens nye projektion af omkostninger** Projektledere skal bruge CTC til at revidere det oprindelige omkostningsestimat for en opgave. Projektlederen kan ændre værdien i CTC til den omkostning, der kræves for at fuldføre opgaven. Hvis du ændrer CTC-værdien, genberegnes opgavens CTC, EAC og procenten for forbrugte omkostninger samt den planlagte omkostningsafvigelse for en opgave. EAC, ETC og procenten for forbrugte omkostninger genberegnes også, og deres projekterede afvigelse i omkostninger opdateres. 

> [!NOTE] 
> Når du reviderer en tidsforbruget i forbindelse med en WBS-opgave i visningen for tidsforbrugssporing, genberegnes opgavens CTC, EAC, procenten af forbrugte omkostninger og planlagt omkostningsafvigelse i visningen for omkostningssporing. Revisioner af omkostninger påvirker dog ikke værdierne i visningen for tidsforbrugssporing, da omkostningerne efter transaktionstype (arbejde, materialer eller udgift) eller projektkategori ikke kan revideres. 

**Projektionsrevision for omkostninger i forbindelse med opsummerende opgaver** Du kan revidere omkostninger for opsummerende opgaver, og beregningerne udføres automatisk i følgende rækkefølge:

1.  EAC, CTC og procenten for forbrugte omkostninger på opgaven genberegnes.
2.  Den nye EAC fordeles til de underordnede opgaver i samme forhold, som den oprindelige EAC på opgaverne blev fordelt.
3.  Den nye EAC for de enkelte opgaver beregnes.
4.  CTS og procenten for forbrugte omkostninger genberegnes for de berørte underordnede opgaver på baggrund af værdien for EAC. Omkostningsafvigelsen for opgaver genberegnes også.
5.  EAC for alle opsummerende opgaver genberegnes på baggrund af denne ændring.

Klik på **Udvid til niveau** i visningen for omkostningssporing for at angive det niveau, hvor WBS skal spores, og vedligeholde din WBS. WBS udvides til det pågældende niveau i visningen for omkostningssporing, hver gang du åbner det.

### <a name="earned-value-management"></a>Administration af optjent værdi

Du kan bruge metoden for optjent værdi (EVM) til at spore et projekts fremgang. Du kan få vist målepunkter for optjente værdier i projektlederens rollecenter. Komponenten for optjent værdi viser tidsfaseværdierne for planlagt værdi og faktiske omkostninger. Optjent værdi pr. dags dato vises som et point. Tidsfasedata for optjent værdi er ikke tilgængelige i øjeblikket. 

Tidsfasen i diagrammet over optjent værdi vises efter uge eller måned. I dette afsnit beskrives de tre søjler i EVM: planlagt værdi, optjent værdi og faktiske omkostninger. 

**Planlagt værdi** EVM-teori fastslår, at det planlagte værdiområde repræsenterer den hastighed, hvormed projektets team planlagde at optjene værdi på projektet. 

Finance bruger 0:100 optjeningsreglen, når den illustrerer en værdi. I henhold til denne regel, bogføres opgavens værdi i den pågældende opgave som sin slutdato. Der bogføres ikke en værdi, før opgaven er 100 procent fuldført. 

I Projektstyring og regnskab skal du angive en slutdato for bladnoderne og de planlagte omkostninger for den. Når diagrammet med den planlagte værdi vises efter uge, opsummeres den planlagte værdi efter uge for alle bladnodeopgaver i projektets løbetid. 

**Optjent værdi** EVM-teori fastslår, at det optjente værdiområde repræsenterer den hastighed, hvormed projektets team faktisk optjener værdi på projektet. 

Finance bruger 0:100 optjeningsreglen, når den illustrerer optjent værdi. I henhold til denne regel, bogføres opgavens værdi i den pågældende opgave som sin slutdato. Der bogføres ikke en værdi, før opgaven er 100 procent fuldført. 

Når optjent værdi beregnes, tages der højde for de enkelte opgavers fremgangsprocent. I henhold til 0:100 optjeningsreglen er det kun opgaver, der er fuldført i en bestemt periode, der medtages i beregningen af optjent værdi ved udløbet af den pågældende periode. Optjent værdi i projektet beregnes for alle opgaver, der er fuldført, når grafen oprettes. 

> [!NOTE] 
> I øjeblikket har systemet til WBS-sporing ikke datastrukturer til lagring af historiske fremgangsprocenter på de enkelte opgaver. Det er derfor kun muligt at rapportere optjent værdi fra det tidspunkt, hvor kuben behandles. Behandl kuben jævnligt for at opdatere data om optjent værdi, der vises i rollecenter. 

**Faktiske omkostninger** EVM-teori fastslår, at den faktiske omkostningsoversigt repræsenterer den kurs, hvormed penge bruges i projektet. 

Transaktioner, der er bogført i et projekt, bruges til at illustrere den faktiske omkostningslinje. Omkostningerne opsummeres efter dato. Disse data bruges herefter til at grafisk illustrere de faktiske omkostninger efter uge eller måned i diagrammet for optjent værdi.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Sådan bruges begreberne planlagt værdi, optjent værdi og faktiske omkostninger

**Afvigelse i planlægning** I forbindelse med planlægningen skal du oprette en prognose for arbejdet på en tidslinje. Den planlagte værdi er derfor den hastighed, som projektplanlæggere mente, at arbejdet ville blive fuldført på projektet. Når et projekt er igangværende, er arbejdet fuldført, og projektet tjener værdi. Ved at sammenligne planlagte værdier med optjent værdi kan du få se, hvordan arbejdet på et projekt skrider frem. Resultatet af denne sammenligning kaldes afvigelse i planlægningen. 

Hvis den planlagte værdi for en periode er større end den optjente værdi, er den mængde arbejde, der er udført på et projekt, mindre end det planlagte. Derfor er projektet bagud i forhold til planlægningen. Da planlagt værdi og optjent værdi er udtrykt i penge, tildeles den mellemliggende tid på projektet også en pengemæssig værdi. 

Hvis den planlagte værdi for en periode er mindre end den optjente værdi, er den mængde arbejde, der er udført på et projekt, større end det planlagte. Derfor er projektet forud i forhold til planlægningen. Gennemløbstiden tildeles også en pengemæssig værdi.

**Omkostningsafvigelse** Da optjent værdi bruger kostprisen som multiplikator, angiver optjent værdi omkostningerne ved det arbejde, der udføres på et projekt. Efterhånden som et projekt skrider frem, indeholder transaktionslogfilen en post over de penge, der faktisk bruges på det pågældende projekt. Ved at sammenligne optjent værdi med faktiske omkostninger kan du få vist det antal penge, der bruges i forhold til den værdi, der er opnået. Resultatet af denne sammenligning kaldes omkostningsafvigelsen. 

Hvis de faktiske omkostninger, der er brugt i en periode, er større end den optjente værdi, blev der brugt flere penge end optjent. Projektet overskrider derfor budgettet. 

Hvis de faktiske omkostninger, der er brugt i en periode, er mindre end den optjente værdi, blev der optjent flere penge, end der blev forbrugt. Projektet holder sig derfor under budgettet.

## <a name="wbs-templates"></a>WBS-skabeloner
Du kan bruge funktionaliteten for WBS-skabeloner til at oprette standardskabeloner til projekter. Hvis de projekter, som din virksomhed tilbyder, involverer en masse gentagende arbejde, kan du overveje at oprette en WBS-skabelon. 

Du kan oprette en WBS-skabelon ud fra et WBS i et eksisterende projekt, så den viden og bedste fremgangsmåde, som du har indsamlet under planlægningen af projektet, kan genbruges på lignende projekter i fremtiden. Nogle gange giver det måske ikke mening at gemme hele WBS'et som en skabelon. Derfor kan du også oprette skabeloner ud fra dele af et WBS for et projekt.

### <a name="saving-a-projects-wbs-as-a-template"></a>Gem et projekts WBS som en skabelon

Når du har oprettet en skabelon, kan du importere den til et nyt projekts WBS under rodnoden eller under en opgave i projektets WBS.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Import af en WBS-skabelon til et projekts WBS

Når du importerer opgaver, organiseres opgaverne i skabelonen på baggrund af startdatoen for den opgave, de importeres under. Under importen bruges foregående relationer i skabelonopgaverne til at beregne startdatoerne for de importerede opgaver. Destinationsprojektets standardarbejdskalender anvendes til at beregne slutdatoerne for de importerede opgaver, så de arbejdsdage og standardarbejdstimer, der er defineret i det aktuelle projekts arbejdskalender, bevares. 

Omkostningsbeløb og salgspriser på estimatlinjerne anvendes for at sikre, at priser, der er specifikke for projektet eller projektkontrakten, har gyldige datoer.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Forskelle mellem et projekts WBS og en WBS-skabelon

-   Opgaverne i WBS-skabeloner indeholder ikke startdatoer og slutdatoer.

Arbejdsdage og fridage angives ikke i WBS-skabeloner.

-   WBS-skabeloner bruger altid den planlægningskalender, der er konfigureret som standardkalender for alle projekter.

Standardplanlægningskalenderen bruges kun til at beregne antal timer på en almindelig arbejdsdag.

-   Foregående relationer kopieres ikke til en WBS-skabelon.

Da WBS-skabeloner ikke har datoer, er den startdatologik, der er baseret på en forgængers slutdato, ikke nødvendig.

-   Der oprettes automatisk en estimatlinje for arbejdsomkostninger, når en opgave oprettes i en WBS-skabelon. Salgspris og omkostningsbeløb kopieres fra den valgte arbejder.

Du kan oprette udgifts- og vareomkostninger manuelt, ligesom på et projekts WBS.

-   Der vises planlægningsfejl, når der er afvigelser i følgende formel:

Tidsforbrug = antal ressourcer × varighed × antal timer på en almindelig arbejdsdag 

Du kan rette alle planlægningsfejl på én gang ved at klikke på **Ret alle planlægningsfejl**. 

Du kan også rette planlægningsfejl individuelt ved at klikke på advarselsikonet for hver enkelt opgave.





[!INCLUDE[footer-include](../includes/footer-banner.md)]