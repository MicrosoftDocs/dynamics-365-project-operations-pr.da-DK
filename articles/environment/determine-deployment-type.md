---
title: Vælg din udrulningstype
description: Dette emne indeholder oplysninger, som hjælper dig med at fastlægge den korrekte udrulningstype for Project operations for din virksomhed.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401211"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="09379-103">Vælg din udrulningstype</span><span class="sxs-lookup"><span data-stu-id="09379-103">Determine your deployment type</span></span>

<span data-ttu-id="09379-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="09379-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09379-105">Når du har købt licensen, skal du starte her for at fastlægge den bedste udrulningsmodel til Dynamics 365 Project operations ved hjælp af det [Styrede installationsflow](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="09379-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="09379-106">Når du har afsluttet det styrede installationsflow, omdirigeres du til den korrekte administrationsportal for at fuldføre installationen.</span><span class="sxs-lookup"><span data-stu-id="09379-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="09379-107">Se detaljerne om udrulning for at fuldføre installationen.</span><span class="sxs-lookup"><span data-stu-id="09379-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="09379-108">Eksisterende Dynamics-kunder, som anvender Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="09379-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="09379-109">Project operations omfatter de funktioner, der blev leveret sammen med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="09379-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="09379-110">Der udgives en opgraderingssti for disse kunder i den første frigivelsesbølge i 2021.</span><span class="sxs-lookup"><span data-stu-id="09379-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="09379-111">Eksisterende Dynamics 365 Finance-kunder, som anvender projektstyring og regnskab</span><span class="sxs-lookup"><span data-stu-id="09379-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="09379-112">Eksisterende Finance-kunder, der benytter funktionen Projektstyring og regnskab, kan fortsætte med at bruge den, som hidtil.</span><span class="sxs-lookup"><span data-stu-id="09379-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="09379-113">Se [Project Operations for lagerbaserede/produktionsordrescenarier](#pma).</span><span class="sxs-lookup"><span data-stu-id="09379-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="09379-114">Udrulningstyper</span><span class="sxs-lookup"><span data-stu-id="09379-114">Deployment types</span></span>
<span data-ttu-id="09379-115">Project Operations understøtter forskellige udrulningsmuligheder, så de passer til dine behov.</span><span class="sxs-lookup"><span data-stu-id="09379-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="09379-116">Uanset om du er ny eller eksisterende Dynamics 365-kunde, kan Project Operations opfylde dine behov.</span><span class="sxs-lookup"><span data-stu-id="09379-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="09379-117">Vores [Spørgeskema vedrørende udrulning](https://aka.ms/provisionprojectoperations) hjælper dig med at finde den rette udrulning.</span><span class="sxs-lookup"><span data-stu-id="09379-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="09379-118">Resultaterne fører dig hen imod en af følgende udrulningstyper:</span><span class="sxs-lookup"><span data-stu-id="09379-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="09379-119">Lille udrulning – aftale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="09379-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="09379-120">Project Operations for ressource/ikke-lagerscenarier</span><span class="sxs-lookup"><span data-stu-id="09379-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="09379-121">Project Operations for lagerbaserede/produktionsordrescenarier</span><span class="sxs-lookup"><span data-stu-id="09379-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="09379-122">Project Operations understøtter scenarier med lagerførte-/produktionsordre og ikke-lagerførte-/ressourcebaserede scenarier i samme miljø via konfigurationer på juridisk enhedsniveau.</span><span class="sxs-lookup"><span data-stu-id="09379-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="09379-123">Contoso kan f eks. bruge egenskaberne for lagerbaserede ordrer/produktionsordre i deres amerikanske produktionsanlæg (juridisk enhed = Contoso Manufacturing USA).</span><span class="sxs-lookup"><span data-stu-id="09379-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="09379-124">Contoso kan bruge de ikke-lagerbaserede/ressourcebasered egenskaber i deres servicevirksomhed Contoso Robotics Arms i Storbritannien (juridisk enhed = Contoso Robotics Storbritannien).</span><span class="sxs-lookup"><span data-stu-id="09379-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="09379-125">Lille udrulning - aftale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="09379-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="09379-126">Den lille udrulning inkluderer følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="09379-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="09379-127">Salgsproces for projekter, der udvider oplevelserne i programmet Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="09379-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="09379-128">Projektplanlægning ved hjælp af Microsoft Project til internettet</span><span class="sxs-lookup"><span data-stu-id="09379-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="09379-129">Flerdimensionel prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="09379-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="09379-130">Fælles ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="09379-130">Unified resource management</span></span>
- <span data-ttu-id="09379-131">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="09379-131">Time tracking</span></span>
- <span data-ttu-id="09379-132">Grundlæggende udgifter</span><span class="sxs-lookup"><span data-stu-id="09379-132">Basic expense</span></span>
- <span data-ttu-id="09379-133">Proforma og kundeorienteret fakturering</span><span class="sxs-lookup"><span data-stu-id="09379-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="09379-134">Installationsprocessen</span><span class="sxs-lookup"><span data-stu-id="09379-134">Deployment steps</span></span>
<span data-ttu-id="09379-135">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="09379-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="09379-136">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](lite-preview-subscription-sign-up.md) og [Klargøring af nyt miljø](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="09379-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="09379-137">Project Operations for ressource/ikke-lagerscenarier</span><span class="sxs-lookup"><span data-stu-id="09379-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="09379-138">Project Operations for ressource/ikke-lagerførte scenarier omfatter følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="09379-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="09379-139">Salgsproces for projekter, der udvider programmet Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="09379-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="09379-140">Projektplanlægning ved hjælp af Microsoft Project til internettet</span><span class="sxs-lookup"><span data-stu-id="09379-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="09379-141">Flerdimensionel prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="09379-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="09379-142">Fælles ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="09379-142">Unified resource management</span></span>
- <span data-ttu-id="09379-143">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="09379-143">Time tracking</span></span>
- <span data-ttu-id="09379-144">Grundlæggende udgifter</span><span class="sxs-lookup"><span data-stu-id="09379-144">Basic expense</span></span>
- <span data-ttu-id="09379-145">Fuld udgift</span><span class="sxs-lookup"><span data-stu-id="09379-145">Full expense</span></span>
- <span data-ttu-id="09379-146">Optisk tegngenkendelseskvittering</span><span class="sxs-lookup"><span data-stu-id="09379-146">Receipt OCR</span></span>
- <span data-ttu-id="09379-147">Proforma og kundeorienteret fakturering</span><span class="sxs-lookup"><span data-stu-id="09379-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="09379-148">Indtægtsføring for projekter</span><span class="sxs-lookup"><span data-stu-id="09379-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="09379-149">Installationsprocessen</span><span class="sxs-lookup"><span data-stu-id="09379-149">Deployment steps</span></span>
<span data-ttu-id="09379-150">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="09379-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="09379-151">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](resource-sign-up-preview-subscription.md) og [Klargøring af nyt miljø](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="09379-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="09379-152">Project Operations for lagerbaserede/produktionsordrescenarier</span><span class="sxs-lookup"><span data-stu-id="09379-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="09379-153">Ofte stillede spørgsmål om brug af WBS</span><span class="sxs-lookup"><span data-stu-id="09379-153">Project planning using WBS</span></span>
- <span data-ttu-id="09379-154">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="09379-154">Resource Management</span></span>
- <span data-ttu-id="09379-155">Tidssporing</span><span class="sxs-lookup"><span data-stu-id="09379-155">Time Tracking</span></span>
- <span data-ttu-id="09379-156">Fuld udgift</span><span class="sxs-lookup"><span data-stu-id="09379-156">Full Expense</span></span>
- <span data-ttu-id="09379-157">Optisk tegngenkendelseskvittering</span><span class="sxs-lookup"><span data-stu-id="09379-157">Receipt OCR</span></span>
- <span data-ttu-id="09379-158">Fuld fakturering</span><span class="sxs-lookup"><span data-stu-id="09379-158">Full Invoicing</span></span>
- <span data-ttu-id="09379-159">Indtægtsanerkendelse</span><span class="sxs-lookup"><span data-stu-id="09379-159">Revenue Recognition</span></span>
- <span data-ttu-id="09379-160">Produktionsordrer</span><span class="sxs-lookup"><span data-stu-id="09379-160">Production Orders</span></span>
- <span data-ttu-id="09379-161">Materialesupport</span><span class="sxs-lookup"><span data-stu-id="09379-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="09379-162">Installationsprocessen</span><span class="sxs-lookup"><span data-stu-id="09379-162">Deployment steps</span></span>
<span data-ttu-id="09379-163">Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="09379-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="09379-164">I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargøring af nyt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="09379-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

