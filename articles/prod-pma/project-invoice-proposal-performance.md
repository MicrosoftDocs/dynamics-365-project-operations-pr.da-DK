---
title: Ydeevne af forslag til projektfaktura
description: Dette emne indeholder oplysninger om forslag til forbedring af ydeevne for forslag til projektfakturaer.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269783"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="609df-103">Ydeevne af forslag til projektfaktura</span><span class="sxs-lookup"><span data-stu-id="609df-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="609df-104">Når du opretter et nyt fakturaforslag, kan du støde på problemer med ydeevnen, efterhånden som antallet af projekter og underprojekter øges.</span><span class="sxs-lookup"><span data-stu-id="609df-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="609df-105">Hvis ydeevnen skal forbedres, er der en funktion, der reducerer den tid, det tager at oprette et nyt fakturaforslag for bogførte projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="609df-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="609df-106">Aktivér forbedret ydeevne i forbindelse med projektfakturaforslag</span><span class="sxs-lookup"><span data-stu-id="609df-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="609df-107">Hvis du vil aktivere funktionen til forbedring af ydeevnen for forslag til projektfaktura, skal du fuldføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="609df-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="609df-108">Gå til **Funktionsstyring** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="609df-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="609df-109">I funktionslisten skal du finde **Forbedring af ydeevne for projektfakturaforslag**.</span><span class="sxs-lookup"><span data-stu-id="609df-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="609df-110">Vælg **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="609df-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="609df-111">Opdater din browser, og opret derefter et nyt fakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="609df-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="609df-112">Deaktivér forbedret ydeevne i forbindelse med projektfakturaforslag</span><span class="sxs-lookup"><span data-stu-id="609df-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="609df-113">Fuldfør følgende trin for at deaktivere funktionen til forbedring af ydeevnen for forslag til projektfaktura.</span><span class="sxs-lookup"><span data-stu-id="609df-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="609df-114">Gå til **Funktionsstyring** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="609df-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="609df-115">I funktionslisten skal du finde **Forbedring af ydeevne for projektfakturaforslag**.</span><span class="sxs-lookup"><span data-stu-id="609df-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="609df-116">Vælg **Deaktiver**.</span><span class="sxs-lookup"><span data-stu-id="609df-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="609df-117">Opdater browseren.</span><span class="sxs-lookup"><span data-stu-id="609df-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="609df-118">Ydeevnen for fakturaforslag kan ikke anvendes, når faktureringsregler er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="609df-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="609df-119">Under batchprocessen for at oprette fakturaforslag opdeler antallet af underopgaver opgaverne til et maksimumantal baseret på af antallet af kontrakter med fakturerbare transaktioner, uanset hvad du har angivet.</span><span class="sxs-lookup"><span data-stu-id="609df-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="609df-120">Hvis du f.eks. angiver **3** for antallet af underopgaver for oprettelse af fakturaforslag i batchjob, og der kun findes to kontrakter med fakturerbare transaktioner, oprettes der kun to underopgaver.</span><span class="sxs-lookup"><span data-stu-id="609df-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
