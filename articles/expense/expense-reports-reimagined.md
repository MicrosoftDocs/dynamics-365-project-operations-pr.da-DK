---
title: Nydesignede udgiftsrapporter (indeholder video)
description: Dette emne beskriver den nydesignede og genskabte oplevelse af indtastning af udgiftsrapporter.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db5812ebf5a96afee53144efb231093f6af85b68
ms.sourcegitcommit: 1186e9822e06a13fde89b67ea89427eddfe23cee
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2021
ms.locfileid: "7941024"
---
# <a name="expense-reports-reimagined"></a>Nye udgiftsrapporter

Registreringer i udgiftsrapporten er blevet ændret for at forenkle processen og reducere den tid, det tager at fuldføre en rapport. Her er de væsentligste komponenter i den nye udgiftsoplevelse:

- Et nyt arbejdsområde til udgiftsstyring, som giver dig mulighed for at få adgang til din stedfortræders udgifter.
- En ny oplevelse, der matcher kvittering for at forbedre visningen af kvitteringer på overskriftsniveau og forenkle processen med tilknytning af kvitteringer til udgiftslinjer.
- Et nyt skrivebeskyttet gitter, der giver dig mulighed for at få vist mange flere udgiftslinjer og andre kolonner med data. Du kan nu se alle specificerede og opdelte linjer sammen med deres overordnede udgifter.
- En forenklet rude til redigering af udgifter.
- Nydesignede meddelelser for fejl, advarsler og politikker for at give den korrekte kontekst og forståelse for problemet, og hvordan det løses. Vi har fjernet nogle af de meddelelser, der blev vist, før brugerne kunne udføre deres opgaver og løse problemerne.
- En ny side til angivelse af obligatoriske felter, valgfrie felter og de felter, der ikke skal inkluderes. På denne side kan du reducere antallet af felter, der skal angives.
- Et nyt udseende for udgiftsrapporter, så rapporterne ikke længere ser ud, som om de er designet til regnskabspersonalet.

Hvis du vil slå den nye oplevelse til, skal du bruge arbejdsområdet **Funktionsadministration** til at slå funktionen til for **Nyt arbejdsområde for udgiftsrapporter**. Når du aktiverer denne funktion, udføres følgende handlinger:

- Det eksisterende arbejdsområde for udgifter erstattes med det nye arbejdsområde.
- Der tilføjes et nyt menupunkt for synligheden af udgiftsfeltet.
- Der fjernes ingen eksisterende menuelementer til udgiftsrapporter (den eksisterende side) eller udgiftsrapportfelter.
- Arbejdsprocesser og eventuelle godkendelser fører dig stadig til siden med den eksisterende udgiftsrapport.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Nye egenskaber

| Ny funktion | Beskrivelse |
|---|----|
| Synlighed for udgiftsfelt | På en ny konfigurationsside kan du angive, hvilke felter der skal deaktiveres for en organisation. Du kan også angive, hvilke felter der skal være obligatoriske, og hvilke felter der anbefales. |
| Obligatoriske felter | Med den nye simple konfiguration kan du gøre nogle af felterne obligatoriske, uden at du skal bruge politikstrukturen. |
| Valgfrie felter | Der tilføjes endnu en side i forbindelse med valgfrie felter. På denne måde vil medarbejderne ikke opfatte det, som om de skal angive felterne, men der er stadig adgang til felterne. |
| Tilføj ikke-tilknyttede kvitteringer | Muligheden for at tilføje ikke-tilknyttede kvitteringer til udgiftsrapport er mere synlig i arbejdsområdet og i udgiftsrapporten. |
| Forbedrede beskeder | Der er bedre synlighed i udgiftslinjer, som indeholder advarsler eller fejl. |
| Reduktion af meddelelser i meddelelseslinjen| Antallet af infolog-meddelelser blev formindsket, og der blev gjort et forsøg på at forhindre, at der vises dubletter i mange tilfælde. |
| Fælles grupperede almindelige handlinger | Grænsefladen blev ryddet op med tilføjelsen af en ny handlingsknap for de fleste fælles handlinger på linjeniveau og tilføjelsen af en ellipseknap (...) for overskrifter og andre mindre hyppige handlinger. |
| Nyt arbejdsområde for at øge synligheden | Et nyt arbejdsområde forener funktioner og links, og gør det muligt for brugere at flytte til forskellige områder. |
| Tilføj eksisterende udgifter og kvitteringer under oprettelse af udgifter | Når du opretter udgiftsrapporter, kan du tilføje alle udgifter eller vælge ikke-tilknyttede udgifter. Ikke-tilknyttede udgifter er udgifter, der er importeret fra firmaets kreditkortudskrift, eller udgifter, der er oprettet manuelt af brugeren, men som ikke er knyttet til en udgiftsrapport.|
| Beregning af valutakurs | Der tilføjes en beregner til valutakurs, som giver dig mulighed for at beregne valutakursen for transaktioner med udlæg med flere valutaer. |
| Gem og tilføj nye udgiftslinjer | Knapperne **Gem** og **Ny** er tilgængelige, når der angives nye udgifter, så du hurtigt kan angive udgiftslinjer. |
| Bedre synlighed til opdelte og specificerede linjer | De specificerede og opdelte linjer tilføjes direkte til listen over udgifter for at øge synligheden og hjælpe dig med hurtigt at finde ud af, om der er opstået fejl. |
| Få vist detaljer om underkategorier i specificerede linjer | Specificerede linjer i en overordnet udgift viser underkategorietiketterne i udgiftsrapporten. Med opdelingen kan du hurtigt gennemse de specifikke detaljer.|
|Specificér hurtigt tilbagevendende udgifter | I det nydesignede arbejdsområde for udgifter kan du hurtigt specificere tilbagevendende udgifter ved at tilføje underkategorien, startdatoen og mængden. Mængden henviser til antal gange, som beløbet gentages over en løbende periode. |
| Vis kvitteringer under specifikation | Kvitteringer kan vises under specifikation. |
| Valg af kontaktforskud | Vælg en eller flere kontantforskud for at gennemføre en enkelt udgiftstransaktion. |
| Kontantforskudssaldi | Gennemse saldoen for kontantforskud i realtid, når du opretter en udgiftspost, i forhold til godkendte og betalte kontantforskud. |

Den første version er fokuseret på scenarier med udgiftsposter. Et scenarie med gennemgang eller godkendelse af en udgiftsrapport vil fortsat bruge den eksisterende udgiftsregistreringsside.


Følgende funktioner understøttes ikke i det nye arbejdsområde for udgiftsrapporter, men de er planlagt til nye versioner: 

- Rejserekvisitionsintegration
- Udgiftsregistrering pr. dag
- Understøttelse af midlertidig godkender
- Mulighed for at få vist historik over arbejdsprocesser


[!INCLUDE[footer-include](../includes/footer-banner.md)]
