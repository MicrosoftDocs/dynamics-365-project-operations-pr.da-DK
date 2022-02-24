---
title: Registrer materialeforbrug på projekter og projektopgaver
description: Dette emne giver oplysninger om, hvordan materialeforbrug logføres i forhold til projekter og projektopgaver.
author: rumant
manager: AnnBe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab431ce4c18a4283cd887de9afcba0dd556d2567
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852842"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Registrer materialeforbrug på projekter og projektopgaver

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Når et projektteam arbejder sig igennem opgaver på et projekt, forbruger de eller anvender materiale. En logfil over materialeforbrug kan bruges til at registrere dette brug, så det kan godkendes af projektlederen og faktureres kunden. 

Benyt følgende fremgangsmåde for at registrere anvendelsen af katalogmaterialer eller materialer, der skal rekvireres, og indsende dem til godkenderen: 

1. Vælg **Materialeforbrug** i navigationsruden, og vælg derefter **Ny**.
2. På siden **Nyt materialeforbrug** skal du angive oplysningerne om det krævede materialeforbrug og derefter vælge **Gem**.

Følgende tabel giver oplysninger om felterne på siden **Logfil for materialeforbrug**. 

| **Felt** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- |
| Beskrivelse | En beskrivelse af det specifikke materialeforbrug. | Dette felt har ingen afledt virkning. |
| Dato | Den dato, hvor materialet forventes at blive brugt. | Dette felt har ingen afledt virkning. |
| Project | En liste over aktive projekter. | Hvis du vælger et projekt til en materialeforbrugslog, påvirkes feltet **Opgave**, så der kun vises de opgaver, som er på projektet. |
| Opgave | En liste over opgaver i projektet, herunder hoved- og bladnodeopgaver. | Hvis du vælger en opgave til en materialeforbrugslog, påvirkes de faktiske materialeomkostninger og det faktiske materialesalg for en opgave. Hvis dette felt er tomt, spores og opsummeres de tilsvarende omkostninger og salg i materialeforbrug kun på projektniveau. |
| Vælg produkt | Angiv, om dette materialebrug gælder for et **Eksisterende** (katalog)produkt eller et produkt, der skal **Rekvireres**. | Dette felt bestemmer produkttypen. |
| Produkt | Id'et for produktet fra produktkataloget. Når du vælger et produkt-id, opdateres feltet **Vælg produkt** automatisk til **Eksisterende produkt**. Id'et bruges til at hente omkostnings- og salgspriser fra prislisten. | Dette felt har ingen afledt virkning. |
| Beskrivelse af produkt, der skal rekvireres | Et tekstfelt, som produktnavnet skal skrives i. Dette felt er tilgængeligt, når du et produkt, der skal **Rekvireres**, i feltet **Vælg produkt**.| Dette felt har ingen afledt virkning. |
| Reserverbar ressource| Ressource, der brugte dette materiale på projektet. Standarden for dette felt er den ressource, der kan reserveres, for den bruger, der er logget på, men kan ændres, således at brug kan registreres på vegne af andre medlemmer af projektteamet. | Dette felt har ingen afledt virkning. |
| Enhedsgruppe | Standardværdien i dette felt kommer fra den enhedsgruppe, der er konfigureret som standardværdi for katalogproduktet. Du kan opdatere dette felt for at vælge en anden enhedsgruppe. | Dette felt har ingen afledt virkning. |
| Enhed | Standardværdien i dette felt er standardenheden for det valgte produkt. Du kan opdatere dette felt for at vælge en anden enhed. | Hvis du ændrer enheden, resulterer det i en anden standardenhedspris og -omkostning. |
| Antal | Den mængde af produktet, der er blevet brugt på projektet eller projektopgaven. | Dette felt har ingen afledt virkning. |
| Enhedsomkostning | Enhedsomkostningen for det valgte produkt og den valgte enheds kombination som angivet på den relevante kostprisliste. | Enhedsomkostningen vises altid i projektets omkostningsvaluta. Hvis der ikke er nogen enhedsomkostninger for kombinationsproduktet og enheden på prislisten, angives enhedsomkostningen som standard til 0,00. |
| Samlet omkostning | Det omkostningsbeløb, der beregnes som mængde \* enhedsomkostning.| Omkostningsbeløbet vises altid i projektets omkostningsvaluta. |


## <a name="submit-material-usage-for-review-and-approval"></a>Indsend materialeforbrug til gennemgang og godkendelse 
Når du har registreret alt dit materialeforbrug, og du er klar til at få det godkendt, skal du indsende oplysninger om brugen til gennemsyn.

1. Gå til **Logfil for materialeforbrug**, og vælg en eller flere poster. Du kan også markere alle materialeforbrugsposter ved hjælp af afkrydsningsfeltet i overskriften.
2. Vælg **Send**. De valgte poster behandles i systemet, og der oprettes derefter anmodninger om godkendelse af materialeforbrug.

## <a name="recall-a-material-usage-log"></a>Tilbagekald en logfil for materialeforbrug

Du kan efter behov tilbagekalde et indsendt materialeforbrug. Den tid, der skal bruges på tilbagekalde en materialeforbrugspost, afhænger af godkendelsesfasen.  Hvis godkenderen endnu ikke har godkendt posten, kan tilbagekaldelsen ske med det samme. Men hvis posten allerede er godkendt, bliver godkenderen bedt om at godkende tilbagekaldelsen og tilbageføre transaktionerne.

1. Gå til **Materialeforbrug**, og vælg det materialeforbrug, som skal tilbagekaldes, på listen over materialeforbrugslogfiler.
2. Vælg **Tilbagekalde**. Hvis materialeforbrugsposten endnu ikke er blevet godkendt, tilbagekalder systemet det med det samme. Hvis materialeposten allerede er blevet godkendt, oprettes der en anmodning om tilbagekaldelse for at give godkenderen besked om, at du ønsker at tilbagekalde materialeforbruget. Godkenderen bekræfter derefter, at tilbageførslen kan udføres, og posten bliver returneret.

## <a name="delete-a-material-usage-log"></a>Slet en logfil for materialeforbrug

Du kan slette materialeforbrugslogfiler, der ikke er indsendt. Hvis du vil slette en materialeforbrugslog, der allerede er blevet indsendt, skal den først tilbagekaldes.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
