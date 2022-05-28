---
title: Hvorfor anvendes en standardpris på nul for faktiske omkostningsudgifter?
description: Fejlfinding af, hvorfor en pris får standardværdien 0 for faktiske omkostningsudgifter.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7de9f660bf38629bb2af4e0fb1ebf815f5e525e2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595583"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Hvorfor er standardprisen for faktiske omkostningsudgifter nul

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse ofte stillede spørgsmål gælder for faktiske udgifter, hvor transaktionsklassen er indstillet til Udgift, og transaktionstypen er Omkostning.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Fejlfinding i forbindelse med omkostningssatser for faktiske omkostningsudgifter

Gå til den relaterede udgiftspost, og sørg for, at der er et beløb i udgiftspostfeltet. Hvis beløbsfeltet ikke var udfyldt for den oprindelige udgift, har du isoleret problemet.
 
Du kan løse dette problem ved at genoprette udgiftsposten med et gyldigt beløb og godkende den.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
