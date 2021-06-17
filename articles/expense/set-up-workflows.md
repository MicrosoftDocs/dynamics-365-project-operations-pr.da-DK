---
title: Konfigurer arbejdsprocesser for udgiftsstyring
description: Du kan konfigurere en arbejdsproces, der bruges til at gennemse og godkende dokumenter for rejser og udgifter.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001014"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="44755-103">Konfigurer arbejdsprocesser for udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="44755-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="44755-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="44755-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44755-105">Du kan konfigurere en arbejdsproces til at gennemse og godkende dokumenter for rejser og udgifter.</span><span class="sxs-lookup"><span data-stu-id="44755-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="44755-106">Du kan definere arbejdsprocesser til udgiftsrapporter, rejserekvisitioner og anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="44755-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="44755-107">En arbejdsproces repræsenterer en forretningsproces, der definerer, hvordan et dokument bevæger sig gennem systemet.</span><span class="sxs-lookup"><span data-stu-id="44755-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="44755-108">Arbejdsprocessen angiver også, hvem der skal udføre en opgave eller godkende et dokument.</span><span class="sxs-lookup"><span data-stu-id="44755-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="44755-109">Der er flere fordele ved at bruge arbejdsprocessystemet i din organisation:</span><span class="sxs-lookup"><span data-stu-id="44755-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="44755-110">**Ensartede processer** : Du kan definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="44755-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="44755-111">Arbejdsprocessystemet er med til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.</span><span class="sxs-lookup"><span data-stu-id="44755-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="44755-112">**Processynlighed** : Du kan spore status, historik og performanceværdier for en bestemt arbejdsprocesforekomst.</span><span class="sxs-lookup"><span data-stu-id="44755-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="44755-113">Det hjælper dig med at afgøre, om der skal foretages ændringer af arbejdsprocessen for at forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="44755-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="44755-114">**Centraliseret opgaveliste** : Brugere kan se en centraliseret opgaveliste for at få vist de arbejdsprocesopgaver og -godkendelser, de har fået tildelt.</span><span class="sxs-lookup"><span data-stu-id="44755-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="44755-115">Arbejdsprocestyper</span><span class="sxs-lookup"><span data-stu-id="44755-115">Workflow types</span></span>

<span data-ttu-id="44755-116">I følgende tabel vises de arbejdsprocestyper, som du kan oprette i **Udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="44755-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="44755-117"><strong>Skriv</strong></span><span class="sxs-lookup"><span data-stu-id="44755-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="44755-118"><strong>Brug denne type for at</strong></span><span class="sxs-lookup"><span data-stu-id="44755-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="44755-119"><strong>Automatisk godkende udgiftsrapporter</strong></span><span class="sxs-lookup"><span data-stu-id="44755-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="44755-120">Opret godkendelsesarbejdsprocesser for udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="44755-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="44755-121"><strong>Automatisk bogføring af udgiftsrapporter</strong></span><span class="sxs-lookup"><span data-stu-id="44755-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="44755-122">Opret automatiske arbejdsprocesser for bogføring af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="44755-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="44755-123"><strong>Udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="44755-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="44755-124">Opret godkendelsesarbejdsprocesser for linjeelementer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="44755-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="44755-125"><strong>Automatisk bogføring af udgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="44755-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="44755-126">Opret automatiske arbejdsprocesser for bogføring af linjeelementer i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="44755-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="44755-127"><strong>Rejserekvisition</strong></span><span class="sxs-lookup"><span data-stu-id="44755-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="44755-128">Opret godkendelsesarbejdsprocesser for rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="44755-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="44755-129"><strong>Anmodning om kontantforskud</strong></span><span class="sxs-lookup"><span data-stu-id="44755-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="44755-130">Opret godkendelsesarbejdsprocesser for anmodninger om kontantforskud.</span><span class="sxs-lookup"><span data-stu-id="44755-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="44755-131"><strong>Moms- og skatteinddrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="44755-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="44755-132">Opret godkendelsesarbejdsprocesser for inddrivelse af moms.</span><span class="sxs-lookup"><span data-stu-id="44755-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]