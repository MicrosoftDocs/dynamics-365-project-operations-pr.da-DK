---
title: Forlængelse af tidsregistreringer
description: Dette emne indeholder oplysninger om, hvordan udviklere kan forlænge tidsregistreringskontrolelementet.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582979"
---
# <a name="extending-time-entries"></a>Forlængelse af tidsregistreringer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations indeholder et brugerdefineret kontrolelement for tidsregistrering, der kan udvides. Dette kontrolelement indeholder følgende funktioner:

- Angivelse af tid horisontalt over en uge
- Totaler efter dag, række eller uge
- Kopier rækker eller uger
- Tidsregistreringer via TT:mm eller HH.hh (konverteres automatisk til HH.hh)
- Importer fra tildelinger, reservationer eller aftaler

Det er muligt at forlænge tidsregistreringer på to områder:
- [Tilføj brugerdefinerede tidsregistreringer til dit eget brug](#add)
- [Brugertilpas kontrolelementet for de ugentlige tidsregistreringer](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Tilføj brugerdefinerede tidsregistreringer til dit eget brug

Tidsregistreringer er et kerneobjekt, der bruges i flere scenarier. I den første bølge i april 2020 blev kerneløsningen TESA introduceret. TESA indeholder et objekt med **Indstillinger** og en ny sikkerhedsrolle i form af **Tidsregistreringsbruger**. De nye felter, **msdyn_start** og **msdyn_slut**, som har en direkte relation til **msdyn_varighed**, er også inkluderet. Det nye objekt, sikkerhedsrolle og felter muliggør en mere ensartet proces for tid på tværs af flere produkter.


### <a name="time-source-entity"></a>Tidskildeobjekt
| Felt | Beskrivelse | 
|-------|------------|
| Navn  | Navnet på det tidskildeobjekt, der bruges som udvælgelsesværdi, når du opretter tidsregistreringer. |
| Standardtidskilde [Tidskilde: erstandard] | Som standard kan kun én tidskilde markeres som standard. Dette gør det muligt for registreringer at gå tilbage til standarden for en tidskilde, hvis der ikke er angivet en. |
|Tidskildetype [Tidskilde: kildetype] | Kildetypen er en indstilling (tidsregistreringskildetype), der gør det muligt at knytte tidskilden til en app. Microsoft reserverer værdier, der er større end 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Tidsregistreringer og tidskildeobjektet
Hver gang tilknyttes en tidsregistrering til en tidskildepost. Denne post bestemmer, hvilke programmer der bør behandle den tidsregistrering, der angives, og hvordan.

Tidsregistreringer er altid én sammenhængende tidsblok med sammenkædet starttidspunkt, sluttidspunkt og varighed.

Logikken for tidsregistrering opdateres automatisk i følgende situationer:

- Hvis to af de tre følgende felter er angivet, beregnes den tredje automatisk: 

    - **msdyn_start**
    - **msdyn_slut**
    - **msdyn_varighed**

- Felterne **msdyn_start** og **msdyn_end** er tidszoneafhængige.
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

1. Tilføj det brugerdefinerede felt til dialogboksen **Hurtig oprettelse**.
2. Konfigurer gitteret for at få vist det brugerdefinerede felt.
3. Tilføj det brugerdefinerede felt til siden **Rediger række** eller **Rediger tidsregistrering** efter behov.

Kontrollér, at det nye felt har de påkrævede valideringer på siden **Rediger række** eller **Rediger tidsregistrering**. Som en del af denne opgave skal du låse feltet på grundlag af tidsregistreringens status.

Når du tilføjer et brugerdefineret felt til gitteret **Tidsregistrering** og derefter opretter tidsregistreringer direkte i gitteret, angives det brugerdefinerede felt for disse registreringer automatisk, så det stemmer overens med rækken. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Tilføj det brugerdefinerede felt til dialogboksen Hurtig oprettelse
Tilføj det brugerdefinerede felt til dialogboksen **Hurtig oprettelse: Opret tidsregistrering**. Brugerne kan derefter angive en værdi, når de tilføjer tidsregistreringer ved at vælge **Ny**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurere gitteret til at vise det brugerdefinerede felt
Der er to måder, hvorpå du kan tilføje et brugerdefineret felt til gitteret **Ugentlig tidsregistrering**:

- Tilpas visningen **Mine ugentlige tidsregistreringer**, og tilføj det brugerdefinerede felt hertil. Du kan specificere placeringen af og størrelsen på det brugerdefinerede felt i gitteret ved at redigere de pågældende egenskaber i visningen.
- Opret en ny brugerdefineret visning for tidsregistrering, og angiv den som standardvisning. Denne visning skal indeholde felterne **Beskrivelse** og **Eksterne kommentarer** ud over de kolonner, der skal inkluderes i gitteret. Du kan specificere placeringen, størrelsen og standardsorteringsrækkefølgen i gitteret ved at redigere de pågældende egenskaber i visningen. Konfigurer derefter det brugerdefinerede kontrolelement for denne visning, så det bliver et kontrolelement af typen **Tidsregistreringsgitter**. Tilføj kontrolelementet til visningen, og vælg det til **Internet**, **Telefon** og **Tablet**. Konfigurer derefter parametrene for gitteret **Ugentlig tidsregistrering**. Angiv feltet **Startdato** til **msdyn\_date**, angiv feltet **Varighed** til **msdyn\_duration**, og angiv feltet **Status** til **msdyn\_entrystatus**. Feltet **Skrivebeskyttet statusliste** er angivet til **192350002 (Godkendt)**, **192350003 (Sendt)** eller **192350004 (anmodet om at blive sendt)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Føje det brugerdefinerede felt til den relevante redigeringsside
De sider, der bruges til at redigere en tidsregistrering eller en række tidsregistreringer, findes under **Formularer**. Knappen **Rediger registrering** i gitteret åbner siden **Rediger registrering**, og knappen **Rediger række** åbner siden **Rediger række**. Du kan redigere disse sider, så de indeholder brugerdefinerede felter.

Begge indstillinger fjerner noget af standardfiltreringen for objekterne **Projekt** og **Projektopgave**, så alle opslagsvisninger for objekterne er synlige. Som standard er det kun de relevante opslagsvisninger, der er synlige.

Du skal vælge den relevante side til det brugerdefinerede felt. Hvis du har tilføjet feltet til gitteret, vil det sandsynligvis fremgå af den side for **Rediger række**, der bruges på felter, som gælder for hele rækken af tidsregistreringer. Hvis det brugerdefinerede felt har en entydig værdi i rækken hver dag (hvis det f.eks. er et brugerdefineret felt til sluttid), bør det fremgå af siden **Rediger tidsregistrering**.

Hvis du vil tilføje det brugerdefinerede felt til en side, skal du trække et **Felt**-element til den relevante placering på siden og derefter angive dets egenskaber.

### <a name="add-new-option-set-values"></a>Angive nye værdier for grupperet indstilling
Hvis du vil tilføje værdier for en grupperet indstilling til et standardfelt, skal du udføre disse trin.

1. Åbn redigeringssiden for feltet, og under **Type** skal du vælge **Rediger** ud for den grupperede indstilling.
2. Tilføj en ny indstilling, der har et brugerdefineret navn og farve. Hvis du vil tilføje en ny status for tidsregistreringen, er navnet på standardfeltet **Status for registrering**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Angive en ny status for tidsregistrering som skrivebeskyttet
Hvis du vil angive skrivebeskyttet som ny status for tidsregistreringen, skal du tilføje den nye værdi for tidsregistreringen til egenskaben **Skrivebeskyttet statusliste**. Sørg for at tilføje nummeret, ikke etiketten. Den redigerbare del af tidsregistreringsgitteret låses nu for rækker, der har den nye status. Hvis du vil angive forskellige egenskaber i form af **Skrivebeskyttet statusliste** for forskellige visninger af **Tidsregistrering**, skal du tilføje gitteret **Tidsregistrering** i en visnings afsnit med **Brugerdefineret kontrol** og konfigurere parameteren efter behov.

Tilføj derefter forretningsregler for at låse alle felter på siderne **Rediger række** og **Rediger tidsregistrering**. Hvis du vil have adgang til forretningsreglerne på disse sider, skal du åbne formulareditor for hver side og derefter vælge **Forretningsregler**. Du kan føje den nye status til betingelsen i de eksisterende forretningsregler, eller du kan tilføje en ny forretningsregel for den nye status.

### <a name="add-custom-validation-rules"></a>Tilføje brugerdefinerede valideringsregler
Du kan tilføje to typer valideringsregler for gitteroplevelsen **Ugentlig tidsregistrering**:

- Forretningsregler på klientsiden, der fungerer på sider
- Plug-in-valideringer på serversiden, der gælder for alle tidsregistreringsopdateringer

#### <a name="client-side-business-rules"></a>Forretningsregler på klientsiden
Brug forretningsregler til at låse og låse op for felter, angive standardværdier i felter og definere valideringer, der kun kræver oplysninger fra den aktuelle tidsregistreringspost. Hvis du vil have adgang til forretningsreglerne for en side, skal du åbne formulareditor og derefter vælge **Forretningsregler**. Du kan derefter redigere de eksisterende forretningsregler eller tilføje en ny forretningsregel.

#### <a name="server-side-plug-in-validations"></a>Validering af plug-in på serversiden
Du skal bruge plug-in-valideringer for alle valideringer, der kræver mere kontekst, end der er tilgængelig i en enkelt tidsregistrering. Du skal også bruge dem til eventuelle valideringer, der skal køres på indbyggede opdateringer i gitteret. Hvis du vil fuldføre valideringerne, skal du oprette en brugerdefineret plug-in i objektet **Tidsregistrering**.

### <a name="limits"></a>Grænser
Gitteret **Tidsregistrering** har i øjeblikket en størrelsesbegrænsning på 500 rækker. Hvis der er mere end 500 rækker, vises overskydende rækker ikke. Det er ikke muligt at øge denne størrelsesbegrænsning.

### <a name="copying-time-entries"></a>Kopiering af tidsregistreringer
Brug visningen **Kopier kolonner med tidsregistreringer** for at definere listen over de felter, der skal kopieres i forbindelse med tidsregistreringer. **Dato** og **Varighed** er obligatoriske felter og skal ikke fjernes fra visningen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
