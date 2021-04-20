---
title: Administrer projektprislister i projektkontrakter
description: Dette emne indeholder oplysninger om administration af projektprislister i projektkontrakter.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffc48782394995781535ae56142dc76afeb9a040
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858556"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Administrer projektprislister i projektkontrakter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Projektkontrakter i Dynamics 365 Project Operations er udviklet til at understøtte salgsprislister med flere ikrafttrædelsesdatoer på en kontrakt. I Project Operations er der et nyt tilknyttet objekt, som kaldes **Projektprislister**. Dette objekt har en en-til-mange-relation til en projektkontrakt.

Projektprislister bruges til at prisfastsætte tids-, materiale- og udgiftstransaktioner på et projekt. Når en kontrakt indeholder en eller flere projektprislister, bruges disse prislister til at prisfastsætte tids-, materiale-, omkostningsestimater samt faktiske værdier på projekter, der er knyttet til kontrakten via kontraktlinjen.

Når der ikke findes projektprislister på en projektkontrakt, får du vist en advarsel om, at der ikke findes nogen projektprislister, og dine estimater, det faktiske projektarbejde, materialer og udgifter logføres uden at blive prisfastsat. Der kan ikke beregnes priser for salgsværdier.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Tilknyt eller fjern tilknytningen for en projektprisliste i en projektkontrakt

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Opret eller tilknyt en bestemt prisliste til estimering af projektbaseret arbejde, materiale og udgifter

1. Vælg fanen **Projektprislister** i projektkontrakten.
2. Vælg **+ Tilføj ny projektprisliste** i undergitteret.
3. I skyderen **Hurtig oprettelse** skal du vælge en prisliste. 

  Rullelisten viser alle de prislister, hvor konteksten er angivet til **Salg**, og hvor valutaen på prislisten stemmer overens med valutaen i kontrakten.
  
4. Angiv en beskrivelse af projektprislistetilknytningen, vælg **Gem**, og luk derefter skyderen til **Hurtig oprettelse**.

   Der oprettes en projektprislistetilknytning.
   
5. Gentag trin 1-4, hvis du vil knytte mere end projektprisliste til projektkontrakten. Du skal kun oprette flere projektprislister, hvis du har forskellige ikrafttrædelsesdatoer for hver af de tilknyttede projektprislister.

> [!NOTE]
> Project Operations understøtter ikke overlappende ikrafttrædelsesdatoer for projektprislisterne. Hvis en transaktion har flere projektprislister med en bestemt dato, angives prisværdien på den pågældende transaktion til nul.

### <a name="remove-a-project-price-list-association"></a>Slet en tilknyttet projektprisliste

- Vælg projektprislisten, og vælg derefter **Slet kontraktens projektprisliste** i undergitteret. 

  Prislisten fjernes fra kontraktens projektprislister. Selve prislisten slettes ikke. Det er kun tilknytningen til kontrakten, der slettes.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Konfigurer automatisk angivelse af projektprislister i en kontrakt

En projektprisliste kan konfigureres som standardprislisten for projektet. Denne konfiguration sikrer, at alle kontrakter i din organisation altid starter med en standardprisliste for projekter for den pågældende prisperiode.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Konfigurer organisationens standard for projektprislister

1. Gå til **Indstillinger** > **Generelt** og vælge derefter **Parametre**.
2. På listesiden **Aktive parametre** skal du vælge og dobbeltklikke på posten for at åbne den. Mens du dobbeltklikker, skal du sørge for, at du ikke klikker på en feltværdi med et hyperlink. 
3. På siden **Aktive parametre** skal du vælge fanen **Prisliste**. Et undergitter med en liste over standardprislisterne vises. Dette er en liste over standardlister for omkostnings- og salgspriser. Ved at tilknytte en prisliste for **Salg** her for alle valutaer, som du sælger i, sikrer du, at salgsprislisten anvendes som standard for en hvilken som helst kontrakt, som du opretter for kunder, der handler i denne valuta.

### <a name="set-up-a-customer-specific-project-price-list"></a>Konfigurer en kundespecifik projektprisliste

Du kan også konfigurere kundespecifikke projektprislister, når du har forhandlet en overordnet aftale om prisfastsættelse med dine kunder.

1. Gå til **Salg** > **Kunder**.
2. Vælg den kunde, der har en special prisliste, på listen over aktive konti.
3. Vælg den kundepost, der skal åbnes, og vælg derefter fanen **Projektprislister** . Et undergitter med en liste over projektprislister, der er specifikke for denne kunde, vises. 
4. Opret en ny prislistetilknytning her for at angive en specifik projektprisliste for denne kunde.

## <a name="custom-pricing-on-a-project-contract"></a>Brugerdefineret prisfastsættelse på en projektkontrakt

Når du har standard organisations- og kundespecifikke projektprislister, oprettes dine projektkontrakter automatisk med disse projektprislister tilknyttet. Projektprislister i en projektkontrakt kopieres dog altid med den dato og det kontraktnavn, de er tilføjet med. Account managere og projektlederne kan derefter begynde at redigere priserne på disse kopier. Disse ændrede priser gælder kun for denne projektkontrakt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]