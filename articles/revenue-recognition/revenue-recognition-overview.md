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
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278861"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="818a3-103">Oversigt over omsætningsanerkendelse</span><span class="sxs-lookup"><span data-stu-id="818a3-103">Revenue recognition overview</span></span>

<span data-ttu-id="818a3-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="818a3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="818a3-105">I Dynamics 365 Project Operations varierer principperne for omsætningsanerkendelse på baggrund af den valgte faktureringsmetode for et projekt eller en del af projektet.</span><span class="sxs-lookup"><span data-stu-id="818a3-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="818a3-106">Dette emne indeholder oplysninger om omsætningsanerkendelse i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="818a3-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="818a3-107">Transaktioner, der bogføres i regnskabet, og som anvender faktureringsmetoden for tids- og materialer</span><span class="sxs-lookup"><span data-stu-id="818a3-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="818a3-108">Omkostnings- og omsætningsanerkendelse er forbundet.</span><span class="sxs-lookup"><span data-stu-id="818a3-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="818a3-109">Transaktionsomkostninger og ikke-fakturerede salg bogføres ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="818a3-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="818a3-110">Projektomkostnings- og indtægtsprofil bestemmer, om ikke-fakturerede salgstransaktioner bogføres i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="818a3-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="818a3-111">Hvis **Periodisering af omsætning** er valgt, bruger systemet kontiene **Salgsværdien for IGVA** og **Salgsværdi af periodiseret omsætning** under bogføringen.</span><span class="sxs-lookup"><span data-stu-id="818a3-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="818a3-112">Følgende eksempel viser denne metode.</span><span class="sxs-lookup"><span data-stu-id="818a3-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="818a3-113">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="818a3-113">Transaction type</span></span> | <span data-ttu-id="818a3-114">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="818a3-114">Debit/Credit</span></span> | <span data-ttu-id="818a3-115">Beløb</span><span class="sxs-lookup"><span data-stu-id="818a3-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="818a3-116">Salgsværdi af IGVA</span><span class="sxs-lookup"><span data-stu-id="818a3-116">WIP Sales value</span></span> | <span data-ttu-id="818a3-117">Debet</span><span class="sxs-lookup"><span data-stu-id="818a3-117">Debit</span></span> | <span data-ttu-id="818a3-118">100</span><span class="sxs-lookup"><span data-stu-id="818a3-118">100</span></span> |
  | <span data-ttu-id="818a3-119">Salgsværdi af periodiseret omsætning</span><span class="sxs-lookup"><span data-stu-id="818a3-119">Accrued revenue sales value</span></span> | <span data-ttu-id="818a3-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="818a3-120">Credit</span></span> | <span data-ttu-id="818a3-121">100</span><span class="sxs-lookup"><span data-stu-id="818a3-121">100</span></span> |

- <span data-ttu-id="818a3-122">Omsætning anerkendes under fakturering.</span><span class="sxs-lookup"><span data-stu-id="818a3-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="818a3-123">Systemet bruger kontoen **Faktureret omsætning** under bogføringen.</span><span class="sxs-lookup"><span data-stu-id="818a3-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="818a3-124">Følgende eksempel viser denne metode.</span><span class="sxs-lookup"><span data-stu-id="818a3-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="818a3-125">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="818a3-125">Transaction type</span></span> | <span data-ttu-id="818a3-126">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="818a3-126">Debit/Credit</span></span> | <span data-ttu-id="818a3-127">Beløb</span><span class="sxs-lookup"><span data-stu-id="818a3-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="818a3-128">Kundesaldo</span><span class="sxs-lookup"><span data-stu-id="818a3-128">Customer balance</span></span> | <span data-ttu-id="818a3-129">Debet</span><span class="sxs-lookup"><span data-stu-id="818a3-129">Debit</span></span> | <span data-ttu-id="818a3-130">120</span><span class="sxs-lookup"><span data-stu-id="818a3-130">120</span></span> |
  | <span data-ttu-id="818a3-131">Skyldig moms</span><span class="sxs-lookup"><span data-stu-id="818a3-131">Sales tax payable</span></span> | <span data-ttu-id="818a3-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="818a3-132">Credit</span></span> | <span data-ttu-id="818a3-133">20</span><span class="sxs-lookup"><span data-stu-id="818a3-133">20</span></span> |
  | <span data-ttu-id="818a3-134">Faktureret omsætning</span><span class="sxs-lookup"><span data-stu-id="818a3-134">Invoiced Revenue</span></span> | <span data-ttu-id="818a3-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="818a3-135">Credit</span></span> | <span data-ttu-id="818a3-136">100</span><span class="sxs-lookup"><span data-stu-id="818a3-136">100</span></span> |

- <span data-ttu-id="818a3-137">Hvis omsætningen blev periodiseret, da det ikke-fakturerede salg blev bogført, tilbageføres den periodiserede omsætning ved fakturering.</span><span class="sxs-lookup"><span data-stu-id="818a3-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="818a3-138">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="818a3-138">Transaction type</span></span> | <span data-ttu-id="818a3-139">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="818a3-139">Debit/Credit</span></span> | <span data-ttu-id="818a3-140">Beløb</span><span class="sxs-lookup"><span data-stu-id="818a3-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="818a3-141">Salgsværdi af IGVA</span><span class="sxs-lookup"><span data-stu-id="818a3-141">WIP Sales value</span></span> | <span data-ttu-id="818a3-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="818a3-142">Credit</span></span> | <span data-ttu-id="818a3-143">100</span><span class="sxs-lookup"><span data-stu-id="818a3-143">100</span></span> |
  | <span data-ttu-id="818a3-144">Salgsværdi af periodiseret omsætning</span><span class="sxs-lookup"><span data-stu-id="818a3-144">Accrued revenue sales value</span></span> | <span data-ttu-id="818a3-145">Debet</span><span class="sxs-lookup"><span data-stu-id="818a3-145">Debit</span></span> | <span data-ttu-id="818a3-146">100</span><span class="sxs-lookup"><span data-stu-id="818a3-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="818a3-147">Transaktioner, der bogføres i regnskabet, og som anvender faktureringsmetoden for fast pris</span><span class="sxs-lookup"><span data-stu-id="818a3-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="818a3-148">Omkostnings- og omsætningsanerkendelse er adskilt.</span><span class="sxs-lookup"><span data-stu-id="818a3-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="818a3-149">Transaktionsomkostninger bogføres ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="818a3-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="818a3-150">Der oprettes ikke ikke-fakturerede salgstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="818a3-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="818a3-151">Omsætning kan anerkendes under fakturering, hvis projektomkostnings- og omsætningsprofilen har **Princip, der bruges til projektfuldførelsesberegninger**, angivet til **Ingen IGVA**.</span><span class="sxs-lookup"><span data-stu-id="818a3-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="818a3-152">Brug kun denne metode til kortsigtede, enkle projekter.</span><span class="sxs-lookup"><span data-stu-id="818a3-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="818a3-153">Omsætning kan anerkendes ved hjælp af estimater for fastprisomsætning enten med metoden **Fuldført kontrakt** eller metoden **Omsætningsanerkendelse ved hjælp af procentvis færdiggørelse**.</span><span class="sxs-lookup"><span data-stu-id="818a3-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="818a3-154">Flere ressourcer</span><span class="sxs-lookup"><span data-stu-id="818a3-154">Additional resources</span></span>
[<span data-ttu-id="818a3-155">Konfigurer regnskab for fakturerbare projektatikler</span><span class="sxs-lookup"><span data-stu-id="818a3-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="818a3-156">Omsætningsestimat for projekter med fast pris</span><span class="sxs-lookup"><span data-stu-id="818a3-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="818a3-157">Administrer omsætningsestimater</span><span class="sxs-lookup"><span data-stu-id="818a3-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="818a3-158">Metoder til færdiggørelsesomkostninger</span><span class="sxs-lookup"><span data-stu-id="818a3-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]