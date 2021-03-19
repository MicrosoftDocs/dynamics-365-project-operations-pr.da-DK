---
title: Tilbud - nøglekoncepter – lille
description: Dette emne indeholder oplysninger om, hvordan du bruger projekttilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 63d9fc56f47c3bb7c5477af8f3bfa1be11a09a45
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272381"
---
# <a name="quotes---key-concepts---lite"></a>Tilbud - nøglekoncepter – lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Følgende er de vigtigste koncepter, som du skal være opmærksom på, før du går i gang med at bruge projekttilbud i Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Kontraktenhed

Kontraktenheden repræsenterer den division eller praksis, som ejer projektleveringen. Du kan konfigurere ressourceomkostninger for de enkelte kontraherende enheder. Når du angiver ressourceomkostningerne for en ressource i den kontraherende enhed, kan du også konfigurere forskellige omkostningssatser for de ressourcer, som kontraktenheden låner fra, eller andre afdelinger eller praksis i virksomheden. Disse kaldes overførselspriser, ressourcelån eller valutapriser. Når du konfigurerer omkostningerne ved at låne ressourcer fra andre divisioner, kan du også vælge at oprette disse omkostningssatser i valutaen i udlånsdivisionen.

## <a name="cost-currency"></a>Omkostningsvaluta

Omkostningsvalutaen i Project Operations er den valuta, som omkostninger rapporteres i. Denne valuta afledes af den valuta, der er knyttet til feltet **Kontraktenhed** på tilbud, kontrakt og projekt. Omkostninger kan logføres i alle valutaer i forhold til et projekt. Men valutaomregningen fra valutabeløbene blev registreret i projektets omkostningsvaluta.

Da valutakurserne i CDS-platformen ikke kan have en ikrafttrædelsesdato, ændres de samlede beløb for omkostninger måske over tid, hvis du opdaterer valutakurserne. De omkostninger, der registreres i databasen, forbliver dog uændrede, fordi beløbene er gemt i den valuta, de blev afholdt i.

## <a name="sales-currency"></a>Salgsvaluta

Salgsvaluta i Project Operations er den valuta, som de estimerede og faktiske salgsbeløb registreres og vises i. Det er også den valuta, som kunden faktureres i for handlen. I et projekttilbud bruges standardværdierne for salgsvalutaen fra kunde- eller firmaposten, og de kan ændres, når tilbuddet oprettes. Når tilbuddet er gemt, kan salgsvalutaen ikke ændres. Produkt- og projektprislister er som standard baseret på tilbuddets salgsvaluta.

I modsætning til omkostninger kan salgsværdier kun registreres i salgsvalutaen.

## <a name="billing-method"></a>Faktureringsmetode

Projekter har typisk faste gebyr- og forbrugsbaserede kontraktmodeller. Dette repræsenteres i Project Operations som **Faktureringsmetode** og har to værdier i form af tid og materiale samt fast pris.

- **Tid og materiale:** Dette er en forbrugsbaseret kontraktmodel, hvor de påløbne omkostninger er understøttet af den tilsvarende indtægt. Efterhånden som du estimerer eller afholder flere omkostninger, vil det tilsvarende estimerede og faktiske salg også stige. Du kan angive grænser, som ikke må overskrides, på tilbudslinjer, der har denne faktureringsmetode. Derved maksimeres den faktiske omsætning. Estimeret omsætning påvirkes ikke af grænser, som ikke må overskrides.
- **Fast pris:** Dette er en kontraktmodel med fast gebyr, der angiver, at salgsværdierne er uafhængige af de omkostninger, der er påløbet. Salgsværdien er fast, og ændres ikke, når du vurderer eller afholder flere omkostninger.

## <a name="project-price-lists"></a>Projektprislister

Projektprislister er prislister, der bruges som standard for priser, ikke omkostningssatser, i relation til tid, udgifter og andre projektrelaterede komponenter. Der kan være flere prislister, og de enkelte lister kan have sin egen ikrafttrædelsesdato for hvert projekttilbud. Overlappende ikrafttrædelsesdatoer på listerne over projektpriser understøttes ikke i Project Operations.

## <a name="product-price-lists"></a>Produktprislister

Produktprislister er prislister, der bruges som standardpriser og ikke omkostningssatser, for produktbaserede linjer på et tilbud. Der findes kun én produktsalgsprisliste pr. tilbud.

## <a name="transaction-classes"></a>Transaktionsklasser

Project Operations understøtter fire typer transaktionsklasser:

- Tid
- Udgift
- Materiale
- Gebyr

Omkostnings- og salgsværdier kan estimeres og afholdes i transaktionsklasserne tid, udgifts og materiale. Gebyr er en transaktionsklasse kun for indtægter.

## <a name="work-entities-and-billing-entities"></a>Arbejdsobjekter og faktureringsobjekter

Objekter, der repræsenterer arbejde, er projekter og opgaver. Objekter, der repræsenterer fakturering, er tilbudslinjer og kontraktlinjer. Du kan knytte forskellige arbejdsobjekter til faktureringsindstillinger ved at knytte dem til tilbud eller kontraktlinjer.

## <a name="multi-customer-deals"></a>Handler med flere kunder

Aftaler med flere kunder finder sted, når der er mere end én kunde, som skal faktureres. Almindelige eksempler herpå omfatter:

- **OEM-virksomheder og deres partnere:** Partnere og forhandlere sælger et produkt med merværdiservice. Dette er som regel et scenarie, hvor OEM-producenten tilbyder at finansiere en del af projektet i forbindelse med en bestemt handel med en kunde. 

- **Projekter i den offentlige sektor:** Flere afdelinger i de lokale offentlige myndigheder er enige om at finansiere et projekt og faktureres i henhold til en tidligere aftalt opdeling. Et skoledistrikt og byen eller den lokale afdeling af de offentlige myndigheder er f.eks. enige om at finansiere opførelsen af en svømmehal.

## <a name="invoice-schedules"></a>Fakturaplaner

Fakturaplaner er specifikke for hver tilbudslinje og er også valgfrie. Fakturaplaner oprettes på baggrund af bestemte start- og slutdatoer og fakturafrekvenser. Fakturaplaner bruges i kontraktfasen, når processen for automatisk oprettelse af fakturaer er konfigureret. I tilbudsfasen er planerne valgfrie. Når der oprettes fakturaplaner i fasen **Tilbud**, kopieres de til den projektkontrakt, der oprettes, når et projekttilbud er vundet.

## <a name="changes-from-dynamics-365-sales-quote"></a>Ændringer fra tilbud i Dynamics 365 Sales:

Tilbud i Project Operations er baseret på tilbud i Dynamics 365 Sales. Der er dog nogle vigtige forskelle i funktionaliteten, som du skal være opmærksom på:

- Handlingerne **Revider** og **Aktiver** understøttes ikke.
- Tilbud i Project Operations indeholder to forskellige typer linjer. Den ene er til projekter, og den anden er til produkter.
- Tilbud i Project Operations har deres egne formular- og brugergrænsefladeelementer, forretningsregler, forretningslogik i plug-ins og klientbaserede scripts, der adskiller dem fra tilbud i Sales.

Af disse årsager anbefales det ikke at skiftevis bruge et tilbud fra Sales og et tilbud fra Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]