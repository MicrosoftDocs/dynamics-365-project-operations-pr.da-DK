---
title: Begreber, der er unikke for projektbaserede tilbud
description: Denne artikel indeholder oplysninger om projekttilbud i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824320"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Begreber, der er unikke for projektbaserede tilbud

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Før du går i gang med at bruge projekttilbud i Microsoft Dynamics 365 Project Operations, skal du være opmærksom på følgende nøglebegreber.

## <a name="owning-company"></a>Ejerselskab

Ejerselskabet repræsenterer den juridiske enhed, der ejer projektleveringen. Kunden i tilbuddet skal være en gyldig kunde i den pågældende juridiske enhed i programmer til finans og drift. Valutaen for ejerselskabet og valutaen for den kontraktenhed, der er valgt i et projektbaseret tilbud, skal være den samme.

## <a name="contracting-unit"></a>Kontraktenhed

En kontraktenhed repræsenterer den afdeling eller praksis, som ejer projektleveringen. Du kan konfigurere ressourceomkostninger for de enkelte kontraherende enheder. Når du angiver ressourceomkostningerne for en ressource i en kontraktenhed, kan du også konfigurere forskellige omkostningssatser for de ressourcer, som kontraktenheden låner fra, eller for andre afdelinger eller praksisser i virksomheden. Disse omkostningssatser kaldes overførselspriser, ressourcelån eller valutapriser. Når du konfigurerer omkostningerne ved at låne ressourcer fra andre afdelinger, kan du oprette omkostningssatserne i valutaen i udlånsafdelingen.

## <a name="cost-currency"></a>Omkostningsvaluta

Omkostningsvalutaen i Project Operations er den valuta, som omkostninger rapporteres i. Denne valuta er afledt af den valuta, der er knyttet til feltet **Kontraktenhed** i tilbuddet, kontrakten og projektet. Omkostninger i forhold til et projekt kan registreres i en hvilken som helst valuta. Men der sker en valutakonvertering fra den valuta, som omkostningerne blev registreret i, til projektets omkostningsvaluta.

Da valutakurser i Dataverse-platformen ikke kan have en ikrafttrædelsesdato, ændres de samlede beløb for omkostninger måske over tid, hvis du opdaterer valutakurserne. De omkostninger, der registreres i databasen, forbliver dog uændrede, fordi beløbene er gemt i den valuta, de blev afholdt i.

## <a name="sales-currency"></a>Salgsvaluta

Salgsvalutaen i Project Operations er den valuta, som de estimerede og faktiske salgsbeløb registreres og vises i. Det er også den valuta, som kunden faktureres i for handlen. For et projekttilbud angives der en standardværdi for salgsvalutaen fra kunde- eller firmaposten, og den kan ændres, når tilbuddet oprettes. Men når tilbuddet er gemt, kan salgsvalutaen ikke ændres. Standardprodukt- og projektprislister angives baseret på tilbuddets salgsvaluta.

I modsætning til omkostninger kan salgsværdier **kun** registreres i salgsvalutaen.

## <a name="billing-method"></a>Faktureringsmetode

Projekter har typisk faste gebyr- og forbrugsbaserede kontraktmodeller. I Project Operations repræsenteres et projekts kontraktmodel ved faktureringsmetoden. Faktureringsmetoden har to værdier: Tid og materiale og Fast pris.

- **Tid og materiale:** – En forbrugsbaseret kontraktmodel, hvor de påløbne omkostninger er understøttet af den tilsvarende indtægt. Efterhånden som du estimerer eller afholder flere omkostninger, stiger det tilsvarende estimerede og faktiske salg også. Du kan angive grænser, som ikke må overskrides, på tilbudslinjer, der har denne faktureringsmetode. På denne måde kan du registrere den faktiske omsætning. Estimeret omsætning påvirkes ikke af grænser, som ikke må overskrides.
- **Fast pris** – En kontraktmodel med fast gebyr, hvor salgsværdier er uafhængige af de omkostninger, der er påløbet. Salgsværdien er fast, og ændres ikke, når du vurderer eller afholder flere omkostninger.

## <a name="project-price-lists"></a>Projektprislister

Projektprislister er prislister, der bruges til at indtaste standardpriser, ikke omkostningssatser, i relation til tid, udgifter og andre projektrelaterede komponenter. Der kan være flere prislister, og de enkelte lister kan have sin egen ikrafttrædelsesdato for hvert projekttilbud. Project Operations understøtter ikke overlappende datointervaller for projektprislister.

## <a name="product-price-lists"></a>Produktprislister

Produktprislister er prislister, der bruges til at indtaste standardpriser, ikke omkostningssatser, for produktbaserede linjer på et tilbud. Der findes kun én produktsalgsprisliste pr. tilbud.

## <a name="transaction-classes"></a>Transaktionsklasser

Project Operations understøtter fire typer transaktionsklasser:

- Tid
- Udgift
- Materiale
- Gebyr

Omkostnings- og salgsværdier kan estimeres og afholdes i transaktionsklasserne **tid**, **udgift** og **materiale**. **Gebyr** er en transaktionsklasse kun for indtægter.

## <a name="work-entities-and-billing-entities"></a>Arbejdsobjekter og faktureringsobjekter

Projekter og opgaver er objekter, der repræsenterer arbejde. Tilbudslinjer og kontraktlinjer er objekter, der repræsenterer fakturering. Du kan knytte forskellige arbejdsobjekter til faktureringsindstillinger ved at knytte dem til tilbudslinjer eller kontraktlinjer.

## <a name="multi-customer-deals"></a>Handler med flere kunder

Aftaler med flere kunder finder sted, når der er mere end én kunde pr. faktura. Her er nogle typiske eksempler:

- **Producenter af originalt udstyr (OEM'er) og deres partnere** – Partnere og forhandlere sælger et produkt, der inkluderer merværdiservice. I forbindelse med en handel med en kunde tilbyder OEM-producenter som regel at finansiere en del af projektet.
- **Projekter i den offentlige sektor** – Flere afdelinger i de lokale offentlige myndigheder er enige om at finansiere et projekt og faktureres i henhold til en tidligere aftalt opdeling. Et skoledistrikt og byen eller den lokale afdeling af de offentlige myndigheder er f.eks. enige om at finansiere opførelsen af en svømmehal.

## <a name="invoice-schedules"></a>Fakturaplaner

Fakturaplaner er specifikke for hver tilbudslinje og er valgfrie. Fakturaplaner oprettes på baggrund af bestemte start- og slutdatoer og en fakturafrekvens. De bruges i kontraktfasen, når processen for automatisk oprettelse af fakturaer er konfigureret. I tilbudsfasen er fakturaplanerne valgfrie. Hvis de oprettes i tilbudsfasen, kopieres de til den projektkontrakt, der oprettes, når et projekttilbud er vundet.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Forskelle fra tilbud i Dynamics 365 Sales

Tilbud i Project Operations er baseret på tilbud i Dynamics 365 Sales. Der er dog nogle vigtige forskelle i funktionaliteten, som du skal være opmærksom på:

- Tilbud i Project Operations har to forskellige typer af linjer: én for projekter og én for produkter.
- Tilbud i Project Operations har deres egne side- og brugergrænsefladeelementer, forretningsregler, forretningslogik i plug-ins og klientbaserede scripts, der adskiller dem fra tilbud i Sales.
- I Sales kan du knytte flere ordrer til et enkelt salgstilbud. I Project Operations kan du kun knytte én projektkontrakt til et projekttilbud.
- Når du vinder et salgstilbud, forbliver den relaterede salgsmulighed muligvis åben. Når et projekttilbud er vundet, lukkes den tilknyttede salgsmulighed.
- Et salgstilbud inkluderer ikke visse felter og begreber, der findes i et projekttilbud. Felterne omfatter **Kontraktenhed**, **Account Manager** og **Kontaktnavn for fakturering**.
- Salgs- og projekttilbud identificeres af feltet **Type**, der er baseret på grupperede indstillinger. I forbindelse med et salgstilbud er værdien dette felt **Elementbaseret**. I forbindelse med et projekttilbud er værdien **Arbejdsbaseret**.

På grund af disse forskelle anbefaler vi, at du ikke skifter mellem at bruge tilbud i Sales og tilbud i Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
