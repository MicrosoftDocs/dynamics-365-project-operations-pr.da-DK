---
title: Afdelinger
description: I denne artikel beskrives konceptet med afdelinger, og det forklares, hvordan du kan oprette og vedligeholde afdelinger i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921617"
---
# <a name="organizational-units-overview"></a>Oversigt over afdelinger

I Microsoft Dynamics 365 Project Operations er en *afdeling* en bestemt gruppe eller division i en professionel servicevirksomhed, som beskæftiger fakturerbare ressourcer med omkostningssatser.

For professionelle servicevirksomheder, der anvender tekniske ressourcer i forskellige øvelses- eller forretningsområder, kan omkostningerne ved at udfylde en rolle i ét øvelses- eller forretningsområde variere afhængigt af det øvelses- eller forretningsområde, hvor rollen udfyldes. I dette scenarie hjælper begrebet afdelinger ved at give måde, hvorpå man kan gruppere et sæt fakturerbare roller i en division i et firma, som har en bestemt omkostningsstruktur for disse roller.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Konceptet med afdelinger i Project Operations

I Project Operations har en afdeling en bestemt valuta og specifikke kostprislister.

En organisationsenheds valuta er den primære valuta, der bruges til at spore omkostninger.

Der kan knyttes en eller flere kostprislister til hver enkelt organisationsenhed. Project Operations sætter følgende begrænsninger på de prislister, der kan tilknyttes en afdeling:

- Prislisterne skal være angivet i valutaen for afdelingen.
- Prislisterne skal være kostprislister.

Derudover omfatter ressourceobjektet en attribut for afdelingen. Hver ressource kan tildeles til én organisationsenhed.

### <a name="roles-of-organizational-units"></a>Roller i organisationsenheder

Afdelingerne spiller to roller i Project Operations:

- **Kontraktenhed** – organisationsenheden, der repræsenterer den virksomhedsgruppe eller division, som primært er ansvarlig for at vinde salg og administrere levering af arbejde og servicer til kunden. Kontraktenheden identificeres via feltet **Kontraktenhed** i overskriftssektionen på siderne **Salgsmulighed**, **Tilbud**, **Projektkontrakt** og **Projekt**.
- **Ressourceenhed** – den organisationsenhed, som en ressource tilhører eller er tildelt til. Denne organisationsenhed kan levere sine ressourcer til bestemte roller i arbejdserklæringer (SOW'er) og projekter, der ejes af kontraktenheden.

![Kontraktenheder og ressourceenheder.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Ofte stillede spørgsmål om afdelinger

Her følger nogle af de oftest stillede spørgsmål om organisationsenheder.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hvordan er objektet Afdelinger i Project Operations relateret til det objektet Afdelinger, der allerede findes i Dynamics 365?

Objektet Afdelinger i Dynamics 365 repræsenterer navnet på en global Dynamics 365-forekomst. Dette navn er som regel navnet på den globale virksomhed.

Objektet Organisationsenhed repræsenterer en gruppe eller division i den globale virksomhed. Denne gruppe eller division har et sæt roller og en kostprisliste for disse roller, og disse roller og prislister adskiller sig fra rollerne og prislisten for andre grupper eller divisioner i virksomheden.

Når Project Operations er installeret, oprettes der en standardafdeling, som er baseret på organisationen. Alle eksisterende ressourcer tildeles til standardorganisationsenheden. Hvis nye Active Directory-brugere eller -ressourcer importeres til Dynamics 365, tildeler brugerimportprocessen dem til standardafdelingen i Project Operations .

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Hvordan adskiller objektet Afdeling sig fra afdelingsobjektet?

I Dynamics 365 er objektet Afdeling en sikkerhedskonstruktion. Tilknytningen af en bruger til en afdeling bestemmer, hvilke objekter og objektposter brugeren har adgang til. Den bestemmer også, hvilke tilladelser (Opret, Læs, Skriv, Slet, Tilføj, Føj til, Tildel eller Del) brugeren har til disse objektposter.

Organisationsenhedsobjektet repræsenterer en firmagruppe eller division, der har bestemte omkostningssatser for medarbejdere, der er tildelt til den. En ressources tilknytning til en organisationsenhed bestemmer ressourcens omkostninger i et projektengagement.

Når du implementerer Dynamics 365, skal du optimere sikkerhedsgodkendelsen for hierarkiet af afdelinger og tildelingen af brugere til afdelinger. Tildel alle brugere, der normalt skal have adgang til det samme sæt poster, til den samme afdeling. Organisationsenheden har ingen indvirkning på sikkerhedstilladelser eller adgang.

**Eksempel, der viser én mulig forskel i opsætningen af organisationsenheder og afdelinger**

Contoso, Ltd. har succes med Microsoft-teknologiøvelser. Prakash og Tricia er begge C\#-udviklere, men Tricia er i USA, mens Prakash er i Indien. De fleste projektarrangementer kræver ressourcer fra både Contoso India og Contoso US, og Prakash og Tricia kræver samme niveau for sikkerhedsadgang til projekter i dette erhvervsområde. Men udgifterne til udviklere fra Contoso India adskiller sig betydeligt fra udgifterne til udviklere fra Contoso US.

Her er en optimal måde at designe dette scenario på i forbindelse med brug af Dynamics 365 og Project Operations.

1. Opret Microsofts-teknologiøvelse som en afdeling, og knyt den til Prakash og Tricia. På denne måde kan du være med til at sikre, at begge medarbejdere har samme sikkerhedsadgang til alle projekter i det pågældende erhvervsområde. De kan både kontrollere status og rapportere tid, udgifter, materialeforbrug og opgaveopdateringer.
2. Opret to organisationsenheder for at få garanti for, at omkostningerne til projektet afspejles korrekt.
3. Tilknyt Tricia til Contoso US og Prakash til Contoso India.
4. Tildel relevante kostprislister til begge organisationsenheder. På denne måde kan du være med til at sikre, at de omkostninger, der er registreret for projektet for Prakash og Tricia, afspejler forskellen i omkostningerne mellem Contoso US og Contoso India nøjagtigt.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Er organisationsenheder relateret til salgsdistrikter i Dynamics 365?

Der er ingen tilknytning eller relation mellem salgsdistrikter og organisationsenheder. Et salgsdistrikt er som regel et geografisk område, hvor salget finder sted. Der kan knyttes en salgsprisliste til de enkelte salgsdistrikter.

En organisationsenhed er en intern gruppe eller division i virksomheden, der sporer omkostninger for et sæt roller, som den sælger til andre divisioner eller eksterne kunder.

**Eksempel, der viser én mulig forskel i opsætningen af organisationsenheder og salgsområder**

Contoso, Ltd. har to udviklingscentre: Contoso US og Contoso India. Omkostningerne til ressourcerne varierer meget mellem disse to udviklingscentre. Contoso sælger sine it-servicer på mange internationale markeder, f.eks. Latinamerika, Nordamerika, Asien og Stillehavsområdet, Vesteuropa og Mellemøsten. Fakturasatser for samme projektroller kan variere meget på tværs af disse markeder. Contoso US og Contoso India skal oprettes som organisationsenheder, og hver enkelt organisationsenhed skal have sin egen kostprisliste. Asien og Stillehavsområdet, Latinamerika, Nordamerika, Vesteuropa og Mellemøsten skal oprettes som salgsdistrikter, og de enkelte salgsdistrikter skal have sin egen salgsprisliste.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Hvorfor er der begrænsning på tilknytning af prislister til organisationsenheder?

Salgsprisfastsættelse er sædvanligvis entydig for de geografiske områder eller markeder, hvor de pågældende servicer sælges. Interne divisioner i en virksomhed har ikke normalt deres egen salgsprisfastsættelse for den samme type servicer. Interne divisioner har dog forskelligt vareforbrug, afhængigt af færdighederne hos de personer, de har ansat, og arbejdsvilkårene i det område de opererer i. Da organisationsenheder er udformet som interne divisioner i en virksomhed, kan de kun have kostprislister.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Hvorfor kan vi ikke knytte salgsprislister sammen med organisationsenheder?

I Project Operations kan salgsprislister knyttes til kunder og salgsområder. Transaktionsobjekter såsom Salgsmulighed, Tilbud, Projektkontrakt og Projekt bruger salgsprislister, som er vedhæftet kundefirmaet eller salgsdistriktet, til at fastlægge fakturasatser og potentiel omsætning for projektengagementet.

Kostprislister er knyttet til organisationsenheder. Transaktionsobjekter såsom Salgsmulighed, Tilbud, Projektkontrakt og Projekt bruger kostprislister, som er vedhæftet kontraktenheden, til at fastlægge omkostninger for et projektengagement.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Er organisationsenheder hierarkisk opdelt i Project Operations ?

Nej. I den aktuelle version af Project Operations er organisationsenheder ikke hierarkiske. Du kan derfor ikke udføre følgende opgaver:

- Konfigurere et mønster til angivelse af standardkostpriser, der flyttes op i et hierarki.
- Rapportere omsætning eller omkostninger, der er akkumuleret på forskellige niveauer i hierarkiet for organisationsenheder.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Vi er et stort multinationalt firma, der har et komplekst hierarki på flere niveauer med omkostningscentre, divisioner og faktureringskontorer. Hvordan kan vi bedst bruge konceptet med organisationsenheder i den aktuelle version af Project Operations?

Når du har et komplekst hierarki af omkostningssteder, divisioner, faktureringssteder osv., skal du konfigurere bladnoderne for dette hierarki som bestemte organisationsenheder.

Følgende eksempel viser et typisk hierarki.

**Contoso India**

- SAP-øvelse

    - Tekniske konsulenter
    - Funktionelle konsulenter

- Microsoft-teknologiøvelse

    - Tekniske konsulenter
    - Funktionelle konsulenter

**Contoso USA**

- SAP-øvelse

    - Tekniske konsulenter
    - Funktionelle konsulenter

- Microsoft-teknologiøvelse

    - Tekniske konsulenter
    - Funktionelle konsulenter

Hvis hierarkiet ligner dette eksempel, skal du konfigurere det som en komprimeret liste, som vist her:

- Contoso India - SAP-øvelse - Tekniske konsulenter
- Contoso India - SAP-øvelse - Funktionelle konsulenter
- Contoso India - Microsoft-teknologiøvelse Funktionelle konsulenter
- Contoso India - Microsoft-teknologiøvelse Funktionelle konsulenter
- Contoso US - SAP-øvelse - Tekniske konsulenter
- Contoso US - SAP-øvelse - Funktionelle konsulenter
- Contoso US - Microsoft-teknologiøvelse - Tekniske konsulenter
- Contoso US - Microsoft-teknologiøvelse - Funktionelle konsulenter

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Vi er en lille professionel servicevirksomhed, der udelukkende fungerer som én division. Hvordan kan vi bedst bruge konceptet med organisationsenheder i den aktuelle version af Project Operations?

Hvis virksomheden opererer som én enhed, der har en kostprisliste, behøver du ikke at konfigurere organisationsenheder. Installationen af Project Operations opretter én standardorganisationsenhed, der har samme navn som organisationen. Alle brugere er som standard tildelt til denne organisationsenhed. Når systemet kræver, at der vælges en organisationsenhed, vælges denne organisationsenhed som standard.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Når et projekt oprettes på baggrund af et tilbud eller en projektkontraktlinje, hentes standardkontraktenheden fra tilbuddet eller projektkontrakten. Hvad er standardkontraktenheden, hvis et projekt oprettes før salgsobjekter, f.eks. tilbud eller projektkontrakt?

Når et projekt oprettes selvstændigt, er standardkontraktenheden for projektet baseret på den bruger, der opretter den. Denne bruger er også standardprojektleder. Hvis projektet er knyttet til et salgsobjekt, f.eks. et tilbud eller en projektkontrakt, er kontraktenheden for projektet i stedet baseret på salgsobjektet. I dette tilfælde beregnes projektestimater muligvis igen, da kostprislisten bruges til at beregne ændringer i omkostningsestimat, hvis kontraktenheden ændres. Salgsprislisten bruges til at beregne de salgsestimater, der skal ændres, så de er synkroniseret med projektprislisten i tilbuddet.

Felterne **Kontraktenhed** og **Valuta** i projektet er låst mod redigering, da de skal være synkroniseret med værdierne i det salgsobjektet (tilbud eller projektkontrakt), som projektet er knyttet til.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Oprettelse og vedligeholdelse af organisationsenheder i Project Operations

Følg disse trin for at oprette organisationsenheder i Project Operations.

1. Gå til **Indstillinger \> Organisationsenheder**.
2. Vælg **Ny**.
3. I området **Generelt** skal du angive et navn for organisationsenheder i feltet **Navn**. Angiv derefter de andre felter efter behov.
4. Vælg **Gem** for at oprette posten, så du kan fortsætte med at redigere den.
5. Under **Kostprislister**, skal du vælge plustegnet (**+**) for at tilføje en prisliste. Du kan kun tilføje prislister, som har **Omkostninger**-konteksten her.
6. I feltet **Navn** skal du vælge knappen **Søg** og vælge en prisliste, som du vil gøre tilgængelige for organisationsenheden. Fortsæt med at tilføje prislister efter behov.
7. Når du er færdig med at tilføje prislister skal du vælge ikonet **Gem** i nederste højre hjørne af siden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
