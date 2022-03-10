---
title: Tilføj teammedlemmer fra teammedlemsgitteret
description: Dette emne indeholder oplysninger om, hvordan du kan administrere teammedlemsressourcer.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c4ff7792a9a99cbbe791a10dbc5157ffd51de285c02f23471532a09e7a55b031
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008399"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Tilføj teammedlemmer fra teammedlemsgitteret

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations indeholder et dashboard for Resource Manager, der giver en visuel oversigt over ressourcebehov og tidsforbrug i hele organisationen. Du kan bruge diagrammerne på dette dashboard til at få vist følgende oplysninger:

- **Ressourcekrav**: Diagrammet **Aktive anmodninger om ressourcer** viser de ressourcer, der er sendt. Ressourcerne samles efter enten rolle eller projekt.
- **Ikke sendt ressourcekrav**: Diagrammet **Ikke-tildelt ressourcekrav** viser alle de ressourcekrav, der ikke er blevet sendt. Dette diagram hjælper ressourceadministratoren med at vise de krav, der ikke er faste, og som muligvis kan sendes via en anmodning om ressourcer.
- **Fakturerbart tidsforbrug for sidste uge**: Diagrammet **Tidsforbrug efter rolle** viser procentdelen af organisationens faktiske fakturerbare tidsforbrug efter rolle i forhold til målets fakturerbare tidsforbrug efter rolle.

    > [!NOTE]
    > Hvis du vil stille diagrammet **Tidsforbrug efter rolle** til rådighed, skal du oprette et jo, der kører arbejdsprocessen **UpdateRoleUtilization**. Dette tilbagevendende job kører hver 7. dag for at beregne fakturerbart tidsforbrug for de foregående syv dage. Resultaterne samles efter rolle.

## <a name="manage-project-team-members"></a>Administrere projektteammedlemmer

Projektledere kan bruge ressourceadministratordashboardet til at styre ressourcer i projekter. De kan f.eks. føje et teammedlem direkte til et projekt og reservere et teammedlem for at opfylde de ressourcekrav, der er registreret af en generisk ressource.

### <a name="add-a-team-member-directly-to-a-project"></a>Føje et teammedlem direkte til et projekt

Hvis du vil tilføje et teammedlem direkte til et projekt, skal du vælge formularen **Projekter** under fanen **Team** og vælge **Nyt**. Dialogboksen **Hurtig oprettelse: Medlem af projektteam** vises. I denne dialogboks kan du udføre følgende opgaver:

- **Reservere en navngivet ressource**: Vælg navnet på ressourcen i feltet **Reserverbar ressource**. Vælg derefter rollen, angiv perioden, og vælg en fordelingsmetode. Den navngivne ressource, du har valgt, føjes til projektet ved hjælp af den valgte fordelingsmetode og ressourcekalenderen.
- **Tilføj en generisk ressource**: Undlad at udfylde feltet **Reserverbar ressource**, og vælg derefter rollen, angiv perioden, og vælg den ønskede fordelingsmetode. Der tilføjes en standardressource til teamet som en pladsholder. Pladsholderen indeholder det efterspørgselsmønster, der bruges til at reservere navngivne ressourcer i teamet. Kravet fremsættes i henhold til projektkalenderen.
- **Tilføj en navngivet ressource til teamet uden at forbruge ressourcekapacitet**: Vælg en ressource i feltet **Reserverbar ressource**. Vælg perioden, og vælg derefter **Ingen** som allokeringsmetode. Ressourcen føjes til teamet, men ressourcens kapacitet forbruges ikke via en reservation.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservere et teammedlem for at opfylde ressourcekravene for en generisk ressource

I Project Operations kan du reservere en generisk ressource i et projektteam. Du kan også angive rollen, den nødvendige kapacitet, og hvordan kapaciteten distribueres. Du kan for ressourcekravet angive de attributter, der er knyttet til den generiske ressource. Disse attributter omfatter påkrævede færdigheder, den foretrukne organisationsenhed og de foretrukne ressourcer.

Udfør følgende trin for at angive de nødvendige færdigheder for en generisk ressource for en udvikler.

1. På formularen **Projekter** under fanen **Team** skal du vælge **Ny** for at reservere en generisk ressource.
2. I kolonnen **Ressourcekrav** i visningen **Alle teammedlemmer** skal du vælge linket for at føje påkrævede færdigheder til den generiske ressource.
3. På Formularen **Ressourcekrav** skal du i gitteret **Færdigheder** vælge ellipsen (**...**) og derefter vælge **Tilføj ny egenskab for krav** for at tilføje de påkrævede færdigheder for din udvikler.
4. I dialogboksen **Hurtig oprettelse: egenskab for krav** skal du vælge den påkrævede færdighed i feltet **Egenskab**.
5. Vælg færdighedsniveauet for den pågældende færdighed i feltet **Klassificeringsværdi**. 
6. I feltet **Ressourcekrav** skal du angive kravet til kildens ressourcer fra organisationsenheder eller endda navngivne ressourcer. Vælg **Gem**, når du er færdig.
7. I formularen **Ressourcekrav** skal du vælge **Reserver** for at opfylde ressourcekravet. Du kan også vælge den generiske ressource i gitteret **Alle teammedlemmer** og derefter vælge **Reservér**.

    > [!NOTE]
    > I dette eksempel er der behov for 40 timer, men der er ikke reserveret nogen timer, fordi generiske ressourcer ikke har reservationer. Derudover er der ingen tildelte timer, da den generiske ressource blev føjet direkte til teamet fremfor at blive tilføjet ved hjælp af opgavetildeling.

    I formularen **Planlægningsassistent** kan du filtrere tilgængelige ressourcer efter de krav, der er angivet i ressourcekravet. Ressourcer sorteres i henhold til de sorteringsparametre, der er angivet i planlægningsområdet.

   Nogle af de mest almindeligt anvendte filtre er:

    - **Egenskaber sammen med en klassificering**: Filtrér efter færdigheder, certificeringer og andre ressourcekvaliteter ud over klassificeringer af kompetence.
    - **Roller**: Filtrér efter de standardroller, der er tildelt de reserverbare ressourcer.
    - **Organisationsenheder**: Filtrer de reserverbare ressourcer efter de organisationsenheder, de er tildelt til.

8. Hvis du ikke er tilfreds med resultaterne af den første søgning efter krav, kan du ændre filterkriterierne. Udvid ruden **Filtervisning** til venstre, og vælg derefter **Søg** for at søge efter flere ressourcer. Hvis du vil ændre den måde, resultater sorteres på, skal du vælge **Sortér**.
9. Vælg ressourcer i henhold til det behov, der er angivet for kravet som vist øverst i gitteret. Du kan fjerne markeringen af celler i gitteret og lade ressourcekapaciteten være åben. Det er kun muligt at markere én ressource ad gangen som reserveret.
10. Vælg **Reservér** for at reservere den valgte ressource, og lad planlægningsområdet forblive åbent, så du kan vælge flere ressourcer. Du kan også vælge **Reservér og luk** for at reservere den valgte ressource og lukke planlægningsområdet.
11. Vend tilbage til visningen **Alle teammedlemmer**. Bemærk, at den generiske ressource er blevet erstattet af den navngivne ressource i gitteret, og at 40 timer vises som reserveret for den pågældende ressource.

    > [!NOTE]
    > Der vises ingen tildelte timer, da de er reserveret direkte i teamet. De blev ikke reserveret ved hjælp af opgavetildeling.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tildele generiske ressourcer til opgaver og oprette ressourcekrav

I Project Operations kan du oprette opgaver og derefter tildele generiske ressourcer til dem. Ressourcebehov kan dernæst repræsenteres af pladsholdere, mens du vurderer din tidsplan og økonomiske tal. Du kan derefter oprette ressourcekrav for de generiske ressourcer og opfylde dem.

1. I formularen **Projekter** skal du vælge under fanen **Planlægning** vælge **Tilføj** for at oprette en opgave.
2. Vælg symbolet for **Ressourcevælger** i feltet **Ressourcer**. Ressourcevælgeren vises og viser eksisterende teammedlemmer for projektet.
3. Angiv navnet på den nye generiske ressource, og vælg derefter **Opret**.
4. I dialogboksen **Hurtig oprettelse: Medlem af projektteam**, der vises, skal du i feltet **Rolle** vælge rollen for den generiske ressource. 
5. I feltet **Ressourceenhed** skal du vælge organisationsenheden for den generiske ressource. Vælg derefter **Gem**. Det generiske teammedlem tildeles nu til opgaven.

   Under fanen **Team** kan du se det nye generiske teammedlem. Bemærk, at det kun har tildelte timer. Disse timer er summen af alle opgaver, der er tildelt til det generiske teammedlem. Det generiske teammedlem har ikke de påkrævede timer eller et ressourcekrav.

6. Du kan nu tildele det generiske teammedlem til andre opgaver ved hjælp af ressourcevælgeren.

   Når du er færdig med at tildele den generiske ressource til opgaver, kan du oprette et ressourcekrav for den generiske ressource.

7. Vælg den generiske ressource, og vælg derefter **Generer krav** under fanen **Team**. Når behovet er genereret, har det generiske teammedlem de nødvendige timer og et link til ressourcebehovet.

  Når du har reserveret en navngivet ressource, fjernes den generiske ressource fra teamet og erstattes af den navngivne ressource. Under fanen **Tidsplan** fjernes de generiske ressourcetildelinger og erstattes med den navngivne ressource.

  > [!NOTE]
  > Denne funktionsmåde forekommer kun, når en navngivet ressource er helt reserveret til det generiske ressourcekrav. Når en navngivet ressource delvist erstatter det generiske ressourcekrav, eller hvis flere navngivne ressourcer erstatter det generiske ressourcekrav, forbliver den generiske ressource tildelt til opgaven.

Project Operations tildeler ikke begge ressourcer til opgaven, da denne funktionsmåde ville resultere i en mindre forudsigelig tidsplan. I dette enkle eksempel er det nemt at opdele timerne ligeligt mellem to ressourcer. I mere komplekse scenarier, der omfatter flere opgaver og flere ressourcer, ville PSA dog være nødt til at antage, hvordan de reservationer, der modtages for flere ressourcer, skal fordeles hen over flere opgaver.

I disse scenarier er projektlederen derfor ansvarlig for at analysere flere reservationer og tildele dem efter behov. For at kunne fordele reservationerne tildeler projektlederen opgaverne fra de generiske ressourcer til de navngivne ressourcer og bruger derefter visningen **Afstemning** til at sikre, at fordelingen fungerer sammen med reservationerne.

### <a name="edit-a-resource-requirement"></a>Redigere et ressourcekrav

Når der er oprettet et ressourcekrav, vil en projektleder eller ressourceadministrator muligvis redigere oplysningerne for at begrænse søgekriterierne, når planlægningsområdet bruges. Benyt følgende fremgangsmåde for at redigere ressourcekravet.

1. Vælg linket til et vilkårligt krav for en generisk ressource i formularen **Projekter** under fanen **Team**.
2. I den viste formular **Ressourcekrav** skal du angive de nødvendige feltoplysninger

   I formularen **Ressourcekrav** kan projektlederen eller ressourceadministratoren også definere færdigheder, roller, ressourcepræferencer og den foretrukne organisationsenhed.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Opdatere ressourcereservationer, efter at de er reserveret til et projekt

Når du har føjet en generisk eller navngivet ressource til et projektteam, kan du ændre ressourcens reservationer.

1. I formularen **Projekter** skal du under fanen **Team** vælge et teammedlem og derefter vælge **Fasthold reservationer**.
 
   Planlægningsområdet vises og angiver projektteammedlemmets reservationer. Udvid teammedlemmets post for at få vist de timer, der er reserveret i forhold til dette projekt og andre projekter, der forbruger teammedlemmets kapacitet.

2. Markér reservationen, og træk den, så den udvides eller forkortes. Dialogboksen **Opret ressourcereservation** vises, hvor du kan justere reservationen.
3. Højreklik på reservationen. Du kan derefter bruge genvejsmenuen til at fuldføre følgende handlinger:

    - Ændre reservationens status
    - Rediger reservationen
    - Erstatte en ressource i projektteamet

### <a name="change-the-booking-status"></a>Ændre reservationens status

Du kan ændre en hvilken som helst standardreservationsstatus eller brugerdefineret reservationsstatus.

Følgende statusser er indeholdt i Project Operations:

- **Annulleret**: Annullerer en ressources reservation og frigør ressourcens kapacitet.
- **Reservér definitivt**: Forbruger en ressources kapacitet. En reservation har som regel denne status, når du åbner **Fasthold reservationer** i gitteret **Alle teammedlemmer** i formularen **Projekter**.
- **Reservér foreløbigt**: Tilføjer en ressource til et team, men forbruger ikke ressourcens kapacitet. Denne status angiver, at ressourcen er reserveret til potentielt arbejde, men stadig har kapacitet, hvis den kræves til andre job. I visningen af den samlede ressourcetilgængelighed har foreløbige reservationer en anden status end definitive reservationer.
- **Foreslået**: Repræsenterer ressourceadministratorens eller projektlederens forslag til en ressource. Forslag forbruger ikke en ressources kapacitet, og ressourcen føjes ikke til projektteamet. For at reservere ressourcen definitivt i teamet skal projektlederen acceptere forslaget.

### <a name="submit-resource-requests"></a>Indsend ressourceanmodninger

Anmodninger om ressourcer bruges til at overføre behovet eller ressourcekravet, der skal opfyldes af en ressourceadministrator. I forbindelse med en generisk ressource, som allerede findes i teamet, kan du sende en anmodning om ressource direkte. En anmodning om ressource kan opfyldes på to måder:

- Ressourceadministratoren opfylder anmodningen direkte. I dette tilfælde erstattes den generiske ressource med en definitiv reservation, der har en navngivet ressource.
- Ressourceadministratoren foreslår en ressource til projektlederen, og projektlederen godkender eller afviser den foreslåede ressource.

#### <a name="direct-fulfillment-of-resource-requests"></a>Direkte opfyldelse af ressourceanmodninger

Når der genereres et ressourcekrav, kan en projektleder sende en ressourceanmodning om en generisk ressource ved at markere ressourcen og derefter vælge **Send anmodning**. Kommentarer til ressourcen kan gives til ressourceadministratoren, der opfylder anmodningen. Når anmodningen er sendt, ændres feltet **Status** for teammedlemmet til **Sendt**. Når ressourceadministratoren opfylder anmodningen, erstattes det generiske teammedlem af den navngivne ressource i gitteret **Alle teammedlemmer**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Bruge et ressourceforslag til ressourceanmodninger

I stedet for at reservere en ressource direkte i en anmodning om ressource kan ressourceadministratoren foreslå en ressource til projektlederen. En ressourceadministrator kan bruge denne indstilling, når der ikke findes et nøjagtigt match med kravene. Når ressourceadministratoren foreslår en ressource, kan projektlederen se, at feltet **Status** for det generiske teammedlem ændres til **Skal gennemses**.

Du kan få vist den foreslåede ressource sammen med en visualisering af effekten af reservationen af forslaget. 

1. Dobbeltklik på det teammedlem, der har statussen **Skal gennemses**. 
2. Vælg fanen **Foreslåede ressourcer**.
3. Vælg **Acceptér alle forslag** for at acceptere alle foreslåede ressourcer eller **Afvis alle forslag** for at afvise dem. Hvis du accepterer de foreslåede ressourcer, bliver de definitivt reserveret til projektet som teammedlemmer og erstatter de generiske ressourcer.

> [!NOTE]
> Du skal enten acceptere eller afvise alle foreslåede ressourcer. Du kan ikke acceptere eller afvise dem delvist.

### <a name="substitute-a-resource-on-the-project-team"></a>Erstatte en ressource i projektteamet

En projektleder skal undertiden erstatte et reserveret teammedlem i et projekt.

1. I formularen **Projekter** skal du under fanen **Team** vælge den ressource, der skal erstattes, og derefter vælge **Fasthold reservationer**.
2. Udvid ressourcen for at få vist de projekter, den er tildelt til.
3. Højreklik på projektet, og vælg derefter **Erstat ressource**.
4. Hvis du ved, hvilken ressource du vil bruge som erstatning for den aktuelle ressource, skal du vælge eller skrive navnet og derefter vælge **Tildel igen**.

eller Hvis du vil søge efter en ressource, skal du benytte følgende fremgangsmåde.

1. Vælg **Find erstatning**.

   Planlægningsassistenten returnerer en liste over tilgængelige erstatninger. I planlægningsassistenten kan du filtrere de tilgængelige ressourcer yderligere for at finde en passende erstatning.

2. Når du vil erstatte ressourcen, skal du vælge den ressource, du vil bruge, og derefter vælge **Erstat**.   

   Reservationerne og tildelingerne erstattes med den nye ressource.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Afstemme teammedlemmers reservationer og tildelinger

For teammedlemmer er reservationer og tildelinger løst sammenkædet. Med andre ord kan ressourcer have tildelinger men ingen reservationer, eller de kan have reservationer men ingen tildelinger. Ideelt set skal reservationer og tildelinger justeres, så ressourcer har bindende kapacitet til at udføre opgavetildelingerne. Reservationerne kan dog muligvis være baseret på tilgængelighed, og opgavetidspunkter kan ændres, efterhånden som projektet fortsætter. Derfor giver den løse sammenkædning mellem reservationer og tildelinger fleksibilitet.

Project Operations har fanen **Afstemning**, som projektledere kan bruge til at afstemme teammedlemmernes reservationer og tildelinger af disse til projektteams.

Fanen **Afstemning** viser reservationer og tildelinger helt ned til niveauet for de enkelte opgavetildelinger for hvert teammedlemmer. Den viser timer i celler, der repræsenterer tidsperioder fra måneder ned til dage.

Under fanen vises også en samlet netto i alt for projektet sammen med en kolonnetotal.

For hver ressource beregner fanen forskellen mellem teammedlemmets reservationer og en akkumulering af teammedlemmets opgavetildelinger. Ideelt skal forskellen være 0 (nul). Det vil sige, at der ikke bør være nogen forskel mellem reservationer og tildelinger. Forskelle er farvede og nedtonede for at henlede opmærksomheden på to forhold:

- **Manglende reservation**: Forekommer, når en ressource har flere tildelinger end reservationer. Da denne kapacitet ikke er reserveret, vil en projektleder muligvis rette dette forhold ved at forlænge reservationer af ressourcen for at dække underskuddet.
- **Overskydende reservationer**: Forekommer, når en ressource er blevet reserveret til projektet, men ikke er tildelt opgaver. Dette forhold kan være acceptabelt i de tilfælde, hvor ressourcen blev reserveret til projektet, før opgavetildeling fandt sted. I andre tilfælde er ressourcen dog ikke planlagt til at blive tildelt til opgaver. I disse tilfælde skal projektlederen overveje at annullere reservationerne af ressourcen, så kapaciteten kan bruges til et andet projekt.

Når du i visse tilfælde får vist tiden på et højere niveau end dagsniveau, f.eks. månedsniveau, kan du muligvis se en nettoforskel på nul for en ressource. Med andre ord: reservationer = tildelinger. Men hvis du får vist tiden på ugeniveau, kan du muligvis se, at der er tildelinger på 0 timer og reservationer på 40 timer i den første uge, men tildelinger på 40 timer og reservationer på nul timer i løbet af den anden uge. Generelt afstemmes reservationerne og tildelingerne, men de er forskellige fra den ene uge til den næste.

Når du får vist tiden på højere niveauer, har fanen **Afstemning** en indikator, der giver dig besked om, at der er forskelle på lavere niveauer. Dobbeltklik på en celle for at zoome ind og se forskellen. Du kan derefter højreklikke for at zoome ud. Hvis du vælger en ressource og derefter vælger **Næste difference** på værktøjslinjen for gitteret, kan du gå til den næste forskel mellem reservationer og tildelinger for den pågældende ressource. Vælg **Forrige difference** for at gå tilbage. Du kan også slå differenceindikatoren og funktionsmåden for navigation fra under **Indstillinger**.

Hvis du har opgavetildelinger for en ressource men ingen reservationer, skal du i formularen **Projekter** på fanen **Afstemning** vælge den manglende reservation og derefter vælge **Forlæng reservation**. Dialogboksen **Udvid reservation** vises og angiver den reservation, der skal bruges for at løse manglen på ressource. Dialogboksen viser også ressourcens eksisterende reservationer på tværs af alle projekter eller andre objekter, der kan planlægges. Hvis du vælger **OK** for at oprette reservationen for ressourcen, uanset den pågældende ressources tilgængelighed, kan det medføre overreservation.

Projektlederen eller ressourceadministratoren kan derefter bruge planlægningsområdet til at administrere de situationer, hvor en ressource overreserveres i forhold til dens kapacitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]