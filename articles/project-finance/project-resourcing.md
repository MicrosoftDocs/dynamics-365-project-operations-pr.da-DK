---
title: Projektressourcer
description: Dette emne indeholder oplysninger om projektressourcer.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750481"
---
# <a name="project-resourcing"></a>Projektressourcer

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om projektressourcer.

En af udfordringerne for projektledere og ressourceledere i forbindelse med projektets planlægningsfase er ressourceallokering, hvor de skal afgøre og reservere den korrekte ressource til at arbejde på et projekt. I Dynamics 365 Finance kan du ved hjælp af ressourcekapaciteter for projekter definere roller, der behandles som midlertidige ressourcer, som kan reserveres til en bestemt aftale eller som en del af en aftale. Denne type ressourcer giver projektledere og ressourceledere mulighed for at udføre følgende opgaver:

- Definer en rolle med de krævede kompetencer, så det er nemt at sammenligne ressourcer.
- Brug roller til at definere en oprindeligt aftalt plan, der er baseret på reserverede ressourcer.
- Estimer omkostninger og fastsæt et indledende budget, der er baseret på de tildelte roller og ressourcer for et projekt.
- Brug roller til at beregne det antal ressourcereservationer, der kræves for hver enkelt aftale.
- Estimer det antal ressourcer, der kræves i hele et projekts livscyklus.
- Udarbejd en kladde over arbejdsopgavehierarki (WBS) ved hjælp af de oprindelige ressourcetildelinger.

[![Projektets livscyklus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Efterhånden som projektplanlægningen skrider frem, kan planlagte ressourcer erstattes af bemandede ressourcer. Projektlederen kan også gå tilbage og opdatere ressourcereservationerne i alle projektfaser.

## <a name="set-up-project-resources"></a>Konfigurer projektressourcer
Du skal konfigurere en kalender og knytte den til en medarbejder eller en arbejder. Kalenderen bruges til at planlægge projektet og arbejdstiden for de ressourcer, der er reserveret til projektet. I forbindelse med kalenderkonfigurationen kan projektledere udføre ressourceudjævning som led i ressourceoptimering. Afhængigt af kalenderplanen kan der indføres begrænsninger for ressourcer. Du kan konfigurere en kalender på siden **Kalendere**.

Når du konfigurerer en arbejder som en projektressource, kan du vælge mellem arbejdere, der arbejder i den virksomhed, som du opretter ressourcer for. Du kan også vælge arbejdere fra andre firmaer i organisationen. Disse arbejdere kaldes interne ressourcer.

I følgende procedurer får du beskrevet, hvordan du kan konfigurere en arbejder som en projektressource i virksomheden, og hvordan du kan konfigurere en intern projektressource.

### <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurere en arbejder som en projektressource

1. På siden **Arbejdere** i listen **Arbejdere** skal du vælge den arbejder, som du tilføjer som en projektressource, og åbne arbejderposten.
2. Vælg **Projekt** &gt; **Opsætning** &gt; **Projektopsætning** i handlingsruden.
3. Vælg en kalender, og luk derefter siden.

Du kan også angive standardprojekter for en ressource som en slags forhåndstildeling. Forhåndstildelinger kan bruges, når ressourceledere eller projektleder på forhånd ved, hvilke projekter, som ressourcen skal arbejde på. Forhåndstildelinger kan også være baseret på anmodningen fra en projektsponsor eller kunde. Hvis du vil forhåndstildele et projekt, skal du på siden **Tildel projekter** under fanen **Projekter** i listen **Resterende projekter** vælge det relevante projekt.

### <a name="set-up-an-intercompany-resource"></a>Konfigurer en intern ressource

Når du konfigurerer en arbejder som en intern ressource, skal du fuldføre opsætningen i udlånsvirksomheden og den låntagende virksomhed.

**I udlånsvirksomheden**

1. I Finance skal du kontrollere, at udlånsvirksomheden er valgt, og derefter fuldføre proceduren i forrige afsnit "Konfigurer en arbejder som en projektressource".
2. På siden **Internt regnskab** skal du vælge **Ny**.
3. I feltet **Juridisk enheds-id** skal du vælge udlånsvirksomheden. Udfyld de resterende felter efter behov, og vælg derefter **Gem**.
4. På siden **Overførelsespris** skal du vælge **Ny**.
5. I feltet **Juridisk låneenhed** skal du vælge den passende virksomhed.
6. Hvis du kun vil låne den låntagende virksomhed den ressource, som du oprettede i starten af denne sektion, skal du i feltet **Ressource** vælge navnet på den ressource, som du oprettede. Lad feltet **Ressource** være tomt, hvis alle ressourcer i udlånsvirksomheden skal være tilgængelige for den låntagende virksomhed.
7. På siden **Projektstyring og regnskabsparametre** skal du under fanen **Internt** angive indstillingen **Aktiver planlægning af intern ressource og timesedler** til **Ja**.

**I den låntagende virksomhed**

- På siden **Ressourceliste** skal du i søgefiltret angive navnet på den ressource, som du oprettede til udlånsvirksomheden, for at verificere, at navnet er inkluderet i ressourcelisten for den låntagende virksomhed.

## <a name="manage-resource-competencies"></a>Administrer ressourcekompetencer
Ressourcekompetencer er en vigtig del af ressourceadministrationen. Kompetencer kan bruges som en basislinje til at afgøre, hvilke ressourcer der har den korrekte balance mellem færdigheder, uddannelse, certificering og projekterfaring. Du bør konfigurere disse oplysninger for hver ressource og opdatere dem med jævne mellemrum. På denne måde kan du maksimere kapaciteterne, når bestemte ressourcekompetencer matches under tildeling af projektressourcer.

[![Eksempler på færdigheder, certificeringer, uddannelser og projekterfaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

I følgende procedurer forklares det, hvordan du kan konfigurere nogle af kompetencerne for en ressource.

Hvis du vil konfigurere kompetencer for en arbejder, kan du enten bruge listesiden **Arbejdere** i Personale eller listesiden **Ressourcer** i Projektstyring og regnskab. I forbindelse med følgende procedurer anvendes listesiden **Arbejdere** i Personale.

### <a name="set-up-competencies-certificates"></a>Konfigurer kompetencer: certifikater

1. På siden **Arbejdere** skal du vælge linjen for den arbejder, som skal have tilføjet oplysninger om et certifikat.
2. I handlingsruden skal du på fanen **Arbejder** i gruppen **Kompetencer** vælge **Certifikater**.
3. Vælg **Ny**, og derefter skal du i feltet **Certifikattype** vælge **PMP**.
4. I feltet **Startdato** skal du vælge **10/1/2015** og vælge **Gem**.

### <a name="set-up-competencies-skills"></a>Konfigurer kompetencer: færdigheder

1. På listesiden **Arbejdere** skal du kontrollere, at den arbejder, som du brugte i forrige procedure, stadig er markeret. Dernæst skal du på fanen **Arbejder** i gruppen **Kompetencer** vælge **Færdigheder** i handlingsruden.
2. Vælg **Ny**.
3. I feltet **Færdigheder** skal du vælge **Projektstyring**.
4. I feltet **Niveau** skal du vælge **5 Ekspert**.
5. I feltet **Niveaudato** skal du vælge **1-/14/2014**.
6. I feltet **Antal års erfaring** skal du angive **10**.
7. Vælg **Gem**, og luk derefter siden.

## <a name="create-a-new-project"></a>Oprette et nyt projekt
1. På siden **Projektstyring** skal du vælge **Nyt projekt** og angive følgende værdier:

    - **Projekttype:** Tid og materiale
    - **Projektnavn:** XYZ-opgraderingsfase 2
    - **Projektgruppe:** TM\_IGVA
    - **Projektkontrakt-id:** 00000002

2. Vælg **Opret projekt**.

### <a name="assign-a-resource-to-a-project"></a>Tildel en ressource til et projekt

1. På siden **Arbejdere** i listen **Arbejdere** skal du vælge posten for den arbejder, som du tidligere konfigurerede kompetencer for, og åbne arbejderposten.
2. I handlingsruden skal du på fanen **Projekt** i gruppen **Opsætning** vælge **Tildel projekter**.
3. På siden **Projekttildelinger til ressourcevalidering** skal du på fanen **Projekter** i feltet **Tilføj projektet til valgte projekter** filtrere efter projektet **XYZ-opgraderingsfase 2**.
4. I ruden **Resterende projekter** skal du vælge et projekt og derefter vælge pileknappen for at tilføje det til ruden **Valgte projekter**.

Du kan også tildele kategorierne for en ressource, efterhånden som du har brug for det. Kategoritypen er enten **Omkostning** eller **Omsætning**. Kategoritypen bestemmes af din organisation. Hvis der ikke er tildelt nogen kategorier for en ressource, søges Finance i standardkategorien efter timepriser for omkostninger og omsætning.

### <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurer egenskaberne for projektressourcer og roller

En projektleder kan bruge funktionen projektressource til at oprette de roller, der kræves for projektet. Roller kan bruges, hvis bekræftede ressourcer stadig ikke er kendte, når ressourcerne reserveres. Roller kan reserveres midlertidigt som planlagte ressourcer, så du kan fortsætte med projektplanlægningsfaserne.

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarie:** Contoso blev hyret til at fuldføre et tids- og materialeprojekt, der har et godkendt projektcharter. Den underordnede projektleder fuldfører stadig omfanget af projektet. Den ressourceansvarlige identificerer i øjeblikket bestemte ressourcer, der skal reserveres til at arbejde på det nye projekt. På grund af projektets vigtigste karakter anmoder projektsponsor om, at en af rollerne er den overordnede projektleder. Den ressourceansvarlige skal erhverve den nye ressource og definere rollen i systemet i tilfælde af, at den underordnede projektleder kræver ressourceoplysningerne i forbindelse med projektplanlægningen.

I følgende trin vises, hvordan den ressourceansvarlige kan konfigurere den overordnede projektleders rolle og knytte ressourceegenskaber til den. Senere kan rollen bruges til at søge efter tilgængelige ressourcer, der matcher de nødvendige ressourcekompetencer.

1. På siden **Opsætning af roller** skal du vælge **Ny** og angive følgende værdier:

    - **Rolle-id:** Overordnet projektleder
    - **Beskrivelse:** Overordnet projektleder

2. Vælg **Opret**.
3. Vælg rollen **Overordnet projektleder**, og vælg derefter **Konfigurer egenskaber**.
4. I feltet **Egenskabstype** skal du vælge **Færdighed**.
5. I feltet **Tilgængelige egenskaber** skal du angive den færdighed, der skal søges efter.
6. I feltet **Egenskabstype** skal du vælge **Certifikat**.
7. I feltet **Tilgængelige egenskaber** skal du angive den certifikattype, der skal søges efter.

### <a name="assign-a-project-resource-to-a-project"></a>Tildel en projektressource til et projekt

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgraderingsfase 2**.
2. På fanen **Projektteam og planlægning** skal du vælge **Tilføj**.
3. I feltet **Rolle** skal du vælge **Teammedlem**.
4. Vælge **Reserver fra kalenderen**.
5. På siden **Ressourcetilgængelighed** skal du vælge **Vis indstillinger**.
6. På siden **Tilpasning visningsindstillinger** skal du angive følgende værdier:

    - **Format for visnings af datointerval:** Dag
    - **Vis beskrivelser af tilgængelighed:** Ja
    - **Vis resterende kapacitet:** Ja

7. Vælg en ressource på listen over ressourcer.
8. Vælg **Reserver definitivt** og **Fuld kapacitet**.


### <a name="assign-a-resource-to-a-default-role"></a>Tildel en ressource til en standardrolle

For at hjælpe projektledere eller ressourceansvarlige med yderligere detailudledning om de ressourcer, der kan reserveres til et projekt. Du kan knytte en standardrolle til en eksisterende ressource eller en nyerhvervet ressource. F.eks. da Daniel blev ansat, havde han den erfaring og de færdigheder, der var nødvendige for at udfylde rollen som forretningsanalytiker. Den ressourceansvarlige har tildelt denne rolle som Daniel standardrolle. Den ressourceansvarlige har derfor føjet Daniel til en gruppe med forretningsanalytikere, som er til rådighed til at kunne arbejde med projekter.

I forbindelse med ressourcereservationen kan projektledere filtrere de rolleressourcer, der er tilgængelige til at kunne arbejde på projekter. De kan bruge disse oplysninger som et kriterium, når de udfører beslutningsanalyse med flere kriterier under ressourceopfyldning. De kan også tilføje andre ressourceegenskaber til filteret for at søge efter ressourcer, der har bestemte færdigheder, uddannelser og erfaring i forbindelse med et bestemt projekt.

**Scenarie:** Et godkendt projekt er påbegyndt, og rollen som overordnet projektleder blev reserveret som en planlagt ressource i projektplanlægningsfasen. Den ressourceansvarlige har nu erhvervet en ressource, der skal udføre rollen overordnet projektleder.

1. På siden **Ressourceliste** skal du vælge **Daniel Goldschmidt**.
2. På siden **Ressourcerolle** skal du vælge **Ny** og angive følgende værdier:

    - **Ikrafttrædelse:** Angiv den aktuelle dato.
    - **Udløb:** Angiv **Aldrig**.
    - **Rolle:** Angiv **Overordnet projektleder**.

3. Vælg **Gem**, og luk derefter siden.
4. På fanen **Kompetencer** skal du tilføje færdigheden **ProjectMgmt** og certifikatet **PMP**.

## <a name="set-up-role-based-pricing"></a>Konfigurer rollebaseret prisfastsættelse
Alle omkostninger, salgs- og overførelsespriser kan konfigureres for roller.

1. På siden **Salgspris (time)** skal du vælge **Ny** og angive en ikrafttrædelsesdato.
2. I kolonnen **Rolle** skal du vælge en rolle.
3. I kolonnen **Prisfastsættelse** skal du angive en pris for den valgte ressourcerolle.

## <a name="form-a-project-team"></a>Opret et projektteam
Hvis du vil bruge de roller, der tidligere blev konfigureret i et projekt, skal en projektleder knytte rollerne sammen med projektet. Der kan tildeles flere roller til et projekt. For at forhindre forvirring navngives disse roller automatisk i forbindelse med reservationen. Hvis projektlederen f.eks. har behov for tre softwareteknikere, oprettes der automatisk tre roller for softwareteknikere, der automatisk navngives **softwareingeniør1**, **softwareingeniør 2** og **softwareingeniør 3**. Hvis der tidligere er konfigureret rolleegenskaber for rollen, anvendes de som et filter under søgninger efter en ressource. Du kan tilføje yderligere egenskaber, hvis du vil begrænse søgningen yderligere.

Visningsindstillinger kan også tilpasses for at give en bedre visning af ressourcetilgængelighed. Der er mulighed for at få vist tilgængelighed baseret på tid, dag, uge, måned, kvartal og år. Der findes også en indstilling, der viser tilgængelighed og resterende kapacitet for ressourcer. Denne indstilling er nyttig i forbindelse med tidsstyring, når du beregner ledig tid for aktiviteter eller tilgængelighed af ressourcer.

Projektlederen kan vælge en rolle på siden og derefter vælge at reservere en ressource til at udfylde rollen, hvis der findes en tilgængelig ressource, der opfylder behovet. Bemærk, at der ikke skal reserveres ressourcer på dette tidspunkt i planlægningsstadiet. Når du opretter en WBS, kan du erstatte roller med personaleressourcer i projektet. Hvis roller erstattes med personaleressourcer i WBS, opdaterer ressourceopsætningen automatisk projektteamets liste og planlægning.

[![Projektteamets liste, som indeholder både roller og faktiske ressourcer](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektlederen har forskellige muligheder for at reservere en ressource til et bestemt projekt, f.eks. **Resterende kapacitet**, **Fuld kapacitet**, **Kapacitetsprocent** og **Angiv timer**. Disse indstillinger for reservation kan når som helst annulleres, hvis ressourcetildelingerne ændres. Der understøttes to typer af reservation:

- **Reserver definitivt** – Ressourcereservationen blev godkendt og bekræftet til at arbejde på aftalen i den angivne periode.
- **Reserver foreløbig** – Ressourcereservationer blev midlertidigt angivet til at arbejde på aftalen i den angivne periode.

Følgende procedure forklarer, hvordan du opretter et projektteam.

### <a name="create-a-project-team"></a>Opret et projektteam

1. På listesiden **Alle projekter** skal du vælge et projekt og derefter vælge **Rediger**.
2. På fanen **Projektteam og planlægning** skal du i feltet **Planlæg slutdato** angive den planlagte startdato plus en måned. Hvis planens startdato f.eks. er den 24. juni 2017 (24/06/2017), skal du angive **24/07/2017**.
3. Vælg **Tilføj**.
4. I ruden **Tilføj roller til projektet** skal du i feltet **Rolle** vælge **Overordnet projektleder**.
5. Vælg **Krævede kompetencer**.
6. På siden **Vælg egenskaber** vælges de egenskaber, som du tidligere har angivet for rollen overordnet projektleder, som standard. Vælg **OK**.
7. På siden **Tilføj roller til projekt** skal du i feltet **Antal ressourcer** angive **1**.
8. I feltet **Ressource** vises opslaget for alle de ressourcer, der har de krævede kompetencer. Vælg **Daniel Goldschmidt**, og vælg derefter **Opret**.
9. På siden **Projekt** skal du vælge **Tilføj**.
10. I ruden **Tilføj roller til projektet** skal du i feltet **Rolle** vælge **Teammedlem**. Angiv **5** i feltet **Antal ressourcer**.
11. Vælg **Opret**.
12. På siden **Projekter** skal du vælge **Opfyld ressource**.

## <a name="resource-capacity-synchronization"></a>Synkronisering af ressourcekapacitet
Processerne for ressourcesynkronisering er med til at sikre, at oplysninger til kalenderen og basiskalenderen når frem til projektets ressourceplanlægningen. Hvis kalenderen ændres, foretager processerne de påkrævede opdateringer i planlægningen af projektressourcer. Processerne er også med til at forbedre ydeevnen, da kalenderens ressourceoplysninger er blevet synkroniseret på forhånd. Opdateringer af oplysninger om ressourceplanlægning sker derfor hurtigere. Det anbefales, at du planlægger processerne som et batch i stedet for en ad gangen. I modsat fald er der risiko for, at en bruger glemmer de inkluderede datoer, da oplysningerne sidst blev synkroniseret. Hvis der ikke bruges inkluderede datoer, kan der opstå huller under datosynkroniseringen.

![Synkronisering af kalendere](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synkronisering af akkumulering af ressourcekapacitet

Synkroniseringsprocessen er tiltænkt at skulle synkronisere alle ressourcekalenderoplysninger. Disse oplysninger inkluderer basiskalenderoplysninger om eventuelle ændringer af tabellen for projektets ressourcekalenderkapacitet. Hvis der tilføjes nye ressourcer i projektet, kan synkroniseringen hjælpe dig med at sikre, at de opdaterede kalenderoplysninger er tilgængelige. Denne synkronisering kan udføres på et hvilket som helst tidspunkt.

Vi anbefaler, at du bruger en batch . Indstillingerne er tilgængelige under synkronisering af kapacitetsreservationer.

1. Vælg **Projektstyring og regnskab** &gt; **Periodisk** &gt; **Kapacitetssynkronisering** &gt; **Synkroniser ressourcekapacitetsakkumuleringer**.
2. Angiv mulighederne i den følgende tabel.

    | Indstilling      | Beskrivelse |
    |-------------|-------------|
    | Periodekode | Du kan evt. vælge intervalkoden for finanskladden for at angive start- og slutdatoer for synkroniseringsprocessen for akkumulering af ressourcekapacitet. |
    | Startdato  | Angiv startdatoen for synkroniseringsprocessen for akkumuleringer af ressourcekapacitet. |
    | Slutdato    | Angiv slutdatoen for synkroniseringsprocessen for akkumuleringer af ressourcekapacitet. |

[![Synkroniseringsproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Konfigurer roller for WBS-skabeloner
Projektledere kan oprette WBS-skabeloner, som de kan anvende, når de opretter et WBS for nye projekter. Projektledere kan tilføje roller, når de opretter en skabelon. Benyt følgende fremgangsmåde for at tildele en rolle til en WBS-skabelon.

1. Vælg **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Projekter** &gt; **Skabeloner til arbejdsopgavehierarki**.
2. Vælg **Detaljer** for en valgt WBS-skabelon.
3. Markér en opgave på listen, og vælg derefter i feltet **Rolle** en rolle, der skal tildeles til opgaven.

### <a name="work-with-a-wbs"></a>Arbejde med et WBS

Du kan oprette et nyt WBS, eller du kan kopiere et WBS fra en eksisterende WBS-skabelon. En projektleder kan nemt administrere ressourcerne ved at tildele roller til nye opgaver i WBS. Roller kan erstattes, enten efter at en ressource er erhvervet, eller når en ressource, der er bekræftet til at skulle arbejde på opgaven, er blevet identificeret. Denne fleksibilitet gør det muligt for projektledere at udføre følgende opgaver:

- Angiv det antal ressourcer, der kræves til WBS-arbejdspakker.
- Estimer projektomkostninger.
- Fastlæg et foreløbigt budget.
- Estimer aktivitetens varighed baseret på roller og ressourcer.
- Opret nogle projektstyringsplaner baseret på tilgængelige projektoplysninger.

Der er tilføjet yderligere muligheder i WBS for at opnå en bedre anvendelse af ressourcefunktionaliteten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indstilling</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressourcetildelinger</td>
<td>Få vist de tildelte ressourcer, datoer, antallet timer og reservationstype for opgaver i WBS.</td>
</tr>
<tr class="even">
<td>Opret team automatisk</td>
<td>Tilføj automatisk planlagte ressourcer ved hjælp af de roller, der er knyttet til en opgave. Finance foreslår automatisk planlagte ressourcer ved hjælp af beslutningsanalyse med flere kriterier, der er baseret på roller. Når der er angivet roller og tidsforbrug (timer) for opgaverne i et WBS, og efter, at strukturen er blevet frigivet, skal du vælge <strong>Opret team automatisk</strong>. Det nødvendige antal planlagte ressourcer tilføjes til WBS og fanen <strong>Projekt- og teamplanlægning</strong>.</td>
</tr>
<tr class="odd">
<td>Ressource (rulleliste)</td>
<td>På siden <strong>Start ressourcetildeling</strong> kan du vælge at reservere ressourcer definitivt eller midlertidigt på grundlag af den angivne varighed. Du kan justere visningsindstillingerne for at få vist og angive varigheden af ressourceaktiviteter. Du kan vælge og tildele ressourcer på arbejdspakkeniveau ved hjælp af følgende indstillinger:
<ul>
<li><strong>Accepter</strong> – Bekræft ændringer af den ressource, der er tildelt til en opgave.</li>
<li><strong>Annuller</strong> – Annuller ændringer af den ressource, der er tildelt til en opgave.</li>
<li><strong>Tildel automatisk</strong> – En tilgængelig personaleressource, der har en tilsvarende rolle, vælges automatisk og tildeles den valgte opgave.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgraderingsfase 2**.
2. Vælg **Plan** &gt; **Aktivitet** &gt; **Arbejdsopgavehierarki**.
3. Vælg **Ny** for at tilføje følgende niveau-et-aktiviteter til WBS:

    - Påbegynder
    - Planlægning
    - Udfører
    - Overvågning og kontrol
    - Luk

4. Angiv datoerne og tidsforbruget (timer) som vist i følgende illustration.

    [![Angivelse af datoer og tidsforbrug](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vælg opgavelinjen **Påbegynd**, og du skal derefter i feltet **Rolle** vælge **Overordnet projektleder**.
6. Vælg **Udgiv**.
7. På den samme linje skal du i feltet **Ressource** vælge **Daniel Goldschmidt** og derefter vælge **Accepter**.
8. Markér opgavelinjen **Planlægning**, og vælge derefter i feltet **Rolle** **Forretningsanalytiker**.
9. Vælg **Publicer**, og vælg **Opret team automatisk**.
10. I bekræftelsesfeltet, der vises, skal du vælge **Ja**.
11. I feltet **Ressource** skal du kontrollere, at værdien er **Forretningsanalytiker 1**.
12. For ressourcen **Forretningsanalytiker 1** skal du åbne opslaget og vælge **Start ressourcetildelinger**. Vælg derefter en arbejder til opgaven.
13. Vælg **Reserver midlertidigt** &gt; **Fuld kapacitet**.

    > [!NOTE] 
    > Du modtager ikke en advarsel om, at den angivne ressource nu er 2, da antallet af ressourcer stadig er 1.

14. På siden **Arbejdsopgavehierarki** skal du kontrollere ressourcetildelingen i WBS og derefter vælge **Gem**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressourceopfyldelse for planlagte ressourcer
En projektleder kan planlægge nødvendige ressource roller for et projekt. Den ressourceansvarlige kan se disse planlagte ressourcer som anmodninger på siden **Ressourceopfyldelse** og kan tildele faktiske ressourcer.

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgraderingsfase 2**.
2. Vælg **Projekt**, og vælg derefter **Rediger**.
3. På fanen **Projektteam og planlægning** skal du vælge **Tilføj**.
4. I dialogboksen **Tilføj roller** skal du vælge rollen **Softwareudvikler**.
5. Vælg **Opret**, og luk derefter projektsiden.
6. På siden **Ressourceopfyldelse** skal du vælge **Softwareudvikler 1** for projektet **XYZ-opgradering af projektfase 2**.
7. Vælg en arbejder, og vælg derefter **Tildel**.
8. Kontroller, at linjen for **Softwareudvikler 1** er blevet fjernet for projektet **XYZ-opgradering af projektfase 2**.
9. Under fanen **Projektteam og planlægning** skal du for projektet **XYZ-opgraderingsfase 2** kontrollere, at den arbejder, du har valgt i forrige trin, er blevet tilføjet som **Softwareudvikler**.

## <a name="requests-for-project-resources"></a>Anmodninger om projektressourcer
Funktionaliteten i planlægningen af projektressourcer giver kun de ressourceansvarlige distribuere personaleressourcer til aftaler eller projekter. Hvis du vil aktivere denne funktion, skal du udføre følgende opgaver eller kontrollere, at de er blevet fuldført:

- Konfigurer nummerserier.
- Konfigurer arbejdsgange for projektstyring og regnskab.
- Aktivér arbejdsprocesser for ressourceanmodninger.

Når de foregående opgaver er fuldført, kan du udføre følgende opgaver, som du har brug for:

- Opret en ressourceanmodning på baggrund af en midlertidigt reserveret personaleressource.
- Overvåg ressourceanmodninger.
- Opfyld ressourcekrav.
- Anmod om en personaleressource fra et WBS.
- Reserver ressourcer til et projekt, uden at der skal anmodes om en personaleressource.

## <a name="monitor-project-teams"></a>Overvåg projektteams
1. På siden **Alle projekter** skal du vælge linket **Projekt-id** for projektet **XYZ-opgraderingsfase 2**.
2. På hurtigfanen **Projektteam og planlægning** skal du kontrollere, at de viste projektressourcer er korrekt angivet.
