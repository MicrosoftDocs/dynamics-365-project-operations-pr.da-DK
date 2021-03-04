---
title: Konfigurer automatisk fakturaoprettelse
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer systemet til at oprette fakturaer automatisk.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122426"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurer automatisk fakturaoprettelse

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_


Benyt følgende fremgangsmåde for at konfigurere en automatiseret fakturakørsel i Dynamics 365 Project Operations.

1. Gå til **Indstillinger** > **Batchjobs**.
2. Opret et batchjob, og kald det **Opret fakturaer i Project Operations**. Navnet på batchjobbet skal indeholde ordene "opret fakturaer".
3. I feltet **Jobtype** skal du vælge **Ingen**. Som standard skal indstillingerne **Hyppighed: Dagligt** og **Er aktiv** angives til **Ja**.
4. Vælg **Kør arbejdsproces**. I dialogboksen **Slå post op** kan du se tre arbejdsprocesser:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vælg **ProcessRunCaller** og derefter **Tilføj**.
6. I den næste dialogboks skal du vælge **OK**. En **slumre**-arbejdsproces efterfølges af en **proces**-arbejdsproces.

  > [!NOTE]
  > Du kan også vælge **ProcessRunner** i trin 5. Når du derefter vælger **OK**, efterfølges en **proces**-arbejdsproces af en **slumre**-arbejdsproces.

Begge arbejdsprocesserne **ProcessRunCaller** og **ProcessRunner** opretter fakturaer. **ProcessRunCaller** kalder på **ProcessRunner**. **ProcessRunner** er den arbejdsproces, der rent faktisk opretter fakturaerne. Denne proces gennemgår alle de kontraktlinjer, der skal oprettes fakturaer for, og den opretter fakturaer for disse linjer. Hvis du vil fastlægge, hvilke kontraktlinjer der skal oprettes fakturaer for, kigger jobbet på fakturaernes kørselsdatoer for kontraktlinjerne. Hvis kontraktlinjer, der er knyttet til en kontrakt, har samme fakturakørselsdato, samles transaktionerne i én faktura, der indeholder to fakturalinjer. Hvis der ikke findes transaktioner, som der skal oprettes fakturaer til, ignorerer jobbet fakturaoprettelse.

Når **ProcessRunner** er færdig med at køre, kalder processen på **ProcessRunCaller**, angiver sluttidspunktet og lukkes. **ProcessRunCaller** starter derefter en timer, der kører i 24 timer fra det angivne sluttidspunkt. Når timeren afsluttes, lukkes **ProcessRunCaller**.

Batchprocesjobbet til oprettelse af fakturaer er et tilbagevendende job. Hvis denne batchproces køres mange gange, oprettes der flere forekomster af jobbet, og der opstår fejl. Du bør derfor kun starte batchprocessen én gang, og du bør kun genstarte den, hvis den holder op med at køre.

> [!NOTE]
> Batchfakturering kører kun for projektkontrakt linjer, der er konfigureret af fakturaplaner. Der skal være konfigureret målepæle for en kontraktlinje med en faktureringsmetode med fast pris. Der skal konfigureres en datobaseret fakturaplan for en projektkontraktlinje med en metode til fakturering af time og materiale. Det samme gælder for en projektbaseret kontraktlinje.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]