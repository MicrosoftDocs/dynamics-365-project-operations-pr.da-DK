---
title: Oprette et nyt projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter et nyt projekt.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006234"
---
# <a name="create-a-new-project"></a><span data-ttu-id="2113c-103">Oprette et nyt projekt</span><span class="sxs-lookup"><span data-stu-id="2113c-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2113c-104">Benyt følgende fremgangsmåde for at oprette et nyt projekt.</span><span class="sxs-lookup"><span data-stu-id="2113c-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="2113c-105">På siden **Projektstyring** skal du vælge **Nyt projekt** og angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="2113c-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="2113c-106">**Projekttype:** Tid og materiale</span><span class="sxs-lookup"><span data-stu-id="2113c-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="2113c-107">**Projektnavn:** XYZ-opgraderingsfase 2</span><span class="sxs-lookup"><span data-stu-id="2113c-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="2113c-108">**Projektgruppe:** TM\_IGVA</span><span class="sxs-lookup"><span data-stu-id="2113c-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="2113c-109">**Projektkontrakt-id:** 00000002</span><span class="sxs-lookup"><span data-stu-id="2113c-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="2113c-110">Vælg **Opret projekt**.</span><span class="sxs-lookup"><span data-stu-id="2113c-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="2113c-111">Tildel en ressource til et projekt</span><span class="sxs-lookup"><span data-stu-id="2113c-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="2113c-112">På siden **Arbejdere** i listen **Arbejdere** skal du vælge posten for den arbejder, som du tidligere konfigurerede kompetencer for, og åbne arbejderposten.</span><span class="sxs-lookup"><span data-stu-id="2113c-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="2113c-113">I handlingsruden skal du på fanen **Projekt** i gruppen **Opsætning** vælge **Tildel projekter**.</span><span class="sxs-lookup"><span data-stu-id="2113c-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="2113c-114">På siden **Projekttildelinger til ressourcevalidering** skal du på fanen **Projekter** i feltet **Tilføj projektet til valgte projekter** filtrere efter projektet **XYZ-opgraderingsfase 2**.</span><span class="sxs-lookup"><span data-stu-id="2113c-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="2113c-115">I ruden **Resterende projekter** skal du vælge et projekt og derefter vælge pileknappen for at tilføje det til ruden **Valgte projekter**.</span><span class="sxs-lookup"><span data-stu-id="2113c-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="2113c-116">Du kan også tildele kategorierne for en ressource, efterhånden som du har brug for det.</span><span class="sxs-lookup"><span data-stu-id="2113c-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="2113c-117">Kategoritypen er enten **Omkostning** eller **Omsætning**.</span><span class="sxs-lookup"><span data-stu-id="2113c-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="2113c-118">Kategoritypen bestemmes af din organisation.</span><span class="sxs-lookup"><span data-stu-id="2113c-118">The category type is determined by your organization.</span></span> <span data-ttu-id="2113c-119">Hvis der ikke er tildelt nogen kategorier for en ressource, søges Finance i standardkategorien efter timepriser for omkostninger og omsætning.</span><span class="sxs-lookup"><span data-stu-id="2113c-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="2113c-120">Konfigurer egenskaberne for projektressourcer og roller</span><span class="sxs-lookup"><span data-stu-id="2113c-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="2113c-121">En projektleder kan bruge funktionen projektressource til at oprette de roller, der kræves for projektet.</span><span class="sxs-lookup"><span data-stu-id="2113c-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="2113c-122">Roller kan bruges, hvis bekræftede ressourcer stadig ikke er kendte, når ressourcerne reserveres.</span><span class="sxs-lookup"><span data-stu-id="2113c-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="2113c-123">Roller kan reserveres midlertidigt som planlagte ressourcer, så du kan fortsætte med projektplanlægningsfaserne.</span><span class="sxs-lookup"><span data-stu-id="2113c-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="2113c-124">[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="2113c-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="2113c-125">**Scenarie:** Contoso blev hyret til at udarbejde et tids- og materialeprojekt, der har et godkendt projektcharter.</span><span class="sxs-lookup"><span data-stu-id="2113c-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="2113c-126">Den underordnede projektleder fuldfører stadig omfanget af projektet.</span><span class="sxs-lookup"><span data-stu-id="2113c-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="2113c-127">Den ressourceansvarlige identificerer i øjeblikket bestemte ressourcer, der skal reserveres til at arbejde på det nye projekt.</span><span class="sxs-lookup"><span data-stu-id="2113c-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="2113c-128">På grund af projektets vigtigste karakter anmoder projektsponsor om, at en af rollerne er den overordnede projektleder.</span><span class="sxs-lookup"><span data-stu-id="2113c-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="2113c-129">Den ressourceansvarlige skal erhverve den nye ressource og definere rollen i systemet i tilfælde af, at den underordnede projektleder kræver ressourceoplysningerne i forbindelse med projektplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="2113c-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="2113c-130">I følgende trin vises, hvordan den ressourceansvarlige kan konfigurere den overordnede projektleders rolle og knytte ressourceegenskaber til den.</span><span class="sxs-lookup"><span data-stu-id="2113c-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="2113c-131">Senere kan rollen bruges til at søge efter tilgængelige ressourcer, der matcher de nødvendige ressourcekompetencer.</span><span class="sxs-lookup"><span data-stu-id="2113c-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="2113c-132">På siden **Opsætning af roller** skal du vælge **Ny** og angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="2113c-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="2113c-133">**Rolle-id:** Overordnet projektleder</span><span class="sxs-lookup"><span data-stu-id="2113c-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="2113c-134">**Beskrivelse:** Overordnet projektleder</span><span class="sxs-lookup"><span data-stu-id="2113c-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="2113c-135">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="2113c-135">Select **Create**.</span></span>
3. <span data-ttu-id="2113c-136">Vælg rollen **Overordnet projektleder**, og vælg derefter **Konfigurer egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="2113c-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="2113c-137">I feltet **Egenskabstype** skal du vælge **Færdighed**.</span><span class="sxs-lookup"><span data-stu-id="2113c-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="2113c-138">I feltet **Tilgængelige egenskaber** skal du angive den færdighed, der skal søges efter.</span><span class="sxs-lookup"><span data-stu-id="2113c-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="2113c-139">I feltet **Egenskabstype** skal du vælge **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="2113c-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="2113c-140">I feltet **Tilgængelige egenskaber** skal du angive den certifikattype, der skal søges efter.</span><span class="sxs-lookup"><span data-stu-id="2113c-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="2113c-141">Tildel en projektressource til et projekt</span><span class="sxs-lookup"><span data-stu-id="2113c-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="2113c-142">På siden **Alle projekter** skal du vælge projektet **XYZ-opgraderingsfase 2**.</span><span class="sxs-lookup"><span data-stu-id="2113c-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="2113c-143">På fanen **Projektteam og planlægning** skal du vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2113c-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="2113c-144">I feltet **Rolle** skal du vælge **Teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="2113c-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="2113c-145">Vælge **Reserver fra kalenderen**.</span><span class="sxs-lookup"><span data-stu-id="2113c-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="2113c-146">På siden **Ressourcetilgængelighed** skal du vælge **Vis indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="2113c-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="2113c-147">På siden **Tilpasning visningsindstillinger** skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="2113c-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="2113c-148">**Format for visnings af datointerval:** Dag</span><span class="sxs-lookup"><span data-stu-id="2113c-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="2113c-149">**Vis beskrivelser af tilgængelighed:** Ja</span><span class="sxs-lookup"><span data-stu-id="2113c-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="2113c-150">**Vis resterende kapacitet:** Ja</span><span class="sxs-lookup"><span data-stu-id="2113c-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="2113c-151">Vælg en ressource på listen over ressourcer.</span><span class="sxs-lookup"><span data-stu-id="2113c-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="2113c-152">Vælg **Reserver definitivt** og **Fuld kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="2113c-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="2113c-153">Tildel en ressource til en standardrolle</span><span class="sxs-lookup"><span data-stu-id="2113c-153">Assign a resource to a default role</span></span>

<span data-ttu-id="2113c-154">For at hjælpe projektledere eller ressourceansvarlige med yderligere detailudledning om de ressourcer, der kan reserveres til et projekt.</span><span class="sxs-lookup"><span data-stu-id="2113c-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="2113c-155">Du kan knytte en standardrolle til en eksisterende ressource eller en nyerhvervet ressource.</span><span class="sxs-lookup"><span data-stu-id="2113c-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="2113c-156">F.eks. da Daniel blev ansat, havde han den erfaring og de færdigheder, der var nødvendige for at udfylde rollen som forretningsanalytiker.</span><span class="sxs-lookup"><span data-stu-id="2113c-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="2113c-157">Den ressourceansvarlige har tildelt denne rolle som Daniel standardrolle.</span><span class="sxs-lookup"><span data-stu-id="2113c-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="2113c-158">Den ressourceansvarlige har derfor føjet Daniel til en gruppe med forretningsanalytikere, som er til rådighed til at kunne arbejde med projekter.</span><span class="sxs-lookup"><span data-stu-id="2113c-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="2113c-159">I forbindelse med ressourcereservationen kan projektledere filtrere de rolleressourcer, der er tilgængelige til at kunne arbejde på projekter.</span><span class="sxs-lookup"><span data-stu-id="2113c-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="2113c-160">De kan bruge disse oplysninger som et kriterium, når de udfører beslutningsanalyse med flere kriterier under ressourceopfyldning.</span><span class="sxs-lookup"><span data-stu-id="2113c-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="2113c-161">De kan også tilføje andre ressourceegenskaber til filteret for at søge efter ressourcer, der har bestemte færdigheder, uddannelser og erfaring i forbindelse med et bestemt projekt.</span><span class="sxs-lookup"><span data-stu-id="2113c-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="2113c-162">**Scenarie:** Et godkendt projekt er påbegyndt, og rollen som overordnet projektleder blev reserveret som en planlagt ressource i projektplanlægningsfasen.</span><span class="sxs-lookup"><span data-stu-id="2113c-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="2113c-163">Den ressourceansvarlige har nu erhvervet en ressource, der skal udføre rollen overordnet projektleder.</span><span class="sxs-lookup"><span data-stu-id="2113c-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="2113c-164">På siden **Ressourceliste** skal du vælge **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="2113c-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="2113c-165">På siden **Ressourcerolle** skal du vælge **Ny** og angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="2113c-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="2113c-166">**Ikrafttrædelse:** Angiv den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="2113c-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="2113c-167">**Udløb:** Angiv **Aldrig**.</span><span class="sxs-lookup"><span data-stu-id="2113c-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="2113c-168">**Rolle:** Angiv **Overordnet projektleder**.</span><span class="sxs-lookup"><span data-stu-id="2113c-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="2113c-169">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="2113c-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="2113c-170">På fanen **Kompetencer** skal du tilføje færdigheden **ProjectMgmt** og certifikatet **PMP**.</span><span class="sxs-lookup"><span data-stu-id="2113c-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]