---
title: Kopier projektbaserede salgsmuligheder
description: Denne artikel indeholder oplysninger om kopiering af projektbaserede salgsmuligheder i Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cc772391de97f4b2de6e9e29f97a6af4d5514319
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926125"
---
# <a name="copy-project-based-opportunities"></a>Kopier projektbaserede salgsmuligheder

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Det er nemt at kopiere projektbaserede salgsmuligheder, så du kan oprette nye projektbaserede salgsmuligheder. 

1. Gå til listesiden **Projektbaserede salgsmuligheder**, og vælg en salgsmulighed på listen. Du kan også åbne siden med detaljer for en bestemt salgsmulighed. 
2. Vælg **Kopier** på en af siderne. Der vises en dialogboks, som indeholder følgende feltoplysninger. Afhængigt af de valgte værdier i denne dialog kan kopiprocessen blive ændret.

    | **Felt** | **Beskrivelse** | **Downstream-virkning** |
    | --- | --- | --- |
    | Emne | Angiv det relevante emne på destinationssalgsmuligheden. Når dialogboksen åbnes, angiver systemet det som emne for kildesalgsmuligheden med **kopi** tilføjet. | Dette felt har ingen afledt virkning. |
    | Konto | Referencer til kundens firma eller firmapost. Når dialogboksen åbnes, konfigurerer systemet det til kontoen i kildesalgsmuligheden. | Dette felt er den primære kunde i salgsmuligheden. |
    | Kontraktenhed | Den organisationsenhed, der er ansvarlig for leveringen af de projekter, der er knyttet til denne handel. Når dialogboksen åbnes, konfigurerer systemet det til kontraktenheden i kildesalgsmuligheden. | Kontraktenheden er afdelingen i det firma, der udfører projekterne, når handlen er indgået. Alle kontraherende enheder har en valuta, og denne valuta bruges til at rapportere de anslåede og faktiske omkostninger, der er påløbet i løbet af projektet. |
    | Valuta | Den valuta, som aftalen handles i. Når dialogsiden åbnes, konfigurerer systemet det til valutaen i kildesalgsmuligheden. | Valuta bruges til en standardprisliste og til at oprette økonomiske estimater for tilbuddet. Til sidst bruges valutaen til at fakturere kunden, når handlen er indgået. |
    | Kopiér prisfastsættelse | En værdi af typen ja/nej, der angiver, om prisfastsættelsen af salgsmuligheden skal kopieres fra kildesalgsmuligheden. | Hvis **Ja** er markeret, kopieres prislister fra kilden til destinationssalgsmuligheden. Hvis der er valgt **Nej** gendannes standarderne for prislisterne på baggrund af de nyeste prislister, der er konfigureret. |

3. Vælg **OK**. Systemet opretter en kopi af projektsalgsmuligheden på baggrund af de valgte parametre, og den nye projektsalgsmulighed åbnes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]