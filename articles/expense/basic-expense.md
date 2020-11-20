---
title: Udgiftspost (lille)
description: Dette emne indeholder oplysninger om, hvordan du kan arbejde med udgiftsposter i en lille udrulning.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121076"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="8f085-103">Udgiftspost (lille)</span><span class="sxs-lookup"><span data-stu-id="8f085-103">Expense entry (lite)</span></span>

<span data-ttu-id="8f085-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="8f085-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8f085-105">Grundlæggende eller lille, udgiftsstyring er muligheden for at registrere simple udgifter.</span><span class="sxs-lookup"><span data-stu-id="8f085-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="8f085-106">Du kan registrere udgifter i et projekt, hvorefter projektgodkenderen vil gennemgå og godkende dem.</span><span class="sxs-lookup"><span data-stu-id="8f085-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="8f085-107">Du kan finde flere oplysninger om udgiftsfunktioner i Dynamics 365 Project Operations under [Udgiftsoversigt](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8f085-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="8f085-108">Indlæs en grundlæggende udgift</span><span class="sxs-lookup"><span data-stu-id="8f085-108">Capture a basic expense</span></span>

<span data-ttu-id="8f085-109">Du kan indlæse dine udgifter, så du kan sende dem til godkenderen.</span><span class="sxs-lookup"><span data-stu-id="8f085-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="8f085-110">Gå til **Udgifter**, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8f085-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="8f085-111">Angiv de krævede udgiftsoplysninger på siden **Ny udgift**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8f085-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="8f085-112">Indsend en grundlæggende udgift</span><span class="sxs-lookup"><span data-stu-id="8f085-112">Submit a basic expense</span></span>

<span data-ttu-id="8f085-113">Når du er færdig med at indlæse alle udgifterne, og du er klar til at godkende dem, skal de sendes.</span><span class="sxs-lookup"><span data-stu-id="8f085-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="8f085-114">Gå til **Udgifter**, og vælg en udgift.</span><span class="sxs-lookup"><span data-stu-id="8f085-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="8f085-115">Du kan også vælge at markere alle udgifterne ved hjælp af afkrydsningsfeltet i overskriften.</span><span class="sxs-lookup"><span data-stu-id="8f085-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="8f085-116">Vælg **Send**.</span><span class="sxs-lookup"><span data-stu-id="8f085-116">Select **Submit**.</span></span> <span data-ttu-id="8f085-117">Systemet behandler de valgte poster og opretter derefter anmodninger om godkendelse af udgifter.</span><span class="sxs-lookup"><span data-stu-id="8f085-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="8f085-118">Tilbagekald en grundlæggende udgift</span><span class="sxs-lookup"><span data-stu-id="8f085-118">Recall a basic expense</span></span>

<span data-ttu-id="8f085-119">Når du indsender en udgift ved en fejl, kan du tilbagekalde den.</span><span class="sxs-lookup"><span data-stu-id="8f085-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="8f085-120">Den tid, der kræves for at tilbagekalde en udgiftspost, afhænger af godkendelsesfasen.</span><span class="sxs-lookup"><span data-stu-id="8f085-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="8f085-121">Hvis godkenderen endnu ikke har godkendt posten, kan tilbagekaldelsen ske med det samme.</span><span class="sxs-lookup"><span data-stu-id="8f085-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="8f085-122">Men hvis posten allerede er godkendt, bliver godkenderen bedt om at godkende tilbagekaldelsen og tilbageføre transaktionerne.</span><span class="sxs-lookup"><span data-stu-id="8f085-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="8f085-123">Gå til **Udgifter**, og vælg derefter de udgifter, der skal tilbagekaldes, på listen over udgifter.</span><span class="sxs-lookup"><span data-stu-id="8f085-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="8f085-124">Vælg **Tilbagekalde**.</span><span class="sxs-lookup"><span data-stu-id="8f085-124">Select **Recall**.</span></span> <span data-ttu-id="8f085-125">Hvis udgiftsposten endnu ikke er godkendt, tilbagekalder systemet dem straks.</span><span class="sxs-lookup"><span data-stu-id="8f085-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="8f085-126">Hvis udgiftsposten allerede er blevet godkendt, oprettes der en anmodning om tilbagekaldelse for underrette godkenderen om, at du vil tilbageføre udgiften.</span><span class="sxs-lookup"><span data-stu-id="8f085-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="8f085-127">Godkenderen bekræfter derefter, at tilbageførslen kan udføres, og posten bliver returneret.</span><span class="sxs-lookup"><span data-stu-id="8f085-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="8f085-128">Slet en grundlæggende udgift</span><span class="sxs-lookup"><span data-stu-id="8f085-128">Delete a basic expense</span></span>

<span data-ttu-id="8f085-129">Udgifter, der endnu ikke er indsendt, kan slettes.</span><span class="sxs-lookup"><span data-stu-id="8f085-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="8f085-130">Hvis du vil slette en udgift, der allerede er indsendt, skal du først tilbagekalde den.</span><span class="sxs-lookup"><span data-stu-id="8f085-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f085-131">Se også</span><span class="sxs-lookup"><span data-stu-id="8f085-131">See also</span></span>

- [<span data-ttu-id="8f085-132">Godkendelsesoversigt</span><span class="sxs-lookup"><span data-stu-id="8f085-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
