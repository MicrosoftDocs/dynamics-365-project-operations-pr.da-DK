---
title: Kopier projektbaserede tilbud
description: Dette emne indeholder oplysninger om, hvordan du kopierer projektbaserede tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1ce6c2b644319f2d822010a34c57c591f82edc9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278141"
---
# <a name="copy-project-based-quotes"></a>Kopier projektbaserede tilbud

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan nemt oprette et nyt projekttilbud ved at kopiere et eksisterende. 

- Hvis du vil kopiere et projekttilbud, skal du på listesiden **Projekttilbud** eller detaljesiden **Projekttilbud** vælge det projekttilbud, du vil kopiere og derefter vælge **Kopiér**.

Derved åbnes en dialogside, hvor du kan angive parametrene for kopien. I følgende tabel kan du se de felter, der er tilgængelige på dialogsiden. Afhængigt af de værdier, du vælger, kan kopiprocessen blive ændret.

| **Felt** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- |
| Emne | Angiv det relevante emne eller navn på destinationstilbuddet. Når dialogboksen åbnes, angiver systemet det som emne for kildetilbuddet med **kopi** tilføjet. | |
| Kundeemne | Reference til kundens firma eller firmapost. Når dialogboksen åbnes, konfigurerer systemet det til kontoen i kildetilbuddet. | Dette felt er den primære kunde i tilbuddet. |
| Kontraktenhed | Den organisationsenhed, der er ansvarlig for leveringen af de projekter, der er knyttet til denne handel.
Når dialogboksen åbnes, konfigurerer systemet det til kontraktenheden i kildetilbuddet. | Kontraktenheden er afdelingen i det firma, der skal udføre projekterne, når handlen er indgået. Alle kontraherende enheder har en valuta. Valutaen bruges til at rapportere forventede og faktiske omkostninger, der påløber under udførelsen af projektet. |
| Valuta | Det er den valuta, som aftalen handles i. Når dialogboksen åbnes, konfigurerer systemet det til valutaen i kildetilbuddet. Denne kan redigeres, og hvis den ændres, angives feltet **Kopier prisfastsættelse** altid til **Nej**. Dette skyldes, at prislisterne i kildetilbuddet ikke længere er relevante. | Valuta bruges til at standardisere en prisliste for at oprette et økonomisk estimat for tilbuddet og til sidst at fakturere kunden, når aftalen er i hus. |
| Anmodet leveringsdato | Det er den leveringsdato, kunden har anmodet om. | Datoen bruges som slutdato, når der oprettes faktureringsdatoer sammen med en bestemt hyppighed. |
| Kopiér prisfastsættelse | Værdien Ja/Nej indikerer, om prisfastsættelsen i tilbuddet skal kopieres fra kildetilbuddet. | Hvis **Ja** er markeret, kopieres referencerne til projektprislisten og produktprislisterne fra kildetilbuddet til destinationstilbuddet. Hvis der er valgt **Nej** gendannes standarderne for prislisterne på baggrund af de nyeste prislister, der er konfigureret i firma- eller projektparametrene. |

Når du vælger **OK** på dialogsiden, opretter systemet en kopi af projekttilbuddet baseret på de parametre, der er valgt i dialogboksen. Det nye projekttilbud åbnes. 

> [!NOTE]
> Følgende oplysninger kopieres ikke fra kilde- til destinationstilbuddet:
>
> - Fakturaplaner
> - Tilbud og tilbudslinjekunder
> - Projektreference på de projektbaserede tilbudslinjer – oplysninger om kundebudget
>
>Da disse oplysninger er meget specifikke for hvert enkelt tilbud, kopieres disse felter og poster ikke. Tilbudslinjer for projekter og produkter, estimater på tilbudslinjedetaljer og maksimale værdier på tilbudsniveau kopieres. Standardværdierne for pris- og omkostningssats afhænger af den valgte indstilling for **Kopier prisfastsætte** på dialogsiden **Kopier parametre**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]