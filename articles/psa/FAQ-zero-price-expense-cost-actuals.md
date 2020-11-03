---
title: Hvorfor anvendes en standardpris på nul for faktiske omkostningsudgifter?
description: Fejlfinding af, hvorfor en pris får standardværdien 0 for faktiske omkostningsudgifter.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074193"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Hvorfor anvendes en standardpris på nul for faktiske omkostningsudgifter?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse ofte stillede spørgsmål gælder for faktiske udgifter, hvor transaktionsklassen er indstillet til Udgift, og transaktionstypen er Omkostning.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Fejlfinding i forbindelse med omkostningssatser for faktiske omkostningsudgifter

Gå til den relaterede udgiftspost, og sørg for, at der er et beløb i udgiftspostfeltet. Hvis beløbsfeltet ikke var udfyldt for den oprindelige udgift, har du isoleret problemet.
 
Du kan løse dette problem ved at genoprette udgiftsposten med et gyldigt beløb og godkende den.
