---
title: Opret en manuel proformafaktura
description: Dette emne indeholder oplysninger om, hvordan du opretter en proformafaktura.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ad85262482f782391eca85f46ca0e63a887c89f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896094"
---
# <a name="create-a-manual-proforma-invoice"></a>Opret en manuel proformafaktura

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Fakturering giver projektledere et to-trins-godkendelsesniveau, før de opretter fakturaer til kunderne. Det første godkendelsesniveau fuldføres, når de tids- og udgiftsposter, som medlemmer af projektteamet sender, godkendes.

Dynamics 365 Project Operations er ikke designet til at generere kundefokuserede fakturaer af følgende årsager:

- Den indeholder ikke skatteoplysninger.
- Det er ikke muligt at konvertere andre valutaer til faktureringsvalutaen ved hjælp af korrekt konfigurerede valutakurser.
- Det er ikke muligt at formatere fakturaer korrekt, så de kan udskrives.

Du kan i stedet bruge et regnskabssystem til at oprette kundefokuserede fakturaer, der bruger oplysninger fra genererede fakturaforslag.

## <a name="creating-project-invoices"></a>Oprettelse af projektfakturaer

Der kan oprettes projektfakturaer én eller flere ad gangen. Du kan oprette dem manuelt, eller de kan konfigureres, så de genereres i automatiserede kørsler.

### <a name="manually-create-project-invoices"></a>Opret projektfakturaer manuelt 

På siden med listen **Projektkontrakter** kan du oprette projektfakturaer separat for hver projektkontrakt, eller du kan oprette fakturaer samlet for flere projektkontrakter.

Følg dette trin for at oprette en faktura for en bestemt projektkontrakt.

- Åbn siden med listen **Projektkontrakter**, åbn en projektkontrakt, og vælg derefter **Opret faktura**.

    Der genereres en faktura for alle transaktioner for den valgte projektkontrakt, der har statussen **Klar til fakturering**. Disse transaktioner omfatter tid, udgifter, milepæle og produktbaserede kontraktlinjer.

Følg disse trin for at oprette flere fakturaer samlet.

1. På siden med listen **Projektkontrakter** skal du vælge en eller flere projektkontrakter, som du skal oprette en faktura for, og derefter vælge **Opret projektfakturaer**.

    Der vises en advarsel om, at der kan være en forsinkelse, inden der oprettes fakturaer. Processen vises også.

2. Vælg **OK** for at lukke meddelelsesfeltet.

    Der genereres en faktura for alle transaktioner på en kontraktlinje, der har statussen **Klar til fakturering**. Disse transaktioner omfatter tid, udgifter, milepæle og produktbaserede kontraktlinjer.

3. Hvis du vil have vist de fakturaer, der er genereret, skal du gå til **Salg** \> **Fakturering** \> **Fakturaer**. Der vises én faktura for hver projektkontrakt.

### <a name="set-up-automated-creation-of-project-invoices"></a>Konfigurer automatisk oprettelse af projektfakturaer 

Følg disse trin for at konfigurere en automatiseret fakturakørsel.

1. Gå til **Indstillinger** \> **Batchjobs**.
2. Opret et batchjob, og navngiv det **Opret fakturaer i Project Operations**. Navnet på batchjobbet skal indeholde udtrykket "Opret fakturaer".
3. I feltet **Jobtype** skal du vælge **Ingen**. Som standard skal indstillingerne **Hyppighed: Dagligt** og **Er aktiv** angives til **Ja**.
4. Vælg **Kør arbejdsproces**. I dialogboksen **Slå post op** kan du se tre arbejdsprocesser:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vælg **ProcessRunCaller** og derefter **Tilføj**.
6. I den næste dialogboks skal du vælge **OK**. En **slumre**-arbejdsproces efterfølges af en **proces**-arbejdsproces.

    Du kan også vælge **ProcessRunner** i trin 5. Når du derefter vælger **OK**, efterfølges en **proces**-arbejdsproces af en **slumre**-arbejdsproces.

Begge arbejdsprocesserne **ProcessRunCaller** og **ProcessRunner** opretter fakturaer. **ProcessRunCaller** kalder på **ProcessRunner**. **ProcessRunner** er den arbejdsproces, der rent faktisk opretter fakturaerne. Denne proces gennemgår alle de kontraktlinjer, der skal oprettes fakturaer for, og den opretter fakturaer for disse linjer. Hvis du vil fastlægge, hvilke kontraktlinjer der skal oprettes fakturaer for, kigger jobbet på fakturaernes kørselsdatoer for kontraktlinjerne. Hvis kontraktlinjer, der er knyttet til en kontrakt, har samme fakturakørselsdato, samles transaktionerne i én faktura, der indeholder to fakturalinjer. Hvis der ikke findes transaktioner, som der skal oprettes fakturaer til, ignorerer jobbet fakturaoprettelse.

Når **ProcessRunner** er færdig med at køre, kalder processen på **ProcessRunCaller**, angiver sluttidspunktet og lukkes. **ProcessRunCaller** starter derefter en timer, der kører i 24 timer fra det angivne sluttidspunkt. Når timeren afsluttes, lukkes **ProcessRunCaller**.

Batchprocesjobbet til oprettelse af fakturaer er et tilbagevendende job. Hvis denne batchproces køres mange gange, oprettes der flere forekomster af jobbet, og der opstår fejl. Du bør derfor kun starte batchprocessen én gang, og du bør kun genstarte den, hvis den holder op med at køre.

> [!NOTE]
> Batchfakturering kører kun for projektkontrakt linjer, der er konfigureret af fakturaplaner. Der skal være konfigureret målepæle for en kontraktlinje med en faktureringsmetode med fast pris. Der skal konfigureres en datobaseret fakturaplan for en projektkontraktlinje med en metode til fakturering af time og materiale. Det samme gælder for en projektbaseret kontraktlinje.      
 
### <a name="edit-a-draft-invoice"></a>Rediger en fakturakladde

Når du opretter en kladde til en projektfaktura, medtages alle ikke-fakturerede salgstransaktioner, der blev oprettet, da tids-og udgiftsposterne blev godkendt, på fakturaen. Du kan foretage følgende justeringer, mens fakturaen stadig er i kladdefasen:

- Slette eller redigere oplysninger om fakturalinjer.
- Redigere og justere antal og faktureringstype.
- Tilføje tid, udgifter og gebyrer direkte som transaktioner på fakturaen. Du kan bruge denne funktion, hvis fakturalinjen er knyttet til en kontraktlinje, der tillader disse transaktionsklasser.

Vælg **Bekræft** for at bekræfte en faktura. Handlingen Bekræft er en envejshandling. Når du vælger **Bekræft**, bliver fakturaen skrivebeskyttet i systemet, og der oprettes fakturerede faktiske salgstal ud fra hver fakturalinjedetalje for hver fakturalinje. Hvis fakturalinjedetaljen refererer til et ikke-faktureret faktisk salgstal, vil systemet også tilbageføre det ikke-fakturerede faktiske salgstal. Alle de fakturalinjedetaljer, der er oprettet ud fra en tids- eller udgiftspost, refererer til et ikke-faktureret faktisk salgstal. Integrationssystemer for generelle hovedbøger kan bruge denne tilbageførsel til at tilbageføre igangværende projektarbejde (WIP) til regnskabsmæssig brug.

### <a name="correct-a-confirmed-invoice"></a>Korriger en bekræftet faktura

Bekræftede fakturaer kan redigeres (korrigeres). Når en bekræftet faktura rettes, oprettes der en ny rettelsesfakturakladde. Da det er en forudsætning, at du vil tilbageføre alle transaktioner og mængder fra den oprindelige faktura, inkluderer denne rettelsesfaktura alle transaktioner fra den oprindelige faktura, og alle mængder på den er 0 (nul).

Hvis der ikke skal rettes i nogen transaktioner, kan du fjerne dem fra rettelsesfakturakladden. Hvis du kun vil tilbageføre eller returnere en delmængde, kan du redigere feltet **Antal** i linjedetaljen. Hvis du åbner fakturalinjedetaljen, kan du se det oprindelige fakturaantal. Du kan derefter redigere det aktuelle fakturaantal, så det er mindre eller større end det oprindelige fakturaantal.

Når du bekræfter en rettelsesfaktura, tilbageføres det oprindeligt fakturerede salgstal, og der oprettes et nyt faktureret faktisk salgstal. Hvis mængden blev reduceret, medfører differencen, at der også oprettes et nyt ikke-faktureret faktisk salgstal. Hvis det oprindelige fakturerede salg f.eks. var otte timer, og linjedetaljen i den korrigerende faktura har et reduceret antal på seks timer, tilbageføres den oprindeligt fakturerede salgslinje, og der oprettes to nye faktiske salgstal:

- Et faktureret faktisk salgstal for seks timer.
- Et ikke-faktureret faktisk salgstal for de resterende to timer. Denne transaktion kan enten faktureres senere eller markeres som ikke-fakturerbar, afhængigt af forhandlingerne med kunden.
