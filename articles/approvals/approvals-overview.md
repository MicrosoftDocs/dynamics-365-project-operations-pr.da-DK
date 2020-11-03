---
title: Godkendelsesoversigt
description: Dette emne indeholder informationer om, hvordan du arbejder med godkendelser i Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074032"
---
# <a name="approvals-overview"></a>Godkendelsesoversigt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Indsendelser af tidsregistrering og udgifter går gennem en godkendelsesarbejdsproces. Når posterne er godkendt, registreres transaktionerne i faktiske tal, eller der reserveres tid i planlægningen.

## <a name="approvals-workflow"></a>Godkendelsesarbejdsproces
Når du opretter og indsender en tids- eller udgiftspost, oprettes der en godkendelsespost. Projektgodkenderen eller din leder gennemgår og godkender din indtastning. Hvis posten vedrører et projekt, og den godkendes, oprettes de faktiske oplysninger. Det giver mulighed for at spore omkostninger og fakturering. 

## <a name="approve-an-entry"></a>Godkend en post
Formularen **Godkendelser** giver dig mulighed for at skifte mellem forskellige visninger, så du kan få vist forskellige typer godkendelser.
  
1. Gå til formularen **Godkendelser** , og vælg **Udgifter** , **Tid** eller **Tilbagekaldelser**.
2. Gennemse de enkelte godkendelser, og vælg dem, du vil godkende.
3. Vælg **Godkend** for at godkende de markerede poster.
Disse poster behandles automatisk i systemet, og der oprettes faktiske oplysninger eller en reservation.

## <a name="reject-an-entry"></a>Afvis en post
Som projektgodkender skal du muligvis sende en post tilbage til en bruger, så brugeren kan rette den.
  
1. Gå til formularen **Godkendelser** , og vælg den post, der skal afvises. 
2. Vælg **Afvis**.
3. Valgfrit - Tilføj en kommentar i dialogboksen **Afvisningskommentarer** for at informere brugeren om, hvorfor posten afvises.
4. Vælg **OK**. Posten sendes til brugeren igen.
  
## <a name="recall-entries"></a>Tilbagekald registreringer
Du kan på et eller andet tidspunkt få brug for at tilbagekalde en indsendt post. Hvis posten ikke er godkendt, vil den blive returneret med det samme. En godkendt post kan dog have en væsentlig indvirkning. Projektgodkenderen skal godkende tilbagekaldelsen for at kunne tilbageføre transaktionen i faktiske tal.

## <a name="specify-project-approvers"></a>Angiv projektgodkendere
Hvert projekt har en række medlemmer af projektteamet. Du kan angive, hvilke teammedlemmer der også er projektgodkendere.

1. Gå til formularen **Projekter** , og åbn projektet på listen.
2. På fanen **Teams** skal du vælge det teammedlem, der skal være projektgodkender, og derefter vælge **Rediger**.
3. Vælg **Ja** i feltet **Projektgodkender**.
4. Vælg **Gem**.
5. Gentag trin 2-4 for at tilføje eller redigere flere projektgodkendere.

## <a name="configure-the-users-manager"></a>Konfigurer brugerens leder

1. Gå til **Indstillinger** > **Sikkerhed** > **Brugere**.
2. Vælg den bruger, du vil tildele en leder, og vælge derefter lederen på listen i området **Organisationsoplysninger**. 
3. Vælg **Gem**.


