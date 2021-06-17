---
title: Pr. dag
description: Dette emne indeholder oplysninger om de diætregler, der bruges i udgiftsstyring.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995254"
---
# <a name="per-diems"></a>Pr. dag

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_


En diæt er en godtgørelse, der udbetales til en arbejder, der rejser i forbindelse med arbejde. I udgiftsstyring kan du oprette diætregler for forskellige rejsesituationer. Diætsatser kan være baseret på tidspunktet for året, rejselokationen eller begge. Når du opretter en diætregel, kan du angive, at en procentdel af diætsatsen skal tilbageholdes, hvis en arbejder modtager gratis måltider eller servicer. Du kan også angive en nedre og øvre grænse for antallet af timer, hvor diætsatsen skal finde anvendelse på en arbejders rejse.

## <a name="configuration"></a>Konfiguration 

1. Hvis du vil tilføje diætlokationer, skal du gå til **Konfigurer** > **Beregninger og koder** > **Diætlokation**.
2. Vælg en diætsats og valuta, der er gyldig i perioden mellem en bestemt start- og slutdato, for hotel, måltider og andre udgifter for hver af de lokationer, der er tilføjet ovenfor. Diætsatser og valutaer konfigureres under **Konfigurer** > **Beregninger og koder** > **Diæter**.
3. På siden **Diætlokationer** skal du konfigurere niveauerne for diætsatser. Diætsatsniveauer giver dig mulighed for at definere den procentvise opdeling af et dagligt tilskud til hotel, måltider og andre udgifter. 
4. Hvis du vil angive den procentvise måltidsreduktion for morgenmad, frokost eller aftensmad, skal du opdatere felterne på siden med **Parametre til udgiftsstyring** under fanen **Diæter**. 
    
## <a name="submit-expenses-using-per-diem"></a>Indsend udgifter ved hjælp af diæter
Hvis du vil indsende udgifter, der anvender diæter, skal du bruge udgiftskategorien **Diæter**, når du opretter en udgiftsrapport. Angiv **Diæt fra dato**, **Diæt til dato** og **Diætlokation**. Beløbet vil blive beregnet på baggrund af diætsatserne for den valgte lokation, og reduktionen af måltid beregnes på baggrund af diætsatsniveauerne.


[!INCLUDE[footer-include](../includes/footer-banner.md)]