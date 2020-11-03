---
title: Fakturering i Project Service Automation
description: Dette emne indeholder oplysninger om fakturering.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f8107a660f9993c7b6a32d69047a81fb7e0abef8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074236"
---
# <a name="invoicing-in-project-service-automation"></a>Fakturering i Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fakturering i Dynamics 365 Project Service Automation er nyttig, fordi den giver projektledere et niveau til godkendelse på et andet niveau, før de opretter fakturaer til kunderne. Det første godkendelsesniveau fuldføres, når de tids- og udgiftsposter, som medlemmer af projektteamet sender, godkendes.

PSA er ikke designet til at generere kundefokuserede fakturaer af følgende årsager:

- Den indeholder ikke skatteoplysninger.
- Det er ikke muligt at konvertere andre valutaer til faktureringsvalutaen ved hjælp af korrekt konfigurerede valutakurser.
- Det er ikke muligt at formatere fakturaer korrekt, så de kan udskrives.

Du kan i stedet bruge et regnskabssystem til at oprette kundefokuserede fakturaer, der bruger oplysninger fra fakturaforslag, som er genereret i PSA.

## <a name="creating-project-invoices-in-psa"></a>Oprettelse af projektfakturaer i PSA.

Der kan oprettes projektfakturaer én eller flere ad gangen. Du kan oprette dem manuelt, eller de kan konfigureres, så de genereres i automatiserede kørsler.

### <a name="manually-create-project-invoices-in-psa"></a>Manuelt oprettede projektfakturaer i PSA

På siden med listen **Projektkontrakter** kan du oprette projektfakturaer separat for hver projektkontrakt, eller du kan oprette fakturaer samlet for flere projektkontrakter.

Følg dette trin for at oprette en faktura for en bestemt projektkontrakt.

- Åbn siden med listen **Projektkontrakter** , åbn en projektkontrakt, og vælg derefter **Opret faktura**.

    ![Oprettelse af projektfakturaer for en bestemt projektkontrakt](media/CreateProjectInvoicesOneByOne.png)

    Der genereres en faktura for alle transaktioner for den valgte projektkontrakt, der har statussen **Klar til fakturering**. Disse transaktioner omfatter tid, udgifter, milepæle og produktbaserede kontraktlinjer.

Følg disse trin for at oprette flere fakturaer samlet.

1. På siden med listen **Projektkontrakter** skal du vælge en eller flere projektkontrakter, som du skal oprette en faktura for, og derefter vælge **Opret projektfakturaer**.

    ![Oprettelse af flere projektfakturaer samlet.](media/CreateProjectInvoicesBulk.png)

    Der vises en advarsel om, at der kan være en forsinkelse, inden der oprettes fakturaer. Processen vises også.

2. Vælg **OK** for at lukke meddelelsesfeltet.

    Der genereres en faktura for alle transaktioner på en kontraktlinje, der har statussen **Klar til fakturering**. Disse transaktioner omfatter tid, udgifter, milepæle og produktbaserede kontraktlinjer.

3. Hvis du vil have vist de fakturaer, der er genereret, skal du gå til **Salg** \> **Fakturering** \> **Fakturaer**. Der vises én faktura for hver projektkontrakt.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Konfigurere automatisk oprettelse af projektfakturaer i PSA

Følg disse trin for at konfigurere en automatiseret fakturakørsel i PSA.

1. Gå til **Project Service** \> **lndstillinger** \> **Batchjob**.
2. Opret et batchjob, og kald det **Opret fakturaer i PSA .** Navnet på batchjobbet skal indeholde udtrykket "Opret fakturaer".
3. I feltet **Jobtype** skal du vælge **Ingen**. Som standard skal indstillingerne **Hyppighed: Dagligt** og **Er aktiv** angives til **Ja**.
4. Vælg **Kør arbejdsproces**. I dialogboksen **Slå post op** kan du se tre arbejdsprocesser:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vælg **ProcessRunCaller** og derefter **Tilføj**.
6. I den næste dialogboks skal du vælge **OK**. En **slumre** -arbejdsproces efterfølges af en **proces** -arbejdsproces.

    Du kan også vælge **ProcessRunner** i trin 5. Når du derefter vælger **OK** , efterfølges en **proces** -arbejdsproces af en **slumre** -arbejdsproces.

Begge arbejdsprocesserne **ProcessRunCaller** og **ProcessRunner** opretter fakturaer. **ProcessRunCaller** kalder på **ProcessRunner**. **ProcessRunner** er den arbejdsproces, der rent faktisk opretter fakturaerne. Denne proces gennemgår alle de kontraktlinjer, der skal oprettes fakturaer for, og den opretter fakturaer for disse linjer. Hvis du vil fastlægge, hvilke kontraktlinjer der skal oprettes fakturaer for, kigger jobbet på fakturaernes kørselsdatoer for kontraktlinjerne. Hvis kontraktlinjer, der er knyttet til en kontrakt, har samme fakturakørselsdato, samles transaktionerne i én faktura, der indeholder to fakturalinjer. Hvis der ikke findes transaktioner, som der skal oprettes fakturaer til, ignorerer jobbet fakturaoprettelse.

Når **ProcessRunner** er færdig med at køre, kalder processen på **ProcessRunCaller** , angiver sluttidspunktet og lukkes. **ProcessRunCaller** starter derefter en timer, der kører i 24 timer fra det angivne sluttidspunkt. Når timeren afsluttes, lukkes **ProcessRunCaller**.

Batchprocesjobbet til oprettelse af fakturaer er et tilbagevendende job. Hvis denne batchproces køres mange gange, oprettes der flere forekomster af jobbet, og der opstår fejl. Du bør derfor kun starte batchprocessen én gang, og du bør kun genstarte den, hvis den holder op med at køre.

> [!NOTE]
> Batchfakturering i Project Service Automation kører kun for projektkontraktlinjer, der er konfigureret af fakturaplaner. Der skal være konfigureret målepæle for en kontraktlinje med en faktureringsmetode med fast pris. Der skal konfigureres en datobaseret fakturaplan for en projektkontraktlinje med en metode til fakturering af time og materiale. Oplysninger om konfiguration af faktureringsfrekvenser i forbindelse med et projekt, der er baseret på en tilbudslinje, findes i emne, [Tilbud og tilbudslinjer](basic-quote-lines.md#invoice-schedule). Det samme gælder for en projektbaseret kontraktlinje.      
 
### <a name="edit-a-draft-psa-invoice"></a>Redigere en kladde af PSA-faktura

Når du opretter en kladde til en projektfaktura, medtages alle ikke-fakturerede salgstransaktioner, der blev oprettet, da tids-og udgiftsposterne blev godkendt, på fakturaen. Du kan foretage følgende justeringer, mens fakturaen stadig er i kladdefasen:

- Slette eller redigere oplysninger om fakturalinjer.
- Redigere og justere antal og faktureringstype.
- Tilføje tid, udgifter og gebyrer direkte som transaktioner på fakturaen. Du kan bruge denne funktion, hvis fakturalinjen er knyttet til en kontraktlinje, der tillader disse transaktionsklasser.

Vælg **Bekræft** for at bekræfte en faktura. Handlingen Bekræft er en envejshandling. Når du vælger **Bekræft** , bliver fakturaen skrivebeskyttet i systemet, og der oprettes fakturerede faktiske salgstal ud fra hver fakturalinjedetalje for hver fakturalinje. Hvis fakturalinjedetaljen refererer til et ikke-faktureret faktisk salgstal, vil systemet også tilbageføre det ikke-fakturerede faktiske salgstal. Alle de fakturalinjedetaljer, der er oprettet ud fra en tids- eller udgiftspost, refererer til et ikke-faktureret faktisk salgstal. Integrationssystemer for generelle hovedbøger kan bruge denne tilbageførsel til at tilbageføre igangværende projektarbejde (WIP) til regnskabsmæssig brug.

### <a name="correct-a-confirmed-psa-invoice"></a>Rette en bekræftet PSA-faktura

Bekræftede PSA-fakturaer kan redigeres (korrigeres). Når en bekræftet faktura rettes, oprettes der en ny rettelsesfakturakladde. Da det er en forudsætning, at du vil tilbageføre alle transaktioner og mængder fra den oprindelige faktura, inkluderer denne rettelsesfaktura alle transaktioner fra den oprindelige faktura, og alle mængder på den er 0 (nul).

Hvis der ikke skal rettes i nogen transaktioner, kan du fjerne dem fra rettelsesfakturakladden. Hvis du kun vil tilbageføre eller returnere en delmængde, kan du redigere feltet **Antal** i linjedetaljen. Hvis du åbner fakturalinjedetaljen, kan du se det oprindelige fakturaantal. Du kan derefter redigere det aktuelle fakturaantal, så det er mindre eller større end det oprindelige fakturaantal.

Når du bekræfter en rettelsesfaktura, tilbageføres det oprindeligt fakturerede salgstal, og der oprettes et nyt faktureret faktisk salgstal. Hvis mængden blev reduceret, medfører differencen, at der også oprettes et nyt ikke-faktureret faktisk salgstal. Hvis det oprindelige fakturerede salg f.eks. var otte timer, og linjedetaljen i rettelsesfakturaen har et reduceret antal på seks timer, tilbagefører PSA den oprindeligt fakturerede salgslinje og opretter to nye faktiske salgstal:

- Et faktureret faktisk salgstal for seks timer.
- Et ikke-faktureret faktisk salgstal for de resterende to timer. Denne transaktion kan enten faktureres senere eller markeres som ikke-fakturerbar, afhængigt af forhandlingerne med kunden.
