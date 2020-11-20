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
# <a name="submitting-a-resource-request"></a><span data-ttu-id="62096-103">Sende en ressourceanmodning</span><span class="sxs-lookup"><span data-stu-id="62096-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="62096-104">Du kan sende et genereret ressourcekrav som en ressourceanmodning.</span><span class="sxs-lookup"><span data-stu-id="62096-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="62096-105">Anmodningen sendes derefter til en personalechef for at blive fuldført.</span><span class="sxs-lookup"><span data-stu-id="62096-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="62096-106">I PSA (Project Service Automation) skal du på siden **Projekter** klikke på fanen **Team** for at få vist en liste over reserverbare ressourcer.</span><span class="sxs-lookup"><span data-stu-id="62096-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="62096-107">Vælg den generiske ressource, der har et ressourcekrav, på listen, og klik derefter på **Send anmodning**.</span><span class="sxs-lookup"><span data-stu-id="62096-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Sende en ressourceanmodning](media/RM-how-to-18.png)

<span data-ttu-id="62096-109">Anmodningstatussen for det generiske teammedlem ændres til **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="62096-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="62096-110">Når anmodningen er fuldført af personalechefen, erstattes den generiske ressource af en navngivet ressource, hvis personalechefen opfylder anmodningen i form af en reservation af en navngivet ressource.</span><span class="sxs-lookup"><span data-stu-id="62096-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="62096-111">Ellers forbliver den generiske ressource i teamet, og anmodningsstatussen ændres til **Skal gennemses**, hvis personalechefen har foreslået en navngivet ressource.</span><span class="sxs-lookup"><span data-stu-id="62096-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
