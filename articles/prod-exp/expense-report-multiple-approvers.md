---
title: Flere godkendere af en udgiftsrapport
description: Dette emne indeholder oplysninger om udgiftsrapporter, der kræver godkendelse af flere personer.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005244"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="a647d-103">Flere godkendere af en udgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="a647d-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="a647d-104">Afhængigt af din organisations politikker for godkendelse af udgifter kan mere end én person godkende en udgiftsrapport, der er indsendt af en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="a647d-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="a647d-105">Når du konfigurerer arbejdsprocessen for godkendelse af udgiftsrapporter, kan du tilføje de arbejdsproceselementer, der indeholder opgaver eller trin for en eller flere godkendere af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="a647d-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="a647d-106">Du kan f.eks. kræve, at alle udgiftsrapporter først skal godkendes af chefen for den medarbejder, der har indsendt rapporten, og dernæst af kreditorkoordinatoren.</span><span class="sxs-lookup"><span data-stu-id="a647d-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="a647d-107">Hvis du beslutter dig for at kræve flere godkendere af udgiftsrapporter, kan du tilføje arbejdsproceselementer på en af følgende måder:</span><span class="sxs-lookup"><span data-stu-id="a647d-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="a647d-108">Tilføj ét godkendelseselement, der indeholder ét trin.</span><span class="sxs-lookup"><span data-stu-id="a647d-108">Add one approval element that has one step.</span></span> <span data-ttu-id="a647d-109">Trinnet kan f.eks. kræve, at der tildeles en udgiftsrapport til en brugergruppe, og at den godkendes af 50 procent af brugergruppens medlemmer.</span><span class="sxs-lookup"><span data-stu-id="a647d-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="a647d-110">Tilføj ét godkendelseselement, der indeholder flere trin.</span><span class="sxs-lookup"><span data-stu-id="a647d-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="a647d-111">Godkendelseselementet kan f.eks. indeholde følgende trin:</span><span class="sxs-lookup"><span data-stu-id="a647d-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="a647d-112">Chefen for den medarbejder, der har indsendt udgiftsrapporten, godkender den.</span><span class="sxs-lookup"><span data-stu-id="a647d-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="a647d-113">Kreditormedarbejderen bekræfter kvitteringerne og udgiftsrapportelementerne.</span><span class="sxs-lookup"><span data-stu-id="a647d-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="a647d-114">Budgetejeren godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="a647d-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="a647d-115">Tilføj flere godkendelseselementer, der hver især har et trin.</span><span class="sxs-lookup"><span data-stu-id="a647d-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="a647d-116">Du kan f.eks. tilføje et separat godkendelseselement for hvert af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="a647d-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="a647d-117">Medarbejderens leder godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="a647d-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="a647d-118">Budgetejeren godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="a647d-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]