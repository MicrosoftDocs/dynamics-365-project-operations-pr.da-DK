---
title: Nøglekoncepter i projektkontrakter
description: Dette emne indeholder oplysninger om nøglekoncepterne i projektkontrakter.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 66d6b72b19a90ecc9161cd16ce9d4dd22798803b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074078"
---
# <a name="key-concepts-of-project-contracts"></a>Nøglekoncepter i projektkontrakter

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dette emner indeholder oplysninger om de nøglekoncepter, som du skal være opmærksom på, inden du går i gang med at bruge projektkontrakter i Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Kontraktenhed

Kontraktenheden repræsenterer den division eller praksis, som ejer leveringen af projektet. Du kan konfigurere ressourceomkostninger for de enkelte kontraherende enheder. Når du angiver ressourceomkostningerne for en ressource, kan du også konfigurere forskellige omkostningssatser for ressourcer. Kontraktenhed låner disse ressourcer fra andre afdelinger eller praksisser i selskabet. Omkostningssatserne for ressourcerne kaldes overførselspriser, ressourcelån eller valutapriser. Når du konfigurerer omkostningssatserne for lån af ressourcer fra andre afdelinger, skal du anvende valutaen i udlånsafdelingen.

## <a name="cost-currency"></a>Omkostningsvaluta

Omkostningsvalutaen er den valuta, som omkostninger rapporteres i på skærmen. Denne valuta afledes af den valuta, der er knyttet til feltet **Kontraktenhed** på kontrakten og i projekt. Omkostninger kan logføres i alle valutaer i forhold til et projekt. Der skal dog en valutakonvertering fra den valuta, som omkostningerne blev registreret i og til projektets valuta, når det vises på skærmen.

Da valutakurserne i Common Data Service (CDS)-platformen ikke kan have en ikrafttrædelsesdato, ændres de samlede beløb for omkostninger måske over tid, hvis du opdaterer valutakurserne. De omkostninger, der registreres i databasen, forbliver dog uændrede, fordi beløbene er gemt i den valuta, de blev afholdt i.

## <a name="sales-currency"></a>Salgsvaluta

Salgsvaluta i Project Operations er den valuta, som de estimerede og faktiske salgsbeløb registreres og vises i. Salgsvalutaen er også den valuta, som kunden faktureres i for handlen. I en projektkontrakt bruges standardværdierne for salgsvalutaen fra kunde- eller firmaposten, og de kan ændres, når kontrakten oprettes. Når der oprettes en kontrakt ved at lukke et tilbud som vundet, hentes valutaen i kontrakten fra den valuta, der er angivet i tilbuddet.

Når du opretter en projektkontrakt fra bunden, kan feltet **Salgsvaluta** ikke redigeres. Produkt- og projektprislister er som standard baseret på denne valuta i kontrakten.

I modsætning til omkostninger kan salgsværdier kun registreres i salgsvalutaen.

## <a name="billing-method"></a>Faktureringsmetode

Der er typisk to typer af kontraktmodeller for projekter, nemlig fast gebyr-projekter og forbrugsbaserede. Disse modeller repræsenteres i Project Operations som faktureringsmetoder med to mulige værdier:

- Tid og materiale: En forbrugsbaseret kontraktmodel, hvor de påløbne omkostninger er understøttet af den tilsvarende indtægt. Efterhånden som du estimerer eller afholder flere omkostninger, stiger det tilsvarende estimerede og faktiske salg også. Angiv grænseværdier, der ikke må overskrides, på kontraktlinjer, som har denne faktureringsmetode, hvilket resulterer i, at der fastsættes et loft for den faktiske omsætning. Estimeret omsætning påvirkes ikke af grænser, som ikke må overskrides.
- Fast pris: En kontraktmodel med fast gebyr, der angiver, at salgsværdierne er uafhængige af de omkostninger, der er påløbet. Salgsværdien er fast, og ændres ikke, når du vurderer eller afholder flere omkostninger.

## <a name="project-price-lists"></a>Projektprislister

Projektprislister bruges som standard for priser, ikke omkostningssatser, i relation til tid, udgifter og andre projektrelaterede komponenter. Der kan være flere prislister. Hver enkelt prisliste har sin egen ikrafttrædelsesdato for hver projektkontrakt. Overlappende ikrafttrædelsesdatoer på listerne over projektpriser understøttes ikke i Project Operations.

Når en projektkontrakt oprettes ved at vinde et projekttilbud, kopieres projektprislisterne, inklusive kontraktnavnet og datoen. Kopiering af disse oplysninger udgør brugerdefineret prisfastsættelse for projektkomponenter i denne projektkontrakt.

## <a name="product-price-lists"></a>Produktprislister

Produktprislister bruges som standardpriser og ikke omkostningssatser, for produktbaserede linjer på en kontrakt. Der findes kun én produktsalgsprisliste pr. kontrakt.

## <a name="transaction-classes"></a>Transaktionsklasser

Project Operations understøtter fire typer transaktionsklasser:

- Tid
- Udgift
- Materiale
- Gebyr

Omkostnings- og salgsværdier kan estimeres og afholdes i transaktionsklasserne tid, udgifts og materiale. Gebyr er en transaktionsklasse kun for indtægter.

## <a name="work-entities-and-billing-entities"></a>Arbejdsobjekter og faktureringsobjekter

Objekter, der repræsenterer arbejde, er projekter og opgaver. Objekter, der repræsenterer faktureringsaspekter, er kontraktlinjer. Du kan knytte forskellige arbejdsobjekter til faktureringsindstillinger ved at forbinde dem med kontraktlinjer.

## <a name="multi-customer-deals"></a>Handler med flere kunder

Aftaler med flere kunder har mere end én kunde, som skal faktureres for en handel. Som almindelige eksempler kan nævnes:

- OEM Enterprises og deres partnere: Partnere og forhandlere sælger et produkt med merværdiservicer, som typisk involverer en bestemt handel med en kunde. OEM tilbyder at finansiere en del af projektet. 

- Projekter i den offentlige sektor: Flere afdelinger i de lokale offentlige myndigheder er enige om at finansiere et projekt og faktureres i henhold til en tidligere aftalt opdeling. Et skoledistrikt og de lokale offentlige myndigheder bliver f.eks. enige om at finansiere opførelsen af en svømmehal.

## <a name="invoice-schedules"></a>Fakturaplaner

Fakturaplaner er specifikke for de enkelte kontraktlinjer og er nødvendige, for at automatisk fakturering kan fungere. Fakturaplaner oprettes på baggrund af bestemte start- og slutdatoer og fakturafrekvenser. Planerne bruges i kontraktfasen, når processen for automatisk oprettelse af fakturaer er konfigureret. Når der oprettes en projektkontrakt fra et tilbud, kopieres fakturaplanen til projektkontrakten fra tilbuddet.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Ændringer fra kontrakten i Dynamics 365 Sales

Kontrakter i Project Operations er baseret på kontrakter i Dynamics 365 Sales. Der er dog nogle vigtige afvigelser og forskelle i funktionaliteten, som du skal være opmærksom på:

- Kontrakter i Project Operations har to forskellige typer af linjer, nemlig én for projekter og én for produkter.
- Kontrakter i Project Operations har deres egne formular- og brugergrænsefladeelementer, forretningsregler, forretningslogik i plug-ins og klientbaserede scripts, der adskiller dem fra kontrakter i Sales.

Du bør derfor ikke skiftevis anvende en kontrakt fra Sales og en projektkontrakt.
