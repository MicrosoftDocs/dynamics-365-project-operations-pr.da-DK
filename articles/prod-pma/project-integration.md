---
title: Integration med Microsoft Project Client
description: Planlægning og vedligeholdelse af en projektplan kan være kompliceret, så projektlederne har brug for værktøjer, der hjælper dem med at administrere denne opgave. Integration med Microsoft Project Client understøtter oprettelse og administration af et projekts arbejdsopgavehierarki.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074233"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="f608a-104">Integration med Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f608a-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f608a-105">Planlægning og vedligeholdelse af en projektplan kan være kompliceret, så projektlederne har brug for værktøjer, der hjælper dem med at administrere denne opgave.</span><span class="sxs-lookup"><span data-stu-id="f608a-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="f608a-106">Integration med Microsoft Project Client understøtter oprettelse og administration af et projekts arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="f608a-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="f608a-107">Projektlederen kan publicere eventuelle ændringer tilbage til Dynamics 365 Finance-projektets arbejdsopgavehierarki.</span><span class="sxs-lookup"><span data-stu-id="f608a-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="f608a-108">Hvis du bruger opdateringen fra juli (version 10.0.4), skal du installere KB 4054797 og 4055884.</span><span class="sxs-lookup"><span data-stu-id="f608a-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="f608a-109">Konfigurer Microsoft Project Client-tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="f608a-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="f608a-110">Hvis du vil aktivere integrationen med Microsoft Project Client, skal du installere et Microsoft Dynamics 365-tilføjelsesprogram i brugerens klient til Microsoft Project-programmet.</span><span class="sxs-lookup"><span data-stu-id="f608a-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="f608a-111">Det kan du gøre ved at åbne **Arbejdsområdet for projektstyring**.</span><span class="sxs-lookup"><span data-stu-id="f608a-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="f608a-112">• Klik på **Konfigurer tilføjelsesprogrammet for projektklient** fra arbejdsområdesektionen **Links** > **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="f608a-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="f608a-113">• Klik på **Åbn** , og klik derefter på **Kør** , når du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="f608a-113">•   Click **Open** , then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="f608a-114">Åbn og rediger et eksisterende udkast til et arbejdsopgavehierarki i Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f608a-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="f608a-115">Hvis et projekt i Dynamics 365 Finance allerede har et arbejdsopgavehierarki, kan arbejdsopgavehierarkiet åbnes i Microsoft Project Client-programmet, hvis arbejdsopgavehierarkiet er i kladdestatus.</span><span class="sxs-lookup"><span data-stu-id="f608a-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="f608a-116">Hvis du vil åbne siden **Projekt** , skal du klikke på linket **Åbn i Microsoft Project** fra fanen **Plan**. Du kan også åbne denne side fra Microsoft Project Client-programmet ved at klikke på **Åbn** i fanen **Microsoft Dynamics 365**. Vælg den **Juridiske enhed** og **Projektet** på listen.</span><span class="sxs-lookup"><span data-stu-id="f608a-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="f608a-117">Hvis du bruger Internet Explorer som browser, skal du klikke på **Gem** for at åbne den manuelt fra den placering, hvor filen er overført til.</span><span class="sxs-lookup"><span data-stu-id="f608a-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="f608a-118">Du kan også klikke på **Gem og Åbn** for at åbne filen i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f608a-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="f608a-119">Du skal ikke omdøbe filnavnet, når du gemmer.</span><span class="sxs-lookup"><span data-stu-id="f608a-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="f608a-120">Før du foretager ændringer af filen ved hjælp af Microsoft Project Client, skal du tjekke den ud. Klik på **Tjek ud** under fanen **Microsoft Dynamics 365**. Derved forhindres andre brugere i at redigere arbejdsopgavehierarkiet i Finance på samme tid.</span><span class="sxs-lookup"><span data-stu-id="f608a-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="f608a-121">Hvis du vil publicere arbejdsopgavehierarkiet, når du har fuldført redigeringen, skal du klikke på **Tjek ind** på fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f608a-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="f608a-122">Hvis der allerede er tilføjet en projektgruppe til projektet i Finance, udfyldes ressourcelisten med teammedlemmerne.</span><span class="sxs-lookup"><span data-stu-id="f608a-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="f608a-123">Hvis et projektteam endnu ikke er blevet tilføjet til projektet, kan du vælge ressourcer og oprette teamet i Microsoft Project Client ved at klikke på knappen **Ressourcer** under fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f608a-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="f608a-124">Følgende data er synkroniseret tilbage til Finance som en del af indtjekningsprocessen:</span><span class="sxs-lookup"><span data-stu-id="f608a-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="f608a-125">• Opgavenavn</span><span class="sxs-lookup"><span data-stu-id="f608a-125">•   Task name</span></span>

<span data-ttu-id="f608a-126">• Startdato</span><span class="sxs-lookup"><span data-stu-id="f608a-126">•   Start date</span></span>

<span data-ttu-id="f608a-127">• Slutdato</span><span class="sxs-lookup"><span data-stu-id="f608a-127">•   Finish date</span></span>

<span data-ttu-id="f608a-128">• Foregående</span><span class="sxs-lookup"><span data-stu-id="f608a-128">•   Predecessors</span></span>

<span data-ttu-id="f608a-129">• Ressourcenavne</span><span class="sxs-lookup"><span data-stu-id="f608a-129">•   Resource names</span></span>

<span data-ttu-id="f608a-130">• Kategori</span><span class="sxs-lookup"><span data-stu-id="f608a-130">•   Category</span></span>

<span data-ttu-id="f608a-131">• Ressourcekategori</span><span class="sxs-lookup"><span data-stu-id="f608a-131">•   Resource category</span></span>

<span data-ttu-id="f608a-132">• Arbejdstimer</span><span class="sxs-lookup"><span data-stu-id="f608a-132">•   Work hours</span></span>

<span data-ttu-id="f608a-133">• Noter</span><span class="sxs-lookup"><span data-stu-id="f608a-133">•   Notes</span></span>

<span data-ttu-id="f608a-134">• Prioritet</span><span class="sxs-lookup"><span data-stu-id="f608a-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="f608a-135">Hvis du tilføjer andre kolonner til din Microsoft Project Client-fil, bliver de ikke gemt i filen, og de vises ikke, når filen åbnes igen.</span><span class="sxs-lookup"><span data-stu-id="f608a-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f608a-136">Opret arbejdsopgavehierarkiet for et eksisterende projekt ved hjælp af Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f608a-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f608a-137">Hvis du vil oprette et nyt arbejdsopgavehierarki ved hjælp af Microsoft Project Client, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="f608a-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="f608a-138">Åbn Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f608a-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f608a-139">På fanen **Microsoft Dynamics 365** skal du klikke på **Åbn** .</span><span class="sxs-lookup"><span data-stu-id="f608a-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="f608a-140">Vælg projektets **Juridiske enhed**.</span><span class="sxs-lookup"><span data-stu-id="f608a-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="f608a-141">Vælg **Projektet**.</span><span class="sxs-lookup"><span data-stu-id="f608a-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="f608a-142">Klik på **Tjek ud** under fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f608a-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="f608a-143">Når du er klar til at publicere til Finance, skal du klikke på **Tjek ind** under fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f608a-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f608a-144">Erstat det eksisterende arbejdsopgavehierarki for et eksisterende projekt ved hjælp af Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f608a-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f608a-145">Hvis du vil oprette et nyt arbejdsopgavehierarki ved hjælp af Microsoft Project Client og erstatte et eksisterende arbejdsopgavehierarki for et eksisterende projekt, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="f608a-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="f608a-146">Åbn Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f608a-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f608a-147">Opret skemaet i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f608a-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f608a-148">På fanen **Microsoft Dynamics 365** skal du klikke på **Gem ændringer** > **Erstat eksisterende projekt**.</span><span class="sxs-lookup"><span data-stu-id="f608a-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="f608a-149">Vælg projektets **Juridiske enhed**.</span><span class="sxs-lookup"><span data-stu-id="f608a-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f608a-150">Vælg **Projektet**.</span><span class="sxs-lookup"><span data-stu-id="f608a-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="f608a-151">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="f608a-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="f608a-152">Opret et nyt projekt fra Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f608a-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="f608a-153">Åbn Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f608a-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f608a-154">Opret skemaet i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f608a-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f608a-155">På fanen **Microsoft Dynamics 365** skal du klikke på **Gem ændringer** > **Gem som nyt projekt**.</span><span class="sxs-lookup"><span data-stu-id="f608a-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="f608a-156">Vælg projektets **Juridiske enhed**.</span><span class="sxs-lookup"><span data-stu-id="f608a-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f608a-157">Angiv eventuelt **Projekt-id**.</span><span class="sxs-lookup"><span data-stu-id="f608a-157">Enter the **Project ID** , if necessary.</span></span>

6.  <span data-ttu-id="f608a-158">Angiv **Projektnavnet**.</span><span class="sxs-lookup"><span data-stu-id="f608a-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="f608a-159">Vælg **Projekttype** , **Projektgruppe** og **Projektkontrakt-id**.</span><span class="sxs-lookup"><span data-stu-id="f608a-159">Select the **Project type** , **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="f608a-160">Du kan også oprette en ny projektkontrakt ved at klikke på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f608a-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="f608a-161">Vælg den **Kalender** , der skal bruges til ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f608a-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="f608a-162">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="f608a-162">Click **OK**.</span></span>
