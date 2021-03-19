---
title: Udgiftspost (lille)
description: Dette emne indeholder oplysninger om, hvordan du kan arbejde med udgiftsposter i en lille udrulning.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276746"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="614f6-103">Udgiftspost (lille)</span><span class="sxs-lookup"><span data-stu-id="614f6-103">Expense entry (lite)</span></span>

<span data-ttu-id="614f6-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="614f6-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="614f6-105">Grundlæggende eller lille, udgiftsstyring er muligheden for at registrere simple udgifter.</span><span class="sxs-lookup"><span data-stu-id="614f6-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="614f6-106">Du kan registrere udgifter i et projekt, hvorefter projektgodkenderen vil gennemgå og godkende dem.</span><span class="sxs-lookup"><span data-stu-id="614f6-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="614f6-107">Du kan finde flere oplysninger om udgiftsfunktioner i Dynamics 365 Project Operations under [Udgiftsoversigt](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="614f6-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="614f6-108">Indlæs en grundlæggende udgift</span><span class="sxs-lookup"><span data-stu-id="614f6-108">Capture a basic expense</span></span>

<span data-ttu-id="614f6-109">Du kan indlæse dine udgifter, så du kan sende dem til godkenderen.</span><span class="sxs-lookup"><span data-stu-id="614f6-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="614f6-110">Gå til **Udgifter**, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="614f6-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="614f6-111">Angiv de krævede udgiftsoplysninger på siden **Ny udgift**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="614f6-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="614f6-112">Indsend en grundlæggende udgift</span><span class="sxs-lookup"><span data-stu-id="614f6-112">Submit a basic expense</span></span>

<span data-ttu-id="614f6-113">Når du er færdig med at indlæse alle udgifterne, og du er klar til at godkende dem, skal de sendes.</span><span class="sxs-lookup"><span data-stu-id="614f6-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="614f6-114">Gå til **Udgifter**, og vælg en udgift.</span><span class="sxs-lookup"><span data-stu-id="614f6-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="614f6-115">Du kan også vælge at markere alle udgifterne ved hjælp af afkrydsningsfeltet i overskriften.</span><span class="sxs-lookup"><span data-stu-id="614f6-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="614f6-116">Vælg **Send**.</span><span class="sxs-lookup"><span data-stu-id="614f6-116">Select **Submit**.</span></span> <span data-ttu-id="614f6-117">Systemet behandler de valgte poster og opretter derefter anmodninger om godkendelse af udgifter.</span><span class="sxs-lookup"><span data-stu-id="614f6-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="614f6-118">Tilføj en vedhæftet fil</span><span class="sxs-lookup"><span data-stu-id="614f6-118">Add an attachment</span></span>

<span data-ttu-id="614f6-119">Det kan være nødvendigt at give godkenderen yderligere dokumentation om din udgift.</span><span class="sxs-lookup"><span data-stu-id="614f6-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="614f6-120">Du kan vedhæfte en kvittering i tidslinjen for udgiftsposten.</span><span class="sxs-lookup"><span data-stu-id="614f6-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="614f6-121">Vælg **Rediger** i sektionen **Tidslinje**, og vælg derefter papirclips-ikonet for at vedhæfte kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="614f6-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="614f6-122">Tilbagekald en grundlæggende udgift</span><span class="sxs-lookup"><span data-stu-id="614f6-122">Recall a basic expense</span></span>

<span data-ttu-id="614f6-123">Når du indsender en udgift ved en fejl, kan du tilbagekalde den.</span><span class="sxs-lookup"><span data-stu-id="614f6-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="614f6-124">Den tid, der kræves for at tilbagekalde en udgiftspost, afhænger af godkendelsesfasen.</span><span class="sxs-lookup"><span data-stu-id="614f6-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="614f6-125">Hvis godkenderen endnu ikke har godkendt posten, kan tilbagekaldelsen ske med det samme.</span><span class="sxs-lookup"><span data-stu-id="614f6-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="614f6-126">Men hvis posten allerede er godkendt, bliver godkenderen bedt om at godkende tilbagekaldelsen og tilbageføre transaktionerne.</span><span class="sxs-lookup"><span data-stu-id="614f6-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="614f6-127">Gå til **Udgifter**, og vælg derefter de udgifter, der skal tilbagekaldes, på listen over udgifter.</span><span class="sxs-lookup"><span data-stu-id="614f6-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="614f6-128">Vælg **Tilbagekalde**.</span><span class="sxs-lookup"><span data-stu-id="614f6-128">Select **Recall**.</span></span> <span data-ttu-id="614f6-129">Hvis udgiftsposten endnu ikke er godkendt, tilbagekalder systemet dem straks.</span><span class="sxs-lookup"><span data-stu-id="614f6-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="614f6-130">Hvis udgiftsposten allerede er blevet godkendt, oprettes der en anmodning om tilbagekaldelse for underrette godkenderen om, at du vil tilbageføre udgiften.</span><span class="sxs-lookup"><span data-stu-id="614f6-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="614f6-131">Godkenderen bekræfter derefter, at tilbageførslen kan udføres, og posten bliver returneret.</span><span class="sxs-lookup"><span data-stu-id="614f6-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="614f6-132">Slet en grundlæggende udgift</span><span class="sxs-lookup"><span data-stu-id="614f6-132">Delete a basic expense</span></span>

<span data-ttu-id="614f6-133">Udgifter, der endnu ikke er indsendt, kan slettes.</span><span class="sxs-lookup"><span data-stu-id="614f6-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="614f6-134">Hvis du vil slette en udgift, der allerede er indsendt, skal du først tilbagekalde den.</span><span class="sxs-lookup"><span data-stu-id="614f6-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="614f6-135">Se også</span><span class="sxs-lookup"><span data-stu-id="614f6-135">See also</span></span>

- [<span data-ttu-id="614f6-136">Godkendelsesoversigt</span><span class="sxs-lookup"><span data-stu-id="614f6-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]