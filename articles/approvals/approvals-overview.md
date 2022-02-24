---
title: Godkendelsesoversigt
description: Dette emne indeholder informationer om, hvordan du arbejder med godkendelser i Project Operations.
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852492"
---
# <a name="approvals-overview"></a>Godkendelsesoversigt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Indsendelse af tid, udgifter og materialeforbrug gennemgår en godkendelsesarbejdsproces. Når posterne er godkendt, registreres transaktionerne i faktiske tal, eller der reserveres tid i planlægningen.

## <a name="approvals-workflow"></a>Godkendelsesarbejdsproces
Når du oprette og indsender en tids-, udgifts- eller materialeforbrugspost, oprettes der en godkendelsespost. Projektgodkenderen eller projektlederen gennemser og godkender posten. Hvis posten er relateret til et projekt, oprettes de faktiske tal, når den godkendes. Det giver mulighed for at spore omkostninger og fakturering.

## <a name="approve-an-entry"></a>Godkend en post
Siden **Godkendelser** giver mulighed for at skifte mellem forskellige visninger, så du kan se de forskellige typer godkendelser.
  
1. Gå til siden **Godkendelser**, og vælg **Udgifter**, **Tid**, **Materialeforbrug** eller **Tilbagekaldelser**.
2. Gennemse de enkelte godkendelser, og vælg dem, du vil godkende.
3. Vælg **Godkend** for at godkende de markerede poster.
Disse poster behandles i systemet, og de faktiske værdier oprettes.

## <a name="reject-an-entry"></a>Afvis en post
Som projektgodkender skal du muligvis sende en post tilbage til en bruger, så brugeren kan rette den.
  
1. Gå til siden **Godkendelser**, og vælg den post, du vil afvise. 
2. Vælg **Afvis**.
3. Du kan også tilføje en kommentar i dialogboksen **Bemærkninger til afvisning**, der giver brugeren besked om, hvorfor posten afvises.
4. Vælg **OK**. Posten sendes til brugeren igen.
  
## <a name="cancel-approval"></a>Annuller godkendelse
I visse tilfælde skal du muligvis annullere en tidligere godkendt post. Annullering af en tidligere godkendt post har økonomiske konsekvenser. 

## <a name="approving-recall-requests"></a>Godkendelse af anmodninger om tilbagekaldelse
I visse tilfælde kan det være nødvendigt for en konsulent at få vist en tidligere godkendt post. Annullering af en tidligere godkendt post har økonomiske konsekvenser. Projektgodkenderen skal godkende tilbagekaldelsen for at tilbageføre transaktionen i Faktiske.

## <a name="specify-project-approvers"></a>Angiv projektgodkendere
Hvert projekt har en række medlemmer af projektteamet. Du kan angive, hvilke teammedlemmer der også er projektgodkendere.

1. Gå til siden **Projekter**, og åbn projektet fra listen.
2. På fanen **Teams** skal du vælge det teammedlem, der skal være projektgodkender, og derefter vælge **Rediger**.
3. Vælg **Ja** i feltet **Projektgodkender**.
4. Vælg **Gem**.
5. Gentag trin 2-4 for at tilføje eller redigere flere projektgodkendere.

## <a name="configure-the-users-manager"></a>Konfigurer brugerens leder

1. Gå til **Indstillinger** > **Sikkerhed** > **Brugere**.
2. Vælg den bruger, du vil tildele en leder, og vælge derefter lederen på listen i området **Organisationsoplysninger**. 
3. Vælg **Gem**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
