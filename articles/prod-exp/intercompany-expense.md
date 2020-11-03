---
title: Interne udgifter
description: En arbejder, der er ansat i én juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation. I denne situation kan du bruge funktionen til interne udgifter til at tildele arbejderens udgifter til den juridiske enhed, som arbejdet blev udført for.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074323"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="63819-104">Interne udgifter</span><span class="sxs-lookup"><span data-stu-id="63819-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63819-105">En arbejder, der er ansat i én juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation.</span><span class="sxs-lookup"><span data-stu-id="63819-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="63819-106">I denne situation kan du bruge funktionen til interne udgifter til at tildele arbejderens udgifter til den juridiske enhed, som arbejdet blev udført for.</span><span class="sxs-lookup"><span data-stu-id="63819-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="63819-107">Den juridiske enhed, hvor arbejderen er ansat, kaldes den juridiske udlånsenhed.</span><span class="sxs-lookup"><span data-stu-id="63819-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="63819-108">Den juridiske enhed, som arbejderen afholder udgifter for, kaldes den juridiske låneenhed.</span><span class="sxs-lookup"><span data-stu-id="63819-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="63819-109">Før en arbejder kan oprette og indsende udgifter for arbejde, der er blevet udført for en anden juridisk enhed, skal du i den juridiske udlånsenhed på siden **Parametre for udgiftsstyring** vælge indstillingen **Tillad interne udgiftslinjer**.</span><span class="sxs-lookup"><span data-stu-id="63819-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="63819-110">Momsbogføring for interne udgifter</span><span class="sxs-lookup"><span data-stu-id="63819-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63819-111">Hvis du vil bruge de momsgrupper, der er knyttet til den juridiske udlånsenhed (kilden) i stedet for den juridiske låneenhed (destination) i udgiftsrapporten, skal du konfigurere dette i momsopsætningen for finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="63819-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="63819-112">Når parameteren for finansbogholderiet i den **Juridiske enhed til intern momsbogføring** er angivet til **Kilde** , og **Anvend regler for moms** er angivet til **Nej** , vil momskombinationen for den juridiske udlånsenhed blive brugt.</span><span class="sxs-lookup"><span data-stu-id="63819-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="63819-113">Når den samme parameter er angivet til **Destination** , bruges momskombinationen for den juridiske låneenhed.</span><span class="sxs-lookup"><span data-stu-id="63819-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="63819-114">For juridiske enheder i USA, hvor parameteren er angivet til **Kilde** , skal feltet **Salgsmoms** også konfigureres på den nye side for **Finanskonteringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="63819-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="63819-115">I regnskabsprogrammet bruges oplysningerne fra dette felt i forbindelse med momsrelateret regnskabspostering.</span><span class="sxs-lookup"><span data-stu-id="63819-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="63819-116">Funktionsmåden er den samme for de udgiftslinjer, der bogføres med eller uden et projekt.</span><span class="sxs-lookup"><span data-stu-id="63819-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
