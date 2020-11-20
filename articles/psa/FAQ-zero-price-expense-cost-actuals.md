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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122111"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="ee248-103">Hvorfor anvendes en standardpris på nul for faktiske omkostningsudgifter?</span><span class="sxs-lookup"><span data-stu-id="ee248-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ee248-104">Disse ofte stillede spørgsmål gælder for faktiske udgifter, hvor transaktionsklassen er indstillet til Udgift, og transaktionstypen er Omkostning.</span><span class="sxs-lookup"><span data-stu-id="ee248-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="ee248-105">Fejlfinding i forbindelse med omkostningssatser for faktiske omkostningsudgifter</span><span class="sxs-lookup"><span data-stu-id="ee248-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="ee248-106">Gå til den relaterede udgiftspost, og sørg for, at der er et beløb i udgiftspostfeltet.</span><span class="sxs-lookup"><span data-stu-id="ee248-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="ee248-107">Hvis beløbsfeltet ikke var udfyldt for den oprindelige udgift, har du isoleret problemet.</span><span class="sxs-lookup"><span data-stu-id="ee248-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="ee248-108">Du kan løse dette problem ved at genoprette udgiftsposten med et gyldigt beløb og godkende den.</span><span class="sxs-lookup"><span data-stu-id="ee248-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
