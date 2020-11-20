---
title: Kontantforskud
description: Dette emne indeholder oplysninger om kontantforskud.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c5839fbdab58903555936324139b76f4c94b6c35
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122742"
---
# <a name="cash-advance"></a>Kontantforskud

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Et kontantforskud giver medarbejderne mulighed for at låne penge fra deres virksomhed, inden de afholder udgifter. Når et ønsket kontantforskud godkendes og betales, kan medarbejderen bruge penge til de forretningsudgifter, de kan blive pålagt. 

## <a name="create-and-submit-a-cash-advance-request"></a>Opret og indsend en anmodning om kontantforskud

1. Under **Mine udgifter** skal du vælge **Kontantforskud** > **Nyt** for at oprette et nyt kontantforskud. 
2. På siden **Ny anmodning om kontantforskud** skal du angive formålet med udgiften og vælge den placering, hvor udgiften afholdes.
3. Angiv det ønskede beløb og den ønskede valuta, og vælg **Gem**. 
4. Når du er klar til at indsende anmodningen om kontantforskud, skal du på siden **Anmodning om kontantforskud** vælge **Arbejdsproces** > **Indsend**.

## <a name="modify-a-cash-advance-request"></a>Lav en ændring i en anmodning om kontantforskud

Du kan ændre en anmodning om kontantforskud, hvis den ikke er sendt til godkendelse.

1. Under **Mine udgifter: kontantforskud** skal du finde og vælge det kontantforskud, du vil redigere.
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

Når du opretter og indsender en udgiftsrapport for det allerede modtagne kontantforskud, justeres udgifterne automatisk i forhold til forskuddet. Hvis kontantforskuddet er større end det udgiftsførte beløb, skal du vende tilbage til virksomhedens saldi ved hjælp af udgiftskategorien **Returner kontanter**. Hvis det virksomhedsbetalte kontantforskud er mindre end det beløb, du har udgiftsført, skal virksomheden refundere differencen. 

### <a name="example"></a>Eksempel
Du har planer om at skulle rejse fra København til Aarhus for at deltage i en konference. Du opretter en anmodning om kontantforskud på 3.000,00 DKK, da du har estimeret omkostningerne til konferencebilletten, fly, hotel, måltider og taxier til at udgør dette beløb. Du modtager ikke udbetalingen, medmindre din leder har godkendt denne anmodning. Når din leder har godkendt det, indbetales det ønskede kontantforskud som 3.000,00 DKK på din bankkonto. Du deltager derefter i konferencen. Når rejsen er gennemført, kan du se, at den samlede udgift kun var 2.790,00 DKK. Vælg **Kontant** i feltet **Betalingsmetode**, og indsend udgiften på 2.790,00 DKK. Det indsendte udgiftsbeløb justeres automatisk i forhold til kontantforskuddet på 3.000,00 DKK, som blev udlånt til dig. Du skylder nu virksomheden 210,00 DKK (3.000,00-2.790,00), som du kan returnere ved hjælp af udgiftskategorien **Returner kontanter**. 
