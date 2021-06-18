---
title: Konfigurer udgiftspolitikker
description: Du kan konfigurere de udgiftspolitikker, som dine medarbejder skal følge, når de angiver og indsender udgiftsrapporter og rejserekvisitioner i Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005739"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="f0983-103">Konfigurer udgiftspolitikker</span><span class="sxs-lookup"><span data-stu-id="f0983-103">Set up expense policies</span></span>

<span data-ttu-id="f0983-104">Du kan definere de politikker, som dine medarbejder skal følge, når de angiver og indsender udgiftsrapporter og rejserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="f0983-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="f0983-105">Implementering af udgiftspolitikker kan gøre det lettere at administrere udgifter effektivt.</span><span class="sxs-lookup"><span data-stu-id="f0983-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="f0983-106">Du kan f.eks. angive en politik for hoteludgifter i New York City, hvor det angives, at udgifterne pr. nat ikke må overstige 250 USD.</span><span class="sxs-lookup"><span data-stu-id="f0983-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="f0983-107">Hvis en arbejder indsender en udgiftsrapport eller rejserekvisition, hvori værelsestaksten overstiger dette beløb, vil systemet underrette den</span><span class="sxs-lookup"><span data-stu-id="f0983-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="f0983-108">arbejder, som har overskredet politikbeløbet.</span><span class="sxs-lookup"><span data-stu-id="f0983-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="f0983-109">Du kan konfigurere den meddelelse, som arbejderen modtager, når du</span><span class="sxs-lookup"><span data-stu-id="f0983-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="f0983-110">definere politikken.</span><span class="sxs-lookup"><span data-stu-id="f0983-110">define the policy.</span></span>      
        
<span data-ttu-id="f0983-111">Du kan definere tre typer politikker:</span><span class="sxs-lookup"><span data-stu-id="f0983-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="f0983-112">Advarsel – Gør det muligt for arbejderen at indsende en udgiftsrapport eller rejserekvisition, men udgiften markeres for alle godkendere og</span><span class="sxs-lookup"><span data-stu-id="f0983-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="f0983-113">til senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="f0983-113">for later reporting.</span></span>        

- <span data-ttu-id="f0983-114">Fejl – Arbejderen skal revidere udgiften for at overholde politikken, før denne indsender udgiftsrapporten eller rejserekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="f0983-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="f0983-115">Begrundelse – Arbejderen eller en leder skal angive en begrundelse for at overskride politikbeløbet, før udgiftsrapporten eller rejserekvisitionen indsendes.</span><span class="sxs-lookup"><span data-stu-id="f0983-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="f0983-116">Politiktips</span><span class="sxs-lookup"><span data-stu-id="f0983-116">Policy tips</span></span>
<span data-ttu-id="f0983-117">Her er et par forslag, der kan hjælpe dig med at oprette nye politikker for udgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="f0983-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="f0983-118">Politikker træder i kraft på en angiven dato og træder ikke i kraft, hvis en politik oprettes med en dato efter den dato, hvor udgiften fandt sted.</span><span class="sxs-lookup"><span data-stu-id="f0983-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="f0983-119">Hvis du f.eks. opretter en ny politik i dag for at gennemtvinge et loft over udgifter til måltider på 50 $, kontrolleres eventuelle eksisterende udgifter, der blev angivet pr. gårsdagens dato, ikke i forhold til denne politik.</span><span class="sxs-lookup"><span data-stu-id="f0983-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="f0983-120">Når du opretter en politik for en udgiftskategori, der kan specificeres, skal du overveje at tilføje en betingelse for udgiftslinjetype.</span><span class="sxs-lookup"><span data-stu-id="f0983-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="f0983-121">Nogle politikker, som f.eks. kræver en kvittering, giver muligvis ikke mening for specificerede linjer og skal kun anvendes på hovedlinjen eller en ikke-specificeret linje.</span><span class="sxs-lookup"><span data-stu-id="f0983-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="f0983-122">Politikker for udgiftsstyring evalueres som standard i forhold til kildeobjektet.</span><span class="sxs-lookup"><span data-stu-id="f0983-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="f0983-123">I forbindelse med interne scenarier kan du i stedet angive den politik, der skal evalueres i forhold til destinationsenheden (lånt enhed).</span><span class="sxs-lookup"><span data-stu-id="f0983-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="f0983-124">Hvis du vil køre politikkerne i forhold til destinationsenheden, skal du aktivere funktionen "Evaluer udgiftspolitik i forhold til den juridiske låneenhed" i arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="f0983-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="f0983-125">Tidspunkt for evaluering af politikker</span><span class="sxs-lookup"><span data-stu-id="f0983-125">When to evaluate policies</span></span>

<span data-ttu-id="f0983-126">I parametre for udgiftsstyring findes en indstillingen, hvor du kan evaluere politikker for udgiftsstyring, enten når en linje gemmes, eller når der indsendes en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="f0983-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="f0983-127">Hvis du vælger at evaluere, når en linje gemmes, sikrer dette, at brugerne får tidligere indsigt i, hvad de skal gøre for at fuldføre deres udgiftsrapporter på én gang.</span><span class="sxs-lookup"><span data-stu-id="f0983-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="f0983-128">Ellers kan du udskyde evalueringen af politikker og spare tid, hvis du validerer til slut i forbindelse med indsendelsen til arbejdsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f0983-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]