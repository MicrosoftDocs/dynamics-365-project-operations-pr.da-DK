---
title: Administrer projektprislister i et tilbud
description: Dette emne indeholder oplysninger om objektet Projektprislister.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8cfabf98f1a38823c777b6e388fbbb65d02877e3cd433069dd3845c292f2b277
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003899"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Administrer projektprislister i et tilbud

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations udvider prislisteobjektet i Dynamics 365 Sales. 

## <a name="key-entities"></a>Nøgleobjekter

En prisliste indeholder oplysninger, der leveres af fire forskellige objekter:

- **Prisliste**: Dette objekt indeholder oplysninger om kontekst, valuta, datointerval og tidsenhed for prissætningstiden. Konteksten viser, om prislisten giver udtryk for omkostningssatser eller salgssatser. 
- **Valuta**: Dette objekt lagrer valutaen for priser på prislisten. 
- **Dato**: Dette objekt bruges, når systemet forsøger at angive en standardpris for en transaktion. En prisliste, der indeholder datointervallet, som inkluderer datoen for transaktionen, vælges. Hvis der findes mere end én prisliste, der er gældende for transaktionsdatoen, og som er knyttet til det relaterede tilbud, kontrakten eller organisationsenheden, er der ingen standardpris. 
- **Tid**: Dette objekt lagrer den tidsenhed, som priser udtrykkes for, f.eks. daglige eller timebaserede satser. 

Objektet Prisliste indeholder tre relaterede tabeller, der gemmer priser:

  - **Rollepris**: I denne tabel gemmes en sats for en kombination af værdier for rolle og organisationsenhed, og den bruges til at konfigurere rollebaserede priser for arbejdskraft.
  - **Transaktionskategoripris**: Denne tabel indeholder priser efter transaktionskategori og bruges til at konfigurere priser for udgiftskategorier.
  - **Prislisteelementer**: Denne tabel indeholder priser på katalogprodukter.
 
Prislisten er en satstabel. En satstabel er en kombination af objektet Prisliste og relaterede rækker i tabellerne Rollepris, Transaktionskategoripris og Prislisteelementer.

## <a name="resource-roles"></a>Ressourceroller

Udtrykket *ressourcerolle* refererer til et sæt færdigheder, kompetencer og certificeringer, som en person skal have for at kunne udføre et bestemt sæt opgaver på et projekt.

HR-tid er baseret på den rolle, som en ressource udfylder på et bestemt projekt. I forbindelse med HR-tid, er omkostninger og fakturering baseret på ressourcerolle. Tid kan prissættes i en hvilken som helst enhed i enhedsgruppen **Tid**.

Enhedsgruppen **Tid** oprettes, når du installerer Project Operations. Den har standardenheden **Time**. Du kan ikke slette, omdøbe eller redigere attributterne for enhedsgruppen **Tid** eller enheden **Time**. Men du kan føje andre enheder til enhedsgruppen **Tid**. Hvis du prøver at slette enhedsgruppen **Tid** eller enheden **Time**, kan der opstå fejl i forretningslogikken.
 
## <a name="transaction-categories-and-expense-categories"></a>Transaktionskategorier og udgiftskategorier

Rejser og andre udgifter, som projektkonsulenter påfører, faktureres til kunden. Prisfastsættelse af udgiftskategorier gennemføres ved hjælp af prislister. Flybillet, hotel og billeje er eksempler på udgiftskategorier. De enkelte prislistelinjer for udgifter angiver prissætningen for en bestemt udgiftskategori. Følgende tre metoder bruges til at prisfastsætte udgiftskategorier:

- **Til kostpris**: Udgiftsomkostningerne faktureres til kunden, og der anvendes ingen avance.
- **Avance som procentdel**: Procentdelen over de faktiske omkostninger faktureres til kunden. 
- **Pris pr. enhed**: Der angives en faktureringspris for hver enhed af udgiftskategorien. Det beløb, som kunden faktureres på baggrund af det antal udgiftsenheder, som konsulenten rapporterer. Kørsel bruger prissætningsmetoden pris pr. enhed. Udgiftskategorien for kørsel kan f.eks. konfigureres til 30 amerikanske dollar (USD) pr. dag eller 2 USD pr. mile. Når en konsulent rapporterer kørsel på et projekt, beregnes det beløb, der skal faktureres, på basis af den afstand, som konsulenten har rapporteret.
 
## <a name="project-sales-pricing-and-overrides"></a>Prissætning og tilsidesættelse af projektsalg

I forbindelse med projekttilbud og kontrakter har en projektprisliste et andet mønster for pristilsidesættelse end en produktprisliste. På en produktkatalogbaseret tilbudslinje kan du tilsidesætte prisen på roller og kategorier direkte på tilbudslinjen, da alle tilbudslinjer peger på præcist ét katalogelement. Men på en projektbaseret tilbudslinje kan du dog ikke tilsidesætte prisen for roller og kategorier direkte på tilbudslinjen. Brug projektprislisten til at understøtte de to forskellige tilsidesættelses mønstre.

> [!NOTE]
> Det anbefales, at du har en separat prisliste for projektressourcerne og dine katalogelementer på grund af de funktionsmæssige forskelle mellem de to, når du tilsidesætter prissætningen.

Hvert af følgende objekter kan have en eller flere tilknyttede salgsprislister for projektprissætning:

- Kunde (konto) 
- Salgsmulighed 
- Tilbud 
- Projektkontrakt

Tilknytningen af disse objekter til en prisliste angives af listerne over projektpriser. Du kan knytte en eller flere prislister til salgsobjekterne Kunde, Salgsmulighed, Tilbud og Projektkontrakt.

Der angives ikke automatisk en standardprisliste for projekter på en kundepost. Du kan dog manuelt knytte en liste over projektpriser til kundeposten. Du bør dog kun tilknytte en liste med projektpriser manuelt, hvis du har en bestemt prisaftale med kunden. 

Når en projektprisliste er knyttet til et salgsobjekt, valideres følgende oplysninger:

- Prislisten har konteksten **Salg**. 
- Valutaen for prislisten svarer til kundevalutaen. 

I en projektkontrakt bruges følgende prioriteret rækkefølge til automatisk at angive tilknyttede projektprislister:

1. Tilbud
2. Salgsmulighed
3. Kunde 
4. Globale indstillinger 

Når en projektprisliste angives som standard, validerer systemet, om valutaen stemmer overens med kundens valuta, og at de standardprislister, der er angivet, har en kontekst af **Salg**.

Du kan knytte flere projektprislister til objekterne Kunde, Salgsmulighed, Tilbud og Projektkontrakt. Denne funktion understøtter datospecifikke standardpriser for en længerevarende projektkontrakt, hvor der kan kræves mere end én prisliste for at tage højde for prisopdateringer, der opstår på grund af inflation. Men hvis de prislister, du knytter til kunde-, salgsmuligheds-, tilbuds- eller projektkontraktobjektet, har et overlappende datointerval, kan standardpriserne være forkerte. Du skal derfor sikre dig, at de projektprislister, der har overlappende datointerval, ikke er knyttet til disse objekter.

### <a name="deal-specific-price-overrides"></a>Aftalespecifikke pristilsidesættelser

Du kan oprette aftalespecifikke tilsidesættelser for udvalgte priser på projektprislister, der er angivet som standard i et tilbud eller en projektkontrakt.

Som standard henter en projektkontrakt altid en kopi af mastersalgsprislisten i stedet for et direkte link til den. Denne funktionsmåde hjælper dig med at sikre, at prisaftaler, der er indgået med en kunde for en arbejdserklæring, ikke ændres, hvis masterprislisten ændres.

Det er dog muligt at bruge en masterprisliste i et tilbud. Du kan også kopiere en masterprisliste og redigere den for at oprette en tilpasset prisliste, der kun gælder for dette tilbud. Hvis du vil oprette en ny prisliste, der er specifik for et tilbud, skal du vælge **Opret brugerdefineret prissætning** på siden **Tilbud**. Du kan kun få adgang til den aftalespecifikke projektprisliste fra tilbuddet. 

Når du opretter en tilpasset liste over projektpriser, kopieres kun projektkomponenterne for prislisten. Med andre ord vil en ny prisliste, der er oprettet som en kopi af den eksisterende projektprisliste, der er knyttet til tilbuddet, kun have tilknyttede rollepriser og transaktionskategoripriser.
  
## <a name="tracking-costs"></a>Sporing af omkostninger

Project Operations sporer omkostninger for brugen af HR-tid på projekter. Det sporer også omkostninger for andre udgifter, der er påløbet under projektet, f.eks. rejseudgifter.

Ligesom fakturasatser konfigureres omkostningssatser for HR også ved hjælp af prislister. Her er de væsentligste forskelle i funktionsmåden for kostprislisten og salgsprislisten:

- Omkostningssatsen for en ressource kan ikke tilsidesættes for et bestemt projekt, en bestemt kontrakt eller et bestemt tilbud. Men fakturasatser kan tilsidesættes på aftalebasis, hvis der foretages ændringer, der er specifikke for aftalens karakter. 

- Følgende rækkefølge bruges til at fortolke en kostprisliste:

    1. Den kostprisliste, der er knyttet til afdelingen.
    2. Den kostprisliste, der er knyttet til Project Operations-parametrene. Da kostprislister i mange forskellige valutaer kan knyttes til parametrene, gennemføres der et valutamatch mellem valutaen i kontraktafdelingen for projektet, kontrakten eller tilbuddet og valutaen på kostprislisten .
    3. I forbindelse med udgifter gælder prissætningsmetoderne til kostprisen og avancen ikke for kostprislister. Selvom disse prissætningsmetoder bruges på kostprislistelinjer til at konfigurere omkostninger for transaktionskategorier, ignoreres de i systemet, og der angives ingen standardkostpris.


[!INCLUDE[footer-include](../includes/footer-banner.md)]