---
title: Udgiftsrapporter og flere godkendere
description: Dette emne indeholder oplysninger om udgiftsrapporter, der kræver godkendelse af mere end én person.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897084"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="89e6a-103">Udgiftsrapporter og flere godkendere</span><span class="sxs-lookup"><span data-stu-id="89e6a-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="89e6a-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="89e6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="89e6a-105">Afhængigt af din organisations politikker for godkendelse af udgifter kan mere end én person godkende en indsendt udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="89e6a-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="89e6a-106">Når du konfigurerer arbejdsprocessen for godkendelse af udgiftsrapporter, kan du tilføje de arbejdsproceselementer, der indeholder opgaver eller trin for en eller flere godkendere af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="89e6a-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="89e6a-107">Du kan f.eks. kræve, at alle udgiftsrapporter skal godkendes af to forskellige personer, chefen for den medarbejder, der har indsendt rapporten, og kreditorkoordinatoren.</span><span class="sxs-lookup"><span data-stu-id="89e6a-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="89e6a-108">Hvis du beslutter dig for at kræve flere godkendere af udgiftsrapporter, kan du tilføje arbejdsproceselementer på en af følgende måder:</span><span class="sxs-lookup"><span data-stu-id="89e6a-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="89e6a-109">Tilføj ét godkendelseselement, der indeholder ét trin.</span><span class="sxs-lookup"><span data-stu-id="89e6a-109">Add one approval element that has one step.</span></span> <span data-ttu-id="89e6a-110">Trinnet kan f.eks. kræve, at der tildeles en udgiftsrapport til en brugergruppe, og at den godkendes af 50 procent af brugergruppens medlemmer.</span><span class="sxs-lookup"><span data-stu-id="89e6a-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="89e6a-111">Tilføj ét godkendelseselement, der indeholder flere trin.</span><span class="sxs-lookup"><span data-stu-id="89e6a-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="89e6a-112">Godkendelseselementet kan f.eks. indeholde følgende trin:</span><span class="sxs-lookup"><span data-stu-id="89e6a-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="89e6a-113">Chefen for den medarbejder, der har indsendt udgiftsrapporten, godkender den.</span><span class="sxs-lookup"><span data-stu-id="89e6a-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="89e6a-114">Kreditormedarbejderen bekræfter kvitteringerne og udgiftsrapportelementerne.</span><span class="sxs-lookup"><span data-stu-id="89e6a-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="89e6a-115">Budgetejeren godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="89e6a-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="89e6a-116">Tilføj flere godkendelseselementer, der hver især har et trin.</span><span class="sxs-lookup"><span data-stu-id="89e6a-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="89e6a-117">Du kan f.eks. tilføje et separat godkendelseselement for hvert af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="89e6a-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="89e6a-118">Medarbejderens leder godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="89e6a-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="89e6a-119">Budgetejeren godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="89e6a-119">The budget owner approves the expense report.</span></span>
