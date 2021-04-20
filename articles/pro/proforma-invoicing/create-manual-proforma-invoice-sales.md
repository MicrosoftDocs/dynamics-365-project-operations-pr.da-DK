---
title: Proformafakturaer på projekter
description: Dette emne indeholder oplysninger om proformafakturaer på projekter i Project Operations.
author: rumant
manager: Annbe
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d08e2b0422a991aa4c98ae5d1e0f60aa0eb9daa6
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867169"
---
# <a name="proforma-project-pnvoices"></a>Proformafakturaer på projekter

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Proformafakturering på projekter er nyttig, fordi det giver projektledere et nyt niveau til godkendelse, før de opretter fakturaer til kunderne. Det første godkendelsesniveau fuldføres, når de tids-, udgifts- og materialeposter, som medlemmer af projektteamet sender, godkendes.

Den lille udrulning af Dynamics 365 Project Operations er ikke udviklet til at oprette kundeorienterede fakturaer. Den følgende liste viser, hvorfor der ikke kan oprettes fakturaer:

- Indeholder ikke skatteoplysninger.
- Det er ikke muligt at konvertere andre valutaer til faktureringsvalutaen.
- Fakturaer til udskrivning kan ikke formateres korrekt.

Du kan i stedet bruge et økonomi- eller regnskabssystem til at oprette kundeorienterede fakturaer, der bruger oplysningerne i de dannede fakturaforslag.

## <a name="creating-project-invoices"></a>Oprettelse af projektfakturaer

Der kan oprettes projektfakturaer én eller flere ad gangen. Du kan oprette dem manuelt, eller de kan konfigureres, så de genereres i automatiserede kørsler.

### <a name="manually-create-project-invoices"></a>Opret projektfakturaer manuelt 

På listesiden **Projektkontrakter** kan du oprette projektfakturaer for hver enkelt projektkontrakt, eller du kan oprette massefakturaer for flere projektkontrakter.

   - På listesiden **Projektkontrakter** skal du åbne en projektkontrakt og dernæst vælge **Opret faktura**.

   Der genereres en faktura for alle transaktioner for den valgte projektkontrakt, der har statussen **Klar til fakturering**. Disse transaktioner omfatter tid, udgifter, materialer, milepæle, produktbaserede kontraktlinjer og andre ikke-fakturerede salgskladdelinjer, der kan være blevet bekræftet.

Sådan oprettes massefakturaer:

1. På listesiden **Projektkontrakter** skal du vælge en eller flere projektkontrakter, som du vil oprette en faktura for, og derefter vælge **Opret projektfakturaer**.
2. Der vises en advarsel om, at der kan være en forsinkelse, inden der oprettes fakturaer. Processen vises også. Vælg **OK** for at lukke meddelelsesfeltet.

   Der genereres en faktura for alle transaktioner på en kontraktlinje, der har statussen **Klar til fakturering**. Disse transaktioner omfatter tid, udgifter, materialer, milepæle, produktbaserede kontraktlinjer og andre ikke-fakturerede salgskladdelinjer, der kan være blevet bekræftet.

3. Se de dannede fakturaer ved at gå til **Salg** \> **Fakturering** \> **Fakturaer**. Der vises én faktura for hver projektkontrakt.

### <a name="set-up-automated-creation-of-project-invoices"></a>Konfigurer automatisk oprettelse af projektfakturaer 

Følg disse trin for at konfigurere en automatiseret fakturakørsel.

1. Gå til **Indstillinger** \> **Batchjobs**.
2. Opret et batchjob, og navngiv det **Opret fakturaer i Project Operations**. Navnet på batchjobbet skal indeholde udtrykket "Opret fakturaer".
3. I feltet **Jobtype** skal du vælge **Ingen**. Som standard skal indstillingerne **Hyppighed: Dagligt** og **Er aktiv** angives til **Ja**.
4. Vælg **Kør arbejdsproces**. I dialogboksen **Slå post op** kan du se følgende tre arbejdsprocesser:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vælg **ProcessRunCaller** og derefter **Tilføj**.
6. I den næste dialogboks skal du vælge **OK**. En **slumre**-arbejdsproces efterfølges af en **proces**-arbejdsproces.

    Du kan også vælge **ProcessRunner** i trin 5. Når du derefter vælger **OK**, efterfølges en **proces**-arbejdsproces af en **slumre**-arbejdsproces.

Begge arbejdsprocesserne **ProcessRunCaller** og **ProcessRunner** opretter fakturaer. **ProcessRunCaller** kalder på **ProcessRunner**. **ProcessRunner** er den arbejdsproces, der opretter fakturaerne. Denne arbejdsproces gennemgår alle de kontraktlinjer, der skal oprettes fakturaer for, og opretter fakturaerne. For at fastlægge hvilke kontraktlinjer der skal oprettes fakturaer for, kigger arbejdsprocessen på fakturaernes kørselsdatoer for kontraktlinjerne. Hvis kontraktlinjer, der er knyttet til en kontrakt, har samme fakturakørselsdato, samles transaktionerne i én faktura, der indeholder to fakturalinjer. Der er ikke er nogen transaktioner at oprette fakturaer for, bliver der ikke dannet fakturaer.

Når **ProcessRunner** er færdig med at køre, kalder processen på **ProcessRunCaller**, angiver sluttidspunktet og lukkes. **ProcessRunCaller** starter derefter en timer, der kører i 24 timer fra det angivne sluttidspunkt. Når timeren afsluttes, lukkes **ProcessRunCaller**.

Batchprocesjobbet til oprettelse af fakturaer er et tilbagevendende job. Hvis denne batchproces køres mange gange, oprettes der flere forekomster af jobbet, og dette kan resultere i fejl. For at undgå dette problem skal du kun starte batchprocessen én gang og kun genstarte den, hvis den holder op med at køre.

> [!NOTE]
> Batchfakturering kører kun for projektkontrakt linjer, der er konfigureret af fakturaplaner. Der skal være konfigureret målepæle for en kontraktlinje med en faktureringsmetode med fast pris. Der skal konfigureres en datobaseret fakturaplan for en projektkontraktlinje med en metode til fakturering af time og materiale. Det samme gælder for en projektbaseret kontraktlinje.      
 
### <a name="edit-a-draft-invoice"></a>Rediger en fakturakladde

Når du opretter en kladde til en projektfaktura, medtages alle ikke-fakturerede salgstransaktioner, der blev oprettet, da tids-og udgiftsposterne blev godkendt, på fakturaen. Du kan foretage følgende justeringer, mens fakturaen stadig er i kladdefasen:

- Slette eller redigere oplysninger om fakturalinjer.
- Redigere og justere antal og faktureringstype.
- Tilføj tid, udgifter, materiale og gebyrer direkte som transaktioner på fakturaen. Du kan bruge denne funktion, hvis fakturalinjen er knyttet til en kontraktlinje, der tillader disse transaktionsklasser.

Vælg **Bekræft** for at bekræfte en faktura. Denne handling er en envejshandling. Når du vælger **Bekræft**, bliver fakturaen skrivebeskyttet, og der oprettes fakturerede faktiske salgstal på grundlag af hver fakturalinjedetalje for hver fakturalinje. Hvis fakturalinjedetaljen refererer til et ikke-faktureret faktisk salgstal, tilbagefører det ikke-fakturerede faktiske salgstal. Alle fakturalinjedetaljer, der blev oprettet på grundlag af en tids-, omkostnings- eller materialeforbrugspost, refererer til et ikke-faktureret faktisk salg. Systemer til integration af finanskonti kan bruge denne tilbageførsel til at tilbageføre igangværende projektarbejde (WIP) af regnskabsmæssige årsager.

### <a name="correct-a-confirmed-invoice"></a>Korriger en bekræftet faktura

Bekræftede fakturaer kan redigeres. Når en bekræftet faktura rettes, oprettes der en ny rettelsesfakturakladde. Da det forudsættes, at du vil tilbageføre alle transaktionerne og mængderne fra den oprindelige faktura, inkluderer denne korrigerende faktura alle transaktionerne fra den oprindelige faktura, og alle mængderne på den er nul.

Hvis der findes transaktioner, som ikke kræver korrektion, kan du fjerne dem fra udkastet til den korrigerende faktura. Hvis du kun vil tilbageføre eller returnere en delmængde, kan du redigere feltet **Antal** i linjedetaljen. Hvis du åbner fakturalinjedetaljen, kan du se det oprindelige fakturaantal. Du kan derefter redigere det aktuelle fakturaantal, så det er mindre eller større end det oprindelige fakturaantal.

Når du bekræfter en rettelsesfaktura, tilbageføres det oprindeligt fakturerede salgstal, og der oprettes et nyt faktureret faktisk salgstal. Hvis mængden blev reduceret, vil differencen medføre, at der oprettes et nyt ikke-faktureret faktisk salgstal. Hvis det oprindelige fakturerede salg f.eks. var otte timer, og linjedetaljen i den korrigerende faktura har et reduceret antal på seks timer, tilbageføres den oprindeligt fakturerede salgslinje, og der oprettes to nye faktiske salgstal:

- Et faktureret faktisk salgstal for seks timer.
- Et ikke-faktureret faktisk salgstal for de resterende to timer. Denne transaktion kan faktureres senere eller markeres som ikke-fakturerbar, afhængigt af forhandlingerne med kunden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
