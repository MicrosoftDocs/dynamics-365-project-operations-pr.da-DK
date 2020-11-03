---
title: Vælg din udrulningstype
description: Dette emne indeholder oplysninger, som hjælper dig med at fastlægge den korrekte udrulningstype for Project operations for din virksomhed.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074176"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="3ff17-103">Vælg din udrulningstype</span><span class="sxs-lookup"><span data-stu-id="3ff17-103">Determine your deployment type</span></span>

<span data-ttu-id="3ff17-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3ff17-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ff17-105">Når du har købt licensen, skal du starte her for at fastlægge den bedste udrulningsmodel til Dynamics 365 Project operations ved hjælp af det [Styrede installationsflow](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3ff17-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="3ff17-106">Når du har afsluttet det styrede installationsflow, omdirigeres du til den korrekte administrationsportal for at fuldføre installationen.</span><span class="sxs-lookup"><span data-stu-id="3ff17-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="3ff17-107">Se detaljerne om udrulning for at fuldføre installationen.</span><span class="sxs-lookup"><span data-stu-id="3ff17-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="3ff17-108">Eksisterende Dynamics-kunder, som anvender Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3ff17-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="3ff17-109">Project operations omfatter de funktioner, der blev leveret sammen med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3ff17-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="3ff17-110">Der frigives en opgraderingssti for disse kunder på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="3ff17-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="3ff17-111">Eksisterende Dynamics 365 Finance-kunder, som anvender projektstyring og regnskab</span><span class="sxs-lookup"><span data-stu-id="3ff17-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="3ff17-112">Eksisterende Finance-kunder, der benytter funktionen projektstyring og regnskab, kan fortsætte med at bruge denne funktion som hidtil.</span><span class="sxs-lookup"><span data-stu-id="3ff17-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="3ff17-113">Se [Project Operations for lagerbaserede/produktionsordrescenarier](#pma).</span><span class="sxs-lookup"><span data-stu-id="3ff17-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="3ff17-114">Udrulningstyper</span><span class="sxs-lookup"><span data-stu-id="3ff17-114">Deployment types</span></span>
<span data-ttu-id="3ff17-115">Project Operations understøtter forskellige udrulningsmuligheder, så de passer til dine behov.</span><span class="sxs-lookup"><span data-stu-id="3ff17-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="3ff17-116">Uanset om du er ny eller eksisterende Dynamics 365-kunde, kan Project Operations opfylde dine behov.</span><span class="sxs-lookup"><span data-stu-id="3ff17-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="3ff17-117">Vores [Spørgeskema vedrørende udrulning](https://aka.ms/provisionprojectoperations) hjælper dig med at finde den rette udrulning.</span><span class="sxs-lookup"><span data-stu-id="3ff17-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="3ff17-118">Resultaterne fører dig hen imod en af følgende udrulningstyper:</span><span class="sxs-lookup"><span data-stu-id="3ff17-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="3ff17-119">Lille udrulning – aftale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="3ff17-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="3ff17-120">Project Operations for ressource/ikke-lagerscenarier</span><span class="sxs-lookup"><span data-stu-id="3ff17-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="3ff17-121">Project Operations for lagerbaserede/produktionsordrescenarier</span><span class="sxs-lookup"><span data-stu-id="3ff17-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="3ff17-122">Project Operations understøtter scenarier med lagerførte-/produktionsordre og ikke-lagerførte-/ressourcebaserede scenarier i samme miljø via konfigurationer på juridisk enhedsniveau.</span><span class="sxs-lookup"><span data-stu-id="3ff17-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="3ff17-123">Contoso kan f eks. bruge egenskaberne for lagerbaserede ordrer/produktionsordre i deres amerikanske produktionsanlæg (juridisk enhed = Contoso Manufacturing USA).</span><span class="sxs-lookup"><span data-stu-id="3ff17-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="3ff17-124">Contoso kan bruge de ikke-lagerbaserede/ressourcebasered egenskaber i deres servicevirksomhed Contoso Robotics Arms i Storbritannien (juridisk enhed = Contoso Robotics Storbritannien).</span><span class="sxs-lookup"><span data-stu-id="3ff17-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="3ff17-125">Lille udrulning - aftale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="3ff17-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="3ff17-126">Den lille udrulning inkluderer følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="3ff17-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="3ff17-127">Projektplanlægning ved hjælp af Microsoft Project til internettet</span><span class="sxs-lookup"><span data-stu-id="3ff17-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="3ff17-128">Flerdimensionel prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="3ff17-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="3ff17-129">Fælles ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="3ff17-129">Unified Resource Management</span></span>
- <span data-ttu-id="3ff17-130">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="3ff17-130">Time Tracking</span></span>
- <span data-ttu-id="3ff17-131">Grundlæggende udgifter</span><span class="sxs-lookup"><span data-stu-id="3ff17-131">Basic Expense</span></span>
- <span data-ttu-id="3ff17-132">Fakturaforslag</span><span class="sxs-lookup"><span data-stu-id="3ff17-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3ff17-133">Installationsprocessen</span><span class="sxs-lookup"><span data-stu-id="3ff17-133">Deployment steps</span></span>
<span data-ttu-id="3ff17-134">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3ff17-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3ff17-135">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](lite-preview-subscription-sign-up.md) og [Klargøring af nyt miljø](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="3ff17-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="3ff17-136">Project Operations for ressource/ikke-lagerscenarier</span><span class="sxs-lookup"><span data-stu-id="3ff17-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="3ff17-137">Project Operations for ressource/ikke-lagerførte scenarier omfatter følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="3ff17-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="3ff17-138">Projektplanlægning ved hjælp af Microsoft Project til internettet</span><span class="sxs-lookup"><span data-stu-id="3ff17-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="3ff17-139">Flerdimensionel prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="3ff17-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="3ff17-140">Fælles ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="3ff17-140">Unified Resource Management</span></span>
- <span data-ttu-id="3ff17-141">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="3ff17-141">Time Tracking</span></span>
- <span data-ttu-id="3ff17-142">Grundlæggende udgifter</span><span class="sxs-lookup"><span data-stu-id="3ff17-142">Basic Expense</span></span>
- <span data-ttu-id="3ff17-143">Fuld udgift</span><span class="sxs-lookup"><span data-stu-id="3ff17-143">Full Expense</span></span>
- <span data-ttu-id="3ff17-144">Optisk tegngenkendelseskvittering</span><span class="sxs-lookup"><span data-stu-id="3ff17-144">Receipt OCR</span></span>
- <span data-ttu-id="3ff17-145">Fuld fakturering</span><span class="sxs-lookup"><span data-stu-id="3ff17-145">Full Invoicing</span></span>
- <span data-ttu-id="3ff17-146">Indtægtsanerkendelse</span><span class="sxs-lookup"><span data-stu-id="3ff17-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3ff17-147">Installationsprocessen</span><span class="sxs-lookup"><span data-stu-id="3ff17-147">Deployment steps</span></span>
<span data-ttu-id="3ff17-148">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3ff17-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3ff17-149">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](resource-sign-up-preview-subscription.md) og [Klargøring af nyt miljø](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3ff17-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="3ff17-150">Project Operations for lagerbaserede/produktionsordrescenarier</span><span class="sxs-lookup"><span data-stu-id="3ff17-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="3ff17-151">Ofte stillede spørgsmål om brug af WBS</span><span class="sxs-lookup"><span data-stu-id="3ff17-151">Project planning using WBS</span></span>
- <span data-ttu-id="3ff17-152">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="3ff17-152">Resource Management</span></span>
- <span data-ttu-id="3ff17-153">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="3ff17-153">Time Tracking</span></span>
- <span data-ttu-id="3ff17-154">Fuld udgift</span><span class="sxs-lookup"><span data-stu-id="3ff17-154">Full Expense</span></span>
- <span data-ttu-id="3ff17-155">Optisk tegngenkendelseskvittering</span><span class="sxs-lookup"><span data-stu-id="3ff17-155">Receipt OCR</span></span>
- <span data-ttu-id="3ff17-156">Fuld fakturering</span><span class="sxs-lookup"><span data-stu-id="3ff17-156">Full Invoicing</span></span>
- <span data-ttu-id="3ff17-157">Indtægtsanerkendelse</span><span class="sxs-lookup"><span data-stu-id="3ff17-157">Revenue Recognition</span></span>
- <span data-ttu-id="3ff17-158">Produktionsordrer</span><span class="sxs-lookup"><span data-stu-id="3ff17-158">Production Orders</span></span>
- <span data-ttu-id="3ff17-159">Materialesupport</span><span class="sxs-lookup"><span data-stu-id="3ff17-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3ff17-160">Installationsprocessen</span><span class="sxs-lookup"><span data-stu-id="3ff17-160">Deployment steps</span></span>
<span data-ttu-id="3ff17-161">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3ff17-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3ff17-162">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargøring af nyt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="3ff17-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

