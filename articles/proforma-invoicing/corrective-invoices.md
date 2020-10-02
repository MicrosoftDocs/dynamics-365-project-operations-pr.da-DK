---
title: Rettede fakturaer
description: Dette emne indeholder oplysninger om rettede fakturaer.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898074"
---
# <a name="corrected-invoices"></a>Rettede fakturaer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Bekræftede fakturaer kan redigeres. Når en rediger en bekræftet faktura, oprettes der en ny kladde for den rettede faktura. Da det er en forudsætning, at du vil tilbageføre alle transaktioner og antal fra den oprindelige faktura, inkluderer denne rettede faktura alle transaktioner fra den oprindelige faktura, og alle antal på fakturaen angives til nul (0).

Når der ikke skal rettes i nogen transaktioner, kan du fjerne dem fra rettelsesfakturakladden. Hvis du vil tilbageføre eller returnere en delmængde, kan du redigere feltet Antal i linjedetaljen. Hvis du åbner fakturalinjedetaljen, kan du se det oprindelige fakturaantal. Du kan derefter redigere det aktuelle fakturaantal, så det er mindre eller større end det oprindelige fakturaantal.

Når du bekræfter en rettelsesfaktura, tilbageføres det oprindeligt fakturerede salgstal, og der oprettes et nyt faktureret faktisk salgstal. Hvis mængden blev reduceret, medfører differencen, at der også oprettes et nyt ikke-faktureret faktisk salgstal. Hvis det oprindelige fakturerede salg f.eks. var otte timer, og linjedetaljen i den rettede faktura har et reduceret antal på seks timer, tilbageføres den oprindeligt fakturerede salgslinje, og der oprettes to nye faktiske salgstal:

- Et faktureret faktisk salgstal for seks timer.
- Et ikke-faktureret faktisk salgstal for de resterende to timer. Denne transaktion kan enten faktureres senere eller markeres som ikke-fakturerbar, afhængigt af forhandlingerne med kunden.
