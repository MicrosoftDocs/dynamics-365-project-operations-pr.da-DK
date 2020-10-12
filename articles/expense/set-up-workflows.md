---
title: Konfigurer arbejdsprocesser for udgiftsstyring
description: Du kan konfigurere en arbejdsproces, der bruges til at gennemse og godkende dokumenter for rejser og udgifter.
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
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896544"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="bac15-103">Konfigurer arbejdsprocesser for udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="bac15-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="bac15-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="bac15-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bac15-105">Du kan konfigurere en arbejdsproces til at gennemse og godkende dokumenter for rejser og udgifter.</span><span class="sxs-lookup"><span data-stu-id="bac15-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="bac15-106">Du kan definere arbejdsprocesser til udgiftsrapporter, rejserekvisitioner og anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="bac15-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="bac15-107">En arbejdsproces repræsenterer en forretningsproces, der definerer, hvordan et dokument bevæger sig gennem systemet.</span><span class="sxs-lookup"><span data-stu-id="bac15-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="bac15-108">Arbejdsprocessen angiver også, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="bac15-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="bac15-109">Der er flere fordele ved at bruge arbejdsprocessystemet i din organisation:</span><span class="sxs-lookup"><span data-stu-id="bac15-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="bac15-110">**Ensartede processer** : Du kan definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="bac15-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="bac15-111">Arbejdsprocessystemet er med til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="bac15-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="bac15-112">**Processynlighed** : Du kan spore status, historik og performanceværdier for en bestemt arbejdsprocesforekomst.</span><span class="sxs-lookup"><span data-stu-id="bac15-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="bac15-113">Det hjælper dig med at afgøre, om der skal foretages ændringer af arbejdsprocessen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="bac15-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="bac15-114">**Centraliseret opgaveliste** : Brugere kan se en centraliseret opgaveliste for at få vist de arbejdsprocesopgaver og -godkendelser, de har fået tildelt.</span><span class="sxs-lookup"><span data-stu-id="bac15-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="bac15-115">Arbejdsprocestyper</span><span class="sxs-lookup"><span data-stu-id="bac15-115">Workflow types</span></span>

<span data-ttu-id="bac15-116">I følgende tabel vises de arbejdsprocestyper, som du kan oprette i **Udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="bac15-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="bac15-117"><strong>Skriv</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="bac15-118"><strong>Brug denne type for at</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="bac15-119"><strong>Automatisk godkende udgiftsrapporter</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="bac15-120">Opret godkendelsesarbejdsprocesser for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="bac15-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="bac15-121"><strong>Automatisk bogføring af udgiftsrapporter</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="bac15-122">Opret automatiske arbejdsprocesser for bogføring af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="bac15-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="bac15-123"><strong>Udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="bac15-124">Opret godkendelsesarbejdsprocesser for linjeelementer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="bac15-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="bac15-125"><strong>Automatisk bogføring af udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="bac15-126">Opret automatiske arbejdsprocesser for bogføring af linjeelementer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="bac15-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="bac15-127"><strong>Rejserekvisition</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="bac15-128">Opret godkendelsesarbejdsprocesser for rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="bac15-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="bac15-129"><strong>Anmodning om kontantforskud</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="bac15-130">Opret godkendelsesarbejdsprocesser for anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="bac15-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="bac15-131"><strong>Moms- og skatteinddrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="bac15-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="bac15-132">Opret godkendelsesarbejdsprocesser for inddrivelse af moms.</span><span class="sxs-lookup"><span data-stu-id="bac15-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |