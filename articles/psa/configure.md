---
title: Konfigurere Project Service Automation
description: Trin til konfiguration af Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 06a29f67040cd7da583bdeae85d6a0f6a3684c52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290577"
---
# <a name="configure-project-service"></a><span data-ttu-id="09970-103">Konfigurere Project Service</span><span class="sxs-lookup"><span data-stu-id="09970-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="09970-104">Før du kan bruge funktionerne til automatisering af [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] til at administrere dine konti, projekter og ressourcer, skal du udføre nogle få konfigurationstrin for at sikre, at løsningen for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] passer til organisationens behov.</span><span class="sxs-lookup"><span data-stu-id="09970-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="09970-105">Det drejer sig om følgende trin:</span><span class="sxs-lookup"><span data-stu-id="09970-105">These steps include:</span></span>  
  
-   <span data-ttu-id="09970-106">[Konfigurere tidsenheder](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="09970-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="09970-107">Konfigurer tidsenhederne i det produktkatalog, du vil bruge som grundlag for planlægning og fakturering af dine projekter.</span><span class="sxs-lookup"><span data-stu-id="09970-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="09970-108">[Konfigurere valutaer og valutakurser](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="09970-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="09970-109">Konfigurer valutaerne, der skal bruges til dine projekter.</span><span class="sxs-lookup"><span data-stu-id="09970-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="09970-110">[Oprette afdelinger](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="09970-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="09970-111">Konfigurer de grupper, som firmaet bruger til at dele sine forretningsopgaver, uanset om det er efter geografi, forretningsfunktion eller anden logisk opdeling.</span><span class="sxs-lookup"><span data-stu-id="09970-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="09970-112">[Konfigurere fakturahyppigheder](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="09970-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="09970-113">Opret de tidsperioder, du vil bruge til fakturering af kunder.</span><span class="sxs-lookup"><span data-stu-id="09970-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="09970-114">[Konfigurere transaktionskategorier](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="09970-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="09970-115">Konfigurer posteringskategorier, som dine konsulenter kan opkræve deres fakturerbare og ikke-fakturerbare udgifter fra.</span><span class="sxs-lookup"><span data-stu-id="09970-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="09970-116">[Konfigurere udgiftskategorier](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="09970-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="09970-117">Konfigurer de kategorier, som dine konsulenter kan opkræve deres fakturerbare og ikke-fakturerbare udgifter fra.</span><span class="sxs-lookup"><span data-stu-id="09970-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="09970-118">[Oprette produktkatalogvarer](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="09970-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="09970-119">Tilføj de produkter, du sælger, f.eks softwarelicenser, i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="09970-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="09970-120">[Oprette en prisliste](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="09970-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="09970-121">Konfigurer forskellige prislister, afhængigt af hvor meget du vil fakturere dine kunder for hver rolle, som deres projekt kræver.</span><span class="sxs-lookup"><span data-stu-id="09970-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="09970-122">[Konfigurere ressourcer](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="09970-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="09970-123">Tilføj de færdigheder, kompetencer, ressourceroller og andre ressourceoplysninger, du skal bruge til dine projekter.</span><span class="sxs-lookup"><span data-stu-id="09970-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="09970-124">Se også</span><span class="sxs-lookup"><span data-stu-id="09970-124">See Also</span></span>  
 <span data-ttu-id="09970-125">[Oversigt over Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="09970-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="09970-126">[Konfigurere Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="09970-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="09970-127">[Vejledning til kundechefer](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="09970-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="09970-128">[Vejledning til projektledere](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="09970-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="09970-129">[Ressourcestyringsvejledning](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="09970-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="09970-130">Tids-, udgifts- og samarbejdsvejledning</span><span class="sxs-lookup"><span data-stu-id="09970-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]