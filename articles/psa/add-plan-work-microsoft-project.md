---
title: Brug tilføjelsesprogrammet Project Service til at planlægge dit arbejde i Microsoft Project | MicrosoftDocs
description: Denne emne indeholder oplysninger om, hvordan du kan tilføje, konfigurere og bruge Microsoft Project-tilføjelsesprogrammet til Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074302"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="dcd0c-103">Brug tilføjelsesprogrammet Project Service Automation til at planlægge dit arbejde i Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="dcd0c-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="dcd0c-104">gør det lettere for dig at foretage din projektplanlægning, herunder estimater.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="dcd0c-105">Du kan definere arbejdet, så omkostninger, indsats og salgsværdi kan ses, når det endelige forslag er sendt.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="dcd0c-106">Nu kan du installere [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] og foretage dit planlægningsarbejde i det velkendte miljø i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="dcd0c-107">Brug de effektive planlægnings- og styringsfunktioner i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og opdater derefter din projektplan i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="dcd0c-108">Hvis du vil bruge funktionen dokumentstyring i SharePoint til at gemme dine [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekter, skal din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-administrator slå dokumentstyring til.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="dcd0c-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] er kun kompatibel med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="dcd0c-110">Hent og installer tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-110">Download and install the add-in</span></span>  
 <span data-ttu-id="dcd0c-111">Hav dine [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-logonoplysninger ved hånden.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="dcd0c-112">Du skal bruge disse oplysninger til at oprette forbindelse fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="dcd0c-113">I Download Center kan du hente tilføjelsesprogrammet til din understøttede version af Project Service, enten [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="dcd0c-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="dcd0c-114">Klik på downloadlinket.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-114">Click the download link.</span></span>  

3.  <span data-ttu-id="dcd0c-115">Når overførslen er fuldført, skal du klikke på **Ja** for at installere tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="dcd0c-116">Konfigurer tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-116">Configure the add-in</span></span>  

1. <span data-ttu-id="dcd0c-117">Åbn [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og klik på fanen **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="dcd0c-118">Klik på **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="dcd0c-119">Angiv dine logonoplysninger, og klik derefter på **Log på**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="dcd0c-120">Nu kan du gå i gang med at bruge tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="dcd0c-121">Læs fra en skabelon</span><span class="sxs-lookup"><span data-stu-id="dcd0c-121">Read from a template</span></span>  
 <span data-ttu-id="dcd0c-122">Læs fra en skabelon, du har oprettet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] og kopieret til [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], for at starte projektplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dcd0c-123">[Opret en projektskabelon (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="dcd0c-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="dcd0c-124">Fra fanen **Project Service** skal du klikke på **Læs** > **Project Service Automation-projektskabelon**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="dcd0c-125">Vælg en skabelon på listen, og klik derefter på **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="dcd0c-126">De opgaver, der kopieres fra skabelonen til projektet, er som standard manuelt planlagte.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="dcd0c-127">Tildel [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller til projektressourcer</span><span class="sxs-lookup"><span data-stu-id="dcd0c-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="dcd0c-128">Åbn et projekt, og klik på båndet **Opgave**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="dcd0c-129">Klik på menuen **Gantt-diagram** , og vælg derefter **Ressourceark**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="dcd0c-130">Klik på rullemenuen **Project Service-ressourcerolle** på ressourcearket, og vælg en Project Service Automation-rolle.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="dcd0c-131">Tildel personaleressourcer til projektet</span><span class="sxs-lookup"><span data-stu-id="dcd0c-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="dcd0c-132">Vælg en række under fanen Project Service, og klik på **Find ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="dcd0c-133">På skærmen **Reservér ressource** skal du vælge den ressource, du vil bruge til projektet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="dcd0c-134">Klik på **Reserver** , og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="dcd0c-135">Udgiv dit projekt</span><span class="sxs-lookup"><span data-stu-id="dcd0c-135">Publish your project</span></span>  
<span data-ttu-id="dcd0c-136">Når projektplanlægningen er afsluttet, er næste trin at importere og udgive projektet til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="dcd0c-137">Projektet importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="dcd0c-138">Processen til generering af pris og team anvendes.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="dcd0c-139">Åbn projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for at se, at gruppen, projekt estimaterne og arbejdsopgavehierarkiet er blevet genereret.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="dcd0c-140">I følgende tabel vises, hvor du kan finde resultaterne:</span><span class="sxs-lookup"><span data-stu-id="dcd0c-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="dcd0c-141">**Gantt-diagrammer**</span><span class="sxs-lookup"><span data-stu-id="dcd0c-141">**Gantt Chart**</span></span>   | <span data-ttu-id="dcd0c-142">Importeres i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Arbejdsopgavehierarki** -skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="dcd0c-143">**Ressourceark**</span><span class="sxs-lookup"><span data-stu-id="dcd0c-143">**Resource Sheet**</span></span> |   <span data-ttu-id="dcd0c-144">Importeres i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Medlemmer af projektteam** -skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="dcd0c-145">**Bruge anvendelse**</span><span class="sxs-lookup"><span data-stu-id="dcd0c-145">**Use Usage**</span></span>    |    <span data-ttu-id="dcd0c-146">Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektestimater** -skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="dcd0c-147">**Sådan importerer og udgiver du projektet**</span><span class="sxs-lookup"><span data-stu-id="dcd0c-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="dcd0c-148">Fra fanen **Project Service** skal du klikke på **Udgiv** > **Nyt Project Service Automation-projekt**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="dcd0c-149">I dialogboksen **Publicer til et nyt projekt i Project Service** skal du angive **Projektnavn** og vælge **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="dcd0c-150">Du kan også markere **Sammenkæd projektplan med Project Service Automation** for at sammenkæde planens projektfil med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="dcd0c-151">Klik på **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-151">Click **Publish**.</span></span>  

   <span data-ttu-id="dcd0c-152">Hvis projektfilen sammenkædes med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], bliver projektfilen master, og den angiver arbejdsopgavehierarkiet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] til skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="dcd0c-153">Hvis du vil foretage ændringer i projektplanen, skal du foretage dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og udgive dem som opdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="dcd0c-154">Rediger et projekt, der er blevet importeret</span><span class="sxs-lookup"><span data-stu-id="dcd0c-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="dcd0c-155">Hvis du vil foretage ændringer i en projektplan, der er importeret i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], har du to muligheder:</span><span class="sxs-lookup"><span data-stu-id="dcd0c-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="dcd0c-156">Åbn masterfilen, og rediger den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="dcd0c-157">Fjern sammenkædning til filen, og rediger den direkte i Project Service.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="dcd0c-158">Som standard er et projekt, der er overført fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], låst og kan kun redigeres i Project.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="dcd0c-159">Hvis du vil redigere filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], skal sammenkædningen til filen være fjernet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="dcd0c-160">Redigere i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="dcd0c-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="dcd0c-161">I hovedmenuen skal du klikke på **Project Service** > **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="dcd0c-162">Åbn det projekt, du har oprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], på listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="dcd0c-163">Klik på **Åbn i MS Project** fra båndet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="dcd0c-164">Derved åbnes den sammenkædede masterfil i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="dcd0c-165">Fjern sammenkædning til en fil, og rediger den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="dcd0c-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="dcd0c-166">I hovedmenuen skal du klikke på **Project Service** > **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="dcd0c-167">Åbn det projekt, du har oprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], på listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="dcd0c-168">Klik på **Fjern link til MS Project** fra båndet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="dcd0c-169">Sende en Project-fil til SharePoint eller Office Grupper</span><span class="sxs-lookup"><span data-stu-id="dcd0c-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="dcd0c-170">Du kan overføre Project-filen til SharePoint og finde den under de tilknyttede dokumenter for dit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="dcd0c-171">Du skal bede din administrator om at konfigurere dokumentstyring i SharePoint og aktivere det for Project-enheden.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="dcd0c-172">Du kan også overføre Project-filen til [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], hvis du har konfigureret Office Groups.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="dcd0c-173">Uploade en fil til SharePoint</span><span class="sxs-lookup"><span data-stu-id="dcd0c-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="dcd0c-174">I hovedmenuen skal du klikke på **Project Service** > **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="dcd0c-175">Vælg **Til Project Service Automation-projektdokumenter**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="dcd0c-176">I dialogboksen **Aktiver Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** skal du vælge **Ja** eller **Nej**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="dcd0c-177">Hvis du klikker på **Ja** , kan du vælge knappen **Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation, starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og indlæse Project-filen fra SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="dcd0c-178">Hvis du klikker på **Nej** virker linket for knappen **Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ikke.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="dcd0c-179">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen findes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det specifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="dcd0c-180">Overfør en fil til Office Groups</span><span class="sxs-lookup"><span data-stu-id="dcd0c-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="dcd0c-181">I hovedmenuen skal du klikke på **Project Service** > **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="dcd0c-182">Vælg **Til Project Service Automation-projektdokumenter**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="dcd0c-183">I dialogboksen **Aktiver Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** skal du vælge **Ja** eller **Nej**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="dcd0c-184">Hvis du klikker på **Ja** , kan du vælge knappen **Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation, starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og indlæse Project-filen fra SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="dcd0c-185">Hvis du klikker på **Nej** virker linket for knappen **Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ikke.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="dcd0c-186">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen findes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det specifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="dcd0c-187">Udgiv et projekt som en skabelon</span><span class="sxs-lookup"><span data-stu-id="dcd0c-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="dcd0c-188">Du kan gemme dit projekt og genbruge det ved at gemme det som en projektskabelon i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="dcd0c-189">Projektskabeloner er projektplaner, der kan genbruges i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dcd0c-190">[Opret en projektskabelon (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="dcd0c-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="dcd0c-191">Fra fanen **Project Service** skal du klikke på **Udgiv** > **Ny Project Service Automation-projektskabelon**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="dcd0c-192">I dialogboksen **Publicer til et nyt projekt i Project Service-skabelon** skal du angive **Navn på projektskabelon**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="dcd0c-193">Du kan også markere **Sammenkæd projektplan med Project Service Automation** for at sammenkæde projektfilen med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="dcd0c-194">Klik på **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-194">Click **Publish**.</span></span>  

<span data-ttu-id="dcd0c-195">Hvis projektfilen sammenkædes med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], bliver projektfilen master, og den angiver arbejdsopgavehierarkiet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-skabelonen til skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="dcd0c-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="dcd0c-196">Hvis du vil foretage ændringer i projektplanen, skal du foretage dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og udgive dem som opdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="dcd0c-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="dcd0c-197">Se også</span><span class="sxs-lookup"><span data-stu-id="dcd0c-197">See Also</span></span>  
 [<span data-ttu-id="dcd0c-198">Vejledning til projektledere</span><span class="sxs-lookup"><span data-stu-id="dcd0c-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)