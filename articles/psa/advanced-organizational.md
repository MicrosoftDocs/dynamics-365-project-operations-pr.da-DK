---
title: Organisationsenheder
description: Dette emne indeholder oplysninger om organisationsenheder i Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: dccb01e5d1c032039cac980061d93b443ef0f9e1296cdd2d8efd7b1bf7338ce0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005069"
---
# <a name="organizational-units"></a>Organisationsenheder 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation er en organisationsenhed i en bestemt gruppe eller division i en professionel servicevirksomhed, der anvender fakturerbare ressourcer med omkostningssatser.

For professionelle servicevirksomheder, der anvender tekniske ressourcer i forskellige øvelses- eller forretningsområder, kan omkostningerne ved at udfylde en rolle i ét øvelses- eller forretningsområde afvige fra omkostningerne ved at udfylde en rolle i et andet øvelses- eller forretningsområde. Begrebet organisationsenheder er i dette scenarie en hjælp, fordi det er en måde, hvorpå man kan gruppere et sæt fakturerbare roller i en division i et firma, som har en bestemt omkostningsstruktur for disse roller.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Nøgleattributter og tilknytninger til organisationsenheder

I PSA har en organisationsenhed i PSA en bestemt valuta og specifikke kostprislister.

En organisationsenheds valuta er den primære valuta, der bruges til at spore omkostninger.

Der kan knyttes en eller flere kostprislister til hver enkelt organisationsenhed. PSA sætter følgende begrænsninger på de prislister, der kan tilknyttes en organisationsenhed:

- Prislister skal være angivet i valutaen for organisationsenheden
- Prislister skal være kostprislister

Derudover er der en attribut for organisationsenheden i objektet Ressource. Hver ressource kan tildeles til én organisationsenhed.

## <a name="roles-of-organizational-units"></a>Roller i organisationsenheder

Organisationsenheden spiller to roller i PSA:

- **Kontraktenhed** – organisationsenheden, der repræsenterer den virksomhedsgruppe eller division, som primært er ansvarlig for at vinde salg og administrere levering af arbejde og servicer til kunden. Kontraktenheden identificeres via feltet **Kontraktenhed** i overskriftssektionen på siderne **Salgsmulighed**, **Tilbud**, **Projektkontrakt** og **Projekt**.
- **Ressourceenhed** – den organisationsenhed, som en ressource tilhører eller er tildelt til. Denne organisationsenhed kan levere sine ressourcer til bestemte roller i arbejdserklæringer (SOW'er) og projekter, der ejes af kontraktenheden.

> ![Kontraktenheder og ressourceenheder.](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Ofte stillede spørgsmål om organisationsenheder

Her følger nogle af de oftest stillede spørgsmål om organisationsenheder.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hvordan er objektet Organisationsenhed i PSA relateret til det organisationsobjekt, der allerede findes i Dynamics 365?

Organisationsobjektet i Microsoft Dynamics 365 repræsenterer navnet på en global Dynamics 365-forekomst. Dette navn er som regel navnet på den globale virksomhed.

Objektet Organisationsenhed repræsenterer en gruppe eller division i den globale virksomhed. Denne gruppe eller division har et sæt roller og en kostprisliste for disse roller, og disse roller og prislister adskiller sig fra rollerne og prislisten for andre grupper eller divisioner i virksomheden.

Når PSA er installeret, oprettes der en standardorganisationsenhed, der er baseret på organisationen. Alle eksisterende ressourcer tildeles til standardorganisationsenheden. Hvis nye Active Directory-brugere eller -ressourcer importeres til Dynamics 365, tildeler brugerimportprocessen dem til standardorganisationsenheden i PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Hvordan adskiller organisationsenhedsobjektet sig fra afdelingsobjektet?

I Dynamics 365 er objektet Afdeling en sikkerhedskonstruktion. Tilknytningen af en bruger til en afdeling bestemmer, hvilke objekter og objektposter brugeren har adgang til. Den bestemmer også, hvilke tilladelser (Opret, Læs, Skriv, Slet, Tilføj, Føj til, Tildel eller Del) brugeren har til disse objektposter.

Organisationsenhedsobjektet repræsenterer en firmagruppe eller division, der har bestemte omkostningssatser for medarbejdere, der er tildelt til den. En ressources tilknytning til en organisationsenhed bestemmer ressourcens omkostninger i et projektengagement.

Når du implementerer Dynamics 365, skal du optimere sikkerhedsgodkendelsen for hierarkiet af afdelinger og tildelingen af brugere til afdelinger. Tildel alle brugere, der normalt skal have adgang til det samme sæt poster, til den samme afdeling. Organisationsenheden har ingen indvirkning på sikkerhedstilladelser eller adgang.

#### <a name="example-of-organizational-units-and-business-units"></a>Eksempel på organisationsenheder og afdelinger

Contoso Ltd. har succes med Microsoft-teknologiøvelser. Prakash og Tricia er begge C\#-udviklere, men Tricia er i USA, mens Prakash er i Indien. De fleste projektarrangementer kræver ressourcer fra Contoso Indien og Contoso USA, og Adam og Birgit kræver samme niveau for sikkerhedsadgang til projekter i dette øvelsesområde. Men udgifterne til udviklere fra Contoso Indien adskiller sig betydeligt fra udgifterne til udviklere fra Contoso USA.

Her er en optimal måde at designe dette scenario på i forbindelse med brug af Dynamics 365 og PSA.

1. Opret Microsofts-teknologiøvelse som en afdeling, og knyt den til Prakash og Tricia. På denne måde kan du være med til at sikre, at begge medarbejdere har samme sikkerhedsadgang til alle projekter i det pågældende øvelsesområde. De kan både kontrollere status og rapportere tid, udgifter og opgaveopdateringer. 
2. Opret to organisationsenheder for at få garanti for, at omkostningerne til projektet afspejles korrekt. 
3. Tilknyt Birgit til Contoso USA og Adam til Contoso Indien.
4. Tildel relevante kostprislister til begge organisationsenheder. På denne måde kan du være med til at sikre, at de omkostninger, der er registreret for projektet for Adam og Birgit, afspejler forskellen i omkostningerne mellem Contoso USA og Contoso Indien nøjagtigt.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Er organisationsenheder relateret til salgsdistrikter i Dynamics 365?

Der er ingen tilknytning eller relation mellem salgsdistrikter og organisationsenheder. Et salgsdistrikt er som regel et geografisk område, hvor salget finder sted. Der kan knyttes en salgsprisliste til de enkelte salgsdistrikter.

En organisationsenhed er en intern gruppe eller division i virksomheden, der sporer omkostninger for et sæt roller, som den sælger til andre divisioner eller eksterne kunder.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Eksempel på organisationsenheder og salgsdistrikter

Contoso Ltd. har to udviklingscentre: Contoso USA og Contoso Indien. Omkostninger til ressourcerne er væsentligt forskellige mellem disse to udviklingscentre.

Contoso sælger sine it-servicer på mange internationale markeder, f.eks. Latinamerika, Nordamerika, Asien og Stillehavsområdet, Vesteuropa og Mellemøsten. Fakturasatser for samme projektroller kan variere meget på tværs af disse markeder.

Contoso USA og Contoso Indien skal oprettes som organisationsenheder, og hver enkelt organisationsenhed skal have sin egen kostprisliste. Asien og Stillehavsområdet, Latinamerika, Nordamerika, Vesteuropa og Mellemøsten skal oprettes som salgsdistrikter, og de enkelte salgsdistrikter skal have sin egen salgsprisliste.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Hvorfor er der begrænsning på tilknytning af prislister til organisationsenheder? 

Salgsprisfastsættelse er sædvanligvis entydig for de geografiske områder eller markeder, hvor de pågældende servicer sælges. Interne divisioner i en virksomhed har ikke normalt deres egen salgsprisfastsættelse for den samme type servicer. Interne divisioner har dog forskelligt vareforbrug, afhængigt af færdighederne hos de personer, de har ansat, og arbejdsvilkårene i det område de opererer i. Da organisationsenheder er udformet som interne divisioner i en virksomhed, kan de kun have kostprislister.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Hvorfor kan vi ikke knytte salgsprislister til organisationsenheder?

I PSA kan salgsprislister knyttes til kunder og salgsdistrikter. Transaktionsobjekter som Salgsmulighed, Tilbud, Projektkontrakt og Projekt bruger salgsprislister, som er vedhæftet kundefirmaet eller salgsdistriktet, til at fastlægge fakturasatser og potentiel omsætning for projektengagementet.

Kostprislister er knyttet til organisationsenheder. Transaktionsobjekter som Salgsmulighed, Tilbud, Projektkontrakt og Projekt bruger kostprislister, som er vedhæftet kontraktenheden, til at fastlægge omkostninger for et projektengagement.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Er organisationsenheder hierarkisk opdelt i PSA?

Nej. I den aktuelle version af PSA er organisationsenheder ikke hierarkiske. Det betyder, at du ikke kan:

- Konfigurere et mønster til standardkostpriser, der flyttes op i et hierarki. 
- Rapportere omsætning eller omkostninger, der er akkumuleret på forskellige niveauer i hierarkiet for organisationsenheder.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Vi er et stort multinationalt firma med et komplekst hierarki med flere niveauer af omkostningssteder, divisioner og faktureringssteder. Hvordan kan vi bedst muligt udnytte begrebet organisationsenhed i denne version af Project Service-appen?

Når du har et komplekst hierarki af omkostningssteder, divisioner, faktureringssteder osv., skal du konfigurere bladnoderne for dette hierarki som bestemte organisationsenheder.
Følgende eksempel viser et typisk hierarki:

**ContosoIndien**

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
 
Hvis hierarkiet er det samme, skal du konfigurere det som en komprimeret liste, som vist her:
- Contoso Indien - SAP-øvelse - Tekniske konsulenter 
- Contoso Indien - SAP-øvelse - Funktionelle konsulenter       
- Contoso Indien - Microsoft-teknologiøvelse Funktionelle konsulenter 
- Contoso Indien - Microsoft-teknologiøvelse Funktionelle konsulenter 
- Contoso USA - SAP-øvelse - Tekniske konsulenter  
- Contoso USA - SAP-øvelse - Funktionelle konsulenter  
- Contoso USA - Microsoft-teknologiøvelse - Tekniske konsulenter 
- Contoso USA - Microsoft-teknologiøvelse - Funktionelle konsulenter

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Vi er en lille professionel servicevirksomhed, der udelukkende fungerer som én division. Hvordan kan vi bedst bruge konceptet organisationsenheder i den aktuelle version af PSA?

Hvis virksomheden opererer som én enhed, der har en kostprisliste, behøver du ikke at konfigurere organisationsenheder. Under PSA-installationen opretter Dynamics 365 én standardorganisationsenhed, der har samme navn som organisationen. Alle brugere er som standard tildelt til denne organisationsenhed. Når systemet kræver, at der vælges en organisationsenhed, vælges denne organisationsenhed som standard.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Når et projekt oprettes på baggrund af et tilbud eller en projektkontraktlinje, hentes standardkontraktenheden fra tilbuddet eller projektkontrakten. Hvis et projekt oprettes før salgsobjekter, f.eks. tilbud eller projektkontrakt, hvad er så standardkontraktenheden?

Når et projekt oprettes selvstændigt, er standardkontraktenheden for projektet baseret på den bruger, der opretter den. Denne bruger er også standardprojektleder. Hvis projektet er knyttet til et salgsobjekt, f.eks. et tilbud eller en projektkontrakt, er kontraktenheden for projektet i stedet baseret på salgsobjektet. I dette tilfælde beregnes projektestimater muligvis igen, da kostprislisten bruges til at beregne ændringer i omkostningsestimat, hvis kontraktenheden ændres. Salgsprislisten bruges til at beregne de salgsestimater, der skal ændres, så de er synkroniseret med projektprislisten i tilbuddet.

Felterne **Kontraktenhed** og **Valuta** i projektet er låst mod redigering, da de skal være synkroniseret med værdierne i det salgsobjektet (tilbud eller projektkontrakt), som projektet er knyttet til.


[!INCLUDE[footer-include](../includes/footer-banner.md)]