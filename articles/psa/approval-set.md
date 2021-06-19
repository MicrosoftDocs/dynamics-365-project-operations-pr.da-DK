---
title: Godkendelsessæt
description: Dette emne indeholder oplysninger om godkendelsessæt, forespørgsler og undergrupper af disse handlinger.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116864"
---
# <a name="approval-sets"></a><span data-ttu-id="a8c19-103">Godkendelsessæt</span><span class="sxs-lookup"><span data-stu-id="a8c19-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a8c19-104">Godkendelsessæt grupperer forespørgsler om godkendelse i mindre undergrupper af handlinger.</span><span class="sxs-lookup"><span data-stu-id="a8c19-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="a8c19-105">Denne gruppering gør det muligt at behandle godkendelser i projektrækkefølge og giver mulighed for at forsøge igen og sekvensering.</span><span class="sxs-lookup"><span data-stu-id="a8c19-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="a8c19-106">Gruppering forbedrer pålideligheden og sporbarheden af godkendelsesbehandling for store mængder godkendelser.</span><span class="sxs-lookup"><span data-stu-id="a8c19-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="a8c19-107">Godkendelsessæt angiver den overordnede behandlingstilstand for de relaterede poster.</span><span class="sxs-lookup"><span data-stu-id="a8c19-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="a8c19-108">Når en godkendelsespost behandles ved hjælp af et godkendelsessæt, flyttes posten fra **Indsendt** til **Godkendt**, og forbindelsen til godkendelsessættet fjernes.</span><span class="sxs-lookup"><span data-stu-id="a8c19-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="a8c19-109">Hvis det ikke lykkes at godkende en post, når den er indsendt til godkendelse, har posten fortsat status som **Indsendt**, og godkendelsessættet er markeret som mislykket.</span><span class="sxs-lookup"><span data-stu-id="a8c19-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="a8c19-110">Godkendelsessættet registrerer fejlmeddelelsen, der opstår.</span><span class="sxs-lookup"><span data-stu-id="a8c19-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="a8c19-111">Behandling af godkendelser og godkendelsessæt</span><span class="sxs-lookup"><span data-stu-id="a8c19-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="a8c19-112">Godkendelser, der er sat i kø til behandling, er synlige i visningen **Behandling af godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="a8c19-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="a8c19-113">Systemet forsøger at behandle alle objekter flere gange asynkront, herunder at køre en godkendelse igen, hvis tidligere forsøg mislykkedes.</span><span class="sxs-lookup"><span data-stu-id="a8c19-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="a8c19-114">Feltet **Levetid for godkendelsessæt** registrerer det resterende antal forsøg til at behandle sættet, før det er markeret som mislykket.</span><span class="sxs-lookup"><span data-stu-id="a8c19-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="a8c19-115">Mislykkede godkendelser og godkendelsessæt</span><span class="sxs-lookup"><span data-stu-id="a8c19-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="a8c19-116">Visningen **Mislykkede godkendelser** indeholder alle godkendelser, der kræver brugerintervention.</span><span class="sxs-lookup"><span data-stu-id="a8c19-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="a8c19-117">Åbn logfilerne for det tilknyttede godkendelsessæt for at identificere årsagen til fejlen.</span><span class="sxs-lookup"><span data-stu-id="a8c19-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="a8c19-118">Hvis du vælger **Prøv igen**, tilføjes levetidstallet for godkendelsessættet, godkendelsen flyttes tilbage til statussen **Behandling**, og det forsøges at behandle de resterende poster.</span><span class="sxs-lookup"><span data-stu-id="a8c19-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="a8c19-119">Konfigurer godkendelsessæt</span><span class="sxs-lookup"><span data-stu-id="a8c19-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="a8c19-120">Aktiver funktionen for godkendelsessæt</span><span class="sxs-lookup"><span data-stu-id="a8c19-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="a8c19-121">Før du aktiverer funktionen Godkendelsessæt, skal du kontrollere, at der ikke er nogen godkendelser, der behandles i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="a8c19-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="a8c19-122">Gå til siden **Projektparametre**, og vælg **Funktionskontrol** > **Aktiver moderne godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="a8c19-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="a8c19-123">Deaktiver funktionen for godkendelsessæt</span><span class="sxs-lookup"><span data-stu-id="a8c19-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="a8c19-124">Før du deaktiverer funktionen Godkendelsessæt, skal du kontrollere, at der ikke er nogen godkendelser, der behandles i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="a8c19-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="a8c19-125">Gå til siden **Projektparametre**, og vælg **Funktionskontrol** > **Deaktiver moderne godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="a8c19-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="a8c19-126">Konfiguration af den asynkrone tærskelværdi</span><span class="sxs-lookup"><span data-stu-id="a8c19-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="a8c19-127">Når der oprettes godkendelsessæt, flyttes behandlingen til baggrunden, når det valgte antal poster til godkendelse overskrider den angivne tærskelværdi.</span><span class="sxs-lookup"><span data-stu-id="a8c19-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="a8c19-128">Brug feltet **Asynkron tærskelværdi** til at konfigurere, hvornår godkendelsesbehandling bør køres synkront eller asynkront.</span><span class="sxs-lookup"><span data-stu-id="a8c19-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="a8c19-129">De gyldige værdier er:</span><span class="sxs-lookup"><span data-stu-id="a8c19-129">Valid values are:</span></span>

  - <span data-ttu-id="a8c19-130">Nul: Alle forespørgsler skal behandles asynkront.</span><span class="sxs-lookup"><span data-stu-id="a8c19-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="a8c19-131">Tal, der er større end nul: Godkendelser behandles kun asynkront, når det indsendte antal godkendelser overskrider denne værdi.</span><span class="sxs-lookup"><span data-stu-id="a8c19-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
