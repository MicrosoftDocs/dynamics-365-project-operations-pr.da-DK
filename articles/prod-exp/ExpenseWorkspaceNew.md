---
title: Nydesignede udgiftsrapporter
description: Dette emne indeholder oplysninger om det nye design og nyudviklede oplevelse med registrering i udgiftsrapporter.
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: bd334d3404e9baae4f8314173834d9fbb708d574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993680"
---
# <a name="redesigned-expense-reports"></a>Nydesignede udgiftsrapporter

Indtastning i udgiftsrapporten er blevet ændret for at forenkle processen med at færdiggøre udgiftsrapporter og reducere den krævede tid. Her er de væsentligste komponenter i den nye udgiftsoplevelse:

- Et nyt arbejdsområde til udgiftsstyring, som giver dig mulighed for at få adgang til din stedfortræders udgifter.
- En ny oplevelse, der matcher kvittering for at forbedre visningen af kvitteringer på overskriftsniveau og forenkle processen med tilknytning af kvitteringer til udgiftslinjer.
- Et nyt skrivebeskyttet gitter, som du kan bruge til at få vist mange flere udgiftslinjer og flere kolonner med data. Du kan nu se alle specificerede og opdelte linjer sammen med deres overordnede udgifter.
- En forenklet rude til redigering af udgifter.
- Nydesignede meddelelser for fejl, advarsler og politikker skal hjælpe med at sikre, at du får den korrekte kontekst, så du forstår, hvad problemet er, og hvordan det løses. Microsoft har fjernet mange af de meddelelser, der blev vist, før brugerne fik mulighed for at fuldføre sine opgaver og løse problemerne, f.eks. meddelelsen om ufuldstændig specifikation.
- En ny side til angivelse af, hvilke felter din organisation kræver, hvilke felter der er valgfrie, og hvilke felter der ikke skal registreres. Denne side vil hjælpe med at reducere antallet af felter, som brugeren skal angive.
- Et nyt udseende for udgiftsrapporter, så rapporterne ikke længere ser ud, som om de er designet til regnskabspersonalet.

Hvis du vil slå den nye oplevelse til, skal du bruge arbejdsområdet **Funktionsstyring** til at aktivere funktionen **Nydesignede udgiftsrapporter**. Når du aktiverer denne funktion, udføres følgende handlinger:

- Det eksisterende arbejdsområde for udgifter erstattes med det nye arbejdsområde.
- Der tilføjes et nyt menupunkt for synligheden af udgiftsfeltet.
- Der fjernes ingen eksisterende menuelementer til udgiftsrapporter (den eksisterende side) eller udgiftsrapportfelter.
- Arbejdsprocesser og eventuelle godkendelser fører dig stadig til siden med den eksisterende udgiftsrapport.

## <a name="new-features"></a>Nye egenskaber

| Ny funktion | Beskrivelse |
|---|----|
| Synlighed for udgiftsfelt | Du kan bruge en ny konfigurationsside til at angive, hvilke felter der skal deaktiveres i en organisation, hvilke felter der skal være obligatoriske, og hvilke felter der skal anbefales. |
| Obligatoriske felter | Med den nye simple konfiguration kan du gøre nogle af felterne obligatoriske, uden at du skal bruge politikstrukturen. |
| Valgfrie felter | Der tilføjes endnu en side i forbindelse med valgfrie felter. På denne måde vil medarbejderne ikke opfatte det, som om de skal angive felterne, men der er stadig adgang til felterne. |
| Tilføj ikke-tilknyttede kvitteringer | Muligheden for at tilføje ikke-tilknyttede kvitteringer til udgiftsrapport er mere synlig i arbejdsområdet og i udgiftsrapporten. |
| Forbedrede beskeder | Der er bedre synlighed i udgiftslinjer, som indeholder advarsler eller fejl. |
| Reduktion af meddelelser i meddelelseslinjen| Antallet af infolog-meddelelser blev formindsket, og der blev gjort et forsøg på at forhindre, at der vises dubletter i mange tilfælde. |
| Fælles grupperede almindelige handlinger | Grænsefladen blev ryddet op med tilføjelsen af en ny handlingsknap for de fleste fælles handlinger på linjeniveau og tilføjelsen af en ellipseknap (...) for overskrifter og andre mindre hyppige handlinger. |
| Nyt arbejdsområde for at øge synligheden | Et nyt arbejdsområde forener funktioner og links, og gør det muligt for brugere at flytte til forskellige områder. |
| Tilføj eksisterende udgifter og kvitteringer under oprettelse af udgifter | Når du opretter udgiftsrapporter, kan du tilføje alle eller udvalgte udgifter og kvitteringer. |
| Beregning af valutakurs | Der tilføjes en beregner til valutakurs, som giver dig mulighed for at beregne valutakursen for transaktioner med udlæg med flere valutaer. |
| Gem og tilføj nye udgiftslinjer | Knapperne **Gem** og **Ny** er tilgængelige, når der angives nye udgifter, så du hurtigt kan angive udgiftslinjer. |
| Bedre synlighed til opdelte og specificerede linjer | De specificerede og opdelte linjer tilføjes direkte til listen over udgifter for at øge synligheden og hjælpe dig med hurtigt at finde ud af, om der er opstået politikfejl eller andre fejl. |
| Vis kvitteringer under specifikation | Kvitteringer kan vises under specifikation. |

Den første version er fokuseret på scenarier med udgiftsposter. Et scenarie med gennemgang eller godkendelse af en udgiftsrapport vil fortsat bruge den eksisterende udgiftsregistreringsside.

Følgende funktioner findes på den eksisterende side, men er endnu ikke til stede på den nye side. Disse funktioner genindføres over de næste kommende frigivelser:

- Godkendelser
- Godkendelse af kreditorer og muligheden for at redigere regnskabet
- Flere registreringspunkter
- Rejserekvisitionsintegration
- Dataobjekt for udgiftsfeltets synlighed
- Registrering af diætudgifter
- Arbejdsproces på linjeniveau
- Understøttelse af midlertidig godkender
- Avanceret specificering


[!INCLUDE[footer-include](../includes/footer-banner.md)]