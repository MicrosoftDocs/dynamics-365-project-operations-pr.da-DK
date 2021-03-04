---
title: Opret en manuel proformafaktura - lille
description: Dette emne indeholder oplysninger om, hvordan du opretter en manuel proformafaktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764496"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="273bb-103">Opret en manuel proformafaktura - lille</span><span class="sxs-lookup"><span data-stu-id="273bb-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="273bb-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="273bb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="273bb-105">I Dynamics 365 Project Operations kan proformafakturaer oprettes manuelt efter behov.</span><span class="sxs-lookup"><span data-stu-id="273bb-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="273bb-106">Du kan manuelt oprette en proformafaktura på listesiden **Projektkontrakter** eller på siden med oplysninger om **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="273bb-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="273bb-107">Listeside med projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="273bb-107">Project Contracts list page</span></span>

<span data-ttu-id="273bb-108">På listesiden **Projektkontrakter** skal du vælge en eller flere projektkontrakter og oprette fakturaer for alle de valgte poster.</span><span class="sxs-lookup"><span data-stu-id="273bb-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="273bb-109">Systemet kontrollerer, hvilke af de valgte projektkontrakter der har et efterslæb med **Klar til at blive faktureret**, som er dateret før dags dato.</span><span class="sxs-lookup"><span data-stu-id="273bb-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="273bb-110">På grundlag af disse kontrakter opretter systemet kladdeproformafakturaer.</span><span class="sxs-lookup"><span data-stu-id="273bb-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="273bb-111">Hvis der er flere kunder i en projektkontrakt, kan der oprettes én faktura pr. kunde og flere fakturaer pr. projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="273bb-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="273bb-112">Alle de oprettede projektfakturaer er tilgængelige på siden **Faktura** i sektionen **Fakturering** i området **Salg**.</span><span class="sxs-lookup"><span data-stu-id="273bb-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="273bb-113">Side med oplysninger om projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="273bb-113">Project Contract details page</span></span>

<span data-ttu-id="273bb-114">Der kan også oprettes en proformafaktura på siden med detaljer for **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="273bb-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="273bb-115">Systemet verficerer, at projektkontrakten et efterslæb med **Klar til at blive faktureret**, som er dateret før dags dato.</span><span class="sxs-lookup"><span data-stu-id="273bb-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="273bb-116">På grundlag af disse kontrakter opretter systemet kladdeproformafakturaer, der er baseret på antallet af kunder på hver kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="273bb-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="273bb-117">Når der er oprettet en enkelt proformafaktura, åbnes siden **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="273bb-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="273bb-118">Hvis der oprettes flere fakturaer for den pågældende projektkontrakt, åbnes listesiden **Fakturaer** for at vise alle de oprettede fakturaer.</span><span class="sxs-lookup"><span data-stu-id="273bb-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
