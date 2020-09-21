---
title: Hvorfor kan jeg ikke slette poster fra objektet med faktiske oplysninger?
description: Denne emne indeholder oplysninger om, hvorfor du ikke kan slette poster fra objektet med faktiske oplysninger.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750498"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Hvorfor kan jeg ikke slette poster fra objektet med faktiske oplysninger?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Project Service Automation (PSA) kan du ikke slette faktiske oplysninger, fordi de tjener som sand kilde for transaktioner, der har økonomiske konsekvenser for de efterfølgende systemer, f.eks. finansregnskabet. Hvis faktiske oplysninger kunne slettes, kunne der blive stillet spørgsmål ved integriteten af økonomiske rapporteringstransaktioner. For at kunne etablere et revisionsspor skal kunderne bruge kladder til at oprette kompensationstransaktioner.

