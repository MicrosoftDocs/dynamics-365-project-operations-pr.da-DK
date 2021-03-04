---
title: Interne udgifter
description: Dette emne indeholder oplysninger om, hvordan du kan bruge interne udgifter til at tildele en medarbejders udgifter til den juridiske enhed, som arbejdet er udført for.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960825"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="316b5-103">Interne udgifter</span><span class="sxs-lookup"><span data-stu-id="316b5-103">Intercompany expenses</span></span>

<span data-ttu-id="316b5-104">En arbejder, der er ansat i én juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation.</span><span class="sxs-lookup"><span data-stu-id="316b5-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="316b5-105">Du kan bruge interne udgifter til at tildele arbejderens udgifter til den juridiske enhed, som arbejdet er udført for.</span><span class="sxs-lookup"><span data-stu-id="316b5-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="316b5-106">Den juridiske enhed, hvor arbejderen er ansat, kaldes den juridiske udlånsenhed.</span><span class="sxs-lookup"><span data-stu-id="316b5-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="316b5-107">Den juridiske enhed, som arbejderen afholder udgifter for, kaldes den juridiske låneenhed.</span><span class="sxs-lookup"><span data-stu-id="316b5-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="316b5-108">Før en medarbejder kan oprette og indsende interne udgifter, skal du aktivere de interne udgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="316b5-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="316b5-109">I den juridiske låneenhed skal du på siden **Parametre for administration af udgifter** vælge **Tillad interne udgiftslinjer**.</span><span class="sxs-lookup"><span data-stu-id="316b5-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="316b5-110">Momsbogføring for interne udgifter</span><span class="sxs-lookup"><span data-stu-id="316b5-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="316b5-111">Før du kan bruge momsgrupper, der er knyttet til den juridiske låneenhed (kilde) i stedet for den juridiske udlånsenhed (destination), i udgiftsrapporten skal du aktivere funktionaliteten i opsætningen af moms i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="316b5-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="316b5-112">Når parameteren **Juridisk enhed for intern momsbogføring** angives til **Kilde**, og **Anvend regler for moms** angives til **Nej**, bruges momskombination for den juridiske låneenhed.</span><span class="sxs-lookup"><span data-stu-id="316b5-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="316b5-113">Når den samme parameter er angivet til **Destination**, bruges momskombinationen for den juridiske låneenhed.</span><span class="sxs-lookup"><span data-stu-id="316b5-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="316b5-114">For juridiske enheder i USA, hvor parameteren er angivet til **Kilde**, skal feltet **Salgsmoms** også konfigureres på den nye side for **Finanskonteringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="316b5-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="316b5-115">Regnskabsprogrammet bruger oplysningerne fra dette felt i forbindelse med momsrelateret regnskabspostering.</span><span class="sxs-lookup"><span data-stu-id="316b5-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="316b5-116">Funktionsmåden er den samme for de udgiftslinjer, der bogføres med eller uden et projekt.</span><span class="sxs-lookup"><span data-stu-id="316b5-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
