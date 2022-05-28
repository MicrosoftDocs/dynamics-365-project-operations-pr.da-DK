---
title: Arbejd med projektbaserede kontraktlinjer
description: Dette emne indeholder oplysninger om projektbaserede kontraktlinjer.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f67c0447c0b2a23d6f7d03dfc5ac7800943bbf36
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595169"
---
# <a name="work-with-projectbased-contract-lines"></a>Arbejd med projektbaserede kontraktlinjer

Projektbaserede kontraktlinjer i Dynamics 365 Project Operations er designet til at rumme estimat- og faktureringsaftaler for specifikke komponenter i projektarbejde på en aftale. Strukturen i en projektbaseret kontraktlinje udvides for projektestimater og faktureringsscenarier med følgende koncepter:

- Faktureringsmetode
- Projekt- og opgavetilknytning
- Inkluderede transaktionsklasser
- Grænse, der ikke må overskrides
- Opsætning af fakturerbarhed
- Estimater ved hjælp af kontraktlinjedetaljer
- Kontraktlinjekunder

Der findes følgende felter under fanen **Generelt** på projektbaserede kontraktlinjer. Disse felter hjælper dig med at konfigurere grundlaget for et detaljeret, grundlæggende estimat og faktureringsordninger for projektbaseret arbejde.

| Felt | Beskrivelse | Downstream-virkning |
| --- | --- | --- |
| **Navn** | Navnet på den kontraktlinje, der identificerer den diskrete komponent i kontrakten, der skal estimeres. I en projektkontrakt, der er oprettet ud fra et tilbud, kopieres denne værdi fra en tilsvarende værdi for den projektbaserede tilbudslinje. | Værdien i feltet kopieres til den projektfakturalinje, der oprettes fra denne kontraktlinje, når fakturaen oprettes. |
| **Faktureringsmetode** | På en projektkontrakt, der er oprettet ud fra et tilbud, kopieres denne værdi fra det tilsvarende felt på tilbudslinjen. Dette er en grupperet indstilling, der repræsenterer de to primære kontraktmodeller, som understøttes af Project Operations:</br>- **Fast pris**</br>- **Tid og materiale** | Den faktiske transaktion behandles på grundlag af faktureringsmetoden for den kontrakt, der henvises til. Hvis den kontraktlinje, der henvises til af den faktiske værdi, har en faktureringsmetode for tid og materialer, oprettes der en post for omkostninger og ikke-faktureret faktisk salgsværdi. Hvis den kontraktlinje, der henvises til af den faktiske værdi, har en faktureringsmetode for fast pris, oprettes der kun en faktisk omkostningsværdi. |
| **Project** | Brug dette felt til at identificere det projekt, der skal bruges til at levere arbejdet på denne aftale. | Værdien i dette felt bruges sammen med felterne **Inkluderede opgaver** og **Inkluderede transaktionsklasser** til at fortolke kontraktlinjereferencen på en post for en faktisk værdi eller en estimatlinje. |
| **Medtag tid** | Et flag angiver, om tidstransaktioner eller arbejdsomkostninger på det valgte projekt medtages på denne kontraktlinje. En værdi angivet til **Nej** medfører, at tidstransaktionerne og arbejdsomkostningerne ikke medtages på denne kontraktlinje. Hvis værdien **Ja** er angivet, betyder det, at de bliver medtaget. | Denne feltværdi bruges sammen med projektet til at fortolke kontraktlinjereferencen på en faktisk værdipost eller en estimatlinjepost. |
| **Medtag udgift** | Et flag angiver, om udgiftsomkostninger på det valgte projekt medtages på denne kontraktlinje. En værdi angivet til **Nej** medfører, at udgiftsomkostningen ikke medtages på denne kontraktlinje. Hvis værdien **Ja** er angivet, betyder det, at den bliver medtaget. | Denne feltværdi bruges sammen med projektet til at fortolke kontraktlinjereferencen på en faktisk værdipost eller en estimatlinjepost. |
| **Medtag gebyr** | Et flag angiver, om gebyrer på det valgte projekt medtages på denne kontraktlinje. En værdi angivet til **Nej** medfører, at gebyrerne ikke medtages på denne kontraktlinje. Hvis værdien **Ja** er angivet, betyder det, at de bliver medtaget. | Denne feltværdi bruges sammen med projektet til at fortolke kontraktlinjereferencen på en faktisk værdipost eller en estimatlinjepost. |
| **Kontraktbeløb** | På en kontraktlinje med fast pris er dette den aftalte værdi, der skal faktureres kunden for alle de arbejdskomponenter, der er knyttet til kontraktlinjen. På en kontraktlinje med tid og materialer er dette beløb en estimeret værdi for det, der skal faktureres kunden for alle de arbejdskomponenter, der er knyttet til kontraktlinjen. På en projektkontrakt, som er oprettet ud fra et tilbud, kopieres denne værdi fra det tilsvarende felt på tilbudslinjen. Når en projektbaseret kontraktlinje indeholder linjeoplysninger, er dette felt låst mod redigering og opsummeres i på grundlag af beløbet i kontraktlinjeoplysningerne. | Når kontraktlinjen indeholder linjeoplysninger, kan denne værdi ændres ved at ændre beløbene på linjedetaljerne. På en kontraktlinje med fast pris bruges denne værdi til at oprette beløbet før moms på periodiske faktureringsmilepæle. |
| **Anslået moms** | Brugeren kan redigere dette felt for at angive det estimerede momsbeløb på kontraktlinjen. Når en projektbaseret kontraktlinje indeholder linjeoplysninger, er dette felt låst mod redigering og opsummeres i på grundlag af momsbeløbet i kontraktlinjeoplysningerne. | Når kontraktlinjen indeholder linjeoplysninger, kan denne værdi ændres ved at ændre momsbeløbene på linjedetaljerne. På en kontraktlinje med fast pris bruges denne værdi til at oprette moms på periodiske faktureringsmilepæle. |
| **Kontraktbeløb efter moms** | Beløbet på kontraktlinjen efter moms. Dette felt er skrivebeskyttet og beregnes som **Kontraktbeløb + moms**. | På en kontraktlinje med fast pris bruges denne værdi til at oprette periodiske faktureringsmilepæle. |
| **Grænse, der ikke må overskrides** | Brugeren kan redigere dette felt, og det er kun tilgængeligt for projektbaserede kontraktlinjer, der har faktureringsmetoden tid og materialer. | Brugeren kan redigere dette felt. Når en faktisk værdi for tid eller udgift refererer til denne kontraktlinje for tid og materiale, evalueres beløbet på den faktiske værdi i forhold til grænsen, der ikke må overskrides, på denne kontraktlinje efter, at der er taget højde for de allerede brugte og tilpligtede beløb. |
| **Kundebudget** | Dette felt kan redigeres og kopieres fra det tilsvarende felt på tilbudslinjen, hvis kontrakten er blevet oprettet på grundlag af et tilbud. | Dette felt bruges kun til orientering, og det har ingen afledede virkninger. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Valideringsregel for indstillingerne under fanen Generelt på projektbaserede kontraktlinjer

Regel: Et projekt og en bestemt transaktionsklasse kan kun inkluderes på én projektbaseret kontraktlinje i en kontrakt.

| Kontrakt | Kontraktlinje | Project | Medtag tid | Medtag udgift | Medtag gebyr | Gyldig/ikke gyldig | Årsag                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Overtræder reglen. Tid, udgifter og gebyrer på projekt P1 findes på både kontraktlinjer, CL1 og CL2.                                                                                       |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Overtræder reglen. Tid, udgifter og gebyrer på projekt P1 findes på både kontraktlinjer, CL1 og CL2.                                                                                       |
| C1       | CL1           | P1      | Ja          | Nr.              | Ja         | Ikke gyldig       | Overtræder reglen. Tid og gebyrer på projekt P1 findes på både kontraktlinjer, CL1 og CL2.                                                                                                   |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Overtræder reglen. Tid og gebyrer på projekt P1 findes på både kontraktlinjer, CL1 og CL2.                                                                                                   |
| C1       | CL1           | P1      | Ja          | Nr.              | Ja         | Gyldig           | Tid og gebyrer på projekt P1 er inkluderet i CL1. Udgift til projekt P1 er inkluderet i CL2. </br>   Der findes ingen overlapning i det, der medtages på hver kontraktlinje, og den er derfor gyldig.  |
| C1       | CL2           | P1      | Nr.           | Ja             | Nr.          | Gyldig           | Tid og gebyrer på projekt P1 er inkluderet i CL1. Udgift til projekt P1 er inkluderet i CL2. </br>   Der findes ingen overlapning i det, der medtages på hver kontraktlinje, og den er derfor gyldig.  |
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Overtræder reglen. Tid, udgifter og gebyrer på projekt P1 findes på linjerne i to kontrakter.                                                                                               |
| CL2      | CL2           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Overtræder reglen. Tid, udgifter og gebyrer på projekt P1 findes på linjerne i to kontrakter.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]