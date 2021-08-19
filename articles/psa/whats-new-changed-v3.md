---
title: Nyheder eller ændringer i Project Service Automation version 3
description: Dette emne indeholder oplysninger om nyheder og ændringer i Project Service Automation version 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: afce9cd2d4b3920dc5de5d3deab8920a7f51f275a73918a84db300739b1b4feb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987069"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Nyheder eller ændringer i Project Service Automation version 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Emnet indeholder oplysninger om ændringerne af brugergrænseflade, funktioner og terminologi i Project Service Automation mellem version 2 eller version 1 og version 3.

## <a name="project-scheduling"></a>Projektplanlægning
Projektplanen, som blev kendt som arbejdsopgavehierarkiet (WBS - work breakdown structure) i tidligere versioner, er blevet omdøbt til Tidsplan, og du får adgang til den ved at klikke på fanen **Tidsplan**. 

![Projektplan.](media/psa-schedule-01.png)

Planlægningen har nu en ny interaktionsoverflade, som er både moderne og tilgængelige. Det underliggende planlægningsprogram for Project Service Automation er dog ikke blevet ændret. Du kan bruge knapperne til kontrolelementer på båndet til tidsplanens gitter til at interagere med tidsplanen på en måde, der minder om den forrige version af Project Service Automation. Du kan ændre tidsplanen ved at benytte følgende fremgangsmåde:

- **Gantt-diagram** – Gantt-diagrammet findes ikke længere. En ny Gannt-visualisering vil vende tilbage i en fremtidig opdatering.
- **Kolonneoverskrifter** – du kan skjule kolonneoverskrifterne i gitteret ved at klikke på nedindikatoren ud for kolonnetitlen. 
- **Kolonner** – du kan få vist skjulte kolonner ved at klikke på **Tilføj kolonne**. 
- **Transaktionskategori** - Der er føjet et **Transaktionskategori**-opslag til tidsplanens gitter, og det vises som standard. 
 
## <a name="project-templates"></a>Projektskabeloner
Der er foretaget følgende ændringer af funktionaliteten i projektskabelonen.

### <a name="create-a-project-template"></a>Oprette en projektskabelon 
Du kan oprette en projektskabelon i version 3, der ligner de tidligere versioner af Project Service Automation. Skabelonen kan kun indeholde en tidsplan, og tidsplanen kan indeholde tildelinger, men de er ikke obligatoriske. Hvis der er tildelinger i tidsplanen, kan de kun bruges som generiske ressourcer. Du kan oprette ressourcekrav for generiske ressourcer, men de kan ikke reserveres med faktiske ressourcer i skabelonen. Du kan ikke reservere en faktisk ressource til et team i en skabelon. 

### <a name="create-a-template-from-an-existing-template"></a>Oprette en skabelon ud fra en eksisterende skabelon
Når du opretter en ny projektskabelon ud fra en eksisterende skabelon i Project Service Automation version 3, sker følgende: 

- Kildeprojektets tidsplan kopieres til skabelonen. 
- Generiske ressourcer kopieres til teamet, og eventuelle generiske ressourcetildelinger kopieres over. Kravene til de generiske ressourcer kopieres ikke over. 

### <a name="create-a-template-from-an-existing-project"></a>Oprette en skabelon ud fra et eksisterende projekt
Når du opretter en ny projektskabelon ud fra et eksisterende projekt, sker følgende: 

- Kildeprojektets tidsplan kopieres til skabelonen. 
- Generiske ressourcer kopieres til teamet, og eventuelle generiske ressourcetildelinger bevares. Kravene til de generiske ressourcer kopieres ikke over.    
- Navngivne ressourcer, både tildelte og ikke-tildelte, fjernes fra teamet og erstattes med generiske ressourcer.
- Hvis der er kundeoplysninger, fjernes disse. 
- Hvis der er referencer til tilbud og kontrakter, fjernes disse. 

### <a name="create-a-project-from-a-template"></a>Oprette et projekt på grundlag af skabelon
Når du opretter et nyt projekt ud fra en skabelon i Project Service Automation version 3, sker følgende:

- Tidsplanen, teamet og tildelingerne kopieres til det nye projekt.   
- Startdatoen er enten kopieringsdatoen eller den dato, der er valgt af brugeren.   
- For et generisk teammedlem med ressourcekrav i skabelonen kopieres eller genereres kravene ikke automatisk. Du skal generere dem. 

## <a name="copy-a-project"></a>Kopiere et projekt
Når du kopierer et projekt i Project Service Automation version 3, sker følgende: 

- Den anslåede startdato kopieres, men den kan ændres.  
- Projektplanen og opgaverne kopieres. 
- Generiske ressourcer og deres tildelinger kopieres. Ressourcekravene til de generiske ressourcer kopieres ikke. Du skal generere dem igen. 
- Reelle ressourcer og deres tildelinger kopieres ikke. De erstattes i stedet af generiske ressourcer. 
- Faktiske data kopieres ikke til det nye projekt. 

## <a name="move-a-scheduled-project"></a>Flytte et planlagt projekt
Når du flytter tidsplanen for et eksisterende projekt fremad, sker der følgende: 

- Opgavedatoer flyttes automatisk, så de svarer til perioden med bevægelser. 
- Tildelte generiske ressourcer forbliver tildelt.   
- Hvis de genereres, før projektet flyttes, forbliver kravene til den generiske ressource de samme, og de oprettes ikke automatisk igen. Du skal oprette dem igen for at afspejle de nye tildelinger som følge af bevægelsen i opgaven. 
- Tildelinger af faktiske ressourcer ændres, så de svarer til bevægelsen på opgavedatoen. Reservationer af faktiske ressourcer ændres ikke. Du skal ændre reservationerne ved hjælp af afstemningsvisningen. 
- Teamressourcer med reservationer men ingen tildelinger ændres ikke. 
- Faktiske flyttes ikke 

## <a name="estimates"></a>Vurderinger
Estimater er opdelt i to faner, **Ressourcetildeling** og **Estimater**. Fanen **Ressourcetildeling** indeholder indsatsestimaterne og viser ressourcetildelingerne for opgaverne i en visning med tidsfaser. Du kan redigere estimaterne på baggrund af det, planlægningsprogrammet har genereret.

![Fanen Ressourcetildelinger, der viser indsatsestimater og ressourcetildelinger for opgaver.](media/resource-assignments-tab-02.png)

Under fanen **Estimater** vises omkostnings- og salgsbeløb for ressourcetildelinger. Beløbene er skrivebeskyttede. Fastsættelse af omkostnings- og salgspriser er nu baseret på teammedlemtildelinger i tidsplanen. Det betyder, at hvis du har en opgave uden tildeling, vises opgaven under den ikke-tildelte bucket. Det betyder også, at uden **rolle**, som er en standardprisdimension, er der ingen anslået omkostning eller intet anslået salg, hvis du har en kunde eller kontrakt/tilbud tilknyttet projektet. 

![Fanen Estimater viser omkostnings- og salgsbeløb.](media/estimates-tab-03.png)
  
Kategori understøttes også i opgaver i tidsplanvisningen. Gruppering efter kategori i den tidsfaseinddelte visning af estimater vil give en bedre oplevelse, især hvis du også har udgiftsestimater i projektet. Udgiftsestimater indtastes ved hjælp af et gitter under en separat fane. 

Udgiftsestimater kan angives i gitteret under fanen **Udgiftsestimater**. 

![Fanen Udgiftsestimater, der viser gitteret for udgiftsestimater.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Ressourcestyring
I Project Service Automation version 3 med den nye Unified-klientbrugergrænseflade og ændringer i relationen mellem reservationer og tildelinger er bemanding af et projekt med generiske eller faktiske ressourcer ændret væsentligt fra version 2 og version 1. Begreberne reserverbare ressourcer, både **faktiske** og **generiske**, forbliver de samme ligesom teammedlemmer, krav, tildelinger og reservationer.   

![Brug af ressourcevælgeren.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Tildele en faktisk reserverbar ressource 
I Project Service Automation version 3 er reservationer og tildeling af opgaver ikke så tæt forbundet som i de tidligere versioner af Project Service Automation. Du kan bruge teamgitteret til at reservere et **faktisk** teammedlem, meget lig in-market.

Ved hjælp af ressourcevælgeren i tidsplanen kan du vælge det teammedlem, der er oprettet i teamvisningen, og derefter tildele vedkommende til opgaver. Du kan fortsat tildele opgaver til dem, selv ud over reservationerne af dem. Brug fanen **Afstemning** til at afstemme de teammedlemmer, der har differencer i reservationer og tildelinger.

Ressourcevælgeren viser teammedlemmerne for projektet. Du kan også bruge ressourcevælgeren til at søge efter og få vist andre reserverbare ressourcer, der ikke er en del af projektteamet. Du kan tildele dem til en opgave, så de bliver en del af projektteamet. Du skal reservere dem ved hjælp af **planlægningsområdet** eller fanen **Afstemning**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Tildele en generisk, reserverbar ressource for en opgave og et projektteam og derefter fuldføre en faktisk ressource via planlægningsområdet 
I Project Service Automation version 3 bruges opret team-funktionaliteten ikke til generiske ressourcer. I stedet kan du oprette og direkte tildele en generisk ressource fra tidsplanen ved at skrive stillingsnavnet for den generiske ressource i ressourcecellen i tidsplanen. Du kan også vælge ressourceikonet i cellen og derefter bruge ressourcevælgeren til at angive navnet på den generiske ressource, du vil oprette. Derved åbnes et panel til hurtig oprettelse, hvor du kan angive rollen og organisationsenheden for det generiske ressourceteammedlem. Når du har oprettet ressourcen, tildeles den til opgaven, og du kan fortsætte med at tildele den pågældende generiske ressource til andre opgaver i tidsplanen.    
 
Når du har tildelt ressourcen til alle relevante opgaver, kan du oprette et ressourcekrav og derefter opfylde det ved direkte reservation via **planlægningsområdet** eller ved at sende en anmodning om ressource. Du kan også føje generiske ressourcer direkte til teammedlemsgitteret. 

Generiske ressourcer føjes til projektteamet uden ressourcekrav og med start-/slutdatoerne for projektet, indtil ressourcekravet er genereret. Hvis du vil generere et krav, skal du vælge den generiske ressource og klikke på **Generer**. Nu vises linket til kravet, og de påkrævede timer udfyldes med de tildelte timer. Du kan klikke på linket for at åbne og opdatere kravet.
  
Når reservationen er fuldført og helt opfyldt med en navngivet ressource, erstattes den generiske ressource med den navngivne ressource, og tildelingen i tidsplanen opdateres med den navngivne ressource. 

Foreslåede ressourcer til krav gemmes nu under en fane i stedet for i en separat sektion.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Flere navngivne ressourcer, der opfylder en generisk ressource
Når et krav opfyldes med flere ressourcer, forbliver den generiske ressource i teamet og tildelt til opgaven. De navngivne teammedlemmer, der er reserveret, er ikke tildelt som en del af stillingen. Projektlederen kan tildele arbejdet efter behov til de faktiske ressourcer.  Visningen **Afstemning** indeholder en opdeling af reservationerne på tværs af flere ressourcer til flere opgavetildelinger. Dette sker ikke automatisk, da det i mere komplicerede scenarier, f.eks. et hvor du har et bundt opgaver, der udgør kravet, er nødvendigt at antage projektlederens hensigt med tildelingen. Da systemet ikke kan forstå hensigten, vil antagelserne sandsynligvis være anderledes end hensigten, og der opstår et forkert eller uforudsigeligt resultat. Det forudsigelige resultat er, at den generiske ressource forbliver tildelt, indtil projektlederen bevidst tildeler ressourcer ved hjælp af visningen **Afstemning**.

### <a name="reconciliation"></a>Afstemning
Fanen **Afstemning** viser reservationer og alle tildelinger for hvert enkelt projektteammedlem. Visningen angiver timer i celler, som kan repræsentere tidspunkter fra måneder ned til dage. Ved hjælp af denne visning kan projektledere afstemme teammedlemmernes reservationer og deres tildelinger for projektteamet. Dette er nyttigt, fordi reservationer og opgavetildelinger ikke er så tæt sammenkædet, hvilket giver større fleksibilitet i forbindelse med planlægning af et projekt. 

![Fanen Afstemning, der viser reservationer og tildelinger for projektteammedlemmer.](media/resource-reconciliation-tab-06.png)

For hver ressource angiver visningen forskellen mellem et teammedlems reservationer og en akkumulering af deres opgavetildelinger og viser følgende to forskelle, som kan forekomme i forbindelse med reservationer og tildelinger i et projekt: 

- **Manglende reservation** – Der opstår manglende reservation, når en ressource har flere tildelinger end reservationer. Da denne kapacitet ikke er reserveret, kan en projektleder rette dette ved at forlænge reservationer af ressourcen for at dække underskuddet. 
- **Overskydende reservationer** – Overskydende reservation forekommer, når en ressource er blevet reserveret til projektet, men ikke har fået tildelt opgaver.  Dette kan være acceptabelt, hvis ressourcen f.eks. er blevet reserveret, før opgavetildelingen. Men i andre tilfælde er ressourcen måske ikke planlagt til at blive tildelt, og projektlederen bør overveje at annullere reservationer af ressourcen, så kapaciteten kan bruges til et andet projekt. 

Når du har opgavetildelinger for en ressource uden reservationer (manglende reservation), kan du vælge den samlede manglende reservation og klikke på **Udvid reservation**. Derefter kan du få vist den reservation, der skal bruges for at løse manglen på ressourcen og dens tilgængelighed. 
 
## <a name="time-and-expense"></a>Tid og udgift
Denne sektion indeholder oplysninger om ændringerne i tid, udgifter og godkendelse i version 3 af Project Service Automation. Som en del af Dynamics 365 Project Service Automation-løsningen er funktionen **Tidsregistrering** opdateret, så den kan udnytte Unified Interface-strukturen. Det giver mulighed for levering af en ensartet brugergrænseflade med dynamisk design og optimal visning på en hvilken som helst skærmstørrelse eller enhed. 

### <a name="landing-page"></a>Landingsside
Oplevelsen med den brugerdefinerede tidsregistrering, der ikke kan udvides, er frarådet i version 3. I stedet er der nu en indbygget gitteroplevelse, som kan udvides. Du kan få adgang til tidsregistreringsfunktionaliteten ved at bruge webstedsoversigten til venstre. Med denne ændring kan du ikke længere angive tid for én uge ad gangen. I stedet skal du oprette en tidsregistrering for hver dag i gitteret. Når der er oprettet nogle få tidsregistreringer, kan brugerne masseoprette tidsregistreringer ved hjælp af funktionen **Kopiér**, der er forklaret senere i denne emne. 

![Landingsside for tidsregistrering.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Oprette nye tidsregistreringer 
Klik på **Ny** på båndet for at åbne en side til hurtig oprettelse for tidsregistrering, hvor du angiver varighed i minutter, timer eller dage. Det kan du gøre ved blot at begynde at skrive t, m eller d sammen med antallet.  

![Hurtig oprettelse af tidsregistrering.](media/quick-create-time-entry-08.png)

Opslagsfelter understøttes af systemvisninger. Når du f.eks. har angivet projektoplysninger, angives feltet **Projektopgave** som standard til visningen **Mine åbne projektopgaver**. Hvis du vil oprette tidsregistreringer for opgaver, der ikke er tildelt til brugeren, skal du klikke på **Skift visning** i opslaget og vælge **Alle aktive projektopgaver**. Når tidsregistreringen er oprettet og vises i gitteret, kan du redigere alle linjeværdier direkte i gitteret.  

### <a name="bulk-createcopy"></a>Masseoprette/-kopiere 
Når der er oprettet nogle få registreringer, kan du bruge kopieringsfunktionen til at masseoprette flere tidsangivelser. Klik på **Kopiér** for at åbne dialogboksen **Kopiér**. I **Fra periode: Start dato** skal du angive det datointerval, som tidsperioder skal kopieres fra. I **Til periode: Startdato** skal du angive den dato, der skal oprettes tidsregistreringer for. Klik på **Kopiér** for at kopiere tidsregistreringsposterne til den tilsvarende dag i ugen, der er angivet i **Til periode**. Tidsregistreringen for mandag i sidste uge kopieres f.eks. til mandag i den uge, der er angivet i **Til periode**. 

![Massekopiér tidsregistreringer.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importér data 
Tildelinger og udveksling følger det samme brugergrænseflademønster, hvilket gør det muligt for brugeren at angive det datointerval, som reservationer skal importeres fra. Du skal derefter udtrykkeligt vælge de reservationer, der skal kopieres til **Kladde**-tidsregistreringer. I version 3 kan du ikke længere se mønsteret med **Foreslået** tidsregistreringer i gitteret og kalenderen.  

### <a name="change-in-calendar-control"></a>Ændring i kalenderkontrolelement
I version 3 er vi flyttet væk fra det brugerdefinerede kalenderkontrolelement og bruger nu UC-kalenderen til at få vist tidsregistreringer for ugen. I denne kalender kan du se dag, uge og måned. 

> [!NOTE]
> Kalenderen har den begrænsning, at dette kontrolelement ikke understøtter handlinger for individuelle kalenderelementer. Du kan f.eks. ikke vælge et eller flere kalenderelementer og sende eller slette disse elementer. Hvis du klikker på et kalenderelement, åbnes siden med **tidsregistreringsobjekt** til flere handlinger. 

### <a name="extensibility"></a>Mulighed for udvidelse af
**Hent udelukkende data i brugerdefinerede felter i objekter med tidsregistreringer og udgiftsposter** – tidsregistrering bruger et redigerbart gitter, et skrivebeskyttet gitter og kalenderkontrolelementer fra platformen. Alle disse kontrolelementer er indbyggede, og de understøtter derfor tilpasninger. I Project Service Automation version 3 kan du tilføje flere brugerdefinerede felter, konfigurere opslagsfelter og sikkerhedskopiere dem med brugerdefinerede visninger. Du kan også angive brugerdefineret forretningslogik baseret på udvalgte værdier i brugerdefinerede felter.  

**Hent data i brugerdefinerede felter i tidsregistrering og udgiftspost, og overfør dem via objekter, der understøtter indsendelses- og godkendelsesflow** – den typiske behandling af tidsregistreringer vises i følgende diagram.

![Proces for tidsregistreringsflow.](media/process-time-entries-10.png)

Hvis virksomhedens krav fastsætter, at tidsregistreringer og udgiftsposter skal registrere brugerdefinerede prisdimensioner og overføre de værdier, der er angivet for en tidsregistrering og en udgiftspost i den brugerdefinerede prisdimension via alle objekterne i den forrige grafik, skal du [Konfigurere brugerdefinerede felter som prisfastsættelsesdimensioner](set-up-pricing-dimensions.md)

Hvis du vil understøtte forretningskrav, hvor tidsregistreringer og udgiftsposter skal registrere brugerdefinerede ikke-prisdimensioner og overføre værdierne, kan du bruge konfigurationen af prisdimensioner og udtrykke de brugerdefinerede dimensioner som prisdimensioner uden omkostnings- eller faktureringssats. Et andet scenarie er at tilføje et brugerdefineret felt til hvert af objekterne ved hjælp af det samme feltnavn på tværs af alle objekter. Det er muligt at oprette brugerdefinerede plug-ins for at relatere poster i de objekter, der deltager i indsendelses-/godkendelsesflowet, ved hjælp af objekterne transaktionsoprindelse og transaktionsforbindelse.  

### <a name="delegate-time-and-expense-entry"></a>Uddelegere tids- og udgiftsregistrering
Common Data Service-platformen understøtter ikke, at en bruger efterligner en anden, hvilket betyder, at uddelegeret tidsregistrering og udgiftspost ikke understøttes i version 3 af Project Service Automation. Partnere og kunder har imidlertid brugt en løsning til aktivering af understøttelse for uddelegerede tidsregistreringsoplevelse i version 3. Dette er kun en midlertidig løsning og ikke en færdig løsning, så det er vigtigt at forstå begrænsningerne og kun bruge denne fremgangsmåde, hvis begrænsningerne er acceptable. 

> [!IMPORTANT]
> Disse oplysninger skal kun betragtes som vejledende vejledning til brugerdefineret implementering af en partner/kunde. Produktteamet tilbyder ikke formel support til denne funktion via en af vores supportkanaler.

### <a name="customization-details"></a>Tilpasningsdetaljer 
Tilpasning giver dig mulighed for tilføje **Reserverbar ressource** for at oprette og redigere oplevelser, som tillader en bruger at fungere som en stedfortræder ved at ændre feltet til **reservation af ressource** til en anden bruger, der skal registreres tids- og udgiftsposter for. Følgende fremgangsmåde dækker delegering af tidsregistrering. De samme oplysninger gælder for delegering af udgiftsposter. 
 
1.  Sørg for, at den stedfortrædende bruger har global sikkerhedsadgang til projekter og projektopgaver. 
1.  Da **Reserverbar ressource**, som er et felt i objektet **Tidsregistrering**, ikke er vist på siden **Hurtig oprettelse**, skal du tilføje det.

    eller

    Opret en brugerdefineret visning, som indeholder kolonnen **Reserverbar ressource**, således at den kun viser tidsregistreringer, der er oprettet for ressourcen. Publicer tilpasningerne i appmoduldesigneren, så du kan se denne visning under **Visningsvælger** på siden **Tidsregistreringer**. Der findes to plug-ins, som håndterer indstillingen af leder for tidsregistreringer, der ikke er relateret til et projekt:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Opret en ny plug-in for at overskrive feltet **Leder** med lederen af den bruger, der er tildelt i feltet **Reserverbar ressource**. Brug samme **Udførelsesfase** som out-of-band (OOB) plug-in'en (før validering), og brug en **Udførelsesrækkefølge**, der er højere end OOB-plug-in'en (større end 1). Dette sikrer, at den brugerdefinerede plug-in er kørt efter OOB-plug-ins.  
 
### <a name="end-user-experience"></a>Slutbrugeroplevelse
1.  Når du opretter en tidsregistrering på siden til hurtig oprettelse, skal du angive oplysningerne om projektet og projektopgaven og derefter vælge brugeren i feltet **Reserverbar ressource**, som tidsregistreringerne skal registreres for. 
2.  Dette felt er som standard angivet til den bruger, der er logget på, men da brugeren har tilsidesat dette felt, oprettes tidsregistreringen nu for den valgte **Reserverbar ressource**.
3.  Når du sender de tidsregistreringer, du har oprettet for disse poster, sættes registreringerne i kø til godkenderen i projektet som forventet. 
4.  Når du tilbagekalder de tidsregistreringer, der er oprettet for den anden bruger, returneres tidsregistreringerne til tilstanden **Kladde** med feltet **Reserverbar ressource** angivet til den anden bruger. 
5.  Du kan også vælge at skifte til den brugerdefinerede visning for at filtrere tidsregistreringer, der er oprettet for den anden bruger. 
 
### <a name="limitations"></a>Begrænsninger
Funktionaliteten **Kopiér** og **Importér** fungererer kun i forbindelse med den bruger, der er logget på. Det betyder, at det ikke er muligt at kopiere eller importere tidsregistreringer, der er oprettet for den bruger, der er logget på som den reserverbare ressource.

Tidsregistreringer, der ikke er til et projekt, distribueres kun til godkendelse hos lederen af den reserverbare ressource, hvis trin 4 i sektionen **Tilpasningsdetaljer** ovenfor er fuldført. Ellers vil tidsregistreringer, der ikke er relateret til et projekt, for den anden bruger fejlagtigt blive distribueret til lederen af den bruger, der er logget på. 

### <a name="other-changes"></a>Andre ændringer 
Funktionaliteten **Reservationer og opgaver** er blevet fjernet. 

## <a name="multidimensional-pricing"></a>Flerdimensionel prisfastsættelse
For at få mest mulig fleksibilitet og opfylde forskellige forretningskrav understøtter version 3 af Project Service Automation diskret anvendelse af prisdimension til omkostnings- og faktureringssatser. Dimensionsværdier kan angives som standard og derefter overføres via omkostnings- og prissætningsprocessen fra ressourceprofilering til tidsregistrering til faktiske projektoplysninger. Kundespecifik konfiguration og ændring eller udvidelse gør brug af infrastruktur med mulighed for standardtilpasning.

Project Service Automation leveres sammen med et standardsæt prisdimensioner og -roller og ressourceenheder og gør det muligt at konfigurere priser og omkostninger for hver kombination af rolle og organisationsenhed.

For Project Service Automation-kunder, der vil fortsætte med at bruge disse standardfelter som prisdimensioner i version 3, er der ingen bemærkelsesværdige ændringer. Du kan fortsætte med at bruge Project Service Automation, som du plejer. Men hvis du har brug for at foretage pris- eller omkostningsberegninger for dine ressourcer ved hjælp af andre ekstra attributter, kan du bruge version 3 til at føje dine egne brugerdefinerede prisdimensioner til Project Service Automation. Udvidelsen af brugerdefinerede prisdimensioner er en kompliceret konfigurationsoplevelse. 

## <a name="quotes-and-contracts"></a>Tilbud og kontrakter
I version 3 af Project Service Automation er aspekter i forbindelse med konfiguration og administration af tilbud og kontrakter blevet ændret. Du kan finde mere detaljerede oplysninger i følgende sektioner.

### <a name="set-up-chargeability-options"></a>Konfigurere indstillinger for fakturerbarhed
I version 1 og 2 blev opsætningen af fakturerbarhed for roller og kategorier for bestemte tilbud og kontrakter udført ved hjælp af visningen **Fakturerbarhed**, der fandtes i den øverste navigation på en tilbudslinje eller en kontraktlinje. Det var også her, du kunne konfigurere priser for disse roller og udgiftskategorier.

Fra og med version 3 udføres konfiguration af indstillinger for fakturerbarhed efter rolle og udgiftskategori på tilbuds- eller kontraktlinjeniveau. Prisopsætning er adskilt fra opsætning af fakturerbarhed. Du kan finde **Fakturerbare roller** og **Fakturerbare kategorier** som faner på siderne **Tilbudslinje** og **Kontraktlinje**, uden at det er nødvendigt at bruge det øverste navigationsområde.

![Fakturerbare roller.](media/chargeable-12.png)
 
Konfigurationen af Fakturerbare roller og Fakturerbare kategorier bruges også standardgitterkontrolelementet, der kan redigeres. For de enkelte roller og kategorier forbliver de understøttede indstillinger for faktureringstype under tilbuds- og kontraktfasen uændret i forhold til tidligere versioner som **Fakturerbar** og **Ikke-fakturerbar**. **Gratis** er ikke en understøttet type i tilbuds- eller kontraktfasen. **Gratis** understøttes kun i forbindelse med tids- eller udgiftsgodkendelse.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Oprette og redigere brugerdefinerede priser for et Project Service Automation-tilbud og en projektkontrakt
I version 1 og 2 foregik brug af brugerdefineret prisliste til bestemte tilbud og kontrakter ved hjælp af **Rediger priser** i visningen **Fakturerbarhed**. Visningen **Fakturerbarhed** var placeret i det øverste navigationsområde til en tilbudslinje eller en kontraktlinje. Det var også her, du kunne konfigurere indstillinger for fakturerbarhed for rolle- og/eller udgiftskategorier.

Fra og med version 3 er oprettelse og brug af en brugerdefineret projektprisliste for et Project Service Automation-tilbud og en Project Service Automation-projektkontrakt adskilt fra opsætningen af fakturerbarhed. Project service Automation-tilbud og Project Service Automation-projektkontrakter har fået en ny fane kaldet **Projektprislister**. Denne fane vises en tilknyttet visning af alle de projektprislister, der er knyttet til Project Service Automation-tilbuddet eller projektkontrakten. Hvis du vil oprette en brugerdefineret prisliste ud fra en eksisterende prisliste, der allerede er knyttet til projekttilbuddet, skal du klikke på **Opret brugerdefineret prissætning**. Derved oprettes der en kopi af alle de tilknyttede prislister, som kan knyttes til tilbuddet eller kontrakten. Du kan nu åbne prislisten og redigere rolle- eller udgiftskategoriprisen, så disse prisændringer kun gælder for dette tilbud eller denne kontrakt. 
  
Følgende grafik er før oprettelse af brugerdefinerede prislister.

![Før brugerdefinerede prislister.](media/before-custom-price-lists-13.png)

Følgende grafik er efter oprettelse af brugerdefinerede prislister.

![Efter brugerdefinerede prislister.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Når du klikker på **Opret brugerdefineret prissætning**, kan der være en kort forsinkelse, før den brugerdefinerede prisliste er oprettet. Det anbefales, at du opdaterer gitteret i stedet for at klikke flere gange. Der er oprettet en brugerdefineret prisliste, hvis navnet på den tilknyttede prisliste har tilbudsnavnet eller projektkontraktnavnet tilføjet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]