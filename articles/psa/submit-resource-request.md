---
title: Sende en ressourceanmodning
description: Dette emne indeholder oplysninger om, hvordan du sender en anmodning om en projektressource.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
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
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131253"
---
# <a name="submitting-a-resource-request"></a>Sende en ressourceanmodning

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan sende et genereret ressourcekrav som en ressourceanmodning. Anmodningen sendes derefter til en personalechef for at blive fuldført.

1. I PSA (Project Service Automation) skal du på siden **Projekter** klikke på fanen **Team** for at få vist en liste over reserverbare ressourcer. 
2. Vælg den generiske ressource, der har et ressourcekrav, på listen, og klik derefter på **Send anmodning**.

![Sende en ressourceanmodning](media/RM-how-to-18.png)

Anmodningstatussen for det generiske teammedlem ændres til **Sendt**.

Når anmodningen er fuldført af personalechefen, erstattes den generiske ressource af en navngivet ressource, hvis personalechefen opfylder anmodningen i form af en reservation af en navngivet ressource. Ellers forbliver den generiske ressource i teamet, og anmodningsstatussen ændres til **Skal gennemses**, hvis personalechefen har foreslået en navngivet ressource.
