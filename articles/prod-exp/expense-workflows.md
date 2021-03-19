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
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271616"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="f657f-103">Konfigurer arbejdsprocesser for udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="f657f-103">Set up Expense management workflows</span></span>

<span data-ttu-id="f657f-104">Du kan konfigurere en arbejdsproces, der bruges til at gennemse og godkende dokumenter for rejser og udgifter.</span><span class="sxs-lookup"><span data-stu-id="f657f-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="f657f-105">Du kan definere arbejdsprocesser for dokumenter såsom udgiftsrapporter, rejserekvisitioner og anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="f657f-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="f657f-106">En arbejdsproces repræsenterer en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="f657f-106">A workflow represents a business process.</span></span> <span data-ttu-id="f657f-107">Den definerer, hvordan et dokument bevæger sig gennem systemet, og angiver, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="f657f-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="f657f-108">Der er flere fordele ved at bruge arbejdsprocessystemet i din organisation:</span><span class="sxs-lookup"><span data-stu-id="f657f-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="f657f-109">**Ensartede processer** – Du kan definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="f657f-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="f657f-110">Arbejdsprocessystemet er med til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="f657f-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="f657f-111">Processynlighed – Du kan spore status, historik og performanceværdier for en bestemt arbejdsprocesforekomst.</span><span class="sxs-lookup"><span data-stu-id="f657f-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="f657f-112">Det hjælper dig med at afgøre, om der skal foretages ændringer af arbejdsprocessen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="f657f-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="f657f-113">Centraliseret opgaveliste – Brugere kan se en centraliseret opgaveliste for at få vist de arbejdsprocesopgaver og -godkendelser, de har fået tildelt.</span><span class="sxs-lookup"><span data-stu-id="f657f-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="f657f-114">**Du kan oprette to forskellige typer af arbejdsprocesser**</span><span class="sxs-lookup"><span data-stu-id="f657f-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="f657f-115">I følgende tabel vises de arbejdsprocestyper, som du kan oprette i **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="f657f-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="f657f-116"><strong>Skriv</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="f657f-117"><strong>Brug denne type for at</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="f657f-118"><strong>Udgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="f657f-119">Opret godkendelsesarbejdsprocesser for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="f657f-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="f657f-120"><strong>Automatisk bogføring af udgiftsrapporter</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="f657f-121">Opret automatiske arbejdsprocesser for bogføring af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="f657f-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="f657f-122"><strong>Udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="f657f-123">Opret godkendelsesarbejdsprocesser for linjeelementer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="f657f-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="f657f-124"><strong>Automatisk bogføring af udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="f657f-125">Opret automatiske arbejdsprocesser for bogføring af linjeelementer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="f657f-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="f657f-126"><strong>Rejserekvisition</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="f657f-127">Opret godkendelsesarbejdsprocesser for rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="f657f-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="f657f-128"><strong>Anmodning om kontantforskud</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="f657f-129">Opret godkendelsesarbejdsprocesser for anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="f657f-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="f657f-130"><strong>Moms- og skatteinddrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="f657f-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="f657f-131">Opret godkendelsesarbejdsprocesser for inddrivelse af moms.</span><span class="sxs-lookup"><span data-stu-id="f657f-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]