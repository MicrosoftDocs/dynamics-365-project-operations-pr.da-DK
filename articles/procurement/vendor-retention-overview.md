---
title: Oversigt over tilbageholdelse af leverandører
description: Dette emne indeholder en oversigt over funktionerne for tilbageholdelse af leverandører.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f9e4a1e63e47524bb622771f645c04e61c279496
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588453"
---
# <a name="vendor-retention-overview"></a>Oversigt over tilbageholdelse af leverandører

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Organisationen ønsker måske at tilbage en del af betalingerne til leverandører, der arbejder på projekter for din organisation. Før du betaler leverandøren, kan du f.eks. sikre dig, at de varer og tjenester, som denne har leveret, lever op til dine forventninger.

Når du forhandler indkøb for projekter med leverandører, kan du angive de betingelser for tilbageholdelse af leverandører, som omfatter den procentdel eller det beløb, der skal tilbageholdes. Når leverandøren leverer varer og tjenester, skal du trække den angivne tilbageholdelsesprocentprocent eller det angivne beløb fra din betaling til leverandøren. Når projektet er fuldført, eller når det når en midlertidig fase som angivet i leverandørkontrakten, frigiver du det tilbageholdte beløb og opretter en betaling til leverandøren.

## <a name="vendor-retention-example"></a>Eksempel på tilbageholdelse af leverandør

I følgende eksempel vises det, hvordan en procentdel af et beløb på en faktura til en leverandør tilbageholdes på baggrund af den procentdel, som projektet er blevet fuldført.

Contoso Robotics USA har indgået aftale med leverandøren Fabrikam om at levere 100 timers træning i udstyrsfornyelsesprojektet. Den samlede kontraktværdi er 30.000 USD, og den aftale købspris er 300 USD i timen.

Træningen sker i tre faser med følgende tidsplan:

- Fase 1: 50 timer eller 50 procent af projektet
- Fase 2: 30 timer eller 80 procent af projektet i alt
- Fase 3: 20 timer eller 100 procent af projektet

I følgende tabel vises betingelserne for tilbageholdelse.

| **Procentdel af leverede enheder** | **Procentdel, der skal tilbageholdes** | **Procentdel, der skal frigives** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100% | 0 % | 100% |

Transaktionerne resulterer i følgende beløb:

- Fase 1:
  - Det beløb, der skal betales, er 50 x 300 eller 15.000.
  - 20 procent af beløbet, eller 3.000, tilbageholdes og frigives i en senere fase.
  - Det beløb, der betales til leverandøren, er 12.000.
- Fase 2:
  - Det beløb, der skal betales, er 30 x 300 eller 9.000.
  - 10 procent af beløbet, eller 900, tilbageholdes.
  - 10 procent af de 3.000, der blev tilbageholdt i fase 1, eller 300, frigives.
  - Det beløb, der betales til leverandøren, er 8.400. Dette beløb er 9.000 mindre end de 900, der er blevet tilbageholdt, plus de 300, der blev frigivet fra fase 1-tilbageholdelsen.
- Fase 3:
  - Det beløb, der skal betales, er 20 x 300 eller 6.000.
  - Der tilbageholdes ikke noget beløb.
  - Det frigivne beløb er 3.600. Dette beløb består af de 3.000, der blev tilbageholdt i fase 1, minus de 300 fra fase 1, der blev frigivet i fase 2, plus de 900, der blev tilbageholdt i fase 2.
  - Det beløb, der betales til leverandøren, er 9.600. Dette beløb består af det tilbageholdte beløb på 3.600 plus de 6.000 for fuldførelse i fase 3.

Det samlede beløb, der er blevet betalt til leverandøren, når de tre faser er fuldført, er 30.000, som er det samlede beløb på købsordren (15.000 + 9.000 + 6.000).
