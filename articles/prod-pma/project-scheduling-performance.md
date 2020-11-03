---
title: Ydeevne for et projekts ressourceplanlægning
description: Dette emne indeholder oplysninger om, hvordan du kan forbedre ydeevnen af ressourceplanlægning for et stort antal projekter.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074155"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="0125d-103">Ydeevne for et projekts ressourceplanlægning</span><span class="sxs-lookup"><span data-stu-id="0125d-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="0125d-104">Ydeevneproblemer, der er relaterede til ressourceplanlægning, kan forekomme, når antallet af projekter når op i tusinder.</span><span class="sxs-lookup"><span data-stu-id="0125d-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="0125d-105">Hvis du vil forbedre ydeevnen i ressourceplanlægning, er der en tilgængelig funktion, som gør det muligt for brugerne at reducere den tid, det tager at åbne formularen med ressourcetilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="0125d-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="0125d-106">Dette fjerner især processen med synkronisering af akkumulering af ressourcekapacitet og bruger tabellen **ResProjectResource** til at gøre søgningen i ressourcer hurtigere.</span><span class="sxs-lookup"><span data-stu-id="0125d-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="0125d-107">Bemærk, at tabellen **ResRollup** ikke længere skal bruges.</span><span class="sxs-lookup"><span data-stu-id="0125d-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0125d-108">Hvis der er en afhængighed i enten processen med synkronisering af akkumulering af ressourcekapacitet eller tabellen **ResProjectResource** , skal du ikke bruge denne funktion.</span><span class="sxs-lookup"><span data-stu-id="0125d-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="0125d-109">Aktiver forbedring af ydeevnen for ressourceplanlægning</span><span class="sxs-lookup"><span data-stu-id="0125d-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="0125d-110">Hvis du vil aktivere forbedring af ydeevnen for ressourceplanlægning, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="0125d-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="0125d-111">Gå til **Funktionsstyring** > **Alle** , og find **Aktiver funktionen til forbedring af ydeevnen for projektressourceplanlægning** på funktionslisten.</span><span class="sxs-lookup"><span data-stu-id="0125d-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="0125d-112">Vælg **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="0125d-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="0125d-113">Hvis du ikke kan finde funktionen på listen, skal du vælge **Søg efter opdateringer** for at opdatere listen.</span><span class="sxs-lookup"><span data-stu-id="0125d-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="0125d-114">Opdater browseren, og gå derefter til **Projektstyring og regnskab** > **Periodisk** > **Projektressourcer** > **Synkroniser ressourcekalenderes kapacitet på tværs af alle virksomheder**.</span><span class="sxs-lookup"><span data-stu-id="0125d-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="0125d-115">Angiv **Fjern eksisterende kapacitetsposter** til **Ja** for at fjerne tidligere data.</span><span class="sxs-lookup"><span data-stu-id="0125d-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="0125d-116">Hvis du vil oprette trinvise data, skal du angive den til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="0125d-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="0125d-117">I feltet **Periodekode** skal du vælge den periode, hvor der skal genereres data.</span><span class="sxs-lookup"><span data-stu-id="0125d-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="0125d-118">Hvis du vælger en periodekode, er det ikke nødvendigt at definere en start- og slutdato.</span><span class="sxs-lookup"><span data-stu-id="0125d-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="0125d-119">Hvis du lader feltet **Periodekode** være tomt, skal du vælge bestemte start- og slutdatoer for at oprette data.</span><span class="sxs-lookup"><span data-stu-id="0125d-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="0125d-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0125d-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="0125d-121">Dette distribuerer generelle data til tabellen **ResCalendarCapacity** på tværs af alle virksomheder i dit miljø, så batchjobbet kun skal køres i én juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="0125d-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="0125d-122">Dataene i denne kørsel skal bruges til at beregne ressourcekapaciteten via den tilknyttede kalender.</span><span class="sxs-lookup"><span data-stu-id="0125d-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="0125d-123">Gå til **Projektstyring og regnskab** > **Periodisk** > **Projektressourcer** > **Udfyld projektressourcer på tværs af alle virksomheder** , og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0125d-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="0125d-124">Dette er scriptet til dataopgradering for generelle data i tabellerne **ResProjectResource** , **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="0125d-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="0125d-125">Værdierne for feltet **PSAPRojSchedRole.RootActivity** opdateres også.</span><span class="sxs-lookup"><span data-stu-id="0125d-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="0125d-126">Hvis den ikke køres, vises der en advarsel, når du forsøger at udføre ressourceplanlægningshandlinger.</span><span class="sxs-lookup"><span data-stu-id="0125d-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="0125d-127">Deaktiver forbedring af ydeevnen for ressourceplanlægning</span><span class="sxs-lookup"><span data-stu-id="0125d-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="0125d-128">Gå til **Funktionsstyring** > **Alle** , og søg efter **Aktiver funktionen til forbedring af ydeevnen for projektressourceplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="0125d-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="0125d-129">Vælg funktionen, og vælg derefter knappen **Deaktiver**.</span><span class="sxs-lookup"><span data-stu-id="0125d-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="0125d-130">Opdater browseren.</span><span class="sxs-lookup"><span data-stu-id="0125d-130">Refresh your browser.</span></span>
4. <span data-ttu-id="0125d-131">Gå til **Projektstyring og regnskab** > **Periodisk** > **Kapacitetssynkronisering** > **Synkroniser ressourcekapacitetsakkumuleringer**.</span><span class="sxs-lookup"><span data-stu-id="0125d-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="0125d-132">På siden **Synkronisering af akkumulering af kapacitet** skal du angive **Fjern eksisterende kapacitetsposter** til **Ja** for at fjerne tidligere data.</span><span class="sxs-lookup"><span data-stu-id="0125d-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="0125d-133">Hvis du vil oprette trinvise data, skal du angive den til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="0125d-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="0125d-134">I feltet **Periodekode** skal du vælge den periode, hvor der skal genereres data.</span><span class="sxs-lookup"><span data-stu-id="0125d-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="0125d-135">Hvis du vælger en periodekode, er det ikke nødvendigt at definere en start- og slutdato.</span><span class="sxs-lookup"><span data-stu-id="0125d-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="0125d-136">Hvis du lader feltet **Periodekode** være tomt, skal du vælge bestemte start- og slutdatoer for at oprette data.</span><span class="sxs-lookup"><span data-stu-id="0125d-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="0125d-137">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0125d-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="0125d-138">Dette distribuerer generelle data til tabellen **ResRollup** på tværs af alle virksomheder i dit miljø, så batchjobbet kun skal køres i én juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="0125d-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="0125d-139">Denne kørsel er nødvendig for alle visninger af **Ressourcetilgængelighed**.</span><span class="sxs-lookup"><span data-stu-id="0125d-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="0125d-140">Hvis batchjobbet ikke køres, vil dataene **ResRollup** blive genereret løbende, hvilket kan tage lang tid.</span><span class="sxs-lookup"><span data-stu-id="0125d-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
