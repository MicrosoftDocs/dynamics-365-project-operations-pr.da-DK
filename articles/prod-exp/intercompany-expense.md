---
title: Interne udgifter
description: Dette emne indeholder oplysninger om, hvordan du kan bruge interne udgifter til at tildele en medarbejders udgifter til den juridiske enhed, som arbejdet er udført for.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684222"
---
# <a name="intercompany-expenses"></a>Interne udgifter

En arbejder, der er ansat i én juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation. Du kan bruge interne udgifter til at tildele arbejderens udgifter til den juridiske enhed, som arbejdet er udført for. Den juridiske enhed, hvor arbejderen er ansat, kaldes den juridiske udlånsenhed. Den juridiske enhed, som arbejderen afholder udgifter for, kaldes den juridiske låneenhed. 

Før en medarbejder kan oprette og indsende interne udgifter, skal du aktivere de interne udgiftslinjer. I den juridiske låneenhed skal du på siden **Parametre for administration af udgifter** vælge **Tillad interne udgiftslinjer**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Momsbogføring for interne udgifter

[!include [banner](../includes/banner.md)]

Før du kan bruge momsgrupper, der er knyttet til den juridiske låneenhed (kilde) i stedet for den juridiske udlånsenhed (destination), i udgiftsrapporten skal du aktivere funktionaliteten i opsætningen af moms i finanskladden. Når parameteren **Juridisk enhed for intern momsbogføring** angives til **Kilde**, og **Anvend regler for moms** angives til **Nej**, bruges momskombination for den juridiske låneenhed. Når den samme parameter er angivet til **Destination**, bruges momskombinationen for den juridiske låneenhed. For juridiske enheder i USA, hvor parameteren er angivet til **Kilde**, skal feltet **Salgsmoms** også konfigureres på den nye side for **Finanskonteringsgrupper**. Regnskabsprogrammet bruger oplysningerne fra dette felt i forbindelse med momsrelateret regnskabspostering.   
Funktionsmåden er den samme for de udgiftslinjer, der bogføres med eller uden et projekt.  

## <a name="new-expense-expression-builder"></a>Ny udtrykgenerator for udgifter

Den nye udtryksgenerator for udgifter løser problemer med interne udgiftsscenarier, der bruger projekter. Denne funktion sikrer, at udgiftspolitikken valideres korrekt i forhold til det projekt, der er valgt på udgiftslinjen, når du opretter en intern udgift, og at udgiftsrapporten kan sendes korrekt.

Hvis udtryksgeneratoren for udgifter skal fungere, skal den være aktiveret. Derudover skal den udgiftspolitik, der har et projekt-id, konfigureres.

Hvis du allerede har konfigureret politikker, der validerer projekt-id'et på udgiftslinjen, skal disse politikker være udgået. Du kan derefter aktivere funktionen og omkonfigurere politikkerne.

Benyt følgende fremgangsmåde for at aktivere disse funktioner.

1. Gå til **Arbejdspladser** \> **Funktionsstyring**.
2. Vælg **Ny udtryksgenerator for udgifter, der skal løse problemer med interne udgiftsscenarier, der bruger projekter** på listen. Vælg derefter **Aktivér nu**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
