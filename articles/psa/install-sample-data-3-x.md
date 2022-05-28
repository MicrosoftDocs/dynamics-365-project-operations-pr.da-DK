---
title: Installation af eksempeldata
description: Dette emne indeholder oplysninger om installation af eksempeldata i Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 952f3c3c037bb8459bdd1400288c4ea8604ce282
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581829"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Installation af eksempeldata til programmet Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

For at hjælpe dig med at udvikle dine egne demonstrationsmiljøer leverer Microsoft eksempeldata, som du kan downloade, og som præsenterer funktionerne i dine apps. Der findes to typer eksempeldatapakker:
- reference/installationsdata
- demonstrationsdata (reference/installations- og transaktionsdata som arbejdsordrer og projekter)

Pakkerne med eksempeldata til **reference** kan hentes i tre separate pakker, så du kan vælge kun at installere data for Project Service eller kun for Field Service, eller du kan installere eksempeldata for begge programmer på samme tid.

Der er følgende eksempelinstallations-/referencedatapakker:

- [**V902PSMasterData** - Kun Project Service version 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Kun Field Service version 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x og Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Den nyeste **demo** datapakke er:

 - [**FPSDemoData** - Field Service 8.x og Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Installationsvejledningen har lidt forskellige afsnit om brugeroprettelse og -konfiguration, men resten er det samme som i det forrige [**blogindlæg**](https://aka.ms/fpsdemodatablog). Denne pakke indeholder et reduceret demonstrationsdatasæt og tager ca. 3 timer at installere.

Disse eksempeldatapakker er kun tilgængelige på engelsk.

> [!IMPORTANT]
> **Det er ikke muligt at afinstallere eksempeldataene.** Derfor skal du kun installere disse pakker på demonstrations-, evaluerings-, øvelses- eller testsystemer. Bemærk også, at du ikke kan installere en individuel pakke og derefter installere den anden individuelle pakke. (Med andre ord kan du ikke installere **FSMasterData** efterfulgt af **PSMasterData** eller omvendt). Hvis du tror, at du kommer til at mangle eksempeldata til begge programmer på et senere tidspunkt, skal du installere **v902FPSMasterData**-pakken.

Når du installerer en eksempeldatapakke, udfører installationsprocessen følgende handlinger:

- Opretter eller angiver standardparametre til brug af Project Service, Field Service eller begge programmer (hvis relevant).

- Importerer eksempeldata til programmerne, f.eks. reserverbare ressourcer, programspecifikke roller, salgs- og kostprislister, organisationsenheder, salgsprocesposter og andre objekter, der viser vigtige egenskaber.  

Med **demonstrationsdata**-pakken får du ovennævnte og yderligere transaktionsdata som f.eks. arbejdsordrer og projekter.

Vil du vide, hvilke funktioner du kan bruge i demoudgaver med eksempeldataene? Se det fiktive Fabrikam Robotics-scenario nedenfor i [Tekniske bemærkninger](#technical-notes).

Hvis du har spørgsmål om installation af disse data eksempelpakker, kan du [sende en e-mail til fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Krav

Installationsprotokollen antager følgende om din målforekomst (organisation):

- Udgangssproget er engelsk, og grundvalutaen er amerikanske dollar (USD, $).

- Organisationen har på forhånd ingen Project Service- eller Field Service-data eller har kun barebone-standarddata, der følger med enhver ny organisation.

- Den korrekte version af virksomhedsprogrammet er allerede installeret:
       
    - **For FPSDemoData eller v902FPSMasterData:** Organisationen har Field Service version 8.x og Project Service version 3.x installeret.

    - **For v902PSMasterData:** Organisationen har Project Service version 3.x installeret.

    - **For v902FSMasterData:** Organisationen har Field Service version 8.x installeret.

> [!NOTE]
> Hvis du har brug for at installere eksempeldataene oven på en eksisterende Project Service- eller Field Service-prøveversion eller -demomiljø, der allerede har data (anbefales ikke), skal du deaktivere de forhåndskontroller af sikkerheden, der udføres af installationsprogrammet. Du kan finde flere oplysninger under Tekniske bemærkninger nedenfor.

## <a name="prepare-for-installation"></a>Gøre klar til installation

Du skal køre installationsprogrammet på en computer med en nyere version af Windows (Windows 10 foretrækkes).

Du skal sørge for, at computeren fortsat kan have forbindelse til et netværk, og at installationen kan køre i op til **1 time** for **installations-/referencedata**. (Normalt tager installationen ca. 30 minutter for **FPSMasterData**, som indeholder eksempeldata til begge programmer). For **FPSDemoData** tager installationen omkring **3 timer**.

Computerens pauseskærm skal være slået fra. I modsat fald kan sessionslegitimationsoplysningerne for installationen gå tabt, når pauseskærmen aktiveres (medmindre du holder sessionen aktiv under hele forløbet).

> [!div class="mx-imgBorder"]
> ![Skærmbillede af indstillinger for pauseskærm med pauseskærmen slået fra.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Hente og pakke ud

Installationsprogrammet til Project Service- og Field Service-eksempeldata distribueres som en selvudpakkende eksekverbar fil. Filnavnene kan variere afhængigt af pakken med eksempeldata, men ellers er trinnene de samme, uanset hvilken pakke du installerer.

Når du har hentet en pakke, skal du køre exe-filen og derefter acceptere vilkår og betingelser for at pakke den komprimerede zip-fil ud. Derefter skal du pakke indholdet af den pågældende fil ud i en mappe på computeren.

Afhængigt af operativsystemet og sikkerhedsindstillingerne skal du evt. udføre følgende trin efter udpakningen af zip-filen:

1. Find og højreklik på filen **FPSDemoData.dll** i mappen **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Vælg **Fjern blokering**.

3. Vælg **Anvend**.

4. Vælg **OK**.


## <a name="create-or-configure-users"></a>Oprette eller konfigurere brugere

Pakken **FPSDemoData** kræver seks brugere, mens **FPSMasterData**-pakker kræver én bruger. Referer til den rigtige for eksempeldatapakken.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Oprette eller konfigurere brugere – installations-/referencedatapakker

Pakken **FPSMasterData** er beregnet til installation med én bruger, der hedder Spencer Low, med de indstillinger, der er beskrevet her. For at installere pakken korrekt skal du oprette (eller midlertidigt omdøbe) brugere i dit miljø, så de passer til den indgående konfiguration for eksempeldataene.

Når du vil oprette eller konfigurere brugere, skal du gå til **Indstillinger** > **Sikkerhed** > **Brugere** og gøre følgende:

1. Angiv UserFullname = "Spencer Low" med brugernavnet "spencerl" (**små bogstaver**) til rollerne Projektleder og Praksisleder.

2. Vælg brugeren **Spencer Low**, og vælg derefter **Administrer roller**. Find og vælg rollen **Systemadministrator**, og vælg derefter **OK** for at tildele fulde administratorrettigheder til Spencer Low. Dette trin er nødvendigt for at sikre, at eksempelposter oprettes med det korrekte brugerejerskab og derfor udfylder visninger korrekt.

3. Fra den hentede pakke skal du opdatere en datatilknytningsfil med e-mailadresser for standardbrugerkonteksten. Det gør du ved at åbne **PkgFolder** og derefter finde og åbne filen **ImportUserMapFile.xml** i Notesblok (eller Visual Studio eller en anden XML-editor). Indstil feltet **DefaultUserToMapTo =** til e-mailadresse for brugeren Spencer Low.

4. Hvis du ikke bruger Spencer Low med brugernavnet **spencerl**, skal du opdatere endnu en fil. Åbn filen **DemoDataPreImportConfig.xml**, og find derefter mærket **userstocreateandconfigure**. Opdater **\<login\>**-mærket med brugernavnet på din Spencer Low-bruger. Du kan finde flere oplysninger under [Tekniske bemærkninger](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Oprette eller konfigurere brugere - demodatapakke

Demodatapakken kræver seks brugere. For at pakken skal blive installeret korrekt, skal du gøre følgende:

 1. Oprette eller midlertidigt omdøbe eksisterende brugere, så de svarer til konfigurationen af indgående eksempeldata, ved at gå til **Indstillinger** > **Sikkerhed** > **Brugere**.
 
    Disse roller er kun nødvendige i forbindelse med personligt baserede demoer.  
    - Brugers Fullname="David So" som servicetekniker   
    - Brugers Fullname="Jamie Reding" som koordinator af kundeservice og teknisk service   
    - Brugers Fullname="Molly Clark" som regnskabschef   
    - Brugers Fullname= "Spencer Low" som praksis- og projektleder  
    - Brugers Fullname="Veronica Quek" som teammedlem   
    - Brugers Fullname="William Contoso"
  
2. Hvad angår import af demonstrationsdata, skal du tildele de seks brugere over Administrator-rollen, så eksempelposterne importeres korrekt. 

3. Åbn **PkgFolder**, og find og åbn derefter **ImportUserMapFile.xml**. Opdater **New=** felterne til mailadresserne på de tilsvarende brugere i systemet.

   > [!div class="mx-imgBorder"]
   > ![Skærmbillede af UserMapFile.](media/sample-data-7.png)

4. Hvis "Spencer Low" full name-brugeren har et andet bruger-id end **"spencerl"**, skal du opdatere endnu en fil. Åbn **DemoDataPreImportConfig.xml**, og find mærket **userstocreateandconfigure**. Opdater **\<login\>**-mærket med loginId'et (der skelnes mellem store og små bogstaver). 

5. Den første brugers kalender (i mærket **userstocreateandconfigure**) bruges til at angive arbejdstimerne for alle reserverbare ressourcer ved import af demonstrationsdata. Naviger til **Indstillinger** > **Sikkerhed** > **Brugere**, søge efter brugeren "Spencer Low", og åbn indstillingen "Arbejdstimer". Rediger de eksisterende arbejdstimer ved at vælge indstillingen **Hele den gentagne ugeplan fra start til slut**. Sørg for, at **Arbejdstimer er indstillet til 8 AM - 5 PM (9 timer), mandag til fredag og med tidszonen indstillet til Pacific Time (USA og Canada)**. Dette er nødvendigt for at sikre, at området med projektplanen og tidsplanen vises som forventet.

**Anbefaling:** Overvej at oprette en sikkerhedskopi af din organisation nu, som du kan bruge, hvis du får brug for at vende tilbage til udgangspunktet, hvis noget går galt under installationen af eksempeldataene. Du kan finde flere oplysninger under [Sikkerhedskopiering og gendannelse af forekomster](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Køre Package Deployer

1. Find og kør **PackageDeployer.exe** i mappen **v902FPSMasterData** ELLER mappen **PackageDeployer_FPSDemoData**.

2. Acceptér vilkårene og betingelserne.

3. I det næste vindue:

   a. Vælg installationstype **Office 365**.

   b. Brug brugeren og adgangskoden for den systemadministrator, der er konfigureret i "Oprette eller konfigurere brugere" ("Spencer Low" med brugernavnet "spencerl").

   c. Kontroller, at **Vis en liste over tilgængelige organisationer** er valgt.

      > [!div class="mx-imgBorder"]
      > ![Skærmbillede af Package Deployer-vinduet med valg af "Viser listen over tilgængelige organisationer"](media/sample-data-2.png)

4. Vælg den organisation, hvor du vil installere eksempeldataene.

5. Vælg **Næste**, indtil du ser dialogen **Opsætning af demodata**.

   > [!div class="mx-imgBorder"]
   > ![Skærmbillede af vinduet med status for installation af demodata.](media/sample-data-3.png)

6. Før du fortsætter, skal du lægge mærke til, at installation af eksempeldata kan tage op til én time (normalt ~ 10 minutter). Du skal først sikre, at computeren forbliver tændt og har forbindelse til et netværk under hele installationen, og, at din session forbliver aktiv.   

7. Når du er færdig, skal du klikke på **Næste** for at starte installationsprocessen for eksempeldataene. Når eksempeldataene er indlæst, skal du klikke på **Udfør**.

## <a name="verify-the-sample-data-installation"></a>Kontrollere installationen af eksempeldataene

For en sikkerheds skyld skal du kontrollere, at antallet af poster og typer af objekter, der vises i det fiktive Fabrikam Robotics-scenario, vises som forventet.

Når eksempeldataene er helt indlæst, skal du logge på som brugeren Spencer Low og kontrollere følgende:

- Hvis programmet Project Service er installeret, skal du gå til **Project Service** > **Indstillinger** > **Prislister**. Bekræft, at faktureringssatser og omkostningssatser findes med den rette valuta for hvert land/område i datasættet.

- Hvis programmet Project Service er installeret, skal du gå til **Universal Resource Scheduling** > **Indstillinger** > **Afdelinger**. Bekræft, at en kostprisliste med den rette valuta er knyttet til hver organisationsenhed (undtagen by-poster). Hvis der mangler nogen, kan du søge efter og tilknytte den korrekte kostprisliste.

- Hvis programmet Field Service er installeret, skal du gå til **Project Service** > **Indstillinger** > **Prislister**. Bekræft, der er angivet fakturasatser og omkostningssatser. Gå til **Field Service** > **Indstillinger** > **Prislister**, og se, at fakturasatser og omkostningssatser er angivet, med den rette valuta for hvert land/område, i datasættet.

  > [!div class="mx-imgBorder"]
  > ![Skærmbillede af aktive prislister.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Skærmbillede af aktive organisationsenheder.](media/sample-data-5.png)

## <a name="technical-notes"></a>Tekniske bemærkninger

Se flere tekniske oplysninger om installationen af disse data nedenfor.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Installation af eksempeldata oven på eksisterende data (anbefales ikke)

Hvis du har brug for at installere eksempeldata oven på en eksisterende Field Service eller Project Service-prøveversion eller -demomiljø, der allerede har data, skal du deaktivere de forhåndskontroller af sikkerheden, der udføres af installationsprogrammet.

For at gøre det skal du gå til mappen **PkgFolder** for at søge efter og åbne filen **DemoDataPreImportConfig.xml** med Notesblok (eller en anden XML-editor).

Find følgende værdi, og rediger derefter indstillingen fra sand til falsk:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Denne ændring medfører, at installationsprogrammet omgår nogle vigtige sikkerhedskontroller, herunder:

- Bekræfter, at der findes mere end én aktiv **Afdeling**-post og omdøber den derefter til **Fabrikam USA**.

- Bekræfter, at der ikke findes mere end én aktiv **Arbejdsskabelon**-post.

- Bekræfter, at der ikke findes mere end én aktiv **Projektparameter**-post og omdøber derefter posten til **Parametre**.

### <a name="configuration-components"></a>Konfigurationskomponenter

Der findes en række andre konfigurationskomponenter i denne konfigurationsfil før import. Følgende komponenter kan bruges af tekniske brugere:

- **\<RequiredSolutions\>** angiver nødvendige løsningsinstallationer og versionsnumre.

- **\<InstallSampleData\>** styrer, om standardeksempeldata til appsene er installeret.

    - false - undlader at foretage installationen af disse indbyggede data (som kan fjernes)

    - true - installerer de indbyggede data, der svarer til installationen af FS- og PSA-eksempeldataene

- **\<PreImportDataCollection\>** angiver datatilknytninger i fil, der ikke kan redigeres, og de tilknyttede poster, der skal importeres forud for installationen af hovedeksempeldataene.

- **\<EntitiesToEnableScheduling\>** angiver, hvilke objekter der skal aktiveres til reservation i Microsoft Dynamics Scheduling (også kaldet Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** angiver reserverbare ressourcer, der bliver oprettet (hvis de ikke allerede findes), før importen af eksempeldata køres. Vær opmærksom på, at kildesystemets eksempeldata for Reserverbare ressource stemmer overens med målsystemet Reserverbare ressource-poster på FullName og logon for de enkelte ressourcer. Det er derfor IKKE muligt at ændre navnene i denne forudkonfigurationsfil, medmindre du først importerer eksempeldata til et målsystem og bruger disse navne og derefter omdøber den Reserverbare ressource til det ønskede navn, som er angivet sammen med aktiverede brugerposter, og derefter eksporterer dataene igen, så de kan importeres til det endelige destinationssystem (opdatering af Gamle og Ny poster for **ImportUserMapFile.xml** tilsvarende).

- **\<PluginsToDisable\>** angiver meget dedikeret linjeelementtilføjelsesprogrammer, der skal deaktiveres under importen af eksempeldataene og derefter aktiveres igen bagefter.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fiktivt Fabrikam Robotics-scenario

Field Service- og Project Service-eksempelreferencedatapakker installerer **Fabrikam Manufacturing Master Data (v3.0.0.0)-løsningen** sammen med ca. 4.000 poster og ca. 40 forskellige objekter. De separat eksempeldatapakker til Field Service eller Project Service indeholder et delsæt af **v902FPSMasterData**-eksempeldataene for det pågældende program. **Demonstrationsdata** pakken installerer **Fabrikam Manufacturing Demo Data (v3.0.0.7)-løsningen** med ca. 22.000 poster på tværs af 148 enheder.

Det fiktive firma, Fabrikam Robotics, er forhandler af assemblylinjerobotter til elektroniske enheder og er kendt for deres produktkvalitet, fornyelse og solide kundeservice, herunder planlægning af installation, implementering og løbende vedligeholdelsestjenester. Fabrikam har hovedkontor i USA (Fabrikam US) og har projektbaserede serviceoperationer i Frankrig, Indien, Østrig og Schweiz.

Field Service-handlinger er centreret i USA for det meste i området omkring Seattle. Virksomheden har fokus på at udnytte Tingenes internet-forbindelser (loT) til at overvåge ydeevnen af kundeaktiver og levere stadigt mere proaktive tjenester hos virksomheden.

En detaljeret oversigt over eksempeldataene er som følger:

- Almindelige eksempeldataelementer (inkluderet for begge programmer)

    - 1 bruger

    - 71 firmaer

    - 137 kontakter

    - Forskellige transaktionstyper og -kategorier

    - 50 produkter med 1 produktprisliste

    - 14 pris/kostlister

    - 31 egenskaber (ressourcernes kvalifikationer) i 2 klassificeringsmodeller med 3 niveauer (klassificeringsværdier)

- Project Service

    - 8 afdelinger

    - 6 rollespecifikke niveauer for tidsforbrug

    - 2,8 k + rolleprisspecifikationer

- Field Service

    - 4 distrikter

    - 5 arbejdsordretyper

    - 22 kundeaktiver

    - 9 hændelsestyper med et udvalg af tilknyttede ressourceegenskaber (9), services (13) og serviceopgaver (13)
   
Pakken med **Demonstrationsdata** installerer ca. 179 arbejdsordrer, 12 projekter og tilknyttede transaktionsdata. 

### <a name="change-the-work-hours-for-sample-resources"></a>Ændre arbejdstimerne for eksempelressourcer

Som standard har alle reserverbare ressourcer en 24 timers kalender.

Hvis du vil ændre arbejdstimerne for reserverbare eksempelressourcer, skal du gå til **Universal Resource Scheduling** > **Planlægning** > **Ressourcer**.

Vælg en bruger (f.eks. Spencer Low), og skift Spencers arbejdstimer til de timer, du vil anvende til flere brugere. Gå til **Universal Resource Scheduling** > **Indstillinger** > **Arbejdstidsskabeloner**, og rediger posten **Standardarbejdssskabelon**. I feltet **Skabelonressource** skal du vælge en bruger med arbejdstimer, som du vil anvende på andre ressourcer. Gå til **Universal Resource Scheduling** > **Planlægning** > **Ressourcer** > **Aktive reserverbare ressourcer**. Vælg de ressourcer, du vil ændre, og vælg derefter **Angiv kalender**. På rullelisten **Arbejdsskabelon** skal du vælge skabelonen **Standardarbejdstime** eller en anden skabelon med den korrekte skabelonressource. Når du skifter til planlægningsområdet, bør du kunne se ressourcerne, der nu har opdaterede arbejdstimer.

> [!div class="mx-imgBorder"]
> ![Skærmbillede af aktive reserverbare ressourcer.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]