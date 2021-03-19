---
title: Fejlfinding i forbindelse med arbejde i opgavegitteret
description: Dette emne indeholder oplysninger om de nødvendige fejlfindingsoplysninger, når du arbejder i opgavegitteret.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286556"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="5d113-103">Fejlfinding i forbindelse med arbejde i opgavegitteret</span><span class="sxs-lookup"><span data-stu-id="5d113-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="5d113-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5d113-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5d113-105">Dette emne beskriver, hvordan du kan løse de problemer, du eventuelt støder på, når du arbejder med omkostningsstyring.</span><span class="sxs-lookup"><span data-stu-id="5d113-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="5d113-106">Aktiver cookies</span><span class="sxs-lookup"><span data-stu-id="5d113-106">Enable cookies</span></span>

<span data-ttu-id="5d113-107">Project Operations kræver aktivering af tredjepartscookies med henblik på at gengive arbejdsopgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5d113-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="5d113-108">Når tredjepartscookies ikke er aktiveret, kan du i stedet for at få vist opgaver se en tom side, når du vælger fanen **Opgaver** på siden **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="5d113-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Der vises en tom fane, når tredjepartscookies er aktiveret](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="5d113-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="5d113-110">Workaround</span></span>
<span data-ttu-id="5d113-111">I Microsoft Edge eller Google Chrome-browsere beskriver følgende procedurer det, hvordan du kan opdatere din browserindstilling for at aktivere tredjepartscookies.</span><span class="sxs-lookup"><span data-stu-id="5d113-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="5d113-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5d113-112">Microsoft Edge</span></span>

1. <span data-ttu-id="5d113-113">Åbn din Edge-browser.</span><span class="sxs-lookup"><span data-stu-id="5d113-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="5d113-114">I øverste højre hjørne skal du vælge **ellipsen** (...) og dernæst vælge **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="5d113-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="5d113-115">Under **Cookies og sidetilladelser** skal du vælge **Cookies og websitedata**.</span><span class="sxs-lookup"><span data-stu-id="5d113-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="5d113-116">Slå **Blokering af tredjepartscookies** fra.</span><span class="sxs-lookup"><span data-stu-id="5d113-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="5d113-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="5d113-117">Google Chrome</span></span>

1. <span data-ttu-id="5d113-118">Åbn din Chrome-browser.</span><span class="sxs-lookup"><span data-stu-id="5d113-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="5d113-119">Vælg de tre vertikale prikker i øverste højre hjørne, og vælg derefter **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="5d113-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="5d113-120">Under **Sikkerhed og privatliv** skal du vælge **Cookies og websitedata**.</span><span class="sxs-lookup"><span data-stu-id="5d113-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="5d113-121">Vælg **Tillad alle cookies**.</span><span class="sxs-lookup"><span data-stu-id="5d113-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d113-122">Hvis du blokerer tredjepartscookies, blokeres alle cookies og websitedata fra andre websteder, også selvom websitet er tilladt på din undtagelsesliste.</span><span class="sxs-lookup"><span data-stu-id="5d113-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="5d113-123">PEX-slutpunkt</span><span class="sxs-lookup"><span data-stu-id="5d113-123">PEX Endpoint</span></span>

<span data-ttu-id="5d113-124">Project Operations kræver, at en projektparameter refererer til PEX-slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="5d113-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="5d113-125">Dette slutpunkt er nødvendigt for at kommunikere med den service, der bruges til at gengive arbejdsopgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5d113-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="5d113-126">Hvis parameteren ikke er aktiveret, modtager du fejlmeddelelsen "Projektparameteren er ikke gyldig".</span><span class="sxs-lookup"><span data-stu-id="5d113-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="5d113-127">Løsning</span><span class="sxs-lookup"><span data-stu-id="5d113-127">Workaround</span></span>
 ![Feltet PEX-slutpunkt på projektparameteren](media/projectparameter.png)

1. <span data-ttu-id="5d113-129">Tilføj feltet **PEX-slutpunkt** til siden **Projektparametre**.</span><span class="sxs-lookup"><span data-stu-id="5d113-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="5d113-130">Opdater feltet med følgende værdi: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="5d113-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="5d113-131">Fjern feltet fra siden **Projektparametre**.</span><span class="sxs-lookup"><span data-stu-id="5d113-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="5d113-132">Rettigheder til projekt til internettet</span><span class="sxs-lookup"><span data-stu-id="5d113-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="5d113-133">Project Operations er afhængig af en ekstern planlægningstjeneste.</span><span class="sxs-lookup"><span data-stu-id="5d113-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="5d113-134">Tjenesten kræver, at en bruger har fået tildelt flere roller og kan læse og skrive til objekter, der er relateret til arbejdsopgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5d113-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="5d113-135">Disse objekter omfatter projektopgaver, ressourcetildelinger og opgaveafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="5d113-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="5d113-136">Hvis en bruger ikke kan få vist arbejdsopgavehierarki under fanen **Opgaver**, skyldes det sandsynligvis, at projekter til Project Operations ikke er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="5d113-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="5d113-137">En bruger modtager måske enten en sikkerhedsrolle eller en fejl, der er relateret til en nægtelse af adgang.</span><span class="sxs-lookup"><span data-stu-id="5d113-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="5d113-138">Løsning</span><span class="sxs-lookup"><span data-stu-id="5d113-138">Workaround</span></span>

1. <span data-ttu-id="5d113-139">Gå til **Indstilling > Sikkerhed > Brugere > Applikationsbruger**.</span><span class="sxs-lookup"><span data-stu-id="5d113-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Applikationslæser](media/applicationuser.jpg)
   
2. <span data-ttu-id="5d113-141">Dobbeltklik på applikationsbrugerposten for at kontrollere følgende:</span><span class="sxs-lookup"><span data-stu-id="5d113-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="5d113-142">Brugeren har adgang til projektet.</span><span class="sxs-lookup"><span data-stu-id="5d113-142">The user has access to the project.</span></span> <span data-ttu-id="5d113-143">Denne verificering foretages typisk ved at sikre, at brugeren har sikkerhedsrollen **Projektleder**.</span><span class="sxs-lookup"><span data-stu-id="5d113-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="5d113-144">Microsoft Project-applikationsbrugeren findes og er konfigureret korrekt.</span><span class="sxs-lookup"><span data-stu-id="5d113-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="5d113-145">Hvis denne bruger ikke findes, kan du oprette en ny brugerpost.</span><span class="sxs-lookup"><span data-stu-id="5d113-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="5d113-146">Vælg **Nye brugere**.</span><span class="sxs-lookup"><span data-stu-id="5d113-146">Select **New Users**.</span></span> <span data-ttu-id="5d113-147">Rediger postformularen til **Applikationsbruger**, og tilføj derefter **Applikations-ID'et**.</span><span class="sxs-lookup"><span data-stu-id="5d113-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detaljer om applikationsbruger](media/applicationuserdetails.jpg)

4. <span data-ttu-id="5d113-149">Kontrollér, at brugeren er blevet tildelt den korrekte licens, og at tjenesten er aktiveret under detaljer om licensens serviceplaner.</span><span class="sxs-lookup"><span data-stu-id="5d113-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="5d113-150">Kontrollér, at brugeren kan åbne project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5d113-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="5d113-151">Kontrollér via projektparametrene, at systemet peger på det rigtige projektslutpunkt.</span><span class="sxs-lookup"><span data-stu-id="5d113-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="5d113-152">Kontroller, at projektapplikationsbrugeren er oprettet.</span><span class="sxs-lookup"><span data-stu-id="5d113-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="5d113-153">Anvend følgende sikkerhedsroller på brugeren:</span><span class="sxs-lookup"><span data-stu-id="5d113-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="5d113-154">Dataverse-bruger</span><span class="sxs-lookup"><span data-stu-id="5d113-154">Dataverse User</span></span>
  - <span data-ttu-id="5d113-155">Systemet Project Operations</span><span class="sxs-lookup"><span data-stu-id="5d113-155">Project Operations System</span></span>
  - <span data-ttu-id="5d113-156">Projektsystem</span><span class="sxs-lookup"><span data-stu-id="5d113-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="5d113-157">Fejl under opdatering af arbejdsopgavehierarkiet</span><span class="sxs-lookup"><span data-stu-id="5d113-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="5d113-158">Når der foretages en eller flere opdateringer af arbejdsopgavehierarkiet, mislykkes ændringerne i sidste ende, og de gemmes ikke.</span><span class="sxs-lookup"><span data-stu-id="5d113-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="5d113-159">Der opstår en fejl i planlægningsgitteret med teksten "Den seneste ændring, du har foretaget, kunne ikke gemmes".</span><span class="sxs-lookup"><span data-stu-id="5d113-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="5d113-160">Løsning</span><span class="sxs-lookup"><span data-stu-id="5d113-160">Workaround</span></span>

1. <span data-ttu-id="5d113-161">Kontrollér, at brugeren er blevet tildelt den korrekte licens, og at tjenesten er aktiveret under detaljer om licensens serviceplaner.</span><span class="sxs-lookup"><span data-stu-id="5d113-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="5d113-162">Kontrollér, at brugeren kan åbne project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5d113-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="5d113-163">Kontrollér, at systemet peger på det rigtige projektslutpunkt.</span><span class="sxs-lookup"><span data-stu-id="5d113-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="5d113-164">Kontroller, at projektapplikationsbrugeren er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="5d113-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="5d113-165">Anvend følgende sikkerhedsroller på brugeren:</span><span class="sxs-lookup"><span data-stu-id="5d113-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="5d113-166">Dataverse-bruger eller basisbruger</span><span class="sxs-lookup"><span data-stu-id="5d113-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="5d113-167">Systemet Project Operations</span><span class="sxs-lookup"><span data-stu-id="5d113-167">Project Operations System</span></span>
  - <span data-ttu-id="5d113-168">Projektsystem</span><span class="sxs-lookup"><span data-stu-id="5d113-168">Project System</span></span>
  - <span data-ttu-id="5d113-169">Dobbeltskrivningssystemet til Project Operations (denne rolle er nødvendig, hvis du installerer det ressourcebaserede/ikke-lagerbaserede scenario for Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="5d113-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]