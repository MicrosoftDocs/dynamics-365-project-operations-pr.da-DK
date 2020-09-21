---
title: Sende en ressourceanmodning
description: Dette emne indeholder oplysninger om, hvordan du sender en anmodning om en projektressource.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750590"
---
# <a name="submit-a-resource-request"></a>Sende en ressourceanmodning

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan sende et genereret ressourcekrav som en ressourceanmodning. Anmodningen sendes derefter til en personalechef for at blive fuldført.

1. I PSA (Project Service Automation) skal du på siden **Projekter** klikke på fanen **Team** for at få vist en liste over reserverbare ressourcer. 
2. Vælg den generiske ressource, der har et ressourcekrav, på listen, og klik derefter på **Send anmodning**.

![Sende en ressourceanmodning](media/RM-how-to-18.png)

Anmodningstatussen for det generiske teammedlem ændres til **Sendt**.

Når anmodningen er fuldført af personalechefen, erstattes den generiske ressource af en navngivet ressource, hvis personalechefen opfylder anmodningen i form af en reservation af en navngivet ressource. Ellers forbliver den generiske ressource i teamet, og anmodningsstatussen ændres til **Skal gennemses**, hvis personalechefen har foreslået en navngivet ressource.
