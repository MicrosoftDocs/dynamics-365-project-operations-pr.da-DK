---
title: Opgradering fra Project Service Automation til Project Operations
description: Denne artikel indeholder en oversigt over processen for opgradering fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686968"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Opgradering fra Project Service Automation til Project Operations

Det glæder os at kunne annoncere den anden af tre faser i opgraderingen fra Microsoft Dynamics 365 Project Service Automation til Microsoft Dynamics 365 Project Operations. Denne artikel giver et overblik over de kunder, der indleder denne spændende rejse. 

Leveringsprogrammet til opgraderingen opdeles i tre faser.

| Levering af opgradering | Fase 1 (januar 2022) | Fase 2 (november 2022) | Fase 3 (april-bølge 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Ingen afhængighed af arbejdsopgavehierarkiets (WBS) for projekter | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| En WBS inden for de grænser for Project Operations, der understøttes i øjeblikket | | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| En WBS uden for de grænser for Project Operations, der understøttes i øjeblikket, herunder understøttelse af Project Desktop Client | | | :heavy_kontrol_mærke: |

## <a name="upgrade-process-features"></a>Opgradering af procesfunktioner 

Som en del af opgraderingsprocessen har vi tilføjet opgraderingslogfiler til oversigten over webstedet, så administratorer lettere kan diagnosticere fejl. Ud over den nye brugergrænseflade tilføjes der nye valideringsregler, som skal sikre dataintegritet efter en opgradering. Følgende valideringer tilføjes til opgraderingsprocessen.

| Valideringer | Fase 1 (januar 2022) | Fase 2 (november 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS valideres i forhold til almindelige brud på dataintegritet (f.eks. ressourcetildelinger, der er knyttet til den samme overordnede opgave, men har forskellige overordnede projekter). | | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| WBS valideres i forhold til [de kendte grænser for Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |
| WBS valideres i forhold til de kendte grænser for Project Desktop Client. | |  | :heavy_kontrol_mærke: |
| Ressourcer og projektkalendere, der kan reserveres, evalueres i forhold til almindelige undtagelser fra inkompatibel kalenderregel. | | :heavy_kontrol_mærke: | :heavy_kontrol_mærke: |

I fase 2 får kunder, der opgraderer til Project Operations, opgraderet deres eksisterende projekter til en skrivebeskyttet oplevelse i forbindelse med projektplanlægning. I denne skrivebeskyttede oplevelse er den fulde WBS synlig i sporingsgitteret. Hvis du vil redigere WBS'en, kan projektledere vælge [**Konverter**](/PSA-Upgrade-Project-Conversion.md) på hovedsiden for Projekter. En baggrundsproces opdaterer derefter projektet, så det understøtter den nye projektplanlægningsoplevelse fra Project for the Web. Denne fase er hensigtsmæssig for kunder, der har projekter, som falder ind under [de kendte grænser for Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

I fase 3 tilføjes understøttelse af Project Desktop Client til stationære computere til fordel for kunder, der fortsat vil redigere deres projekter fra programmet. Men hvis eksisterende projekter konverteres til det nye Project for the Web-oplevelsen, deaktiveres adgangen til tilføjelsesprogrammet for hvert konverteret projekt.

## <a name="prerequisites"></a>Forudsætninger

En kunde skal opfylde følgende kriterier for at være berettiget til fase 1-opgraderingen:

- Destinationsmiljøet må ikke indeholde poster i objektet **msdyn_projecttask**.
- Gyldige Project Operations-licenser skal tildeles til alle aktive brugere. 
- Du skal validere opgraderingsprocessen i mindst ét ikke-produktionsmiljø, som indeholder et repræsentativt datasæt, der stemmer overens med produktionsdata.
- Destinationsmiljøet skal opdateres til Project Service Automation opdateringsudgivelse 37 (V3.10.58.120) eller nyere.

En kunde skal opfylde følgende kriterier for at være berettiget til fase 2-opgraderingen:

- Gyldige Project Operations-licenser skal tildeles til alle aktive brugere. 
- Du skal validere opgraderingsprocessen i mindst ét ikke-produktionsmiljø, som indeholder et repræsentativt datasæt, der stemmer overens med produktionsdata.
- Destinationsmiljøet skal opdateres til Project Service Automation opdateringsudgivelse 37 (V3.10.58.120) eller nyere.
- Miljøer, der indeholder opgaver (msdyn_projecttask), understøttes kun, hvis det samlede antal opgaver pr. projekt er 500 eller mindre.

Forudsætningerne for fase 3 opdateres efterhånden, som datoen for generel tilgængelighed nærmer sig.

## <a name="licensing"></a>Licensering

Hvis du har aktive licenser til Project Service Automation, kan du installere og bruge Project Operations, som omfatter alle funktionerne i Project Service Automation og meget mere. Du kan teste funktionerne i Project Operations i et separat miljø, mens du fortsætter med at bruge Project Service Automation i produktionen. Når dine licenser til Project Service Automation udløber, skal du overgå til Project Operations. Når du planlægger overgangen, skal du tage højde for, at licensen til Project Operations ikke inkluderer en licens til Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Test og refaktorering af tilpasninger

Som udgangspunkt skal du importere alle tilpasninger i et rent miljø for Project Operations (Lite) for at bekræfte, at importen er vellykket, og at virksomhedens drift fungerer som forventet.

Her er nogle ting, du skal holde øje med:

- Importen kan mislykkes på grund af manglende afhængigheder. Tilpasningerne refererer med andre ord til felter eller andre komponenter, der er blevet fjernet i Project Operations. I dette tilfælde skal du fjerne disse afhængigheder fra udviklingsmiljøet.
- Hvis de ikke-administrerede og administrerede løsninger indeholder komponenter, der ikke er tilpasset, skal du fjerne disse komponenter fra løsningen. Hvis du f.eks. tilpasser objektet **Projekt**, skal du kun tilføje objektoverskriften til løsningen. Tilføj ikke alle felterne. Hvis du tidligere har tilføjet alle underkomponenter, skal du måske oprette en ny løsning manuelt og tilføje relevante komponenter til den.
- Formularer og visninger vises muligvis ikke som forventede. Hvis du har tilpasset en af standardformularerne eller -visningerne, kan tilpasningerne i nogle tilfælde forhindre, at nye opdateringer i Project Operations træder i kraft. Hvis du vil identificere disse problemer, anbefales det, at du udfører en oprydning sideløbende med en ren installation af Project Operations og en installation af Project Operations, der omfatter tilpasningerne. Sammenlign de mest almindeligt brugte formularer i virksomheden for at bekræfte, at din version af formularen stadig giver mening, og at der ikke mangler noget i den rene version af formularen. Du kan udføre den samme type sideløbende gennemgang for visninger, du har tilpasset.
- Forretningslogik kan mislykkes under kørsel. Da referencer til felter i plug-ins ikke valideres på tidspunktet for importen, kan forretningslogikken mislykkes på grund af referencer til felter, der ikke længere findes, og du modtager måske en fejlmeddelelse, der ligner følgende eksempel: "Objektet 'Projekt' indeholder ikke attributten med navn = 'msdyn_plannedhours' og NameMapping = 'Logisk'." I dette tilfælde skal du redigere tilpasningerne, så de bruger de nye felter. Hvis du bruger automatisk genererede proxyklasser og stærke typereferencer i plug-in-logikken, bør du overveje at genoprette disse proxyer fra en ren installation. På denne måde kan du let identificere alle de steder, hvor plug-ins er afhængige af udfasede felter.

Når du har opdateret tilpasningerne for at importere Project Operations rent, skal du gå videre til de næste trin.

## <a name="end-to-end-testing-in-development-environments"></a>Komplet test i udviklingsmiljøer

### <a name="initiate-upgrade"></a>Start opgradering 

1. Find og vælg dit miljø i Power Platform Administration. Find og vælg derefter **Dynamics 365 Project Operations** i programmerne.
2. Vælg **Installer** for at starte opgraderingen. Power Platform Administration præsenterer denne installation som en ny installation. Men tilstedeværelsen af en tidligere version af Project Service Automation registreres, og den eksisterende installation opgraderes.

    Når opgraderingen er fuldført, bør miljøet vise, at Project Operations er installeret, og at Project Service Automation ikke er installeret.

    Opgraderingen kan tage flere timer, afhængigt af mængden af data i miljøet. Det kerneteam, der administrerer opgraderingen, skal planlægge og køre opgraderingen uden for arbejdstiden. I visse tilfælde, hvis datamængden er stor, skal opgraderingen køres i løbet af weekenderne. Beslutningen om planlægning skal være baseret på testresultaterne i lavere miljøer.

3. Opgrader brugerdefinerede løsninger efter behov. Du skal nu udrulle eventuelle ændringer, som du har foretaget af tilpasningerne i afsnittet [Test og refaktorering af tilpasninger](#testing-and-refactoring-customizations) i denne artikel.
4. Gå til **Indstillinger** \> **Løsninger**, og vælg at afinstallere løsningen **Udfasede komponenter til Project Operations**.

    Denne løsning er en midlertidig løsning, som indeholder den eksisterende datamodel og komponenter, der findes under opgraderingen. Ved at fjerne denne løsning fjerner du alle de felter og komponenter, der ikke længere bruges. På denne måde kan du forenkle brugergrænsefladen og gøre integration og udvidelse nemmere.
    
### <a name="upgrade-to-project-operations-lite"></a>Opgrader til Project Operations Lite

I følgende trin beskrives opgraderingsprocessen og den tilknyttede fejllogføring:

1. **Kontrol af PSA-version:** Hvis du vil installere Project Operations, skal du have V3.10.58.120 eller nyere.
1. **Forudvalidering:** Når en administrator starter en opgradering, kører systemet en forudvalideringshandling for hvert enkelt objekt, der er kerne i project operations-løsningen. I dette trin kontrolleres, at alle objekters referencer er gyldige, og det sikrer, at data, der er relateret til WBS, er inden for de publicerede grænser for Project for the Web.
1. **Opgradering af metadata:** Efter en vellykket forudvalidering starter systemet ændringer af skemaet og opretter en frabedt komponentløsning. Du kan fjerne denne frabedte løsning, når du har fuldført alle nødvendige tilpasninger igen. Dette trin er en del af opgraderingsprocessen, som kan tage op til fire timer.
1. **Dataopgradering:** Når alle påkrævede skemaændringer er fuldført i opgraderingstrinnet til metadata, overføres dataene til det nye skema, og eventuel påkrævet standardindstilling og genberegning foretages.
1. **Opdatering af projektplanprogrammet:** Efter en vellykket dataopgradering er fanen **Planlæg** på hovedsiden navnmærket **Opgaver**. Når en bruger vælger denne fane efter opgraderingen, dirigeres brugeren til at navigere til sporingsgitteret for at få vist en skrivebeskyttet version af WBS. Hvis de vil redigere WBS, skal de starte [konverteringsprocessen for planen](/PSA-Upgrade-Project-Conversion.md). Alle projekter uden en eksisterende WBS kan bruge den nye planlægningsoplevelse direkte uden konvertering.
 
### <a name="validate-common-scenarios"></a>Valider almindelige scenarier

Når du validerer specifikke tilpasninger, anbefales det, at du også gennemgår de forretningsprocesser, der understøttes på tværs af programmerne. Disse forretningsprocesser omfatter, men er ikke begrænset til, oprettelse af salgsobjekter, f.eks. tilbud og kontrakter, og oprettelse af projekter, der omfatter WBS'er og godkendelse af faktiske værdier.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Store forskelle mellem Project Service Automation og Project Operations

Dette afsnit indeholder en oversigt over de store forskelle, som du kan forvente mellem Project Service Automation og Project Operations.

### <a name="project-planning"></a>Projektplanlægning

Projektplanlægningsfunktionerne i Project Operations er ikke længere afhængig af en kombinationslogik på klientsiden og en serverlogik. Project Operations bruger i stedet Project for the Web som planlægningsprogram. Denne ændring i planlægningsfunktionerne gør det muligt at få adskillige nye funktioner, f.eks. visninger af bestyrelse og Gantt, ressourcebaseret planlægning, [kontrollistepunkter for opgaver](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) og projektplanlægningstilstande. De nye planlægningsfunktioner understøttes også af et omfattende sæt nye [programmeringsgrænseflader (API'er)](../project-management/schedule-api-preview.md). Disse API'er med til at sikre, at ingen programmeringshandling til oprettelse, opdatering eller sletning af et objekt i WBS beskadiger de beregnede felter i tidsplanen.

### <a name="billing-and-pricing"></a>Fakturering og prisfastsættelse

Som en del af det fortsatte arbejde med Project Operations findes der flere nye funktioner inden for fakturering og fastsættelse. Her er nogle eksempler:

- [Registrering af materialeforbrug på projekter og projektopgaver](../material/material-usage-log.md)
- [Administration af underentrepriser](../pro/subcontracting/managing-subcontracts-overview.md)
- [Forskudskontrakter og kontrakter baseret på forskudshonorar](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontraktstatus, som ikke må overskrides, og valideringer](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Opgavebaseret fakturering

### <a name="resource-management"></a>Ressourcestyring

Project Operations yder valgfri support til Universal Resource Scheduling (URS)-tavlen og planlægningsassistenten. Denne nye oplevelse bliver obligatorisk i april 2023-runden.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Hvilke udrulningstyper understøttes i øjeblikket i forbindelse med opgradering?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations lille udrulning                        | Understøttet               |
| Projektstyring og regnskab i Dynamics 365 Finance | Project Operations lille udrulning                        | Understøttes ikke i øjeblikket |
| Projektstyring og regnskab i Finance              | Project Operations for ressource/ikke-lagerscenarier     | Understøttes ikke i øjeblikket |
| Project Service Automation 3.x                         | Project Operations for ressource/ikke-lagerscenarier     | Understøttes ikke i øjeblikket |
| Project for the Web (forældet miljø)            | Project Operations lille udrulning                        | Understøttes ikke i øjeblikket |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Hvordan installerer jeg Project Operations, før opgraderingsværktøjet bliver tilgængeligt?

Der findes to muligheder for at installere Project Operations, før opgraderingsværktøjet er tilgængeligt:

- Klargør et nyt miljø.
- Udrul Project Operations separat i alle salgsorganisationer, hvor Project Service Automation ikke findes.

Hvis Project Service Automation installeres i en organisation, men ikke bruges, kan programmet afinstalleres. Når du har fjernet Project Service Automation fuldstændigt, kan Project Operations installeres på den samme organisation.
