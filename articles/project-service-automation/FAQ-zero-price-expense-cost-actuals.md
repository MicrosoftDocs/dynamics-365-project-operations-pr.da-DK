---
title: Hvorfor anvendes en standardpris på nul for faktiske omkostningsudgifter?
description: Fejlfinding af, hvorfor en pris får standardværdien 0 for faktiske omkostningsudgifter.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750537"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Hvorfor anvendes en standardpris på nul for faktiske omkostningsudgifter?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse ofte stillede spørgsmål gælder for faktiske udgifter, hvor transaktionsklassen er indstillet til Udgift, og transaktionstypen er Omkostning.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Fejlfinding i forbindelse med omkostningssatser for faktiske omkostningsudgifter

Gå til den relaterede udgiftspost, og sørg for, at der er et beløb i udgiftspostfeltet. Hvis beløbsfeltet ikke var udfyldt for den oprindelige udgift, har du isoleret problemet.
 
Du kan løse dette problem ved at genoprette udgiftsposten med et gyldigt beløb og godkende den.
