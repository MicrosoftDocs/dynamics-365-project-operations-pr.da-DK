---
title: Forlængelse af tidsregistreringer
description: Dette emne indeholder oplysninger om, hvordan udviklere kan forlænge tidsregistreringskontrolelementet.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 190ad9e1f9ced690aee953ed992bf7aa2844c3b3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074071"
---
# <a name="extending-time-entries"></a>Forlængelse af tidsregistreringer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations indeholder et brugerdefineret tidsregistreringskontrolelement, som kan forlænges. Dette kontrolelement indeholder følgende funktioner:

- Angivelse af tid horisontalt over en uge
- Totaler efter dag, række eller uge
- Kopier rækker eller uger
- Tidsregistreringer via TT:mm eller HH.hh (konverteres automatisk til HH.hh)
- Importer fra tildelinger, reservationer eller aftaler

Det er muligt at forlænge tidsregistreringer på to områder:
- [Tilføj brugerdefinerede tidsregistreringer til dit eget brug](#add)
- [Brugertilpas kontrolelementet for de ugentlige tidsregistreringer](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Tilføj brugerdefinerede tidsregistreringer til dit eget brug

Tidsregistreringer er et kerneobjekt, der bruges i flere scenarier. I den første bølge i april 2020 blev kerneløsningen TESA introduceret. TESA indeholder et objekt med **Indstillinger** og en ny sikkerhedsrolle i form af **Tidsregistreringsbruger**. De nye felter, **msdyn_start** og **msdyn_slut** , som har en direkte relation til **msdyn_varighed** , er også inkluderet. Det nye objekt, sikkerhedsrolle og felter muliggør en mere ensartet proces for tid på tværs af flere produkter.


### <a name="time-source-entity"></a>Tidskildeobjekt
| Felt | Beskrivelse | 
|-------|------------|
| Navn  | Navnet på det tidskildeobjekt, der bruges som udvælgelsesværdi, når du opretter tidsregistreringer. |
| Standardtidskilde [Tidskilde: erstandard] | Som standard kan kun én tidskilde markeres som standard. Dette gør det muligt for registreringer at gå tilbage til standarden for en tidskilde, hvis der ikke er angivet en. |
|Tidskildetype [Tidskilde: kildetype] | Kildetypen er en indstilling (tidsregistreringskildetype), der gør det muligt at knytte tidskilden til en app. Microsoft reserverer værdier, der er større end 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Tidsregistreringer og tidskildeobjektet
Hver gang tilknyttes en tidsregistrering til en tidskildepost. Denne post bestemmer, hvordan og hvilke programmer der skal behandle tidsregistreringen.

Tidsregistreringer er altid én sammenhængende tidsblok med sammenkædet starttidspunkt, sluttidspunkt og varighed.

Logikken for tidsregistrering opdateres automatisk i følgende situationer:

- Hvis to af de tre følgende felter er angivet, beregnes den tredje automatisk: 

    - **msdyn_start**
    - **msdyn_slut**
    - **msdyn_varighed**

- Felterne **msdyn_start** og **msdyn_slut** er tidszonefølsomme.
- Tidsregistreringer, der kun oprettes med **msdyn_dato** og **msdyn_varighed** angivet, starter ved midnat. Felterne **msdyn_start** og **msdyn_slut** opdaterer i overensstemmelse hermed.

#### <a name="time-entry-types"></a>Tidsregistreringstyper

Tidsregistreringsposter har en tilknyttet type, der definerer funktionsmåden i indsendelsesflowet for det tilknyttede program.

|Etiket | Værdi|
|-----|-----|
|Holder pause   |192,355,000|
|Rejse | 192,355,001|
|Overtid   | 192,354,320|
|Arbejde   | 192,350,000|
|Fravær    | 192,350,001|
|Ferie   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Brugertilpas kontrolelementet for de ugentlige tidsregistreringer
Udviklere kan tilføje flere felter og opslag til andre objekter og implementere brugerdefinerede forretningsregler, der understøtter virksomhedens forretningsscenarier.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Tilføj brugerdefinerede felter med opslag til andre objekter
Der er tre hovedtrin, når du vil føje et brugerdefineret felt til det ugentlige tidsregistreringsgitter.

1. Føj det brugerdefinerede felt til dialogboksen til hurtig oprettelse.
2. Konfigurer gitteret for at få vist det brugerdefinerede felt.
3. Tilføj det brugerdefinerede felt til opgaveprocessen for rækkeredigering eller celleredigering.

Sørg for, at det nye felt har de krævede valideringer i række- eller celleredigeringen af opgaveprocessen. Som en del af dette trin skal feltet låses på basis af tidsregistreringens status.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Føj det brugerdefinerede felt til dialogboksen til hurtig oprettelse
Tilføj det brugerdefinerede felt til dialogboksen **Hurtig oprettelse af tidsregistrering**. Der kan herefter angives en værdi, når tidsregistreringer tilføjes, ved at vælge **Ny**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurere gitteret til at vise det brugerdefinerede felt
Der er to måder, du kan føje et brugerdefineret felt til det ugentlige tidsregistreringsgitter på:

  - Tilpas en visning og tilføj et brugerdefineret felt
  - Opret en ny standard og brugertilpasset tidsregistrering 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Tilpas en visning og tilføj et brugerdefineret felt

Tilpas visningen **Mine ugentlige tidsregistreringer** og tilføj det brugerdefinerede felt hertil. Du kan vælge placeringen af og størrelsen på det brugerdefinerede felt i gitteret ved at redigere egenskaberne i visningen.

#### <a name="create-a-new-default-custom-time-entry"></a>Opret en ny standard og brugertilpasset tidsregistrering

Denne visning skal indeholde felterne **Beskrivelse** og **Eksterne kommentarer** ud over de kolonner, der skal være i gitteret. 

1. Vælg placeringen, størrelsen og standardsorteringsrækkefølgen i gitteret ved at redigere de pågældende egenskaber i visningen. 
2. Konfigurer det brugerdefinerede kontrolelement for denne visning, så det bliver et kontrolelement af typen **Tidsregistreringsgitter**. 
3. Føj dette kontrolelement til visningen, og vælg det til internettet, telefonen og tabletten. 
4. Konfigurer parametrene for det ugentlige tidsregistreringsgitter. 
5. Angiv feltet **Startdato** til **msdyn_date** , angiv feltet **Varighed** til **msdyn_duration** , og angiv feltet **Status** til **msdyn_entrystatus**. 
6. I standardvisningen er feltet **Skrivebeskyttet statusliste** angivet til **192350002,192350003,192350004**. Feltet **Opgaveproces for redigering af række** er angivet til **msdyn_tidsregistreringredigeringafrække**. Feltet **Opgaveproces for redigering af celle** er angivet til **msdyn_tidsregistreringredigering**. 
7. Du kan tilpasse disse felter for at tilføje eller fjerne status for skrivebeskyttelse eller bruge en anden opgavebaseret oplevelse (TBX) til række- eller celleredigering. Disse felter er nu bundet til en statisk værdi.


> [!NOTE] 
> Begge indstillinger fjerner noget af standardfiltreringen for objekterne **Projekt** og **Projektopgave** , så alle opslagsvisninger for objekterne er synlige. Som standard er det kun de relevante opslagsvisninger, der er synlige.

Vælg den relevante opgaveproces til det brugerdefinerede felt. Hvis du har tilføjet feltet til gitteret, bør det blive placeret i opgaveprocessen for redigering af rækker, der bruges til felter, som gælder for hele rækken af tidsregistreringer. Hvis det brugerdefinerede felt har en entydig værdi hver dag, f.eks. et brugerdefineret felt for **Sluttidspunkt** , skal det placeres i celleredigeringen af opgaveprocessen.

Hvis du vil føje det brugerdefinerede felt til en opgaveproces, skal du trække et **Felt** -element til den relevante placering på siden og derefter angive feltets egenskaber. Angiv egenskaben **Kilde** til **Tidsregistrering** , og angiv egenskaben **Datafelt** til det brugerdefinerede felt. Egenskaben **Felt** angiver det viste navn på TBX-siden. Vælg **Anvend** for at gemme dine ændringer i feltet, og vælg derefter **Opdater** for at gemme ændringerne på siden.

Hvis du vil bruge en ny brugerdefineret TBX-side i stedet, skal du oprette en ny proces. Angiv kategorien til **Forretningsprocesforløb** , angiv objektet til **Tidsregistrering** , og angiv forretningsprocestypen til **Kør processen som en opgaveproces**. Egenskaben **Sidenavn** under **Egenskaber** skal angives til det viste navn for siden. Føj alle de relevante felter til TBX-siden. Gem og aktivér processen. Opdater egenskaben for det brugerdefinerede kontrolelement for den relevante opgaveproces til værdien af **Navn** i processen.

### <a name="add-new-option-set-values"></a>Angive nye værdier for grupperet indstilling
Hvis du vil føje værdier for grupperet indstilling til et standardfelt, skal du åbne redigeringssiden til feltet og under **Type** vælge **Rediger** ud for den grupperede indstilling. Tilføj en ny indstilling, der har et brugerdefineret navn og farve. Hvis du vil tilføje en ny status for tidsregistreringen, er kaldes standardfeltet **Status for registrering** og ikke **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Angive en ny status for tidsregistrering som skrivebeskyttet
Hvis du vil angive skrivebeskyttet som ny status for tidsregistreringen, skal du tilføje den nye værdi for tidsregistreringen til egenskaben **Skrivebeskyttet statusliste**. Den redigerbare del af tidsregistreringsgitteret låses for rækker, der har den nye status.
Tilføj derefter forretningsregler for at låse alle felter på TBX-siderne **Redigering af tidsregistreringsrække** og **Redigering af tidsregistrering**. Du kan få adgang til forretningsreglerne for disse sider ved at åbne editoren for forretningsprocesforløb og derefter vælge **Forretningsregler**. Du kan føje den nye status til betingelsen i de eksisterende forretningsregler, eller du kan tilføje en ny forretningsregel for den nye status.

### <a name="add-custom-validation-rules"></a>Tilføje brugerdefinerede valideringsregler
Der findes to typer valideringsregler, som du kan tilføje i det ugentlige tidsregistreringsgitter:

- Forretningsregler, der fungerer på klientsiden, i hurtig oprettelse af dialogbokse og på TBX-sider.
- Plug-in-valideringer på serversiden, der gælder for alle tidsregistreringsopdateringer.

#### <a name="business-rules"></a>Forretningsregler
Brug forretningsregler til at låse og låse op for felter, angive standardværdier i felter og definere valideringer, der kun kræver oplysninger fra den aktuelle tidsregistreringspost. Du kan få adgang til forretningsreglerne for en TBX-side ved at åbne editoren for forretningsprocesforløb og derefter vælge **Forretningsregler**. Du kan derefter redigere de eksisterende forretningsregler eller tilføje en ny forretningsregel. Hvis du vil have endnu flere brugerdefinerede valideringer, kan du bruge en forretningsregel til at køre JavaScript.

#### <a name="plug-in-validations"></a>Plug-in-valideringer
Brug plug-in-valideringer for alle valideringer, der kræver mere kontekst, end hvad der er tilgængeligt i en enkelt tidsregistreringspost eller for eventuelle valideringer, som du vil køre for indbyggede opdateringer i gitteret. Hvis du vil fuldføre valideringen, skal du oprette en brugerdefineret plug-in i objektet **Tidsregistrering**.

### <a name="copying-time-entries"></a>Kopiering af tidsregistreringer
Brug visningen **Kopier kolonner med tidsregistreringer** for at definere listen over de felter, der skal kopieres i forbindelse med tidsregistreringer. **Dato** og **Varighed** er obligatoriske felter og skal ikke fjernes fra visningen.
