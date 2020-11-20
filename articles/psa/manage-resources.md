---
title: Administrer ressourcer
description: Dette emne indeholder oplysninger om, hvordan du kan administrere ressourcer.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132326"
---
# <a name="manage-resources"></a>Administrer ressourcer

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation indeholder et ressourcestyringsdashboard, der giver en visuel oversigt over ressourcebehov og tidsforbrug i hele organisationen. Du kan bruge diagrammerne på dette dashboard til at få vist følgende oplysninger:

- **Ressourcekrav** – diagrammet **Aktive anmodninger om ressourcer** viser de ressourcer, der er sendt. Ressourcerne samles efter enten rolle eller projekt.
- **Ikke sendt ressourcekrav** – diagrammet **Ikke-tildelt ressourcekrav** viser alle de ressourcekrav, der ikke er blevet sendt. Den hjælper ressourcestyringen til at få vist krav, der ikke er faste, og som muligvis kan sendes via en anmodning om ressourcer.
- **Fakturerbart tidsforbrug for sidste uge** – diagrammet **Tidsforbrug efter rolle** viser procentdelen af organisationens faktiske fakturerbare tidsforbrug efter rolle i forhold til målets fakturerbare tidsforbrug efter rolle.

    > [!NOTE]
    > Hvis du vil stille diagrammet **Tidsforbrug efter rolle** til rådighed, skal du oprette et jo, der kører i arbejdsprocessen UpdateRoleUtilization. Dette tilbagevendende job kører hver 7. dag for at beregne fakturerbart tidsforbrug for de foregående syv dage. Resultaterne samles efter rolle.

## <a name="manage-project-team-members"></a>Administrere projektteammedlemmer

Projektledere kan bruge ressourcestyringsdashboardet til at styre ressourcer i projekter. De kan f.eks. føje et teammedlem direkte til et projekt og reservere et teammedlem for at opfylde de ressourcekrav, der er registreret af en generisk ressource.

### <a name="add-a-team-member-directly-to-a-project"></a>Føje et teammedlem direkte til et projekt

Hvis du vil føje et teammedlem direkte til et projekt, skal du vælge **Ny** under fanen **Team** på siden **Projekter**. Dialogboksen **Hurtig oprettelse: Medlem af projektteam** vises. I denne dialogboks kan du udføre følgende opgaver:

- **Reservere en navngivet ressource** – vælg navnet på ressourcen i feltet **Reserverbar ressource**. Vælg derefter rollen, angiv perioden, og vælg en fordelingsmetode. Den navngivne ressource, du har valgt, føjes til projektet ved hjælp af den valgte fordelingsmetode og ressourcekalenderen.
- **Tilføj en generisk ressource** – undlad at udfylde feltet **Reserverbar ressource**, og vælg derefter rollen, angiv perioden, og vælg den ønskede fordelingsmetode. Der føjes en generisk ressource til teamet som en pladsholder for det kravsmønster, der bruges til at reservere navngivne ressourcer i teamet. Kravet fremsættes i henhold til projektkalenderen.
- **Føj en navngivet ressource til teamet uden at forbruge ressourcekapacitet** – vælg en ressource i feltet **Reserverbar ressource**. Vælg derefter perioden, og vælg **Ingen** som allokeringsmetode. Ressourcen føjes til teamet, men ressourcens kapacitet forbruges ikke via en reservation.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservere et teammedlem for at opfylde ressourcekravene for en generisk ressource

I PSA kan du reservere en generisk ressource i et projektteam, og du kan angive rollen, den nødvendige kapacitet og måden kapaciteten distribueres på. Du kan angive de attributter, der er knyttet til den generiske ressource, i ressourcekravet. Disse attributter omfatter påkrævede færdigheder, den foretrukne organisationsenhed og de foretrukne ressourcer.

Følg disse trin for at angive de nødvendige færdigheder for en generisk ressource for en udvikler.

1. Vælg **Ny** under fanen **Team** på siden **Projekter** for at reservere en generisk ressource.

    ![Generisk ressource, der er reserveret til teamet](media/Resource-Management-image9.png)

2. I kolonnen **Ressourcekrav** i visningen **Alle teammedlemmer** skal du vælge linket for at føje påkrævede færdigheder til den generiske ressource.

    ![Link til krav](media/Resource-Management-image10.png)

3. På siden **Ressourcekrav**, der vises, skal du i gitteret **Færdigheder** vælge ellipsen (**...**) og derefter vælge **Tilføj ny kravsegenskab** for at tilføje de påkrævede færdigheder for din udvikler.

    ![Kommandoen Tilføj ny kravsegenskab](media/Resource-Management-image11.png)

4. I dialogboksen **Hurtig oprettelse: Kravsegenskab**, der vises, skal du vælge den påkrævede færdighed i feltet **Egenskab**. Vælg derefter ressourcekundskabsniveauet for den pågældende færdighed i feltet **Klassificeringsværdi**. Endelig skal du i feltet **Ressourcekrav** angive kravet til kildens ressourcer fra organisationsenheder eller endda navngivne ressourcer. Vælg **Gem**, når du er færdig.

    ![Hurtig oprettelse: dialogboksen Kravsegenskab](media/Resource-Management-image12.png)

5. Vælg **Reservér** på siden **Ressourcekrav** for at opfylde ressourcekravet.

    ![Reservér-knap på siden Ressourcekrav](media/Resource-Management-image13.png)

    Du kan også vælge den generiske ressource i gitteret **Alle teammedlemmer** og derefter vælge **Reservér**.

    ![Knappen Reservér over gitteret Alle teammedlemmer](media/Resource-Management-image14.png)

    > [!NOTE]
    > I dette eksempel er der behov for 40 timer, men der er ikke reserveret nogen timer, fordi generiske ressourcer ikke har reservationer. Derudover er der ingen tildelte timer, da den generiske ressource blev føjet direkte til teamet. Den blev ikke tilføjet ved hjælp af opgavetildeling.

    På siden **Planlægningsassistent** kan du filtrere tilgængelige ressourcer efter de krav, der er angivet i ressourcekravet. Ressourcer sorteres i henhold til de sorteringsparametre, der er angivet i planlægningsområdet.

    ![Siden Planlægningsassistent](media/Resource-Management-image15.png)

    Her er nogle filtre, der ofte bruges:

    - **Egenskaber sammen med en klassificering** – filtrér efter færdigheder, certificeringer og andre ressourcekvaliteter ud over klassificeringer af kompetence.
    - **Roller** – filtrér efter de standardroller, der er tildelt de reserverbare ressourcer.
    - **Organisationsenheder** – filtrér de reserverbare ressourcer efter de organisationsenheder, de er tildelt til.

6. Hvis du ikke er tilfreds med resultaterne af den første søgning efter krav, kan du ændre filterkriterierne. Udvid ruden **Filtervisning** til venstre, og vælg derefter **Søg** for at søge efter flere ressourcer.

    ![Ruden Filtervisning](media/Resource-Management-image16.png)

7. Hvis du vil ændre den måde, resultater sorteres på, skal du vælge **Sortér**.

    ![Kommandoen Sortér](media/Resource-Management-image17.png)

8. Vælg ressourcer i henhold til det behov, der er angivet for kravet som vist øverst i gitteret. Du kan fjerne markeringen af celler i gitteret og lade ressourcekapaciteten være åben. Det er kun muligt at markere én ressource ad gangen som reserveret.

9. Vælg **Reservér** for at reservere den valgte ressource, og lad planlægningsområdet forblive åbent, så du kan vælge flere ressourcer. Du kan også vælge **Reservér og luk** for at reservere den valgte ressource og lukke planlægningsområdet.

    ![Ressource, der skal reserveres](media/Resource-Management-image19.png)

    Du modtager en meddelelse om besked om reserverede timer. Behovsindikatorerne viser, hvor meget af reservationskravet der er opfyldt, og hvor meget der er tilbage. Du kan også se, hvor meget af den valgte ressources kapacitet, der er forbrugt. Vælg **Udvid** for at få vist flere detaljer om ressourcereservationer.

9. Vend tilbage til visningen **Alle teammedlemmer**. Bemærk, at den generiske ressource er blevet erstattet af den navngivne ressource i gitteret, og at 40 timer vises som reserveret for den pågældende ressource.

    ![Opdateret Alle teammedlemmer-gitter](media/Resource-Management-image20.png)

    > [!NOTE]
    > Der vises ingen tildelte timer, da de er reserveret direkte i teamet. De blev ikke reserveret ved hjælp af opgavetildeling.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tildele generiske ressourcer til opgaver og oprette ressourcekrav

I PSA kan du oprette opgaver og derefter tildele generiske ressourcer til dem. På denne måde kan ressourcebehov repræsenteres af pladsholdere, mens du vurderer din tidsplan og økonomiske tal. Du kan derefter oprette ressourcekrav for de generiske ressourcer og opfylde dem.

1. På siden **Projekter** skal du vælge **Tilføj** under fanen **Tidsplan** for at oprette en opgave.

    ![Ny opgave er oprettet](media/Resource-Management-image21.png)

2. Vælg symbolet for **Ressourcevælger** i feltet **Ressourcer**. Ressourcevælgeren vises og viser eksisterende teammedlemmer for projektet.

    ![Ressourcevælger](media/Resource-Management-image22.png)

3. Angiv navnet på den nye generiske ressource, og vælg derefter **Opret**.

    ![Navnet på en ny generisk ressource er angivet](media/Resource-Management-image23.png)

4. I dialogboksen **Hurtig oprettelse: Medlem af projektteam**, der vises, skal du i feltet **Rolle** vælge rollen for den generiske ressource. I feltet **Ressourceenhed** skal du vælge organisationsenheden for den generiske ressource. Vælg derefter **Gem**.

    ![Dialogboksen Hurtig oprettelse: Medlem af projektteam](media/Resource-Management-image24.png)

    Det generiske teammedlem tildeles nu til opgaven.

    ![Generisk teammedlem, der er tildelt til opgaven.](media/Resource-Management-image25.png)

    Under fanen **Team** kan du se det nye generiske teammedlem. Bemærk, at det kun har tildelte timer. Disse timer er summen af alle opgaver, der er tildelt til det generiske teammedlem. Det generiske teammedlem har endnu ikke de påkrævede timer eller et ressourcekrav.

    ![Generisk teammedlem under fanen Team](media/Resource-Management-image26.png)

5. Du kan nu tildele det generiske teammedlem til andre opgaver ved hjælp af ressourcevælgeren.

    ![Generisk teammedlem i ressourcevælgeren](media/Resource-Management-image27.png)

    Når du er færdig med at tildele den generiske ressource til opgaver, kan du oprette et ressourcekrav for den generiske ressource.

5. Vælg den generiske ressource, og vælg derefter **Generer krav** under fanen **Team**.

    ![Kommandoen Generer krav](media/Resource-Management-image28.png)

    Når behovet er genereret, har det generiske teammedlem de nødvendige timer og et link til ressourcebehovet.

    ![Link til ressourcekrav](media/Resource-Management-image29.png)

    Når du har reserveret en navngivet ressource, fjernes den generiske ressource fra teamet og erstattes af den navngivne ressource.

    ![Generisk ressource, der er erstattet af den navngivne ressource](media/Resource-Management-image30.png)

    Under fanen **Tidsplan** fjernes de generiske ressourcetildelinger og erstattes med den navngivne ressource.

    ![Generiske ressourcetildelinger erstattet med den navngivne ressource under fanen Tidsplan](media/Resource-Management-image31.png)

    > [!NOTE]
    > Denne funktionsmåde forekommer kun, når en navngivet ressource er helt reserveret til det generiske ressourcekrav. Når en navngivet ressource delvist erstatter det generiske ressourcekrav, eller hvis flere navngivne ressourcer erstatter det generiske ressourcekrav, forbliver den generiske ressource tildelt til opgaven.

    I følgende illustration er der planlagt en 80 timers opgave med en varighed på fem dage (16 timer pr. dag over fem dage), og den er tildelt den generiske ressource med navnet **Funktionelt**.

    ![Fem dages opgave med 80 timer tildelt til den generiske ressource Funktionelt](media/Resource-Management-image32.png)

    Når du opretter kravet, er det for 80 timer fordelt over fem dage.

    ![Krav, der er oprettet for 80 timer fordelt over fem dage](media/Resource-Management-image33.png)

    Da tilgængelige ressourcer kun arbejder otte timer om dagen, skal der bruges to ressourcer til at imødekomme behovet.

    ![Anden ressource](media/Resource-Management-image35.png)

    Under fanen **Team** kan du nu se, at den generiske ressource ikke har nogen påkrævede timer, men de tildelte timer vises stadig sammen med de to navngivne ressourcer, der udgør indfrielsen.

    ![To navngivne ressourcer under fanen Team](media/Resource-Management-image36.png)

    Under fanen **Tidsplan** forbliver den generiske ressource tildelt til opgaven.

    ![Generiske ressourcer under fanen Tidsplan](media/Resource-Management-image37.png)

PSA tildeler ikke begge ressourcer til opgaven, da denne funktionsmåde ville resultere i en mindre forudsigelig tidsplan. I dette enkle eksempel er det nemt at opdele timerne ligeligt mellem to ressourcer. I mere komplekse scenarier, der omfatter flere opgaver og flere ressourcer, ville PSA dog være nødt til at antage, hvordan de reservationer, der modtages for flere ressourcer, skal fordeles hen over flere opgaver.

I disse scenarier er projektlederen derfor ansvarlig for at analysere flere reservationer og tildele dem efter behov. For at kunne fordele reservationerne tildeler projektlederen opgaverne fra de generiske ressourcer til de navngivne ressourcer og bruger derefter visningen **Afstemning** til at sikre, at fordelingen fungerer sammen med reservationerne.

### <a name="edit-a-resource-requirement"></a>Redigere et ressourcekrav

Når der er oprettet et ressourcekrav, vil en projektleder eller ressourcestyring muligvis redigere oplysningerne for at begrænse søgekriterierne, når planlægningsområdet bruges. Benyt følgende fremgangsmåde for at redigere ressourcekravet.

1. Vælg linket til et vilkårligt krav for en generisk ressource under fanen **Team** på siden **Projekter**.
2. På siden **Ressourcekrav**, der vises, kan du opdatere flere attributter. Her er nogle eksempler:

    - Navn
    - Fra-dato
    - Til-dato
    - Varighed
    - Ressourcetype

På siden **Ressourcekrav** kan projektlederen eller ressourcestyring også definere følgende oplysninger:

- Færdigheder
- Roller
- Ressourcepræferencer
- Foretrukket organisationsenhed

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Opdatere ressourcereservationer, efter at de er reserveret til et projekt

Når du har føjet en generisk eller navngivet ressource til et projektteam, kan du ændre ressourcens reservationer.

1. På siden **Projekter** skal du under fanen **Team** vælge et teammedlem og derefter vælge **Vedligehold reservationer**.

    ![Planlægningsområde, der er åbnet for det valgte teammedlem](media/Resource-Management-image40.png)

    Planlægningsområdet vises og angiver projektteammedlemmets reservationer. Udvid teammedlemmets post for at få vist de timer, der er reserveret i forhold til dette projekt og andre projekter, der forbruger teammedlemmets kapacitet.

2. Markér reservationen, og træk den, så den udvides eller forkortes. Dialogboksen **Opret ressourcereservation** vises, hvor du kan justere reservationen.

    ![Dialogboksen Opret ressourcereservation](media/Resource-Management-image41.png)

3. Højreklik på reservationen. Du kan derefter bruge genvejsmenuen til at fuldføre følgende handlinger:

    - Ændre reservationens status.
    - Redigere reservationen.
    - Erstatte en ressource i projektteamet.

### <a name="change-the-booking-status"></a>Ændre reservationens status

Du kan ændre en hvilken som helst standardreservationsstatus eller brugerdefineret reservationsstatus.

![Kommandoen Skift status](media/Resource-Management-image42.png)

Følgende statusser findes i PSA:

- **Annulleret** – denne status annullerer en ressources reservation og frigør ressourcens kapacitet.
- **Reservér definitivt** – denne status forbruger en ressources kapacitet. En reservation har som regel denne status, når du åbner **Vedligehold reservationer** i gitteret **Alle teammedlemmer** på siden **Projekter**.
- **Reservér foreløbigt** – denne status føjer en ressource til et team, men forbruger ikke ressourcens kapacitet. Det angiver, at ressourcen er reserveret til potentielt arbejde, men stadig har kapacitet, hvis det kræves til andre job. I visningen af den samlede ressourcetilgængelighed har foreløbige reservationer en anden status end definitive reservationer.
- **Foreslået** – denne status repræsenterer ressourcestyrings eller projektleders forslag til en ressource. Forslag forbruger ikke en ressources kapacitet, og ressourcen føjes ikke til projektteamet. For at reservere ressourcen definitivt i teamet skal projektlederen acceptere forslaget.

### <a name="submit-resource-requests"></a>Sende anmodninger om ressourcer

Anmodninger om ressourcer bruges til at overføre behovet (ressourcekrav), der skal opfyldes af ressourcestyring. I forbindelse med en generisk ressource, som allerede findes i teamet, kan du sende en anmodning om ressource direkte. En anmodning om ressource kan opfyldes på to måder:

- Ressourcestyring opfylder anmodningen direkte. I dette tilfælde erstattes den generiske ressource med en definitiv reservation, der har en navngivet ressource.
- Ressourcestyring foreslår en ressource til projektlederen, og projektlederen godkender eller afviser den foreslåede ressource.

#### <a name="direct-fulfillment-of-resource-requests"></a>Direkte opfyldelse af ressourceanmodninger

Når der genereres et ressourcekrav, kan en projektleder sende en ressourceanmodning om en generisk ressource ved at markere ressourcen og derefter vælge **Send anmodning**.

![Knappen Send anmodning](media/Resource-Management-image45.png)

Kommentarer til ressourcen kan gives til ressourcestyringen, der opfylder anmodningen. Når anmodningen er sendt, ændres feltet **Status** for teammedlemmet til **Sendt**.

![Indtastning af valgfrie kommentarer](media/Resource-Management-image46.png)

Når ressourcestyringen opfylder anmodningen, erstattes det generiske teammedlem af den navngivne ressource i gitteret **Alle teammedlemmer**.

![Generisk teammedlem erstattet med den navngivne ressource i gitteret Alle teammedlemmer](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Bruge et ressourceforslag til ressourceanmodninger

I stedet for at reservere en ressource direkte i en anmodning om ressource kan ressourcestyring foreslå en ressource til projektlederen. En ressourcestyring kan bruge denne indstilling, når der ikke findes et nøjagtigt match med kravene. Når ressourcestyring foreslår en ressource, kan projektlederen se, at feltet **Status** for det generiske teammedlem ændres til **Skal gennemses**.

![Generisk teammedlems status er ændret til Skal gennemses](media/Resource-Management-image48.png)

Hvis du vil have vist den foreslåede ressource sammen med en visualisering af effekten af reservationen for tilbuddet, skal du dobbeltklikke på det teammedlem, der har statussen **Skal gennemses**. Vælg derefter fanen **Foreslåede ressourcer**.

![Fanen Foreslåede ressourcer](media/Resource-Management-image49.png)

Vælg **Acceptér alle forslag** for at acceptere alle foreslåede ressourcer eller **Afvis alle forslag** for at afvise dem. Hvis du accepterer de foreslåede ressourcer, bliver de definitivt reserveret til projektet som teammedlemmer og erstatter de generiske ressourcer.

> [!NOTE]
> Du skal enten acceptere eller afvise alle foreslåede ressourcer. Du kan ikke acceptere eller afvise dem delvist.

### <a name="substitute-a-resource-on-the-project-team"></a>Erstatte en ressource i projektteamet

En projektleder må undertiden erstatte et reserveret teammedlem i et projekt.

1. På siden **Projekter** skal du under fanen **Team** vælge den ressource, der skal erstattes, og derefter vælge **Vedligehold reservationer**.
2. Udvid ressourcen for at få vist de projekter, den er tildelt til.

    ![Udvidet ressourcen, der viser tildelte projekter](media/Resource-Management-image50.png)

3. Højreklik på projektet, og vælg derefter **Erstat ressource**.
4. Hvis du ved, hvilken ressource du vil bruge som erstatning for den aktuelle ressource, skal du vælge eller skrive navnet og derefter vælge **Tildel igen**.

    ![Angive en erstatningsressource](media/Resource-Management-image51.png)

    Du kan også benytte denne fremgangsmåde for at søge efter en ressource:

    1. Vælg **Find erstatning**.

        ![Søgning efter en erstatningsressource](media/Resource-Management-image52.png)

        Planlægningsassistenten returnerer en liste over tilgængelige erstatninger. I planlægningsassistenten kan du filtrere de tilgængelige ressourcer yderligere for at finde en passende erstatning.

        ![Liste over tilgængelige erstatninger](media/Resource-Management-image53.png)

    2. Når du vil erstatte ressourcen, skal du vælge den ressource, du vil bruge, og derefter vælge **Erstat**.

        ![Erstatningsressource valgt](media/Resource-Management-image54.png)

    Reservationerne og tildelingerne erstattes med den nye ressource.

    ![Reservationer og tildelinger erstattet med den nye ressource](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Afstemme teammedlemmers reservationer og tildelinger

For teammedlemmer er reservationer og tildelinger løst sammenkædet. Med andre ord kan ressourcer have tildelinger men ingen reservationer, eller de kan have reservationer men ingen tildelinger. Ideelt set skal reservationer og tildelinger justeres, så ressourcer har bindende kapacitet til at udføre opgavetildelingerne. Reservationerne kan dog muligvis være baseret på tilgængelighed, og opgavetidspunkter kan ændres, efterhånden som projektet fortsætter. Derfor giver den løse sammenkædning mellem reservationer og tildelinger fleksibilitet.

PSA har fanen **Afstemning**, som projektledere kan bruge til at afstemme teammedlemmernes reservationer og tildelinger af disse til projektgrupper.

![Fanen Afstemning](media/Resource-Management-image56.png)

Fanen **Afstemning** viser reservationer og tildelinger helt ned til niveauet for de enkelte opgavetildelinger for hvert teammedlemmer. Den viser timer i celler, der repræsenterer tidsperioder fra måneder ned til dage.

Under fanen vises også en samlet netto i alt for projektet sammen med en kolonnetotal.

For hver ressource beregner fanen forskellen mellem teammedlemmets reservationer og en akkumulering af teammedlemmets opgavetildelinger. Ideelt skal forskellen være 0 (nul). Det vil sige, at der ikke bør være nogen forskel mellem reservationer og tildelinger. Forskelle er farvede og nedtonede for at henlede opmærksomheden på to forhold:

- **Manglende reservation** – der opstår manglende reservation, når en ressource har flere tildelinger end reservationer. Da denne kapacitet ikke er reserveret, vil en projektleder muligvis rette dette forhold ved at forlænge reservationer af ressourcen for at dække underskuddet.
- **Overskydende reservationer** – Der forekommer overskydende reservationer, når en ressource er blevet reserveret til projektet, men ikke er tildelt opgaver. Dette forhold kan være acceptabelt i de tilfælde, hvor ressourcen blev reserveret til projektet, før opgavetildeling fandt sted. I andre tilfælde er ressourcen dog ikke planlagt til at blive tildelt til opgaver. I disse tilfælde skal projektlederen overveje at annullere reservationerne af ressourcen, så kapaciteten kan bruges til et andet projekt.

Når du i visse tilfælde får vist tiden på et højere niveau end dagsniveau (f.eks. månedsniveau), kan du muligvis se en nettoforskel på nul for en ressource (med andre ord reservationer = tildelinger). Men hvis du får vist tiden på ugeniveau, kan du muligvis se, at der er tildelinger på 0 timer og reservationer på 40 timer i den første uge, men tildelinger på 40 timer og reservationer på nul timer i løbet af den anden uge. Generelt afstemmes reservationerne og tildelingerne, men de er forskellige fra den ene uge til den næste.

Når du får vist tiden på højere niveauer, har fanen **Afstemning** en indikator, der giver dig besked om, at der er forskelle på lavere niveauer. Når du dobbeltklikker på en celle, kan du zoome ind for at få vist forskellen. Du kan derefter højreklikke for at zoome ud. Hvis du vælger en ressource og derefter bruger kontrolelementet **Næste difference** på værktøjslinjen for gitteret, kan du gå til den næste forskel mellem reservationer og tildelinger for den pågældende ressource. Du kan derefter bruge kontrolelementet **Forrige difference** til at gå tilbage. Du kan også slå differenceindikatoren og funktionsmåden for navigation fra under **Indstillinger**.

![Differenceindikator](media/Resource-Management-image57.png)

Hvis du har opgavetildelinger for en ressource men ingen reservationer, skal du under fanen **Afstemning** på siden **Projekter** vælge den manglende reservation og derefter vælge **Udvid reservation**. Dialogboksen **Udvid reservation** vises og angiver den reservation, der skal bruges for at løse manglen på ressource. Den viser også ressourcens eksisterende reservationer på tværs af alle projekter eller andre objekter, der kan planlægges. Hvis du vælger **OK** for at oprette reservationen for ressourcen, uanset den pågældende ressources tilgængelighed, kan det medføre overreservation.

![Dialogboksen Udvid reservation](media/Resource-Management-image58.png)

Projektlederen eller ressourcestyringen kan derefter bruge planlægningsområdet til at administrere de situationer, hvor en ressource overreserveres i forhold til dens kapacitet.
