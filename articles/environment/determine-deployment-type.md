---
title: Udrulningstyper
description: Dette emne indeholder oplysninger, som hjælper dig med at fastlægge den korrekte udrulningstype for Project operations for din virksomhed.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948808"
---
# <a name="deployment-types"></a><span data-ttu-id="09c4b-103">Udrulningstyper</span><span class="sxs-lookup"><span data-stu-id="09c4b-103">Deployment types</span></span>

<span data-ttu-id="09c4b-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="09c4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09c4b-105">Når du har købt licensen, skal du starte her for at fastlægge den bedste udrulningsmodel til Dynamics 365 Project operations ved hjælp af det [Styrede installationsflow](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="09c4b-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="09c4b-106">Når du har afsluttet det styrede installationsflow, omdirigeres du til den korrekte administrationsportal for at fuldføre installationen.</span><span class="sxs-lookup"><span data-stu-id="09c4b-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="09c4b-107">Se nedenstående detaljer om udrulning for at fuldføre installationen.</span><span class="sxs-lookup"><span data-stu-id="09c4b-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="09c4b-108">Eksisterende Dynamics-kunder, som anvender Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="09c4b-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="09c4b-109">Project operations omfatter de funktioner, der blev leveret sammen med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="09c4b-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="09c4b-110">Der frigives en opgraderingssti for disse kunder på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="09c4b-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="09c4b-111">Eksisterende Dynamics 365 Finance-kunder, som anvender projektstyring og regnskab</span><span class="sxs-lookup"><span data-stu-id="09c4b-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="09c4b-112">Eksisterende Finance-kunder, der benytter funktionen projektstyring og regnskab, kan fortsætte med at bruge denne funktion som hidtil.</span><span class="sxs-lookup"><span data-stu-id="09c4b-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="09c4b-113">Se [Project Operations for lagerbaserede/produktionsordrescenarier](#pma).</span><span class="sxs-lookup"><span data-stu-id="09c4b-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="09c4b-114">Project Operations understøtter forskellige udrulningsmuligheder, så de passer til dine behov.</span><span class="sxs-lookup"><span data-stu-id="09c4b-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="09c4b-115">Uanset om du er ny eller eksisterende Dynamics 365-kunde, kan Project Operations opfylde dine behov.</span><span class="sxs-lookup"><span data-stu-id="09c4b-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="09c4b-116">Vores [Spørgeskema vedrørende udrulning](https://aka.ms/provisionprojectoperations) hjælper dig med at finde den rette udrulning.</span><span class="sxs-lookup"><span data-stu-id="09c4b-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="09c4b-117">Resultaterne fører dig hen imod en af følgende udrulningstyper:</span><span class="sxs-lookup"><span data-stu-id="09c4b-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="09c4b-118">Lille udrulning – aftale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="09c4b-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="09c4b-119">Project Operations for ressource/ikke-lagerscenarier</span><span class="sxs-lookup"><span data-stu-id="09c4b-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="09c4b-120">Project Operations for lagerbaserede/produktionsordrescenarier</span><span class="sxs-lookup"><span data-stu-id="09c4b-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="09c4b-121">Project Operations understøtter scenarier med lagerførte-/produktionsordre og ikke-lagerførte-/ressourcebaserede scenarier i samme miljø via konfigurationer på juridisk enhedsniveau.</span><span class="sxs-lookup"><span data-stu-id="09c4b-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="09c4b-122">Contoso kan f.eks. bruge funktioner for lagerførte-/produktionsordrekapaciteter i deres amerikanske produktionslokale (juridisk enhed = Contoso Manufacturing USA) og ikke-lagerførte/ressourcebaserede kapaciteter i deres lokale for servicering af Contoso Robotics Arms i Storbritannien (juridisk enhed = Contoso Robotics Storbritannien).</span><span class="sxs-lookup"><span data-stu-id="09c4b-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="09c4b-123"><a name="lite"><a/>Lille udrulning - aftale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="09c4b-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="09c4b-124">Den lille udrulning inkluderer følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="09c4b-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="09c4b-125">Projektplanlægning ved hjælp af Microsoft Project til internettet</span><span class="sxs-lookup"><span data-stu-id="09c4b-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="09c4b-126">Flerdimensionel prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="09c4b-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="09c4b-127">Fælles ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="09c4b-127">Unified Resource Management</span></span>
- <span data-ttu-id="09c4b-128">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="09c4b-128">Time Tracking</span></span>
- <span data-ttu-id="09c4b-129">Grundlæggende udgifter</span><span class="sxs-lookup"><span data-stu-id="09c4b-129">Basic Expense</span></span>
- <span data-ttu-id="09c4b-130">Fakturaforslag</span><span class="sxs-lookup"><span data-stu-id="09c4b-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="09c4b-131">Udrulningstrin:</span><span class="sxs-lookup"><span data-stu-id="09c4b-131">Deployment steps:</span></span>
<span data-ttu-id="09c4b-132">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="09c4b-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="09c4b-133">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](lite-preview-subscription-sign-up.md) og [Klargøring af nyt miljø](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="09c4b-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="09c4b-134"><a name="integrated"><a/>Project Operations for ressource/ikke-lagerscenarier</span><span class="sxs-lookup"><span data-stu-id="09c4b-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="09c4b-135">Project Operations for ressource/ikke-lagerførte scenarier omfatter følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="09c4b-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="09c4b-136">Projektplanlægning ved hjælp af Microsoft Project til internettet</span><span class="sxs-lookup"><span data-stu-id="09c4b-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="09c4b-137">Flerdimensionel prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="09c4b-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="09c4b-138">Fælles ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="09c4b-138">Unified Resource Management</span></span>
- <span data-ttu-id="09c4b-139">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="09c4b-139">Time Tracking</span></span>
- <span data-ttu-id="09c4b-140">Grundlæggende udgifter</span><span class="sxs-lookup"><span data-stu-id="09c4b-140">Basic Expense</span></span>
- <span data-ttu-id="09c4b-141">Fuld udgift</span><span class="sxs-lookup"><span data-stu-id="09c4b-141">Full Expense</span></span>
- <span data-ttu-id="09c4b-142">Optisk tegngenkendelseskvittering</span><span class="sxs-lookup"><span data-stu-id="09c4b-142">Receipt OCR</span></span>
- <span data-ttu-id="09c4b-143">Fuld fakturering</span><span class="sxs-lookup"><span data-stu-id="09c4b-143">Full Invoicing</span></span>
- <span data-ttu-id="09c4b-144">Indtægtsanerkendelse</span><span class="sxs-lookup"><span data-stu-id="09c4b-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="09c4b-145">Udrulningstrin:</span><span class="sxs-lookup"><span data-stu-id="09c4b-145">Deployment steps:</span></span>
<span data-ttu-id="09c4b-146">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="09c4b-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="09c4b-147">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](resource-sign-up-preview-subscription.md) og [Klargøring af nyt miljø](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="09c4b-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="09c4b-148">Project Operations for lagerbaserede/produktionsordrescenarier</span><span class="sxs-lookup"><span data-stu-id="09c4b-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="09c4b-149">Ofte stillede spørgsmål om brug af WBS</span><span class="sxs-lookup"><span data-stu-id="09c4b-149">Project planning using WBS</span></span>
- <span data-ttu-id="09c4b-150">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="09c4b-150">Resource Management</span></span>
- <span data-ttu-id="09c4b-151">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="09c4b-151">Time Tracking</span></span>
- <span data-ttu-id="09c4b-152">Fuld udgift</span><span class="sxs-lookup"><span data-stu-id="09c4b-152">Full Expense</span></span>
- <span data-ttu-id="09c4b-153">Optisk tegngenkendelseskvittering</span><span class="sxs-lookup"><span data-stu-id="09c4b-153">Receipt OCR</span></span>
- <span data-ttu-id="09c4b-154">Fuld fakturering</span><span class="sxs-lookup"><span data-stu-id="09c4b-154">Full Invoicing</span></span>
- <span data-ttu-id="09c4b-155">Indtægtsanerkendelse</span><span class="sxs-lookup"><span data-stu-id="09c4b-155">Revenue Recognition</span></span>
- <span data-ttu-id="09c4b-156">Produktionsordrer</span><span class="sxs-lookup"><span data-stu-id="09c4b-156">Production Orders</span></span>
- <span data-ttu-id="09c4b-157">Materialesupport</span><span class="sxs-lookup"><span data-stu-id="09c4b-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="09c4b-158">Udrulningstrin:</span><span class="sxs-lookup"><span data-stu-id="09c4b-158">Deployment steps:</span></span>
<span data-ttu-id="09c4b-159">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="09c4b-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="09c4b-160">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargøring af nyt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="09c4b-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



