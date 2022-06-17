---
title: Hvorfor kan jeg ikke slette poster fra objektet med faktiske oplysninger?
description: Denne artikel indeholder oplysninger om, hvorfor du ikke kan slette poster fra objektet med faktiske værdier.
author: JPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925573"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Hvorfor kan jeg ikke slette poster fra objektet med faktiske oplysninger?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Project Service Automation (PSA) kan du ikke slette faktiske oplysninger, fordi de tjener som sand kilde for transaktioner, der har økonomiske konsekvenser for de efterfølgende systemer, f.eks. finansregnskabet. Hvis faktiske oplysninger kunne slettes, kunne der blive stillet spørgsmål ved integriteten af økonomiske rapporteringstransaktioner. For at kunne etablere et revisionsspor skal kunderne bruge kladder til at oprette kompensationstransaktioner.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
