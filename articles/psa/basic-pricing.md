---
title: Projektprissætning
description: Denne emne indeholder oplysninger om, hvordan prissætning fungerer i Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: b319f9be9fd72ac99ce6012b6baffde812e3077d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074369"
---
# <a name="project-pricing"></a>Projektprissætning 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation udvider prislisteobjektet i Dynamics 365 Sales. 

## <a name="key-entities"></a>Nøgleobjekter

En prisliste indeholder oplysninger, der leveres af fire forskellige objekter:

- **Prisliste** – Dette objekt indeholder oplysninger om kontekst, valuta, datointerval og tidsenhed for prissætningstiden. Konteksten viser, om prislisten udtrykker omkostningssatser eller salgssatser. 
- **Valuta** – Dette objekt lagrer valutaen for priser på prislisten. 
- **Dato** – Dette objekt bruges, når systemet forsøger at angive en standardpris for en transaktion. PSA-prissætning vælger den prisliste, der indeholder datointervallet, som inkluderer datoen for transaktionen. Hvis PSA-prissætningen finder mere end én prisliste, der er gældende for transaktionsdatoen, og som er knyttet til det relaterede tilbud, kontrakten eller organisationsenheden, er der ingen standardpris. 
- **Tid** – Dette objekt lagrer den tidsenhed, som priser udtrykkes for, f.eks. daglige eller timebaserede satser. 

Objektet Prisliste indeholder tre relaterede tabeller, der gemmer priser:

  - **Rollepris** – I denne tabel gemmes en sats for en kombination af værdier for rolle og organisationsenhed, og den bruges til at konfigurere rollebaserede priser for arbejdskraft.
  - **Transaktionskategoripris** – Denne tabel indeholder priser efter transaktionskategori og bruges til at konfigurere priser for udgiftskategorier.
  - **Prislisteelementer** – Denne tabel indeholder priser på katalogprodukter.

> ![Konfiguration af priser ved hjælp af en prisliste](media/basic-guide-12.png)
 
Prislisten er en satstabel. En satstabel er en kombination af objektet Prisliste og relaterede rækker i tabellerne Rollepris, Transaktionskategoripris og Prislisteelementer.

## <a name="resource-roles"></a>Ressourceroller

Udtrykket *ressourcerolle* refererer til et sæt færdigheder, kompetencer og certificeringer, som en person skal have for at kunne udføre et bestemt sæt opgaver på et projekt.

HR-tid er normalt baseret på den rolle, som en ressource udfylder på et bestemt projekt. I forbindelse med HR-tid understøtter PSA efterkalkulation og fakturering, der er baseret på ressourcerollen. Tid kan prissættes i en hvilken som helst enhed i enhedsgruppen **Tid**.

**Tid** -enhedsgruppen oprettes, når PSA installeres. Den har standardenheden **Time**. Du kan ikke slette, omdøbe eller redigere attributterne for enhedsgruppen **Tid** eller enheden **Time**. Men du kan føje andre enheder til enhedsgruppen **Tid**. Hvis du prøver at slette enhedsgruppen **Tid** eller enheden **Time** , kan der opstå fejl i PSA-forretningslogikken.

> ![Konfiguration af priser efter rolle](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Transaktionskategorier og udgiftskategorier

Rejser og andre udgifter, som projektkonsulenter påfører, faktureres normalt til kunden. PSA understøtter prissætning af udgiftskategorier ved hjælp af prislister. Flybillet, hotel og billeje er eksempler på udgiftskategorier. De enkelte prislistelinjer for udgifter angiver prissætningen for en bestemt udgiftskategori. I forbindelse med prissætning af udgiftskategorier understøtter PSA følgende tre prissætningsmetoder:

- **Til kostpris** – Udgiftsomkostningerne faktureres til kunden, og der anvendes ingen avance.
- **Avance som procentdel** – Procentdelen over de faktiske omkostninger faktureres til kunden. 
- **Pris pr. enhed** – Der angives en faktureringspris for hver enhed af udgiftskategorien. Det beløb, som kunden faktureres på baggrund af det antal udgiftsenheder, som konsulenten rapporterer. Kørsel bruger prissætningsmetoden pris pr. enhed. Udgiftskategorien for kørsel kan f.eks. konfigureres til 30 amerikanske dollar (USD) pr. dag eller 2 USD pr. mile. Når en konsulent rapporterer kørsel på et projekt, beregnes det beløb, der skal faktureres, på basis af den afstand, som konsulenten har rapporteret.

> ![Konfiguration af prissætning for udgiftskategorier](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Prissætning og tilsidesættelse af projektsalg

I forbindelse med projekttilbud og kontrakter har en projektprisliste et andet mønster for pristilsidesættelse end en produktprisliste. På en produktkatalogbaseret tilbudslinje kan du tilsidesætte prisen på roller og kategorier direkte på tilbudslinjen, da alle tilbudslinjer peger på præcist ét katalogelement. Men på en projektbaseret tilbudslinje kan du dog ikke tilsidesætte prisen for roller og kategorier direkte på tilbudslinjen. For at understøtte de to forskellige tilsidesættelsesmønstre har PSA introduceret en ny prislistetilknytning, som er listen over projektpriser.

> [!NOTE]
> Det anbefales, at du har en separat prisliste for projektressourcerne og dine katalogelementer på grund af de funktionsmæssige forskelle mellem de to, når du tilsidesætter prissætningen.

Hvert af følgende objekter kan have en eller flere tilknyttede salgsprislister for projektprissætning:

- Kunde (konto) 
- Salgsmulighed 
- Tilbud 
- Projektkontrakt

Tilknytningen af disse objekter til en prisliste angives af listerne over projektpriser. Du kan knytte en eller flere prislister til salgsobjekterne Kunde, Salgsmulighed, Tilbud og Projektkontrakt.

Der angives ikke automatisk en standardprisliste for projekter på en kundepost. Du kan dog manuelt knytte en liste over projektpriser til kundeposten. Du bør dog kun tilknytte en liste med projektpriser manuelt, hvis du har en bestemt prisaftale med kunden. 

Når en projektprisliste er knyttet til et salgsobjekt, validerer PSA følgende oplysninger:

- Prislisten har konteksten **Salg**. 
- Valutaen for prislisten svarer til kundevalutaen. 

I en projektkontrakt bruger PSA følgende prioriteret rækkefølge til automatisk at angive tilknyttede projektprislister:

1. Tilbud
2. Salgsmulighed
3. Kunde 
4. Globale indstillinger for PSA

Når en projektprisliste angives som standard, validerer PSA, om valutaen stemmer overens med kundens valuta, og at de standardprislister, der er angivet, har en kontekst af **Salg**.

Du kan knytte flere projektprislister til objekterne Kunde, Salgsmulighed, Tilbud og Projektkontrakt. Denne funktion understøtter datospecifikke standardpriser for en længerevarende projektkontrakt, hvor der kan kræves mere end én prisliste for at tage højde for prisopdateringer, der opstår på grund af inflation. Men hvis de prislister, du knytter til kunde-, salgsmuligheds-, tilbuds- eller projektkontraktobjektet, har et overlappende datointerval, kan standardpriserne være forkerte. Du skal derfor sikre dig, at de projektprislister, der har overlappende datointerval, ikke er knyttet til disse objekter.

### <a name="deal-specific-price-overrides"></a>Aftalespecifikke pristilsidesættelser

I PSA kan du oprette aftalespecifikke tilsidesættelser for udvalgte priser på projektprislister, der er angivet som standard i et tilbud eller en projektkontrakt.

Som standard henter en projektkontrakt altid en kopi af mastersalgsprislisten i stedet for et direkte link til den. Denne funktionsmåde hjælper dig med at sikre, at prisaftaler, der er indgået med en kunde for en arbejdserklæring, ikke ændres, hvis masterprislisten ændres.

Det er dog muligt at bruge en masterprisliste i et tilbud. Du kan også kopiere en masterprisliste og redigere den for at oprette en tilpasset prisliste, der kun gælder for dette tilbud. Hvis du vil oprette en ny prisliste, der er specifik for et tilbud, skal du vælge **Opret brugerdefineret prissætning** på siden **Tilbud**. Du kan kun få adgang til den aftalespecifikke projektprisliste fra tilbuddet. 

Når du opretter en tilpasset liste over projektpriser, kopieres kun projektkomponenterne for prislisten. Med andre ord vil en ny prisliste, der er oprettet som en kopi af den eksisterende projektprisliste, der er knyttet til tilbuddet, kun have tilknyttede rollepriser og transaktionskategoripriser.

> ![Visning og konfiguration af tilpasset prissætning for en projektkontrakt](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Sporing af omkostninger

PSA sporer omkostninger for brugen af HR-tid på projekter. Det sporer også omkostninger for andre udgifter, der er påløbet under projektet, f.eks. rejseudgifter.

Ligesom fakturasatser konfigureres omkostningssatser for HR også ved hjælp af prislister. Her er de væsentligste forskelle i funktionsmåden for kostprislisten og salgsprislisten:

- Omkostningssatsen for en ressource kan ikke tilsidesættes for et bestemt projekt, en bestemt kontrakt eller et bestemt tilbud. Men fakturasatser kan tilsidesættes på aftalebasis, hvis der foretages ændringer, der er specifikke for aftalens karakter. 

- Følgende rækkefølge bruges til at fortolke en kostprisliste:

    1. Den kostprisliste, der er knyttet til afdelingen.
    2. Den kostprisliste, der er knyttet til projektstyringsparametre. Da kostprislister i mange forskellige valutaer kan knyttes til projektstyringsparametre, sker der et PSA-valutamatch mellem valutaen i kontraktafdelingen for projektet, kontrakten eller tilbuddet og valutaen på kostprislisten .
    3. I forbindelse med udgifter gælder prissætningsmetoderne til kostprisen og avancen ikke for kostprislister. Selvom disse prissætningsmetoder bruges på kostprislistelinjer til at konfigurere omkostninger for transaktionskategorier, ignoreres de i systemet, og der angives ingen standardkostpris.
