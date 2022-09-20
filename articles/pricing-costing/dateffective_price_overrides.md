---
title: Gældende pristilsidesættelser for dato
description: I denne artikel forklares, hvordan du kan konfigurere pristilsidesættelser for bestemte priser på prislisten.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445964"
---
# <a name="date-effective-price-overrides"></a>Gældende pristilsidesættelser for dato 

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

*Gældende pristilsidesættelser for dato* giver mulighed for at tilsidesætte eller ændre bestemte priser på prislisten. Du har f.eks. en standardprisliste, der er gældende fra 1. januar 2022 til 31. december 2022. Denne prisliste indeholder priser for mange roller. Den pris, der angives for rollen **Netværkstekniker**, er 100 amerikanske dollar (USD) pr. time. Når en netværkstekniker logger tid mellem 1. januar 2022 og 31. december 2022, bliver prisen 100 USD. Den 1. oktober 2022 skal du *kun* justere prisen for rollen **Netværkstekniker** fra 100 USD pr. time til 110 USD pr. time. Med funktionen **Gældende pristilsidesættelser for dato** kan du konfigurere denne ændring som en tilsidesættelse af rækken for den pågældende rollepris. Det er derfor ikke nødvendigt at kopiere hele prislisten og ændre prisen på kun denne ene række.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Gældende pristilsidesættelser for arbejdsdato

Processen til angivelse af datobaserede pristilsidesættelser for arbejdstid på et projekt består af to grundlæggende trin.

1. Aktivér funktionen **Gældende pristilsidesættelser for dato**.
1. Konfigurer en gældende pristilsidesættelse for dato.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Aktivere funktionen Gældende pristilsidesættelser for dato

> [!NOTE]
> Når funktionen **Gældende pristilsidesættelser for dato** er aktiveret, kan den ikke deaktiveres.

Benyt følgende fremgangsmåde for at aktivere funktionen **Gældende pristilsidesættelser for dato**.

1. Gå til **Indstillinger** \> **Parametre**.
1. Åbn posten **Parametre**.
1. Vælg **Aktivér gældende pristilsidesættelser for dato** under fanen **Funktionskontrol** i handlingsruden.
1. Vælg **OK** i bekræftelsesdialogboksen.
1. Efter et øjeblik skal du opdatere browseren. Funktioner for gældende pristilsidesættelser for dato skal nu være tilgængelige. Du ved, at disse funktioner er aktiveret, hvis knappen **Aktivér gældende pristilsidesættelser for dato** ikke længere vises i handlingsruden.

### <a name="set-up-a-date-effective-price-override"></a>Konfigurere en gældende pristilsidesættelse for dato

Gældende pristilsidesættelser for dato kan konfigureres på prislisterne **Omkostning**, **Salg** eller **Køb**.

> [!NOTE]
>Funktionsmåden for **Gældende pristilsidesættelser for dato** har i øjeblikket følgende begrænsninger:
>
> - Det er kun rollepriser og rolleprisavancer, der understøtter funktionen **Gældende pristilsidesættelser for dato** i Project Operations.
> - Når du kopierer en prisliste ved hjælp af handlingen **Kopiér** på siden **Prislistedetaljer**, og når du opretter en projektprisliste ud fra en standardprisliste eller brugerdefineret prisliste under oprettelse af en kontrakt, kopieres datobaserede pristilsidesættelser **ikke** fra kildeprislisten.

Hvis du vil konfigurere en datobaseret pristilsidesættelse for en rollepris eller rolleprisavance, skal du følge disse trin.

1. Åbn siden for den prisliste, du vil konfigurere den datobaserede pristilsidesættelse for.
1. Vælg fanen **Rollepriser**. Under denne fane vises alle **Rollepris**-posterne på prislisten.
1. Vælg den **Rollepris**-post, du vil konfigurere en ny datobaseret tilsidesættelse af pris for, og dobbeltklik derefter på **Rollepris** for at åbne siden **Oplysninger om rollepris**.
1. Vælg fanen **Gældende tilsidesættelser for dato**. I gitteret under denne fane vises alle de datobaserede pristilsidesættelser for den valgte **Rollepris**-post.
1. Vælg **Ny rollepristilsidesættelse** på værktøjslinjen over gitteret. Skyderen **Ny rollepristilsidesættelse** åbnes.
1. Angiv startdatoen, enheden og den nye pris for pristilsidesættelse. Vælg **Gem**, og luk formularen.

> [!NOTE]
> - En datobaseret pristilsidesættelse for en rollepris eller en rolleprisavance gælder for den samme kombination af prisdimensionsværdier, der findes i den overordnede **Rollepris**- eller **Rolleprisavance**-række.
> - Den dato, der vælges i feltet **Gældende fra**, skal være inden for de gældende datoer for den overordnede prisliste. Pristilsidesættelsen træder i kraft på den dato, der er valgt i feltet **Gældende fra**, og gælder indtil slutdatoen for den overordnede prisliste. Hvis du konfigurerer en anden datobaseret pristilsidesættelse for den samme rollepris, træder den første pristilsidesættelse i kraft på den dato, der er valgt i feltet **Gældende fra**, og gælder indtil starten af den anden tilsidesættelse.

## <a name="examples"></a>Eksempler

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Eksempel 1: Fastlæggelse af gældende dato for en rollepris, der har rollepristilsidesættelser

I følgende eksempel kan du se, hvordan gældende dato bestemmes for en bestemt rollepris, hvor rollepristilsidesættelser er konfigureret.

**Prisliste A: 1. januar til 30. juni**

*Rollepris*

| Rollepris | Enhed | Pris | Indvirkning på prissætning af indgående transaktioner |
|---|---|---|---|
| Netværkstekniker | Time | 100 | Denne pris bruges i alle transaktioner, hvor transaktionsdatoen er mellem 1. januar og 14. marts. |

*Rollepristilsidesættelse*

| Gældende fra | Enhed | Pris | Indvirkning på prissætning af indgående transaktioner |
|---|---|---|---|
| Marts 15 | Time | 110 | Denne pris bruges i alle transaktioner, hvor transaktionsdatoen er mellem 15. marts og 30. marts. |
| April 1 | Time | 120 | Denne pris bruges i alle transaktioner, hvor transaktionsdatoen er mellem 1. april og 30. juni. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Eksempel 2: Fastlæggelse af gældende dato for en rolleprisavance, der har tilsidesættelser af rolleprisavance

I følgende eksempel kan du se, hvordan gældende dato bestemmes for en bestemt rolleprisavance, hvor tilsidesættelser af rolleprisavance er konfigureret.

**Prisliste A: 1. januar til 30. juni**

*Rollepris*

| Rollepris | Arbejdstimer | Enhed | Pris | Indvirkning på prissætning af indgående transaktioner |
|---|---|---|---|---|
| Netværkstekniker | Regulær | Time | 100 | Denne pris bruges i alle transaktioner, hvor transaktionsdatoen er mellem 1. januar og 14. marts. |

*Rolleprisavance*

| Organisationsenhed | Arbejdstimer | Avance i % |
|---|---|---|
| Contoso USA | Overtid | 10 % |

*Tilsidesættelse af rolleprisavance*

| Gældende fra | Pris | Indvirkning på prissætning af indgående transaktioner |
|---|---|---|
| Marts 15 | 20 % | Denne avanceprocent bruges i alle transaktioner, hvor transaktionsdatoen er mellem 15. marts og 30. marts. |
| April 1 | 25 % | Denne avance bruges i alle transaktioner, hvor transaktionsdatoen er mellem 1. april og 30. juni. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
