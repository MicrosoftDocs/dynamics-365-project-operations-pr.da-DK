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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992779"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="8a81c-103">Hvorfor er standardprisen for faktiske omkostningsudgifter nul</span><span class="sxs-lookup"><span data-stu-id="8a81c-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8a81c-104">Disse ofte stillede spørgsmål gælder for faktiske udgifter, hvor transaktionsklassen er indstillet til Udgift, og transaktionstypen er Omkostning.</span><span class="sxs-lookup"><span data-stu-id="8a81c-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="8a81c-105">Fejlfinding i forbindelse med omkostningssatser for faktiske omkostningsudgifter</span><span class="sxs-lookup"><span data-stu-id="8a81c-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="8a81c-106">Gå til den relaterede udgiftspost, og sørg for, at der er et beløb i udgiftspostfeltet.</span><span class="sxs-lookup"><span data-stu-id="8a81c-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="8a81c-107">Hvis beløbsfeltet ikke var udfyldt for den oprindelige udgift, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="8a81c-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="8a81c-108">Du kan løse dette problem ved at genoprette udgiftsposten med et gyldigt beløb og godkende den.</span><span class="sxs-lookup"><span data-stu-id="8a81c-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]