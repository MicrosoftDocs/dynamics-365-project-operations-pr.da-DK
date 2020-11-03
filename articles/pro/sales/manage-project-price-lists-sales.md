---
title: Administrer projektprislister i projekttilbud
description: Dette emne indeholder oplysninger om at arbejde med projektprislister på tilbud. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074095"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Administrer projektprislister i projekttilbud (Sales)

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Projekttilbud er udviklet for at understøtte flere salgsprislister med gældende datoer. Med Dynamics 365 Project Operations tilføjes der et nyt tilknyttet objekt, der kaldes **Projektprislister**. Dette objekt har en 1-til-mange-relation til et projekttilbud.

Projektprislister bruges til at prisfastsætte tids- og udgiftstransaktioner på et projekt. Når et tilbud indeholder en eller flere projektprislister, bruges disse prislister til at prisfastsætte tids- og udgiftsestimater og faktiske værdier på projekter, der er knyttet til tilbuddet, via tilbudslinjen.

Når der ikke er nogen projektprislister på et projekttilbud, vises der en advarsel. Meddelelsen angiver, at idet der ikke er nogen projektprislister, vil dit estimerede og faktiske projektarbejde og udgifter ikke vil være prisfastsat. I stedet har de prisen nul (0) for salgsværdier.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Tilknyt eller ophæv tilknytningen af en projektprisliste i et projekttilbud

Hvis du vil oprette eller vælge en bestemt prisliste til estimering af projektbaseret arbejde og udgifter, skal du udføre følgende trin.

1. På tilbuddet skal du vælge fanen **Projektpris** og i undergitteret vælge **+ Tilføj ny projektprisliste**.
2. Vælg en prisliste på siden med hurtig oprettelse. På rullelisten vises alle de prislister, hvor konteksten er angivet til **Salg** , og valutaen stemmer overens med valutaen i tilbuddet.
4. Angiv en beskrivelse af projektprislistetilknytningen, og vælg **Gem og luk**.

Der oprettes en projektprislistetilknytning.

Du kan gentage denne fremgangsmåde, hvis du har brug for at tilknytte mere end én liste med projektpriser til projekttilbuddet. Du kan kun oprette flere projektprislister, hvis du har forskellige ikrafttrædelsesdatoer for hver af de tilknyttede projektprislister.

> [!NOTE]
> Project Operations understøtter ikke overlappende ikrafttrædelsesdato på listerne over projektpriser. Hvis der er flere projektprislister for en transaktion med en bestemt dato, angives prisen for den transaktioner som standard til nul (0).
Hvis du vil fjerne en tilknytning til en projektprisliste, skal du vælge projektprislisten og derefter vælge **Slet tilbudsprojektprisliste**. Prislisten flyttes fra tilbuddets projektprislister, men selve prislisten slettes ikke. Det er kun tilknytningen til tilbuddet, der slettes.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Konfigurer standardprojektprislister på et tilbud

Projektprislister kan oprettes som standard på et projekttilbud. Denne konfiguration sikrer, at alle tilbud i organisationen altid starter med en standardprisliste for prisperioden.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Konfigurer organisationens standard for projektprislister

1. Gå til **Indstillinger** > **Generelt** > **Parametre**.
2. På listesiden **Aktive parametre** skal du finde posten og dobbeltklik på den for at åbne den. 
3. På siden **Parametre** skal du vælge fanen **Prisliste**. Du kan se, at listen over standardprislisterne er vist. Dette er en liste over standardomkostninger og salgsprislister. Hvis du har en salgsprisliste tilknyttet her for hver valuta, du sælger i, sikrer, at denne salgsprisliste hentes som standard i et hvilket som helst tilbud, som du opretter for kunder, der har en transaktion i denne valuta.

### <a name="set-up-customer-specific-project-price-lists"></a>Konfigurer kundespecifikke projektprislister

Der kan også konfigureres kundespecifikke projektprislister, når du har forhandlet en overordnet prisfastsættelsesaftale med dine kunder.

Hvis du vil konfigurere en kundespecifik projektprisliste, skal du benytte følgende fremgangsmåde.

1. I området **Salg** skal du vælge **Kunder**.
2. På listen over dine aktive firmaer skal du vælge og åbne den kundepost, som du har en særlig prisliste til.
3. Under fanen **Projektprislister** kan du oprette en ny prislistetilknytning, så den projektprisliste, der er specifik for denne kunde, vises.

## <a name="create-custom-pricing-on-a-project-quote"></a>Opret brugerdefineret prisfastsættelse på et projekttilbud

Når du har organisations- og kundespecifikke standardprojektprislister, oprettes dine projekttilbud automatisk med disse projektprislistetilknytninger. I visse tilfælde kan det dog være nødvendigt at oprette brugerdefineret prisfastsættelse for et bestemt projekttilbud. 

1. I **Projekttilbud** skal du på fanen **Projektprisliste** kontrollere, at der ikke er valgt en specifik prislistepost i undergitteret.
2. Vælg **Opret brugerdefineret prisfastsættelse**. Dette opretter kopier af de standardprislister, der i øjeblikket er knyttet til tilbuddet, og disse kopier knyttes til tilbuddet. De tilknytninger, der findes til standardprislisterne, fjernes. Sælgeren kan derefter begynde at foretage ændringer af priserne i disse kopier. Disse ændrede priser gælder kun for dette projekttilbud.
