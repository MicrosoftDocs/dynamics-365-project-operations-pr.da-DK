---
title: Klargør et nyt miljø
description: Dette emne indeholder oplysninger om, hvordan du klargør et nyt Project Operations-miljø.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121166"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="8d8fd-103">Klargør et nyt miljø</span><span class="sxs-lookup"><span data-stu-id="8d8fd-103">Provision a new environment</span></span>

<span data-ttu-id="8d8fd-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="8d8fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8d8fd-105">Dette emne indeholder oplysninger om, hvordan du klargør et nyt Dynamics 365 Project Operations-miljø for ressource-/ikke-lagerbaserede scenarier.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="8d8fd-106">Aktivér automatisk klargøring af Project Operations i et LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="8d8fd-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="8d8fd-107">Benyt følgende fremgangsmåde for at aktivere den automatiserede klargøring af Project Operations for dit LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="8d8fd-108">Gå til [LCS](https://lcs.dynamics.com/v2), og vælg feltet **Administration af prøveversionsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="8d8fd-109">I listen **Prøveversionsfunktion** skal du vælge **Funktionen Project Operations** og dernæst vælge **Aktiver prøveversionsfunktion** for at aktivere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8d8fd-110">Dette trin udføres kun én gang pr. LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="8d8fd-111">Klargør et Project Operations-miljø</span><span class="sxs-lookup"><span data-stu-id="8d8fd-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="8d8fd-112">Åbn en udrulning af et [demonstrationsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller [sandkasse-/produktionsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="8d8fd-113">Gennemgå guiden **Miljøklargøring**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8d8fd-114">Kontrollér, at den valgte programversion er 10.0.13 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="8d8fd-115">Hvis du vil klargøre Project Operations, skal du vælge **Avancerede indstillinger** og vælge **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="8d8fd-116">Aktiver **Common Data Service-indstillingen** ved at vælge **Ja** og derefter angive oplysninger i de påkrævede felter:</span><span class="sxs-lookup"><span data-stu-id="8d8fd-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="8d8fd-117">Navn</span><span class="sxs-lookup"><span data-stu-id="8d8fd-117">Name</span></span>
  - <span data-ttu-id="8d8fd-118">Land/område</span><span class="sxs-lookup"><span data-stu-id="8d8fd-118">Region</span></span>
  - <span data-ttu-id="8d8fd-119">Sprog</span><span class="sxs-lookup"><span data-stu-id="8d8fd-119">Language</span></span>
  - <span data-ttu-id="8d8fd-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="8d8fd-120">Currency</span></span>
 
5. <span data-ttu-id="8d8fd-121">I feltet **Common Data Service-skabelon** skal du vælge **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="8d8fd-122">Vælg miljøtypen til din udrulning.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="8d8fd-123">En abonnementsbaseret prøveversion giver dig mulighed for at installere et CDS-miljø i 30 dage.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Udrulningsindstillinger](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="8d8fd-125">Vælg **Accepter** for at bekræfte servicebetingelserne, og vælg derefter **Udfør** for at vende tilbage til udrulningsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Samtykke til udrulning](./media/2DeploymentConsent.png)

7. <span data-ttu-id="8d8fd-127">Udfyld de resterende obligatoriske felter i guiden, og bekræft udrulningen.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="8d8fd-128">Varigheden af miljøklargøring varierer afhængigt af miljøtypen.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="8d8fd-129">Klargøringen kan tage op til seks timer.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="8d8fd-130">Når udrulningen er fuldført, vises miljøet som **Udrullet**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="8d8fd-131">For at bekræfte at miljøet er blevet udrullet kan du vælge **Logon** og logge på miljøet.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detaljer for -miljø](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="8d8fd-133">Anvend demonstrationsdata til Project Operations Finance (valgfrit trin)</span><span class="sxs-lookup"><span data-stu-id="8d8fd-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="8d8fd-134">Anvend demonstrationsdata for Project Operations Finance på det i 10.0.13-serviceudgivelsen indeholdte skybaserede miljø som beskrevet i [denne artikel](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="8d8fd-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="8d8fd-135">Anvend opdateringer på Finance-miljøet</span><span class="sxs-lookup"><span data-stu-id="8d8fd-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="8d8fd-136">Project Operations kræver et Finance-miljø med programversion **10.0.13 (10.0.569.20009)** eller nyere.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="8d8fd-137">Det kan være nødvendigt at anvende kvalitetsopdateringer i dit Finance-miljø for at modtage denne version.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="8d8fd-138">I LCS skal du på siden **Miljødetaljer** i sektionen **Tilgængelige opdateringer** vælge **Vis opdatering**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Vis opdateringer](./media/5ViewUpdates.png)

2. <span data-ttu-id="8d8fd-140">På siden **Binære opdateringer** skal du vælge **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-140">On the **Binary updates** page, select **Save package.**</span></span>

![Gem pakke](./media/6SavePackage.png)

3. <span data-ttu-id="8d8fd-142">Klik på **Vælg alle** og vælg derefter **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-142">Click **Select all** and then select **Save package**.</span></span>

![Gennemse og gem opdateringer](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="8d8fd-144">Angiv et navn for og en beskrivelse af pakken, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="8d8fd-145">Afhængigt af internetforbindelsen kan denne proces tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-145">Depending on the internet connection, this process might take some time.</span></span>

![Overfør pakken til aktivbiblioteket](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="8d8fd-147">Når pakken er blevet gemt, skal du vælge **Udført** og gemme denne pakke i aktivbiblioteket i dit LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="8d8fd-148">Det kan tage op til mere end 15 minutter at gemme og validere pakken.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="8d8fd-149">Hvis du vil anvende opdateringen, skal du gå til siden med **Miljødetaljer** i LCS og vælge **Vedligehold** > **Anvend opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Vedligehold miljøer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="8d8fd-151">Vælg den pakke, du har oprettet, på listen over opdateringer, og vælg **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Anvend opdateringer](./media/10ApplyUpdates.png)

<span data-ttu-id="8d8fd-153">Det vil tage et stykke tid at vedligeholde miljøet.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-153">Environment servicing will take some time.</span></span> <span data-ttu-id="8d8fd-154">Når installationen er fuldført, vil miljøet vende tilbage til en udrullet tilstand.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-154">After it is complete, the environment will return to a deployed state.</span></span>

![Udrullet miljø](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="8d8fd-156">Opret en forbindelse til dobbelt skrivning</span><span class="sxs-lookup"><span data-stu-id="8d8fd-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="8d8fd-157">I dit LCS-projekt skal du gå til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8d8fd-158">Under **Common Data Service-miljøoplysninger** skal du vælge **Forbind til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="8d8fd-159">Når forbindelsen er oprettet, skal du vælge **Forbind til CDS for Apps** igen.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="8d8fd-160">Du bliver omdirigeret til dobbelt skrivning i Finance.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-160">You will be redirected to Dual Write in Finance.</span></span>

![Link til CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="8d8fd-162">Vælg **Anvend løsning** for at få adgang til de objekter, der skal tilknyttes i integrationen.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Anvend løsninger](./media/13ApplySolutions.png)

5. <span data-ttu-id="8d8fd-164">Vælg begge løsninger, **Dynamics 365 Finance and Operations dobbelt skrivningsobjekttilknytninger** og **Dynamics 365 Project Operations dobbelt skrivningsobjekttilknytninger**, og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Bekræft løsninger](./media/14ConfirmSolutions.png)

<span data-ttu-id="8d8fd-166">Når løsningerne er anvendt, anvendes dobbelt skrivningsobjekter på miljøet.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Anvendelse af løsninger](./media/15ApplyingSolutions.png)

<span data-ttu-id="8d8fd-168">Når objekterne er anvendt, vises alle tilgængelige tilknytninger i miljøet.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Dobbelt skrivningstilknytninger](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="8d8fd-170">Opdater dataobjekterne efter opdateringen</span><span class="sxs-lookup"><span data-stu-id="8d8fd-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="8d8fd-171">I Finance skal du gå til arbejdsområdet **Dataadministration**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-171">In Finance, go to the **Data management** workspace.</span></span>

![Arbejdsområde for Dataadministration](./media/16DataManagement.png)

2. <span data-ttu-id="8d8fd-173">Vælg feltet **Strukturparametre**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-173">Select the **Framework parameters** tile.</span></span>

![Strukturparametre](./media/17FrameworkParameters.png)

3. <span data-ttu-id="8d8fd-175">På siden **Objektindstillinger** skal du vælge **Opdater objektliste**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Opdater objektliste](./media/18RefreshEntityList.png)

<span data-ttu-id="8d8fd-177">Opdateringen tager ca. 20 minutter.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="8d8fd-178">Du modtager en besked, når den er fuldført.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-178">You will receive an alert when it is complete.</span></span>

![Opdater bekræftelse](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="8d8fd-180">Kør Project Operations dobbelt skrivningstilknytninger</span><span class="sxs-lookup"><span data-stu-id="8d8fd-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="8d8fd-181">I dit LCS-projekt skal du gå til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8d8fd-182">Under **Common Data Service-miljøoplysninger** skal du vælge **Forbind til CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="8d8fd-183">Når du har valgt forbindelsen, bliver du omdirigeret til listen over objekter i tilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="8d8fd-184">Start tilknytningerne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="8d8fd-185">Sørg for at følge rækkefølgen på listen.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="8d8fd-186">**Objekttilknytning**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-186">**Entity Map**</span></span> | <span data-ttu-id="8d8fd-187">**Opdater enhed**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-187">**Refresh entity**</span></span> | <span data-ttu-id="8d8fd-188">**Første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-188">**Initial sync**</span></span> | <span data-ttu-id="8d8fd-189">**Master til første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-189">**Master for initial sync**</span></span> | <span data-ttu-id="8d8fd-190">**Kør forudsætninger**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-190">**Run prerequisites**</span></span> | <span data-ttu-id="8d8fd-191">**Forudsætning for første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="8d8fd-192">**Projektressourceroller for alle firmaer (reserverbareressourcekategorier)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="8d8fd-193">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-193">No</span></span> | <span data-ttu-id="8d8fd-194">Ja</span><span class="sxs-lookup"><span data-stu-id="8d8fd-194">Yes</span></span> | <span data-ttu-id="8d8fd-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8d8fd-195">Common Data Service</span></span> | <span data-ttu-id="8d8fd-196">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-196">No</span></span> | <span data-ttu-id="8d8fd-197">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-197">N\A</span></span> |
| <span data-ttu-id="8d8fd-198">**Juridiske enheder (cdm\_virksomheder)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="8d8fd-199">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-199">No</span></span> | <span data-ttu-id="8d8fd-200">Ja</span><span class="sxs-lookup"><span data-stu-id="8d8fd-200">Yes</span></span> | <span data-ttu-id="8d8fd-201">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="8d8fd-201">Finance and Operations apps</span></span> | <span data-ttu-id="8d8fd-202">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-202">No</span></span> | <span data-ttu-id="8d8fd-203">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-203">N\A</span></span> |
| <span data-ttu-id="8d8fd-204">**Integration af faktiske oplysninger i Project Operations (msdyn\_faktiske oplysninger)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="8d8fd-205">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-205">No</span></span> | <span data-ttu-id="8d8fd-206">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-206">No</span></span> | <span data-ttu-id="8d8fd-207">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-207">N\A</span></span> | <span data-ttu-id="8d8fd-208">Ja</span><span class="sxs-lookup"><span data-stu-id="8d8fd-208">Yes</span></span> | <span data-ttu-id="8d8fd-209">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-209">No</span></span> |
| <span data-ttu-id="8d8fd-210">**Projekkontraktlinjer (salgsordredetaljer)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="8d8fd-211">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-211">No</span></span> | <span data-ttu-id="8d8fd-212">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-212">No</span></span> | <span data-ttu-id="8d8fd-213">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-213">N\A</span></span> | <span data-ttu-id="8d8fd-214">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-214">No</span></span> | <span data-ttu-id="8d8fd-215">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-215">No</span></span> |
| <span data-ttu-id="8d8fd-216">**Integrationsobjekt for projekttransaktionsrelationer (msdyn\_transaktionsforbindelser)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="8d8fd-217">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-217">No</span></span> | <span data-ttu-id="8d8fd-218">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-218">No</span></span> | <span data-ttu-id="8d8fd-219">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-219">N\A</span></span> | <span data-ttu-id="8d8fd-220">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-220">No</span></span> | <span data-ttu-id="8d8fd-221">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-221">N\A</span></span> |
| <span data-ttu-id="8d8fd-222">**Integration af kontraktlinjemilepæle i Project Operations (msdyn\_kontraktlinjeplanmedværdier)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="8d8fd-223">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-223">No</span></span> | <span data-ttu-id="8d8fd-224">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-224">No</span></span> | <span data-ttu-id="8d8fd-225">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-225">N\A</span></span> | <span data-ttu-id="8d8fd-226">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-226">No</span></span> | <span data-ttu-id="8d8fd-227">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-227">N\A</span></span> |
| <span data-ttu-id="8d8fd-228">**Integrationsobjekt for udgiftsestimater i Project Operations (msdyn\_estimeredelinjer)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="8d8fd-229">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-229">No</span></span> | <span data-ttu-id="8d8fd-230">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-230">No</span></span> | <span data-ttu-id="8d8fd-231">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-231">N\A</span></span> | <span data-ttu-id="8d8fd-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-232">No</span></span> | <span data-ttu-id="8d8fd-233">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-233">N\A</span></span> |
| <span data-ttu-id="8d8fd-234">**Integrationsobjekt for eksport af projektudgiftskategorier i Project Operations (msdyn\_udgiftskategorier)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="8d8fd-235">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-235">No</span></span> | <span data-ttu-id="8d8fd-236">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-236">No</span></span> | <span data-ttu-id="8d8fd-237">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-237">N\A</span></span> | <span data-ttu-id="8d8fd-238">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-238">No</span></span> | <span data-ttu-id="8d8fd-239">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-239">N\A</span></span> |
| <span data-ttu-id="8d8fd-240">**Integrationsobjekt for eksport af projektudgifter i Project Operations (msdyn\_udgifter)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="8d8fd-241">Ja</span><span class="sxs-lookup"><span data-stu-id="8d8fd-241">Yes</span></span> | <span data-ttu-id="8d8fd-242">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-242">No</span></span> | <span data-ttu-id="8d8fd-243">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-243">N\A</span></span> | <span data-ttu-id="8d8fd-244">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-244">No</span></span> | <span data-ttu-id="8d8fd-245">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-245">N\A</span></span> |
| <span data-ttu-id="8d8fd-246">**Integrationsobjekt for timeestimater i Project Operations (msdyn\_ressourcetildelinger)**</span><span class="sxs-lookup"><span data-stu-id="8d8fd-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="8d8fd-247">Ja</span><span class="sxs-lookup"><span data-stu-id="8d8fd-247">Yes</span></span> | <span data-ttu-id="8d8fd-248">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-248">No</span></span> | <span data-ttu-id="8d8fd-249">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-249">N\A</span></span> | <span data-ttu-id="8d8fd-250">Nr.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-250">No</span></span> | <span data-ttu-id="8d8fd-251">I\R</span><span class="sxs-lookup"><span data-stu-id="8d8fd-251">N\A</span></span> |


4. <span data-ttu-id="8d8fd-252">Hvis du vil opdatere objektet, skal du vælge tilknytningens navn og derefter vælge **Opdater objekter**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Opdater tilknytning](./media/20RefreshMapping.png)

5. <span data-ttu-id="8d8fd-254">Kør tilknytningen, når opdateringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="8d8fd-255">Før du aktiverer næste tilknytning, skal du kontrollere, at tilknytningen i tabellen er i tilstanden **Kører**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="8d8fd-256">Det kan tage et stykke tid at køre tilknytningerne med et større antal forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="8d8fd-257">Hvis du vil køre en tilknytning med forudsætninger, skal du aktivere funktionen **Vis relaterede objekttilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="8d8fd-258">Hvis tabellen indikerer, at **Indledende synkronisering af forudsætning** er **Nej**, skal du kontrollere, at flaget for den **Indledende synkronisering** er **Slået fra** i alle de påkrævede tilknytninger, før du kører programmet.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kør tilknytning](./media/21RunMap.png)

6. <span data-ttu-id="8d8fd-260">Valider, at alle projektrelaterede tilknytninger er i kørselstilstand.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-260">Validate all project related maps are in the running state.</span></span>

![Alle tilknytninger kører](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="8d8fd-262">Anvend konfigurationsdata i CDS for Project Operations (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="8d8fd-262">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="8d8fd-263">Hvis du har anvendt demodata i Finance-miljøet, skal du se [Konfigurere og anvende konfigurationsdata i Common Data Service til Project Operations](resource-apply-pro-setup-config-data.md) for at anvende demodata i CDS-miljøer.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-263">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="8d8fd-264">Dit Project Operations-miljø er nu klargjort og konfigureret.</span><span class="sxs-lookup"><span data-stu-id="8d8fd-264">Your Project Operations environment is now provisioned and configured.</span></span> 
