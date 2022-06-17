---
title: Funktionsmåde for brugergrænsefladen for tidsregistrering
description: Denne artikel indeholder oplysninger om adfærden for brugergrænsefladen for tidsregistrering.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b39f182901681875eb90f17d9421bcad63762f54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918167"
---
# <a name="time-entry-ui-behavior"></a>Funktionsmåde for brugergrænsefladen for tidsregistrering

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Gitteret for **Ugentlig tidsregistrering** er et brugerdefineret kontrolelement med to hovedsektioner **Dimensioner** og **Varighed**.

## <a name="keyboard-shortcuts"></a>Tastaturgenveje
| Handling        | Genvej                  |
|------------   |------------------------   |
| Nyt           | Alt + Shift + n           |
| Kopiér række      | Alt + Shift + c           |
| Rediger registrering    | Alt + Shift + e           |
| Rediger række      | Alt + Shift + Ctrl + e    |
| Åbn post    | Alt + Shift + o           |
| Indsend        | Alt + Shift + s           |
| Tilbagekald        | Alt + Shift + r           |
| Delete        | Alt + Shift + d           |
| Kopiér uge     | Alt + Shift + w           |

## <a name="dimensions"></a>Dimensioner
Sektionen **Dimensioner** viser alle de dimensioner, som tid kan registreres i forhold til. Følgende dimensioner understøttes som standard:

  - Project
  - Projektopgave
  - Rolle
  - Skriv
  - Status for registrering

I sektionen **Dimensioner** er det ikke muligt at foretage redigering. Sektionen understøttes af en visning, hvor brugerdefinerede felter kan føjes til det ugentlige tidsregistreringsgitter.

## <a name="duration"></a>Varighed
I sektionen Varighed vises dagene i ugen som kolonneoverskrifter. I denne sektion er det muligt at foretage redigering. Når der er oprettet en tidsregistreringsrække med de rette dimensioner, kan brugere hurtigt angive den tid, de har brugt på disse dimensioner.

## <a name="create-a-new-time-entry"></a>Oprette en ny tidsregistrering

1. I gitteret for tidsregistreringer skal du vælge **Ny**. 
2. I dialogboksen for **Hurtig oprettelse af tidsregistrering** skal du vælge datoen for tidsregistreringen.
3. Angiv data for dimensionerne **Projekt**, **Projektopgave**, **Rolle** og **Varighed**. Disse oplysninger skal tilføjes i minutter, timer eller dage ved at skrive **t**, **m** eller **d** sammen med tallet. 
4. Angiv en beskrivelse af registreringen og eventuelle kommentarer, der kan deles eksternt i forhold til tidsregistreringen. 

Når du gemmer registreringen, vises de angivne værdier i sektionen **Dimensioner**. De oplysninger, som der er angivet i feltet **Varighed**, vises på den dato, som tidsregistreringen blev oprettet for.

Opslagsfelter understøttes af systemvisninger. Når en bruger f.eks. indtaster et projekt, er feltet **Projektopgave** som standard angivet til visningen **Kopiér**. Hvis du vil oprette tidsregistreringer for opgaver, der ikke er tildelt til en bruger, skal du vælge **Skift visning** i opslagsdialogboksen og derefter vælge visningen **Alle aktive projektopgaver**.

## <a name="edit-a-time-entry"></a>Redigere en tidsregistrering 
Detaljer fra visse felter på siden med tidsregistrering, f.eks **Beskrivelse** og **Eksterne kommentarer** vises ikke i det ugentlige tidsregistreringsgitteret. I stedet vises en lille trekantet indikator i celler med **Varighed**, der indeholder disse yderligere detaljer. 

1. Hvis du vil redigere en tidsregistrering, skal du markere den celle, du vil opdatere i tidsregistreringen.
2. Vælg **Rediger detaljer** for at opdatere dataene i ruden **Primær formular for tidsregistrering**. 

## <a name="copy-a-time-entry-row"></a>Kopiere en tidsregistreringsrække
Når rækken er oprettet, kan du vælge **Kopiér række** for at kopiere hele rækken til en ny række. Når en række kopieres på denne måde, kopieres mål og varighed også. Du kan også vælge **Rediger række** for at opdatere målværdier og varigheder i sektionen **Varighed**.

## <a name="open-a-time-entry-behavior"></a>Åbne en tidsregistreringsfunktion
For at understøtte optimal og hurtig indtastning i de mest fremtrædende felter viser det ugentlige tidsregistreringsgitter et undersæt af valgte dimensioner og varigheder for tid. Hvis du vil have vist alle detaljer om en enkelt tidsregistrering, skal du vælge **Åbn** under **Rediger registrering**.

## <a name="submit-a-time-entry"></a>Sende en tidsregistrering
Du kan sende en enkelt tidsregistrering eller en gruppe af tidsregistreringer ved at markere en blok med celler eller en hel tidsregistreringsrække og derefter vælge **Indsend**. Indsendte tidsregistreringer vises som registreringer, der afventer godkendelse, på godkendersiden **Godkendelse**. Når tidsregistreringerne er sendt, kan de ikke redigeres.

## <a name="recall-a-time-entry"></a>Tilbagekalde en tidsregistrering
Du kan tilbagekalde tidsregistreringer, som du har sendt. Du kan tilbagekalde en enkelt tidsregistrering, en blok med tidsregistreringer eller en hel række med tidsregistreringer. Du kan redigere gentagne tidsregistreringer.

## <a name="time-entry-status"></a>Status for tidsregistrering

- **Kladde**: Nye tidsregistreringer får automatisk tildelt statussen **Kladde**. Det er kun tidsregistreringer med statussen **Kladde**, der kan slettes.
- **Indsendt**: Når en tidsregistrering er indsendt, opdateres statussen til **Indsendt**. 
- **Godkendt**: Når en indsendt tidsregistrering godkendes, opdateres statussen til **Godkendt**. 
- **Returneret**: Hvis en tidsregistrering afvises, opdateres statussen til **Returneret**, og registreringen bliver tilgængelig, så den kan rettes og indsendes igen. 

## <a name="view-rejection-comments"></a>Se kommentarer til afvisning
Når en tidsregistrering afvises af en godkender, kan godkenderen tilføje kommentarer, så ressourcen bedre forstår årsagen til afvisningen. Hvis du vil have vist kommentarerne til afslaget for en tidsregistrering, skal du vælge **Åbn post**. Kommentarerne til afvisningen vises på tidslinjen. Brugeren kan svare på kommentarerne til afvisningen, før de indsender registreringen igen.

## <a name="copy-week"></a>Kopiér uge
Når der er oprettet nogle få tidsregistreringer, kan brugerne oprette flere tidsregistreringer på én gang.

1. I formularen **Tidsregistreringer** skal du vælge **Kopiér uge** for at masseoprette flere tidsregistreringer. 
2. I dialogboksen **Kopier** skal du i sektionen **Fra-periode** bruge felterne **Startdato** og **Slutdato** til at definere det datointerval, der skal kopieres tidsregistreringer fra. 
3. I feltet **Startdato** i sektionen **Til periode** skal du angive den dato, der skal oprettes tidsregistreringer for. 
4. Vælg **Kopier**. I forbindelse med den angivne dato i **Til-periode** oprettes der en kopi af tidsregistreringerne for den tilsvarende ugedag i **Fra-perioden**. Tidsregistreringen for mandag i sidste uge kopieres f.eks. til mandag i den uge, der er angivet som **Til-perioden**.

## <a name="import"></a>Importer
Den samme grundlæggende fremgangsmåde bruges til at importere fra reservationer, tildelinger og udvekslinger. Du kan angive datointervallet, som reservationer importeres fra, og derefter eksplicit vælge de reservationer, der skal kopieres som kladde-tidsregistreringer. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
