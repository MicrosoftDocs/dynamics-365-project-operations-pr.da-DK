---
title: Interne udgifter
description: En arbejder, der er ansat i én juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation. I denne situation kan du bruge funktionen til interne udgifter til at tildele arbejderens udgifter til den juridiske enhed, som arbejdet blev udført for.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074323"
---
# <a name="intercompany-expenses"></a>Interne udgifter

[!include [banner](../includes/banner.md)]

En arbejder, der er ansat i én juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation. I denne situation kan du bruge funktionen til interne udgifter til at tildele arbejderens udgifter til den juridiske enhed, som arbejdet blev udført for. Den juridiske enhed, hvor arbejderen er ansat, kaldes den juridiske udlånsenhed. Den juridiske enhed, som arbejderen afholder udgifter for, kaldes den juridiske låneenhed. 

Før en arbejder kan oprette og indsende udgifter for arbejde, der er blevet udført for en anden juridisk enhed, skal du i den juridiske udlånsenhed på siden **Parametre for udgiftsstyring** vælge indstillingen **Tillad interne udgiftslinjer**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Momsbogføring for interne udgifter

[!include [banner](../includes/banner.md)]

Hvis du vil bruge de momsgrupper, der er knyttet til den juridiske udlånsenhed (kilden) i stedet for den juridiske låneenhed (destination) i udgiftsrapporten, skal du konfigurere dette i momsopsætningen for finansbogholderiet. Når parameteren for finansbogholderiet i den **Juridiske enhed til intern momsbogføring** er angivet til **Kilde** , og **Anvend regler for moms** er angivet til **Nej** , vil momskombinationen for den juridiske udlånsenhed blive brugt. Når den samme parameter er angivet til **Destination** , bruges momskombinationen for den juridiske låneenhed. For juridiske enheder i USA, hvor parameteren er angivet til **Kilde** , skal feltet **Salgsmoms** også konfigureres på den nye side for **Finanskonteringsgrupper**. I regnskabsprogrammet bruges oplysningerne fra dette felt i forbindelse med momsrelateret regnskabspostering.   
Funktionsmåden er den samme for de udgiftslinjer, der bogføres med eller uden et projekt.  
