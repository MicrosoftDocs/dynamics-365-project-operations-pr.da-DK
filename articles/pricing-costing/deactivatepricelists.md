---
title: Deaktivér prislister
description: I dette emne forklares det, hvordan du deaktiverer eller fjerner ubrugte eller gamle prislister.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701920"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="b8c4d-103">Deaktivér prislister</span><span class="sxs-lookup"><span data-stu-id="b8c4d-103">Deactivate price lists</span></span> 

<span data-ttu-id="b8c4d-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b8c4d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b8c4d-105">Hvis du vil fjerne gamle eller ubrugte fra Dynamics 365 Project Operations, skal du fuldføre to trin.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="b8c4d-106">Fjern eller slet prislisten fra bestemte sider.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="b8c4d-107">Deaktivér eller slet prislisten fra de aktive prislister på siden **Prislister**.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="b8c4d-108">Du skal fuldføre begge trin for at fjerne en prisliste fuldstændigt.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="b8c4d-109">Det er ikke tilstrækkeligt kun at udføre trin 2, som er at slette eller deaktivere prislisten direkte fra visningen Aktive prislister.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="b8c4d-110">Du skal også slette denne prislistes tilknytning fra alle de steder, der er nævnt i trin 1.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="b8c4d-111">Slet prislisten fra bestemte sider</span><span class="sxs-lookup"><span data-stu-id="b8c4d-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="b8c4d-112">Hvis du vil slette en prisliste i Project Operations, skal du gå til følgende sider:</span><span class="sxs-lookup"><span data-stu-id="b8c4d-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="b8c4d-113">Siden **Projektparametere** > fanen **Prislister**</span><span class="sxs-lookup"><span data-stu-id="b8c4d-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="b8c4d-114">Siden **Afdeling** > gitteret **Prislister**</span><span class="sxs-lookup"><span data-stu-id="b8c4d-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="b8c4d-115">Siden **Konto** > gitteret **Projektprislister**</span><span class="sxs-lookup"><span data-stu-id="b8c4d-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="b8c4d-116">Siden **Projekttilbud** > gitteret **Projektprislister**: Dette gælder for alle aktive projekttilbud.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="b8c4d-117">Siden **Projektkontrakter** > gitteret **Projektprislister**: Dette gælder for alle aktive projektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="b8c4d-118">På hver enkelt side skal du vælge den prisliste, som du vil slette, og derefter vælge **Slet**.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="b8c4d-119">Slet eller deaktivér prislisten fra siden Prislister</span><span class="sxs-lookup"><span data-stu-id="b8c4d-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="b8c4d-120">Hvis du vil slette en prisliste fra de aktive prislister, skal du gå til **Salg** > **Kunder** > **Prislister**.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="b8c4d-121">Vælg den prisliste, som du vil slette, og vælg derefter **Slet**.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="b8c4d-122">Hvis der refereres til prislisten i eksisterende transaktioner, kan du ikke slette den.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="b8c4d-123">Hvis dette sker, kan du deaktivere prislisten, så den ikke vises i visninger.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="b8c4d-124">Hvis du vil deaktivere prislisten, skal du vælge prislisten igen og derefter vælge **Deaktivér**.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
