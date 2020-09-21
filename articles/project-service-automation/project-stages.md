---
title: Projektfaser
description: Dette emne indeholder oplysninger om projektfaser.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750519"
---
# <a name="project-stages"></a><span data-ttu-id="ab15b-103">Projektfaser</span><span class="sxs-lookup"><span data-stu-id="ab15b-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ab15b-104">Projektfaserne opdateres, så de afspejler projektets tilstand, mens det skrider frem.</span><span class="sxs-lookup"><span data-stu-id="ab15b-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="ab15b-105">I standardforretningsprocesforløbet opdateres nogle faser i projektet automatisk, mens andre opdateres manuelt af projektlederen.</span><span class="sxs-lookup"><span data-stu-id="ab15b-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="ab15b-106">Følgende faser er defineret i standard-BPF-forløbet:</span><span class="sxs-lookup"><span data-stu-id="ab15b-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="ab15b-107">Ny</span><span class="sxs-lookup"><span data-stu-id="ab15b-107">New</span></span>
- <span data-ttu-id="ab15b-108">Tilbud</span><span class="sxs-lookup"><span data-stu-id="ab15b-108">Quote</span></span>
- <span data-ttu-id="ab15b-109">Planlæg</span><span class="sxs-lookup"><span data-stu-id="ab15b-109">Plan</span></span>
- <span data-ttu-id="ab15b-110">Levér</span><span class="sxs-lookup"><span data-stu-id="ab15b-110">Deliver</span></span>
- <span data-ttu-id="ab15b-111">Afsluttet</span><span class="sxs-lookup"><span data-stu-id="ab15b-111">Complete</span></span>
- <span data-ttu-id="ab15b-112">Luk</span><span class="sxs-lookup"><span data-stu-id="ab15b-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="ab15b-113">Ny</span><span class="sxs-lookup"><span data-stu-id="ab15b-113">New</span></span>

<span data-ttu-id="ab15b-114">Når du opretter et projekt, indstilles projektfasen til **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab15b-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="ab15b-115">Hvis projektet blev oprettet ud fra en skabelon, kan det indeholde planlægnings-, estimat- og teamdata.</span><span class="sxs-lookup"><span data-stu-id="ab15b-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="ab15b-116">Ellers er det blot en kontur for projektet, og de resterende komponenter skal angives.</span><span class="sxs-lookup"><span data-stu-id="ab15b-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="ab15b-117">Tilbud</span><span class="sxs-lookup"><span data-stu-id="ab15b-117">Quote</span></span>

<span data-ttu-id="ab15b-118">Når du knytter et projekt til et tilbud, eller når du opretter et projekt fra et tilbud, angives projektfasen til **Tilbud**, og de forventede start- og slutdatoer opdateres.</span><span class="sxs-lookup"><span data-stu-id="ab15b-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="ab15b-119">Når projektet befinder sig i fasen **Tilbud**, vises oplysninger om tilbuddet under fanen **Salg** på siden **Projektenhed**.</span><span class="sxs-lookup"><span data-stu-id="ab15b-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="ab15b-120">Planlæg</span><span class="sxs-lookup"><span data-stu-id="ab15b-120">Plan</span></span>

<span data-ttu-id="ab15b-121">Når du vinder et tilbud, der er knyttet til et projekt, og projektet flyttes til fasen **Kontrakt**, opdateres projektfasen til **Plan**.</span><span class="sxs-lookup"><span data-stu-id="ab15b-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="ab15b-122">Når projektet befinder sig i fasen **Plan**, vises oplysninger om kontrakten på fanen **Projektenhed**.</span><span class="sxs-lookup"><span data-stu-id="ab15b-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="ab15b-123">Levér</span><span class="sxs-lookup"><span data-stu-id="ab15b-123">Deliver</span></span>

<span data-ttu-id="ab15b-124">Når projektplanen er fuldført, og du er klar til at starte projektet, skal projektlederen opdatere projektfasen for **Levér** for at vise, at projektet er startet.</span><span class="sxs-lookup"><span data-stu-id="ab15b-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="ab15b-125">Fuldført</span><span class="sxs-lookup"><span data-stu-id="ab15b-125">Complete</span></span> 

<span data-ttu-id="ab15b-126">Når arbejdet på projektet er fuldført, kan projektlederen opdatere fasen til **Fuldført.**</span><span class="sxs-lookup"><span data-stu-id="ab15b-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="ab15b-127">Ved at opdatere projektfasen til **Fuldført**indikerer projektlederen, at arbejdet er 100 % fuldført, men at projektet holdes åbent, så alle uafsluttede tids- eller udgiftsposter kan registreres.</span><span class="sxs-lookup"><span data-stu-id="ab15b-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="ab15b-128">Luk</span><span class="sxs-lookup"><span data-stu-id="ab15b-128">Close</span></span>

<span data-ttu-id="ab15b-129">Når alle transaktioner er registreret for projektet, kan projektlederen opdatere fasen til **Luk.**</span><span class="sxs-lookup"><span data-stu-id="ab15b-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="ab15b-130">På dette tidspunkt kan der ikke registreres flere transaktioner, og projektet får indstillingen skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="ab15b-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
