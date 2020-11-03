---
title: Eliminer et projektestimat
description: Dette emne indeholder oplysninger om, hvordan du eliminerer et projektestimat, efter at det er fuldført.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074225"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="c1d9c-103">Eliminer et projektestimat</span><span class="sxs-lookup"><span data-stu-id="c1d9c-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1d9c-104">Projektestimater giver en økonomisk visning af det arbejde, der er estimeret og planlagt i et projekt.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="c1d9c-105">Hvis du vil arbejde med estimater for et projekt, skal du knytte projektet til et estimatprojekt.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="c1d9c-106">Et estimatprojekt er altid baseret på et eksisterende projekt, men flere projekter kan referere til et enkelt estimatprojekt.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="c1d9c-107">Det er kun fastprisprojekter og investeringsprojekter, der kan tilknyttes estimatprojekter, og de pågældende projekter skal tilhøre samme projektgruppe som det estimerede projekt.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="c1d9c-108">Hvis du vil eliminere et estimatprojekt, skal det være fuldført.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="c1d9c-109">Følgende fremgangsmåde beskriver, hvordan du kan eliminerer et estimat.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="c1d9c-110">Gå til **Projektstyring og regnskab** > **Alle projekter** , og åbn projektet.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="c1d9c-111">På fanen **Administrer** skal du vælge **Estimater** , og på siden **Estimer** skal du vælge **Eliminer**.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="c1d9c-112">På siden **Eliminer estimat** skal du på fanen **Generelt** angive følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="c1d9c-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="c1d9c-113">**Periodekode** : Vælg periodekoden for at vælge de relevante estimatprojekter.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="c1d9c-114">**Estimatdato** : Vælg den relevante estimatdato, der skal elimineres.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="c1d9c-115">**Fjern med IGVA-advarsler** : Aktivér denne indstilling for at give besked, når et estimat, der er knyttet til igangværende arbejde (IGVA), elimineres.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="c1d9c-116">Hvis denne indstilling ikke er aktiveret, kan elimineringen ikke fortsætte, hvis der findes ikke-estimerede transaktioner.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="c1d9c-117">Denne indstilling er kun tilgængelig, når elimineringen finder anvendelse på et estimatprojekt.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="c1d9c-118">Den er ikke tilgængelig, hvis du bruger periodiske bogføringer.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="c1d9c-119">Denne indstilling fungerer sammen med indstillingerne under fanen **Estimat** på siden **Projektparametre** i feltgruppen **Tillad eliminering, når der findes ikke-estimerede transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="c1d9c-120">**Angiv stadie for afslutning** : Aktivér denne indstilling for at angive, at estimatprojektets fase skal **Afsluttes** , når du har kørt elimineringen.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="c1d9c-121">**Udskriv estimatliste** : Vælg de oplysninger, der skal medtages, når estimatlisten udskrives.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="c1d9c-122">**Vis infolog** : Aktivér denne indstilling for at få vist infologgen.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="c1d9c-123">**Bogføringsdato** : Vælg estimatets bogføringsdato i hovedbogen.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="c1d9c-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-124">Select **OK**.</span></span>
5. <span data-ttu-id="c1d9c-125">Når elimineringsprocessen er fuldført, vises det eliminerede estimatprojekt med en negativ værdi.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="c1d9c-126">Hvis du ikke har tænkt dig at eliminere et estimat, kan du vælge det eliminerede estimat og vælge **Tilbagefør eliminering**.</span><span class="sxs-lookup"><span data-stu-id="c1d9c-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
