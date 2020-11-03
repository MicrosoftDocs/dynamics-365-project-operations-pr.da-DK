---
title: Nye udgiftsrapporter
description: Dette emne indeholder oplysninger om det nye design og nyudviklede oplevelse med registrering i udgiftsrapporter.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 47c1bce0c886897b295a3c1a355f4db843c4b73a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074238"
---
# <a name="expense-reports-reimagined"></a>Nye udgiftsrapporter

Registreringer i udgiftsrapporten er blevet ændret for at forenkle processen og reducere den tid, det tager at fuldføre en rapport. Her er de væsentligste komponenter i den nye udgiftsoplevelse:

- Et nyt arbejdsområde til udgiftsstyring, som giver dig mulighed for at få adgang til din stedfortræders udgifter.
- En ny oplevelse, der matcher kvittering for at forbedre visningen af kvitteringer på overskriftsniveau og forenkle processen med tilknytning af kvitteringer til udgiftslinjer.
- Et nyt skrivebeskyttet gitter, som du kan bruge til at få vist mange flere udgiftslinjer og flere kolonner med data. Du kan nu se alle specificerede og opdelte linjer sammen med deres overordnede udgifter.
- En forenklet rude til redigering af udgifter.
- Nydesignede meddelelser for fejl, advarsler og politikker for at give den korrekte kontekst og forståelse for problemet, og hvordan det løses. Vi har fjernet nogle af de meddelelser, der blev vist, før brugerne kunne udføre deres opgaver og løse problemerne.
- En ny side til angivelse af obligatoriske felter, valgfrie felter og de felter, der ikke skal inkluderes. På denne side kan du reducere antallet af felter, der skal angives.
- Et nyt udseende for udgiftsrapporter, så rapporterne ikke længere ser ud, som om de er designet til regnskabspersonalet.

Hvis du vil slå den nye oplevelse til, skal du bruge arbejdsområdet **Funktionsstyring** til at aktivere funktionen **Nyt design af udgiftsrapporter**. Når du aktiverer denne funktion, udføres følgende handlinger:

- Det eksisterende arbejdsområde for udgifter erstattes med det nye arbejdsområde.
- Der tilføjes et nyt menupunkt for synligheden af udgiftsfeltet.
- Der fjernes ingen eksisterende menuelementer til udgiftsrapporter (den eksisterende side) eller udgiftsrapportfelter.
- Arbejdsprocesser og eventuelle godkendelser fører dig stadig til siden med den eksisterende udgiftsrapport.

## <a name="getting-started-video-for-new-users"></a>Introduktionsvideo til nye brugere

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Videoen [Udgiftsoplevelsen i Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (vist ovenfor) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

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
| Bedre synlighed til opdelte og specificerede linjer | De specificerede og opdelte linjer tilføjes direkte til listen over udgifter for at øge synligheden og hjælpe dig med hurtigt at finde ud af, om der er opstået fejl. |
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
