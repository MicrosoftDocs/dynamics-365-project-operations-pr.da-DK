---
title: Opdater Project Operations i dit Finance-miljø
description: Dette emne indeholder oplysninger om, hvordan du opdaterer Project Operations i dit Dynamics 365 Finance-miljø.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291972"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="5188b-103">Opdater Project Operations i dit Finance-miljø</span><span class="sxs-lookup"><span data-stu-id="5188b-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="5188b-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="5188b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="5188b-105">Dette emne indeholder oplysninger om, hvordan du opdaterer Dynamics 365 Project Operations i dit Dynamics 365 Finance-miljø.</span><span class="sxs-lookup"><span data-stu-id="5188b-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="5188b-106">Det kræver tre procedurer at opdatere Project Operations til opdatering 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="5188b-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="5188b-107">Importér pakken til dit eksempelprojekt</span><span class="sxs-lookup"><span data-stu-id="5188b-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="5188b-108">Anvend opdateringen</span><span class="sxs-lookup"><span data-stu-id="5188b-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="5188b-109">Opdater dit Dataverse-miljø</span><span class="sxs-lookup"><span data-stu-id="5188b-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="5188b-110">Importér pakken til dit LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="5188b-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="5188b-111">Log på [Lifecycle Services (LCS)](https://lcs.dynamics.com/) som projektejer eller miljøadministrator.</span><span class="sxs-lookup"><span data-stu-id="5188b-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="5188b-112">Vælg dit LCS-projekt fra listen over projekter.</span><span class="sxs-lookup"><span data-stu-id="5188b-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="5188b-113">På siden **Projekt** skal du i gruppen **Miljø** åbne det miljø, som du ønsker at opdatere.</span><span class="sxs-lookup"><span data-stu-id="5188b-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="5188b-114">Kontrollér, at miljøet kører.</span><span class="sxs-lookup"><span data-stu-id="5188b-114">Verify that the environment is running.</span></span> <span data-ttu-id="5188b-115">Start miljøet, hvis det ikke er startet.</span><span class="sxs-lookup"><span data-stu-id="5188b-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="5188b-116">I afsnittet **Ny udgivelse** under **Tilgængelige opdateringer** skal du vælge **Se opdatering** for 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="5188b-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Knappen Se opdatering](media/view-update.png)

6. <span data-ttu-id="5188b-118">På siden **Binære opdateringer** skal du vælge **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="5188b-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="5188b-119">På siden **Gennemse og gem opdateringer** skal du vælge **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="5188b-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="5188b-120">I ruden **Gem pakke i aktivbibliotek**, der åbnes, skal du angive pakkens navn og derefter vælge **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="5188b-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="5188b-121">Når LCS er færdig med at gemme pakken, aktiveres knappen **Udført**.</span><span class="sxs-lookup"><span data-stu-id="5188b-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="5188b-122">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="5188b-122">Select **Done**.</span></span> <span data-ttu-id="5188b-123">LCS kontrollerer pakken.</span><span class="sxs-lookup"><span data-stu-id="5188b-123">LCS will verify the package.</span></span> <span data-ttu-id="5188b-124">Det kan tage et par minutter eller op til en time at kontrollere.</span><span class="sxs-lookup"><span data-stu-id="5188b-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="5188b-125">Anvend pakkeopdateringen</span><span class="sxs-lookup"><span data-stu-id="5188b-125">Apply the package update</span></span>

1. <span data-ttu-id="5188b-126">I LCS skal du på siden **Miljødetaljer** vælge **Vedligehold** > **Anvend opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="5188b-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="5188b-127">Markér den pakke, du har gemt tidligere, på listen, og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="5188b-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="5188b-128">Vælg **Ja** for at bekræfte, at du vil installere pakken.</span><span class="sxs-lookup"><span data-stu-id="5188b-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Dialogboksen Bekræft pakkeudrulning](media/confirm-package-deployment.png)

4. <span data-ttu-id="5188b-130">Vælg **Ja** for at bekræfte, at du vil opdatere applikationen.</span><span class="sxs-lookup"><span data-stu-id="5188b-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Dialogboksen Bekræft opdatering af applikation](media/confirm-application-update.png)

<span data-ttu-id="5188b-132">Udrulningen og opdateringen af applikationen starter.</span><span class="sxs-lookup"><span data-stu-id="5188b-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="5188b-133">På siden **Miljødetaljer** opdateres miljøstatus til **Servicering** i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="5188b-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="5188b-134">Om ca. to timer er opdateringen gennemført.</span><span class="sxs-lookup"><span data-stu-id="5188b-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="5188b-135">Oplysningerne om programudgivelsen opdateres til **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**, og miljøstatussen opdateres til **Udrullet**.</span><span class="sxs-lookup"><span data-stu-id="5188b-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="5188b-136">Opdater dit Dataverse-miljø</span><span class="sxs-lookup"><span data-stu-id="5188b-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="5188b-137">Log på [Power Platform Administration](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="5188b-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="5188b-138">I listen skal du finde og åbne det miljø, som du anvendte til at installere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5188b-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="5188b-139">På siden **Miljøer** skal du vælge **Ressource** > **Dynamics 365-applikationer**.</span><span class="sxs-lookup"><span data-stu-id="5188b-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="5188b-140">Du skal finde **Microsoft Dynamics 365 Project Operations** på listen og derefter i kolonnen **Status** vælge **Tilgængelig opdatering**.</span><span class="sxs-lookup"><span data-stu-id="5188b-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="5188b-141">Markér afkrydsningsfeltet **Jeg accepterer servicebetingelserne**, og vælg derefter **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="5188b-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="5188b-142">Den nyeste version af løsningen installeres.</span><span class="sxs-lookup"><span data-stu-id="5188b-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="5188b-143">Når installationen er fuldført, er versionen 4.5.0.134 blevet installeret.</span><span class="sxs-lookup"><span data-stu-id="5188b-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="5188b-144">Konfigurer nye funktioner</span><span class="sxs-lookup"><span data-stu-id="5188b-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="5188b-145">Aktiver tilknytning med dobbelt skrivning</span><span class="sxs-lookup"><span data-stu-id="5188b-145">Enable dual-write mapping</span></span>

<span data-ttu-id="5188b-146">Når du har fuldført opdateringen i Finance- og Dataverse-miljøerne, kan du aktivere de påkrævede tilknytninger med dobbelt skrivning.</span><span class="sxs-lookup"><span data-stu-id="5188b-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="5188b-147">Følg følgende procedurer for at aktivere tilknytninger med dobbelt skrivning.</span><span class="sxs-lookup"><span data-stu-id="5188b-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="5188b-148">Opdater sikkerhedsindstillinger i Customer Engagement-miljøet</span><span class="sxs-lookup"><span data-stu-id="5188b-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="5188b-149">Opdater dataobjekter</span><span class="sxs-lookup"><span data-stu-id="5188b-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="5188b-150">Opdater og kør tilknytninger med dobbelt skrivning</span><span class="sxs-lookup"><span data-stu-id="5188b-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="5188b-151">Opdater sikkerhedsindstillinger i Dataverse-miljøet</span><span class="sxs-lookup"><span data-stu-id="5188b-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="5188b-152">Følgende opdateringer af sikkerhedsrettighederne for objekter er påkrævet som en del af opdateringen til UR5.</span><span class="sxs-lookup"><span data-stu-id="5188b-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="5188b-153">I dit Dataverse-miljø skal du gå til **Indstillinger**, og i gruppen **System** skal du vælge **Sikkerhed**.</span><span class="sxs-lookup"><span data-stu-id="5188b-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse-miljøindstillinger](media/Picture21.png)

2. <span data-ttu-id="5188b-155">Vælg **Sikkerhedsroller**.</span><span class="sxs-lookup"><span data-stu-id="5188b-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="5188b-156">I listen med roller skal du vælge **applikationsbruger med dobbeltskrivning** og vælge fanen **Brugerdefinerede objekter**.</span><span class="sxs-lookup"><span data-stu-id="5188b-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="5188b-157">Kontrollér, at rollen har tilladelserne **Læse** og **Tilføj til** for:</span><span class="sxs-lookup"><span data-stu-id="5188b-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="5188b-158">**Type af valutakurs**</span><span class="sxs-lookup"><span data-stu-id="5188b-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="5188b-159">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="5188b-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="5188b-160">**Regnskabskalender**</span><span class="sxs-lookup"><span data-stu-id="5188b-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="5188b-161">**Hovedbog**</span><span class="sxs-lookup"><span data-stu-id="5188b-161">**Ledger**</span></span>

5. <span data-ttu-id="5188b-162">Når sikkerhedsrollen er opdateret, skal du gå til **Indstillinger** > **Sikkerhed** > **Teams**.</span><span class="sxs-lookup"><span data-stu-id="5188b-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="5188b-163">Kontrollér, at rollen **applikationsbruger med dobbeltskrivning** er blevet anvendt på teamet.</span><span class="sxs-lookup"><span data-stu-id="5188b-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="5188b-164">Opdater dataobjekter fra opdateringen</span><span class="sxs-lookup"><span data-stu-id="5188b-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="5188b-165">I dit Finance-miljø skal du åbne arbejdsområdet **Dataadministration**, og derefter åbne siden **Rammeparametre**.</span><span class="sxs-lookup"><span data-stu-id="5188b-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="5188b-166">På fanen **Objektindstillinger** skal du vælge **Opdater objektliste**.</span><span class="sxs-lookup"><span data-stu-id="5188b-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="5188b-167">Vælg **Luk** for at bekræfte opdatering af objektet.</span><span class="sxs-lookup"><span data-stu-id="5188b-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="5188b-168">Processen tager ca. 20 minutter at gennemføre.</span><span class="sxs-lookup"><span data-stu-id="5188b-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="5188b-169">Når opdateringen er fuldført, får du besked.</span><span class="sxs-lookup"><span data-stu-id="5188b-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="5188b-170">Opdater tilknytninger med dobbelt skrivning</span><span class="sxs-lookup"><span data-stu-id="5188b-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="5188b-171">I arbejdsområdet **Dataadministration** skal du vælge **Dobbeltskrivning**.</span><span class="sxs-lookup"><span data-stu-id="5188b-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="5188b-172">Vælg **Anvend løsninger**, vælg begge løsninger på listen, og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="5188b-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="5188b-173">På siden **Dobbeltskrivning** skal du vælge følgende tabeltilknytninger og derefter vælge **Stop**.</span><span class="sxs-lookup"><span data-stu-id="5188b-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="5188b-174">**Integration af faktiske oplysninger i Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="5188b-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="5188b-175">**Integration af projektomkostningskategorier i Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="5188b-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="5188b-176">**Eksport af objektet integration af faktiske projektomkostninger i Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="5188b-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="5188b-177">På siden **Tabeltilknytningsversion** skal du anvende en ny version af tilknytningen på hver af de tre objekter.</span><span class="sxs-lookup"><span data-stu-id="5188b-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="5188b-178">På siden **Dobbeltskrivning** skal du vælge kør for at genstarte tilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="5188b-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="5188b-179">Markér listet med tilknytning, vælg tilknytningen **Hovedbog (msdyn_ledgers)** med alle forudsætninger, og markér afkrydsningsfeltet **Oprindelig synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="5188b-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="5188b-180">I feltet **Master for oprindelig synkronisering** skal du vælge **Finance and Operations-applikationer** og derefter vælge **Kør**.</span><span class="sxs-lookup"><span data-stu-id="5188b-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synkronisering af tilknytning i hovedbog](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]