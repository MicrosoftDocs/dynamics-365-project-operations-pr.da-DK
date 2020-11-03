---
title: Kopier projektbaserede salgsmuligheder
description: Dette emne indeholder oplysninger om kopiering af projektbaserede salgsmuligheder i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074111"
---
# <a name="copy-project-based-opportunities"></a>Kopier projektbaserede salgsmuligheder

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_


Det er nemt at kopiere projektbaserede salgsmuligheder, så du kan oprette nye projektbaserede salgsmuligheder. 

1. Gå til listesiden **Projektbaserede salgsmuligheder** , og vælg en salgsmulighed på listen. Du kan også åbne siden med detaljer for en bestemt salgsmulighed. 
2. Vælg **Kopier** på en af siderne. Der vises en dialogboks, som indeholder følgende feltoplysninger. Afhængigt af de valgte værdier i denne dialog kan kopiprocessen blive ændret.

    | **Felt** | **Relevans, formål og vejledning** | **Downstream-virkning** |
    | --- | --- | --- |
    | Emne | Angiv det relevante emne på destinationssalgsmuligheden. Når dialogboksen åbnes, angiver systemet det som emne for kildesalgsmuligheden med **kopi** tilføjet. | Dette felt har ingen afledt virkning. |
    | Konto | Referencer til kundens firma eller firmapost. Når dialogboksen åbnes, konfigurerer systemet det til kontoen i kildesalgsmuligheden. | Dette felt er den primære kunde i salgsmuligheden. |
    | Kontraktenhed | Den organisationsenhed, der er ansvarlig for leveringen af de projekter, der er knyttet til denne handel. Når dialogboksen åbnes, konfigurerer systemet det til kontraktenheden i kildesalgsmuligheden. | Kontraktenheden er afdelingen i det firma, der udfører projekterne, når handlen er indgået. Alle kontraherende enheder har en valuta, og denne valuta bruges til at rapportere de anslåede og faktiske omkostninger, der er påløbet i løbet af projektet. |
    | Valuta | Den valuta, som aftalen handles i. Når dialogsiden åbnes, konfigurerer systemet det til valutaen i kildesalgsmuligheden. | Valuta bruges til en standardprisliste og til at oprette økonomiske estimater for tilbuddet. Til sidst bruges valutaen til at fakturere kunden, når handlen er indgået. |
    | Kopiér prisfastsættelse | En værdi af typen ja/nej, der angiver, om prisfastsættelsen af salgsmuligheden skal kopieres fra kildesalgsmuligheden. | Hvis **Ja** er markeret, kopieres prislister fra kilden til destinationssalgsmuligheden. Hvis der er valgt **Nej** gendannes standarderne for prislisterne på baggrund af de nyeste prislister, der er konfigureret. |

3. Vælg **OK**. Systemet opretter en kopi af projektsalgsmuligheden på baggrund af de valgte parametre, og den nye projektsalgsmulighed åbnes.
