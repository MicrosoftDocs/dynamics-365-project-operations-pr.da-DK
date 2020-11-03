---
title: Udgiftspost (lille)
description: Dette emne indeholder oplysninger om, hvordan du kan arbejde med udgiftsposter i en lille udrulning.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074056"
---
# <a name="expense-entry-lite"></a>Udgiftspost (lille)

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Grundlæggende eller lille, udgiftsstyring er muligheden for at registrere simple udgifter. Du kan registrere udgifter i et projekt, hvorefter projektgodkenderen vil gennemgå og godkende dem.

Du kan finde flere oplysninger om udgiftsfunktioner i Dynamics 365 Project Operations under [Udgiftsoversigt](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Indlæs en grundlæggende udgift

Du kan indlæse dine udgifter, så du kan sende dem til godkenderen.

1. Gå til **Udgifter** , og vælg **Ny**.
2. Angiv de krævede udgiftsoplysninger på siden **Ny udgift** , og vælg derefter **Gem**.

## <a name="submit-a-basic-expense"></a>Indsend en grundlæggende udgift

Når du er færdig med at indlæse alle udgifterne, og du er klar til at godkende dem, skal de sendes.

1. Gå til **Udgifter** , og vælg en udgift. Du kan også vælge at markere alle udgifterne ved hjælp af afkrydsningsfeltet i overskriften.
2. Vælg **Send**. Systemet behandler de valgte poster og opretter derefter anmodninger om godkendelse af udgifter.

## <a name="recall-a-basic-expense"></a>Tilbagekald en grundlæggende udgift

Når du indsender en udgift ved en fejl, kan du tilbagekalde den. Den tid, der kræves for at tilbagekalde en udgiftspost, afhænger af godkendelsesfasen.  Hvis godkenderen endnu ikke har godkendt posten, kan tilbagekaldelsen ske med det samme. Men hvis posten allerede er godkendt, bliver godkenderen bedt om at godkende tilbagekaldelsen og tilbageføre transaktionerne.

1. Gå til **Udgifter** , og vælg derefter de udgifter, der skal tilbagekaldes, på listen over udgifter.
2. Vælg **Tilbagekalde**. Hvis udgiftsposten endnu ikke er godkendt, tilbagekalder systemet dem straks. Hvis udgiftsposten allerede er blevet godkendt, oprettes der en anmodning om tilbagekaldelse for underrette godkenderen om, at du vil tilbageføre udgiften. Godkenderen bekræfter derefter, at tilbageførslen kan udføres, og posten bliver returneret.

## <a name="delete-a-basic-expense"></a>Slet en grundlæggende udgift

Udgifter, der endnu ikke er indsendt, kan slettes. Hvis du vil slette en udgift, der allerede er indsendt, skal du først tilbagekalde den.

## <a name="see-also"></a>Se også

- [Godkendelsesoversigt](../approvals/approvals-overview.md)
