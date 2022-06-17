---
title: Sende en ressourceanmodning
description: Denne artikel indeholder oplysninger om, hvordan du sender en anmodning om en projektressource.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c446dc0f99a5b9c9cdf3698cdf774cfd1e5d4d6a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928839"
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
