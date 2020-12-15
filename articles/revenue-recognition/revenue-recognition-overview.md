---
title: Oversigt over omsætningsanerkendelse
description: Dette emne indeholder oplysninger om omsætningsanerkendelse i Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531392"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="4de42-103">Oversigt over omsætningsanerkendelse</span><span class="sxs-lookup"><span data-stu-id="4de42-103">Revenue recognition overview</span></span>

<span data-ttu-id="4de42-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="4de42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4de42-105">I Dynamics 365 Project Operations varierer principperne for omsætningsanerkendelse på baggrund af den valgte faktureringsmetode for et projekt eller en del af projektet.</span><span class="sxs-lookup"><span data-stu-id="4de42-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="4de42-106">Dette emne indeholder oplysninger om omsætningsanerkendelse i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4de42-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="4de42-107">Transaktioner, der bogføres i regnskabet, og som anvender faktureringsmetoden for tids- og materialer</span><span class="sxs-lookup"><span data-stu-id="4de42-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="4de42-108">Omkostnings- og omsætningsanerkendelse er forbundet.</span><span class="sxs-lookup"><span data-stu-id="4de42-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="4de42-109">Transaktionsomkostninger og ikke-fakturerede salg bogføres ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="4de42-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="4de42-110">Projektomkostnings- og indtægtsprofil bestemmer, om ikke-fakturerede salgstransaktioner bogføres i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="4de42-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="4de42-111">Hvis **Periodisering af omsætning** er valgt, bruger systemet kontiene **Salgsværdien for IGVA** og **Salgsværdi af periodiseret omsætning** under bogføringen.</span><span class="sxs-lookup"><span data-stu-id="4de42-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="4de42-112">Følgende eksempel viser denne metode.</span><span class="sxs-lookup"><span data-stu-id="4de42-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="4de42-113">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="4de42-113">Transaction type</span></span> | <span data-ttu-id="4de42-114">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="4de42-114">Debit/Credit</span></span> | <span data-ttu-id="4de42-115">Beløb</span><span class="sxs-lookup"><span data-stu-id="4de42-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="4de42-116">Salgsværdi af IGVA</span><span class="sxs-lookup"><span data-stu-id="4de42-116">WIP Sales value</span></span> | <span data-ttu-id="4de42-117">Debet</span><span class="sxs-lookup"><span data-stu-id="4de42-117">Debit</span></span> | <span data-ttu-id="4de42-118">100</span><span class="sxs-lookup"><span data-stu-id="4de42-118">100</span></span> |
  | <span data-ttu-id="4de42-119">Salgsværdi af periodiseret omsætning</span><span class="sxs-lookup"><span data-stu-id="4de42-119">Accrued revenue sales value</span></span> | <span data-ttu-id="4de42-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="4de42-120">Credit</span></span> | <span data-ttu-id="4de42-121">100</span><span class="sxs-lookup"><span data-stu-id="4de42-121">100</span></span> |

- <span data-ttu-id="4de42-122">Omsætning anerkendes under fakturering.</span><span class="sxs-lookup"><span data-stu-id="4de42-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="4de42-123">Systemet bruger kontoen **Faktureret omsætning** under bogføringen.</span><span class="sxs-lookup"><span data-stu-id="4de42-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="4de42-124">Følgende eksempel viser denne metode.</span><span class="sxs-lookup"><span data-stu-id="4de42-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="4de42-125">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="4de42-125">Transaction type</span></span> | <span data-ttu-id="4de42-126">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="4de42-126">Debit/Credit</span></span> | <span data-ttu-id="4de42-127">Beløb</span><span class="sxs-lookup"><span data-stu-id="4de42-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="4de42-128">Kundesaldo</span><span class="sxs-lookup"><span data-stu-id="4de42-128">Customer balance</span></span> | <span data-ttu-id="4de42-129">Debet</span><span class="sxs-lookup"><span data-stu-id="4de42-129">Debit</span></span> | <span data-ttu-id="4de42-130">120</span><span class="sxs-lookup"><span data-stu-id="4de42-130">120</span></span> |
  | <span data-ttu-id="4de42-131">Skyldig moms</span><span class="sxs-lookup"><span data-stu-id="4de42-131">Sales tax payable</span></span> | <span data-ttu-id="4de42-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="4de42-132">Credit</span></span> | <span data-ttu-id="4de42-133">20</span><span class="sxs-lookup"><span data-stu-id="4de42-133">20</span></span> |
  | <span data-ttu-id="4de42-134">Faktureret omsætning</span><span class="sxs-lookup"><span data-stu-id="4de42-134">Invoiced Revenue</span></span> | <span data-ttu-id="4de42-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="4de42-135">Credit</span></span> | <span data-ttu-id="4de42-136">100</span><span class="sxs-lookup"><span data-stu-id="4de42-136">100</span></span> |

- <span data-ttu-id="4de42-137">Hvis omsætningen blev periodiseret, da det ikke-fakturerede salg blev bogført, tilbageføres den periodiserede omsætning ved fakturering.</span><span class="sxs-lookup"><span data-stu-id="4de42-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="4de42-138">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="4de42-138">Transaction type</span></span> | <span data-ttu-id="4de42-139">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="4de42-139">Debit/Credit</span></span> | <span data-ttu-id="4de42-140">Beløb</span><span class="sxs-lookup"><span data-stu-id="4de42-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="4de42-141">Salgsværdi af IGVA</span><span class="sxs-lookup"><span data-stu-id="4de42-141">WIP Sales value</span></span> | <span data-ttu-id="4de42-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="4de42-142">Credit</span></span> | <span data-ttu-id="4de42-143">100</span><span class="sxs-lookup"><span data-stu-id="4de42-143">100</span></span> |
  | <span data-ttu-id="4de42-144">Salgsværdi af periodiseret omsætning</span><span class="sxs-lookup"><span data-stu-id="4de42-144">Accrued revenue sales value</span></span> | <span data-ttu-id="4de42-145">Debet</span><span class="sxs-lookup"><span data-stu-id="4de42-145">Debit</span></span> | <span data-ttu-id="4de42-146">100</span><span class="sxs-lookup"><span data-stu-id="4de42-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="4de42-147">Transaktioner, der bogføres i regnskabet, og som anvender faktureringsmetoden for fast pris</span><span class="sxs-lookup"><span data-stu-id="4de42-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="4de42-148">Omkostnings- og omsætningsanerkendelse er adskilt.</span><span class="sxs-lookup"><span data-stu-id="4de42-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="4de42-149">Transaktionsomkostninger bogføres ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="4de42-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="4de42-150">Der oprettes ikke ikke-fakturerede salgstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="4de42-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="4de42-151">Omsætning kan anerkendes under fakturering, hvis projektomkostnings- og omsætningsprofilen har **Princip, der bruges til projektfuldførelsesberegninger**, angivet til **Ingen IGVA**.</span><span class="sxs-lookup"><span data-stu-id="4de42-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="4de42-152">Brug kun denne metode til kortsigtede, enkle projekter.</span><span class="sxs-lookup"><span data-stu-id="4de42-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="4de42-153">Omsætning kan anerkendes ved hjælp af estimater for fastprisomsætning enten med metoden **Fuldført kontrakt** eller metoden **Omsætningsanerkendelse ved hjælp af procentvis færdiggørelse**.</span><span class="sxs-lookup"><span data-stu-id="4de42-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4de42-154">Flere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4de42-154">Additional resources</span></span>
[<span data-ttu-id="4de42-155">Konfigurer regnskab for fakturerbare projektatikler</span><span class="sxs-lookup"><span data-stu-id="4de42-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="4de42-156">Omsætningsestimat for projekter med fast pris</span><span class="sxs-lookup"><span data-stu-id="4de42-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="4de42-157">Administrer omsætningsestimater</span><span class="sxs-lookup"><span data-stu-id="4de42-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="4de42-158">Metoder til færdiggørelsesomkostninger</span><span class="sxs-lookup"><span data-stu-id="4de42-158">Cost to complete methods</span></span>](cost-complete-methods.md)
