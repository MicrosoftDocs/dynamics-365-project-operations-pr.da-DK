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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="9f4e1-103">Hvorfor anvendes en standardpris på nul for faktiske omkostningsudgifter?</span><span class="sxs-lookup"><span data-stu-id="9f4e1-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9f4e1-104">Disse ofte stillede spørgsmål gælder for faktiske udgifter, hvor transaktionsklassen er indstillet til Udgift, og transaktionstypen er Omkostning.</span><span class="sxs-lookup"><span data-stu-id="9f4e1-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="9f4e1-105">Fejlfinding i forbindelse med omkostningssatser for faktiske omkostningsudgifter</span><span class="sxs-lookup"><span data-stu-id="9f4e1-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="9f4e1-106">Gå til den relaterede udgiftspost, og sørg for, at der er et beløb i udgiftspostfeltet.</span><span class="sxs-lookup"><span data-stu-id="9f4e1-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="9f4e1-107">Hvis beløbsfeltet ikke var udfyldt for den oprindelige udgift, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="9f4e1-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="9f4e1-108">Du kan løse dette problem ved at genoprette udgiftsposten med et gyldigt beløb og godkende den.</span><span class="sxs-lookup"><span data-stu-id="9f4e1-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
