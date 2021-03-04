---
title: Interne udgifter
description: Dette emne indeholder oplysninger om, hvordan du kan bruge interne udgifter til at tildele en medarbejders udgifter til den juridiske enhed, som arbejdet er udført for.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960825"
---
# <a name="intercompany-expenses"></a>Interne udgifter

En arbejder, der er ansat i én juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation. Du kan bruge interne udgifter til at tildele arbejderens udgifter til den juridiske enhed, som arbejdet er udført for. Den juridiske enhed, hvor arbejderen er ansat, kaldes den juridiske udlånsenhed. Den juridiske enhed, som arbejderen afholder udgifter for, kaldes den juridiske låneenhed. 

Før en medarbejder kan oprette og indsende interne udgifter, skal du aktivere de interne udgiftslinjer. I den juridiske låneenhed skal du på siden **Parametre for administration af udgifter** vælge **Tillad interne udgiftslinjer**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Momsbogføring for interne udgifter

[!include [banner](../includes/banner.md)]

Før du kan bruge momsgrupper, der er knyttet til den juridiske låneenhed (kilde) i stedet for den juridiske udlånsenhed (destination), i udgiftsrapporten skal du aktivere funktionaliteten i opsætningen af moms i finanskladden. Når parameteren **Juridisk enhed for intern momsbogføring** angives til **Kilde**, og **Anvend regler for moms** angives til **Nej**, bruges momskombination for den juridiske låneenhed. Når den samme parameter er angivet til **Destination**, bruges momskombinationen for den juridiske låneenhed. For juridiske enheder i USA, hvor parameteren er angivet til **Kilde**, skal feltet **Salgsmoms** også konfigureres på den nye side for **Finanskonteringsgrupper**. Regnskabsprogrammet bruger oplysningerne fra dette felt i forbindelse med momsrelateret regnskabspostering.   
Funktionsmåden er den samme for de udgiftslinjer, der bogføres med eller uden et projekt.  
