---
title: Hvorfor kan jeg ikke slette poster fra objektet med faktiske oplysninger?
description: Denne emne indeholder oplysninger om, hvorfor du ikke kan slette poster fra objektet med faktiske oplysninger.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148951"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="5685a-103">Hvorfor kan jeg ikke slette poster fra objektet med faktiske oplysninger?</span><span class="sxs-lookup"><span data-stu-id="5685a-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5685a-104">I Project Service Automation (PSA) kan du ikke slette faktiske oplysninger, fordi de tjener som sand kilde for transaktioner, der har økonomiske konsekvenser for de efterfølgende systemer, f.eks. finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="5685a-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="5685a-105">Hvis faktiske oplysninger kunne slettes, kunne der blive stillet spørgsmål ved integriteten af økonomiske rapporteringstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="5685a-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="5685a-106">For at kunne etablere et revisionsspor skal kunderne bruge kladder til at oprette kompensationstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="5685a-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

