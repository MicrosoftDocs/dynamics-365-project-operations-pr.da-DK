---
title: Rettede fakturaer
description: Dette emne indeholder oplysninger om rettede fakturaer.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287816"
---
# <a name="corrected-invoices"></a>Rettede fakturaer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Bekræftede fakturaer kan redigeres. Når en rediger en bekræftet faktura, oprettes der en ny kladde for den rettede faktura. Da det er en forudsætning, at du vil tilbageføre alle transaktioner og antal fra den oprindelige faktura, inkluderer denne rettede faktura alle transaktioner fra den oprindelige faktura, og alle antal på fakturaen angives til nul (0).

Når der ikke skal rettes i nogen transaktioner, kan du fjerne dem fra rettelsesfakturakladden. Hvis du vil tilbageføre eller returnere en delmængde, kan du redigere feltet Antal i linjedetaljen. Hvis du åbner fakturalinjedetaljen, kan du se det oprindelige fakturaantal. Du kan derefter redigere det aktuelle fakturaantal, så det er mindre eller større end det oprindelige fakturaantal.

Når du bekræfter en rettelsesfaktura, tilbageføres det oprindeligt fakturerede salgstal, og der oprettes et nyt faktureret faktisk salgstal. Hvis mængden blev reduceret, medfører differencen, at der også oprettes et nyt ikke-faktureret faktisk salgstal. Hvis det oprindelige fakturerede salg f.eks. var otte timer, og linjedetaljen i den rettede faktura har et reduceret antal på seks timer, tilbageføres den oprindeligt fakturerede salgslinje, og der oprettes to nye faktiske salgstal:

- Et faktureret faktisk salgstal for seks timer.
- Et ikke-faktureret faktisk salgstal for de resterende to timer. Denne transaktion kan enten faktureres senere eller markeres som ikke-fakturerbar, afhængigt af forhandlingerne med kunden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]