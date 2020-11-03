---
title: Oprettelse af en manuel proformafaktura
description: Dette emne indeholder oplysninger om, hvordan du opretter en manuel proformafaktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074401"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="cdc2b-103">Oprettelse af en manuel proformafaktura</span><span class="sxs-lookup"><span data-stu-id="cdc2b-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="cdc2b-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="cdc2b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cdc2b-105">I Dynamics 365 Project Operations kan du oprette proformafakturaer manuelt efter behov.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="cdc2b-106">Du kan manuelt oprette en proformafaktura på listesiden **Projektkontrakter** eller på siden med oplysninger om **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="cdc2b-107">Listeside med projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="cdc2b-107">Project Contracts list page</span></span>

<span data-ttu-id="cdc2b-108">På listesiden **Projektkontrakter** skal du vælge en eller flere projektkontrakter og oprette fakturaer for alle de valgte poster.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="cdc2b-109">Systemet kontrollerer, hvilke af de valgte projektkontrakter der har et efterslæb med **Klar til at blive faktureret** , som er dateret før dags dato.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="cdc2b-110">På grundlag af disse kontrakter opretter systemet kladdeproformafakturaer.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="cdc2b-111">Hvis der er flere kunder i en projektkontrakt, kan der oprettes én faktura pr. kunde og flere fakturaer pr. projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="cdc2b-112">Alle de oprettede projektfakturaer er tilgængelige på siden **Faktura** i sektionen **Fakturering** i området **Salg**.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="cdc2b-113">Side med oplysninger om projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="cdc2b-113">Project Contract details page</span></span>

<span data-ttu-id="cdc2b-114">Du kan også oprette en proformafaktura på siden med oplysninger om **Projektkontrakt** , hvilket opretter fakturaen for den pågældende projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="cdc2b-115">Systemet kontrollerer, om den valgte projektkontrakt har et efterslæb med **Klar til at blive faktureret** , som er dateret før dags dato.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="cdc2b-116">På grundlag af disse kontrakter opretter systemet kladdeproformafakturaer, der er baseret på antallet af kunder på hver kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="cdc2b-117">Når der er oprettet en enkelt proformafaktura, åbnes siden **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="cdc2b-118">Hvis der er oprettet flere fakturaer for den pågældende projektkontrakt, åbnes listesiden **Fakturaer** , hvor du kan se alle de oprettede fakturaer.</span><span class="sxs-lookup"><span data-stu-id="cdc2b-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
