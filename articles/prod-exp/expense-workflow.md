---
title: Arbejdsproces for udgiftsstyring
description: I dette emne forklares det, hvordan du kan bruge arbejdsprocessystemet i Microsoft Dynamics 365 Finance til at oprette en revisionsproces for udgiftsrapporter i udgiftsstyring.
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
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271661"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="50cfa-103">Arbejdsproces for udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="50cfa-103">Expense management workflow</span></span>

<span data-ttu-id="50cfa-104">Du kan bruge arbejdsprocessystemet til at oprette en revisionsproces for udgiftsrapporter i udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="50cfa-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="50cfa-105">Du kan konfigurere en arbejdsproces, der bruger følgende kriterier til at afgøre, hvem der skal godkende udgiftsrapporter:</span><span class="sxs-lookup"><span data-stu-id="50cfa-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="50cfa-106">Medarbejderens rapporteringshierarki og foruddefinerede godkendelsesgrænser</span><span class="sxs-lookup"><span data-stu-id="50cfa-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="50cfa-107">Godkendelse på flere niveauer, der understøtter midlertidige godkendere og en endelig godkender</span><span class="sxs-lookup"><span data-stu-id="50cfa-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="50cfa-108">Økonomiske dimensioner og projektansvar</span><span class="sxs-lookup"><span data-stu-id="50cfa-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="50cfa-109">Tildeling til bestemte brugere eller brugergrupper</span><span class="sxs-lookup"><span data-stu-id="50cfa-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="50cfa-110">Det er muligt at oprette arbejdsprocesgodkendelser for udgiftsrapporter, rejserekvisitioner, kontantforskud og momsopkrævning.</span><span class="sxs-lookup"><span data-stu-id="50cfa-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="50cfa-111">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="50cfa-111">**Example**</span></span>

<span data-ttu-id="50cfa-112">Følgende proces er et eksempel på arbejdsprocessen for udgiftsstyring for en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="50cfa-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="50cfa-113">En medarbejder opretter og gemmer en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="50cfa-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="50cfa-114">Medarbejderen indsender udgiftsrapporten til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="50cfa-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="50cfa-115">Godkenderen identificeres på baggrund af de regler, der blev defineret under opsætningen af arbejdsprocessen.</span><span class="sxs-lookup"><span data-stu-id="50cfa-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="50cfa-116">Godkenderen modtager en meddelelse om, at en udgiftsrapport er klar til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="50cfa-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="50cfa-117">Godkenderen gennemser udgiftsrapporten og bekræfter, at følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="50cfa-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="50cfa-118">Udgifterne overtræder ikke nogen udgiftspolitikker.</span><span class="sxs-lookup"><span data-stu-id="50cfa-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="50cfa-119">Hvis en udgift overtræder en politik, kontrollerer godkenderen, at udgiftsrapporten indeholder en gyldig forretningsmæssig berettigelse.</span><span class="sxs-lookup"><span data-stu-id="50cfa-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="50cfa-120">Elektroniske kvitteringer er vedhæftet udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="50cfa-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="50cfa-121">Godkenderen godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="50cfa-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="50cfa-122">Udgiftsrapporten tildeles kreditorkoordinatoren med henblik på bogføring.</span><span class="sxs-lookup"><span data-stu-id="50cfa-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="50cfa-123">Et af følgende trin indtræffer, afhængigt af om der er konfigureret automatisk bogføring:</span><span class="sxs-lookup"><span data-stu-id="50cfa-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="50cfa-124">Hvis der er konfigureret automatisk bogføring, behandles udgiftsrapporten med henblik på betaling, og udgiftsrapportens status opdateres.</span><span class="sxs-lookup"><span data-stu-id="50cfa-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="50cfa-125">Hvis der ikke er konfigureret automatisk bogføring, bekræfter kreditorkoordinatoren, at alle oprindelige kvitteringer er blevet indsendt, og at kvitteringerne er afstemt med udgifterne i udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="50cfa-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="50cfa-126">Alle de momskoder, der er angivet i udgiftsrapporten, skal også verificeres som værende korrekte.</span><span class="sxs-lookup"><span data-stu-id="50cfa-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="50cfa-127">Når disse krav er kontrolleret, bogføres udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="50cfa-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="50cfa-128">Når udgiftsrapporten er bogført, godkendes betalingen i udgiftsrapporten, og medarbejderen refunderes.</span><span class="sxs-lookup"><span data-stu-id="50cfa-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]