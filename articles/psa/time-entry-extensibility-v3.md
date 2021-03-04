---
title: Tilpas ugentlige tidsregistreringer
description: Dette emne indeholder oplysninger om, hvordan du implementerer brugerdefinerede forretningsregler, der understøtter praksis i en organisation.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
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
ms.openlocfilehash: a34244884bc81da74ae3bf550bde6f982d04abd3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149626"
---
# <a name="customize-weekly-time-entry"></a>Tilpas ugentlige tidsregistreringer 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Microsoft Dynamics 365 Project Service Automation version 3.3 introducerede Microsoft et moderne gitter, hvor projektressourcer hurtigt kan angive tid for op til en uge ad gangen. Det nye ugentlige tidsregistreringsgitter kan vise totaler for poster efter dato, række eller uge. Ressourcer kan oprette kopier af tidsregistreringer i løbet af ugen og desuden massekopiere fra tidligere uger. Systemtilpassere kan tilpasse visningen ved at tilføje felter, føje opslag til andre objekter og implementere brugerdefinerede forretningsregler for at understøtte organisationens praksis.

Der er adgang til tidsregistreringen og det nye ugentlige tidsregistreringsgitter via oversigten over webstedet. Oplevelsen med den brugerdefinerede tidsregistrering, der ikke kan udvides, som var en del af tidligere PSA-versioner, er blevet erstattet af det ugentlige tidsregistreringsgitter, som kan udvides, og også af en alternativ oplevelse i det skrivebeskyttede gitter og kalenderen. På grund af denne ændring kan brugerne foretage ugentlige tidsangivelser.

## <a name="page-layout"></a>Sidelayout
Det nye ugentlige tidsregistreringsgitter er et brugerdefineret kontrolelement, der har en værktøjslinje og to hovedsektioner **Mål** og **Varighed**. Værktøjslinjen har en knap, der kun gælder for det brugerdefinerede kontrolelement for tidsregistreringsgitteret. Derimod gælder knapperne i handlingsruden øverst på siden for de tre typer kontrolelementer, der understøttes i forbindelse med tidsregistrering: kontrolelementet for ugentlig tidsregistrering, kontrolelementet for skrivebeskyttelse og kalenderkontrolelementet.

### <a name="dimensions"></a>Mål
Sektionen **Mål** viser alle de mål, som tid kan angives i forhold til, som kolonneoverskrifter. Følgende mål understøttes som standard:

- Projekt
- Projektopgave
- Rolle
- Skriv
- Status for registrering

I sektionen **Mål** er det ikke muligt at foretage indbygget redigering. Sektionen understøttes af en visning, hvor brugerdefinerede felter kan føjes til det ugentlige tidsregistreringsgitter. Oplysninger om, hvordan du tilføjer brugerdefinerede felter, finder du i sektionen "Mulighed for udvidelse" senere i dette emne.

### <a name="duration"></a>Varighed
I sektionen Varighed vises dagene i ugen som kolonneoverskrifter. I denne sektion er det muligt at foretage indbygget redigering. Når der er oprettet en tidsregistreringsrække med de rette mål, kan brugere hurtigt angive den tid, de har brugt på disse mål, indlejret.

## <a name="create-a-new-time-entry"></a>Oprette en ny tidsregistrering
Hvis du vil oprette en ny tidsregistrering i tidsregistreringsgitteret, skal du vælge **Ny**. Dialog **Hurtig oprettelse af tidsregistrering** vises. I denne dialogboks kan brugerne vælge dato for tidsregistreringen, og derefter angive data for målene **Projekt**, **Projektopgave**, **Rolle**, og **Varighed** i minutter, timer eller dage ved at skrive **t**, **m** eller **d** sammen med tallet. Brugerne kan også angive en beskrivelse og indtaste kommentarer, der kan deles eksternt i forbindelse med tidsregistreringen. Når brugere gemmer deres ændringer, vises de værdier, de har angivet i forhold til målene, i sektionen **Mål**. De varighedsoplysninger, som de har angivet i feltet **Varighed**, vises på den dato, som tidsregistreringen blev oprettet for.

Opslagsfelter understøttes af systemvisninger. Når en bruger f.eks. indtaster et projekt, er feltet **Projektopgave** som standard angivet til visningen **Kopiér**. Hvis du vil oprette tidsregistreringer for opgaver, der ikke er tildelt til en bruger, skal du vælge **Skift visning** i opslagsdialogboksen og derefter vælge visningen **Alle aktive projektopgaver**.

## <a name="edit-a-time-entry"></a>Redigere en tidsregistrering
Detaljer fra visse felter på siden med tidsregistrering, f.eks **Beskrivelse** og **Eksterne kommentarer** vises ikke i det ugentlige tidsregistreringsgitteret. I stedet vises en lille trekantet indikator i celler med varighed, der indeholder disse yderligere detaljer. Markér cellen, og vælg derefter **Rediger oplysninger** for at få vist dataene i ruden **Hurtig redigering**. For at redigere eller opdatere oplysninger for en bestemt tidsregistrering, der ikke er en del af det ugentlige tidsregistreringsgitter, skal brugerne åbne ruden **Hurtig redigering**.

## <a name="copy-a-time-entry-row"></a>Kopiere en tidsregistreringsrække
Når den første tidsregistreringsrække er oprettet, kan brugerne vælge **Kopiér række** for at kopiere hele rækken til en ny række. Når en række kopieres på denne måde, kopieres mål og varighed også. Brugerne kan også vælge **Rediger række** for at opdatere målværdier og varigheder indlejret i sektionen **Varighed**.

## <a name="open-a-time-entry"></a>Åbne en tidsregistrering
For at understøtte optimal og hurtig indtastning i de mest fremtrædende felter viser det ugentlige tidsregistreringsgitter en delmængde af valgte mål og tidsvarigheder. Hvis du vil have vist alle detaljer om en enkelt tidsregistrering, skal du vælge **Åbn** under **Rediger registrering**.

## <a name="submit-a-time-entry"></a>Sende en tidsregistrering
Brugerne kan sende en enkelt tidsregistrering eller en gruppe tidsregistreringer ved at markere en blok med celler eller en hel tidsregistreringsrække og derefter vælge **Send.** Indsendte tidsregistreringer vises som registreringer, der afventer godkendelse, på godkendersiden **Godkendelse**. Når tidsregistreringerne er sendt, kan de ikke redigeres.

## <a name="recall-a-time-entry"></a>Tilbagekalde en tidsregistrering
Du kan tilbagekalde tidsregistreringer, som du har sendt. Du kan tilbagekalde en enkelt tidsregistrering, en blok med tidsregistreringer eller en hel række med tidsregistreringer. Tilbagekaldte tidsregistreringer er tilgængelige for ressourcer, så de kan redigere dem.

## <a name="time-entry-status"></a>Status for tidsregistrering
Nye tidsregistreringer får automatisk tildelt statussen **Kladde**. Når en tidsregistrering er sendt, opdateres statussen til **Sendt**. Når en sendt tidsregistrering godkendes, opdateres statussen til **Godkendt**. Hvis en tidsregistrering afvises, opdateres statussen til **Returneret**, og registreringen bliver tilgængelig, så den kan rettes og sendes igen. Det er kun tidsregistreringer med statussen **Kladde**, der kan slettes.

## <a name="view-rejection-comments"></a>Se kommentarer til afvisning
Når en tidsregistrering afvises af en godkender, kan godkenderen tilføje kommentarer til afvisningen, så ressourcen bedre forstår årsagen til afvisningen. Hvis du vil have vist kommentarerne til afslaget for en tidsregistrering, skal du vælge **Åbn post**. Kommentarerne til afvisningen vises på tidslinjen. På tidslinjen kan ressourcen give sit svar til kommentarerne til afvisningen, før vedkommende sender registreringen igen.

## <a name="copy-week"></a>Kopiere uge
Når der er oprettet nogle få registreringer, kan brugerne vælge **Kopiér uge** for at masseoprette flere tidsangivelser. Dialogboksen **Kopiér** vises. I sektionen **Fra periode** skal du bruge felterne **Startdato** og **Slutdato** til at definere det datointerval, der skal kopieres tidsregistreringer fra. I feltet **Startdato** i sektionen **Til periode** skal du angive den dato, der skal oprettes tidsregistreringer for. Vælg derefter **Kopiér**. I forbindelse med den angivne dato i perioden "til" oprettes der en kopi af tidsregistreringerne for den tilsvarende ugedag i perioden "fra". Tidsregistreringen for mandag i sidste uge kopieres f.eks. til mandag i den uge, der er angivet som "til"-perioden.

## <a name="import"></a>Importere
Den samme grundlæggende fremgangsmåde bruges til at importere fra reservationer, tildelinger og udvekslinger. Brugerne kan angive det datointerval, som reservationer er importeret fra. De skal derefter udtrykkeligt vælge de reservationer, der skal kopieres til kladder for tidsregistreringer. I den forrige udgivelse blev foreslåede tidsregistreringer vist i gitteret og i kalenderen, og når sessionen blev opdateret, gik de tabt.

## <a name="extensibility"></a>Mulighed for udvidelse af 
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Tilføje brugerdefinerede felter, der har opslag til andre objekter
Der er tre hovedtrin, når du vil føje et brugerdefineret felt til det ugentlige tidsregistreringsgitter.

1.  Føj det brugerdefinerede felt til dialogboksen til hurtig oprettelse.
2.  Konfigurer gitteret for at få vist det brugerdefinerede felt.
3.  Føj det brugerdefinerede felt til enten rækkeredigering af opgaveprocessen eller celleredigering af opgaveprocessen efter behov.

Du skal også sikre dig, at det nye felt har de krævede valideringer i række- eller celleredigeringen af opgaveprocessen. Som en del af dette trin skal du låse feltet på basis af tidsregistreringens status.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Føj det brugerdefinerede felt til dialogboksen til hurtig oprettelse
Du skal føje det brugerdefinerede felt til dialogboksen til hurtig oprettelse af tidsregistrering. Så brugerne kan angive en værdi for den, når de tilføjer tidsregistreringer ved hjælp af knappen **Ny**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurere gitteret til at vise det brugerdefinerede felt
Der er to måder, du kan føje et brugerdefineret felt til det ugentlige tidsregistreringsgitter på. Den første mulighed er at tilpasse visningen **Mine ugentlige tidsregistreringer** og føje det brugerdefinerede felt til den. Du kan vælge placeringen af og størrelsen på det brugerdefinerede felt i gitteret ved at redigere de pågældende egenskaber i visningen.

Den anden mulighed er at oprette en ny brugerdefineret visning for tidsregistrering og angive den som standardvisning. Denne visning skal indeholde felterne **Beskrivelse** og **Eksterne kommentarer** ud over de kolonner, der skal være i gitteret. Du kan vælge placering, størrelse og standardsorteringsrækkefølge i gitteret ved at redigere de pågældende egenskaber i visningen. Konfigurer derefter det brugerdefinerede kontrolelement for denne visning, så det bliver et kontrolelement af typen **Tidsregistreringsgitter**. Føj dette kontrolelement til visningen, og vælg det til internettet, telefonen og tabletten. Konfigurer derefter parametrene for det ugentlige tidsregistreringsgitter. Angiv feltet **Startdato** til **msdyn_date**, angiv feltet **Varighed** til **msdyn_duration**, og angiv feltet **Status** til **msdyn_entrystatus**. Til standardvisningen er feltet **Skrivebeskyttet statusliste** angivet til **192350002,192350003,192350004**, feltet **Rækkerediger opgaveproces** er angivet til **msdyn_timeentryrowedit**, og feltet **Cellerediger opgaveproces** er angivet til **msdyn_timeentryedit**. Du kan tilpasse disse felter for at tilføje eller fjerne status for skrivebeskyttelse eller bruge en anden opgavebaseret oplevelse (TBX) til række- eller celleredigering. Disse felter skal bindes til en statisk værdi.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Føje det brugerdefinerede felt til den relevante redigering af opgaveforløbet
De TBX-sider, der bruges til redigering, kan findes under **Processer**. Standardsiderne er **Project Service - Redigering af tidsregistreringsrække** og **Project Service - Redigering af tidsregistrering**. Du kan enten redigere disse standardsider eller oprette nye brugerdefinerede TBX-sider.

> [!NOTE] 
> Begge indstillinger fjerner noget af standardfiltreringen for objekterne **Projekt** og **Projektopgave**, så alle opslagsvisninger for objekterne er synlige. Som standard er det kun de relevante opslagsvisninger, der er synlige.

Du skal vælge den relevante opgaveproces til det brugerdefinerede felt. Hvis du har føjet feltet til gitteret, skal det sandsynligvis placeres i den rækkeredigering af opgaveprocessen, der bruges til felter, som gælder for hele rækken af tidsregistreringer. Hvis det brugerdefinerede felt har en entydig værdi hver dag, f.eks. et brugerdefineret felt for **Sluttidspunkt**, skal det placeres i celleredigeringen af opgaveprocessen.

Hvis du vil føje det brugerdefinerede felt til en opgaveproces, skal du trække et **Felt**-element til den relevante placering på siden og derefter angive dets egenskaber. Angiv egenskaben **Kilde** til **Tidsregistrering**, og angiv egenskaben **Datafelt** til det brugerdefinerede felt. Egenskaben **Felt** angiver det viste navn på TBX-siden. Vælg **Anvend** for at gemme dine ændringer af feltet. Vælg derefter **Opdater** for at gemme dine ændringer af siden.

Hvis du vil bruge en ny brugerdefineret TBX-side i stedet, skal du oprette en ny proces. Angiv kategorien til **Forretningsprocesforløb**, angiv objektet til **Tidsregistrering**, og angiv forretningsprocestypen til **Kør processen som en opgaveproces**. Egenskaben **Sidenavn** under **Egenskaber** skal angives til det viste navn for siden. Føj alle de relevante felter til TBX-siden. Gem og aktivér processen, og opdater derefter det brugerdefinerede kontrolelement egenskab for den relevante opgaveproces til værdien af **Navn** i processen.

### <a name="add-new-option-set-values"></a>Angive nye værdier for grupperet indstilling
Hvis du vil føje værdier for grupperet indstilling til et standardfelt, skal du åbne redigeringssiden til feltet, og derefter skal du under **Type** vælge **Rediger** ud for den grupperede indstilling. Tilføj derefter en ny indstilling, der har et brugerdefineret navn og farve. Hvis du vil tilføje en ny status for tidsregistreringen, er navnet på standardfeltet **Status for registrering**, ikke **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Angive en ny status for tidsregistrering som skrivebeskyttet
Hvis du vil angive skrivebeskyttet som ny status for tidsregistreringen, skal du føje den nye værdi for tidsregistreringen (nummeret, ikke navnet) til egenskaben **Skrivebeskyttet statusliste**. Den redigerbare del af tidsregistreringsgitteret låses for rækker, der har den nye status.
Tilføj derefter forretningsregler for at låse alle felter på TBX-siderne **Redigering af tidsregistreringsrække** og **Redigering af tidsregistrering**. Du kan få adgang til forretningsreglerne for disse sider ved at åbne editoren for forretningsprocesforløb og derefter vælge **Forretningsregler**. Du kan føje den nye status til betingelsen i de eksisterende forretningsregler, eller du kan tilføje en ny forretningsregel for den nye status.

### <a name="add-custom-validation-rules"></a>Tilføje brugerdefinerede valideringsregler
Der findes to typer valideringsregler, som du kan tilføje i forbindelse med det ugentlige tidsregistreringsgitter: • Forretningsregler på klientsiden, der fungerer i dialogbokse til hurtig oprettelse og på TBX sider • Plug-in-validering på serversiden, der gælder for alle opdateringer af tidsregistreringer

#### <a name="business-rules"></a>Forretningsregler
Brug forretningsregler til at låse og låse op for felter, angive standardværdier i felter og definere valideringer, der kun kræver oplysninger fra den aktuelle tidsregistreringspost. Du kan få adgang til forretningsreglerne for en TBX-side ved at åbne editoren for forretningsprocesforløb og derefter vælge **Forretningsregler**. Du kan derefter redigere de eksisterende forretningsregler eller tilføje en ny forretningsregel. Hvis du vil have endnu flere brugerdefinerede valideringer, kan du bruge en forretningsregel til at køre JavaScript.

#### <a name="plug-in-validations"></a>Plug-in-valideringer
Du skal bruge plug-in-valideringer for alle valideringer, der kræver mere kontekst, end hvad der er tilgængeligt i en enkelt tidsregistreringspost eller for eventuelle valideringer, som du vil køre for indbyggede opdateringer i gitteret. Hvis du vil fuldføre valideringen, skal du oprette en brugerdefineret plug-in i objektet **Tidsregistrering**.

> [!IMPORTANT] 
> Et kendt problem på TBX-siderne forhindrer i øjeblikket brugere i at rette oplysninger og igen markere Udført, når en opdatering ikke lykkes for en plug-in-validering. Du kan løse problemet ved at konfigurere valideringer af forretningsregler, for at denne situation for så vidt muligt undgås.
