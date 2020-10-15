---
title: Godkendelsesoversigt
description: Dette emne indeholder informationer om, hvordan du arbejder med godkendelser i Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961159"
---
# <a name="approvals-overview"></a><span data-ttu-id="29b07-103">Godkendelsesoversigt</span><span class="sxs-lookup"><span data-stu-id="29b07-103">Approvals overview</span></span>

<span data-ttu-id="29b07-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="29b07-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="29b07-105">Indsendelser af tidsregistrering og udgifter går gennem en godkendelsesarbejdsproces.</span><span class="sxs-lookup"><span data-stu-id="29b07-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="29b07-106">Når posterne er godkendt, registreres transaktionerne i faktiske tal, eller der reserveres tid i planlægningen.</span><span class="sxs-lookup"><span data-stu-id="29b07-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="29b07-107">Godkendelsesarbejdsproces</span><span class="sxs-lookup"><span data-stu-id="29b07-107">Approvals workflow</span></span>
<span data-ttu-id="29b07-108">Når du opretter og indsender en tids- eller udgiftspost, oprettes der en godkendelsespost.</span><span class="sxs-lookup"><span data-stu-id="29b07-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="29b07-109">Projektgodkenderen eller din leder gennemgår og godkender din indtastning.</span><span class="sxs-lookup"><span data-stu-id="29b07-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="29b07-110">Hvis posten vedrører et projekt, og den godkendes, oprettes de faktiske oplysninger.</span><span class="sxs-lookup"><span data-stu-id="29b07-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="29b07-111">Det giver mulighed for at spore omkostninger og fakturering.</span><span class="sxs-lookup"><span data-stu-id="29b07-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="29b07-112">Godkend en post</span><span class="sxs-lookup"><span data-stu-id="29b07-112">Approve an entry</span></span>
<span data-ttu-id="29b07-113">Formularen **Godkendelser** giver dig mulighed for at skifte mellem forskellige visninger, så du kan få vist forskellige typer godkendelser.</span><span class="sxs-lookup"><span data-stu-id="29b07-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="29b07-114">Gå til formularen **Godkendelser**, og vælg **Udgifter**, **Tid** eller **Tilbagekaldelser**.</span><span class="sxs-lookup"><span data-stu-id="29b07-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="29b07-115">Gennemse de enkelte godkendelser, og vælg dem, du vil godkende.</span><span class="sxs-lookup"><span data-stu-id="29b07-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="29b07-116">Vælg **Godkend** for at godkende de markerede poster.</span><span class="sxs-lookup"><span data-stu-id="29b07-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="29b07-117">Disse poster behandles automatisk i systemet, og der oprettes faktiske oplysninger eller en reservation.</span><span class="sxs-lookup"><span data-stu-id="29b07-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="29b07-118">Afvis en post</span><span class="sxs-lookup"><span data-stu-id="29b07-118">Reject an entry</span></span>
<span data-ttu-id="29b07-119">Som projektgodkender skal du muligvis sende en post tilbage til en bruger, så brugeren kan rette den.</span><span class="sxs-lookup"><span data-stu-id="29b07-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="29b07-120">Gå til formularen **Godkendelser**, og vælg den post, der skal afvises.</span><span class="sxs-lookup"><span data-stu-id="29b07-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="29b07-121">Vælg **Afvis**.</span><span class="sxs-lookup"><span data-stu-id="29b07-121">Select **Reject**.</span></span>
3. <span data-ttu-id="29b07-122">Valgfrit - Tilføj en kommentar i dialogboksen **Afvisningskommentarer** for at informere brugeren om, hvorfor posten afvises.</span><span class="sxs-lookup"><span data-stu-id="29b07-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="29b07-123">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="29b07-123">Select **OK**.</span></span> <span data-ttu-id="29b07-124">Posten sendes til brugeren igen.</span><span class="sxs-lookup"><span data-stu-id="29b07-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="29b07-125">Tilbagekald registreringer</span><span class="sxs-lookup"><span data-stu-id="29b07-125">Recall entries</span></span>
<span data-ttu-id="29b07-126">Du kan på et eller andet tidspunkt få brug for at tilbagekalde en indsendt post.</span><span class="sxs-lookup"><span data-stu-id="29b07-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="29b07-127">Hvis posten ikke er godkendt, vil den blive returneret med det samme.</span><span class="sxs-lookup"><span data-stu-id="29b07-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="29b07-128">En godkendt post kan dog have en væsentlig indvirkning.</span><span class="sxs-lookup"><span data-stu-id="29b07-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="29b07-129">Projektgodkenderen skal godkende tilbagekaldelsen for at kunne tilbageføre transaktionen i faktiske tal.</span><span class="sxs-lookup"><span data-stu-id="29b07-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="29b07-130">Angiv projektgodkendere</span><span class="sxs-lookup"><span data-stu-id="29b07-130">Specify Project approvers</span></span>
<span data-ttu-id="29b07-131">Hvert projekt har en række medlemmer af projektteamet.</span><span class="sxs-lookup"><span data-stu-id="29b07-131">Each project has a number of project team members.</span></span> <span data-ttu-id="29b07-132">Du kan angive, hvilke teammedlemmer der også er projektgodkendere.</span><span class="sxs-lookup"><span data-stu-id="29b07-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="29b07-133">Gå til formularen **Projekter**, og åbn projektet på listen.</span><span class="sxs-lookup"><span data-stu-id="29b07-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="29b07-134">På fanen **Teams** skal du vælge det teammedlem, der skal være projektgodkender, og derefter vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="29b07-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="29b07-135">Vælg **Ja** i feltet **Projektgodkender**.</span><span class="sxs-lookup"><span data-stu-id="29b07-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="29b07-136">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="29b07-136">Select **Save**.</span></span>
5. <span data-ttu-id="29b07-137">Gentag trin 2-4 for at tilføje eller redigere flere projektgodkendere.</span><span class="sxs-lookup"><span data-stu-id="29b07-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="29b07-138">Konfigurer brugerens leder</span><span class="sxs-lookup"><span data-stu-id="29b07-138">Configure the user's manager</span></span>

1. <span data-ttu-id="29b07-139">Gå til **Indstillinger** > **Sikkerhed** > **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="29b07-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="29b07-140">Vælg den bruger, du vil tildele en leder, og vælge derefter lederen på listen i området **Organisationsoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="29b07-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="29b07-141">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="29b07-141">Select **Save**.</span></span>


