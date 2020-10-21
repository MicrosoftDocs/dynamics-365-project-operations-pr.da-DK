---
title: Forlængelse af tidsregistreringer
description: Dette emne indeholder oplysninger om, hvordan udviklere kan forlænge tidsregistreringskontrolelementet.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930873"
---
# <a name="extending-time-entries"></a>Forlængelse af tidsregistreringer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations indeholder et brugerdefineret tidsregistreringskontrolelement, som kan forlænges. Dette kontrolelement indeholder følgende funktioner:

- Angivelse af tid horisontalt over en uge
- Totaler efter dag, række eller uge
- Kopier rækker eller uger
- Tidsregistreringer via TT:mm eller HH.hh (konverteres automatisk til HH.hh)
- Importere fra tildelinger, reservationer eller aftaler

Det er muligt at forlænge tidsregistreringer på to områder:
- [Tilføj brugerdefinerede tidsregistreringer til dit eget brug](#add)
- [Brugertilpas kontrolelementet for de ugentlige tidsregistreringer](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Tilføj brugerdefinerede tidsregistreringer til dit eget brug.

Tidsregistreringer er et kerneobjekt, der er udviklet til at blive brugt i flere scenarier. I den første bølge i april 2020 blev TESA-kerneløsningen introduceret, hvilken indeholder et objekt af typen **Indstillinger** og en ny sikkerhedsrolle i form af **Tidsregistreringsbruger**. De nye felter, **msdyn_start** og **msdyn_slut**, som har en direkte relation til **msdyn_varighed**, er også inkluderet. Det nye objekt, sikkerhedsrolle og felter muliggør en mere ensartet proces for tid på tværs af flere produkter.


### <a name="time-source-entity"></a>Tidskildeobjekt
| Felt | Beskrivelse | 
|-------|------------|
| Navn  | Navnet på det tidskildeobjekt, der bruges som udvælgelsesværdi i forbindelse med oprettelse af tidsregistreringen. |
| Standardtidskilde [Tidskilde: erstandard] | Som standard er det kun én tidskilde, der kan være markeret som standardtidskilde. Denne funktion gør det muligt for registreringer at gå tilbage til standarden for en tidskilde, hvis der ikke er angivet en. |
|Tidskildetype [Tidskilde: kildetype] | Kildetypen er en indstilling (tidsregistreringskildetype), der gør det muligt at knytte tidskilden til en app. Der tilføjes flere værdier til denne grupperet indstilling, efterhånden som der tilføjes flere programmer. Bemærk, at Microsoft reserverer værdier, der er større end 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Tidsregistreringer og tidskildeobjektet
Hver gang tilknyttes en tidsregistrering til en tidskildepost. Denne post bestemmer, hvordan og hvilke programmer der skal behandle tidsregistreringen.

Tidsregistreringer er altid én sammenhængende tidsblok med sammenkædet starttidspunkt, sluttidspunkt og varighed.

Logikken for tidsregistrering opdateres automatisk i følgende situationer:

- Hvis to af de tre følgende felter er angivet, beregnes den tredje automatisk 

    - **msdyn_start**
    - **msdyn_slut**
    - **msdyn_varighed**

- Felterne **msdyn_start** og **msdyn_slut** er tidszonefølsomme.
- Tidsregistreringer, der kun oprettes med **msdyn_dato** og **msdyn_varighed** angivet, går i gang ved midnat, og **msdyn_start** og **msdyn_slut** opdateres tilsvarende.

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

- Føj det brugerdefinerede felt til dialogboksen til hurtig oprettelse.
- Konfigurer gitteret for at få vist det brugerdefinerede felt.
- Tilføj det brugerdefinerede felt til enten opgaveprocessen for rækkeredigering eller celleredigering.

Du skal også sikre dig, at det nye felt har de krævede valideringer i række- eller celleredigeringen af opgaveprocessen. Som en del af dette trin skal du låse feltet på basis af tidsregistreringens status.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Føj det brugerdefinerede felt til dialogboksen til hurtig oprettelse
Du skal føje det brugerdefinerede felt til dialogboksen **Hurtig oprettelse af tidsregistrering**. Brugerne kan derefter angive en værdi, når de tilføjer tidsregistreringer ved at vælge **Ny**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurere gitteret til at vise det brugerdefinerede felt
Der er to måder, du kan føje et brugerdefineret felt til det ugentlige tidsregistreringsgitter på:

  - Tilpas en visning og tilføj et brugerdefineret felt
  - Opret en ny standard og brugertilpasset tidsregistrering 


**Tilpas en visning og tilføj et brugerdefineret felt**

Du kan tilpasse visningen **Mine ugentlige tidsregistreringer** og tilføje det brugerdefinerede felt til den. Du kan vælge placeringen af og størrelsen på det brugerdefinerede felt i gitteret ved at redigere de pågældende egenskaber i visningen.

**Opret en ny standard og brugertilpasset tidsregistrering** 

Denne visning skal indeholde felterne **Beskrivelse** og **Eksterne kommentarer** ud over de kolonner, der skal være i gitteret. 

1. Vælg placeringen, størrelsen og standardsorteringsrækkefølgen i gitteret ved at redigere de pågældende egenskaber i visningen. 
2. Konfigurer det brugerdefinerede kontrolelement for denne visning, så det bliver et kontrolelement af typen **Tidsregistreringsgitter**. 
3. Føj dette kontrolelement til visningen, og vælg det til internettet, telefonen og tabletten. 
4. Konfigurer parametrene for det ugentlige tidsregistreringsgitter. Angiv feltet **Startdato** til **msdyn_date**, angiv feltet **Varighed** til **msdyn_duration**, og angiv feltet **Status** til **msdyn_entrystatus**. 
5. Til standardvisningen er feltet **Skrivebeskyttet statusliste** angivet til **192350002,192350003,192350004**, feltet **Rækkerediger opgaveproces** er angivet til **msdyn_timeentryrowedit**, og feltet **Cellerediger opgaveproces** er angivet til **msdyn_timeentryedit**. 
6. Du kan tilpasse disse felter for at tilføje eller fjerne status for skrivebeskyttelse eller bruge en anden opgavebaseret oplevelse (TBX) til række- eller celleredigering. Disse felter skal bindes til en statisk værdi.


> [!NOTE] 
> Begge indstillinger fjerner noget af standardfiltreringen for objekterne **Projekt** og **Projektopgave**, så alle opslagsvisninger for objekterne er synlige. Som standard er det kun de relevante opslagsvisninger, der er synlige.
Du skal vælge den relevante opgaveproces til det brugerdefinerede felt. Hvis du har føjet feltet til gitteret, skal det sandsynligvis placeres i den rækkeredigering af opgaveprocessen, der bruges til felter, som gælder for hele rækken af tidsregistreringer. Hvis det brugerdefinerede felt har en entydig værdi hver dag, f.eks. et brugerdefineret felt for **Sluttidspunkt**, skal det placeres i celleredigeringen af opgaveprocessen.

Hvis du vil føje det brugerdefinerede felt til en opgaveproces, skal du trække et **Felt**-element til den relevante placering på siden og derefter angive feltets egenskaber. Angiv egenskaben **Kilde** til **Tidsregistrering**, og angiv egenskaben **Datafelt** til det brugerdefinerede felt. Egenskaben **Felt** angiver det viste navn på TBX-siden. Vælg **Anvend** for at gemme dine ændringer i feltet, og vælg derefter **Opdater** for at gemme ændringerne på siden.

Hvis du vil bruge en ny brugerdefineret TBX-side i stedet, skal du oprette en ny proces. Angiv kategorien til **Forretningsprocesforløb**, angiv objektet til **Tidsregistrering**, og angiv forretningsprocestypen til **Kør processen som en opgaveproces**. Egenskaben **Sidenavn** under **Egenskaber** skal angives til det viste navn for siden. Føj alle de relevante felter til TBX-siden. Gem og aktivér processen, og opdater derefter det brugerdefinerede kontrolelement egenskab for den relevante opgaveproces til værdien af **Navn** i processen.

### <a name="add-new-option-set-values"></a>Angive nye værdier for grupperet indstilling
Hvis du vil føje værdier for grupperet indstilling til et standardfelt, skal du åbne redigeringssiden til feltet, og derefter skal du under **Type** vælge **Rediger** ud for den grupperede indstilling. Tilføj derefter en ny indstilling, der har et brugerdefineret navn og farve. Hvis du vil tilføje en ny status for tidsregistreringen, er navnet på standardfeltet **Status for registrering**, ikke **Status**.

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
Du skal bruge plug-in-valideringer for alle valideringer, der kræver mere kontekst, end hvad der er tilgængeligt i en enkelt tidsregistreringspost eller for eventuelle valideringer, som du vil køre for indbyggede opdateringer i gitteret. Hvis du vil fuldføre valideringen, skal du oprette en brugerdefineret plug-in i objektet **Tidsregistrering**.
