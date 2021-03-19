---
title: Opret prognosemodeller for projektbudgetter
description: I dette emne beskrives det, hvordan du kan oprette en prognosemodel for resterende budgetter.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271031"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="c75b4-103">Opret prognosemodeller for projektbudgetter</span><span class="sxs-lookup"><span data-stu-id="c75b4-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c75b4-104">I dette emne beskrives det, hvordan du kan oprette en prognosemodel for resterende budgetter.</span><span class="sxs-lookup"><span data-stu-id="c75b4-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="c75b4-105">I et projekt, der er underlagt budgetstyring, bruges der to typer budgetter: oprindelig og resterende.</span><span class="sxs-lookup"><span data-stu-id="c75b4-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="c75b4-106">Når du opretter et projektbudget, skal du angive de oprindelige og resterende budgetprognosemodeller, der er oprettet på siden **Prognosemodeller**.</span><span class="sxs-lookup"><span data-stu-id="c75b4-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="c75b4-107">Projektbudgetter, der er baseret på de angivne modeller, oprettes, når du bekræfter projektbudgettet.</span><span class="sxs-lookup"><span data-stu-id="c75b4-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="c75b4-108">En prognosemodel, der bruges til budgetstyring, kan ikke have en undermodel eller bruges som undermodel.</span><span class="sxs-lookup"><span data-stu-id="c75b4-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="c75b4-109">Vælg **Projektstyring og regnskab** > **Opsætning** > **Prognoser**  > **Prognosemodeller**.</span><span class="sxs-lookup"><span data-stu-id="c75b4-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="c75b4-110">Vælg **Ny** for at oprette en ny budgetmodel, og angiv derefter et model-id-nummer og et navn for den nye model.</span><span class="sxs-lookup"><span data-stu-id="c75b4-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="c75b4-111">Angiv indstillingen **Afbrudt** til **Ja** for at forhindre ændringer af prognoselinjerne i prognosemodellen.</span><span class="sxs-lookup"><span data-stu-id="c75b4-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="c75b4-112">Hvis de prognoselinjer, som modellen er knyttet til, skal oprette likviditetsprognoser i finansbogholderiet, skal du angive **Inkluder i likviditetsprognoser** til **Ja.**</span><span class="sxs-lookup"><span data-stu-id="c75b4-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="c75b4-113">Hvis du vil bruge projektdatoen som fakturadatoen, skal du angive **Prognosefakturadato** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c75b4-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="c75b4-114">I feltet **Budgettype** skal du vælge en af følgende modeltyper:</span><span class="sxs-lookup"><span data-stu-id="c75b4-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="c75b4-115">**Oprindeligt budget**: Brug de oprindelige budgetbeløb, der er bindende, når det første budget oprettes og godkendes.</span><span class="sxs-lookup"><span data-stu-id="c75b4-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="c75b4-116">**Resterende budget**: Brug de resterende budgetbeløb i projektets levetid.</span><span class="sxs-lookup"><span data-stu-id="c75b4-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="c75b4-117">Saldiene i denne prognosemodel reduceres med faktiske transaktioner og forøges eller formindskes via budgetrevisioner.</span><span class="sxs-lookup"><span data-stu-id="c75b4-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="c75b4-118">**Overfør**: Brug overførte budgetbeløb til projektet.</span><span class="sxs-lookup"><span data-stu-id="c75b4-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="c75b4-119">Overførsel er en valgfri proces, der kan køres for at overføre ubrugte budgetbeløb fra et regnskabsår til et andet.</span><span class="sxs-lookup"><span data-stu-id="c75b4-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="c75b4-120">Angiv følgende indstillinger efter behov:</span><span class="sxs-lookup"><span data-stu-id="c75b4-120">Set the following options as required:</span></span>

   - <span data-ttu-id="c75b4-121">Aktiver **Prognosefakturadato** for at bruge projektdataene som fakturadato.</span><span class="sxs-lookup"><span data-stu-id="c75b4-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="c75b4-122">Aktivér **Prognose med IGVA** for at udarbejde en prognose, der er baseret på igangværende arbejde, og vælg derefter typen af IGVA.</span><span class="sxs-lookup"><span data-stu-id="c75b4-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="c75b4-123">Du kan bevare standarden **Budgettype** som **Ingen** eller angive en ny type.</span><span class="sxs-lookup"><span data-stu-id="c75b4-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="c75b4-124">Budgettypen kan ikke ændres, når du har ændret en post.</span><span class="sxs-lookup"><span data-stu-id="c75b4-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="c75b4-125">Hvis du ændrer standardbudgettypen, vil alle andre indstillinger ikke være tilgængelige for opdateringer, og du kan ikke genbruge denne prognosemodel.</span><span class="sxs-lookup"><span data-stu-id="c75b4-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]