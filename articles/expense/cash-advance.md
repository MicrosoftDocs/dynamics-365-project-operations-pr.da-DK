---
title: Kontantforskud
description: Dette emne indeholder oplysninger om kontantforskud.
author: suvaidya
manager: AnnBe
ms.date: 03/25/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5ac8956720deac9e9c9191cefb870a7fbbeedcca
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715553"
---
# <a name="cash-advance"></a>Kontantforskud

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Et kontantforskud giver medarbejderne mulighed for at låne penge fra deres virksomhed, inden de afholder udgifter. Når et ønsket kontantforskud godkendes og betales, kan medarbejderen bruge penge til de forretningsudgifter, de kan blive pålagt. 

## <a name="create-and-submit-a-cash-advance-request"></a>Opret og indsend en anmodning om kontantforskud
Hvis du vil oprette et nyt kontantforskud og indsende en anmodning om kontantforskud, skal du gøre følgende: 

1. Under **Mine udgifter** skal du vælge **Kontantforskud** > **Nyt**. 
2. På siden **Ny anmodning om kontantforskud** skal du angive formålet med udgiften og vælge den placering, hvor udgiften afholdes.
3. Angiv det ønskede beløb og den ønskede valuta, og vælg **Gem**. 
4. Når du er klar til at indsende anmodningen om kontantforskud, skal du på siden **Anmodning om kontantforskud** vælge **Arbejdsproces** > **Indsend**.

## <a name="modify-a-cash-advance-request"></a>Lav en ændring i en anmodning om kontantforskud

Du kan ændre en anmodning om kontantforskud, hvis den ikke er sendt til godkendelse.

1. Under **Mine udgifter: Kontantforskud** skal du finde og vælge det kontantforskud, som du ønsker at redigere.
2. Vælg **Rediger**, og foretag de nødvendige ændringer af anmodningen om kontantforskud. 
3. Vælg **Gem og luk**.


## <a name="view-cash-advance-requests"></a>Se anmodninger om kontantforskud
Du kan gennemse listen over alle de kontantforskud, der er i kladde, sendt til gennemsyn eller betalt, under **Mine udgifter: kontantforskud**. 

## <a name="approve-cash-advance-requests"></a>Godkend anmodninger om kontantforskud

Ledere eller brugere, der er konfigureret som godkendere i arbejdsprocessen, kan godkende de kontantforskud, de har sendt til gennemsyn. 

1. Hvis du vil godkende et kontantforskud, skal du under **Behandling af kontantforskud** vælge **Kontantforskud til gennemsyn**.
2. Vælg det kontantforskud, du skal gennemgå, og vælg **Godkend**.  

## <a name="pay-cash-advances"></a>Udbetal kontantforskud 
Følgende procedure gennemføres typisk af en bogholder eller en bruger med regnskabstilladelser.

1. Hvis du vil bogføre godkendte kontantforskud, skal du vælge **Godkendte kontantforskud** og derefter vælge **Betal og overfør**.  
2. Angiv kladdeoplysningerne for kontantforskuddene, og vælg derefter **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Indsend en udgiftsrapport mod et betalt kontantforskud 

Når du opretter og indsender en udgiftsrapport for det kontantforskud, som du allerede har modtaget, justeres udgifterne automatisk i forhold til det pågældende forskud. Hvis kontantforskuddet er større end det udgiftsførte beløb, skal du vende tilbage til virksomhedens saldi ved hjælp af udgiftskategorien **Returner kontanter**. Hvis det af virksomheden betalte kontantforskud er mindre end det beløb, som du har angivet som udgiv, skal virksomheden udbetale saldoen til dig. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Vælg kontantforskud, der gælder for dine udgifter
Før du indsender en udgiftsrapport, kan du vælge det kontantforskud, der stemmer overens med udgiftstransaktionerne i rapporten. Hvis du vil bruge denne funktion, skal følgende to funktioner aktiveres fra arbejdsområdet **Funktionsstyring**:

  - Nye udgiftsrapporter
  - Mulighed for at tilknytte kontantforskud til udgiftslinjer
 
 Når disse funktioner er aktiveret:
 
  - Du kan vælge en eller flere kontantforskud for hver udgiftslinje.
  - Den tilgængelige saldo for et kontantforskud kan ses i realtid, når en udgiftsrapport gemmes. Dette giver dig mulighed for at behandle udgiftstransaktioner og samtidig tilbageføre kontanttransaktioner.
  - Du kan vælge flere kontantforskud for en udgiftstransaktion.
  - Dataene for afstemning af kontantforskuddet er tilgængelig via en forespørgsel. 
 
Hvis du ikke bruger disse funktioner, forbliver funktionaliteten den samme, og det eksisterende kontantforskud reduceres automatisk, når en udgift indsendes.

### <a name="example"></a>Eksempel 
Du planlægger at rejse fra København til New York City for at deltage i en konference. Du opretter en anmodning om et kontantforskud på 3.000,00 USD på baggrund af de anslåede omkostninger til konferencebilletten, flybilletten, hotellet, måltider og taxi. Du modtager ikke betaling, medmindre din leder godkender denne anmodning. Når din leder har godkendt det, indbetales det ønskede kontantforskud som 3.000,00 DKK på din bankkonto. Du deltager derefter i konferencen. Når rejsen er gennemført, kan du se, at den samlede udgift kun var 2.790,00 DKK. Vælg **Kontant** i feltet **Betalingsmetode**, og indsend dine udgifter på 2.790,00 USD. Det indsendte udgiftsbeløb justeres automatisk i forhold til kontantforskuddet på 3.000,00 DKK, som blev udlånt til dig. Du har nu en balance på 210,00 USD (3.000,00-2.790,00), som du kan betale tilbage til virksomheden ved hjælp af udgiftskategorien **Tilbagebetal kontanter**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
