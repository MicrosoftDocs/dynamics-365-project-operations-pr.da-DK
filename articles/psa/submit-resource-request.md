---
title: Sende en ressourceanmodning
description: Dette emne indeholder oplysninger om, hvordan du sender en anmodning om en projektressource.
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
ms.openlocfilehash: da3e2798079816409ffbcfed911c05f3d51307fef22c48d112802927828faeb2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6984955"
---
# <a name="submitting-a-resource-request"></a>Sende en ressourceanmodning

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan sende et genereret ressourcekrav som en ressourceanmodning. Anmodningen sendes derefter til en personalechef for at blive fuldført.

1. I PSA (Project Service Automation) skal du på siden **Projekter** klikke på fanen **Team** for at få vist en liste over reserverbare ressourcer. 
2. Vælg den generiske ressource, der har et ressourcekrav, på listen, og klik derefter på **Send anmodning**.

![Indsendelse af en ressourceanmodning.](media/RM-how-to-18.png)

Anmodningstatussen for det generiske teammedlem ændres til **Sendt**.

Når anmodningen er fuldført af personalechefen, erstattes den generiske ressource af en navngivet ressource, hvis personalechefen opfylder anmodningen i form af en reservation af en navngivet ressource. Ellers forbliver den generiske ressource i teamet, og anmodningsstatussen ændres til **Skal gennemses**, hvis personalechefen har foreslået en navngivet ressource.


[!INCLUDE[footer-include](../includes/footer-banner.md)]