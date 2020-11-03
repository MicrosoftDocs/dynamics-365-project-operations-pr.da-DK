---
title: Produktbaserede salgsmulighedslinjer
description: Dette emne indeholder oplysninger om produktbaserede salgsmulighedslinjeelementer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074098"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="116f9-103">Produktbaserede salgsmulighedslinjer</span><span class="sxs-lookup"><span data-stu-id="116f9-103">Product-based opportunity lines</span></span>

<span data-ttu-id="116f9-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="116f9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="116f9-105">Produktbaserede salgsmulighedslinjer er linjeelementer på salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="116f9-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="116f9-106">Disse linjer leveres til kunden som særskilte linjeelementer på fakturaen uden nogen anden værditilvækstservice.</span><span class="sxs-lookup"><span data-stu-id="116f9-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="116f9-107">Det tilknyttede forbrug spores ikke ved opgaver i relaterede projekter.</span><span class="sxs-lookup"><span data-stu-id="116f9-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="116f9-108">Produktbaserede linjer kan være katalogvarer eller produkter, der skal rekvireres.</span><span class="sxs-lookup"><span data-stu-id="116f9-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="116f9-109">De fleste funktioner i en salgsmuligheds produktbaserede linjer følger de funktioner, der findes i programmet Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="116f9-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="116f9-110">Du kan finde flere oplysninger om produktbaserede salgsmulighedslinjer under [Tilføj produkter til en salgsmulighed](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="116f9-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="116f9-111">Et af koncepterne ved produktbaserede salgsmulighedslinjer er, som er specifikke for projektbaserede salgsmuligheder, er **Kundebudget**.</span><span class="sxs-lookup"><span data-stu-id="116f9-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="116f9-112">Brug dette felt til at spore det beløb, som kunden vil betale for linjeelementet.</span><span class="sxs-lookup"><span data-stu-id="116f9-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="116f9-113">Hvis omsætningsmetoden for salgsmulighedsoversigten er angivet til **Systemberegnet** , opsummeres kundebudgetværdierne på tværs af produkt- og projektbaserede linjer for at beregne den anslåede omsætning.</span><span class="sxs-lookup"><span data-stu-id="116f9-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
