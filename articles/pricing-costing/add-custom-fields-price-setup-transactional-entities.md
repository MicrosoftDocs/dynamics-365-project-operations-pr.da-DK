---
title: Tilføj krævede brugerdefinerede felter til prisopsætning og transaktionsobjekter
description: Dette emne indeholder oplysninger om, hvordan du tilføjer nødvendige brugerdefinerede feltreferencer til objekter og til formularer og visninger.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c324e0e8797d0b6d3a06ffc2a40b787a475c49b5
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590894"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Tilføj krævede brugerdefinerede felter til prisopsætning og transaktionsobjekter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I dette emne antages det, at du har fuldført procedurerne i emnet, [Opret brugerdefinerede felter og objekter, som skal anvendes som prisfastsættelsesdimensioner](create-custom-fields-entities-pricing-dimensions.md). Hvis du ikke har fuldført procedurerne, skal du gå tilbage og fuldføre dem og derefter vende tilbage til dette emne. 

I dette emne viser procedurerne dig, hvordan du kan føje de påkrævede brugerdefinerede feltreferencer til objekter og til brugergrænsefladeelementerne (UI), f.eks. formularer og visninger.

## <a name="add-custom-pricing-dimension-fields"></a>Tilføje brugerdefinerede felter for prisdimensioner 
Når der er oprettet brugerdefinerede felter og objekter, er det næste trin at gøre opsætningen af priser og transaktionsobjekter opmærksom på eventuelle brugerdefinerede objekter eller grupper ved at oprette referencefelter. Afhængigt af, om dine prisdimensioner indeholder dimensioner for grupperet indstilling objektdimensioner eller begge, skal du kun følge trinene i **Brugertilpassede prisdimensioner baseret på grupperet indstilling** eller **Brugerdefinerede prisdimensioner baseret på objekter** eller begge.

### <a name="option-set-based-custom-pricing-dimensions"></a>Brugerdefinerede prisdimensioner baseret på grupperet indstilling
Når en brugerdefineret prisdimension er baseret på grupperet indstilling, skal du tilføje den som et felt til nøgleobjekter. I den følgende procedure bruges **Arbejdssted for ressource** og **Arbejdstimer for ressource** som prisdimensioner baseret på grupperet indstilling. Disse skal først tilføjes som felter til prisobjekterne **rollepris,** og **rolleprisavance**.

1. Vælg **Indstillinger** > **Løsninger** og dobbeltklik på **\<your organization name> prisfastsættelsesdimensioner** i Project Operations. 
2. Vælg **Objekter > Rollepris** i den venstre navigationsrude i løsningsoversigten.
3. Udvid objeket **Rollepris**, og vælg **Felter**.
4. Vælg **Ny** for at oprette et nyt felt med navnet **Arbejdssted for ressource**, og vælg **Grupperet indstilling** som felttype. 
5. Vælg **Brug en eksisterende grupperet indstilling**, vælg den grupperede indstilling **Arbejdssted for ressource**, og vælg derefter **Gem**.
6. Gentag trin 1-5 for at føje dette felt til objektet **Rolleprisavance**. 
7. Gentag trin 1-5 for den grupperede indstilling **Arbejdstimer for ressource**.

> [!IMPORTANT]
> Når du føjer et felt til mere end ét objekt, skal du bruge samme feltnavn på tværs af alle objekterne. 

> ![Føje arbejdssted for ressource til rollepris](media/RWL-Field.png)

I salgs- og estimatfaserne for et projekt bruges estimater af den arbejdsindsats, der kræves til at udføre **lokalt** arbejde og arbejde **på stedet** inden for **Ordinær arbejdstid** og **Overarbejde** til at estimere værdien af tilbuddet/projektet. Felterne **Arbejdssted for ressource** og **Arbejdstid for ressource** føjes til estimatobjekterne **Tilbudslinjedetaljer**, **Kontraktlinjedetaljer**, **Medlem af projektteam** og **Estimatlinje**.

1. Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner** i Project Operations. 
2. Vælg **Objekter > Tilbudslinjedetaljer** i den venstre navigationsrude i løsningsoversigten.
3. Udvid objektet **Tilbudslinjedetaljer**, og vælg **Felter**.
4. Vælg **Ny** for at oprette et nyt felt med navnet **Arbejdssted for ressource**, og vælg felttypen **Grupperet indstilling**. 
5. Vælg **Brug en eksisterende grupperet indstilling** og **Arbejdssted for ressource**, og vælg derefter **Gem**.
6. Gentag trin 1-5 for at føje dette felt til objekterne **Projektkontraktlinjedetalje**, **Medlem af projektteam** og **Estimatlinje**.
7. Gentag trin 1-6 for den grupperede indstilling **Arbejdstimer for ressource**. 

> ![Føje arbejdssted for ressource til estimatlinje](media/RWL-Default-Value.png)

I forbindelse med levering og fakturering skal fuldført arbejde prissættes korrekt for at kunne vælge, om det blev udført **lokalt** eller **på stedet**, og om det blev udført inden for den **ordinære arbejdstid** eller som **overarbejde** under Projektets faktiske værdier. Felterne **Arbejdssted for ressource** og **Arbejdstimer for ressource** skal føjes til objekterne **Tidsregistrering**, **Faktisk**, **Fakturalinjedetalje** og **Kladdelinje**.

1. Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner**.
2. Vælg **Objekter > Tidsregistrering** i venstre navigationsrude i løsningsoversigten.
3. Udvid objektet **Tilbudslinjedetaljer**, og vælg derefter **Felter**.
4. Vælg **Ny** for at oprette et nyt felt med navnet **Arbejdssted for ressource**, og vælg **Grupperet indstilling** som felttype. 
5. Vælg **Brug en eksisterende grupperet indstilling**, vælg den grupperede indstilling **Arbejdssted for ressource**, og vælg derefter **Gem**.
6. Gentag trin 1-5 for at føje dette felt til objekterne **Faktisk**, **Fakturalinjedetalje** og **Kladdelinje**.
7. Gentag trin 1-6 for den grupperede indstilling **Arbejdstimer for ressource**. 

> ![Føje arbejdssted for ressource til tidsregistrering](media/RWL-time-entry.png)

Derved er de nødvendige skemaændringer fuldført for brugerdefinerede dimensioner, der er baseret på grupperede indstillinger.

## <a name="entity-based-custom-pricing-dimensions"></a>Brugerdefinerede prisdimensioner baseret på objekter

Når den brugerdefinerede prisdimension er et objekt, skal du tilføje 1:N-relationer mellem dimensionsobjektet og nøgleobjekterne. Hvis du bruger standardtiteleksemplet ovenfor, er det rimeligt at forvente, at de enkelte medarbejdere får tildelt en standardtitel. Som resultat heraf skal du have en 1:N-relation fra standardtitel til fakturerbar ressource eller en N:1-relation, hvis den blev oprettet fra reserverbar ressource til standardtitlen.

1. Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner** i Project Operations. 
2. Vælg **Objekter > Standartitel** i venstre navigationsrude i løsningsoversigten.
3. Udvid objektet **Standardtitel**, og vælg **1:N-relationer**.
4. Vælg **Ny** for at oprette en ny 1:N-relation med navnet **Standardtitel til reserverbar ressource**. Angiv de nødvendige oplysninger, og vælg derefter **Gem**.

> ![Tilføjelse af standardtitel som et referencefelt til en ressource, der kan reserveres](media/ST-BR.png)

Standardtitlen skal også tilføjes til objekterne for prisfastsættelse, **Rollepris** og **Rolleprisavance**. Dette udfyldes også ved brug af 1:N-relationer mellem objekterne **Standardtitel** og **Rollepris** og objekterne **Standardtitel** og **Rolleprisavance**.

1. Vælg **Objekter > Standartitel** i venstre navigationsrude i løsningsoversigten.
2. Udvid objektet **Standardtitel**, og vælg **1:N-relationer**.
3. Vælg **Ny** for at oprette en ny 1:N-relation med navnet **Standardtitel for rollepris**. Angiv de nødvendige oplysninger, og vælg derefter **Gem**.
4. Gentag trin 1-4 for at oprette 1:N-relationer mellem objekterne **Standardtitel** og **Rolleprisavance**.

I salgs- og estimatfaserne for projektet er det nødvendigt at prissætte tilbuds-/projektestimater for arbejdsindsatsen for de enkelte standardtitler. Det betyder, at der skal bruges 1:N-relationer fra Standardtitel til hvert af disse estimatobjekter: 

- **Tilbudslinjedetaljer**
- **Projektkontraktlinjedetalje**
- **Medlem af projektteam**
- **Estimatlinje**

5. Gentag trin 1-5 for at oprette 1:N-relationer fra **Standardtitel** til **Tilbudslinjedetaljer**, **Projektkontraktlinjedetaljer**, **Medlem af projektteam** og **Estimatlinje**.

> ![Tilføjelse af standardtitel som et referencefelt til en estimatlinje](media/ST-Estimate-Line.png)

  I faserne levering og fakturering skal det arbejde, der er udført af hver enkelt standardtitel, være præcist prissat under Projektets faktiske værdier. Det betyder, at der skal være 1:N-relationer fra **Standardtitel** til objekterne **Tidsregistrering**, **Faktisk**, **Fakturalinjedetaljer** og **Kladdelinje**.

6. Gentag trin 1-6 for at oprette 1:N-relationer fra **Standardtitel** til objekterne **Tidsregistrering**, **Faktisk**, **Fakturalinjedetalje** og **Kladdelinje**.

> ![Tilføjelse af standardtitel som et referencefelt til tidsregistrering](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Konfigurer dimensionsværdierne som standard ved hjælp af tilknytningsfunktionerne i platformen
I forbindelse med tidsregistrering ville det være en hjælp at have systemet til som standard at angive standardtitlen på tidsregistreringen fra den reserverbare ressource, der registrerer tidsposten. Benyt følgende fremgangsmåde for at føje felttilknytninger i 1:N-relationen fra **Reserverbar ressource** til **Tidsregistrering**.

1. Vælg **Objekter > Standartitel** i venstre navigationsrude i løsningsoversigten.
2. Udvid objektet **Standardtitel**, og vælg **1:N-relationer**.
3. Dobbeltklik på **Reserverbar ressource til tidsregistrering**. På siden **Relation** skal du vælge **Brug felttilknytninger**. 
4. Vælg **Ny** for at oprette en ny felttilknytning mellem feltet **Standardtitel** på objektet **Reserverbar ressource** til referencefeltet **Standardtitel** på objektet **Tidsregistrering**. 

> ![Konfigurer felttilknytninger for at give mulighed for at anvende standardtitel som standard fra reserverbar ressource til tidsregistrering](media/ST-Mapping2.png)

Derved er de nødvendige skemaændringer fuldført for brugerdefinerede dimensioner, der er baseret på objekter.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Føje brugertilpassede felter til formularer, visninger og forretningsregler

Når du har foretaget alle de nødvendige skemaændringer, er det næste trin at gøre felterne synlige i BRUGERGRÆNSEFLADEN ved at føje felterne til formularerne og visningerne.

1. Åbn formularen eller visningen. Vælg feltet i højre navigationsrude, og træk det til formularlærredet. 
2. Hvis du redigerer en visning, skal du bruge højre navigationsrude, vælge **Tilføj felter** og i dialogboksen **Liste over felter** vælge de felter, du har brug for, og vælge **OK**.

Følgende tabel indeholder en omfattende liste over standardformularer og -visninger, efter objekt, der skal opdateres med de nye felter. Hvis du har flere visninger eller formularer i tilpasningerne af disse objekter, kan du også føje de nye felter til dem.

| Enhed        | Formularer, der skal bruge det nye felt   |Visninger, der skal bruge det nye felt      |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris|• Oplysninger |• Aktive ressourcekategoripriser<br> • Visning for tilknyttede ressourcekategoripriser|
|  Rolleprisavance|• Oplysninger|• Aktiv rolleprisavance<br>• Visning for tilknyttet rolleprisavance|
|  Tilbudslinjedetaljer|• Projektoplysninger<br>• Hurtig oprettelse af projekt|• Aktiv tilbudslinjedetalje<br>• Kombinerede tilbudslinjedetaljer<br>• Visning for tilknyttet tilbudslinjedetalje|
|  Projektkontraktlinjedetalje|• Projektoplysninger<br>• Hurtig oprettelse af projekt|• Kombinerede kontraktlinjedetaljer<br>• Aktive kontraktlinjedetaljer<br>• Tilknyttet visning af kontraktlinjedetaljer|
|  Medlem af projektteam|• Oplysninger<br>• Ny formular|• Aktive medlemmer af projektteam<br>• Medlemmer af projektteam<br>• Visning for tilknyttede medlemmer af projektteam|
|  Tidsregistrering|• Oplysninger<br>• Oprette tidsregistrering|• Mine tidsregistreringer efter dato<br>• Mine tidsregistreringer for denne uge<br>• Tidsregistreringer til godkendelse.|
|  Kladdelinje|• Oplysninger<br>• Hurtig oprettelse:|• Aktive kladdelinjer<br>• Visning for tilknyttet kladdelinje|
|  Fakturalinjedetalje|• Oplysninger<br>• Hurtig oprettelse:|• Aktive fakturalinjedetaljer<br>• Fakturerbare fakturatransaktioner<br>• Gratis fakturatransaktioner<br>• Visning for tilknyttede fakturalinjedetaljer<br>• Ikke-fakturerbar fakturatransaktion|
|  Faktisk|• Oplysninger<br>• Aktive faktiske|• Visning for tilknyttet faktisk|

Det kan også være nødvendigt at tilføje brugerdefinerede felter i forretningsregler, afhængigt af hvad du har defineret. Et standardeksempel gælder forretningsreglen **Redigerbarhed af Tidsregistrering baseret på status**. Denne regel definerer, hvilke felter der skal låses, når tidsregistreringen befinder sig i en status, der ikke kan redigeres, f.eks. **Godkendt**. Føj felter til denne forretningsregel, så felterne låses mod redigering, når tidsregistreringen befinder sig i en status, der ikke er **Kladde** eller **Returneret**.
