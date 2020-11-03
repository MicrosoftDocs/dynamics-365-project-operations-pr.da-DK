---
title: Konfigurer integration af Project Operations for de enkelte juridiske enheder
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer integrationen af juridiske enheder i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096745"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="6a8df-103">Konfigurer integration af Project Operations for de enkelte juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="6a8df-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="6a8df-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="6a8df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6a8df-105">Dette emne gennemgår de trin, der er nødvendige for at konfigurere Dynamics 365 Project Operations pr. juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="6a8df-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="6a8df-106">Aktiver funktionsnøgler i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="6a8df-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="6a8df-107">Benyt følgende fremgangsmåde for at aktivere de påkrævede funktioner.</span><span class="sxs-lookup"><span data-stu-id="6a8df-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="6a8df-108">I Dynamics 365 Finance skal du gå til arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="6a8df-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="6a8df-109">I **Funktionslisten** skal du finde og aktivere følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="6a8df-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="6a8df-110">**Aktiver flere kontraktlinjer for et projekt**</span><span class="sxs-lookup"><span data-stu-id="6a8df-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="6a8df-111">**Aktiver Project Operations på Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="6a8df-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="6a8df-112">Hvis du ikke kan se de anførte **Funktionsnøgler** , skal du kontrollere, at din version af Finance opfylder minimumsversionskravet (programversion 10.0.13 eller højere, hvor alle kvalitetsopdateringer er anvendt).</span><span class="sxs-lookup"><span data-stu-id="6a8df-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="6a8df-113">Vælg **Kontroller, om der er opdateringer** for at opdatere funktionslisten.</span><span class="sxs-lookup"><span data-stu-id="6a8df-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="6a8df-114">Definer udrulningsscenariet for Project Operations for en juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="6a8df-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="6a8df-115">Du kan aktivere Project Operations på Dynamics 365 Customer Engagement på juridisk enhedsniveau.</span><span class="sxs-lookup"><span data-stu-id="6a8df-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="6a8df-116">Du kan have én juridisk enhed, som anvender Project Operations på Dynamics 365 Customer Engagement til ressource/ikke-lagerbaserede scenarier.</span><span class="sxs-lookup"><span data-stu-id="6a8df-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="6a8df-117">Du kan i det samme miljø have en anden juridisk enhed, som anvender Project Operations i forbindelse med lagerførte/produktionsordrebaserede scenarier.</span><span class="sxs-lookup"><span data-stu-id="6a8df-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="6a8df-118">I Dynamics 365 Finance skal du gå til **Projektstyring og regnskab** > **Opsætning** > **Globale parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="6a8df-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="6a8df-119">Vælg objekter på listen over tilgængelige juridiske objekter, hvor funktioner vedrørende flere kontraktlinjer og Project Operations på Dynamics 365 Customer Engagement er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="6a8df-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="6a8df-120">Lad være med at vælge de juridiske enheder, der skal bruge Project Operations i forbindelse med lagerbaserede/produktionsordrescenarier.</span><span class="sxs-lookup"><span data-stu-id="6a8df-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="6a8df-121">Det er kun muligt at vælge en juridisk enhed, hvis den ikke har eksisterende projekter.</span><span class="sxs-lookup"><span data-stu-id="6a8df-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="6a8df-122">Konfigurer parametre for Projektstyring og regnskab</span><span class="sxs-lookup"><span data-stu-id="6a8df-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="6a8df-123">De enkelte juridiske objekter, der bruger lagerbaserede/produktionsordrescenarier på Dynamics 365 Customer Engagement, skal have et sæt standardparametre.</span><span class="sxs-lookup"><span data-stu-id="6a8df-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="6a8df-124">Disse parametre er konfigureret under fanen **Project Operations** på siden **Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="6a8df-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="6a8df-125">Parametrene er:</span><span class="sxs-lookup"><span data-stu-id="6a8df-125">The parameters are:</span></span>

  - <span data-ttu-id="6a8df-126">**Standardfaktureringstyper** : Project Operations bruger et fast sæt faktureringstypestandarder, der skal knyttes til linjeegenskaber i Finance.</span><span class="sxs-lookup"><span data-stu-id="6a8df-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="6a8df-127">Opret en post for hver faktureringstype: **Ikke angivet** , **Fakturerbar** , **Ikke-fakturerbar** , **Gratis** og **Ikke tilgængelig**.</span><span class="sxs-lookup"><span data-stu-id="6a8df-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="6a8df-128">**Standardprojektkategorier** : Vælg de standardprojektkategorier, der skal bruges for de enkelte transaktionstyper.</span><span class="sxs-lookup"><span data-stu-id="6a8df-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="6a8df-129">Disse standardindstillinger bruges i **Integrationskladden i Project Operations** og i estimater, hvor der ikke er angivet nogen transaktionskategori for projektets faktiske værdi.</span><span class="sxs-lookup"><span data-stu-id="6a8df-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="6a8df-130">**Prognoser** : Vælg den prognosemodel, der skal bruges til estimater for tid og udgifter.</span><span class="sxs-lookup"><span data-stu-id="6a8df-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
