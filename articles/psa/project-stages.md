---
title: Typer af projektfaser
description: Dette emne indeholder oplysninger om projektfaser.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 521bf4b3090473a603626a99fded53906b644a7a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074223"
---
# <a name="project-stage-types"></a><span data-ttu-id="f07cf-103">Typer af projektfaser</span><span class="sxs-lookup"><span data-stu-id="f07cf-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f07cf-104">Projektfaser er udformet, så de afspejler projektets tilstand, mens det skrider frem.</span><span class="sxs-lookup"><span data-stu-id="f07cf-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="f07cf-105">Tilpasninger kan bruges til automatisk at opdatere faserne med forretningsprocesforløb, Power Automate eller plug-in-udvidelser.</span><span class="sxs-lookup"><span data-stu-id="f07cf-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="f07cf-106">Følgende faser er defineret i standard-BPF-forløbet:</span><span class="sxs-lookup"><span data-stu-id="f07cf-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="f07cf-107">Nyt</span><span class="sxs-lookup"><span data-stu-id="f07cf-107">New</span></span>
- <span data-ttu-id="f07cf-108">Tilbud</span><span class="sxs-lookup"><span data-stu-id="f07cf-108">Quote</span></span>
- <span data-ttu-id="f07cf-109">Planlæg</span><span class="sxs-lookup"><span data-stu-id="f07cf-109">Plan</span></span>
- <span data-ttu-id="f07cf-110">Levér</span><span class="sxs-lookup"><span data-stu-id="f07cf-110">Deliver</span></span>
- <span data-ttu-id="f07cf-111">Afsluttet</span><span class="sxs-lookup"><span data-stu-id="f07cf-111">Complete</span></span>
- <span data-ttu-id="f07cf-112">Luk</span><span class="sxs-lookup"><span data-stu-id="f07cf-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="f07cf-113">Ny</span><span class="sxs-lookup"><span data-stu-id="f07cf-113">New</span></span>

<span data-ttu-id="f07cf-114">Når du opretter et projekt, indstilles projektfasen til **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f07cf-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="f07cf-115">Hvis projektet blev oprettet ud fra en skabelon, kan det indeholde planlægnings-, estimat- og teamdata.</span><span class="sxs-lookup"><span data-stu-id="f07cf-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="f07cf-116">Ellers er det blot en kontur for projektet, og de resterende komponenter skal angives.</span><span class="sxs-lookup"><span data-stu-id="f07cf-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="f07cf-117">Tilbud</span><span class="sxs-lookup"><span data-stu-id="f07cf-117">Quote</span></span>

<span data-ttu-id="f07cf-118">Når du knytter et projekt til et tilbud, eller når du opretter et projekt fra et tilbud, angives projektfasen til **Tilbud** , og de forventede start- og slutdatoer opdateres.</span><span class="sxs-lookup"><span data-stu-id="f07cf-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote** , and the estimated start and end dates are updated.</span></span> <span data-ttu-id="f07cf-119">Når projektet befinder sig i fasen **Tilbud** , vises oplysninger om tilbuddet under fanen **Salg** på siden **Projektenhed**.</span><span class="sxs-lookup"><span data-stu-id="f07cf-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="f07cf-120">Planlæg</span><span class="sxs-lookup"><span data-stu-id="f07cf-120">Plan</span></span>

<span data-ttu-id="f07cf-121">Når du vinder et tilbud, der er knyttet til et projekt, og projektet flyttes til fasen **Kontrakt** , opdateres projektfasen til **Plan**.</span><span class="sxs-lookup"><span data-stu-id="f07cf-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="f07cf-122">Når projektet befinder sig i fasen **Plan** , vises oplysninger om kontrakten på fanen **Projektenhed**.</span><span class="sxs-lookup"><span data-stu-id="f07cf-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="f07cf-123">Levér</span><span class="sxs-lookup"><span data-stu-id="f07cf-123">Deliver</span></span>

<span data-ttu-id="f07cf-124">Når projektplanen er fuldført, og du er klar til at starte projektet, skal projektlederen opdatere projektfasen for **Levér** for at vise, at projektet er startet.</span><span class="sxs-lookup"><span data-stu-id="f07cf-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="f07cf-125">Fuldført</span><span class="sxs-lookup"><span data-stu-id="f07cf-125">Complete</span></span> 

<span data-ttu-id="f07cf-126">Når arbejdet på projektet er fuldført, kan projektlederen opdatere fasen til **Fuldført.**</span><span class="sxs-lookup"><span data-stu-id="f07cf-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="f07cf-127">Ved at opdatere projektfasen til **Fuldført** indikerer projektlederen, at arbejdet er 100 % fuldført, men at projektet holdes åbent, så alle uafsluttede tids- eller udgiftsposter kan registreres.</span><span class="sxs-lookup"><span data-stu-id="f07cf-127">By updating the project stage to **Complete** , the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="f07cf-128">Luk</span><span class="sxs-lookup"><span data-stu-id="f07cf-128">Close</span></span>

<span data-ttu-id="f07cf-129">Når alle transaktioner er registreret for projektet, kan projektlederen opdatere fasen til **Luk.**</span><span class="sxs-lookup"><span data-stu-id="f07cf-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="f07cf-130">På dette tidspunkt kan der ikke registreres flere transaktioner, og projektet får indstillingen skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="f07cf-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
