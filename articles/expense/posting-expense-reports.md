---
title: Bogfør udgiftsrapporter
description: I denne artikel forklares det, hvordan du kan bogføre udgiftsrapporter.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524862"
---
# <a name="post-expense-reports"></a>Bogfør udgiftsrapporter

Når en udgiftsrapport er godkendt og overført til finanskladden, kan den bogføres. Når du bogfører en udgiftsrapport, identificeres de udgifter, der er berettiget til inddrivelse af moms. Den medarbejder, der er ansvarlig for at kontrollere udgiftsrapporten, tildeles opgaven med at bekræfte og inddrive momsbetalinger.

Hvis udgifter i en udgiftsrapport skal overføres til en anden virksomhed end den virksomhed, hvor medarbejderen er ansat, skal du kontrollere begge de firmaer, som udgifterne udbetales til, og den virksomhed, hvor de har tilgodehavender. Den medarbejder, der har indsendt en udgiftsrapport, kan f.eks. være ansat i virksomheden DAT, men fakturerede en udgift til virksomheden DIR. I dette tilfælde er DAT det firma, som udgiften skyldes til, og DIR er det firma, som skylder udgiften. Når du har kontrolleret disse kladdelinjer, kan du bogføre udgiftslinjerne i finanskladden.

Hvis du vil bogføre en udgiftsrapport, skal du på siden **Godkend udgiftsrapporter** vælge den godkendte udgiftsrapport og derefter vælge **Bogfør** i handlingsruden.

Du kan også bogføre alle udgiftsrapporter på listen på én gang. Vælg alle udgiftsrapporter, og vælg derefter **Bogfør**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Aktivere funktionen Mulighed for at bogføre udgifter i leverandørens valuta for kontantbetalingsmetoden

Funktionen **Mulighed for at bogføre udgifter i leverandørens valuta for kontantbetalingsmetoden** gør det muligt at bogføre udgiftsrapporter i en leverandørvaluta for kontantbetalingsmetoden.

Når du sender kontante udgifter, bogføres udgiftsrapporter i regnskabsvalutaen. På grund af beløbskonvertering mellem transaktionsvalutaen, regnskabsvalutaen og leverandørvalutaen betales der et forkert beløb til leverandører, hvis transaktionsdatoen for udgifterne og den faktiske betalingsdato har forskellige valutakurser.

Denne funktion sikrer, at kreditorsaldoen registreres i leverandørvalutaen, når udgiftsrapporten bogføres.

1. Gå til **Arbejdspladser** \> **Funktionsstyring**.
2. På listen skal du søge efter og vælge **Mulighed for at bogføre udgifter i leverandørens valuta for kontantbetalingsmetoden** og derefter vælge **Aktivér nu**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
