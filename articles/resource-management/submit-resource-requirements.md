---
title: Send en anmodning om ressource(r)
description: Du kan sende et genereret ressourcekrav som en ressourceanmodning. Anmodningen sendes derefter til en personalechef for at blive fuldført.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014019"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="4d0de-104">Send en anmodning om ressource(r)</span><span class="sxs-lookup"><span data-stu-id="4d0de-104">Submit a resource request</span></span>

<span data-ttu-id="4d0de-105">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="4d0de-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d0de-106">Du kan sende et genereret ressourcekrav som en ressourceanmodning.</span><span class="sxs-lookup"><span data-stu-id="4d0de-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="4d0de-107">Anmodningen sendes derefter til en personalechef for at blive fuldført.</span><span class="sxs-lookup"><span data-stu-id="4d0de-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="4d0de-108">I Dynamics 365 Project Operations skal du på siden **Projekter** vælge på fanen **Team** for at få vist en liste over reserverbare ressourcer.</span><span class="sxs-lookup"><span data-stu-id="4d0de-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="4d0de-109">Vælg den generiske ressource, der har et ressourcekrav, på listen, og klik derefter på **Send anmodning**.</span><span class="sxs-lookup"><span data-stu-id="4d0de-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="4d0de-110">Anmodningstatussen for det generiske teammedlem ændres til **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="4d0de-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="4d0de-111">Når anmodningen er fuldført erstattes den generiske ressource af en navngivet ressource, hvis Resource Manageren opfylder anmodningen ved at reservere en navngivet ressource.</span><span class="sxs-lookup"><span data-stu-id="4d0de-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="4d0de-112">Ellers forbliver den generiske ressource i teamet, og anmodningsstatussen ændres til **Skal gennemses**, hvis personalechefen har foreslået en navngivet ressource.</span><span class="sxs-lookup"><span data-stu-id="4d0de-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]