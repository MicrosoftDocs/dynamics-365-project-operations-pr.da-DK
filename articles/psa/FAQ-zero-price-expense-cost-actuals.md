---
title: Hvorfor anvendes en standardpris på nul for faktiske omkostningsudgifter?
description: Fejlfinding af, hvorfor en pris får standardværdien 0 for faktiske omkostningsudgifter.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285836"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Hvorfor er standardprisen for faktiske omkostningsudgifter nul

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse ofte stillede spørgsmål gælder for faktiske udgifter, hvor transaktionsklassen er indstillet til Udgift, og transaktionstypen er Omkostning.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Fejlfinding i forbindelse med omkostningssatser for faktiske omkostningsudgifter

Gå til den relaterede udgiftspost, og sørg for, at der er et beløb i udgiftspostfeltet. Hvis beløbsfeltet ikke var udfyldt for den oprindelige udgift, har du isoleret problemet.
 
Du kan løse dette problem ved at genoprette udgiftsposten med et gyldigt beløb og godkende den.


[!INCLUDE[footer-include](../includes/footer-banner.md)]