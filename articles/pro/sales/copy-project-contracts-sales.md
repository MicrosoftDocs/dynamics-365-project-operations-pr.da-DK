---
title: Kopiering af projektkontrakter
description: Dette emne indeholder oplysninger om kopiering af projektkontrakter i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074077"
---
# <a name="copying-project-contracts"></a>Kopiering af projektkontrakter

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Du kan nemt oprette nye projektkontrakter ved at oprette kopier af eksisterende kontrakter på en af to måder: 

  - Åbn siden med listen **Projektkontrakter** , vælg en projektkontrakt, og vælg derefter **Kopier**.
  - På siden med oplysninger for **Projektkontrakten** skal du vælge **Kopier**.

Der åbnes en dialogside, hvor du kan vælge parametrene for den kopierede kontrakt. Følgende felter indgår i dialogen: Afhængigt af de værdier, som du har valgt i denne dialog, kan kopiprocessen blive ændret.

| **Felt** | **Relevans, formål og vejledning** | **Downstream-virkning** |
| --- | --- | --- |
| Emne | Angiv emnet for destinationskontrakten. Når dialogsiden åbnes, angiver systemet dette felt som navnet på kildekontrakten med **kopi** tilføjet. | Dette felt har ingen afledt virkning. |
| Kunde | Reference til kundens firma eller firmapost. Når dialogboksen åbnes, konfigurerer systemet dette felt til kontoen i kildekontrakten. | Dette felt er den primære kunde i kontrakten. |
| Kontraktenhed | Den organisationsenhed, der er ansvarlig for leveringen af de projekter, der er knyttet til denne handel. Når dialogsiden åbnes, konfigurerer systemet det til kontraktenheden i kildekontrakten. | Kontraktenheden er afdelingen i det firma, som skal udføre projekterne, når handlen er indgået. Alle kontraherende enheder har en valuta. Denne valuta bruges til at rapportere forventede og faktiske omkostninger, der påløber under projektet. |
| Valuta | Den valuta, som aftalen handles i. Når dialogsiden åbnes, konfigurerer systemet feltet til valutaen i kildekontrakten. Valutaen kan ændres. Hvis den ændres, angives feltet **Kopier prisfastsættelse** altid til **Nej** , da prislisterne på kildekontrakten ikke længere er relevante. | Valuta bruges til standardprislister, til at oprette økonomiske estimater på kontrakten og til at fakturere kunden, når aftalen er i hus. |
| Anmodet leveringsdato | Den leveringsdato, som kunden har anmodet om. | Datoen bruges som slutdato, når du opretter faktureringsdatoer sammen med en bestemt hyppighed. |
| Kopiér prisfastsættelse | Indikerer, om prisfastsættelsen i kontrakten skal kopieres fra kildekontrakten. | Hvis feltet er angivet til **Ja** , kopieres referencerne til projektprislisten og produktprislisten fra kildekontrakten til destinationskontrakten. Hvis der er valgt **Nej** , konverterer prislisterne tilbage til standarderne for kontoen eller projektparametrene. |

Når du vælger **OK** på dialogsiden, opretter systemet en kopi af kontrakten baseret på de valgte parametre. Den nye kontrakt åbnes.

Følgende oplysninger kopieres ikke fra **Kilde** til **Destinationskontrakt** :

  - Fakturaplaner
  - Kontrakt- og kontraktlinjekunder
  - Projektreference på de projektbaserede kontraktlinjer
  - Oplysninger om kundebudget

Da disse oplysninger er specifikke for hver kontrakt, kopieres disse felter og poster ikke. Kontraktlinjer for projekter og produkter, estimeringer på kontraktlinjedetaljer og maksimale værdier på kontraktniveau kopieres. Konvertering til standardværdierne for pris- og omkostningssatser afhænger af det foretagne valg i feltet **Kopier prisfastsættelse** på dialogsiden **Kopier parametre**.
