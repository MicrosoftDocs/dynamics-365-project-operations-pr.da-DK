---
title: Konfigurer arbejdsprocesser for udgiftsstyring
description: Du kan konfigurere en arbejdsproces til at gennemse og godkende dokumenter for rejser og udgifter.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960510"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="ac530-103">Konfigurer arbejdsprocesser for udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="ac530-103">Set up Expense management workflows</span></span>

<span data-ttu-id="ac530-104">Du kan konfigurere en arbejdsproces, der bruges til at gennemse og godkende dokumenter for rejser og udgifter.</span><span class="sxs-lookup"><span data-stu-id="ac530-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="ac530-105">Du kan definere arbejdsprocesser for dokumenter såsom udgiftsrapporter, rejserekvisitioner og anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="ac530-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="ac530-106">En arbejdsproces repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="ac530-106">A workflow represents a business process.</span></span> <span data-ttu-id="ac530-107">Den definerer, hvordan et dokument bevæger sig gennem systemet, og angiver, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="ac530-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ac530-108">Der er flere fordele ved at bruge arbejdsprocessystemet i din organisation:</span><span class="sxs-lookup"><span data-stu-id="ac530-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="ac530-109">**Ensartede processer** – Du kan definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="ac530-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ac530-110">Arbejdsprocessystemet er med til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="ac530-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="ac530-111">Processynlighed – Du kan spore status, historik og performanceværdier for en bestemt arbejdsprocesforekomst.</span><span class="sxs-lookup"><span data-stu-id="ac530-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ac530-112">Det hjælper dig med at afgøre, om der skal foretages ændringer af arbejdsprocessen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="ac530-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="ac530-113">Centraliseret opgaveliste – Brugere kan se en centraliseret opgaveliste for at få vist de arbejdsprocesopgaver og -godkendelser, de har fået tildelt.</span><span class="sxs-lookup"><span data-stu-id="ac530-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="ac530-114">**Du kan oprette to forskellige typer af arbejdsprocesser**</span><span class="sxs-lookup"><span data-stu-id="ac530-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="ac530-115">I følgende tabel vises de arbejdsprocestyper, som du kan oprette i **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="ac530-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="ac530-116"><strong>Skriv</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="ac530-117"><strong>Brug denne type for at</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="ac530-118"><strong>Udgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="ac530-119">Opret godkendelsesarbejdsprocesser for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="ac530-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="ac530-120"><strong>Automatisk bogføring af udgiftsrapporter</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="ac530-121">Opret automatiske arbejdsprocesser for bogføring af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="ac530-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="ac530-122"><strong>Udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="ac530-123">Opret godkendelsesarbejdsprocesser for linjeelementer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="ac530-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="ac530-124"><strong>Automatisk bogføring af udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="ac530-125">Opret automatiske arbejdsprocesser for bogføring af linjeelementer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="ac530-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="ac530-126"><strong>Rejserekvisition</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="ac530-127">Opret godkendelsesarbejdsprocesser for rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="ac530-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="ac530-128"><strong>Anmodning om kontantforskud</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="ac530-129">Opret godkendelsesarbejdsprocesser for anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="ac530-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="ac530-130"><strong>Moms- og skatteinddrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="ac530-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="ac530-131">Opret godkendelsesarbejdsprocesser for inddrivelse af moms.</span><span class="sxs-lookup"><span data-stu-id="ac530-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

