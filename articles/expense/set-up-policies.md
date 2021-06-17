---
title: Definer udgiftspolitikker
description: Du kan definere de udgiftspolitikker, som dine medarbejder skal følge, når de angiver og indsender udgiftsrapporter og rejserekvisitioner.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001869"
---
# <a name="define-expense-policies"></a><span data-ttu-id="69d74-103">Definer udgiftspolitikker</span><span class="sxs-lookup"><span data-stu-id="69d74-103">Define expense policies</span></span>

<span data-ttu-id="69d74-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="69d74-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="69d74-105">Du kan definere de politikker, som dine medarbejder skal følge, når de angiver og indsender udgiftsrapporter og rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="69d74-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="69d74-106">Implementering af udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt.</span><span class="sxs-lookup"><span data-stu-id="69d74-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="69d74-107">Du kan f.eks. angive en politik for hoteludgifter i New York City, hvor det angives, at udgifterne pr. nat ikke må overstige 250 USD.</span><span class="sxs-lookup"><span data-stu-id="69d74-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="69d74-108">Hvis en arbejder indsender en udgiftsrapport eller rejserekvisition, hvor værelsestaksten overstiger dette beløb, vil systemet underrette</span><span class="sxs-lookup"><span data-stu-id="69d74-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="69d74-109">arbejder, som har overskredet politikbeløbet.</span><span class="sxs-lookup"><span data-stu-id="69d74-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="69d74-110">Du kan konfigurere den meddelelse, som arbejderen modtager, når du</span><span class="sxs-lookup"><span data-stu-id="69d74-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="69d74-111">definere politikken.</span><span class="sxs-lookup"><span data-stu-id="69d74-111">define the policy.</span></span>      
        
<span data-ttu-id="69d74-112">Du kan definere tre typer politikker:</span><span class="sxs-lookup"><span data-stu-id="69d74-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="69d74-113">**Advarsel**: Gør det muligt for arbejderen at indsende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og</span><span class="sxs-lookup"><span data-stu-id="69d74-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="69d74-114">til senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="69d74-114">for later reporting.</span></span>        

- <span data-ttu-id="69d74-115">**Fejl** : Arbejderen skal revidere udgiften for at overholde politikken, før denne indsender udgiftsrapporten eller rejserekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="69d74-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="69d74-116">**Begrundelse** : Arbejderen eller en leder skal angive en begrundelse for at overskride politikbeløbet, før udgiftsrapporten eller rejserekvisitionen indsendes.</span><span class="sxs-lookup"><span data-stu-id="69d74-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="69d74-117">Politiktips</span><span class="sxs-lookup"><span data-stu-id="69d74-117">Policy tips</span></span>
<span data-ttu-id="69d74-118">Her er et par forslag, der kan hjælpe dig med at oprette nye politikker for udgiftsstyring:</span><span class="sxs-lookup"><span data-stu-id="69d74-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="69d74-119">Politikker træder i kraft på en angiven dato, hvilket betyder, at en politik ikke træder i kraft, hvis den oprettes med en dato efter den dato, hvor udgiften fandt sted.</span><span class="sxs-lookup"><span data-stu-id="69d74-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="69d74-120">Du kan f.eks. oprette en ny politik i dag for at gennemtvinge et maksimalt beløb for udgifter til måltider på 50 USD.</span><span class="sxs-lookup"><span data-stu-id="69d74-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="69d74-121">Eksisterende udgifter, der er angivet i går, kontrolleres ikke i forhold til denne politik.</span><span class="sxs-lookup"><span data-stu-id="69d74-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="69d74-122">Når du opretter en politik for en udgiftskategori, der kan specificeres, skal du overveje at tilføje en betingelse for udgiftslinjetype.</span><span class="sxs-lookup"><span data-stu-id="69d74-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="69d74-123">Nogle politikker, f.eks. dem, der kræver en kvittering, giver muligvis ikke mening for specificerede linjer.</span><span class="sxs-lookup"><span data-stu-id="69d74-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="69d74-124">I denne situation gælder politikken kun for overskriftslinjen eller en ikke-specificeret linje.</span><span class="sxs-lookup"><span data-stu-id="69d74-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="69d74-125">Politikker for udgiftsstyring evalueres som standard i forhold til kildeobjektet.</span><span class="sxs-lookup"><span data-stu-id="69d74-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="69d74-126">I forbindelse med interne scenarier kan du i stedet angive den politik, der skal evalueres i forhold til destinationsenheden (lånt enhed).</span><span class="sxs-lookup"><span data-stu-id="69d74-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="69d74-127">Hvis du vil køre politikkerne i forhold til destinationsenheden, skal du aktivere funktionen **Evaluer udgiftspolitik i forhold til den juridiske låneenhed** i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="69d74-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="69d74-128">Tidspunkt for evaluering af politikker</span><span class="sxs-lookup"><span data-stu-id="69d74-128">When to evaluate policies</span></span>

<span data-ttu-id="69d74-129">I parametre for udgiftsstyring kan du vælge at evaluere politikker for udgiftsstyring, når en linje gemmes, eller når der indsendes en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="69d74-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="69d74-130">Hvis du vælger at evaluere, når en linje gemmes, får brugerne tidligere indsigt i, hvad de skal gøre for at fuldføre deres udgiftsrapporter på én gang.</span><span class="sxs-lookup"><span data-stu-id="69d74-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="69d74-131">Ellers kan du forsinke evalueringen af politikker og spare tid ved at validere den til slut i forbindelse med indsendelsen til arbejdsprocessen.</span><span class="sxs-lookup"><span data-stu-id="69d74-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]