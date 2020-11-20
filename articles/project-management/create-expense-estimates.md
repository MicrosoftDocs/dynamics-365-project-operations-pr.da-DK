---
title: Udgiftsestimater
description: Dette emne indeholder oplysninger om, hvordan du definerer eller estimerer projektbaserede udgifter.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131696"
---
# <a name="expense-estimates"></a><span data-ttu-id="3df61-103">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="3df61-103">Expense estimates</span></span>
<span data-ttu-id="3df61-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3df61-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3df61-105">Når der defineres ressourcebaserede estimater, giver Dynamics 365 Project Operations projektledere mulighed for at definere projektbaserede udgifter for hvert enkelt projekt.</span><span class="sxs-lookup"><span data-stu-id="3df61-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="3df61-106">De enkelte udgiftsenheder kan knyttes til en bestemt projektopgave eller udgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="3df61-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="3df61-107">Udgiftskategorier defineres typisk på organisationsniveau.</span><span class="sxs-lookup"><span data-stu-id="3df61-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="3df61-108">Prisfastsættelse for de enkelte udgiftskategorier defineres typisk i følgende hierarki:</span><span class="sxs-lookup"><span data-stu-id="3df61-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="3df61-109">Organisation</span><span class="sxs-lookup"><span data-stu-id="3df61-109">Organization</span></span>
- <span data-ttu-id="3df61-110">Kunde</span><span class="sxs-lookup"><span data-stu-id="3df61-110">Customer</span></span>
- <span data-ttu-id="3df61-111">Tilbud/kontrakt</span><span class="sxs-lookup"><span data-stu-id="3df61-111">Quote/contract</span></span>

<span data-ttu-id="3df61-112">Fuldfør følgende fremgangsmåde for at få vist, tilføje eller slette en projektudgift.</span><span class="sxs-lookup"><span data-stu-id="3df61-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="3df61-113">Gå til **Projekter**, og vælg det projekt, som du vil arbejde på.</span><span class="sxs-lookup"><span data-stu-id="3df61-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="3df61-114">Vælg fanen **Projektestimater**, og få vist listen over projektudgifter.</span><span class="sxs-lookup"><span data-stu-id="3df61-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="3df61-115">Vælg **Ny udgift** for at tilføje en udgift.</span><span class="sxs-lookup"><span data-stu-id="3df61-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="3df61-116">Du kan også vælge en udgift, du vil slette, og derefter vælge **Slet udgift**.</span><span class="sxs-lookup"><span data-stu-id="3df61-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="3df61-117">Følgende attributter defineres for de enkelte udgiftslinjeelementer:</span><span class="sxs-lookup"><span data-stu-id="3df61-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="3df61-118">**Kategori**: De almindelige grupperinger, der bruges til at beskrive alle de udgifter, der påløber et projekt.</span><span class="sxs-lookup"><span data-stu-id="3df61-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="3df61-119">**Startdato**: Den dato, hvor udgiften estimeres at skulle afholdes.</span><span class="sxs-lookup"><span data-stu-id="3df61-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="3df61-120">**Antal**: Det estimerede antal udgiftsenheder for en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="3df61-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="3df61-121">**Enhedskostpris**: Den enhedspris, der bruges til at beregne omkostningerne for udgiften.</span><span class="sxs-lookup"><span data-stu-id="3df61-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="3df61-122">**Enhedssalgspris**: Den enhedspris, der bruges til at beregne salgspriserne for udgiften.</span><span class="sxs-lookup"><span data-stu-id="3df61-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

