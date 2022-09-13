---
title: Kopiere projektbaserede kontrakter
description: Denne artikel indeholder oplysninger om kopiering af projektkontrakter i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410313"
---
# <a name="copy-project-based-contracts"></a>Kopiere projektbaserede kontrakter

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Du kan nemt oprette nye projektkontrakter ved at kopiere eksisterende kontrakter på en af to måder:

- Åbn siden med listen **Projektkontrakter**, vælg en projektkontrakt, og vælg derefter **Kopiér**.
- På siden med oplysninger for **Projektkontrakten** skal du vælge **Kopier**.

I begge tilfælde åbnes en dialogboks, hvor du kan vælge parametrene for den kopierede kontrakt. Følgende felter indgår i dialogboksen: Afhængigt af de værdier, du vælger, kan kopiprocessen blive ændret.

| Felt | Beskrivelse | Downstream-virkning |
| --- | --- | --- |
| Emne | Angiv emnet for destinationskontrakten. Når dialogboksen åbnes, angiver systemet dette felt som navnet på kildekontrakten med ordet "kopi" tilføjet. | Dette felt har ingen afledt virkning. |
| Kunde | En reference til kundens firma eller firmapost. Når dialogboksen åbnes, angiver systemet dette felt til kontoen i kildekontrakten. | Dette felt er den primære kunde i kontrakten. |
| Ejende virksomhed | Det firma, der er ansvarlig for leveringen af de projekter, der er knyttet til denne handel. Når dialogboksen åbnes, angiver systemet dette felt til ejerfirmaet i kildekontrakten. | Det firma, der ejer, er den juridiske enhed, der skal udføre projektet, når handlen er lukket. Ejerfirmaets valuta skal matche valutaen for kontraktenheden. |
| Kontraktenhed | Den organisationsenhed, der er ansvarlig for leveringen af de projekter, der er knyttet til denne handel. Når dialogboksen åbnes, angiver systemet dette felt til kontraktenheden i kildekontrakten. | Kontraktenheden er afdelingen i det firma, som skal udføre projekterne, når handlen er indgået. Alle kontraherende enheder har en valuta. Denne valuta bruges til at rapportere forventede og faktiske omkostninger, der påløber under projektet. |
| Valuta | Den valuta, som aftalen handles i. Når dialogboksen åbnes, konfigurerer systemet feltet til valutaen i kildekontrakten. Valutaen kan ændres. Hvis den ændres, angives feltet **Kopiér prisfastsættelse** altid til **Nej**, da prislisterne på kildekontrakten ikke længere er relevante. | Valutaen bruges til standardprislister, til at oprette økonomiske estimater på kontrakten og til at fakturere kunden, når handlen er vundet. |
| Anmodet leveringsdato | Den leveringsdato, som kunden har anmodet om. | Datoen bruges som slutdato, når du opretter faktureringsdatoer med en bestemt hyppighed. |
| Kopiér prisfastsættelse | En værdi indikerer, om prisfastsættelsen i kontrakten skal kopieres fra kildekontrakten. | Hvis feltet er angivet til **Ja**, kopieres referencerne til projektprislisten og produktprislisten fra kildekontrakten til destinationskontrakten. Hvis det er **Nej**, bruges standardprislister på baggrund af de nyeste prislister for kontoen eller projektparametrene. |

Når du vælger **OK** i dialogboksen, opretter systemet en kopi af kontrakten baseret på de parameterværdier, du angiver. Den nye kontrakt åbnes.

Følgende oplysninger kopieres **ikke** fra kildekontrakten til destinationskontrakten, da de er specifikke for de enkelte kontrakter:

- Fakturaplaner
- Kontrakt- og kontraktlinjekunder
- Projektreference på de projektbaserede kontraktlinjer
- Oplysninger om kundebudget

Kontraktlinjer for projekter og produkter, estimater på kontraktlinjedetaljer og maksimale værdier på kontraktniveau kopieres. Angivelse af standardpriser og omkostningssatser afhænger af valget i feltet **Kopiér prisfastsættelse** i dialogboksen **Kopiér parametre**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
