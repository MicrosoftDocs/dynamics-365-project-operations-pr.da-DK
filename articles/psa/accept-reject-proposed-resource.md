---
title: Acceptere eller afvise en foreslået projektressource
description: Denne emne indeholder oplysninger om, hvordan du godkender eller afviser en foreslået projektressource.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/07/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 4c10c55961c74c2dc53fabd1d041a935ca9a4870
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074336"
---
# <a name="accept-or-reject-a-proposed-project-resource"></a>Acceptere eller afvise en foreslået projektressource

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Denne emne indeholder oplysninger om, hvordan du godkender eller afviser en foreslået projektressource.

Når en ressourcestyring foreslår, at en navngivet ressource skal udfylde den generiske ressourceanmodning for et projekt, opdateres feltet **Anmodningsstatus** for det generiske teammedlem til **Skal gennemses**. Anmodningen sendes til projektlederen til godkendelse eller afvisning.

![Generisk teammedlem med et forslag](media/RM-how-to-19.png)

Gitteret under fanen **Foreslåede ressourcer** på siden **Medlem af projektteam** viser den foreslåede ressources aktuelle reservationer. Når forslaget er accepteret, opdateres gitteret, så det afspejler denne reservation. 

Hvis du vil acceptere den foreslåede ressource og reservere ressourcen i dit team, skal du klikke på **Acceptér forslag**.  
Hvis du vil afvise forslaget, skal du klikke på **Afvis ressource**.

![Acceptere et ressourceforslag](media/RM-how-to-20.png) 

På samme måde, som når du direkte opfylder en generisk ressourceanmodning med en navngivet ressource, erstattes den generiske ressource, og de tildelte opgaver opdateres med det navngivne teammedlem.
