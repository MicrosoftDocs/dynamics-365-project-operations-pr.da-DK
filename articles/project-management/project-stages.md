---
title: Projektfaser
description: Dette emne indeholder oplysninger om de projektstadier, der er tilgængelige i Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996919"
---
# <a name="project-stages"></a><span data-ttu-id="b5a15-103">Projektfaser</span><span class="sxs-lookup"><span data-stu-id="b5a15-103">Project stages</span></span>

<span data-ttu-id="b5a15-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b5a15-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b5a15-105">Projektfaser er udformet, så de afspejler projektets tilstand, mens det skrider frem.</span><span class="sxs-lookup"><span data-stu-id="b5a15-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="b5a15-106">Tilpasninger kan bruges til automatisk at opdatere faserne med forretningsprocesforløb, Power Automate eller plug-in-udvidelser.</span><span class="sxs-lookup"><span data-stu-id="b5a15-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="b5a15-107">Følgende faser er defineret i standardforretningsprocesforløbet:</span><span class="sxs-lookup"><span data-stu-id="b5a15-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="b5a15-108">Nyt</span><span class="sxs-lookup"><span data-stu-id="b5a15-108">New</span></span>
- <span data-ttu-id="b5a15-109">Tilbud</span><span class="sxs-lookup"><span data-stu-id="b5a15-109">Quote</span></span>
- <span data-ttu-id="b5a15-110">Abonnement</span><span class="sxs-lookup"><span data-stu-id="b5a15-110">Plan</span></span>
- <span data-ttu-id="b5a15-111">Levér</span><span class="sxs-lookup"><span data-stu-id="b5a15-111">Deliver</span></span>
- <span data-ttu-id="b5a15-112">Afsluttet</span><span class="sxs-lookup"><span data-stu-id="b5a15-112">Complete</span></span>
- <span data-ttu-id="b5a15-113">Luk</span><span class="sxs-lookup"><span data-stu-id="b5a15-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="b5a15-114">Nyt</span><span class="sxs-lookup"><span data-stu-id="b5a15-114">New</span></span>

<span data-ttu-id="b5a15-115">Når du opretter et projekt, indstilles projektfasen til **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b5a15-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="b5a15-116">Hvis projektet blev oprettet ud fra en skabelon, kan det indeholde planlægnings-, estimat- og teamdata.</span><span class="sxs-lookup"><span data-stu-id="b5a15-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="b5a15-117">Ellers er det en kontur for projektet, og de resterende komponenter skal angives.</span><span class="sxs-lookup"><span data-stu-id="b5a15-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="b5a15-118">Tilbud</span><span class="sxs-lookup"><span data-stu-id="b5a15-118">Quote</span></span>

<span data-ttu-id="b5a15-119">Når du knytter et projekt til et tilbud, eller når du opretter et projekt fra et tilbud, angives projektfasen til **Tilbud**, og de forventede start- og slutdatoer opdateres.</span><span class="sxs-lookup"><span data-stu-id="b5a15-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="b5a15-120">Når projektet befinder sig i fasen **Tilbud**, vises oplysninger om tilbuddet under fanen **Salg** på siden **Projektenhed**.</span><span class="sxs-lookup"><span data-stu-id="b5a15-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="b5a15-121">Planlæg</span><span class="sxs-lookup"><span data-stu-id="b5a15-121">Plan</span></span>

<span data-ttu-id="b5a15-122">Når du vinder et tilbud, der er knyttet til et projekt, og projektet flyttes til fasen **Kontrakt**, opdateres projektfasen til **Plan**.</span><span class="sxs-lookup"><span data-stu-id="b5a15-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="b5a15-123">Når projektet befinder sig i fasen **Plan**, vises oplysninger om kontrakten på fanen **Projektenhed**.</span><span class="sxs-lookup"><span data-stu-id="b5a15-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="b5a15-124">Levér</span><span class="sxs-lookup"><span data-stu-id="b5a15-124">Deliver</span></span>

<span data-ttu-id="b5a15-125">Når projektplanen er fuldført, og du er klar til at starte projektet, skal projektlederen opdatere projektfasen for **Levér** for at vise, at projektet er startet.</span><span class="sxs-lookup"><span data-stu-id="b5a15-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="b5a15-126">Fuldført</span><span class="sxs-lookup"><span data-stu-id="b5a15-126">Complete</span></span> 

<span data-ttu-id="b5a15-127">Når arbejdet på projektet er fuldført, kan projektlederen opdatere fasen til **Fuldført.**</span><span class="sxs-lookup"><span data-stu-id="b5a15-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="b5a15-128">Ved at opdatere projektfasen til **Fuldført** indikerer projektlederen, at arbejdet er 100 % fuldført, men at projektet holdes åbent, så alle uafsluttede tids- eller udgiftsposter kan registreres.</span><span class="sxs-lookup"><span data-stu-id="b5a15-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="b5a15-129">Luk</span><span class="sxs-lookup"><span data-stu-id="b5a15-129">Close</span></span>

<span data-ttu-id="b5a15-130">Når alle transaktioner er registreret for projektet, kan projektlederen opdatere fasen til **Luk.**</span><span class="sxs-lookup"><span data-stu-id="b5a15-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="b5a15-131">På dette tidspunkt kan der ikke registreres flere transaktioner, og projektet får indstillingen skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="b5a15-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]