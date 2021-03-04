---
title: Gennemse ordrebeholdning for fakturering vedrørende projekter og projektkontrakter
description: Dette emne indeholder oplysninger om, hvordan du gennemgår tid, udgifter og produktbeholdninger, og hvordan du markerer dem som klar til fakturering.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150481"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="e6e02-103">Gennemse ordrebeholdning for fakturering vedrørende projekter og projektkontrakter</span><span class="sxs-lookup"><span data-stu-id="e6e02-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e6e02-104">Når en transaktion er klar til at få oprettet og behandlet en faktura, skal transaktionen markeres som **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="e6e02-105">I dette emne beskrives de transaktionstyper, der kan oprettes.</span><span class="sxs-lookup"><span data-stu-id="e6e02-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="e6e02-106">Gennemse ordrebeholdning for fakturering af tid og materiale</span><span class="sxs-lookup"><span data-stu-id="e6e02-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="e6e02-107">Når en tidsregistrering eller en udgiftspost sendes og godkendes til et projekt, opretter PSA en faktisk projektkomponent.</span><span class="sxs-lookup"><span data-stu-id="e6e02-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="e6e02-108">Hvis kombinationen af projektet og transaktionsklassen er knyttet til en kontraktlinje for et tids- og materialeprojekt, oprettes der to faktiske oplysninger, når posten godkendes:</span><span class="sxs-lookup"><span data-stu-id="e6e02-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="e6e02-109">Faktisk omkostning</span><span class="sxs-lookup"><span data-stu-id="e6e02-109">Cost actual</span></span> 
- <span data-ttu-id="e6e02-110">Ikke-faktureret faktisk salg</span><span class="sxs-lookup"><span data-stu-id="e6e02-110">Unbilled sales actual</span></span>

<span data-ttu-id="e6e02-111">Ikke-fakturerede faktiske salgsværdier repræsenterer ordrer til fakturering, og deres faktureringsstatus skal angives til **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="e6e02-112">Når der oprettes en projektfaktura, kopieres ikke-fakturerede faktiske salgsværdier, der er markeret som **Klar til fakturering,** over som fakturalinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="e6e02-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="e6e02-113">Hvis du vil gennemgå ordrebeholdning for fakturering af tid og materiale, skal du gå til **Salg** \> **Fakturering** \> **Ordrebeholdning for fakturering af tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="e6e02-114">Markér alle de ikke-fakturerede faktiske salgstal, der er klar til at blive faktureret, og vælg derefter **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="e6e02-115">Faktureringsstatussen for disse faktiske tal ændres til **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Ordrebeholdning for fakturering af tid og materiale](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="e6e02-117">Gennemgå ordrebeholdning for produktfakturering</span><span class="sxs-lookup"><span data-stu-id="e6e02-117">Review the product billing backlog</span></span>

<span data-ttu-id="e6e02-118">Når en projektkontrakt har produktbaserede kontraktlinjer i PSA, betragtes disse linjer som klar til fakturering, hver gang der oprettes en faktura for projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="e6e02-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="e6e02-119">Alle produkter, som har kontraktlinjer, der er markeret som **Klar til fakturering,** kopieres til projektfakturaen som projektfakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="e6e02-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="e6e02-120">Hvis du vil gennemse ordrebeholdningen for produktfakturering, skal du gå til **Salg** \> **Fakturering** \> **Ordrebeholdning for produktfakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="e6e02-121">Markér alle produktbaserede kontraktlinjer, der er klar til at blive faktureret, og vælg derefter **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="e6e02-122">Faktureringsstatussen for disse linjer ændres til **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Ordrebeholdning for produktfakturering](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="e6e02-124">Gennemse faktureringsmilepæle for fastpriskontrakter</span><span class="sxs-lookup"><span data-stu-id="e6e02-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="e6e02-125">Hver projektkontraktlinje, der har en fastpris-faktureringsmetode, skal definere kontraktmilepæle.</span><span class="sxs-lookup"><span data-stu-id="e6e02-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="e6e02-126">Disse kontraktmilepæle kan kun faktureres, hvis de er markeret som **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="e6e02-127">Hvis du vil gennemse faktureringsmilepæle, skal du gå til **Salg** \> **Fakturering** \> **Milepæle for fast pris**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="e6e02-128">Markér de milepæle, der er klar til at blive faktureret, og vælg derefter **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="e6e02-129">Faktureringsstatussen for disse milepæle ændres til **Klar til fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e6e02-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Milepæle for fast pris](media/FPBacklog.png)
