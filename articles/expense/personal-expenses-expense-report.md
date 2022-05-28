---
title: Arbejd med personlige udgifter i en udgiftsrapport
description: Dette emne indeholder oplysninger om, hvordan du arbejder med personlige udgifter, som medarbejdere afholder sig, mens de rejser i erhvervsmæssige øjemed.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: d35bf6960bb60e2ad4184e1b5f188695a3525be0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586521"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Arbejd med personlige udgifter i en udgiftsrapport

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I forbindelse med forretningsrejser kan en medarbejder betale personlige udgifter med deres firmakreditkort. Hvis der ikke er defineret en proces til håndtering af personlige udgifter, kan godkendelsesprocessen for udgiftsrapporten blive afbrudt, når en medarbejder indsender sin specificerede udgiftsrapport.

Der er to metoder, som du kan bruge til at arbejde med en medarbejders personlige udgifter:

  - **Betalt af medarbejder**: Din organisation betaler ikke de personlige udgifter, der fremgår af fakturaen for virksomhedens kreditkort. I stedet betaler medarbejderen kreditkortleverandøren direkte for udgifterne. 
  - **Betalt af virksomhed**: Din organisation betaler den fulde faktura for firmakreditkortet og debiterer derefter arbejderens konto for de personlige udgifter.

Du kan vælge den metode, som din organisation bruger, på siden **Parametre for udgiftsstyring**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Aktivér funktionen til opdeling af udgifter, når der er defineret en værdi i et personligt beløbsfelt

Funktionen **Aktivér omkostningsfordeling, når der er defineret en værdi i et personligt beløbsfelt** gælder kun for udgiftsrapporter, der er godkendt ved hjælp af en arbejdsproces på linjeniveau. Rapporter godkendes ved at gå til **Behandl udgiftsrapporter** > **Udgiftsrapporter, der er tildelt til mig** > **Åbn udgiftsrapport**. 

Hvis du vil aktivere denne funktion, skal du gå til **Arbejdsområder** > **Funktionsadministration**, vælge **Aktiver funktionen til opdeling af udgifter, når der er defineret en værdi i et personligt beløbsfelt**, og vælg derefter **Aktivér nu**. 

Når funktionen er aktiveret, opretter de udgiftslinjer, der bruger denne funktion, to linjer, når rapporten indsendes. Der oprettes to linjer, så godkenderen kan godkende hver linje separat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
