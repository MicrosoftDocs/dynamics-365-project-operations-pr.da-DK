---
title: Standarder for økonomiske dimensioner
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer standarder for økonomiske dimensioner.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013299"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="66944-103">Standarder for økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="66944-103">Financial dimension defaults</span></span>

<span data-ttu-id="66944-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="66944-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="66944-105">Dynamics 365 Project Operations bruger strukturen for [Økonomiske dimensioner](/dynamics365/finance/general-ledger/financial-dimensions) i Dynamics 365 Finance til at give yderligere indsigt i projekters underfinanskonto og generelle transaktioner på finanskontoen.</span><span class="sxs-lookup"><span data-stu-id="66944-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="66944-106">Økonomiske standarddimensioner kan angives for en kunde, et projekts finansieringskilde, en milepæl, en projektkontraktlinje eller et projekt.</span><span class="sxs-lookup"><span data-stu-id="66944-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="66944-107">Definer økonomiske standarddimensioner for en kunde</span><span class="sxs-lookup"><span data-stu-id="66944-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="66944-108">Standardværdier for kundedimensioner angives i Finance.</span><span class="sxs-lookup"><span data-stu-id="66944-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="66944-109">Gennemfør følgende trin for at konfigurere dimensionsstandarder .</span><span class="sxs-lookup"><span data-stu-id="66944-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="66944-110">Gå til **Debitor** > **Kunder** > **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="66944-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="66944-111">På siden **Kunder** skal du på fanen **Økonomiske dimensioner** angive de økonomiske dimensionsværdier for bestemte kunder.</span><span class="sxs-lookup"><span data-stu-id="66944-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="66944-112">Definer økonomiske standarddimensioner for projektkontrakter</span><span class="sxs-lookup"><span data-stu-id="66944-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="66944-113">Projektkontrakter oprettes og vedligeholdes i Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="66944-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="66944-114">Regnskabsattributter for projektkontrakter angives i modulet **Projektstyring og regnskab** i Finance.</span><span class="sxs-lookup"><span data-stu-id="66944-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="66944-115">Angiv økonomiske dimensioner for en finansieringskilde for et projekt</span><span class="sxs-lookup"><span data-stu-id="66944-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="66944-116">Gå til **Projektstyring og regnskab** > **Projekter** > **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="66944-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="66944-117">Vælg den post, som du vil opdatere, og på fanen **Projektkontrakt** skal du vælge **Vis standardregnskab**.</span><span class="sxs-lookup"><span data-stu-id="66944-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="66944-118">Udvid **Relaterede oplysninger**, og vælg fanen **Finansieringskilder**.</span><span class="sxs-lookup"><span data-stu-id="66944-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="66944-119">Angiv standarderne for økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="66944-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="66944-120">Bemærk, at de økonomiske dimensioner hentes som standard fra kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="66944-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="66944-121">Angiv økonomiske dimensioner for en projektkontraktlinje</span><span class="sxs-lookup"><span data-stu-id="66944-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="66944-122">Gå til **Projektstyring og regnskab** > **Projekter** > **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="66944-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="66944-123">Vælg den post, som du vil opdatere, og på fanen **Projektkontrakt** skal du vælge **Vis standardregnskab**.</span><span class="sxs-lookup"><span data-stu-id="66944-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="66944-124">Udvid **Relaterede oplysninger**, og vælg fanen **Kontraktlinjer**.</span><span class="sxs-lookup"><span data-stu-id="66944-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="66944-125">Angiv standarderne for økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="66944-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="66944-126">Standarderne for den økonomiske dimension er gældende og kan kun bruges sammen med kontraktlinjer med fast pris (milepæl).</span><span class="sxs-lookup"><span data-stu-id="66944-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="66944-127">Disse standardindstillinger bruges på relaterede linjer for aconto transaktioner for projekt og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="66944-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="66944-128">Definer økonomiske standarddimensioner for projekter</span><span class="sxs-lookup"><span data-stu-id="66944-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="66944-129">Projekter oprettes og vedligeholdes i CDS.</span><span class="sxs-lookup"><span data-stu-id="66944-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="66944-130">Regnskabsattributter for projekter angives i modulet **Projektstyring og regnskab** i Finance.</span><span class="sxs-lookup"><span data-stu-id="66944-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="66944-131">Gå til **Projektstyring og regnskab** > **Projekter** > **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="66944-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="66944-132">Vælg den post, som du vil opdatere, og på fanen **Projekt** skal du vælge **Vis standardregnskab**.</span><span class="sxs-lookup"><span data-stu-id="66944-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="66944-133">Udvid **Relaterede oplysninger**, og vælg fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="66944-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="66944-134">Angiv standarderne for økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="66944-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="66944-135">Bemærk, at økonomiske dimensioner hentes som standard fra kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="66944-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="66944-136">Hvis projektet er knyttet til en kontraktlinje med flere projektkontraktkunder, bruges den primære kunde som standard som den økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="66944-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="66944-137">Projektets standarder for økonomiske dimensioner bruges til at angive standarder for kladdelinjer for tid, udgifter og gebyrtransaktioner i **Integrationskladden i Project Operations** og på relaterede projektfakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="66944-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]