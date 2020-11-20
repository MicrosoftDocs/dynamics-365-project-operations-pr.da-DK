---
title: Konfigurer automatisk fakturaoprettelse - lille
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer automatisk oprettelse af proformafakturaer.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176559"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Konfigurer automatisk fakturaoprettelse - lille
 
_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Du kan konfigurere automatisk oprettelse af faktura i Dynamics 365 Project Operations. Systemet opretter en proformafaktura i kladde, der er baseret på fakturaplanen for hver projektkontrakt og kontraktlinje. Fakturaplaner konfigureres på kontraktlinjeniveau. De enkelte linjer i en kontrakt kan have en særskilt fakturaplan, eller du kan inkludere den samme fakturaplan på alle kontraktlinjer.

Når du opretter en faktura, opretter systemet altid mindst én faktura pr. projektkontrakt. I visse tilfælde kan der oprettes flere fakturaer.

Hvis kontrakten f.eks. har flere kunder, oprettes samme antal fakturaer som det antal kunder, der har fakturerbare transaktioner, der skal faktureres på den pågældende projektkontrakt.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Forstå, hvordan transaktioner medtages i en faktura 

Nogle gange angiver de enkelte projektbaserede kontraktlinjer en separat fakturaplan. Implementeringsservicer for Adatum-kontrakten indeholder f.eks. følgende kontraktlinjer:

- Prototypearbejde, der er en fast pris med to manuelt oprettede milepæle.
- Implementeringsarbejde, der omfatter tid, og som vil blive faktureret mandage i hver anden uge.
- De udgifter, der påløber, og som skal faktureres den første mandag i hver måned.

De fakturaplaner, der er defineret for hvert af disse to linjeelementer, ligner følgende tabel:

| Kontraktlinje | Dato for fakturakørsel | Skæringsdato for transaktion | Milepælsdato | Beløb for milepæl |
| --- | --- | --- | --- | --- |
| Prototypearbejde | Mandag den 5. oktober | - | Mandag den 5. oktober | 5000 USD |
| - | Tirsdag den 3. november | - | Tirsdag den 3. november | 12,000 USD |
| Implementeringsarbejde | Mandag den 5. oktober | Søndag den 4. oktober | - | - |
| - | Mandag den 19. oktober | Søndag den 18. oktober | - | - |
| - | Mandag den 2. november | Søndag den 1. november | - | - |
| - | Mandag den 16. november | Søndag den 15. november | - | - |
| Påløbne udgifter | Mandag den 5. oktober | Søndag den 4. oktober | - | - |
| - | Mandag den 2. november | Søndag den 1. november | - | - |

I dette eksempel, når den automatiske fakturering køres:

- **Den 4. oktober eller en hvilken som helst dato før**: Der genereres ikke en faktura for denne kontrakt, da tabellen **Fakturaplan** for hver af disse kontraktlinjer ikke angiver søndag den 4. oktober som en fakturakørselsdato.
- **Mandag den 5. oktober**: Der oprettes en faktura for:

    - Prototypearbejde, som inkluderer milepælen, hvis den er markeret som **Klar til fakturering**.
    - Implementeringsarbejde, som omfatter alle de tidstransaktioner, der er oprettet før skæringsdatoen for transaktioner, søndag den 4. oktober, og som er markeret med **Klar til fakturering**.
    - Påløbne udgifter, som omfatter alle de udgiftstransaktioner, der er oprettet før skæringsdatoen for transaktioner, søndag den 4. oktober, og som er markeret med **Klar til fakturering**.
  
- **Den 6. oktober eller en hvilken som helst dato før den 19. oktober**: Der genereres ikke en faktura for denne kontrakt, da tabellen **Fakturaplan** for hver af disse kontraktlinjer ikke angiver den 6. oktober eller en hvilken som helst dato før den 19. oktober som en fakturakørselsdato.
- **Mandag den 19. oktober**: Der genereres en faktura for implementeringsarbejde, som omfatter alle de tidstransaktioner, der er oprettet før skæringsdatoen for transaktioner, søndag den 18. oktober, og som er markeret med **Klar til fakturering**.
- **Mandag den 2. november**: Der oprettes en faktura for:

    - Implementeringsarbejde, som omfatter alle de tidstransaktioner, der er oprettet før skæringsdatoen for transaktioner, søndag den 1. november, og som er markeret med **Klar til fakturering**.
    - Påløbne udgifter, som omfatter alle de udgiftstransaktioner, der er oprettet før skæringsdatoen for transaktioner, søndag den 1. november, og som er markeret med **Klar til fakturering**.

- **Tirsdag den 3. november**: Der genereres en faktura for prototypearbejde, som inkluderer milepælen på 12.000 USD, hvis den er markeret som **Klar til fakturering**.

## <a name="configure-automatic-invoicing"></a>Konfigurer automatisk fakturering

Fuldfør følgende trin for at konfigurere en automatiseret fakturakørsel.

1. I **Project Operations** skal du gå til **Indstillinger** > **Konfiguration af tilbagevende faktura**.
2. Opret et batchjob, og navngiv det **Opret fakturaer i Project Operations**. Navnet på batchjobbet skal indeholde ordene "opret fakturaer".
3. I feltet **Jobtype** skal du vælge **Ingen**. Som standard skal felterne **Hyppighed: Dagligt** og **Er aktiv** angives til **Ja**.
4. Vælg **Kør arbejdsproces**. I dialogboksen **Slå post op** kan du se tre arbejdsprocesser:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Vælg **ProcessRunCaller** og derefter **Tilføj**.
6. I den næste dialogboks skal du vælge **OK**. En **slumre**-arbejdsproces efterfølges af en **proces**-arbejdsproces. 

> [!NOTE]
> Du kan også vælge **ProcessRunner** i trin 5. Når du derefter vælger **OK**, efterfølges en **proces**-arbejdsproces af en **slumre**-arbejdsproces.

Begge arbejdsprocesserne **ProcessRunCaller** og **ProcessRunner** opretter fakturaer. **ProcessRunCaller** kalder på **ProcessRunner**. **ProcessRunner** er den arbejdsproces, der rent faktisk opretter fakturaerne. Denne arbejdsproces gennemgår alle de kontraktlinjer, der skal oprettes fakturaer for, og opretter fakturaer for disse linjer. Hvis du vil fastlægge, hvilke kontraktlinjer der skal oprettes fakturaer for, kigger jobbet på fakturaernes kørselsdatoer for kontraktlinjerne. Hvis kontraktlinjer, der er knyttet til en kontrakt, har samme fakturakørselsdato, samles transaktionerne i én faktura, der indeholder to fakturalinjer. Hvis der ikke findes transaktioner, som der skal oprettes fakturaer til, springer jobbet over oprettelsen af en faktura.

Når **ProcessRunner** er færdig med at køre, kalder processen på **ProcessRunCaller**, angiver sluttidspunktet og lukkes. **ProcessRunCaller** starter derefter en timer, der kører i 24 timer fra det angivne sluttidspunkt. Når timeren afsluttes, lukkes **ProcessRunCaller**.

Batchprocesjobbet til oprettelse af fakturaer er et tilbagevendende job. Hvis denne batchproces køres mange gange, oprettes der flere forekomster af jobbet, og der opstår fejl. Du bør derfor kun starte batchprocessen én gang og kun genstarte den, hvis den holder op med at køre.

> [!NOTE]
> Batchfakturering i Project Operations køres kun for projektkontrakt linjer, der er konfigureret af fakturaplaner. Der skal være konfigureret målepæle for en kontraktlinje med en faktureringsmetode med fast pris. Der skal konfigureres en datobaseret fakturaplan for en projektkontraktlinje med en metode til fakturering af time og materiale.
