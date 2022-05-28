---
title: Deaktivér prislister
description: I dette emne forklares det, hvordan du deaktiverer eller fjerner ubrugte eller gamle prislister.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ab790764f7a99118fd42bc76934105389173ff88
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596876"
---
# <a name="deactivate-price-lists"></a>Deaktivér prislister 

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Hvis du vil fjerne gamle eller ubrugte fra Dynamics 365 Project Operations, skal du fuldføre to trin. 

1. Fjern eller slet prislisten fra bestemte sider.
2. Deaktivér eller slet prislisten fra de aktive prislister på siden **Prislister**.

>[!IMPORTANT]
> Du skal fuldføre begge trin for at fjerne en prisliste fuldstændigt. Det er ikke tilstrækkeligt kun at udføre trin 2, som er at slette eller deaktivere prislisten direkte fra visningen Aktive prislister. Du skal også slette denne prislistes tilknytning fra alle de steder, der er nævnt i trin 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Slet prislisten fra bestemte sider
1. Hvis du vil slette en prisliste i Project Operations, skal du gå til følgende sider:  

      - Siden **Projektparametere** > fanen **Prislister**
      - Siden **Afdeling** > gitteret **Prislister**
      - Siden **Konto** > gitteret **Projektprislister**
      - Siden **Projekttilbud** > gitteret **Projektprislister**: Dette gælder for alle aktive projekttilbud.
      - Siden **Projektkontrakter** > gitteret **Projektprislister**: Dette gælder for alle aktive projektkontrakter.

 2. På hver enkelt side skal du vælge den prisliste, som du vil slette, og derefter vælge **Slet**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Slet eller deaktivér prislisten fra siden Prislister
 
1. Hvis du vil slette en prisliste fra de aktive prislister, skal du gå til **Salg** > **Kunder** > **Prislister**. 
2. Vælg den prisliste, som du vil slette, og vælg derefter **Slet**. Hvis der refereres til prislisten i eksisterende transaktioner, kan du ikke slette den. Hvis dette sker, kan du deaktivere prislisten, så den ikke vises i visninger. 
3. Hvis du vil deaktivere prislisten, skal du vælge prislisten igen og derefter vælge **Deaktivér**.   
