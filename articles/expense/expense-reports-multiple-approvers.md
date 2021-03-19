---
title: Udgiftsrapporter og flere godkendere
description: Dette emne indeholder oplysninger om udgiftsrapporter, der kræver godkendelse af mere end én person.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276521"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="86f25-103">Udgiftsrapporter og flere godkendere</span><span class="sxs-lookup"><span data-stu-id="86f25-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="86f25-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="86f25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="86f25-105">Afhængigt af din organisations politikker for godkendelse af udgifter kan mere end én person godkende en indsendt udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="86f25-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="86f25-106">Når du konfigurerer arbejdsprocessen for godkendelse af udgiftsrapporter, kan du tilføje de arbejdsproceselementer, der indeholder opgaver eller trin for en eller flere godkendere af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="86f25-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="86f25-107">Du kan f.eks. kræve, at alle udgiftsrapporter skal godkendes af to forskellige personer, chefen for den medarbejder, der har indsendt rapporten, og kreditorkoordinatoren.</span><span class="sxs-lookup"><span data-stu-id="86f25-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="86f25-108">Hvis du beslutter dig for at kræve flere godkendere af udgiftsrapporter, kan du tilføje arbejdsproceselementer på en af følgende måder:</span><span class="sxs-lookup"><span data-stu-id="86f25-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="86f25-109">Tilføj ét godkendelseselement, der indeholder ét trin.</span><span class="sxs-lookup"><span data-stu-id="86f25-109">Add one approval element that has one step.</span></span> <span data-ttu-id="86f25-110">Trinnet kan f.eks. kræve, at der tildeles en udgiftsrapport til en brugergruppe, og at den godkendes af 50 procent af brugergruppens medlemmer.</span><span class="sxs-lookup"><span data-stu-id="86f25-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="86f25-111">Tilføj ét godkendelseselement, der indeholder flere trin.</span><span class="sxs-lookup"><span data-stu-id="86f25-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="86f25-112">Godkendelseselementet kan f.eks. indeholde følgende trin:</span><span class="sxs-lookup"><span data-stu-id="86f25-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="86f25-113">Chefen for den medarbejder, der har indsendt udgiftsrapporten, godkender den.</span><span class="sxs-lookup"><span data-stu-id="86f25-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="86f25-114">Kreditormedarbejderen bekræfter kvitteringerne og udgiftsrapportelementerne.</span><span class="sxs-lookup"><span data-stu-id="86f25-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="86f25-115">Budgetejeren godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="86f25-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="86f25-116">Tilføj flere godkendelseselementer, der hver især har et trin.</span><span class="sxs-lookup"><span data-stu-id="86f25-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="86f25-117">Du kan f.eks. tilføje et separat godkendelseselement for hvert af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="86f25-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="86f25-118">Medarbejderens leder godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="86f25-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="86f25-119">Budgetejeren godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="86f25-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]